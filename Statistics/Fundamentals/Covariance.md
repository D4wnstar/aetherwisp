---
aliases:
  - correlation coefficient
---
The **covariance** of two [[random variable|random variables]] is a measure of their correlation and joint variability. For two [[Joint distribution function|jointly-distributed]] variables $X$ and $Y$ with finite [[variance]], their covariance is defined as
$$\text{cov}(X,Y)=E[(X-E[X])(Y-E[Y])]$$
where $E[\cdot]$ is the [[expected value]]. Unlike variance, which is strictly positive, covariance may take any real value. High positive values indicate strong correlation, whereas high negative values indicate strong anticorrelation. The **correlation coefficient** or just **correlation** $\rho_{XY}$ is a scale-independent form of the covariance, defined as
$$\rho_{XY}=\frac{\text{cov}(X,Y)}{\sigma_{X}\sigma_{Y}}$$
which is defined in $[-1,1]$. It has the same meaning as the covariance, but with [[Normalizzazione|normalized]] values. By convention, it is said that two variables with correlation $\lvert \rho_{XY} \rvert\leq 0.3$ are *weakly correlated*, whereas variables with $\lvert \rho_{XY} \rvert\geq 0.7$ are *strongly correlated*.

> [!example] Two normally-distributed variables
> Consider two [[Gaussian distribution|normally-distributed]] random variables $X_{1}$ and $X_{2}$, with [[mean]] $\mu_{1}$ and $\mu_{2}$ and variance $\sigma ^{2}_{1}$ and $\sigma_{2}^{2}$. Let's define $Y_{1}=X_{1}$ and $Y_{2}=X_{2}+aX_{1}$. We want to find the correlation between $Y_{1}$ and $Y_{2}$, so we calculate the covariance:
> $$\begin{align}
> \text{cov}(Y_{1},Y_{2})&=E[(Y_{1}-\mu_{1})(Y_{2}-\mu_{2}-a\mu_{1})] \\
> &=E[(X_{1}-\mu_{1})(X_{2}-\mu_{2}+a(X_{1}-\mu_{1}))] \\
> &=E[(X_{1}-\mu_{1})(X_{2}-\mu_{2})]+E[(X_{1}-\mu_{1})^{2}a] \\
> &=a\sigma_{1}^{2}
> \end{align}$$

