---
wiki-publish: true
aliases:
  - PDF
---
A **probability density function** (**PDF**) is a function associated with a continuous [[Random variable]] that gives the [[Probability]] that the variable, when measured, falls between a certain range of values. The PDF describes the [[Probability distribution]] that the variable follows, though some care should be taken when interpreting individual values of the PDF.

Formally, for a random variable $X$, its probability density function $f_{X}(x)$ is a non-negative [[Integrale secondo Lebesgue|Lebesgue-integrable]] function such that the probability of $X$ falling in the range $[a,b]$ is
$$P[a\leq x\leq b]=\int_{a}^{b}f_{X}(x)dx$$
Unlike the [[Probability mass function]], the probability density function does not give probability values alone: it must be integrated to gather the probabilities. In fact, unlike the mass version, the density's image is not limited between 0 and 1 and may output values greater than 1, thus not qualifying as a probability by definition. The *integral* of the density, however, does have an image of $[0,1]$ and fits the needs of a probability. It is therefore convenient to define the following integral of the PDF
$$\int_{-\infty}^{x} f_{X}(u)du=F_{X}(x)$$
as the [[Cumulative distribution function]] of $X$. It represents the probability that $X$ will be lower than $x$.
### Transformations
Given a continuous random variable $X$ of PDF $f_{X}$ and an invertible [[transformation]] $g(x)$, we can define the transformed random variable as $Y=g(X)$. The PDF of $Y$ is
$$f_{Y}(y)=f_{X}(g^{-1}(y)) \left\lvert  \frac{dx}{dy}  \right\rvert $$
The same definition applies to a continuous [[Random variable|random vector]] $\mathbf{X}$ that is invertibly transformed into another random vector $\mathbf{Y}=g(\mathbf{X})$, except that the derivative becomes the [[determinant]] of the [[Jacobian]] of $\mathbf{X}$ with respect to $\mathbf{Y}$:
$$f_{\mathbf{Y}}(\mathbf{y})=f_{\mathbf{X}}(g^{-1}(\mathbf{y}))\ \lvert \mathrm{J} \rvert \quad\text{where}\quad J_{ij}=\frac{ \partial x_{i} }{ \partial y_{j} } $$
