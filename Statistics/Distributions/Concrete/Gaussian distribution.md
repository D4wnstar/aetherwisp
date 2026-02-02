---
wiki-publish: true
aliases:
  - normal distribution
  - standard normal distribution
---
The **Gaussian distribution** or **normal distribution** is a real univariate continuous [[Probability distribution]]. For a [[Random variable]] $X$, the [[Probability density function]] is
$$f_{X}(x;\mu,\sigma ^{2})=\frac{1}{\sqrt{ 2\pi \sigma^{2} }}e^{- \frac{(x-\mu)^{2}}{2\sigma ^{2}}}$$
where $\mu$ is the [[Expected value]] e $\sigma ^{2}$ is the [[Variance]].

A **standard normal distribution** is defined as a normal distribution with $\mu=0$ and $\sigma ^{2}=1$:
$$f_{X}(x;0,1)=\frac{1}{\sqrt{ 2\pi }}e^{-x^{2}/2}$$
### Moments
The central and raw [[Moment-generating function]] for the Gaussian are
$$M_{X}(t)=\text{E}[e^{t(X-\mu)}]=e^{\sigma ^{2}t^{2}/2},\qquad M_{X}^{*}(t)=e^{t\mu}M_{X}(t)=e^{t\mu+t^{2}\sigma ^{2}/2}$$
For a standard normal distribution, they simplify to
$$M_{X}(t)=e^{t^{2}/2}=M_{X}^{*}(t)$$

> [!quote]- Proof
> Use the definition of central MGF:
> $$M_{X}(t)=\text{E}[e^{t(X-\mu)}]=\frac{1}{\sqrt{ 2\pi }\sigma}\int_{-\infty}^{+\infty}e^{t(x-\mu)}e^{-(x-\mu)^{2}/2\sigma ^{2}}dx$$
> Combine exponentials:
> $$e^{t(x-\mu)}e^{-(x-\mu)^{2}/2\sigma ^{2}}=e^{t(x-\mu)-(x-\mu)^{2}/2\sigma ^{2}}$$
> Use the following identity:
> $$\begin{align}
> t(x-\mu)-\frac{(x-\mu)^{2}}{2\sigma ^{2}}&=t(x-\mu)- \frac{(x-\mu)^{2}}{2\sigma ^{2}}+ \frac{\sigma ^{2}t^{2}}{2}- \frac{\sigma ^{2}t^{2}}{2} \\
> &=\left[- \frac{(x-\mu)^{2}}{2\sigma ^{2}}+ t(x-\mu)- \frac{\sigma ^{2}t^{2}}{2} \right]+ \frac{\sigma ^{2}t^{2}}{2} \\
> \left( \text{extract } \frac{-1}{2\sigma ^{2}} \right)&=- \frac{1}{2\sigma ^{2}}[(x-\mu)^{2}- 2\sigma ^{2}t(x-\mu)+\sigma^{4}t^{2}]+ \frac{\sigma ^{2}t^{2}}{2} \\
> (\text{recognize square})&=- \frac{1}{2\sigma ^{2}}[(x-\mu)-\sigma ^{2}t]^{2}+ \frac{\sigma ^{2}t^{2}}{2} \\
> &=\frac{\sigma ^{2}t^{2}}{2}- \frac{(x-\mu+\sigma ^{2}t)^{2}}{2\sigma ^{2}}
> \end{align}$$
> Substitute in the integral:
> $$M_{X}(t)=\frac{1}{\sqrt{ 2\pi }\sigma}e^{\sigma ^{2}t^{2}/2}\int_{-\infty}^{+\infty}e^{-(x-\mu-\sigma ^{2}t)^{2}/2\sigma ^{2}}dx$$
> This is a [[Gaussian integral]] with $a=1/2\sigma ^{2}$ and $b=-\mu-\sigma ^{2}t$. Gaussian integrals are equal to $\sqrt{ \pi/a }$ so
> $$M_{X}(t)=\frac{1}{\sqrt{ 2\pi }\sigma}e^{\sigma ^{2}t^{2}/2} \sqrt{ 2\pi }\sigma=e^{\sigma ^{2}t^{2}/2}$$
> The raw MGF follows immediately by
> $$M_{X}^{*}(t)=e^{t\mu}M_{X}(t)=e^{t\mu+\sigma ^{2}t^{2}/2}$$
> For a standard normal $\mathcal{N}(0,1)$ we then have
> $$M_{X}(t)=M_{X}^{*}(t)=e^{t^{2}/2}$$

Some [[Function moments|moments]] are:
- Raw
	0. $\mu_{0}^{*}=1$
	1. $\mu_{1}^{*}=\mu$ ([[Expected value]])
- Central
	0. $\mu_{0}=1$
	1. $\mu_{1}=0$
	2. $\mu_{2}=\sigma ^{2}$ ([[Variance]])
	3. $\mu_{3}=0$
	4. $\mu_{4}=3\sigma^{4}$
- Coefficients
	1. $\gamma_{1}=0$ ([[skewness]], it is symmetrical around the mean)
	2. $\gamma_{2}=0$ ([[kurtosis]])

These moments have particular significance, as the Gaussian distribution is the gold standard of distributions. It is extremely common, well-understood and well-behaved, so other distributions and their moments are frequently compared to it to get an idea of how they behave. For kurtosis in particular, negative values can be seen as "flatter than Gaussian" and positive ones as "more peaked than Gaussian."
### As sum of normal variables
A sum of [[independent variables]] $X_{i}$ that are normally distributed is itself a normal distribution:
$$Y=\sum_{i=1}^{n} X_{i}$$
and its MGF is the sum of all the MGF over $x$:
$$M_{Y}^{*}(t)=\prod_{i=1}^{n}M_{X}^{*}(t)$$
Let's consider a set of normal variables $\{X_{i}\}_{i}$ that are all normally distributed with mean $\mu$ and [[Variance]] $\sigma ^{2}$. As the number of variables $n$ goes to infinity, the sum distribution goes like
$$N\left( \mu, \frac{\sigma ^{2}}{n} \right)$$
so the deviation tends to go to zero. Now let's consider the variable
$$z=\frac{\bar{x}-\mu}{\frac{\sigma}{\sqrt{ n }}}$$
where $\bar{x}=\frac{1}{n}\sum_{i=1}^{N}x_{i}$. This follows a standard normal distribution.


$$z= \frac{\sum_{i}x_{i}-n\mu}{\sigma \sqrt{ n }}=\sum_{i=1}^{n} \frac{x_{i}-\mu}{\sigma\sqrt{ n }}=\sum_{i=1}^{n} z_{i}$$
