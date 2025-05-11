---
wiki-publish: true
---
A **cumulative distribution function** (**CDF**) is a function associated with a [[random variable]] that gives the [[probability]] that the variable will take a value less than or equal to some value $x$.

Formally, for a random variable $X$, its cumulative density function $F_{X}(x)$ is
$$F_{X}(x)= P(X\leq x)$$
where $P$ is a [[measure]] of probability. The probability that $X$ lies within the semi-closed interval $]a,b]$ is
$$P(a\leq x\leq b)=F_{X}(b)-F_{X}(a)$$
If $X$'s [[probability distribution]] has a [[probability density function]] $f_{X}(x)$, we can write
$$f_{X}(x)=\frac{d}{dx}F_{X}(x),\quad F_{X}(x)=\int_{-\infty}^{x}f_{X}(u)du$$
It is not necessary for the PDF to exist for the CDF to exist: for instance, discrete probability distributions have a CDF without a PDF. More generally, a probability distribution has a PDF if and only if its CDF is [[absolute continuity|absolutely continuous]].