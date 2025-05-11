---
wiki-publish: true
---
The **Kullback-Leibler divergence** or **KL-divergence** gives a measure of how "different" two [[probability distribution|probability distributions]] are. Given two [[random variable|random variables]] in a shared [[sample space]] $\mathcal{X}$ described by their [[probability mass function|probability mass functions]] $p(x)$ and $q(x)$, the KL-divergence is
$$D(q||p)=\sum_{x \in \mathcal{X}} q(x)\log \frac{p(x)}{q(x)} $$
or for continuous [[probability density function|probability density functions]],
$$D(q||p)=\int_{-\infty}^{\infty} p(x)\log \frac{p(x)}{q(x)} \ dx $$
### Properties
- The KL-divergence is not symmetrical: $D(q||p)\neq D(p||q)$ in general.
- It is non-negative: $D(q||p)\geq 0$. It is zero only if $p(x)=q(x)$.