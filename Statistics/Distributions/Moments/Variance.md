---
wiki-publish: true
aliases:
  - Bessel correction
  - sample variance
---
The **variance** $\sigma ^{2}$ of a [[Random variable]] $X$ is a measure of its [[statistical dispersion]]. It is defined as the [[Expected value]] of the square of the deviation from the population [[mean]] $\mathrm{E}[X]=\mu$:
$$\text{var}(X)\equiv\sigma ^{2}_{X}=\mathrm{E}[(X-\mu)^{2}]$$
The variance can also be expressed as
$$\begin{align}
\text{var}(X)&=\mathrm{E}[(X-\mathrm{E}[X])^{2}] \\
&=\mathrm{E}[X^{2}-2X\mathrm{E}[X]+\mathrm{E}[X]^{2}] \\
&=\mathrm{E}[X^{2}]-2\mathrm{E}[X]\mathrm{E}[X]+\mathrm{E}[X]^{2} \\
&=\mathrm{E}[X^{2}]-\mathrm{E}[X]^{2} \\
&=\mathrm{E}[X^{2}]-\mu ^{2}
\end{align}$$
Or as the [[Covariance]] of a variable with itself
$$\text{var}(X)=\text{cov}(X,X)$$
The primary draw of variance as a measure of dispersion is that it is mathematically convenient to use in calculations and to derive results with. For instance, [[Chebyshev's inequality]] forces constraints onto what values the variable can take depending on its variance. Furthermore, it is the second central [[function moments|function moment]] of a [[probability distribution]].

The square root of variance is the [[standard deviation]]: $\sqrt{ \sigma ^{2} }=\sigma$. The variance is (approximately) related to the [[absolute error]] $\Delta$ by $\sigma ^{2}=\Delta ^{2}/3$.
## Definitions
### Discrete random variable
Given a discrete random variable $X$ with [[Probability mass function]] $p_{X}(x)$ of expected value $\mu$, the variance is
$$\text{var}(X)=\sum_{i=1}^{n} p_{X}(x_{i})(x_{i}-\mu)^{2}$$
### Continuous random variable
Given a continuous random variable $X$ with [[Probability density function]] $f_{X}(x)$ of expected value $\mu$, the variance is
$$\text{var}(X)=\int_{-\infty}^{+\infty}f_{X}(x)(x-\mu)^{2}\ dx$$
or equivalently
$$\text{var}(X)=\int_{-\infty}^{+\infty}x^{2}f_{X}(x)\ dx-\mu ^{2}$$
### Multiple variables
The variance is not defined for multiple variables (see instead [[Covariance]]). However, it is possible to find the variance of one variable among many from the [[joint distribution function]].

For $N$ continuous random variables $X_{1},\ldots,X_{N}$ with JDF $f(x_{1},\ldots,x_{N})$, the variance of $X_{i}$ is
$$\text{var}(X_{i})= \mathrm{E}[(X_{i}-\mu_{i})^{2}]=\int_{\Omega_{N}}\ldots \int_{\Omega_{1}}(x_{i}-\mu_{i})^{2}f(x_{1},\ldots,x_{N})dx_{1}\ldots dx_{N}$$
where $\mu_{i}=\mathrm{E}[X_{i}]$ is the expected value of $X_{i}$.
### Sample variance
By definition, calculating the true variance requires knowing the true mean $\mu$. This is often not the case, so the true mean must be substituted by its [[estimator]]: the [[Arithmetic mean|sample mean]]. For a random [[sample]] of [[independent variables]] $X_{1},\ldots,X_{N}$, we can look for the average of the square deviations from the sample mean $\bar{X}$:
$$S^{2}_\text{biased}=\frac{1}{N}\sum_{i=1}^{N} (X_{i}-\bar{X})^{2}$$
This is known as the **sample variance** and is an estimator of the true variance. However, in this form, it is imperfect. Similarly to the variance of the sample mean, it is a *biased* estimator of the true variance $\sigma ^{2}$. To fix the bias, we apply **Bessel's correction** (changing $N$ to $N-1$):
$$S^{2}=\frac{1}{N-1}\sum_{i=1}^{N} (X_{i}-\bar{X})^{2}$$
This is the unbiased sample variance and is the appropriate estimator for the true variance in most cases.[^1] Its expected value is, in fact, $\mathrm{E}[S^{2}]=\sigma ^{2}$.
## Properties
- If $X_{1},\ldots,X_{N}$ are [[independent variables]], the variance of the sum is the sum of the variances: $\text{var}\left( \sum_{i=1}^{N}X_{i} \right)=\sum_{i=1}^{N}\text{var}(X_{i})$. Also, it is linear with respect to constant scaling: $\text{var}\left( a\sum_{i=1}^{N}X_{i} \right)=a^{2}\text{var}\left( \sum_{i=1}^{N}X_{i} \right)$.
## Propagation of variance
It is common for a quantity $w$ to be dependent on other quantities $x,y,\ldots$ according to some function $w(x,y,\ldots)$. If we take the variables $x,y,\ldots$ to be independent of each other, the variance of $w$ is expressed by the **law of propagation of variance**:
$$\boxed{\begin{align}
\text{var}(w)&=\sum_{x_{i}=x,y,\ldots}\left( \frac{ \partial w }{ \partial x_{i} }  \right)^{2}\text{var}(x_{i}) \\
&=\left( \frac{ \partial w }{ \partial x }  \right)^{2}\text{var}(x)+\left( \frac{ \partial w }{ \partial y }  \right)^{2}\text{var}(y)+\ldots
\end{align}}$$
For this to work, $w$ must be twice-[[Differential|differentiable]] in all of its arguments. This is a special case (and an approximation nonetheless) of the general properties of [[functions of random variables]].

[^1]: But not all. Bias is far from the only problem to consider in choosing an estimator. $S^{2}_\text{biased}$ actually has legitimate use cases, as it has lower variance than unbiased $S^{2}$, at the cost of missing the mark due to the bias. In fact, if using $S^{2}$ over $S^{2}_\text{biased}$ causes estimates to go all over the place due to the higher variance, the little gain from removing bias is probably not enough to offset that, so you end up with worse estimates despite using the unbiased estimator. This usually happens when the sample size $N$ is small, when adding a bit of bias is often an acceptable price to pay to reduce variance.
