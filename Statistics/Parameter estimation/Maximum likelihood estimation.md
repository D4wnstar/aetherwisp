---
wiki-publish: true
aliases:
  - MLE
  - binned maximum likelihood
---
**Maximum likelihood estimation** (**MLE**) is a [[parameter estimation]] method that uses the [[likelihood]] function to determine the most accurate [[Estimator|point estimate]], specifically by finding the maximum of the likelihood.

Given a likelihood function $\mathcal{L}(x_{1},\ldots,x_{n};\theta_{1},\ldots,\theta_{m})$ for a set of parameter $\theta_{1},\ldots,\theta_{m}$ and a [[sample]] $\{ x_{i} \}_{i\in \mathbb{N}}$, the most accurate point estimates $\theta_{1}^{*},\ldots,\theta_{m}^{*}$ are the values for which the following system of derivatives is verified:
$$\left\{\begin{align}
\frac{ \partial \mathcal{L} }{ \partial \theta_{1} } &=0 \\
\vdots& \\
\frac{ \partial \mathcal{L} }{ \partial \theta_{m} } &=0
\end{align}\right.$$

Since $\mathcal{L}$ and $\ln \mathcal{L}$ share maxima, it is common to attempt to maximize $\ln \mathcal{L}$ instead since it makes the expression easier to solve.
### Approximation
The behavior of the logarithm can be shown through a [[Serie di Taylor|Taylor series]] around the best point estimate:
$$\ln \mathcal{L}(\theta)=\ln \mathcal{L}(\theta^{*})+ \frac{d\ln \mathcal{L}}{d\theta}(\theta^{*})(\theta-\theta^{*})+ \frac{1}{2} \frac{d^{2}\ln \mathcal{L}}{d\theta}(\theta^{*})(\theta-\theta^{*})^{2}+\ldots$$
The first terms is the maximum, whereas the second vanishes due to being a [[Punto critico|stationary point]]. The third term can be expressed using a inverted, saturated [[Kramer-Rao-Frechet inequality]] so that we're left with
$$\ln \mathcal{L}(\theta)\simeq \ln \mathcal{L}_{\text{max}}- \frac{1}{2} \frac{(\theta-\theta^{*})^{2}}{\sigma^{2}_{\theta^{*}}}$$
and so the likelihood itself is approximately
$$\mathcal{L}(\theta)\simeq \mathcal{L}_\text{max}e^{- (\theta-\theta^{*})^{2}/\sigma^{2}_{\theta^{*}}}$$
This can be used, for instance, for numerical maximization algorithms, as it is often not possible to find the analytical form of the likelihood. More generally, the $N$-dimensional expression can be shown to use the [[Covariance|covariance matrix]] $\mathrm{V}$:
$$\mathcal{L}(\boldsymbol{\theta})\simeq \mathcal{L}_\text{max}e^{- \frac{1}{2}(\boldsymbol{\theta}-\boldsymbol{\theta}^{*})\mathrm{V}_{\theta^{*}}^{-1}(\boldsymbol{\theta}-\boldsymbol{\theta}^{*})}$$
### Linear regression with standard normal
For [[linear regression]], MLE takes on a particular form. For the relation $y_{i}=mx_{i}+q$ with a sample set $\{ x_{i},y_{i} \}_{i\in \mathbb{N}}$, each following a [[Gaussian distribution|standard normal distribution]], the likelihood function is
$$\mathcal{L}(y_{1},\ldots,y_{n};m,q)=\left[ \prod_{i=1}^{n} \frac{1}{\sqrt{ 2\pi }\sigma_{i}} \right]e^{-\sum_{i=1}^{n} (y_{i}-mx_{i}-q)^{2}/2\sigma^{2}_{i}}$$
Taking the logarithm we obtain
$$\ln \mathcal{L}=\ln\left( \prod_{i=1}^{n} \frac{1}{\sqrt{ 2\pi }\sigma_{i}} \right)-\sum_{i=1}^{n} \frac{(y_{i}-mx_{i}-q)^{2}}{2\sigma^{2}_{i}}$$
We take the derivatives for both parameters to maximize
$$\begin{align}
\frac{ \partial \ln \mathcal{L} }{ \partial m } &=\sum_{i=1}^{n} \frac{x_{i}}{\sigma ^{2}_{i}}(y_{i}-mx_{i}-q) \\
\frac{ \partial \ln \mathcal{L} }{ \partial q } &=\sum_{i=1}^{n} \frac{1}{2\sigma^{2}_{i}}(y_{i}-mx_{i}-q)
\end{align}$$

### Exponential distribution
Consider a sample $\{ t_{i} \}_{1\leq i\leq n}$ for a [[random variable]] $T$ that follows an [[exponential distribution]]
$$f(t)=\frac{1}{\tau}e^{-t/\tau}$$
The likelihood function is
$$\mathcal{L}=\prod_{i=1}^{n} \frac{1}{\tau}e^{-t_{i}/\tau}$$
and its logarithm
$$\ln \mathcal{L}=-n\ln \tau-\sum_{i} \frac{t_{i}}{\tau}$$
Taking the derivative for $\tau$ we get
$$\frac{d\ln\mathcal{L}}{d\tau}=- \frac{n}{\tau}+ \frac{1}{\tau ^{2}}\sum_{i=1}^{n}t_{i}=0 $$
which is true for
$$\tau^{*}=\frac{1}{n}\sum_{i=1}^{n} t_{i},\qquad \sigma ^{2}_{t^{*}}=\frac{(\tau^{*})^{2}}{n}$$
We already know the [[mean]] $\tau^{*}$ is the best estimator, so this proves that the method works.
### Binned maximum likelihood
It's possible to use the histogram bin amounts instead of the actual sampled values to run MLE. This is called **binned maximum likelihood** (as opposed to **unbinned maximum likelihood**). To prove that it works, consider a [[Joint distribution function|joint]] exponential distribution $f(x_{1},\ldots,x_{n};\boldsymbol{\theta})$ of [[iid]] variables $(X_{1},\ldots,X_{n})$, which becomes the distribution $g(n_{1},\ldots,n_{m};\boldsymbol{\theta})$ when represented as a histogram. $n_{i}$ is the amount of samples in the $i$-th bin. This distribution is given by a multivariate [[binomial distribution]]:
$$g(n_{1},\ldots,n_{m};\boldsymbol{\theta})=\frac{n!}{n_{1}!\ldots n_{m}!}p_{1}^{n_{1}}\ldots p_{m}^{n_{m}}=\mathcal{L}$$
Each [[probability]] function $p_{i}$ is
$$p_{i}=\int_{x_{i}^{*}-\Delta_{i}/2}^{x_{i}^{*}+\Delta_{i}/2}f(x_{i};\boldsymbol{\theta})\ dx \simeq f(x_{i}^{*};\boldsymbol{\theta})\Delta_{i}=\frac{1}{\tau}e^{-x_{i}^{*}/\tau}\Delta_{i}$$
where $x_{i}^{*}$ is the center of the $i$-th bin and $\Delta_{i}$ is its width. The logarithm of the likelihood is
$$\ln \mathcal{L}=c+\sum_{i=1}^{m} n_{i}\ln p_{i}(\boldsymbol{\theta})=c'+\sum_{i=1}^{m} n_{i}\left( \ln \frac{1}{\tau}- \frac{x_{i}^{*}}{\tau} \right)$$
and the derivative is
$$\frac{d\ln \mathcal{L}}{d\tau}=\sum_{i=1}^{m} n_{i}\left( - \frac{1}{\tau}+ \frac{x_{i}^{*}}{\tau ^{2}} \right)=- \frac{1}{\tau}n+ \frac{1}{\tau ^{2}}\sum_{i=1}^{m} n_{i}n_{i}x_{i}^{*}=0$$
which is true for
$$\tau^{*}=\frac{1}{n}\sum_{i=1}^{m} n_{i}x_{i}^{*}$$
which is, again, the correct result.