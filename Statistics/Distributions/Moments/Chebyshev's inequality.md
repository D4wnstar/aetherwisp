---
wiki-publish: true
---
**Chebyshev's inequality** is an inequality that sets bounds to the [[probability]] of deviation of a [[random variable]]. Given a RV $X$, Chebyshev's inequality states
$$P(\lvert X-\mu \rvert \geq \lambda \sigma)\leq \frac{1}{\lambda ^{2}}$$
where $\lambda$ is a positive real number, $\sigma$ is the [[standard deviation]] of $X$ and $\mu$ is its [[mean]]. Only the cases $\lambda>1$ is significant. When $\lambda\leq1$, then $1/\lambda ^{2}\geq 1$, which is a trivial bound since $P\leq 1$ always.

> [!quote]- Proof
> This proof is for continuous RVs. Call $f_{X}(x)$ the [[probability density function]] of $X$. Let's consider a nonnegative function $h(x)\geq 0$ defined on the [[sample space]] $\Omega$ of $X$. Now call $I=[h_\text{min},h_\text{max}]$ the interval between the minimum $h_\text{min}$ and maximum $h_\text{max}$ of $h(x)$. Call $k\geq 0$ some nonnegative value in $I$, and call $R$ the subset of $\Omega$ where $h(x)\geq k$. The mean of $h(x)$ is
> $$E[h(x)]=\int_{\Omega}h(x)f_{X}(x)\ dx\geq \int_{R}h(x)f_{X}(x)\ dx\geq k\int_{R}f_{X}(x)\ dx=kP(h(x)\geq k)$$
> and thus
> $$P(h(x)\geq k)=\frac{E[h(x)]}{k}$$
> If we call $k=\lambda ^{2}\sigma ^{2}$ and $h(x)=(x-\mu)^{2}$, we get the inequality.

This inequality says is that the probability that $X$ deviates from its mean by $\lambda \sigma$ is at most $1/\lambda ^{2}$. For instance, it states that there is at most a $1/2^{2}=0.25=25\%$ chance that $X$ assumes a value that is $2\sigma$ or higher from the mean. Seeing it the other way around, it says that at least $75\%$  of values sampled from $X$ must be within $2\sigma$ of the mean.

This inequality is almost universal: it applies to all RVs with a finite mean and [[variance]], regardless of their [[probability distribution]]. This provides universal bounds across almost all distributions, but because it's so general, it is rather imprecise compared to distribution-specific arguments. For example, this inequality states that there must be at least $0\%$, $75\%$ and $88.89\%$ of values within $1\sigma$, $2\sigma$ and $3\sigma$. The [[Gaussian distribution]] on the other hand is known to instead require a minimum of $68\%$, $95\%$ and $99.7\%$ of values within the same ranges.
