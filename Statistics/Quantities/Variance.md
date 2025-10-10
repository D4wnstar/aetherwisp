---
wiki-publish: true
aliases:
  - Bessel correction
  - sample variance
---
The **variance** $\sigma ^{2}$ of a [[Random variable]] $X$ is a measure of its [[dispersion]]. It is defined as the [[expected value]] of the square of the deviation from the [[mean]] $E[X]=\mu$:
$$\text{var}(X)\equiv\sigma ^{2}_{X}=E[(X-\mu)^{2}]$$
The variance can also be expressed as
$$\begin{align}
\text{var}(X)&=E[(X-E[X])^{2}] \\
&=E[X^{2}-2XE[X]+E[X]^{2}] \\
&=E[X^{2}]-2E[X]E[X]+E[X]^{2} \\
&=E[X^{2}]-E[X]^{2}
\end{align}$$
Or as the [[Covariance]] of a variable with itself
$$\text{var}(X)=\text{cov}(X,X)$$
The primary draw of variance as a measure of dispersion is that it is mathematically convenient to use in calculations and to derive results with. For instance, [[Chebyshev's inequality]] forces constraints onto what values the variable can take depending on its variance.

The square root of variance is the [[standard deviation]]: $\sqrt{ \sigma ^{2} }=\sigma$. The variance is related to the [[absolute error]] $\Delta$ by $\sigma ^{2}=\Delta ^{2}/3$.
## Definitions
### Discrete random variable
Given a discrete random variable $X$ with [[Probability mass function]] $p_{X}(x)$ of expected value $\mu$, the variance is
$$\text{var}(X)=\sum_{i=1}^{n} p_{X}(x_{i})(x_{i}-\mu)^{2}$$
### Continuous random variable
Given a continuous random variable $X$ with [[Probability density function]] $f_{X}(x)$ of expected value $\mu$, the variance is
$$\text{var}(X)=\int_{-\infty}^{+\infty}f_{X}(x)(x-\mu)^{2}\ dx$$
or equivalently
$$\text{var}(X)=\int_{-\infty}^{+\infty}x^{2}f_{X}(x)\ dx-\mu ^{2}$$
### Population and sample variance
The term "variance" can refer to two different but closely related concept. When the analytic form of a [[Probability distribution]] is known, it is possible to calculate that distribution's variance using the formulas above. This is the "true" measure of dispersion of that distribution. However, variance may also be calculated from a dataset built from empirical observations, by finding estimates of the distribution and of the mean. This type of observed variance can be further divided into two categories: if all possible observations of the system are present, it is known as the **population variance**, whereas if only a subset of measurements are available (a [[sample]]), it is known as the **sample variance**. Typically, the amount of measurements/trials that can be taken is infinite (there is no physical limit on how many times you can toss a coin, or a die, etc...), so only the sample variance can be found experimentally. In fact, the sample variance is essentially just an estimate of the population variance, which itself behaves as the theoretical (and unreachable) variance.

When working with a set of $N$ samples $x_{1},\ldots,x_{N}$ of a random variable $X$, we can use the arithmetic [[mean]] as the expected value (the sample mean):
$$\text{E}[X]=\mu_{x}=\frac{1}{N}\sum_{i=1}^{N} x_{i}$$
Then, the sample variance is
$$\text{var}(X)=\text{E}[X]^{2}-\text{E}[X]^{2}=\frac{1}{N}\sum_{i=1}^{N} (x_{i}-\mu_{x})^{2}$$
This is an [[estimator]] of the true population variance. It is, however, imperfect. It is found that this value consistently diverges from the population variance, with the effect being more pronounced for small $N$. The mistake is that this sample variance is calculated with the sample mean instead of the population mean. This introduces some [[Estimator|bias]] into the estimator. Thankfully, it can be proven that the bias can be removed using the **Bessel correction**:
$$\boxed{\text{var}(X)=\frac{1}{N-1}\sum_{i=1}^{N}(x_{i}-\mu_{x})^{2}}$$
where we changed $N$ to $N-1$. This corrected variance is an unbiased estimator of the population variance.
## Propagation of variance
It is common for a quantity $w$ to be dependent on other quantities $x,y,\ldots$ according to some function $w(x,y,\ldots)$. If we take the variables $x,y,\ldots$ to be independent of each other, the variance of $w$ is expressed by the **law of propagation of variance**:
$$\boxed{\begin{align}
\text{var}(w)&=\sum_{x_{i}=x,y,\ldots}\left( \frac{ \partial w }{ \partial x_{i} }  \right)^{2}\text{var}(x_{i}) \\
&=\left( \frac{ \partial w }{ \partial x }  \right)^{2}\text{var}(x)+\left( \frac{ \partial w }{ \partial y }  \right)^{2}\text{var}(y)+\ldots
\end{align}}$$
For this two work, $w$ must be twice-[[Differential|differentiable]] in all of its arguments.