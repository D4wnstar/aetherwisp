---
wiki-publish: true
aliases:
  - sample mean
---
The **arithmetic mean** is a function of a [[set]] of numbers that gives the sum of all the numbers divided the count of numbers. Calling $x_{1},\ldots,x_{N}$ the $N$ numbers, the arithmetic mean is
$$\bar{x}\equiv\frac{1}{N} \sum_{i=1}^{N} x_{i}=\frac{x_{1}+\ldots+x_{N}}{N}$$
It is a measure of [[central tendency]].
### In statistics
The arithmetic mean commonly appears in statistics as a descriptive [[statistic]] of a [[sample]], both in the sense [[Random variable|random variables]] and data points. Despite its simplicity, it benefits from remarkable properties that make it a commonly employed statistic.

Consider a sample of $N$ [[Independent variables|independent]] random variables $X_{1},\ldots,X_{N}$. The **sample mean** is
$$\boxed{\bar{X}=\frac{1}{N}\sum_{i=1}^{N} X_{i}}$$
This quantity is a [[Functions of random variables|function of random variables]] and hence follows its own [[probability distribution]] with its own true [[mean]] $\mu$ and true [[variance]] $\sigma ^{2}$. Estimating these quantities through the sample mean is rather straightforward. The [[expected value]] is simple:
$$\mathrm{E}[\bar{X}]=\frac{1}{N}\sum_{i=1}^{N} \mathrm{E}[X_{i}]=\frac{1}{N}\sum_{i=1}^{N} \mu_{i}=\mu$$
In other words, the sample (arithmetic) mean is an unbiased [[estimator]] of the true mean. The [[variance]] of this estimator is:
$$\text{var}(\bar{X})=\text{var}\left( \frac{1}{N}\sum_{i=1}^{N} X_{i} \right)=\frac{1}{N^{2}}\text{var}\left( \sum_{i=1}^{N} X_{i} \right)=\frac{1}{N^{2}}\sum_{i=1}^{N} \text{var}(X_{i})=\frac{1}{N^{2}}\sum_{i=1}^{N} \sigma_{i}^{2}$$
by using properties of the variance for independent variables. If the $X_{1},\ldots,X_{N}$ are [[iid]], then $\sigma_{i}^{2}=\sigma ^{2}$ and $\sum_{i=1}^{N}\sigma ^{2}=N\sigma ^{2}$ so
$$\boxed{\text{var}(\bar{X})=\frac{\sigma ^{2}}{N}\quad\text{if }X_{1},\ldots,X_{N}\text{ are iid}}$$
If they are not, we can define the **average population variance**
$$\bar{\sigma}^{2}=\frac{1}{N}\sum_{i=1}^{N} \sigma ^{2}_{i}$$
for which
$$\boxed{\text{var}(\bar{X})=\frac{\bar{\sigma}^{2}}{N}\quad\text{if }X_{1},\ldots,X_{N}\text{ are independent}}$$
This form goes back to the previous one for iid variables. These variances tell us how precise the estimate is.

These formulas are true regardless of the [[probability distribution|probability distributions]] of $X_{1},\ldots,X_{N}$ and they become particularly useful after remembering that the arithmetic mean obeys the [[law of large numbers]]:
$$\lim_{ N \to \infty } P(\lvert \bar{X}-\mu \rvert \geq \varepsilon)=0$$
In other words, as the number of random variables (in practice, data points) grows large, the sample mean becomes a progressively better (more precise) estimator of the true mean.[^1] Moreover, when rescaled to $\sqrt{ N }(\bar{X}-\mu)$, then sample mean's distribution approaches a [[Gaussian distribution]] $\mathcal{N}(0,\sigma ^{2})$, as proven by the [[central limit theorem]].

[^1]: You can also see this due to how $\text{var}(\bar{X})\to 0$ when $N\to \infty$.
