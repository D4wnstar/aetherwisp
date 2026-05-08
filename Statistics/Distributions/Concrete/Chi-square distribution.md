---
hl-publish: true
---
The **chi-square distribution** or **$\chi ^{2}$ distribution** is a real, continuous [[Probability distribution]] over $\Omega\equiv[0,\infty)$. For a [[Random variable]] $X$, the [[Probability density function]] is
$$f_{X}(x;k)=\frac{1}{\Gamma\left( \frac{k}{2} \right)} \frac{1}{2^{k/2}}x^{k/2 -1}e^{-x/2}$$
where $k\geq1$ is an integer parameter called the **[[degrees of freedom]]** of the distribution and $\Gamma$ is the [[Gamma function]].

Its most common application is for [[hypothesis test|hypothesis testing]], specifically [[Chi-square test|chi-square tests]]. Moreover, since $\chi ^{2}$ distributions arise from the sum of squares of [[Gaussian distribution|Gaussian distributions]], the square [[norm]] of any [[Vector space|vector]] whose components follow a Gaussian is $\chi ^{2}$.
### Moments
The raw [[moment-generating function]] is
$$\begin{align}
M_{X}^{*}(t)=\mathrm{E}[e^{tX}]&=\frac{1}{2^{k/2}\Gamma\left( \frac{k}{2} \right)}\int_{0}^{\infty}e^{tx}x^{k/2-1}e^{-x/2}\ dx \\
&=\frac{1}{2^{k/2}\Gamma\left( \frac{k}{2} \right)}\Gamma\left( \frac{k}{2} \right) \frac{1}{2^{-k/2}}(1-2t)^{-k/2} \\
&=(1-2t)^{-k/2}
\end{align}$$
which is similar to the [[Exponential distribution]] MGF. The central MGF is
$$M_{X}(t)=e^{-tk}(1-2t)^{-k/2}$$
We can substitute $Y=\frac{X-k}{\sqrt{ 2k }}$. With this, the raw MGF becomes
$$M_{Y}^{*}(t)=e^{t^{2}/2}$$
which is the [[Gaussian distribution|standard normal distribution]]'s MGF.

Some [[Function moments|moments]] are:
- Raw
	0. $\mu_{0}^{*}=1$
	1. $\mu_{1}^{*}=k$ ([[Expected value]])
- Central
	0. $\mu_{0}=1$
	1. $\mu_{1}=0$
	2. $\mu_{2}=2k$ ([[Variance]])
	3. $\mu_{3}=8k$
	4. $\mu_{4}=12k^{2}+48k$
- Coefficients
	1. $\gamma_{1}=2 \sqrt{ \frac{2}{k} }$ ([[skewness]], it peaks at low values and tapers off to the right, becomes symmetrical for $k\to \infty$)
	2. $\gamma_{2}=\frac{12}{k}$ ([[kurtosis]], goes to zero for $k\to \infty$)
### Relation to other distributions
- It is a special case of the [[Gamma distribution]] with $\alpha=k/2$ and $\beta=2$.
- It follows the [[central limit theorem]]: if $k\gg 1$, the $\chi ^{2}_{k}$ approximately becomes a [[Gaussian distribution]] $\mathcal{N}(k,2k)$.
- It is related to the [[Maxwell-Boltzmann distribution]] (see [[#In molecular velocity analysis]]).
#### As sum of $\chi ^{2}$ distributions
The sum of $N$ [[Independent variables|independent]] variables $X_{i}\sim \chi ^{2}_{k_{i}}$ is itself a $\chi ^{2}$ distribution with degrees of freedom equal to the sum of all individual degrees:
$$Y=\sum_{i=1}^{N} X_{i}\sim \chi ^{2}_{k_{1}+\ldots+k_{N}}$$

> [!quote]- Proof
> The joint MGF of a sum of [[independent variables]] is the product of MGFs:
> $$M_{Y}^{*}(t)=\prod_{i=1}^{N} M_{X}^{*}(t)=\prod_{i=1}^{N} (1-2t)^{-k_{i}/2}=(1-2t)^{-\left( \sum_{i=1}^{N} k_{i} \right)/2}=(1-2t)^{-k/2}$$
> where $k=\sum_{i=1}^{N}k_{i}$. This is the MGF of a $\chi ^{2}_{k}$ distribution.
#### As sum of square Gaussian distributions
As a particularly interesting case, a $\chi ^{2}$ distribution is the result of the sum of squares of Gaussian distributions. Given a set of $N$ [[iid]] normally-distributed variables $\{ X_{1},\ldots,X_{N} \}$, the sum of their squares $Y=\sum_{i=1}^{N}X_{i}^{2}$ is chi-square-distributed with $N$ degrees of freedom, $Y\sim \chi ^{2}_{N}$. As Gaussian RVs are quite common, the $\chi ^{2}$ distribution tends to appear frequently even if there is no individual phenomenon that follows it.

> [!quote]- Proof for standard normals
> Say $X_{1},\ldots,X_{N}$ all independently follow $\mathcal{N}(0,1)$. Then $X_{1}^{2},\ldots,X_{N}^{2}$ all follow $\chi ^{2}_{1}$; for proof see [[Functions of random variables#Distribution, expectation, variance|here]]. But then $Y$ is a sum of $\chi ^{2}_{1}$ distributions. Using the proof above, we can state that $Y\sim \chi ^{2}_{N}$.

> [!quote]- Extension to any normal
> Say $X_{1},\ldots,X_{N}$ independently follow $\mathcal{N}(\mu_{i},\sigma ^{2}_{i})$. Then $(X_{i}-\mu_{i})/\sigma_{i}$ follow $\mathcal{N}(0,1)$. Then, the sum of these squares is $\chi_{N}^{2}$ as per the previous point. Therefore in general
> $$Y=\sum_{i=1}^{N} \frac{(X_{i}-\mu_{i})^{2}}{\sigma ^{2}_{i}}\sim \chi_{N}^{2}$$
> This is the basis behind the $\chi ^{2}$ hypothesis tests.
> 
> If $X_{1},\ldots,X_{N}$ are dependent, then it can be proven (in a much more involved manner) that the quantity that follows a $\chi ^{2}_{N}$ distribution is
> $$Y=(\mathbf{X}-\boldsymbol{\mu})^{T}\Sigma^{-1}(\mathbf{X}-\boldsymbol{\mu})\sim \chi_{N}^{2}$$
> where $\Sigma$ is the [[Covariance|covariance matrix]] of $X_{1},\ldots,X_{N}$. The proof involves finding that, as long as $\Sigma$ is not singular, there always exists an orthogonal [[transformation]] that allows changing from $X_{1},\ldots,X_{N}$ correlated variables to $\tilde{X}_{1},\ldots,\tilde{X}_{N}$ independent variables, then reusing the above proof.
### In molecular velocity analysis
The chi-square distribution can be used to derive a statistical description of the motion of molecules in a gas. Consider a gas of identical molecules each with velocity $\mathbf{v}=(v_{1},v_{2},v_{3})\in \mathbb{R}^{3}$. Each component of each $\mathbf{v}$ is considered a normally-distributed random variable with parameters $N(0,\sigma ^{2})$. We can define the scale-independent variable $\mathbf{q}$ as $\mathbf{q}=\mathbf{v}/\sigma=(q_{1},q_{2},q_{3})$, the components of which are also normally distributed but following the standard normal $N(0,1)$ instead. The square [[Norma|norm]] of $\mathbf{q}$, $\lvert \mathbf{q} \rvert^{2}\equiv q^{2}=q_{1}^{2}+q_{2}^{2}+q_{3}^{2}$ is therefore chi-squared-distributed with 3 degrees of freedom: $\chi ^{2}_{3}$. The probability density function for $q^{2}$ thus is
$$f(q^{2})=\frac{1}{\sqrt{ 2\pi }}(q^{2})^{1/2}e^{-q^{2}/2}$$
and therefore the one for $v^{2}$ is, by substitution,
$$g(v^{2})=\frac{1}{\sqrt{ 2\pi }}\left( \frac{v^{2}}{\sigma ^{2}} \right)^{1/2}e^{-v^{2}/2\sigma ^{2}} \frac{1}{\sigma ^{2}}=\frac{1}{\sqrt{ 2\pi }} \frac{v}{\sigma ^{3}}e^{-v^{2}/2\sigma ^{2}}$$
and for $v$ we get
$$h(v)=g(v^{2})2v=\frac{2}{\sqrt{ 2\pi }}\frac{v^{2}}{\sigma ^{3}}e^{-v^{2}/2\sigma ^{2}}$$
This is called the [[Maxwell-Boltzmann distribution]] and is used for modeling stochastic motion at molecular or atomic scale. It can be found that $\sigma=k_{B}T/m$ where $k_{B}$ is the [[Boltzmann constant|Boltzmann constant]], $T$ is the gas temperature and $m$ is the mass of the molecules.