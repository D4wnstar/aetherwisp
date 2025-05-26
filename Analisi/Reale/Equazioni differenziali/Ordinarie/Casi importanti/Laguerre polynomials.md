---
wiki-publish: true
aliases:
  - Laguerre functions
  - associated Laguerre polynomials
---
The **Laguerre polynomials** are are a sequence of polynomials indexed by a nonnegative integer $n$ given by
$$L_{n}(x)=\frac{e^{x}}{n!} \frac{d^{n}}{dx^{n}}(x^{n}e^{-x})$$
The $n=0$ case is trivial and simply resolves to $L_{0}=1$. These polynomials arise as the nontrivial solutions to [[Laguerre's differential equation]] for nonnegative $n$. More generally, the **Laguerre functions** are the nontrivial solutions for any real $n$, not just integers. An alternate definition uses the generating function
$$U(t,x)=\sum_{n=0}^{\infty} t^{n}L_{n}(x)=\frac{1}{1-t}e^{-tx/(1-t)}$$
The **associated Laguerre polynomials** are the nontrivial solution to the generalized Laguerre differential equation and are given by
$$L_{n}^{(\alpha)}=\frac{x^{-\alpha}e^{ x }}{n!} \frac{d^{n}}{dx^{n}}(x^{n+\alpha}e^{-x})$$
or alternatively the generating function
$$U(t,x;\alpha)=\sum_{n=0}^{\infty} t^{n}L_{n}^{(\alpha)}=\frac{1}{(1-t)^{1+\alpha}}e^{-tx/(1-t)}$$
or even as derivatives of $L_{n}(x)$ if $\alpha \in \mathbb{N}$
$$L_{n}^{(\alpha)}(x)=\frac{d^{\alpha}}{dx^{\alpha}}L_{n}(x)$$

In physics it is common to use an alternative definition of the Laguerre polynomials (both regular and associated) that eschews the $n!$ factor:
$$L_{n}(x)=e^{ x } \frac{d^{n}}{dx^{n}}(x^{n}e^{-x}),\quad L_{n}^{(\alpha)}=x^{-\alpha}e^{ x } \frac{d^{n}}{dx^{n}}(x^{n+\alpha}e^{-x})$$
They are related to the [[Hermite polynomials]] $H_{n}(x)$ by
$$\begin{align}
H_{2n}(x)&=(-1)^{n}2^{n}n!\ L_{n}^{(-1/2)}(x^{2}) \\
H_{2n+1}(x)&=(-1)^{n}2^{n+1}n!\ xL_{n}^{(1/2)}(x^{2})
\end{align}$$
