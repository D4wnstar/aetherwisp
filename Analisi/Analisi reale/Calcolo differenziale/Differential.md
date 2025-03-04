---
aliases:
  - differentiable
---
Given a function $f:A\subset \mathbb{R}^{N}\to \mathbb{R}^{M}$ where $A$ is an open subset, and a point $x_{0}\in A$, the function is said to be **differentiable** in $x_{0}$ if there exist a linear function $Df(x_{0}):\mathbb{R}^{N}\to \mathbb{R}^{M}$, called the **differential**, such that
$$\lim\limits_{h \to 0} \frac{f(x_{0}+h) - f(x_{0})-Df(h)}{\lVert h \rVert } = 0\in\mathbb{R}^M$$
where $h\in V$. The differential is
$$Df(x_{0})[v]\equiv \lim_{ h \to 0 } \frac{f(x_{0}-hv)-f(x_{0})}{\lVert h \rVert },\qquad v\in \mathbb{R}^{N}$$
When evaluated on a [[basis]] vector $e_{i}$ in a [[vector space]] $V$, the differential becomes a [[partial derivative]] over that coordinate:
$$Df(x_{0})[e_{i}]=\frac{ \partial f }{ \partial x_{i} } (x_{0})$$
### For real-valued functions
If $f$ is instead $f:A\subset \mathbb{R}^{N}\to \mathbb{R}$, the differential of $f$ is the [[linear functional]] $df:\mathbb{R}^{N}\to \mathbb{R}$ such that $v\to df(x_{0})[v]$. It is a member of the [[dual vector space]] of $V$.

If we specifically take the functions $x_{1},\ldots,x_{n}:\mathbb{R}^{N}\to \mathbb{R}$ that extract the $i$-th component of a vector $v=(v_{1},\ldots,v_{n})\in V$, so $x_{i}(v)=v_{i}$, the differentials of these functions $dx_{i}$ make a [[Dual vector space|dual basis]]. When $dx_{i}$ is applied onto the basis vector $e_{j}$ of $V$ we get
$$dx_{i}[e_{j}]=\frac{ \partial x_{i} }{ \partial x_{j} } =\delta_{ij}$$
using the [[Delta di Kronecker]].

