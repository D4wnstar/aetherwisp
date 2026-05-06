---
hl-publish: true
---
The **Erlang distribution** is a continuous [[Probability distribution]] over non-negative reals $[0,\infty)$. For a [[Random variable]] $X$, the [[Probability density function]] is
$$f_{X}(x;k,\tau)=\frac{1}{(k-1)!} \frac{1}{\tau^{k}}x^{k-1}e^{-x/\tau}$$
where $k\geq 1$ is an integer shape parameter and $\tau$ is a positive real scale parameter. Equivalently, it can be parameterized as
$$f_{X}(x;k,\lambda)=\frac{1}{(k-1)!} \lambda^{k}x^{k-1}e^{-\lambda x}$$
where $\lambda$ is a positive real rate parameter. The two are related by $\lambda=1/\tau$.

It is often used to model the time it takes for $k$ [[Poisson distribution|Poisson-distributed]] events to occur (in a [[Poisson process]]). In this sense, it is the "inverse" of the Poisson distribution, which instead models the number of events in a given time.

The $\mu=1$ is also commonly encountered. The expression for this case is
$$f_{T}(t)=\frac{1}{(k-1)!}t^{k-1}e^{-t}$$
### Moments
The [[Expected value]] and [[Variance]] are
$$\text{E}[X]=k\tau=\frac{k}{\lambda},\qquad\text{var}(X)=k\tau ^{2}=\frac{k}{\lambda ^{2}}$$
### Relation to other distributions
- For $k=1$, we get an [[Exponential distribution]], $\text{Exp}(x;\tau)$. In fact, an Erlang distribution is the sum of $k$ exponential random variables.
- It is a special case of the [[Gamma distribution]] with integer $\alpha=k$.