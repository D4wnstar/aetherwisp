---
aliases:
  - normal distribution
  - standard normal distribution
---
The **Gaussian distribution** or **normal distribution** is a real univariate continuous [[probability distribution]]. For a [[random variable]] $X$, the [[probability density function]] is
$$N(x;\mu,\sigma ^{2})=\frac{1}{\sqrt{ 2\pi \sigma^{2} }}e^{- \frac{(x-\mu)^{2}}{2\sigma ^{2}}}$$
where $\mu$ is the [[expected value]] e $\sigma ^{2}$ is the [[variance]].

```mathpad
%$2:=abs(sigma)^(-1)*e^((-1/2)*(-mu+x)^2*sigma^(-2))*sqrt(2)^(-1)*sqrt(pi)^(-1)
mu:=0
%$3:=0
sigma:=1/2
%$4:=1/2
%f(x):=1/sqrt(2pi*sigma^2)*e^(-(x-mu)^2/(2sigma^2))
plot(f(x), [-4,4], [0,1])==?
```


A **standard normal distribution** is defined as a normal distribution with $\mu=0$ and $\sigma=1$, which looks like
$$N(x;0,1)=\frac{1}{\sqrt{ 2\pi }}e^{-x^{2}/2}$$
### Moments
The central and algebraic [[moment-generating function]] for the Gaussian are
$$M_{X}(t)=E[e^{t(X-\mu)}]=e^{\sigma ^{2}t^{2}/2},\qquad M_{X}^{*}(t)=e^{t\mu}M_{X}(t)=e^{t\mu+t^{2}\sigma ^{2}/2}$$
For a standard normal distribution, they simplify to
$$M_{X}(t)=e^{t^{2}/2},\qquad M_{X}^{*}(t)=e^{t+t^{2}/2}$$


The expected value is
$$E[X]=\mu=\frac{1}{\sqrt{ 2\pi \sigma ^{2} }}\int_{-\infty}^{\infty} xe^{(x-\mu)^{2}/2\sigma ^{2}} \ dx$$
The variance is
$$\text{var}(X)=\sigma ^{2}=\frac{1}{\sqrt{ 2\pi \sigma ^{2} }}\int_{-\infty}^{\infty} x^{2}e^{(x-\mu)^{2}/2\sigma ^{2}} \ dx - \mu ^{2} $$
Generally, the [[Function moments|moments]] are
0. $\mu_{0}^{*}=1$
1. $\mu_{1}^{*}=\mu$ ([[mean]])

0. $\mu_{0}=1$
1. $\mu_{1}=0$
2. $\mu_{2}=\sigma ^{2}$ ([[variance]])
3. $\mu_{3}=0$
4. $\mu_{4}=3\sigma^{4}$

and the coefficients are
1. $\gamma_{1}=0$ ([[skewness]], it is symmetrical around the mean)
2. $\gamma_{2}=0$ ([[kurtosis]])
### Properties
- It is [[Normalization|normalized]]: $\frac{1}{\sqrt{ 2\pi \sigma ^{2} }}\int_{-\infty}^{\infty} e^{(x-\mu)^{2}/2\sigma ^{2}} \ dx=1$.
### As sum of normal variables
A sum of [[independent variables]] $X_{i}$ that are normally distributed is itself a normal distribution:
$$Y=\sum_{i=1}^{n} X_{i}$$
and its MGF is the sum of all the MGF over $x$:
$$M_{Y}^{*}(t)=\prod_{i=1}^{n}M_{X}^{*}(t)$$
Let's consider a set of normal variables $\{X_{i}\}_{i}$ that are all normally distributed with mean $\mu$ and [[variance]] $\sigma ^{2}$. As the number of variables $n$ goes to infinity, the sum distribution goes like
$$N\left( \mu, \frac{\sigma ^{2}}{n} \right)$$
so the deviation tends to go to zero. Now let's consider the variable
$$z=\frac{\bar{x}-\mu}{\frac{\sigma}{\sqrt{ n }}}$$
where $\bar{x}=\frac{1}{n}\sum_{i=1}^{N}x_{i}$. This follows a standard normal distribution.


$$z= \frac{\sum_{i}x_{i}-n\mu}{\sigma \sqrt{ n }}=\sum_{i=1}^{n} \frac{x_{i}-\mu}{\sigma\sqrt{ n }}=\sum_{i=1}^{n} z_{i}$$
