---
wiki-publish: true
aliases:
  - moment
  - algebraic moment
  - central moment
  - raw moment
---
The **moments** of a function are quantities pertaining to the shape of the function's graph. Although general mathematical concepts, they are most commonly used in statistics to describe the shape of a [[probability distribution]]. A real-valued function $f(x)$ has countably infinite moments $\mu^{*}_{n}$, indexed by their order $n$ and defined as
$$\mu^{*}_{n}=\sum_{i=1}^{\infty} x^{n}_{i}f(x_{i}),\qquad \mu^{*}_{n}=\int_{-\infty}^{\infty} x^{n}f(x) \ dx  $$
depending on whether the function is discrete or continuous. These moments are about the origin. A more general form that defines the moments about an arbitrary point $c$ is
$$\mu_{n}=\sum_{i=1}^{\infty} (x_{i}-c)^{n}f(x_{i}),\qquad \mu_{n}=\int_{-\infty}^{\infty} (x-c)^{n}f(x) \ dx $$

Moments have the interesting property that the (infinite) set of all moments fully determines the function $f$. As such, if the set of moments is available, it is possible to draw conclusions about $f$ without using it directly. More realistically, even an incomplete set of moments can give very valuable information about the shape and behavior of $f$.
### For random variables
Moments are particularly useful in the context of [[Random variable|random variables]] since they give information on the distribution they follow. In this context, the moments gain specific interpretations.

Consider a random variable $X$ (assumed continuous; for a discrete one, just change [[integral|integrals]] into [[Serie|series]]). The moments about zero take the name of **raw** or **algebraic moments** of order $n$ and are defined as the [[expected value]] of the $n$-th power of $X$:
$$\mu^{*}_{n}=\text{E}[X^{n}]=\int_{\Omega}x^{n}f_{X}(x)\ dx$$
$f_{X}(x)$ is the [[probability density function]]. The first couple of moments are:
0. $\mu^{*}_{0}=\int_{\Omega}f_{X}(x)\ dx$ is the [[Normalization|normalization condition]] for $f_{X}(x)$.
1. $\mu^{*}_{1}=\int_{\Omega}xf_{X}(x)\ dx=\mu_{X}$ is the expected value ([[mean]]) of $X$, an index of [[central tendency]].

Orders 2 and up don't have a clear interpretation and are therefore mostly unused.

The **central moments** of order $n$ are instead defined as the expected values of powers about the mean:
$$\mu_{n}=E[(X-\mu_{X})^{n}]=\int_{\Omega}(x-\mu_{X})^{n}f_{X}(x)\ dx$$
The first few moments are
0. $\mu_{0}=\int_{\Omega}f_{X}(x)\ dx=\mu^{*}_{0}$ is again the normalization condition for $f_{X}(x)$.
1. $\mu_{1}=\int_{\Omega}(x-\mu_{X})f_{X}(x)\ dx$ is expected value of $x-\mu_{X}$.
2. $\mu_{2}=\int_{\Omega}(x-\mu_{X})^{2}f_{X}(x)\ dx=\sigma ^{2}$ is the [[variance]] of $X$, an index of [[statistical dispersion]].
3. $\mu_{3}=\int_{\Omega}(x-\mu_{X})^{3}f_{X}(x)\ dx$ is an index of asymmetry.
4. $\mu_{4}=\int_{\Omega}(x-\mu_{X})^{4}f_{X}(x)\ dx$ is an index of "tailedness".

Orders 5 and up don't have an easy interpretation. For orders 3 and up, we define **coefficients** or **standardized moments**, which are divided by some power of the variance and are thus scale-independent. The **asymmetry coefficient** $\gamma_{1}$ is called **[[skewness]]** and, just like $\mu_{3}$, it represents how asymmetrical $f_{X}(x)$ is:
$$\gamma_{1}=\frac{\mu_{3}}{\mu_{2}^{3/2}}=\frac{\mu_{3}}{\sigma_{X}^{3}}$$
The higher it is, the more slanted and asymmetrical the distribution is. It is zero if the distribution is symmetrical about $\mu_{X}$.

The **flatness coefficient** $\gamma_{2}$ is called **[[kurtosis]]** and, just like $\mu_{4}$, it represents how tall the "tails" of $f_{X}(x)$ is:
$$\gamma_{2}=\frac{\mu_{4}}{\mu_{2}^{2}}-3=\frac{\mu_{4}}{\sigma^{4}_{X}}-3$$
The $-3$ term is a completely arbitrary choice and was historically decided just so the kurtosis of the [[Gaussian distribution]] would be zero. The higher it is, the taller the "tails" of the distribution (going to $\pm \infty$) are.
#### Equality of distributions with same moments
Say we have two probability density functions $f_{1}(x)$ and $f_{2}(x)$ for the same random variable $X$. If the set of all moments (either raw or central) is the same for both functions, then $f_{1}(x)=f_{2}(x)$.

> [!quote]- Proof
>Expand $f_{1}(x)$ and $f_{2}(x)$ as a [[serie di potenze|power series]]: $f_{1}(x)=\sum_{n=0}^{\infty}a_{n}x^{n}$ and $f_{2}(x)=\sum_{n=0}^{\infty}b_{n}x^{n}$. The difference between the two is
> $$f_{1}(x)-f_{2}(x)=\sum_{n=0}^{\infty} (a_{n}-b_{n})x^{n}$$
> The square of the difference is
> $$[f_{1}(x)-f_{2}(x)]^{2}=\sum_{n=0}^{\infty} c_{n}x^{n}[f_{1}(x)-f_{2}(x)]$$
> and if we integrate over the [[sample space]] $\Omega$ of $X$, we get
> $$\begin{align}
> \int_{\Omega}[f_{1}(x)-f_{2}(x)]^{2}\ dx&=\sum_{n=0}^{\infty} c_{n}\int_{\Omega}x^{n}[f_{1}(x)-f_{2}(x)]\ dx \\
> &=\sum_{n=0}^{\infty} c_{n}\left( \int_{\Omega}x^{n}f_{1}(x)\ dx-\int_{\Omega}x^{n}f_{2}(x)\ dx \right)  \\
> &=\sum_{n=0}^{\infty} c_{n}[\mu_{n,1}^{*}-\mu_{n,2}^{*}] \\
> &=0
> \end{align}$$
> if $\mu_{n,1}^{*}=\mu_{n,2}^{*}$ for all $n$. Thus, $f_{1}(x)=f_{2}(x)$ over all $\Omega$.

If nothing else, this is further proof that the probability distribution of a random variable is unique.