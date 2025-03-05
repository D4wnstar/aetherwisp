The **chain rule** is a formula that expresses the derivative of the composition of two functions. Given two real univariate functions $f(t)$ and $g(t)$, their composition is $h(t)=g(f(t))=(g\circ f)(t)$. The derivative of $h$ is
$$h'(t)=g'(f(t))f'(t)$$
This can be extended to arbitrary dimensions. Say now that $f$ and $g$ are defined as $f:\mathbb{R}^{N}\to \mathbb{R}^{M}$ and $g:\mathbb{R}^{M}\to \mathbb{R}^{L}$. The composition is now $h:\mathbb{R}^{N}\to \mathbb{R}^{L}$. The [[differential]] of $h$ is given by
$$Dh(t)=D(g\circ f)(t)=Dg(f(t))\cdot Df(t)$$
For a [[partial derivative]] of the $a$-th component of $h$ in the $b$-th argument of $f$, and calling $x_{j}$ the arguments of $g$, it reads as
$$\frac{ \partial h_{a} }{ \partial t_{b} }(t)=\sum_{j}\left.{\frac{ \partial g_{a} }{ \partial x_{j} }}\right|_{x=f(t)} \frac{ \partial f_{j} }{ \partial t_{b} } (t) $$
where the vertical bar denotes that the derivative of $g_{a}$ is evaluated in $f(t)$.