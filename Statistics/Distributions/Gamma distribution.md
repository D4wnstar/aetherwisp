---
wiki-publish: true
---
The **gamma distribution** is a real continuous [[probability distribution]] defined by two parameters, $\alpha$ and $\beta$. For a [[random variable]] $X$, the [[probability density function]] is
$$f_{X}(x;\alpha,\beta)=\frac{1}{\beta^{\alpha}\Gamma(\alpha)}x^{\alpha-1}e^{-x/\beta}$$
where $\Gamma$ is the [[Gamma function]].

![[Gamma_distribution_pdf.svg]]

It is a very general distribution that has applications in many fields, such as modeling wait times in queue theory. Specific cases of this distribution are themselves well-known: for $\alpha=k$ and $\beta=1$, we find the [[Erlang distribution]], for $\alpha=k/2$ and $\beta=2$ we get the [[chi-square distribution]], and for $\alpha=1$ and $\beta=\tau$ we get the [[exponential distribution]].
### Moments
The [[expected value]] is
$$E[X]=\alpha \beta$$
and the [[variance]] is
$$\text{var}(X)=\alpha \beta ^{2}$$
### Properties
It is [[Normalization|normalized]] with a constant of $c=1$.