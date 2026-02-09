---
wiki-publish: true
aliases:
  - confidence region
---
A **confidence interval** of an [[Estimator|estimate]] is an interval that contains the estimate and conveys the likelihood that the [[Sample|true value]] is within the interval across repeated measurements. The likelihood of containing the true value is called the **confidence level** and, importantly, it does not convey the [[probability]] that the true value falls in that *individual* confidence interval. Rather, it refers to how frequently it does across repeated measurements. A 95% confidence level does not say "there is a 95% chance that the true value is in *this* interval" but rather "across 100 different measurements with 100 different intervals, around 95 of them contain the true value." Confidence intervals are a fundamentally frequentist tool: they require repetition of the same phenomenon to have meaning. As such, they convey confidence on the repeated *process* more so than the estimate.

When estimating multiple parameters at the same time, their individual intervals can be combined into **confidence regions**, but they are seldom used in practice.
## Construction
Confidence intervals can be constructed in multiple ways, some more specific than others. The general method requires choosing a confidence level and integrating over a region of the parameter space. In practice, special [[statistic|statistics]] called **pivots** can be used.
### General method
Call $\theta$ the population parameter to be estimated and $\hat{\theta}$ an estimator that we are calculating on some [[sample]]. To proceed, we need to know the [[probability distribution]] that $\hat{\theta}$ follows, specifically its [[probability density function]] (or [[probability mass function]]) $f_{\hat{\theta}}(\hat{\theta}^{*})$. We choose a confidence level $\gamma \in[0,1]$ by hand: typically, numbers near $1$ are chosen, such as $0.90$, $0.95$ and $0.99$.[^1] Once fixed, the interval $[\theta_{a},\theta_{b}]$ is determined by the integral
$$P(\theta_{a}<\theta<\theta_{b})=\int_{\theta_{a}}^{\theta_{b}}f_{\hat{\theta}}(\hat{\theta}^{*})d \hat{\theta}^{*}=\gamma\tag{1}$$
where $P$ is a [[measure]] of probability. This probability is observed by repeating the experiment multiple times and constructing the interval for each.

The interval bounds are two, but equation $(1)$ is only one. As such, it does not fully define the bounds. One more condition is needed to fully determine the interval. Multiple such conditions exist and depend on the specifics of the problem. A common one is to state that the interval is centered on $\theta$ and symmetric, so that $\theta_{a}$ and $\theta_{b}$ are equally distant from $\theta$. Then, the interval (half-)width is the only bound that needs to be estimated.
### Pivots
The construction of a confidence interval typically makes use of a **pivot**, a statistic of both the estimate and the parameter, whose [[probability distribution]] is known.

Let's start with a practical example. A common pivot function is the following, defined for a random sample of iid [[Gaussian distribution|normal distributions]]  $X_{1},\ldots,X_{N}\sim\mathcal{N}(\mu,\sigma ^{2})$ for which we wish to estimate the [[mean]] $\mu$ through the [[Arithmetic mean|sample mean]] $\bar{X}$. The [[variance]] $\sigma ^{2}$ may be known or unknown. The pivot function changes a bit between these two cases. If $\sigma ^{2}$ is known, we define
$$T(\mu)=\frac{\bar{X}-\mu}{\sqrt{ \sigma ^{2}/N }}\sim \mathcal{N}(0,1)$$
which follows a standard normal distribution. Because of this, the probability that a realization of $T(\mu)$ falls in $[-1,1]$ is 68.3%, since that's a well-known property of the standard normal. Therefore, we can construct the confidence interval as $[\bar{X}-\sigma,\bar{X}+\sigma]$ with $\gamma=0.683$. Viceversa, since the standard normal is known, it is possible to manually define $\gamma$ and calculate the scaling factor $c$ for the corresponding $[\bar{X}-c\sigma,\bar{X}+c\sigma]$ interval.

If $\sigma ^{2}$ is *not* known, then we employ the unbiased [[Variance|sample variance]] $S^{2}$ as a substitute. The pivot is now defined as
$$T(\mu)=\frac{\bar{X}-\mu}{\sqrt{ S^{2}/N }}\sim t_{N-1}$$
which instead follows a [[Student's t distribution]] with $N-1$ degrees of freedom. This pivot is a bit more complicated, but since the [[Probability density function|PDF]] of $t_{N-1}$ is known, it is possible to calculate the confidence interval in the same way as above. Notably, the Student's t distribution obeys the [[central limit theorem]], so for large $N$, it converges to a normal distribution and the difference between the two pivots shrinks.

More technically, this pivot carries the property
$$\text{Prob}(t_{N-1;\ \alpha/2}\leq T(\mu)\leq t_{N-1;\ 1-\alpha/2})=1-\alpha$$
where $t_{N-1;\ \alpha}$ is $\alpha$ [[Quantile function|quantile]] of the $t_{N-1}$ distribution and $\alpha=1-\gamma$. By symmetry arguments, $t_{N-1;\ \alpha/2}=-t_{N-1;\ 1-\alpha/2}$. With some algebra, the previous property can be manipulated to read
$$\text{Prob}\left( \bar{X}-t_{N-1;1-\alpha/2}\sqrt{ \frac{S^{2}}{N} }\leq \mu \leq \bar{X}+t_{N-1;\ 1-\alpha/2}\sqrt{ \frac{S^{2}}{N} } \right)=1-\alpha$$
Hence, the random interval of bounds
$$\bar{X}-t_{N-1;\ 1-\alpha/2}\sqrt{ \frac{S^{2}}{N} }\quad\text{and}\quad \bar{X}+t_{N-1;\ 1-\alpha/2}\sqrt{ \frac{S^{2}}{N} }$$
contains the mean $\mu$ with probability $\gamma$.

In practice, given a particular set of data $x_{1},\ldots,x_{N}$, we calculate the confidence interval by replacing $\bar{X}$ and $S^{2}$ with their observed values $\bar{x}$ and $s^{2}$ for the data that we have:
$$\bar{x}-t_{N-1;\ 1-\alpha/2}\sqrt{ \frac{s^{2}}{N} }\quad\text{and}\quad \bar{x}+t_{N-1;\ 1-\alpha/2}\sqrt{ \frac{s^{2}}{N} }$$
This interval either contains the true value of $\mu$ or it does not, with the probability given by $\gamma\%$. In other words, given some dataset $x_{1},\ldots,x_{N}$, there's a $\gamma\%$ chance that the confidence interval defined as above will contain the true value of the mean.

Choosing $\gamma$ (or $\alpha$) is therefore crucial: $\gamma$ is arbitrary because it's not an inherent property of the dataset or distribution. It's essentially a push-pull relation between accuracy and guarantees. On one hand, if $\gamma$ is very high, then basically every dataset we collect will contain the true value. In theory that sounds great; in practice the price we pay is that the confidence interval is huge. Indeed, what varying $\alpha$ does is essentially making the interval larger or smaller. The larger the interval, the more likely the true value is to fall in it, but the more error we accept. On the other hand, small intervals are very accurate, but they have a very high chance of being straight-up wrong. The figures for $\alpha$ given before are a good mixture of reliable and "accurate enough". For instance, the $95\%$ figure is wrong about 1 in 20 times.

As for the endpoints, it depends on $\alpha$. It's generally chosen to be symmetrical $1-\alpha/2$ and $1+\alpha/2$, and these kinds of intervals are called **equi-tailed**, but strictly speaking there's no need. We can generalize to $1-\alpha_{1}$ and $1-\alpha_{2}$, with the only necessary condition being $\alpha_{1}+\alpha_{2}=\alpha$. Other notable choices are $(\alpha_{1},\alpha_{2})=(0,\alpha)$ and $(\alpha_{1},\alpha_{2})=(\alpha,0)$. These respectively make the left and right endpoints infinitely far, so that the confidence interval is only bounded to the left or right. These are called **one-sided** confidence intervals.

Exact confidence intervals are few and far between. Thankfully, approximate intervals are rather easy to find. A common approximate interval is given by the **Wald pivot**, for some parameter $\psi$. It is based on a consistent estimator which is approximately standard-normally-distributed for large sample sizes:
$$Z(\psi)=\frac{\hat{\psi}-\psi}{\text{SE}(\psi)}\approx N(0,1)$$
for all $\psi$. $\text{SE}(\psi)$ is the [[Standard error]]. The corresponding confidence interval is between
$$\hat{\psi}-z_{1-\alpha/2}\text{SE}(\hat{\psi})\quad\text{and}\quad\hat{\psi}+z_{1-\alpha/2}\text{SE}(\hat{\psi})$$
The benefit of this pivot is that the [[central limit theorem]] makes it work in many cases when $\psi$ is the sample mean of each variable.

[^1]: A notable exception is if $\hat{\theta}$ is known to follow a [[Gaussian distribution]], in which case $0.68$ is also common, as it's the interval spanned by one [[standard deviation]].
