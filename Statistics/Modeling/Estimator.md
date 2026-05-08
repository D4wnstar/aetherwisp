---
hl-publish: true
aliases:
  - point estimate
  - bias
  - estimate
---
An **estimator** is a [[statistic]] that attempts to faithfully recreate the [[Sample|true value]] of a quantity. An estimator is typically denoted by adding a hat over the quantity's symbol, though some common estimators use conventional letters without the hat. The letter theta is a common choice: $\hat{\theta}$ is an estimator of the quantity $\theta$.

Being a statistic, it is a [[random variable]].  As such, it carries all the machinery inherited from having a [[probability distribution]], like having an [[expected value]] and a [[variance]]. By design, the expected value of an estimator is either equal or near the true value it is estimating. In general, it is
$$\text{E}[\hat{\theta}]=\theta+b$$
The quantity $b$ is known as **bias** and it represents how consistently off the mark the estimator is. If $b\neq 0$, the estimator is said to be **biased**, else it is **unbiased**. Since the end goal of an estimator $\hat{\theta}$ is to provide as close a value as possible to $\theta$, we ideally want all our estimators to be unbiased. However, it's not that easy in practice, as removing bias often comes at a cost of other valuable properties, such as increasing [[variance]].

A **(point) estimate** is the value of an estimator calculated on a specific [[sample]] of numbers. It's usually denoted with an asterisk, like $\hat{\theta}^{*}$. This difference is important: an *estimator* is a statistic and random variable, while an *estimate* is a number. It is the estimator that carries all the properties; estimates are just numbers. This is true for all statistics, but it's worth stressing here because the terminology is so similar between the two that it's easy to get mixed up.

The level of confidence of an estimate can be quantified by a [[confidence interval]], which is an interval that contains the estimate and represents the region of space in which the true value is likely to be, within a chosen level of significance. In multiple dimensions, intervals can be extended to **confidence regions**, but they are seldom used in practice.
### Properties
Estimators have numerous properties that determine how well they behave and how good their estimates are. Choosing between different estimators of the same quantity is a game of weighing these properties and choosing which one better fits the problem at hand. As a rather universal rule, the best estimator is usually the one with the lowest [[mean squared error]].

An estimator is **unbiased** if its bias is always zero. It is **asymptotically unbiased** if its bias in nonzero in general, but approaches zero as the sample size grows infinite
$$\lim_{ n \to \infty }b=0$$

A ([[Scalar]]) estimator $\hat{\theta}_{n}$ over a sample of size $n$ is said to be **(weakly) consistent** if, for any arbitrarily small number $\epsilon>0$, we have
$$\lim_{ N \to \infty } P(\lvert \hat{\theta}_{n}-\theta \rvert \geq\epsilon)=0$$
where $P$ is a [[measure]] of [[probability]]. Consistency is basically a generalized [[law of large numbers]] for any estimator. Conversely, the law of large numbers is just saying "the sample mean is a consistent estimator of the expected value." Basically, as the sample size goes to infinity, the difference between a consistent estimator and the true value becomes arbitrarily small, so that increasing the sample size always leads to better estimates. A sufficient condition to guarantee consistency is that the [[Mean squared error]] of the estimator goes to zero as $n\to \infty$.

An unbiased estimator is **efficient** if it has small variance. Efficiency is a property that's often relative to another estimator; an estimator may be more or less efficient than another, but it's hard to say if it is efficient or not by itself. One good way of doing so is finding the lowest possible variance that an estimator can reach, which is given by the [[Cramer-Rao inequality]]. Calling $\sigma ^{2}_\text{min}$ the minimum variance, a measure of efficiency is
$$\varepsilon=\frac{\sigma ^{2}_\text{min}}{\sigma ^{2}_{\hat{\theta}}}$$

An estimator is **robust** if it is has good performance across a wide range of statistical [[Statistics/Modeling/Model|models]] built on the sample data. Robust estimators are typically less efficient than flimsy ones, but in return they are more resistant to outliers, which are a major source of large errors and biases.
### Examples
The sample [[mean]] $\hat{\mu}\equiv \bar{X}$ is a common unbiased estimator of the true population mean. In fact, for a [[sample]] set $\{ x_{1},\ldots,x_{N} \}$ sampled from a random variable $X$ we have
$$\hat{\mu}=\frac{1}{N}\sum_{i=1}^{N} x_{i}\quad\to \quad \text{E}[\hat{\mu}]=\mu$$
The [[Variance|sample variance]] is also an estimator of the true population variance, though it is only unbiased with some care:
$$\hat{\sigma}^{2}=\frac{1}{N-1}\sum_{i=1}^{N} (x_{i}-\hat{\mu})^{2}\quad\to \quad\text{E}[\hat{\sigma}^{2}]=\sigma ^{2}$$
Note the $n-1$ in the sample variance: that is the **Bessel correction** and it's what allows the estimator to be unbiased. If we just used $N$, there would be a negative bias that would consistently underestimate the variance. Specifically, the bias would be
$$b_{\hat{\sigma}^{2}}=- \frac{\sigma ^{2}}{N}$$
where $\sigma ^{2}$ is the true variance. Notably, even the uncorrected sample variance becomes unbiased asymptotically for $N\to \infty$. The sample variance has in general higher variance than the sample mean at the same sample size, making it a less efficient estimator.

The sample [[median]] is a robust estimate of [[central tendency]], being much less sensitive to outliers than the sample mean at the cost of some efficiency. In general, it's good to calculate both the sample mean and median to see if they match or have large differences. If they do, it might be time look at the outliers.

The generalized [[law of large numbers]] holds:
$$\lim_{ n \to \infty } P(\lvert \hat{\mu}-\mu \rvert <\varepsilon)=1$$

> [!quote]- Proof
> Using [[Chebyshev's inequality]] we get
> $$P(\lvert \hat{\mu}-\mu \rvert \geq \lambda \sigma_{\hat{\mu}})< \frac{1}{\lambda ^{2}}$$
> If we call $\varepsilon=\frac{\lambda \sigma}{\sqrt{ n }}$ we get $\frac{1}{\lambda ^{2}}=\frac{\sigma ^{2}}{\varepsilon ^{2}n}$ which means
> $$P(\lvert \hat{\mu}-\mu \rvert \geq \varepsilon)< \frac{\sigma ^{2}}{\varepsilon ^{2}n}$$
> As $n\to \infty$ we get
> $$\lim_{ n \to \infty } P(\lvert \hat{\mu}-\mu \rvert \geq \varepsilon)= 0$$
> By logical inversion, we get the previous statement.
