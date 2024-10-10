The **Erlang distribution** is a continuous [[probability distribution]] over non-negative reals $[0,\infty)$. For a [[random variable]] $T$, the [[probability density function]] is
$$f_{T}(x)=\mu\frac{(\mu t)^{k-1}e^{-\mu t}}{(k-1)!}$$
where $\mu$ is the rate parameter and $k$ is the shape parameter.

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
### Moments
The [[expected value]] is
$$E[T]=\frac{k}{\mu}=k\tau$$
and the [[variance]] is
$$\text{var}(T)=\frac{k}{\mu ^{2}}=k\tau ^{2}$$
### Relation to other distribution
If $k=1$, if simplifies to an [[exponential distribution]]. In fact, an Erlang distribution can be derived as a sum of exponential random variables. It is also a special case of the [[Gamma distribution]] with $\alpha=k$ and $\beta=1$.