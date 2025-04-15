Given a space of functions $U$, a **functional** defined on $U$ is a map $F$ that maps a function $u\in U$ to a [[scalar]] number:
$$\begin{align}
F:\;&U\to \mathbb{R} \\
&u\to F[u]\in \mathbb{R}
\end{align}$$
where we chose real numbers. Functionals can also be dependent on multiple functions:
$$\begin{align}
F:\;&U\times U\times\ldots\times U\to \mathbb{R} \\
&(u_{1},\ldots,u_{n})\to F[u_{1},\ldots,u_{n}]\in \mathbb{R}
\end{align}$$
### Properties
- A functional is linear if $F[\alpha u+\beta v]=\alpha F[u]+\beta F[v]$.
### Variation
The **variation** $\delta F$ of a functional $F$ in some point $u_{0}$ relative to the variation $\delta u$ is defined as
$$\delta F[u_{0},\delta u]\equiv \left.{\frac{d}{d\alpha} F[u_{0}+\alpha u]}\right|_{\alpha=0}$$
It is itself a functional, which takes two functions as an argument. It is fundamentally an extension of the [[directional derivative]] for a functional. In fact, for a *function* $F:U\subset \mathbb{R}^{N}\to \mathbb{R}$ , the directional derivative $\delta F$ on a direction vector $\delta \mathbf{x} \in \mathbb{R}^{N}$ is:
$$\delta F(\mathbf{x},\delta \mathbf{x})=\left.{\frac{d}{d\alpha}F(\mathbf{x}+\delta \mathbf{x})}\right|_{\alpha=0}=\left.{\sum_{i=1}^{N} \frac{ \partial F }{ \partial x_{i} } (\mathbf{x}+\delta \mathbf{x})\delta \mathbf{x}_{i}}\right|_{\alpha=0}=\sum_{i=1}^{N} \frac{ \partial F }{ \partial x_{i} } (\mathbf{x})\delta \mathbf{x}_{i}=\nabla F\cdot \delta \mathbf{x}$$
Similarly to usual derivatives, the functional $F$ is said to be **stationary** in $u_{0}$ if $\delta F[u_{0},\delta u]=0$. Furthermore, if we define $\Delta F=F[u+\delta u]-F[u]$ for some *small* $\delta u$, $\delta F$ is the **linear part** of $\delta u$ of the increase $\Delta F$.
### Examples
Let $U=\{ \text{smooth functions}:[0,1]\to \mathbb{R} \}$.

> [!example] Integral over set extrema
> An example of a function from $U$ to $\mathbb{R}$ is
> $$F[u]=\int_{0}^{1}u(t)dt$$
> If for instance $u(t)=\sin \pi t$, the functional would give us
> $$F[\sin \pi t]=\int_{0}^{1}\sin \pi t\ dt=\frac{1}{\pi}\int_{0}^{\pi}\sin \xi\ d\xi=\frac{2}{\pi}$$

> [!example] Maxima and minima
> Another example is
> $$F[u]=u(t_{0})=1$$
> which gives us the value $t_{0}$ for which the function is equal to $1$. With our previous $u$:
> $$F[\sin \pi t]=\sin(\pi t_{0})=1\quad\to \quad t_{0}= \frac{1}{2}$$
> One could also do the same thing to find the zeros of a derivative:
> $$F[u]=u'(t_{0})=0$$
> This statement is in essence a compact way of expressing the search for maxima and minima of $u$.

> [!example] Curve length
> An example of a functional of several functions is the length of a [[curve]]. Given some curve in $\mathbb{R}^{3}$, $\gamma(t)=(u(t),v(t),w(t))$, its length is the functional
> $$F[u,v,w]=\int_{0}^{1}\sqrt{ u'(t)^{2}+v'(t)^{2}+w'(t)^{2} }\ dt$$

> [!example] Variation of an integral
> Consider again the first example, where $F[u]=\int_{0}^{1}u(t)dt$. Its variation over a generic direction $\delta u$ is
> $$\delta F[u,\delta u]=\left.{\frac{d}{d\alpha} \left( \int_{0}^{1}(u+\alpha \delta u) dt\right)}\right|_{\alpha=0}=\int_{0}^{1}\delta u(t)\ dt$$
> The increment $\Delta F$ is
> $$\Delta F=\int_{0}^{1}(u+\delta u)dt-\int_{0}^{1}udt=\int_{0}^{1}\delta u\ dt$$
> 
> If we now take the integral of the *square* of the function $F[u]=\int_{0}^{1}u(t)^{2}dt$ we get
> $$\delta F[u,\delta u]=\left.{\frac{d}{d\alpha}\left( \int_{0}^{1}(u+\alpha \delta u)^{2}dt \right)}\right|_{\alpha=0}=\left.{\int_{0}^{1}2(u+\alpha \delta u)\delta udx}\right|_{\alpha=0}=2\int_{0}^{1}u(x)\delta u(x)dx$$
> and the increment is
> $$\Delta F=\int_{0}^{1}(u^{2}+2u\delta u+\delta u^{2})dx-\int_{0}^{1}u^{2}dx=2\int_{0}^{1} u\delta udx+\int_{0}^{1} \delta u^{2}dx$$
