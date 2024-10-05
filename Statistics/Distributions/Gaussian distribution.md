---
aliases:
  - normal distribution
---
The **Gaussian distribution** or **normal distribution** is a real univariate continuous [[probability distribution]] defined as
$$N(x;\mu,\sigma ^{2})=\frac{1}{\sqrt{ 2\pi \sigma^{2} }}e^{- \frac{(x-\mu)^{2}}{2\sigma ^{2}}}$$
where $\mu$ is the [[expected value]] e $\sigma$ is the [[standard deviation]].

A **standard normal distribution** is defined as a normal distribution with $\mu=0$ and $\sigma=1$.
### Moments
The [[moment-generating function]] for the Gaussian is
$$M_{x}^{*}(t)=e^{t\mu+t^{2}\sigma ^{2}/2}$$
For a standard normal distribution, it simplifies to
$$M_{x}^{*}(t)=e^{t^{2}/2}$$
### As sum of normal variables
A sum of [[independent variable|independent variables]] $x_{i}$ that are normally distributed is itself a normal distribution:
$$y=\sum_{i=1}^{n} x_{i}$$
and its MGF is the sum of all the MGF over $x$:
$$M_{y}^{*}(t)=\prod_{i=1}^{n}M_{x}^{*}(t)$$
Let's consider a set of normal variables $\{x_{i}\}_{i}$ that are all normally distributed with mean $\mu$ and [[variance]] $\sigma ^{2}$. As the number of variables $n$ goes to infinity, the sum distribution goes like
$$N\left( \mu, \frac{\sigma ^{2}}{n} \right)$$
so the deviation tends to go to zero. Now let's consider the variable
$$z=\frac{\bar{x}-\mu}{\frac{\sigma}{\sqrt{ n }}}$$
where $\bar{x}=\frac{1}{n}\sum_{i=1}^{N}x_{i}$. This follows a standard normal distribution.


$$z= \frac{\sum_{i}x_{i}-n\mu}{\sigma \sqrt{ n }}=\sum_{i=1}^{n} \frac{x_{i}-\mu}{\sigma\sqrt{ n }}=\sum_{i=1}^{n} z_{i}$$
