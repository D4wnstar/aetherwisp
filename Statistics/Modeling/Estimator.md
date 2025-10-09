---
wiki-publish: true
aliases:
  - point estimate
  - bias
  - estimate
---
An **estimator** is a [[statistic]] that attempts to faithfully recreate the [[true value]] of a quantity. Being a statistic, it is a [[random variable]]. An estimator is typically denoted by adding a hat over the quantity's symbol, usually using the letter theta: $\hat{\theta}$ is an estimator of the quantity $\theta$.

The [[expected value]] of an estimator differs from the true value of the quantity by some amount $b$:
$$\text{E}[\hat{\theta}]=\theta+b$$
This quantity is known as **bias**. If $b\neq 0$, the estimator is said to be **biased**, else it is **unbiased**.

A **(point) estimate** $\hat{\theta}^{*}$ is the value of an estimator calculated at a certain point. This difference is important: an *estimator* is a statistic and random variable, while an *estimate* is a number. It is the estimator that carries all the properties; estimates are just numbers.
### Properties
A ([[scalar]]) estimator over a sample of size $N$ is said to be **(weakly) consistent** if, for any arbitrarily small $\epsilon>0$, we have
$$\lim_{ N \to \infty } P(\lvert \hat{\theta}-\theta \rvert >\epsilon)=0$$
where $P$ is a [[probability]]. Basically, as the sample size goes to infinity, the difference between a consistent estimator and the true value becomes arbitrarily small, so that increasing the sample size always leads to better estimates. A sufficient condition to guarantee consistency is that the [[mean squared error]] of the estimator goes to zero as $N\to \infty$.

An unbiased estimator is **efficient** if it has small variance. Efficiency is a property that's typically relative to another estimator; an estimator may be more or less efficient than another, but it's hard to say if it efficient or not by itself.

An estimator is **robust** if it is has good performance across a wide range of statistical [[Statistics/Modeling/Model|models]] built on the sample data. Robust estimators are typically less efficient than flimsy ones, but in return they are more resistant to outliers, which are a major source of large errors and biases.
### Bias
Say we have an estimator $\hat{\theta}$ and a function to [[Parameter estimation|fit]] $g(\hat{\theta})$. The expected value of $\hat{\theta}$ is
$$E[\hat{\theta}]=\int_{\Omega_{\theta}}\hat{\theta}g(\hat{\theta})d \hat{\theta}=\int_{\Omega_{x}}\hat{\theta}f(x_{1},\ldots,x_{n})dx_{1}\ldots dx_{n}=\theta+b$$
### Examples
The sample [[mean]] $\hat{\mu}\equiv \bar{X}$ is a common unbiased estimator of the true population mean. In fact, for a [[sample]] set $\{ x_{1},\ldots,x_{N} \}$ sampled from a random variable $X$ we have
$$\hat{\mu}=\frac{1}{N}\sum_{i=1}^{N} x_{i}\quad\to \quad \text{E}[\hat{\mu}]=\mu$$
The [[Variance|sample variance]] is also an estimator of the true population variance, though it is only unbiased with some care:
$$\hat{\sigma}^{2}=\frac{1}{N-1}\sum_{i=1}^{N} (x_{i}-\hat{\mu})^{2}\quad\to \quad\text{E}[\hat{\sigma}^{2}]=\sigma ^{2}$$
Note the $n-1$ in the sample variance: that is the **Bessel correction** and it's what allows the estimator to be unbiased. If we just used $N$, there would be a negative bias that would consistently underestimate the variance. Specifically, the bias would be
$$b_{\hat{\sigma}^{2}}=- \frac{\sigma ^{2}}{N}$$
where $\sigma ^{2}$ is the true variance. Notably, even the uncorrected sample variance becomes unbiased for $N\to \infty$, a property known as **asymptotic unbiasedness**. The sample variance has in general higher variance than the sample mean at the same sample size, making it a less efficient estimator.

The sample [[median]] is a robust estimate of central location, being much less sensitive to outliers than the sample mean at the cost of some efficiency. In general, it's good to calculate both the sample mean and median to see if they match or have large differences. If they do, it might be time look at the outliers.

The "arbitrarily close to the true value" property holds:
$$\lim_{ n \to \infty } P(\lvert \hat{\mu}-\mu \rvert <\varepsilon)=1$$

> [!quote]- Proof
> Using [[Chebyshev's inequality]] we get
> $$P(\lvert \hat{\mu}-\mu \rvert \geq \lambda \sigma_{\hat{\mu}})< \frac{1}{\lambda ^{2}}$$
> If we call $\varepsilon=\frac{\lambda \sigma}{\sqrt{ n }}$ we get $\frac{1}{\lambda ^{2}}=\frac{\sigma ^{2}}{\varepsilon ^{2}n}$ which means
> $$P(\lvert \hat{\mu}-\mu \rvert \geq \varepsilon)< \frac{\sigma ^{2}}{\varepsilon ^{2}n}$$
> As $n\to \infty$ we get
> $$\lim_{ n \to \infty } P(\lvert \hat{\mu}-\mu \rvert \geq \varepsilon)= 0$$
> By logical inversion, we get the previous statement.

