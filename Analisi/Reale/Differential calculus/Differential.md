---
aliases:
  - differentiable
---
Given a function $f:A\subset \mathbb{R}^{N}\to \mathbb{R}^{M}$ where $A$ is an open subset, and a point $x_{0}\in A$, the function is said to be **differentiable** in $x_{0}$ if there exist a linear map[^1] $Df(x_{0}):\mathbb{R}^{N}\to \mathbb{R}^{M}$, called the **differential**, such that
$$\lim\limits_{h \to 0} \frac{f(x_{0}+h) - f(x_{0})-Df(h)}{\lVert h \rVert } = 0\in\mathbb{R}^M$$
where $h\in V$. The differential is
$$Df(x_{0})[v]\equiv \lim_{ h \to 0 } \frac{f(x_{0}-hv)-f(x_{0})}{\lVert h \rVert },\qquad v\in \mathbb{R}^{N}$$
and represents a generalized form of the idea of "rate of change" that the normal derivative represents. This rate of change is evaluated in a certain point $x_{0}$ in space and in the direction given by $v$.

When evaluated on a [[Basis]] vector $e_{i}$ in a [[Vector space]] $V$, the differential becomes a [[partial derivative]] over that coordinate:
$$Df(x_{0})[e_{i}]=\frac{ \partial f }{ \partial x_{i} } (x_{0})$$

A more specific and particularly useful form is the [[Exact differential]].
### For real-valued functions
If we set $M=1$, $f$ is instead a real-valued function $f:A\subset \mathbb{R}^{N}\to \mathbb{R}$. Its differential is the [[linear functional]] $df:\mathbb{R}^{N}\to \mathbb{R}$ such that $v\to df(x_{0})[v]$. It is a member of the [[Dual vector space]] of $V$.

If we specifically take the functions $x_{1},\ldots,x_{n}:\mathbb{R}^{N}\to \mathbb{R}$ that extract the $i$-th component of a vector $v=(v_{1},\ldots,v_{n})\in V$, so $x_{i}(v)=v_{i}$, the differentials of these functions $dx_{i}$ make a [[Dual vector space|dual basis]]. When $dx_{i}$ is applied onto the basis vector $e_{j}$ of $V$ we get
$$dx_{i}[e_{j}]=\frac{ \partial x_{i} }{ \partial x_{j} } =\delta_{ij}$$
using the [[Kronecker delta]].
### For invertible functions
Consider an invertible function $\varphi:\mathbb{R}^{N}\to \mathbb{R}^{N}$. These are particularly useful for coordinates changes. The differential $D\varphi(x_{0})$ of such a function is a square $N\times N$ matrix. The [[Jacobian]] in some basis $\{ e_{k} \}$ is a square matrix given by the elements
$$J_{ki}=e_{k}\cdot D\varphi[e_{k}]=e_{k}\cdot \frac{ \partial \varphi }{ \partial x_{i} }=\frac{ \partial \varphi_{k} }{ \partial x_{i} }$$
where $\varphi_{k}$ is the $k$-th component of $\varphi$.

[^1]: Here linear map does *not* mean linear function. It is a general operation which obeys the general linear property $f(\alpha v+\beta w)=\alpha f(v)+\beta f(w)$.
