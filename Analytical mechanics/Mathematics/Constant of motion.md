A **constant of motion** is a quantity that does not change over time and over a trajectory of motion. Formally, a constant of motion is defined as a function $I:\mathbb{R}^{N}\to \mathbb{R}$, $\mathbf{x}\to I(\mathbf{x})$, for which, given an autonomous system of [[Ordinary differential equation|ODEs]] $\dot{\mathbf{x}}=f(\mathbf{x})$ and a starting condition $\mathbf{x}_{0}$, we have $I(\mathbf{x}(t;\mathbf{x}_{0}))=I(\mathbf{x}_{0})$ for all $t$ and all solutions $\mathbf{x}(t;\mathbf{x}_{0})$ of the system. Its time derivative is zero everywhere: $\frac{d}{dt}I(\mathbf{x}(t;\mathbf{x}_{0}))=0$.

The locus of points in $\mathbb{R}^{N}$ that satisfies the equation $I(\mathbf{x})=\rho$, where $\rho$ is a constant, is a [[hypersurface]] in $\mathbb{R}^{N}$, specifically a [[Insieme di livello|level set]]. For example, in $\mathbb{R}^{3}$, the quantity $I(\mathbf{x})=x^{2}+y^{2}+z^{2}=\rho=R^{2}$ is a sphere. The constant of motion $I$ defines a family of *disjoint* (i.e. non-intersecting) hypersurfaces dependent on the parameter $\rho$. The union of all of these hypersurfaces is $\mathbb{R}^{N}$. Formally, such a family is known in differential geometry as a **[[foliation]]** of $\mathbb{R}^{N}$.

The benefit of finding constants of motion is that they add bindings to the parameters of a system. Specifically, each constant reduces the [[degrees of freedom]], and therefore the dimensionality of the system, by one. The more constants of motion are known beforehand, the fewer parameters need to be solved to find a trajectory. For instance, a three-dimensional system with two known constants of motion simplifies down to a one dimensional system.
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
> As you can see, we reduced a two-dimensional problem (solving for all phase space) into a one-dimensional one (solving only for the constant energy [[Curve|curve]]).

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
### In Lagrangian mechanics
Within the context of a Lagrangian system of $n$ [[degrees of freedom]], a constant of motion is a function $I:\mathbb{R}^{2n+1}\to \mathbb{R},(q,\dot{q},t)\to I(q,\dot{q},t)$ for which $\frac{d}{dt}I(q(t),\dot{q}(t),t)=0$ that solves the [[Lagrange equation]].

If we know a constant of motion $I(q,\dot{q},t)$ and, then we can write the following equation:
$$I(q(t),\dot{q}(t),t)=I_{0}$$
where $I_{0}$ is some constant. This is a first order [[Ordinary differential equation|ODE]] in $q(t)$ (technically a family of ODEs). If we solve this equation, we can find the motion $q(t)$ just from the constant of motion.

Let's consider the [[dynamical variable]] for a [[Lagrangian]] $L$:
$$E(q,\dot{q},t)=\sum_{i=1}^{n} \dot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }(q,\dot{q},t)-L(q,\dot{q},t) $$
The derivative of this is
$$\begin{align}
\frac{d}{dt} E(q,\dot{q},t)&=\sum_{i=1}^{n} \left( \ddot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }+\dot{q}_{i} \frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{i} }   \right)-\sum_{i=1}^{n} \left( \frac{ \partial L }{ \partial q_{i} } \dot{q}_{i} + \frac{ \partial L }{ \partial \dot{q}_{i} }\ddot{q}_{i} \right)-\frac{ \partial L }{ \partial t } \\
&=\sum_{i=1}^{n} \dot{q}_{i}\left( \frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{i} } -\frac{ \partial L }{ \partial q_{i} }   \right) - \frac{ \partial L }{ \partial t }  \\
(\text{if }q(t)\text{ solves Lag. eq.})&=-\frac{ \partial L }{ \partial t } 
\end{align} $$
Clearly then, if $\frac{ \partial L }{ \partial t }=0$, then $E$ is a constant of motion. This occurs when $L$ does not explicitly depend on time, that is, $L\equiv L(q,\dot{q})$, and in these cases, the quantity $E$ can always be used as a constant of motion. This property is known as the **time-shift invariance** of $L$. In plain terms, $L$ does not change in time: the dynamics of the system *now* are the same as they were in the past and will always be the same in the future.
#### Examples
> [!example] Mechanical system with purely positional forces
> For a mechanical system with purely positional forces, if the Lagrangian is explicitly time independent, $L\equiv L(q,\dot{q})$, then we can write
> $$L(q,\dot{q})=\frac{1}{2}\sum_{n,k} a_{nk}(q)\dot{q}_{n}\dot{q}_{k}-V(q)=T_{2}-V$$
> $a$ is a [[homogeneous function]] of degree $2$ in $\dot{q}$ and $V$ is a homogeneous function of degree $0$ in $\dot{q}$. The quantity $E$ is
> $$E=\sum_{k=1}^{n} \dot{q}_{k}\frac{ \partial L }{ \partial \dot{q}_{k} } -L=\underbrace{ \sum_{k=1}^{n} \dot{q}_{k}\frac{ \partial T_{2} }{ \partial \dot{q}_{k} } }_{ 2T_{2} } -T_{2}+V=T_{2}+V$$
> We can see that $E$ is the *total* mechanical energy of the system, given by the sum of [[kinetic energy]] and [[potential energy]].

> [!example] 2D harmonic oscillator
> We now imagine a two-dimension [[harmonic oscillator]] of Lagrangian
 >$$L=\frac{m}{2}(\dot{x}^{2}+\dot{y}^{2})- \frac{m\omega ^{2}}{2}(x^{2}+y^{2})$$
> where $\omega ^{2}=k/m$. Think of it a spring being pushed and pulled away and towards the origin. It is not rotating. We can find the motion pretty easily from each term of $E$:
> $$\frac{d}{dt} \frac{ \partial L }{ \partial x } -\frac{ \partial L }{ \partial x } =0\quad\to \quad \ddot{x}=-\omega ^{2}x$$
> $$\frac{d}{dt} \frac{ \partial L }{ \partial y } -\frac{ \partial L }{ \partial y } =0\quad\to \quad \ddot{y}=-\omega ^{2}y$$
> These are simple second order ODEs that solve to
> $$x(t)=A_{x}\cos(\omega t+\varphi_{x}),\qquad y(t)=A_{y}\cos(\omega t+\varphi_{y})$$
> We could have also solved this in [[polar coordinates]]. If we use the [[coordinate transformation]] $r=\cos \varphi,\ y=r\sin \varphi$, the Lagrangian becomes
> $$L=\frac{m}{2}(\dot{r}^{2}+r^{2}\dot{\varphi}^{2})- \frac{m\omega ^{2}}{2}r^{2}$$
> This Lagrangian does not explicitly depend on $\varphi$. The terms of $E$ are
> $$0=\frac{d}{dt} \frac{ \partial L }{ \partial \dot{r} } -\frac{ \partial L }{ \partial r } =m \ddot{r}-mr \dot{\varphi}^{2}+m \omega ^{2}r\quad\to \quad \ddot{r}=-\omega ^{2}r+r \dot{\varphi}^{2}$$
> $$0=\frac{d}{dt} \frac{ \partial L }{ \partial \dot{\varphi} }\quad\to \quad \frac{ \partial L }{ \partial \dot{\varphi} } =mr^{2}\dot{\varphi}$$
> The latter equation is a constant of motion. If we set $mr^{2}\dot{\varphi}=\ell$, we can invert to get $\dot{\varphi}=\ell/mr^{2}$. If we plug this into $\ddot{r}$ we get
> $$\ddot{r}=-\omega ^{2}r+ \frac{\ell^{2}}{m^{2}r^{3}}$$
> This is an ODE in $r(t)$ of the form $\ddot{r}=f(r)$ and can therefore be solved generally. We can also plug $\dot{\varphi}$ in the polar Lagrangian to get
> $$L_\text{eff}(r,\dot{r},\ell)=\frac{m\dot{r}^{2}}{2}- \frac{m\omega ^{2}r^{2}}{2}- \frac{\ell^{2}}{2mr^{2}}$$
> This isn't the original Lagrangian and does not even depend on the same variables, but it nonetheless contains the same information to the original. This *effective* Lagrangian uses the fact that the oscillator is not rotating, so the angular dependency in polar coordinates collapses to a constant of motion and we can get all the information about the system by just solving a single ODE, $\ddot{r}$, instead of two, $\ddot{x}$ and $\ddot{y}$.
