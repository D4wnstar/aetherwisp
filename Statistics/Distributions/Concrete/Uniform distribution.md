---
hl-publish: true
---
The **uniform distribution** is a continuous [[Probability distribution]] with constant [[Probability]] over an interval. For an interval $(a,b)$, the [[Probability density function]] of a uniform [[Random variable]] $X$ is
$$f_{X}(x)=\begin{cases}
c & \text{if }x\in (a,b) \\
0 & \text{if }x\notin(a,b)
\end{cases}$$
It is also possible to define a discrete uniform distribution over $n$ possible outcomes as a simple [[probability mass function]]:
$$p_{X}(x)=\frac{1}{n}$$
The discrete version is a simple mathematical description of a set of $n$ possibilities that are all equally likely to happen. For example, a fair coin toss is a discrete uniform distribution with $n=2$, while a fair $n$-sided die is, unsurprisingly, the same but with $n$ outcomes.

The continuous version is often used as a placeholder distribution when lacking information. For instance, if the main error on a measurement is due to tool precision constraints ([[absolute error]] $\Delta X$), a uniform distribution is used to model what possible values the measured variable could take in the $2\Delta X$ interval.
### Moments
The raw and central [[Moment-generating function|Moment-generating function]] are
$$M^{*}_{X}(t)=\frac{1}{t(b-a)}(e^{bt}-e^{at}),\qquad M_{X}(t)=\frac{1}{t(b-a)}(e^{(b-a)t/2}-e^{-(b-a)t/2})$$
The [[Function moments|moments]] are:
- Raw
	0. $\mu_{0}^{*}=1$
	1. $\mu_{1}^{*}=\frac{a+b}{2}$ ([[mean]])
- Central
	0. $\mu_{0}=1$
	1. $\mu_{1}=0$
	2. $\mu_{2}=\frac{(b-a)^{2}}{12}$ ([[Variance]])
	3. $\mu_{3}=0$
	4. $\mu_{4}=\frac{(b-a)^{4}}{80}$
- Coefficients
	0. $\gamma_{1}=0$ ([[skewness]], it is symmetrical around the mean)
	1. $\gamma_{2}=- 6/5$ ([[kurtosis]])
### Properties
It is [[Normalization|normalized]] by $c=1/(b-a)$.