The **Erlang distribution** is a continuous [[probability distribution]] over non-negative reals $[0,\infty)$. For a [[random variable]] $T$, the [[probability density function]] is
$$f_{T}(t)=\mu\frac{(\mu t)^{k-1}e^{-\mu t}}{(k-1)!}$$
where $\mu$ is the rate parameter and $k$ is the shape parameter. Another common parameterization is using $\tau=1/\mu$.

```mathpad
mu:=2
%$1:=2
k:=2
%$2:=2
%$3:=4*e^(-2*t)*factorial(1)^(-1)*t
%f(t):=mu*(mu*t)^(k-1)*e^(-mu*t)/(k-1)!
plot(f(t), [0,5], [0,1])==?
```


It is often used to model the time it takes for a given number of [[Poisson distribution|Poisson-distributed]] events to occur. In this way, it is the dual of the Poisson distribution, which instead models the number of events in a given time.

The $\mu=1$ is also commonly encountered. The expression for this case is
$$f_{T}(t)=\frac{1}{(k-1)!}t^{k-1}e^{-t}$$
### Moments
The [[expected value]] and [[variance]] are
$$E[T]=\frac{k}{\mu}=k\tau,\qquad\text{var}(T)=\frac{k}{\mu ^{2}}=k\tau ^{2}$$
and in the $\mu=1$ case
$$E[T]=k,\qquad\text{var}(T)=k$$
### Relation to other distribution
If $k=1$, if simplifies to an [[exponential distribution]]. In fact, an Erlang distribution can be derived as a sum of exponential random variables. It is also a special case of the [[Gamma distribution]] with $\alpha=k$ and $\beta=1$.