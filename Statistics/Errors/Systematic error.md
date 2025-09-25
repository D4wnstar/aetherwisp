---
wiki-publish: true
---
A **systematic error** is a type of measurement error that occurs consistently across measurements and is due to a repeatable, non-random process. It has non-zero [[mean]] and it does not reduce over large numbers of measurements.

Systematic errors can be corrected by deriving the magnitude of the error and subtracting it from the measurements. However, the derivation of the systematic error is itself prone to error, which propagates to the corrected measurements, making it impossible to fully remove the error. In fact, the term "systematic error" generally refers to the uncertainty on the correction, rather than the error itself.

Given a measurement $t$ for a [[true value]] $T$, the systematic error $\delta$ and its correction $\hat{\delta}$ can be written as
$$t=T-\delta+\hat{\delta}$$
$\delta$ is the mean of the error and it has a [[Variance]] $\sigma ^{2}_{\delta}$.
### Effect on multiple measurements
Consider two different measurements $t_{1}$ and $t_{2}$ of the true values $T_{1}$ and $T_{2}$, both affected by [[random error|random errors]] $u_{1}$ and $u_{2}$, and corrected systematic error $a=-\delta+\hat{\delta}$, with variances $\sigma ^{2}_{u}$ and $\sigma ^{2}_{\delta}$, like
$$t_{1}=T_{1}+u_{1}+a,\qquad t_{2}=T_{2}+u_{2}+a$$
Let's find their [[Covariance]]:
$$\text{cov}(t_{1},t_{2})=E[t_{1}t_{2}]-\underbrace{ E[t_{1}] }_{ T_{1} }\underbrace{ E[t_{2}] }_{ T_{2} }=\sigma ^{2}_{\delta}$$
since
$$E[t_{1}t_{2}]=E[(T_{1}+u_{1}+a)(T_{2}+u_{2}+a)]=$$
$$=E[T_{1}T_{2}]+E[T_{2}(u_{1}+a)]+E[T_{1}(u_{2}+a)]+E[(u_{1}+a)(u_{2}+a)]$$
The [[Covariance|correlation coefficient]] is
$$\rho=\frac{\text{cov}(t_{1},t_{2})}{\sigma_{t_{1}}\sigma_{t_{2}}}=\frac{\sigma_{\delta}^{2}}{\sigma ^{2}_{u}\sigma ^{2}_{\delta}}=\frac{1}{1+ \frac{\sigma ^{2}_{u}}{\sigma ^{2}_{\delta}}}$$
which tends to zero when the random errors are much more variable ($\sigma ^{2}_{u}\gg \sigma_{\delta}^{2}$) and to one if the systematic error is much more variable ($\sigma ^{2}_{\delta}\gg \sigma ^{2}_{u}$). So a high systematic error variance makes measurements strongly correlated, whereas a low one makes measurements independent.