---
aliases:
  - moment
  - algebraic moment
  - central moment
---
The **moments** of a function are quantities pertaining to the shape of the function's graph. They are most commonly used in statistics to describe the shape of a [[probability distribution]]. A real-valued function $f(x)$ has countably infinite moments $\mu^{*}_{n}$, indexed by their order $n$ and defined as
$$\mu^{*}_{n}=\sum_{i=1}^{\infty} x^{n}_{i}f(x_{i}),\qquad \mu^{*}_{n}=\int_{-\infty}^{\infty} x^{n}f(x) \ dx  $$
depending on whether the function is discrete or continuous. These moments are about the origin. It is possible to have a more general form that defines the moment about an arbitrary point $c$ as
$$\mu_{n}=\sum_{i=1}^{\infty} (x_{i}-c)^{n}f(x_{i}),\qquad \mu_{n}=\int_{-\infty}^{\infty} (x-c)^{n}f(x) \ dx $$

Moments are interesting values because the (infinite) set of all moments for a function $f$ completely determines $f$ and are thus an alternative way of working with the function.
### For random variables
Moments are particularly useful to calculate for [[random variable|random variables]] in order to gain information on the distribution they follow. In this context, the moments gain specific interpretations.

Consider a random variable $X$ (here continuous; discrete just uses [[serie|series]] instead of integrals). The moments about zero take the name of **algebraic** or **raw moments** of order $k$ and are defined as
$$\mu^{*}_{k}=E[X^{k}]=\int_{\Omega}x^{k}f_{X}(x)\ dx$$
where $E$ is the [[expected value]] operator and $f_{X}(x)$ is the [[probability density function]]. The first few moments are:
0. $\mu^{*}_{0}=\int_{\Omega}f_{X}(x)\ dx$ is the [[Normalizzazione|normalization condition]] for $f_{X}(x)$.
1. $\mu^{*}_{1}=\int_{\Omega}xf_{X}(x)\ dx=\mu_{X}$ is the [[mean]] of $X$, an index of position.
2. ...

Orders 2 and up don't have an immediate interpretation and are therefore mostly unused.

The **central moments** of order $k$ are instead defined as the moments about the expectation of $X$, $\mu_{X}$:
$$\mu_{k}=E[(X-\mu_{X})^{k}]=\int_{\Omega}(x-\mu_{X})^{k}f_{X}(x)\ dx$$
The first few moments are
0. $\mu_{0}=\int_{\Omega}f_{X}(x)\ dx=\mu^{*}_{0}$ is again the normalization condition for $f_{X}(x)$.
1. $\mu_{1}=\int_{\Omega}(x-\mu_{X})f_{X}(x)\ dx$ is expectation of $x-\mu_{X}$.
2. $\mu_{2}=\int_{\Omega}(x-\mu_{X})^{2}f_{X}(x)\ dx=\sigma ^{2}$ is the [[variance]] of $X$, an index of [[dispersion]].
3. $\mu_{3}=\int_{\Omega}(x-\mu_{X})^{3}f_{X}(x)\ dx$ is an index of asymmetry.
4. $\mu_{4}=\int_{\Omega}(x-\mu_{X})^{4}f_{X}(x)\ dx$ is an index of "tailedness".
5. ...

Orders 5 and up don't have an easy interpretation. For orders 3 and up, we define **coefficients** or **standardized moments**, which are divided by the variance and thus scale-independent. The **asymmetry coefficient** $\gamma_{1}$ is called [[skewness]] and, just like $\mu_{3}$, it represents how asymmetrical $f_{X}(x)$ is:
$$\gamma_{1}=\frac{\mu_{3}}{\mu_{2}^{3/2}}=\frac{\mu_{3}}{\sigma_{X}^{3}}$$
The higher it is, the more slanted and asymmetrical the distribution is. It is zero if the distribution is symmetrical about $\mu_{X}$.

The **flatness coefficient** $\gamma_{2}$ is called [[kurtosis]] and, just like $\mu_{4}$, it represents how tall the "tails" of $f_{X}(x)$ is:
$$\gamma_{2}=\frac{\mu_{4}}{\mu_{2}^{2}}-3=\frac{\mu_{4}}{\sigma^{4}_{X}}-3$$
The $-3$ term is a completely arbitrary choice and was historically decided just so the kurtosis of the [[Gaussian distribution]] would be zero. The higher it is, the taller the "tails" of the distribution (going to $\pm \infty$) are.
#### Equality of distributions with same moments
Say we have two probability density functions $f_{1}(x)$ and $f_{2}(x)$ for the same random variable $X$. If the set of all moments (either algebraic or central) is the same for both functions, then $f_{1}(x)=f_{2}(x)$.

> [!example] Proof
>Expand $f_{1}(x)$ and $f_{2}(x)$ as a [[serie di potenze|power series]]: $f_{1}(x)=\sum_{k=0}^{\infty}a_{k}x^{k}$ and $f_{2}(x)=\sum_{k=0}^{\infty}b_{k}x^{k}$. The difference between the two is
> $$f_{1}(x)-f_{2}(x)=\sum_{k=0}^{\infty} (a_{k}-b_{k})x^{k}$$
> The square of the difference is
> $$[f_{1}(x)-f_{2}(x)]^{2}=\sum_{k=0}^{\infty} c_{k}x^{k}[f_{1}(x)-f_{2}(x)]$$
> and if we integrate over the [[sample space]] $\Omega$ of $X$, we get
> $$\begin{align}
> \int_{\Omega}[f_{1}(x)-f_{2}(x)]^{2}\ dx&=\sum_{k=0}^{\infty} c_{k}\int_{\Omega}x^{k}[f_{1}(x)-f_{2}(x)]\ dx \\
> &=\sum_{k=0}^{\infty} c_{k}\left( \int_{\Omega}x^{k}f_{1}(x)\ dx-\int_{\Omega}x^{k}f_{2}(x)\ dx \right)  \\
> &=\sum_{k=0}^{\infty} c_{k}[\mu_{k,1}^{*}-\mu_{k,2}^{*}] \\
> &=0
> \end{align}$$
> Thus, $f_{1}(x)=f_{2}(x)$ over all $\Omega$.

If nothing else, this is further proof that the probability distribution of a random variable is unique.