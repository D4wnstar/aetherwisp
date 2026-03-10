---
wiki-publish: true
---
The **Kullback-Leibler divergence** or **KL-divergence** gives a measure of how "different" two [[Probability distribution|probability distributions]] are. Given two [[Random variable|random variables]] in a shared [[sample space]] $\mathcal{X}$ described by their [[Probability mass function|probability mass functions]] $p(x)$ and $q(x)$, the KL-divergence is
$$D(q||p)=\sum_{x \in \mathcal{X}} q(x)\log \frac{q(x)}{p(x)} $$
or for continuous [[Probability density function|probability density functions]],
$$D(q||p)=\int_{\mathcal{X}} q(x)\log \frac{q(x)}{p(x)} \ dx $$
### Properties
- The KL-divergence is not symmetric: $D(q||p)\neq D(p||q)$ in general.
- It is non-negative: $D(q||p)\geq 0$. It is zero only if $p(x)=q(x)$.
- It is a [[convex function]] of $q$ and $p$.
- It is sometimes called **KL-distance**, but it does not actually meet the definition of a distance (in the [[metric space]] sense) as it is not symmetric.
- It is related to [[Entropy (information theory)|information-theoretical entropy]] by $D(q||p)=\mathrm{E}_{q}[\log p]-H(q)$. Note that the [[expected value]] is with respect to $q$: it is called **cross-entropy**.

### Relation to maximum likelihood
KL-divergence is linked to [[maximum likelihood estimation]]. To see it, consider an empirical probability distribution $p_\text{emp}(x)$ that we are trying to [[Parameter estimation|fit]] to a theoretical distribution $q(x)$. We can measure the KL-divergence between the two to determine how different they are:
$$D(p_\text{emp}||q)=-H(p_\text{emp})-\mathrm{E}_{p_\text{emp}}[\log q(x)]=-H(p_\text{emp})- \underbrace{ \frac{1}{N}\sum_{i}\log q(x_{i}) }_{ \propto\text{ log-likelihood} }$$
The last term, the cross-entropy, is proportional to the log-likelihood. Therefore, we can conclude that maximum likelihood estimation is a special case of the more general technique of KL-divergence minimization.