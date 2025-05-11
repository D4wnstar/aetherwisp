---
wiki-publish: true
---
The **exact differential** of a multivariate function $f(x,y):\mathbb{R}^{2}\to \mathbb{R}$ is defined as the [[differential form]]
$$df=\frac{ \partial f }{ \partial x } dx+\frac{ \partial f }{ \partial y } dy$$
where the arguments $x$ and $y$ are independent of each other. It is a specific form of the [[differential]] for a [[scalar field]]. This is a specific case of the general differential form
$$df=g(x,y)dx+h(x,y)dy$$
where $g=\frac{ \partial f }{ \partial x }$ and $h=\frac{ \partial f }{ \partial y }$. The definition can be extended to an arbitrary $N$-dimensional function $f(x_{1},\ldots,x_{n}):\mathbb{R}^{N}\to \mathbb{R}$ as
$$df=\sum_{i=1}^{N} \frac{ \partial f }{ \partial x_{i} }dx_{i} $$

$df$ is exact if and only if $f$ is a multivariate function whose arguments are independent of each other, that is, changing one has no effect on the others.

The benefit of an exact differential is that any integral over it is independent of the [[Curve|path]] chosen, such that for any two paths $\gamma_{1}$ and $\gamma_{2}$ defined in $f$'s domain we have
$$\int_{\gamma_{1}}df=\int_{\gamma_{2}}df$$
In thermodynamics, a function that has an exact differential and determines the [[stato|state]] of a [[physical system]] is called an [[equation of state]].