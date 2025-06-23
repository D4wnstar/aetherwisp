---
wiki-publish: true
---
Motion as described from the [[Lagrange equation]] is said to be **local**, as it evaluates motion point-wise in time. The opposite is **global** motion, which is determined from global properties of the entire [[Physical system|system]] instead of local ones. It is easiest to explain by example.

In $\mathbb{R}^{2}$, we can say that an object, like a [[point mass]], begins its motion in $x_{\text{start}}$ and ends it in $x_{\text{end}}$. Its coordinates $x$ and $y$ are bound by some function $u(x)=y$, which describes a locus of points in $\mathbb{R}^{2}$ that says where the particle can be found. This space can be described as a [[curve]] $\gamma$, its *trajectory*. The length of $u$ is its [[measure]] and can be found through a [[functional]]:
$$F[u]=\int_{x_{\text{start}}}^{x_{\text{end}}}\sqrt{ 1+u'(x)^{2} }\ dx$$
The length is a global property: it affects the whole motion, not just one piece at one time. As such, we can use it to set a condition for the motion to satisfy. For example, we can state the we want only the motion that leads to the shortest trajectory between $x_{\text{start}}$ and $x_{\text{end}}$[^1]. In other words, we want whatever motion minimizes $F[u]$. For it to be minimum, $u'(x)^{2}$ needs to be $0$, which means that the shortest trajectory must be one for which $u'(x)=0$ everywhere. But this is just a constant, $u(x)=y_{0}$, which is a straight line. This shouldn't be surprising: the shortest way from point A to point is B *is* a straight line after all.

Another useful property to minimize is the **travel time**, the time it takes for the particle to go from one end to the other. In other words, we're now looking not for the *shortest* path, but the *fastest* path, which may not be the same. To do so, we minimize the following functional:
$$T[u]=\int_{\gamma} \frac{ds}{v}=\int_{x_{\text{start}}}^{x_{\text{end}}} \frac{\sqrt{ 1+u'(x)^{2} }}{v(x,u(x))}dx$$
where the velocity is dependent on the position of the particle. This comes up a few times in physics.

> [!example] 2D conservative system
> A 2D [[conservative system]] has velocity given by
> $$v(x,y)=\sqrt{ \frac{2}{m}(E-V(x,y)) }$$
> Say the [[potential energy]] is given by [[Interazione gravitazionale|gravity]], we get velocity $v=\sqrt{ 2gy }$. Our functional becomes
> $$T[u]=\int_{x_{\text{start}}}^{x_{\text{end}}}\sqrt{ \frac{1+u'(x)^{2}}{2gu(x)} }dx$$
Finding the minimum gives us the correct trajectory.

> [!example] Beams of light
> Another times this comes up is in optics. Its been known for a long time throughout history that light follows the path that minimizes travel time, so the trajectory of a ray of light can be described with this very functional. The speed of light as it travels through space is given by $v=c/n(x,y)$, where $n$ is the [[refractive index]] of whichever material the ray is in at a certain point, so we are looking to minimize
> $$T[u]=\frac{1}{c}\int_{x_{\text{start}}}^{x_{\text{end}}}n(x,u(x))\sqrt{ 1+u'(x)^{2} }\ dx$$

These are nice example, but the meat of the discussion is in the minimization of a different quantity: the [[Lagrangian]]. Consider some Lagrangian $L:\mathbb{R}^{3}\to \mathbb{R}$, $L\equiv L(u,u',x)$. Our functional here is
$$F[u]=\int_{x_{\text{start}}}^{x_{\text{end}}}L(u(x),u'(x),x)dx$$
The variation of $F$ is
$$\begin{align}
\delta F[u,\delta u]&=\left.{\frac{d}{d\alpha}\int_{x_{\text{start}}}^{x_{\text{end}}}L(u+\alpha\delta u,u'+\alpha \delta u',x)dx}\right|_{\alpha=0} \\
&=\int_{x_{\text{start}}}^{x_{\text{end}}}\left( \frac{ \partial L }{ \partial u } \delta u+\underbrace{ \frac{ \partial L }{ \partial u' } \delta u' }_{ fg' } \right)dx \\
(\text{integration by parts})&=\int_{x_{\text{start}}}^{x_{\text{end}}}\left( \frac{ \partial L }{ \partial u } \delta u- \frac{d}{dx}\frac{ \partial L }{ \partial u' } \delta u' \right)dx+\int_{x_{\text{start}}}^{x_{\text{end}}} \frac{d}{dx}\left( \frac{ \partial L }{ \partial u' } \delta u \right)dx \\
&=\left.{\frac{ \partial L }{ \partial u' } \delta u}\right|_{x_{\text{start}}}^{x_{\text{end}}}-\int_{x_{\text{start}}}^{x_{\text{end}}}\left(  \frac{d}{dx}\frac{ \partial L }{ \partial u' } - \frac{ \partial L }{ \partial u }  \right)\delta udx \\
&=\ldots
\end{align}$$
The [[Lagrange equation]] spontaneously came up in the integral there. Before we move on, let's better define what $u$ even is by giving a solid definition of its space $U$:
$$U=\{ \text{functions }[x_{\text{start}},x_{\text{end}}]\to \mathbb{R}\text{ such that }u(x_\text{start})=y_\text{start},\ u(x_{\text{end}})=y_\text{end} \}$$
$\delta u$ is defined such that $u$ and $u+\delta u$ are both in $U$ and it vanishes at the boundaries:
$$\delta u(x_\text{start})=0, \quad \delta u(x_\text{end})=0$$
We can use these boundary conditions to state that the first term in our calculation is *zero*, which leaves us with:
$$\ldots=-\int_{x_\text{start}}^{x_\text{end}}\left( \frac{d}{dx}\frac{ \partial L }{ \partial u' } -\frac{ \partial L }{ \partial u }  \right)\delta udx$$
(TODO: Finish this, end of lesson 15/04/25) We know from the theory of functionals that a function $u_{0}$ for which the argument of this integral is zero is a stationary point. Thus, we can state that if a function $u$ is a stationary point for the functional
$$S[u]=\int_{x_\text{start}}^{x_\text{end}}L(u(x),u'(x),x)\ dx$$
it describes motion, and it is defined from the global properties of motion. We should first reflavor our variables to be more familiar. Firstly, let's definitively call $L$ the Lagrangian of our system. Then, in one dimensions, we can just rename $u(x)$ to be the more familiar $q(t)$ and get
$$\boxed{S[q]=\int_{t_{1}}^{t_{2}}L(q(t),q'(t),t)\ dt}$$
This functional is called **[[action]]** and the functions $q(t)$ that minimize it fully determine motion and solve the [[Lagrange equation]], a fact known as the [[least action principle]]. This can be trivially extended to multiple dimensions by adding more variables: if $L:\mathbb{R}^{2n+1}\to \mathbb{R}$, the action is
$$\boxed{S[q_{1},\ldots,q_{n}]=\int_{t_{1}}^{t_{2}}L(q_{1}(t),\ldots,q_{n}(t),\dot{q}_{1}(t),\ldots,\dot{q}_{n}(t))\ dt}$$
which is sometimes called the **Hamiltonian action**.

[^1]: Such as trajectory is called a [[geodetic curve]] and is very important in general relativity.
