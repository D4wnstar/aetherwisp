---
aliases:
  - binomial expansion
---
The **binomial theorem**, or **binomial expansion**, describes the algebraic expansion of powers in a binomial $(x+y)^{n}$. $n$ is typically an integer, but there are generalization for real and complex numbers as well, which are particularly useful to approximate square roots.

> [!info] Binomial theorem
> Given a binomial $(x+y)^{n}$ where $n$ is a nonnegative integer, its expansion is of the form
> $$(x+y)^{n}=\sum_{k=0}^{n}\begin{pmatrix}n \\ k\end{pmatrix}x^{n-k}y^{k}=\sum_{k=0}^{n}\begin{pmatrix}n \\ k\end{pmatrix}x^{k}y^{n-k}$$
> where the **binomial coefficient** is defined as
> $$\begin{pmatrix}n \\ k\end{pmatrix}=\frac{n!}{k!(n-k)!}$$

Newton also devised a generalization that allows the binomial theorem to apply to real and complex exponents too. Here, the finite sum becomes as [[Serie|series]].

> [!info] Generalized binomial theorem
> Given a binomial $(x+y)^{r}$ where $x$ and $y$ are real numbers such that $|x|>|y|$ and $r$ is any complex number, its expansion is of the form
> $$(x+y)^{r}=\sum_{k=0}^{\infty} \begin{pmatrix}r \\ k\end{pmatrix}x^{r-k}y^{k}$$
> where the binomial coefficient is defined as
> $$\begin{pmatrix}r \\ k\end{pmatrix}=\frac{(r)_{k}}{k!}$$
> with $(r)_{k}=r(r-1)\ldots(r-k+1)$ the [[falling factorial]] function.

This generalization gives rise to useful approximations for the square root and its inverse, where $r=1/2$ and $r=-1/2$ respectively:
$$\sqrt{ 1+x }=1+ \frac{1}{2}x- \frac{1}{8}x^{2}+ \frac{1}{16}x^{3} - \frac{5}{128}x^{4}+\ldots$$
$$\frac{1}{\sqrt{ 1+x }}=1- \frac{1}{2}x+ \frac{3}{8}x^{2}- \frac{5}{8}x^{3}+ \frac{35}{128}x^{4}+\ldots$$
$$\frac{1}{\sqrt{ 1-x }}=1+ \frac{1}{2}x+ \frac{3}{8}x^{2}+ \frac{5}{8}x^{3}+ \frac{35}{128}x^{4}+\ldots$$
These approximations are best when $x$ is very small.