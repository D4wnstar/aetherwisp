---
wiki-publish: true
---
A **probability density function** (**PDF**) is a function associated with a continuous [[random variable]] that gives the [[probability]] that the variable, when measured, falls between a certain range of values. The PDF describes the [[probability distribution]] that the variable follows, though some care should be taken when interpreting individual values of the PDF.

Formally, for a random variable $X$, its probability density function $f_{X}(x)$ is a non-negative [[Integrale secondo Lebesgue|Lebesgue-integrable]] function such that the probability of $X$ falling in the range $[a,b]$ is
$$P[a\leq x\leq b]=\int_{a}^{b}f_{X}(x)dx$$
Unlike the [[probability mass function]], the probability density function does not give probability values alone: it must be integrated to gather the probabilities. In fact, unlike the mass version, the density's image is not limited between 0 and 1 and may output values greater than 1, thus not qualifying as a probability by definition. The *integral* of the density, however, does have an image of $[0,1]$ and fits the needs of a probability. It is therefore convenient to define the following integral of the PDF
$$\int_{-\infty}^{x} f_{X}(u)du=F_{X}(x)$$
as the [[cumulative distribution function]] of $X$. It represents the probability that $X$ will be lower than $x$.