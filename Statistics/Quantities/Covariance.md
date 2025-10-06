---
wiki-publish: true
aliases:
  - correlation coefficient
  - covariance matrix
---
The **covariance** of two [[random variable|random variables]] is a measure of how linearly related they are. For two [[Joint distribution function|jointly-distributed]] variables $X$ and $Y$ with finite [[variance]], their covariance is defined as
$$\text{cov}(X,Y)=\text{E}[(X-\text{E}[X])(Y-\text{E}[Y])]$$
where $\text{E}[\cdot]$ is the [[expected value]]. Unlike variance, which is strictly positive, covariance may take any real value. High positive values indicate strong correlation, whereas high negative values indicate strong anticorrelation.

The **correlation coefficient** or just **correlation** $\rho_{XY}$ is a scale-independent form of the covariance, defined as
$$\rho_{XY}=\frac{\text{cov}(X,Y)}{\sigma_{X}\sigma_{Y}}$$
which is defined in $[-1,1]$. It has the same meaning as the covariance, but with [[Normalization|normalized]] values. By convention, it is said that two variables with correlation $\lvert \rho_{XY} \rvert\leq 0.3$ are **weakly correlated**, whereas variables with $\lvert \rho_{XY} \rvert\geq 0.7$ are **strongly correlated**.

> [!example]- Two normally-distributed variables
> Consider two [[Gaussian distribution|normally-distributed]] random variables $X_{1}$ and $X_{2}$, with [[mean]] $\mu_{1}$ and $\mu_{2}$ and variance $\sigma ^{2}_{1}$ and $\sigma_{2}^{2}$. Let's define $Y_{1}=X_{1}$ and $Y_{2}=X_{2}+aX_{1}$. We want to find the correlation between $Y_{1}$ and $Y_{2}$, so we calculate the covariance:
> $$\begin{align}
> \text{cov}(Y_{1},Y_{2})&=E[(Y_{1}-\mu_{1})(Y_{2}-\mu_{2}-a\mu_{1})] \\
> &=E[(X_{1}-\mu_{1})(X_{2}-\mu_{2}+a(X_{1}-\mu_{1}))] \\
> &=E[(X_{1}-\mu_{1})(X_{2}-\mu_{2})]+E[(X_{1}-\mu_{1})^{2}a] \\
> &=a\sigma_{1}^{2}
> \end{align}$$

### Properties
- It commutes: $\text{cov}(X,Y)=\text{cov}(Y,X)$.
- If $X$ and $Y$ are [[independent variables]], then $\text{cov}(X,Y)=0$.
- If $\text{cov}(X,Y)=0$, $X$ and $Y$ are *not* in general independent variables. They are only linearly uncorrelated. They may still be nonlinearly correlated. The covariance does not provide information on nonlinear correlation.
### Covariance matrix
The **covariance matrix** $\Sigma$ of a random vector $\mathbf{X}=(X_{1},\ldots,X_{N})$ is the [[matrix]] that contains the information about all of the variances and covariances within the system. It is defined by its elements $\Sigma_{ij}$:
$$\Sigma_{ij}\equiv\rho_{ij}\sigma_{i}\sigma_{j}$$
Explicitly it reads
$$\Sigma\equiv \text{E}[(\mathbf{X}-\text{E}[\mathbf{X}])(\mathbf{X}-\text{E}[\mathbf{X}])^{T}]= \begin{pmatrix}
\text{var}(X_{1}) & \text{cov}(X_{1},X_{2}) & \ldots & \text{cov}(X_{1},X_{N}) \\
\text{cov}(X_{2},X_{1}) & \text{var}(X_{2}) & \ldots & \text{cov}(X_{2},X_{N}) \\
\vdots & \vdots & \ddots & \vdots \\
\text{cov}(X_{N},X_{1}) & \text{cov}(X_{N},X_{2}) & \ldots & \text{var}(X_{N})
\end{pmatrix}$$
#### Properties
- From the commutativity of covariance, we see that the covariance matrix is is a [[Symmetric matrix|symmetrical matrix]], so $\Sigma_{ij}=\Sigma_{ji}$.
- The diagonal contains the variance of each random variable: $\Sigma_{ii}=\sigma ^{2}_{i}$.
- It is [[Matrix sign definitions|positive semidefinite]] and therefore also has nonnegative [[determinant]] $\det \Sigma\geq 0$ and is [[Invertible matrix|invertible]].
- For the covariance matrix of a linear relation: $\Sigma_{\mathrm{A}\mathbf{X}+\mathbf{b}}=\mathrm{A}\Sigma_{\mathbf{X}}\mathrm{A}^{T}$
