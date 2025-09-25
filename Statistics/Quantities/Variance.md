---
wiki-publish: true
---
The **variance** $\sigma ^{2}$ of a [[random variable]] $X$ is a measure of its [[dispersion]]. It is defined as the [[Expected value]] of the square of the deviation from the [[mean]] $E[X]=\mu$:
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
### Discrete random variable
Given a discrete random variable $X$ with [[probability mass function]] $p_{X}(x)$ of expected value $\mu$, the variance is
$$\text{var}(X)=\sum_{i=1}^{n} p_{X}(x_{i})(x_{i}-\mu)^{2}$$
### Continuous random variable
Given a continuous random variable $X$ with [[probability density function]] $f_{X}(x)$ of expected value $\mu$, the variance is
$$\text{var}(X)=\int_{-\infty}^{+\infty}f_{X}(x)(x-\mu)^{2}\ dx$$
or equivalently
$$\text{var}(X)=\int_{-\infty}^{+\infty}x^{2}f_{X}(x)\ dx-\mu ^{2}$$
### Theoretical and observed variance
The term "variance" can refer to two different but closely related concept. When the analytic form of a [[probability distribution]] is known, it is possible to calculate that distribution's variance using the formulas above. This is the "true" measure of dispersion of that distribution. However, variance may also be calculated from a dataset built from empirical observations, by finding estimates of the distribution and of the mean. This type of observed variance can be further divided into two categories: if all possible observations of the system are present, it is known as the **population variance**, whereas if only a subset of measurements are available, it is known as the **sample variance**. Typically, the amount of measurements/trials that can be taken is infinite (there is no physical limit on how many times you can toss a coin, or a die, etc...), so only the sample variance can be found experimentally. In fact, the sample variance is essentially just an estimate of the population variance, which itself behaves as the theoretical (and unreachable) variance.