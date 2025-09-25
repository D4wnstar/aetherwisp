---
wiki-publish: true
---
The **uniform distribution** is a continuous [[probability distribution]] with constant [[probability]] over an interval. For an interval $(a,b)$, the [[probability density function]] of a uniform [[random variable]] $X$ is
$$f_{X}(x)=\begin{cases}
c & \text{se }x\in (a,b) \\
0 & \text{se }x\notin(a,b)
\end{cases}$$

It is often used as a placeholder distribution when lacking information. For instance, if the main error on a measurement is due to tool precision constraints ([[maximum error]] $\Delta X$), a uniform distribution is used to model what possible values the measured variable could take in the $2\Delta X$ interval as there is no way of knowing a more applicable distribution.
### Moments
The algebraic and central [[moment-generating function|moment-generating function]] are
$$M^{*}_{X}(t)=\frac{1}{t(b-a)}(e^{bt}-e^{at}),\qquad M_{X}(t)=\frac{1}{t(b-a)}(e^{(b-a)t/2}-e^{-(b-a)t/2})$$

The [[Expected value]] is
$$E[X]=\int_{a}^{b}xc\ dx=\frac{a+b}{2}$$
and the [[Variance]] is
$$\text{var}(X)=\int_{a}^{b}x^{2}c\ dx-E[X]^{2}=\frac{(b-a)^{2}}{12}$$

The [[Function moments|moments]] are
0. $\mu_{0}^{*}=1$
1. $\mu_{1}^{*}=\frac{a+b}{2}$ ([[mean]])

0. $\mu_{0}=1$
1. $\mu_{1}=0$
2. $\mu_{2}=\frac{(b-a)^{2}}{12}$ ([[Variance]])
3. $\mu_{3}=0$
4. $\mu_{4}=\frac{(b-a)^{4}}{80}$

The coefficients are
1. $\gamma_{1}=0$ ([[skewness]], it is symmetrical around the mean)
2. $\gamma_{2}=- 6/5$ ([[kurtosis]])
### Properties
It is [[Normalization|normalized]] by $c=\frac{1}{b-a}$.