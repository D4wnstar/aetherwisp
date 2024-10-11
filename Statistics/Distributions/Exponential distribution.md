The **exponential distribution** is a continuous [[probability distribution]] over non-negative reals $[0,\infty)$. For a [[random variable]] $X$, the [[probability density function]] is
$$f_{X}(x)=\frac{1}{\tau}e^{-x/\tau}$$
where $\tau$ is a parameter that is usually a characteristic time.

```mathpad
tau:=1
%$1:=1
%$2:=(1/3)*e^((-1/3)*x)
%f(x):=1/tau*e^(-x/tau)
plot(f(x), [0,5], [0,1])==?
```


This distribution is commonly used in physics to model the wait times of random independent events, such a [[Decadimento nucleare|radioactive]] or [[Decadimento di particelle|particle decay]].
### Moments
The algebraic and central [[Moment-generating function|moment-generating functions]] are
$$M^{*}_{X}(t)=\frac{1}{1-t\tau},\qquad M_{X}(t)=\frac{e^{-t\tau}}{1-t\tau}$$

The [[expected value]] is
$$\mu_{X}=\int_{0}^{\infty}xf_{X}(x)\ dx=\tau$$
and the [[variance]] is
$$\sigma ^{2}_{X}=\int_{0}^{\infty}(x-\tau)^{2}f_{X}(x)\ dx=\tau ^{2}$$

The [[Function moments|moments]] are
0. $\mu_{0}^{*}=1$
1. $\mu_{1}^{*}=\tau$ ([[mean]])

0. $\mu_{0}=1$
1. $\mu_{1}=0$
2. $\mu_{2}=\tau ^{2}$ ([[variance]])
3. $\mu_{3}=2\tau ^{3}$
4. $\mu_{4}=9\tau^{4}$

The coefficients are
1. $\gamma_{1}=2$ ([[skewness]], it asymmetrical around the mean)
2. $\gamma_{2}=6$ ([[kurtosis]])
### Properties
It is [[Normalizzazione|normalized]] with a constant of $c=1$.
### Relation to other distributions
The sum of several exponential random variables, all with the same parameter $\tau$, is an [[Erlang distribution]].