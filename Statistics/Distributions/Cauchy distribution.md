The **Cauchy distribution** is a real, continuous, univariate [[probability distribution]]. For a [[random variable]] $X$, the [[probability density function]] is
$$f_{X}(x)=\frac{1}{\pi} \frac{1}{1+x^{2}}$$
Notably, it has no parameters.

```mathpad
%$1:=(1+x^2)^(-1)*pi^(-1)
f(x):=(1/pi)1/(1+x^2)
plot(f(x), [-5,5], [0,0.5])==?
```

The shape is similar to that of the [[Gaussian distribution]], but the Cauchy distribution is considerably less well-behaved.
### Moments
The [[expected value]] is
$$E[X]=\int_{-\infty}^{\infty} \frac{1}{\pi} \frac{x}{1+x^{2}} \ dx =\frac{1}{\pi} \frac{1}{2}\ln(1+x^{2})|_{\infty}^{\infty}=\text{undefined}$$
which means that the Cauchy distribution has no expected value. The [[variance]] instead is
$$\text{var}(X)=\int_{-\infty}^{\infty} \frac{1}{\pi} \frac{x^{2}}{1+x^{2}} \ dx \to \infty$$
which tends to infinity (this is somewhat improper notation, formally the bounds of the integral should be some value $a$ and this expression becomes true in the limit $a\to \infty$). Notably, the lack of a well-defined expectation and variance imply that [[Chebyshev's inequality]] does not hold and neither does the [[central limit theorem]].
### Sum of variables
It can be proven that the sum of Cauchy-distributed [[iid]] variables is itself a Cauchy distribution.
### Relation to other distributions
The ratio $Y=\frac{X_{1}}{X_{2}}$ of two [[Gaussian distribution|standard-normally-distributed]] iid variables $X_{1},X_{2}\sim N(0,1)$ is a Cauchy distribution.