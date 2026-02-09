---
wiki-publish: true
aliases:
  - t-test
---
As the [[Gaussian distribution]] is ubiquitous, there exists some [[Hypothesis test|hypothesis tests]] whose entire purpose is to validate the parameters of this kind of distribution. These tests should be used when the [[sample]] is composed of [[iid]] Gaussian [[Random variable|random variables]].
### Mean test
Given a random sample $\{ X_{1},\ldots,X_{N} \}$ of Gaussian variables $X_{i}\sim \mathcal{N}(\mu,\sigma^{2})$, a classical test is to determine whether the [[mean]] $\mu$ is a specific value $\mu_{0}$:
$$\begin{cases}
H_{0}:\mu=\mu_{0} \\
H_{1}:\mu\neq \mu_{0}
\end{cases}$$
The test [[statistic]] is given by
$$T=\frac{\bar{X}-\mu_{0}}{S/\sqrt{ N }}\sim t_{N-1}$$
where $S$ is the sample [[standard deviation]]. This statistic follows a [[Student's t distribution]] $t_{N-1}$ with $N-1$ degrees of freedom when $H_{0}$ is true. Because of this, it's also called the **t-test**.

Alternatively, if $\sigma$ is known, it can be used instead of $S$. In that case, $T$ is usually called $Z$ and follows a [[Gaussian distribution|standard normal distribution]], $Z\sim \mathcal{N}(0,1)$. This test is known as a **Z-test**.

Since Gaussian (and Student's t) distributions are symmetrical around the mean, the critical region is chosen to be double-sided, as both too large and too small values of $\mu$ don't satisfy $\mu=\mu_{0}$. Given an a priori significance level $\alpha$, in the case $T\sim \mathcal{N}(0,1)$, the critical region is defined by the integrals
$$\int_{-\infty}^{-r_{\alpha/2}} \frac{e^{-r^{2}/2}}{\sqrt{ 2\pi }/\sqrt{ N }}dr=\int_{r_{\alpha/2}}^{+\infty} \frac{e^{-r^{2}/2}}{\sqrt{ 2\pi }/\sqrt{ N }}dr=\frac{\alpha}{2}$$
From this, you can find the critical region bound $r_{\alpha/2}$ for both sides. If $T\sim t_{N-1}$, simply integrate the Student's t distribution instead.

It is also possible to use $\mu>\mu_{0}$ and $\mu<\mu_{0}$ as alternative hypothesis if you want to know if $\mu$ is an over- or underestimate. In these cases, the critical region is one-sided, since the equality permits one of the two sides.
### Variance test
The premise is the same as above, except we're testing $\sigma^{2}$ instead of $\mu$:
$$\begin{cases}
H_{0}:\sigma ^{2}=\sigma_{0}^{2} \\
H_{1}:\sigma ^{2}\neq \sigma_{0}^{2}
\end{cases}$$
If we know $\mu$ and $H_{0}$ is true, the test statistic is
$$T=\sum_{i=1}^{N} \frac{(x_{i}-\mu)^{2}}{\sigma_{0}^{2}}\sim\chi ^{2}_{N}$$
which has [[chi-square distribution]] with $N$ degrees of freedom. The test is also double-tailed, and you integrate the $\chi ^{2}_{N}$ for the critical region. Given an $\alpha$, you find the values $r_{\alpha/2}^{+}$ and $r_{\alpha/2}^{-}$ for which the integrals are both equal to $\alpha/2$. However, since the $\chi ^{2}_{N}$ is asymmetrical for low $N$, these values are going to be different, unlike above where there's a common $r_{\alpha/2}$.