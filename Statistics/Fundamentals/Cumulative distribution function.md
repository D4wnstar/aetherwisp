---
wiki-publish: true
aliases:
  - CDF
---
A **cumulative distribution function** (**CDF**) is a function associated with a [[random variable]] that gives the [[probability]] that the variable will take a value less than or equal to some value $x$.

Formally, for a random variable $X$, its cumulative density function $F_{X}(x)$ is
$$F_{X}(x)= P(X\leq x)$$
where $P$ is a [[measure]] of probability. The probability that $X$ lies within the semi-closed interval $]a,b]$ is
$$P(a\leq x\leq b)=F_{X}(b)-F_{X}(a)$$
If $X$'s [[probability distribution]] has a [[probability density function]] $f_{X}(x)$, we can state
$$f_{X}(x)=\frac{d}{dx}F_{X}(x),\quad F_{X}(x)=\int_{-\infty}^{x}f_{X}(u)du$$
In this case, the CDF is said to **identify** the distribution.
### Properties
- $F(-\infty)=0$
- $F(+\infty)=1$
- The inverse of the CDF is defined as $F^{-1}(p)=\min(x|F(x)\geq p)$ where $0\leq p\leq 1$. If $F$ is continuous, this is equivalent to the usual definition of inverse. $F^{-1}$ is the [[quantile function]].
- If $F$ is continuous, then the random variable $W=F_{X}(X)$ follows a [[uniform distribution]]. If it does, then the random variable $X=F^{-1}_{X}(W)$ has $F$ as its CDF[^1].
- The CDF can exist even if the PDF doesn't: for instance, discrete probability distributions have a CDF without a PDF. More generally, a probability distribution has a PDF if and only if its CDF is [[absolute continuity|absolutely continuous]].
#### Empirical CDF
The **empirical cumulative distribution function** (**ECDF**) is the CDF that is obtained from empirical measurements. Since measurements are discrete, the ECDF is always discrete. As the empirical data increases in number, the ECDF starts to approximate a continuous CDF.

[^1]: Basically, you can freely convert between $X$ and $W$ as long as you know $F_{X}$ and its inverse $F^{-1}_{X}$. This might seem like a forgettable property, but it's central to the [[inversion sampling method]] for generating data following a PDF $f_{X}(x)=\int_{-\infty}^{\infty}F_{X}(x)dx$.
