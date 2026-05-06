---
hl-publish: true
---
The **Cauchy distribution** is a real, continuous, univariate [[Probability distribution]]. For a [[Random variable]] $X$, the [[Probability density function]] is
$$f_{X}(x)=\frac{1}{\pi} \frac{1}{1+x^{2}}$$
It has no parameters.

The shape is similar to that of the [[Gaussian distribution]], but the Cauchy distribution has heavier tails and is considerably less well-behaved. In fact, it is often studied specifically because of its difficult properties as a pathological case of probability distribution.
### Moments
The [[moment-generating function]] does not exist. The [[characteristic function]] does and should be used in its place. All [[function moments]] either diverge or are undefined.

The [[expected value]] is
$$\text{E}[X]=\int_{-\infty}^{\infty} \frac{1}{\pi} \frac{x}{1+x^{2}} \ dx =\frac{1}{\pi} \frac{1}{2}\ln(1+x^{2})|_{\infty}^{\infty}=\text{undefined}$$
Thus, the Cauchy distribution has no expected value. The [[variance]] is
$$\text{var}(X)=\int_{-\infty}^{\infty} \frac{1}{\pi} \frac{x^{2}}{1+x^{2}} \ dx \to \infty$$
which tends to infinity.[^1] Notably, the lack of a well-defined expectation and variance imply that [[Chebyshev's inequality]] does not hold and neither does the [[central limit theorem]].
### Properties
- It is symmetrical around $x=0$.
- The sum of Cauchy-distributed [[iid]] variables is itself a Cauchy distribution.
### Relation to other distributions
- The ratio $Y=\frac{X_{1}}{X_{2}}$ of two [[Gaussian distribution|standard-normal]] iid variables $X_{1},X_{2}\sim \mathcal{N}(0,1)$ is a Cauchy distribution.
- A [[Student's t distribution]] with one [[Degrees of freedom|degree of freedom]] is a Cauchy distribution.
- The [[Breit-Wigner distribution]] used in [[particle]] physics is a form of the Cauchy distribution.

[^1]: This is somewhat improper notation. Formally, the integral should go from $-\infty$ to $a$, then in the limit $a\to \infty$ the integral goes to infinity.
