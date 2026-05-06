---
hl-publish: true
---
The **gamma distribution** is a real continuous [[Probability distribution]] defined by a shape parameters $\alpha$ and a scale parameter $\tau$. For a [[Random variable]] $X$, the [[Probability density function]] is
$$f_{X}(x;\alpha,\tau)=\frac{1}{\Gamma(\alpha)} \frac{1}{\tau^{\alpha}}x^{\alpha-1}e^{-x/\tau}$$
where $\Gamma$ is the [[Gamma function]]. Both $\alpha$ and $\tau$ are positive real numbers. Equivalently, it can be parameterized as
$$f(x;\alpha,\lambda)=\frac{1}{\Gamma(\alpha)}\lambda^{\alpha}x^{\alpha-1}e^{-\lambda x}$$
where $\lambda$ is a positive real rate parameter. The two are related by $\lambda=1/\tau$.

It is a very general distribution that has applications in many fields, such as modeling wait times in queue theory, polymer chemistry and more. It is most often used with specific parameters to form more specific distributions; see [[#Relation to other distributions]] below.
### Moments
The central and raw [[moment-generating function]] for the Gaussian are
$$M_{X}^{*}(t)=(1-\tau t)^{-\alpha},\qquad M_{X}(t)=e^{-t\alpha \tau}(1-\tau t)^{-\alpha}$$
The [[expected value]] is
$$E[X]=\alpha \tau$$
and the [[variance]] is
$$\text{var}(X)=\alpha \tau ^{2}$$
### Relation to other distributions
Specific cases of this distribution are themselves well-known and more often used.
- For $\alpha=1$ and any $\tau$, we get an [[Exponential distribution]], $\text{Exp}(x;\tau)$.[^1]
- For integer $\alpha$ and any $\tau$, we get an [[Erlang distribution]], $\text{Erlang}(x;\alpha,\tau)$.
- For positive integer $\alpha$ and $\tau=2$, we get a [[Chi-square distribution]] with $2\alpha$ degrees of freedom, $\chi ^{2}_{2\alpha}(x)$.

[^1]: Take care with the parameterization. A "scale parameter" $\Gamma$ distribution maps to a "scale parameter" exponential or Erlang. Similarly, rate parameter maps to rate parameter.
