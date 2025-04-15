---
aliases:
  - differentiable
  - total derivative
  - exact differential
---
Given a function $f:A\subset \mathbb{R}^{N}\to \mathbb{R}^{M}$ where $A$ is an open subset, and a point $x_{0}\in A$, the function is said to be **differentiable** in $x_{0}$ if there exist a [[linear map]][^1] $Df(x_{0}):\mathbb{R}^{N}\to \mathbb{R}^{M}$, called the **differential**, such that
$$\lim\limits_{h \to 0} \frac{f(x_{0}+h) - f(x_{0})-Df(h)}{\lVert h \rVert } = 0\in\mathbb{R}^M$$
where $h\in V$. The differential is
$$Df(x_{0})[v]\equiv \lim_{ h \to 0 } \frac{f(x_{0}-hv)-f(x_{0})}{\lVert h \rVert },\qquad v\in \mathbb{R}^{N}$$
and represents a generalized form of the idea of "rate of change" that the normal derivative represents. This rate of change is evaluated in a certain point $x_{0}$ in space and in the direction given by $v$.

When evaluated on a [[basis]] vector $e_{i}$ in a [[vector space]] $V$, the differential becomes a [[partial derivative]] over that coordinate:
$$Df(x_{0})[e_{i}]=\frac{ \partial f }{ \partial x_{i} } (x_{0})$$
### For real-valued functions
If we set $M=1$, $f$ is instead a real-valued function $f:A\subset \mathbb{R}^{N}\to \mathbb{R}$. Its differential is a linear [[functional]] and is typically denoted as $df:\mathbb{R}^{N}\to \mathbb{R}$ such that $v\to df(x_{0})[v]$. Being a linear function, it is a member of the [[dual vector space]] of $V$. Like before,
$$df(x_{0})[e_{i}]=\frac{ \partial f }{ \partial x_{i} } (x_{0})$$

If we specifically take the functions $x_{1},\ldots,x_{n}:\mathbb{R}^{N}\to \mathbb{R}$ that extract the $i$-th component of a vector $v=(v_{1},\ldots,v_{n})\in V$, so that $x_{i}(v)=v_{i}$, the differentials of these functions $\{ dx_{i} \}_{i=1,\ldots,N}$ make a [[Dual vector space|dual basis]] of $\{ e_{i} \}_{i=1,\ldots,N}$. $df(x)$ can be expressed in this basis as
$$df(x_{0})=\sum_{i=1}^{N} \frac{ \partial f }{ \partial x_{i} } (x_{0})dx_{i}$$
The differential in general goes by a few names, **total/exact derivative/differential**, but the name "total derivative" is especially common to refer to the form above, used to extend the concept of derivative in the most straightforward way possible. For instance, the total derivative of a function $f(x(t),y(t),t)$ in $t$ is, using the [[chain rule]],
$$\frac{df}{dt}=\sum_{i=1}^{2} \frac{ \partial f }{ \partial x_{i} } \frac{dx_{i}}{dt}+\frac{ \partial f }{ \partial t } \frac{dt}{dt}=\frac{ \partial f }{ \partial x } \frac{dx}{dt}+\frac{ \partial f }{ \partial y } \frac{dy}{dt}+\frac{ \partial f }{ \partial t } $$

It is related to the [[gradient]] by
$$\begin{align}
df(x_{0})[v]&=\sum_{i=1}^{N} \frac{ \partial f }{ \partial x_{i} } (x_{0})dx_{i}\ v=\sum_{i=1}^{N} \frac{ \partial f }{ \partial x_{i} } (x_{0})dx_{i}\sum_{j=1}^{N} v_{i}e_{i}=\sum_{i=1}^{N} \frac{ \partial f }{ \partial x_{i} } \sum_{j=1}^{N} v_{j}\underbrace{ dx_{i}[e_{j}] }_{ \delta_{ij} }= \\
&=\sum_{i=1}^{N} \frac{ \partial f }{ \partial x_{i} } v_{i}=\nabla f\cdot v
\end{align}$$
using the [[Kronecker delta]] $\delta_{ij}$.

When $dx_{i}$ is applied onto the basis vector $e_{j}$ of $V$ we get
$$dx_{i}[e_{j}]=\frac{ \partial x_{i} }{ \partial x_{j} } =\delta_{ij}$$
using the [[Kronecker delta]].
### Matrix representation
If the differential is a [[Operatore lineare|linear operator]] from $\mathbb{R}^{N}$ to $\mathbb{R}^{M}$, it can be represented as an $N\times M$ square matrix. This matrix is exactly the [[Jacobian]] matrix of $f$. In fact, for a linear operator, its matrix elements in a given basis $\{ e_{i} \}_{i=1,\ldots,N}$ are given by
$$J_{ij}=e_{i}\cdot Df(x_{0})[e_{j}]=e_{i}\cdot \frac{ \partial f }{ \partial x_{j} } =\frac{ \partial f_{i} }{ \partial x_{j} } $$
which is the matrix of all first-order partial derivatives of $f$, i.e. its Jacobian.

[^1]: Here linear map does *not* necessarily mean linear function. It is a general operation which obeys the general linear property $f(\alpha v+\beta w)=\alpha f(v)+\beta f(w)$.
