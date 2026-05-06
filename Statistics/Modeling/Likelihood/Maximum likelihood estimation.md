---
hl-publish: true
aliases:
  - MLE
  - binned maximum likelihood
---
**Maximum likelihood estimation** (**MLE**) is a [[parameter estimation]] method that uses the [[likelihood]] function to determine accurate [[Estimator|estimators]] of the parameters of a statistical [[Statistics/Modeling/Model|model]] by finding which parameters maximize the likelihood.

Given a likelihood function $\mathcal{L}(\boldsymbol{\theta};\mathbf{x})$ for a set of parameter $\boldsymbol{\theta}=(\theta_{1},\ldots,\theta_{M})$ on a realized [[sample]] $\mathbf{x}=(x_{1},\ldots,x_{N})$, the most credible point estimates $\boldsymbol{\theta}^{*}=(\theta_{1}^{*},\ldots,\theta_{M}^{*})$ of the parameters are the values for which the likelihood function is maximized. Formally, it's the set of parameters for which:
$$\begin{cases}
\dfrac{ \partial \mathcal{L} }{ \partial \theta_{1} } &=0 \\
&\vdots \\
\dfrac{ \partial \mathcal{L} }{ \partial \theta_{M} } &=0
\end{cases}\quad\text{and}\quad\begin{cases}
\dfrac{ \partial ^{2} \mathcal{L} }{ \partial ^{2} \theta_{1} } &<0 \\
&\vdots \\
\dfrac{ \partial ^{2} \mathcal{L} }{ \partial ^{2} \theta_{M} } &<0
\end{cases}$$
These are sometimes called the **likelihood equations**. The log-likelihood $\log \mathcal{L}$ can be substituted for $\mathcal{L}$, as the maximum is found for the same parameters. This is almost always done because it simplifies calculations by hand and restrains numerical range on a computer.

Maximum likelihood estimators carry remarkable properties. Under very general conditions, they can be proven to be consistent, asymptotically unbiased, asymptotically efficient and asymptotically [[Gaussian distribution|Gaussian]]. Often, but not always, some these properties are always true instead of just asymptotically. They are popular choices, especially for large sample sizes where the asymptotic properties are verified.
### Analytical solution
For some simpler [[Probability distribution|probability distributions]], the method is analytically tractable. One such case is the [[exponential distribution]].

> [!example]- Exponential distribution
> Consider a sample $T_{1},\ldots,T_{N}$ of $N$ [[iid]] [[random variable|random variables]] following an exponential distribution with scale parameter $\tau$, with [[Probability density function|PDF]]
> $$f(t;\tau)=\frac{1}{\tau}e^{-t/\tau}$$
> The likelihood function for $\tau$ on a realized sample $\mathbf{t}=(t_{1},\ldots,t_{N})$ is
> $$\mathcal{L}(\tau;\mathbf{t})=\prod_{i=1}^{N} \frac{1}{\tau}e^{-t_{i}/\tau}$$
> and its logarithm is
> $$\log \mathcal{L}=-N\log \tau- \frac{1}{\tau}\sum_{i=1}^{N} t_{i}$$
> Taking the derivative for $\tau$ and setting it to zero yields
> $$\frac{d\log\mathcal{L}}{d\tau}=- \frac{N}{\tau}+ \frac{1}{\tau ^{2}}\sum_{i=1}^{N}t_{i}=0 $$
> This is true for the specific value $\hat{\tau}^{*}$ for which
> $$\frac{1}{\hat{\tau}^{*}}\sum_{i=1}^{N} t_{i}=N\quad\Rightarrow \quad \hat{\tau}^{*}=\frac{1}{N}\sum_{i=1}^{N} t_{i}$$
> Thus, the best estimator of $\tau$ according to maximum likelihood is the [[Arithmetic mean|sample mean]], which we know to be an unbiased estimator with $\mathrm{E}[\hat{\tau}]=\tau^{}$. The second derivative can be proven to be negative, so this is indeed the maximum of $\mathcal{L}$.
> 
> We can also prove that it is a minimum-variance estimator. The [[Cramer-Rao inequality]] is saturated when
> $$\frac{ \partial \log \mathcal{L} }{ \partial \tau } =k(\hat{\tau}-\tau)$$
> where $k$ is either constant or a function of $\tau$. Using our derivative of $\log \mathcal{L}$ we can extract $N/\tau$ to find:
> $$\frac{ \partial \log \mathcal{L} }{ \partial \tau } =\frac{N}{\tau}\left( -1+ \frac{1}{\tau N}\sum_{i=1}^{N} t_{i} \right)=\frac{N}{\tau}\left( -1+ \frac{\hat{\tau}}{\tau} \right)=\frac{N}{\tau ^{2}}(\hat{\tau}-\tau)$$
> Since $k=N/\tau ^{2}$, the property is verified.
### Series expansion
Solving the system analytically is not always possible. Thankfully, the behavior of the log-likelihood can be expressed through a [[Taylor series|Taylor series]] around the best point estimate:[^1]
$$\log \mathcal{L}(\theta)=\log \mathcal{L}(\theta^{*})+ \frac{d\log \mathcal{L}}{d\theta}(\theta^{*})(\theta-\theta^{*})+ \frac{1}{2} \frac{d^{2}\log \mathcal{L}}{d\theta}(\theta^{*})(\theta-\theta^{*})^{2}+\ldots$$
The first term is the maximum, whereas the second vanishes due to being a [[Punto critico|stationary point]]. The third term can be expressed using a inverted, saturated [[Cramer-Rao inequality]] so that we're left with
$$\log \mathcal{L}(\theta)\simeq \log \mathcal{L}_{\text{max}}- \frac{1}{2} \frac{(\theta-\theta^{*})^{2}}{\sigma^{2}_{\theta^{*}}}$$
and so the likelihood itself is approximately
$$\mathcal{L}(\theta)\simeq \mathcal{L}_\text{max}e^{- (\theta-\theta^{*})^{2}/2\sigma^{2}_{\theta^{*}}}$$
This can be used, for instance, for numerical maximization algorithms, as it is often not possible to find the analytical form of the likelihood. The important part is that this is only valid near the maximum, so selecting where the maximum search is conducted is important. Notice also that this is essentially a Gaussian distribution: proof that maximum likelihood estimators are asymptotically Gaussian.

More generally, the $N$-dimensional expression can be shown to follow a [[multivariate normal distribution]] and use the [[Covariance|covariance matrix]] $\Sigma$:
$$\mathcal{L}(\boldsymbol{\theta})\simeq \mathcal{L}_\text{max}e^{- \frac{1}{2}(\boldsymbol{\theta}-\boldsymbol{\theta}^{*})\Sigma_{\theta^{*}}^{-1}(\boldsymbol{\theta}-\boldsymbol{\theta}^{*})}$$

There is also another useful conclusion from this for numerical purposes. From the $\log \mathcal{L}(\theta)$ expression, notice that when $\theta-\theta^{*}=\pm \sigma_{\theta^{*}}$, it evaluates to $\log \mathcal{L}(\theta)=\log \mathcal{L}_\text{max}-1/2$. In other words, you can numerically search for the value of $\theta$ for which this is true and that's the value $1\sigma$ away from the mean. This lets you also get an estimate of the [[standard deviation]]  Similarly, when $\log \mathcal{L}(\theta)=\log \mathcal{L}_\text{max}-2$, you find the value $2\sigma$ away and so on.
### Binned maximum likelihood
It's possible to use the histogram bin amounts instead of the actual sampled values to run MLE. This is called **binned maximum likelihood** (**BML**), as opposed to **unbinned maximum likelihood** (**UML**). Consider an [[iid]] sample $X_{1},\ldots,X_{N}$ of common [[Probability density function|PDF]] $f(x;\boldsymbol{\theta})$ which is binned into the approximate distribution $g(n_{1},\ldots,n_{M};\boldsymbol{\theta})$ when represented as a histogram. $n_{i}$ is the amount of samples occupying the $i$-th bin. The occupations are well-approximated by [[multinomial distribution]], which we use as our likelihood
$$\mathcal{L}(\boldsymbol{\theta};\mathbf{n})=g(\mathbf{n};\boldsymbol{\theta})=\frac{N!}{n_{1}!\ldots n_{M}!}p_{1}^{n_{1}}\ldots p_{M}^{n_{M}}$$
with logarithm
$$\log \mathcal{L}(\boldsymbol{\theta};\mathbf{n})=c+\sum_{i=1}^{N} n_{i}\log p_{i}(\boldsymbol{\theta})$$
where $c$ is a constant combinatorial factor. Since it's constant, it can be safely ignored as it doesn't change where the maximum is located.

Despite not looking like it, this function still depends on $\boldsymbol{\theta}$ because it's hidden in the $p_{i}$. The [[probability]] $p_{i}$ of falling in the $i$-th bin can be found by taking the difference of [[Cumulative distribution function|CDF]] at the bin edges $x_{i}$ and $x_{i+1}$. As an analytically simpler approximation, it's also the PDF calculated in the midpoint $x_{i}^{*}$ times the bin width $\Delta_{i}$, if it's thin enough:[^2]
$$p_{i}=F\left( x_{i+1} \right)-F\left( x_{i} \right) \simeq f(x_{i}^{*};\boldsymbol{\theta})\Delta_{i}$$
You can then run the optimization algorithm on the binned likelihood instead.

> [!example]- Exponential distribution (BML)
> Consider an iid sample $X_{1},\ldots,X_{N}$ of exponential random variables. A realized sample can be binned into a histogram with observed bins $n_{1},\ldots,n_{M}$ with expected bin counts given by a multinomial distribution. For an exponential distribution, the bin probabilities are, with the midpoint approximation
> $$p_{i}=f\left( x_{i}^{*};\tau \right)=\frac{1}{\tau}e^{ - x_{i}^{*}/\tau }\Delta_{i}$$
> So the logarithm of the likelihood is (ignoring $c$)
> $$\log \mathcal{L}=\sum_{i=1}^{M} n_{i}\log p_{i}(\boldsymbol{\theta})=\sum_{i=1}^{M} n_{i}\left( \log \frac{1}{\tau}- \frac{x_{i}^{*}}{\tau} \right)$$
> and the derivative is
> $$\frac{d\log \mathcal{L}}{d\tau}=\sum_{i=1}^{M} n_{i}\left( - \frac{1}{\tau}+ \frac{x_{i}^{*}}{\tau ^{2}} \right)=- \frac{N}{\tau}+ \frac{1}{\tau ^{2}}\sum_{i=1}^{M} n_{i}x_{i}^{*}=0$$
> which is true for
> $$\tau^{*}=\frac{1}{N}\sum_{i=1}^{M} n_{i}x_{i}^{*}$$
> which is, again, the sample mean, but on the histogram.

[^1]: For brevity, $\mathcal{L}(\theta;\mathbf{x})\equiv \mathcal{L}(\theta)$.

[^2]: Though on a computer there's almost no reason to use this approximation, as you can just calculate the CDF numerically, at least for one-dimensional histograms. For multi-dimensional histograms, you'd have to numerically integrate the JDF over the bin area/volume/[[hyperrectangle]], which can get computationally expensive, so in that case the approximation might be fine as a time-saving measure.
