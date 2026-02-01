---
wiki-publish: true
---
The **exponential distribution** is a continuous [[Probability distribution]] over non-negative reals $[0,\infty)$. For a [[Random variable]] $X$, the [[Probability density function]] is
$$f_{X}(x;\tau)=\frac{1}{\tau}e^{-x/\tau}$$
where $\tau$ is a positive real scale parameter. Equivalently, it can be parameterized as
$$f_{X}(x;\lambda)=\lambda e^{-\lambda x}$$
where $\lambda$ is also a positive real rate parameter. The two are related by $\lambda=1/\tau$.

This distribution is commonly used in physics to model the wait times of random independent events, such a [[Nuclear decay|radioactive]] or [[Particle decay|particle decay]]. $\tau$ is then usually interpreted as the characteristic time of the process. See the [[radioactive decay law]] for a related phenomenon.
### Moments
The raw and central [[Moment-generating function|moment-generating functions]] are
$$M^{*}_{X}(t)=\frac{1}{1-t\tau},\qquad M_{X}(t)=\frac{e^{-t\tau}}{1-t\tau}$$
Some [[Function moments|moments]] are:
- Raw
	0. $\mu_{0}^{*}=1$
	1. $\mu_{1}^{*}=\tau$ ([[Expected value]])
- Central
	0. $\mu_{0}=1$
	1. $\mu_{1}=0$
	2. $\mu_{2}=\tau ^{2}$ ([[Variance]])
	3. $\mu_{3}=2\tau ^{3}$
	4. $\mu_{4}=9\tau^{4}$
- Coefficients
	1. $\gamma_{1}=2$ ([[skewness]], it asymmetrical around the mean)
	2. $\gamma_{2}=6$ ([[kurtosis]])
### Relation to other distributions
- The sum of $k$ [[iid]] exponential random variables follows an [[Erlang distribution]] $\text{Erlang}(x;k,\tau)$.