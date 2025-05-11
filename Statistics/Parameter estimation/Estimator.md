---
wiki-publish: true
aliases:
  - point estimate
  - bias
---
An **estimator** is a value whose [[expected value]] is the [[true value]] of a quantity. If the true value is $\theta$, an estimator is denoted $\hat{\theta}$ and we have $E[\hat{\theta}]=\theta$. A **point estimate** $\hat{\theta}^{*}$ is the value of an estimator calculated at a certain point. Note that an estimator is a [[random variable]], whereas a point estimate is a number. Sometimes the word **estimate** is ambiguously used to refer to either.
### Properties
For a [[sample]] size of $n$, we have the following property
$$\lim_{ n \to \infty } P(\lvert \hat{\theta}-\theta \rvert <\varepsilon)=1$$
where $P$ is [[probability]] and $\varepsilon$ is an arbitrarily small number. Basically, as the sample size goes to infinity, the difference between an estimator and the true value become arbitrarily small, so increasing the sample size always leads to better estimates.
### Bias
Say we have an estimator $\hat{\theta}$ and a function to [[Parameter estimation|fit]] $g(\hat{\theta})$. The expected value of $\hat{\theta}$ is
$$E[\hat{\theta}]=\int_{\Omega_{\theta}}\hat{\theta}g(\hat{\theta})d \hat{\theta}=\int_{\Omega_{x}}\hat{\theta}f(x_{1},\ldots,x_{n})dx_{1}\ldots dx_{n}=\theta+b$$
The value $b$ is called **bias** and it shifts the expected value away from the true value. If $b=0$, the estimator is said to be **unbiased**, else it is **biased**.
### Examples
The [[mean]] $\hat{\mu}\equiv \bar{x}$ is a common unbiased estimator. In fact, for a sample set $\{ x_{1},\ldots,x_{n} \}$ we have
$$\hat{\mu}=\frac{1}{n}\sum_{i=1}^{n} x_{i}\quad\to \quad E[\hat{\mu}]=\mu$$
Its [[variance]] is also the same as that of the true value:
$$\sigma ^{2}=\frac{1}{n}\sum_{i=1}^{n} (x_{i}-\mu)^{2},\quad \hat{\sigma}^{2}=\frac{1}{n-1}\sum_{i=1}^{n} (x_{i}-\hat{\mu})^{2}$$
for which
$$E[\sigma ^{2}]=\sigma ^{2},\qquad E[\hat{\sigma}^{2}]=\sigma ^{2}$$
Note the $n-1$ in the estimator variance. That is the **Bessel correction** and it allows the estimate to be unbiased. If we just used $n$, there would be a bias in the expectation value.

The "arbitrarily close to the true value" property holds:
$$\lim_{ n \to \infty } P(\lvert \hat{\mu}-\mu \rvert <\varepsilon)=1$$
> [!example] Proof
> Using [[Chebyshev's inequality]] we get
> $$P(\lvert \hat{\mu}-\mu \rvert \geq \lambda \sigma_{\hat{\mu}})< \frac{1}{\lambda ^{2}}$$
> If we call $\varepsilon=\frac{\lambda \sigma}{\sqrt{ n }}$ we get $\frac{1}{\lambda ^{2}}=\frac{\sigma ^{2}}{\varepsilon ^{2}n}$ which means
> $$P(\lvert \hat{\mu}-\mu \rvert \geq \varepsilon)< \frac{\sigma ^{2}}{\varepsilon ^{2}n}$$
> As $n\to \infty$ we get
> $$\lim_{ n \to \infty } P(\lvert \hat{\mu}-\mu \rvert \geq \varepsilon)= 0$$
> By logical inversion, we get the previous statement.

