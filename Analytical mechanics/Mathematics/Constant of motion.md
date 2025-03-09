A **constant of motion** is a quantity that does not change over time and over a trajectory of motion. Formally, a constant of motion is defined as a function $I:\mathbb{R}^{N}\to \mathbb{R}$, $\mathbf{x}\to I(\mathbf{x})$, for which, given an autonomous system of [[Ordinary differential equation|ODEs]] $\dot{\mathbf{x}}=f(\mathbf{x})$ and a starting condition $\mathbf{x}_{0}$, we have $I(\mathbf{x}(t;\mathbf{x}_{0}))=I(\mathbf{x}_{0})$ for all $t$ and all solutions $\mathbf{x}(t;\mathbf{x}_{0})$ of the system. Its time derivative is zero everywhere: $\frac{d}{dt}I(\mathbf{x}(t;\mathbf{x}_{0}))=0$.

The locus of points in $\mathbb{R}^{N}$ that satisfies the equation $I(\mathbf{x})=\rho$, where $\rho$ is a constant, is a [[hypersurface]] in $\mathbb{R}^{N}$, specifically a [[Insieme di livello|level set]]. For example, in $\mathbb{R}^{3}$, the quantity $I(\mathbf{x})=x^{2}+y^{2}+z^{2}=\rho=R^{2}$ is a sphere. The constant of motion $I$ defines a family of *disjoint* (i.e. non-intersecting) hypersurfaces dependent on the parameter $\rho$. The union of all of these hypersurfaces is $\mathbb{R}^{N}$. Formally, such a family is known in differential geometry as a **[[foliation]]** of $\mathbb{R}^{N}$.

The benefit of finding constants of motion is that they add bindings to the parameters of a system. Specifically, each constant reduces the [[degree of freedom|degrees of freedom]], and therefore the dimensionality of the system, by one. The more constants of motion are known beforehand, the fewer parameters need to be solved to find a trajectory. For instance, a three-dimensional system with two known constants of motion simplifies down to a one dimensional system.
### Examples
> [!example] Harmonic oscillator
> A typical constant of motion is the total mechanical [[energy]] of a body, defined as the sum of its [[kinetic energy|kinetic]] and [[potential energy]]. A common case is, as always, the [[harmonic oscillator]]. We consider a [[point mass]] in oscillation, with unit [[mass]] $m=1$ for simplicity. The solution is well known and is the set
> $$x(t)=x_{0}\cos \omega t+ \frac{v_{0}}{\omega}\sin \omega t$$
> $$v(t)=-\omega x_{0}\sin \omega t+v_{0}\cos \omega t$$
> The total energy of the particle is $I(x,v)=\frac{1}{2}v^{2}+ \frac{1}{2}\omega ^{2}x^{2}$. To prove that this is, in fact, a constant of motion, we just substitute $x$ and $v$ with the solutions above:
> $$\begin{align}
> I(x(t),v(t))&= \frac{1}{2}(-x_{0}\sin \omega t+v_{0}\cos \omega t)^{2} + \frac{1}{2}\omega ^{2}\left( x_{0}\cos \omega t+ \frac{v_{0}}{\omega}\sin \omega t \right)^{2} \\
> &=\frac{\omega ^{2}x_{0}^{2}}{2}\sin ^{2}\omega t-\omega x_{0}v_{0}\sin \omega t\cos \omega t+ \frac{v_{0}^{2}}{2}\cos ^{2}\omega t+ \\
  &+ \frac{\omega ^{2}x_{0}^{2}}{2}\cos ^{2}\omega t+\omega x_{0}v_{0}\cos \omega t\sin \omega t + \frac{v_{0}^{2}}{2}\sin ^{2}\omega t \\
> &=\frac{\omega ^{2}x_{0}^{2}}{2}\underbrace{ (\sin ^{2}\omega t+\cos ^{2}\omega t) }_{ 1 }+ \omega x_{0}v_{0}\underbrace{ (-\sin \omega t\cos \omega t+\cos \omega t\sin \omega t) }_{ 0 }+ \\
  & + \frac{v_{0}^{2}}{2}\underbrace{ (\cos ^{2}\omega t+\sin ^{2}\omega t) }_{ 1 } \\
> &=\frac{\omega ^{2}x_{0}^{2}}{2}+ \frac{v_{0}^{2}}{2}=I(x_{0},v_{0})
> \end{align}$$
> It is dependent only on the starting conditions.
> 
> For an even simpler form, let's now set $\omega=1$. The energy therefore becomes $I(x,v)=\frac{1}{2}(x^{2}+v^{2})$. If we set an arbitrary energy quantity $E$, then the system will maintain this total energy throughout its entire motion. The formula for $I$ is well-known: it is a circle. In fact, each value $E$ describes a circle in $(x,v)$-space (i.e. [[phase space]]). Lower energies make for smaller circles and viceversa.
> 
> ![[Plot 1D Harmonic oscillator constant energy surfaces|70%]]
> 
> As you can see, we reduced a two-dimensional problem (solving for all phase space) into a one-dimensional one (solving only for the constant energy [[curva|curve]]).

> [!example] 1D conservative system
> In a [[conservative system]] (here given with one degree of freedom), the total force $F(x)$ can be given as the derivative of a [[potential energy]] $V(x)$:
> $$\frac{F(x)}{m}=f(x)=- \frac{V'(x)}{m}$$
> where $m$ is the mass. $f(x)$ is an acceleration, $f(x)=a=\ddot{x}$. The total energy therefore is
> $$E(x,v)=\frac{1}{2}mv^{2}+V(x)$$
> where the first term is [[kinetic energy]]. In such a system, this is always a constant of motion. In fact, using the [[chain rule]] we get
> $$\frac{d}{dt}E(x(t),v(t))=\frac{ \partial E }{ \partial x } (x(t),v(t))\dot{x}(t)+\frac{ \partial E }{ \partial v } (x(t),v(t))\dot{v}(t)=\ldots$$
> This system is described by the two ODEs $\dot{x}=v$ and $\dot{v}=f(x)$. We can substitute these two above
> $$\ldots=\frac{ \partial E }{ \partial x } (x(t),v(t))v(t)+\frac{ \partial E }{ \partial v } (x(t),v(t))f(x(t))=\ldots$$
> If $v$ does not depend on $x$, we have
> $$\frac{ \partial E(x,v) }{ \partial x } =V'(x),\qquad \frac{ \partial E(x,v) }{ \partial v } =mv$$
> and so
> $$\ldots=V'(x(t))v(t)+mv(t)f(x(t))=-F(x(t))v(t)+v(t)F(x(t))=0$$
> which proves our point.
