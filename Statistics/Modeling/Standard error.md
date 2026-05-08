---
hl-publish: true
---
The **standard error** is a metric of error for a [[Scalar]] [[estimator]]. Given an estimator $\hat{\theta}$, it is defined as
$$\text{SE}(\hat{\theta})=\sqrt{ \text{var}(\hat{\theta}) }$$
It is a more convenient error metric than simple [[Variance]] because it has the same units as the estimator. Once a [[sample]] of $N$ elements is collected and a numerical estimate $\theta$ is obtained, the estimated standard error is obtained by replacing $\hat{\theta}$ with $\theta$. A common related quantity is the standard error of the sample [[mean]]
$$\text{SE}(\bar{X})=\frac{\sigma}{\sqrt{ N }}$$
where $\sigma$ is the [[standard deviation]].
### Delta method
Suppose that we are interested in a parameter which is a function of a scalar parameter $\theta$, namely
$$\psi=g(\theta)$$
where $g$ is some continuous [[Differential|differentiable]] function. In this situation, we can apply the **continuous mapping theorem**.

> [!info] Continuous mapping theorem
> If $\hat{\theta}$ is a consistent estimator of $\theta$, then $\hat{\psi}=g(\hat{\theta})$ is consistent for $\psi$.

The standard error of $\psi$ is approximately provided by the so-called **delta method**, which states
$$\text{SE}(\hat{\psi})\simeq\text{SE}(\hat{\theta})\left\lvert  \frac{dg(\theta)}{d\theta}  \right\rvert $$
The approximation improves as the sample size $N$ gets larger.

> [!quote]- Proof
> To prove this, consider $\hat{\theta}=T$. It approximately follows a [[Gaussian distribution|normal distribution]] $N(\theta, \sigma ^{2}/N)$. We can shift and rescale this to follow a nicer normal:
> $$\sqrt{ n }(T-\theta)\approx N(0,\sigma ^{2})$$
> We know that $\psi=g(\theta)$ and that its estimator is $\hat{\psi}=g(\hat{\theta})=g(T)$. We want to know $\hat{\psi}$. We'll use a [[Taylor series]] expansion in $t=\theta$ and truncate to first order:
> $$g(T)\simeq g(\theta)+g'(\theta)(T-\theta)$$
> We can reorder this to read
> $$\sqrt{ n }(g(T)-g(\theta))\simeq(g'(\theta)(T-\theta))\ldots$$
> and so
> $$\hat{\psi}=g(T)\approx$$
> (Finish this 10/10/2025)
