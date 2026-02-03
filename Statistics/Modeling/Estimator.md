---
wiki-publish: true
aliases:
  - point estimate
  - bias
  - estimate
---
An **estimator** is a [[statistic]] that attempts to faithfully recreate the [[Sample|true value]] of a quantity. An estimator is typically denoted by adding a hat over the quantity's symbol, though some common estimators use conventional letters without the hat. The letter theta is a common choice: $\hat{\theta}$ is an estimator of the quantity $\theta$.

Being a statistic, it is a [[random variable]].  As such, it carries all the machinery inherited from having a [[probability distribution]], like having an [[expected value]] and a [[variance]]. By design, the expected value of an estimator is either equal or near the true value it is estimating. In general, it is
$$\text{E}[\hat{\theta}]=\theta+b$$
The quantity $b$ is known as **bias** and it represents how consistently off the mark the estimator is. If $b\neq 0$, the estimator is said to be **biased**, else it is **unbiased**. Since the end goal of an estimator $\hat{\theta}$ is to provide as close a value as possible to $\theta$, we ideally want all our estimators to be unbiased. However, it's not that easy in practice, as removing bias often comes at a cost of other valuable properties, such as increasing [[variance]].

A **(point) estimate** $\hat{\theta}^{*}$ is the value of an estimator calculated at a certain point. This difference is important: an *estimator* is a statistic and random variable, while an *estimate* is a number. It is the estimator that carries all the properties; estimates are just numbers. This is true for all statistics, but it's worth stressing here because the terminology is so similar between the two that it's easy to get mixed up.

The level of confidence of an estimate can be quantified by a [[confidence interval]], which is an interval that contains the estimate and represents the region of space in which the true value is likely to be, within a chosen level of significance. In multiple dimensions, intervals can be extended to **confidence regions**, but they are seldom used in practice.
### Properties
A ([[scalar]]) estimator over a sample of size $N$ is said to be **(weakly) consistent** if, for any arbitrarily small $\epsilon>0$, we have
$$\lim_{ N \to \infty } P(\lvert \hat{\theta}-\theta \rvert >\epsilon)=0$$
where $P$ is a [[measure]] of [[probability]]. Consistency is, at heart, the generalized form of the [[law of large numbers]] for any estimator. Conversely, the law of large numbers is just saying "the sample mean is a consistent estimator of the expected value." Basically, as the sample size goes to infinity, the difference between a consistent estimator and the true value becomes arbitrarily small, so that increasing the sample size always leads to better estimates. A sufficient condition to guarantee consistency is that the [[Mean squared error]] of the estimator goes to zero as $N\to \infty$.

An unbiased estimator is **efficient** if it has small variance. Efficiency is a property that's typically relative to another estimator; an estimator may be more or less efficient than another, but it's hard to say if it is efficient or not by itself.

An estimator is **robust** if it is has good performance across a wide range of statistical [[Statistics/Modeling/Model|models]] built on the sample data. Robust estimators are typically less efficient than flimsy ones, but in return they are more resistant to outliers, which are a major source of large errors and biases.
### Examples
The sample [[mean]] $\hat{\mu}\equiv \bar{X}$ is a common unbiased estimator of the true population mean. In fact, for a [[sample]] set $\{ x_{1},\ldots,x_{N} \}$ sampled from a random variable $X$ we have
$$\hat{\mu}=\frac{1}{N}\sum_{i=1}^{N} x_{i}\quad\to \quad \text{E}[\hat{\mu}]=\mu$$
The [[Variance|sample variance]] is also an estimator of the true population variance, though it is only unbiased with some care:
$$\hat{\sigma}^{2}=\frac{1}{N-1}\sum_{i=1}^{N} (x_{i}-\hat{\mu})^{2}\quad\to \quad\text{E}[\hat{\sigma}^{2}]=\sigma ^{2}$$
Note the $n-1$ in the sample variance: that is the **Bessel correction** and it's what allows the estimator to be unbiased. If we just used $N$, there would be a negative bias that would consistently underestimate the variance. Specifically, the bias would be
$$b_{\hat{\sigma}^{2}}=- \frac{\sigma ^{2}}{N}$$
where $\sigma ^{2}$ is the true variance. Notably, even the uncorrected sample variance becomes unbiased for $N\to \infty$, a property known as **asymptotic unbiasedness**. The sample variance has in general higher variance than the sample mean at the same sample size, making it a less efficient estimator.

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
### Confidence intervals
The construction of a confidence interval typically makes use of a **pivot**, a function of the data and the parameter, whose [[probability distribution]] is known.

Let's start with an example. A pivot function is, for instance, the following, defined for a random sample of a [[Gaussian distribution|normal distribution]] $N(\mu,\sigma ^{2})$ in which we wish to estimate $\mu$ and $\sigma ^{2}$ is *not* known. In this case, the parameters are $\boldsymbol{\theta}=(\mu,\sigma ^{2})$ and the pivot is
$$T(\mu)=\frac{\bar{X}-\mu}{\sqrt{ S^{2}/N }}\sim t_{N-1}$$
where $\bar{X}$ is the sample mean, $S^{2}$ is the sample variance and $t_{N-1}$ is the [[Student's t distribution]]. This pivot carries the property
$$\text{Prob}(t_{N-1;\ \alpha/2}\leq T(\mu)\leq t_{N-1;\ 1-\alpha/2})=1-\alpha$$
where $t_{N-1;\ \alpha}$ is $\alpha$ [[Quantile function|quantile]] of the $t_{N-1}$ distribution. By symmetry arguments, $t_{N-1;\ \alpha/2}=-t_{N-1;\ 1-\alpha/2}$. With some algebra, the previous property can be manipulated to read
$$\text{Prob}\left( \bar{X}-t_{N-1;1-\alpha/2}\sqrt{ \frac{S^{2}}{N} }\leq \mu \leq \bar{X}+t_{N-1;\ 1-\alpha/2}\sqrt{ \frac{S^{2}}{N} } \right)=1-\alpha$$
Hence, the random interval of bounds
$$\bar{X}-t_{N-1;\ 1-\alpha/2}\sqrt{ \frac{S^{2}}{N} }\quad\text{and}\quad \bar{X}+t_{N-1;\ 1-\alpha/2}\sqrt{ \frac{S^{2}}{N} }$$
contains the mean $\mu$ with probability $1-\alpha$. This interval is known as a $(1-\alpha)\times100\%$ confidence interval. The parameter $\alpha$ is arbitrarily chosen: typical choices are $1-\alpha=99\%$ and $1-\alpha=95\%$.

In practice, given a particular set of data $x_{1},\ldots,x_{N}$, we calculate the confidence interval by replacing $\bar{X}$ and $S^{2}$ with their observed values $\bar{x}$ and $s^{2}$ for the data that we have:
$$\bar{x}-t_{N-1;\ 1-\alpha/2}\sqrt{ \frac{s^{2}}{N} }\quad\text{and}\quad \bar{x}+t_{N-1;\ 1-\alpha/2}\sqrt{ \frac{s^{2}}{N} }$$
This interval either contains the true value of $\mu$ or it does not, with the probability given by $(1-\alpha)\%$. In other words, given some dataset $x_{1},\ldots,x_{N}$, there's a $(1-\alpha)\%$ chance that the confidence interval defined as above will contain the true value of the mean.

Choosing $\alpha$ is therefore crucial: $\alpha$ is arbitrary because it's not an inherent property of the dataset or distribution. It's essentially a push-pull relation between accuracy and guarantees. On one hand, if $(1-\alpha)$ is very high, then basically every dataset we collect will contain the true value. In theory that sounds great; in practice the price we pay is that the confidence interval is huge. Indeed, what varying $\alpha$ does is essentially making the interval larger or smaller. The larger the interval, the more likely the true value is to fall in it, but the more error we accept. On the other hand, small intervals are very accurate, but they have a very high chance of being straight-up wrong. The figures for $\alpha$ given before are a good mixture of reliable and "accurate enough". For instance, the $95\%$ figure is wrong about 1 in 20 times.

As for the endpoints, it depends on $\alpha$. It's generally chosen to be symmetrical $1-\alpha/2$ and $1+\alpha/2$, and these kinds of intervals are called **equi-tailed**, but strictly speaking there's no need. We can generalize to $1-\alpha_{1}$ and $1-\alpha_{2}$, with the only necessary condition being $\alpha_{1}+\alpha_{2}=\alpha$. Other notable choices are $(\alpha_{1},\alpha_{2})=(0,\alpha)$ and $(\alpha_{1},\alpha_{2})=(\alpha,0)$. These respectively make the left and right endpoints infinitely far, so that the confidence interval is only bounded to the left or right. These are called **one-sided** confidence intervals.

Exact confidence intervals are few and far between. Thankfully, approximate intervals are rather easy to find. A common approximate interval is given by the **Wald pivot**, for some parameter $\psi$. It is based on a consistent estimator which is approximately standard-normally-distributed for large sample sizes:
$$Z(\psi)=\frac{\hat{\psi}-\psi}{\text{SE}(\psi)}\approx N(0,1)$$
for all $\psi$. $\text{SE}(\psi)$ is the [[Standard error]]. The corresponding confidence interval is between
$$\hat{\psi}-z_{1-\alpha/2}\text{SE}(\hat{\psi})\quad\text{and}\quad\hat{\psi}+z_{1-\alpha/2}\text{SE}(\hat{\psi})$$
The benefit of this pivot is that the [[central limit theorem]] makes it work in many cases when $\psi$ is the sample mean of each variable.