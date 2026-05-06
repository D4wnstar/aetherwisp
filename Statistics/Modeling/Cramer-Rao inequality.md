---
hl-publish: true
aliases:
  - Cramer-Rao lower bound
  - CRLB
  - CRF
---
The **Cramer-Rao** or **Cramer-Rao-Frechèt inequality** gives a lower bound to the [[variance]] of an [[estimator]]. Given an unbiased estimator $\hat{\theta}$ for a [[Sample|population parameter]] $\theta$ , its variance is bounded by
$$\hat{\sigma}^{2}_{\hat{\theta}}\geq\frac{1}{\mathrm{E}\left[ - \dfrac{d^{2}\log \mathcal{L}}{d\theta ^{2}} \right]}$$
where $\mathrm{E}$ is the [[expected value]] and $\mathcal{L}$ is the twice-[[Differential|differentiable]] [[likelihood]] function evaluated over the same [[sample]] of the estimator. The inequality is saturated when
$$\frac{ \partial \log \mathcal{L} }{ \partial \theta } =k(\hat{\theta}-\theta)$$
where $k$ is either a constant or a function of $\theta$. In this case, $\hat{\theta}$ is said to be a **minimum-variance** estimator or that it achieves the **Cramer-Rao lower bound** (**CRLB**).

The inequality has two generalization. For one, we can assume the estimator is biased (with bias $b$). For the other, we can assume that instead of estimating a parameter $\theta$, we are estimating a function $\tau(\theta)$ of the parameter. The general estimator therefore is $\hat{\tau}$ with $\mathrm{E}[\hat{\tau}]=\tau(\theta)+b(\theta)$. With this estimator, the inequality becomes
$$\hat{\sigma}^{2}_{\hat{\tau}}\geq \frac{\left( \dfrac{d\tau}{d\theta}+ \dfrac{db}{d\theta} \right)^{2}}{\mathrm{E}\left[ - \dfrac{d^{2}\log \mathcal{L}}{d\theta ^{2}}  \right]}$$
This form goes back to the previous one when the estimator is unbiased ($b=0$) or constant with respect to $\theta$ ($db/d\theta=0$) and $\tau$ is the identity function ($\tau(\theta)=\theta$).

> [!quote]- Proof
> Consider an estimator $\hat{\tau}$ on a sample $X_{1},\ldots,X_{N}$ with [[sample space|sample spaces]] $\Omega_{1},\ldots,\Omega_{N}$ such that
> $$\mathrm{E}[\hat{\tau}]=\tau(\theta)+b(\theta)=\int_{\Omega_{N}}\ldots \int_{\Omega_{1}}\hat{\tau} f(\mathbf{x};\boldsymbol{\phi})\, dx_{1}\ldots dx_{N}$$
> using the definition of expected value over multiple dimensions. $f(\mathbf{x};\boldsymbol{\phi})$ is the [[joint distribution function]] of the sample, where $\boldsymbol{\phi}$ is the set of parameters that defines it. $\boldsymbol{\phi}$ includes $\theta$, with the others (if any) are assumed fixed. Hence, we write $f(\mathbf{x};\theta)$ instead to clarify that $f$ is a function of $\theta$ only. Furthermore, since the sample is fixed and we are analyzing the parameter (and its estimator), it is useful to reinterpret the JDF as the [[likelihood]] function $\mathcal{L}(\theta;\mathbf{x})$. Finally, for brevity, we write
> $$\int_{\Omega_{N}}\ldots \int_{\Omega_{1}}\equiv \int_{\boldsymbol{\Omega}}\quad\text{and}\quad dx_{1}\ldots dx_{N}\equiv d\mathbf{x}$$
> With all this, we can write
> $$\mathrm{E}[\hat{\tau}]=\int_{\boldsymbol{\Omega}}\hat{\tau}\mathcal{L}(\theta;\mathbf{x})d\mathbf{x}$$
> We want to calculate the variance of $\hat{\tau}$, so by definition $\sigma ^{2}_{\hat{\tau}}=\mathrm{E}[(\hat{\tau}-\tau)^{2}]$. To start, we find the derivative
> $$\frac{d\mathrm{E}[\hat{\tau}]}{d\theta}=\int_{\Omega}\hat{\tau}\frac{ d \mathcal{L} }{ d \theta }d\mathbf{x}=\int_{\boldsymbol{\Omega}} \hat{\tau}\frac{ d \log \mathcal{L} }{ d \theta }\mathcal{L}\ d\mathbf{x}=\mathrm{E}\left[ \hat{\tau} \frac{ d \log \mathcal{L} }{ d \theta }  \right]$$
> But also
> $$\frac{d\mathrm{E}[\hat{\tau}]}{d\theta}=\frac{d\tau}{d\theta}+ \frac{db}{d\theta}$$
> Since $\mathcal{L}$ is a JDF, it must be normalized, which means $\int_{\boldsymbol{\Omega}}\mathcal{L}(\theta;\mathbf{x})d\mathbf{x}=1$. Taking the $\theta$-derivative of this condition yields
> $$\int_{\boldsymbol{\Omega}}\frac{ d \mathcal{L} }{ d \theta }d\mathbf{x} =\int_{\boldsymbol{\Omega}}\frac{ d \log\mathcal{L} }{ d \theta }\mathcal{L}\ d\mathbf{x}=0\tag{Norm}$$
> Since $\tau$ (not $\hat{\tau}$!) is a function of only $\theta$, we can multiply both sides by it to get
> $$\int_{\boldsymbol{\Omega}}\tau\frac{ d \log\mathcal{L} }{ d \theta }\mathcal{L}\ d\mathbf{x}=\mathrm{E}\left[ \tau \frac{ d \log \mathcal{L} }{ d \theta }  \right]=0$$
> The difference between the previous expectation and this one is (using the linearity of the expectation operator):
> $$\mathrm{E}\left[ (\hat{\tau}-\tau)\frac{ d \log \mathcal{L} }{ d \theta }  \right]=\frac{d\tau}{d\theta}+ \frac{db}{d\theta}$$
> Invoking the [[Schwarz inequality]] we can state that $\mathrm{E}[XY]^{2}\leq \mathrm{E}[X^{2}]\mathrm{E}[Y^{2}]$, so
> $$\mathrm{E}[(\hat{\tau}-\tau)^{2}]\mathrm{E}\left[ \left( \frac{ d \log \mathcal{L} }{ d \theta } \right)^{2} \right]\geq\left( \frac{d\tau}{d\theta}+ \frac{db}{d\theta} \right)^{2}$$
> and so, recognizing the variance, we can write
> $$\sigma ^{2}_{\hat{\tau}}\geq\frac{\left( \dfrac{d\tau}{d\theta}+ \dfrac{db}{d\theta} \right)^{2}}{\mathrm{E}\left[ \left( \dfrac{ d \log\mathcal{\mathcal{L}} }{ d \theta } \right)^{2}  \right]}$$
> From equation $(\text{Norm})$, we can take the $\theta$-derivative to find
> $$\begin{align}
> \int_{\boldsymbol{\Omega}}\left[ \frac{ d \mathcal{L} }{ d \theta } \frac{ d \log \mathcal{L} }{ d \theta } +\mathcal{L}\frac{ d ^{2}\log \mathcal{L} }{ d \theta ^{2} }  \right]&=\int_{\boldsymbol{\Omega}}\mathcal{L}\left[ \mathcal{L}\left( \frac{ d \log \mathcal{L} }{ d \theta }  \right)^{2}+\mathcal{L}\frac{ d ^{2}\log \mathcal{L} }{ d \theta ^{2} }  \right] \\
> &=\mathrm{E}\left[ \left( \frac{ d \log \mathcal{L} }{ d \theta }  \right)^{2} \right]-\mathrm{E}\left[ - \frac{ d ^{2}\log \mathcal{L} }{ d \theta ^{2} }  \right]=0
> \end{align}$$
> We can thus state and
> $$\mathrm{E}\left[ \left( \frac{ d \log \mathcal{L} }{ d \theta }  \right)^{2} \right]=\mathrm{E}\left[ - \frac{ d ^{2}\log \mathcal{L} }{ d \theta ^{2} }  \right]$$
> and hence finally
> $$\sigma ^{2}_{\hat{\tau}}\geq\frac{\left( \dfrac{d\tau}{d\theta}+ \dfrac{db}{d\theta} \right)^{2}}{\mathrm{E}\left[- \dfrac{ d ^{2} \log\mathcal{\mathcal{L}} }{ d \theta ^{2} }  \right]}$$
> which completes our proof.
