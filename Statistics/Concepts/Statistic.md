---
wiki-publish: true
aliases:
  - sufficient statistic
---
A **statistic** is a function of a statistical [[sample]], in the sense of a [[set]] of [[random variable|random variables]]. It is itself a random variable. Examples include the sample [[mean]] and sample [[variance]].
### Sufficient statistic
Given a [[Random variable|random vector]] $\mathbf{X}$ of [[Probability density function|PDF]] $f_{\mathbf{X}}(x;\theta)$ ($\theta$ is a parameter), a statistic $t(\mathbf{X})$ is said to be **sufficient** for $\theta$ if it such that $f_{\mathbf{X}}(x;\theta)$ can be written as
  $$f_{X}(x;\theta)=h(\mathbf{X})g(t(\mathbf{X});\theta)$$
where $h$ is a statistic that is independent of $\theta$ and $g$ is a statistic that depends on $\mathbf{X}$ only through $t(\mathbf{X})$. All the information available on $\theta$ contained in $\mathbf{X}$ is supplied by $t(\mathbf{X})$.

Given a vector of [[iid]] [[Gaussian distribution|Gaussian]] random variables, $X_{i}\sim \mathcal{N}(\mu,\sigma ^{2})$, the parameters $\boldsymbol{\theta}$ are $\boldsymbol{\theta}=(\mu,\sigma ^{2})$. The PDF of the random vector is a [[Multivariate normal distribution|multivariate normal]]:
$$\begin{align}
f(\mathbf{X};\boldsymbol{\theta})&=\prod_{i=1}^{N} \frac{1}{\sqrt{ 2\pi }\sigma}\exp\left( - \frac{1}{2\sigma ^{2}}(x_{i}-\mu)^{2} \right) \\
&=\frac{1}{(\sqrt{ 2\pi })^{N}\sigma^{N}}\exp\left( - \frac{1}{2\sigma ^{2}}\sum_{i=1}^{N} (y_{i}-\mu)^{2} \right)
\end{align}$$
It can be proven that the statistic $t(\mathbf{X})=(\bar{y},s^{2})$ is sufficient for $\boldsymbol{\theta}$. $\bar{y}$ and $s^{2}$ are the sample mean and sample variance of the random vector (interpreted as a sample).