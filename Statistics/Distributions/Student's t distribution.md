---
wiki-publish: true
---
The **Student's $t$ distribution** is a real, continuous [[probability distribution]] commonly used in statistical inference. Given a [[Gaussian distribution|standard-normal]]-distributed [[random variable]] $Z\sim \mathcal{N}(0,1)$ and a [[Chi-square distribution|chi-square]]-distributed one $X\sim \chi ^{2}_{n}$, the [[probability density function]] is
$$T=\frac{Z}{\sqrt{ X/n }}$$
$Z$ may follow a more general [[Gaussian distribution]], though that is considered to be an extension of the $t$ distribution.

The $t$ distribution differs from the more usual Gaussian because it has much heavier tails, meaning there is less of a focus on the center. As the $\chi ^{2}$ distribution, when $n$ grows large the $t$ distribution converges back to a Gaussian. $n\simeq 30$ is a good practical number where the $t$ distribution becomes a good approximation of a Gaussian.

It's most useful when the amount of available data is small or when outliers are present.
### Relation to other distributions
If $n=1$, the tails are as heavy as the distribution allows: in this case it's known as the [[Cauchy distribution]].