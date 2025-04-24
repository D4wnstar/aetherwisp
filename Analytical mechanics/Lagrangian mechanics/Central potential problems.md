Consider two bodies of [[mass|masses]] $m_{1}$ and $m_{2}$ moving in $\mathbb{R}^{3}$, for a total of $n=6$ [[degrees of freedom]]. Each position vector is $\mathbf{r}_{i}=(x_{i},y_{i},z_{i})$ for $i=1,2$. The [[kinetic energy]] is
$$T=\frac{1}{2}m_{1} \dot{\mathbf{r}}_{1}^{2}+ \frac{1}{2}m_{2}\dot{\mathbf{r}}_{2}^{2}$$
The [[potential energy]] is dependent on the distance between the bodies, $V\equiv V(\mathbf{r}_{1}-\mathbf{r}_{2})=V(\mathbf{r})$, where we defined $\mathbf{r}\equiv \mathbf{r}_{1}-\mathbf{r}_{2}$ for the sake of brevity. Like in most $N$-body systems, we use the [[center of mass]] frame to simplify our treatment. Call $M\equiv m_{1}+m_{2}$ the total mass. The center of mass is located by
$$\mathbf{R}=\frac{m_{1}\mathbf{r}_{1}+m_{2}\mathbf{r}_{2}}{M}$$
We can retroactively get the positions of the two bodies from the center of mass as
$$\mathbf{r}_{1}=\mathbf{R}+ \frac{m_{2}\mathbf{r}}{M},\qquad \mathbf{r}_{2}=\mathbf{R}- \frac{m_{1}\mathbf{r}}{M}$$
With these new coordinates, we can rewrite the expression of kinetic energy in this frame:
$$\begin{align}
T&=\frac{1}{2}m_{1}\left( \dot{\mathbf{R}}^{2}+ \cancel{ \frac{2m_{2}}{M}\dot{\mathbf{R}}\cdot\dot{\mathbf{r}} }+ \frac{m_{2}^{2}}{M}\dot{\mathbf{r}}^{2} \right)+ \frac{1}{2}m_{2}\left( \dot{\mathbf{R}}^{2}- \cancel{ \frac{2m_{1}}{M}\dot{\mathbf{R}}\cdot \dot{\mathbf{r}} }+ \frac{m_{1}^{2}}{M}\dot{\mathbf{r}}^{2} \right) \\
&=\frac{1}{2}M \dot{\mathbf{R}}^{2}+ \frac{1}{2} \frac{m_{1}m_{2}^{2}+m_{2}m_{1}^{2}}{M^{2}}\dot{\mathbf{r}}^{2}
\end{align}$$
We now defined the reduced mass $\mu\equiv m_{1}m_{2}/M$, with which we can comfortably write
$$T=\frac{1}{2}M \dot{\mathbf{R}}^{2}+ \frac{1}{2}\mu \dot{\mathbf{r}}^{2}$$
The kinetic energy has gone from the sums if kinetic energy of the bodies to the sums of kinetic energy of the "center of mass" and of another terms that evidently takes up "everything else". With the kinetic energy known, we are ready to write the [[Lagrangian]] of this system:
$$L=\frac{1}{2}M \dot{\mathbf{R}}^{2}+ \frac{1}{2}\mu \dot{\mathbf{r}}^{2}- V(\mathbf{r})$$
for some potential energy $V$. Note that this does not depend on *where* the center of mass is, as there is no mention of $\mathbf{R}$ (only its derivative $\dot{\mathbf{R}}$).

We can interpret this equation as the sum of a free particle of mass $M$ and a particle of mass $\mu$ subject to a potential $V(\mathbf{r})$. In this light, we'll split the Lagrangian in two. Specifically, the latter part is
$$L(\mathbf{r},\dot{\mathbf{r}})=\frac{1}{2}\mu \lvert \dot{\mathbf{r}} \rvert ^{2}-V(\lvert \mathbf{r} \rvert )$$
As with all Lagrangians, our priority should be to sniff out [[Constant of motion|constants of motion]], as each and every one we find makes our problem easier. This Lagrangian of $\mathbf{r}$, for instance, is invariant to [[Rotation|rotations]] (in $SO(3)$). Invoking [[Nöther's theorem]], this means that the [[angular momentum]] $\mathbf{A}$[^1] is a constant of motion (all three components actually, so $A_{x}$, $A_{y}$ and $A_{z}$). Let's analyze what this invariance implies. The momentum is $\mathbf{A}=\mu \mathbf{r}\times \dot{\mathbf{r}}$. If it's constant over $\mathbf{r}(t)$, then $\mu \mathbf{r}(t)\times \dot{\mathbf{r}}(t)=\mathbf{A}_\text{const}$, but for a [[vector product]] to give an angle-independent constant we must have both $\mathbf{r}(t)$ and $\dot{\mathbf{r}}(t)$ lying [[Orthogonality|orthogonal]] to $\mathbf{A}_\text{const}$. In other words, both $\mathbf{r}(t)$ and $\dot{\mathbf{r}}(t)$ (and by extension the whole motion) lie on a plane perpendicular to $\mathbf{A}_\text{const}$.

This bit of geometry gives us the information that we need to simplify our coordinates. We'll then pick a [[frame of reference]] in which $(A_\text{const})_{x}=(A_\text{const})_{y}=0$[^2]. In this frame, we can pick the canonical [[basis]] $\{ \mathbf{e}_{x} ,\mathbf{e}_{y}\}$ and express $\mathbf{r}$ and $\dot{\mathbf{r}}$ as a [[linear combination]] of these:
$$\mathbf{r}=x\mathbf{e}_{x}+y\mathbf{e}_{y},\qquad \dot{\mathbf{r}}=\dot{x}\mathbf{e}_{x}+\dot{y}\mathbf{e}_{y}$$
In here, the Lagrangian becomes
$$L=\frac{1}{2}\mu(\dot{x}^{2}+\dot{y}^{2})- V(\sqrt{ x^{2}+y^{2} })$$
Since we're on a plane, we might as well move to [[polar coordinates]]. The appropriate [[coordinate transformation]] is
$$x=r\cos \theta,\qquad y=r\sin \theta$$
for which
$$L=\frac{1}{2}\mu(\dot{r}^{2}+r^{2}\dot{\theta}^{2})-V(r)$$
You might be wondering why the switch: the answer is that our "$\mu$" particle is moving in a straight line. Of course: there's no angular momentum, it can't be rotating! So our angular coordinate must be *[[Lagrangian|cyclical]]* and, as such, its [[Conjugate momenta|conjugate momentum]] is another constant of motion:
$$p_{\theta}=\frac{ \partial L }{ \partial \theta } =mr^{2}\dot{\theta}\equiv l=\text{constant}$$
As usual, this leads to an easy first order [[Ordinary differential equation|ODE]]:
$$\dot{ \theta}=\frac{l}{mr^{2}}$$
We can look for an effective Lagrangian
$$\begin{align}
L_\text{eff}&=L-\left.{\dot{\theta}l}\right|_{\dot{ \theta}=l/mr^{2}} \\
&=\frac{1}{2}m \dot{ r}^{2}+ \frac{m}{2}r^{2} \frac{l^{2}}{(mr^{2})^{2}}-V(r)- \frac{l^{2}}{mr^{2}} \\
&=\frac{1}{2}m \dot{r}^{2}- V(r)- \frac{l^{2}}{2mr^{2}} \\
&=\frac{1}{2}m \dot{r}^{2}-V_\text{eff}(r)
\end{align}$$
where
$$V_\text{eff}(r)=V(r)+\frac{l^{2}}{2mr^{2}}$$
Solving the [[Lagrange equation]] yields $r(t)$, which we can put into $\dot{\theta}$ to get
$$\dot{\theta}(t)=\frac{l}{mr(t)^{2}}$$
which we can solve to find $\theta(t)$. More importantly, $\theta(t)$ is invertible so we can find $t(\theta)$. Since $r(\theta(t)))$ is a composite function, we can use the [[chain rule]]:
$$\dot{r}(t)=\frac{d}{d\theta}r(\theta(t))\dot{\theta }(t)=\frac{dr}{d\theta} \frac{l}{mr^{2}}=- \frac{l}{m} \left.{\frac{d}{d\theta}\left( \frac{1}{r} \right)}\right|_{\theta=\theta(t)}$$
and
$$\ddot{r}(t)=- \frac{l}{m} \frac{d^{2}}{d\theta ^{2}}\left( \frac{1}{r} \right)\dot{\theta}=- \frac{l^{2}}{m^{2}r^{2}} \left.{\frac{d^{2}}{d\theta ^{2}}\left( \frac{1}{r} \right)}\right|_{\theta=\theta(t)}$$
Specifically when $\ddot{r}(t(\theta))$ we have
$$\ddot{r}(t(\theta))=- \frac{l^{2}}{m^{2}r^{2}} \frac{d^{2}}{d\theta ^{2}}\left( \frac{1}{r} \right)$$
### Keplerian potential
This is about as far as we get without knowing the specifics of the system. Everything up until now is perfectly general, provided the system matches our specifications. We now need some form of potential to keep going: we'll use a Keplerian potential to analyze gravitationally bound (or unbound) systems like [[Pianeta|planets]] around a [[stella|star]]. We start with a qualitative analysis of the one dimensional analog of potential
$$V(r)=- \frac{k}{r}$$
for some constant $k>0\in \mathbb{R}$. Our effective potential then is
$$V_\text{eff}(r)=- \frac{k}{r}+ \frac{l^{2}}{2mr^{2}}$$
There's a few cases of interest here that are already well known from classical mechanics depending on the total energy $E$ of the system.

![[Diagram Gravitational system]]

$E_{1}$ is the circular orbit case. In that case
$$\dot{\theta}(t)=\frac{l}{mr(t)^{2}}=\frac{l}{mr_{0}^{2}}\quad\to \quad \theta(t)=\frac{l}{mr_{0}^{2}}t+\theta_{0}$$
where $r_{0}$ is the constant orbit distance and $\theta_{0}$ is the starting angle.

$E_{2}$ is the elliptic orbit case. Here, the solution is similar to $E_{1}$ but $r(t)$ is no longer constant.

$E_{3}$ and $E_{4}$ are known as **collision events**. This is because the orbits may end up passing through the source point of the potential (the "star" so to speak) and collide with it. It doesn't necessarily need to happen however, and they may also described open orbits that only do a single pass near the star and then leave forever. $E_{3}$ is the specific case where the orbit is exactly parabolic.
#### Solving for distance
Now, to actually quantitatively solve for the motion itself, we need to tackle the Lagrange equation. The actual equation to solve is
$$\frac{d}{dt} \frac{ \partial L_\text{eff} }{ \partial \dot{r} } =m \ddot{r}\quad\to \quad \ddot{r}=- \frac{k}{mr^{2}}+ \frac{l^{2}}{m^{2}r^{3}}$$
and
$$\frac{ \partial L_\text{eff} }{ \partial r } =- \frac{k}{r^{2}}+ \frac{l^{2}}{m^{3}}$$
The condition that $r(\theta)$ needs to satisfy then is
$$- \frac{l^{2}}{m^{2}r^{2}} \frac{d^{2}}{d\theta ^{2}}\left( \frac{1}{r} \right)=- \frac{k}{mr^{2}}+ \frac{l^{2}}{m^{2}r^{3}}$$
which when rearranged is
$$\frac{d^{2}}{d\theta ^{2}}\left( \frac{1}{r} \right)= \frac{km}{l^{2}}- \frac{1}{r}$$
Since it's all reliant on $1/r$, we'll define $1/r(\theta)\equiv u(\theta)$ and $km/l^{2}=1/\eta$. With these symbols, our ODE simplifies to
$$u''+u=\frac{1}{\eta}$$
This leads to the solution
$$u(\theta)=\frac{1}{\eta}+ \frac{e}{\eta}\cos(\theta-\theta_{0})$$
for some value $e$. If we put $1/r(\theta)$ back in we finally get our orbit:
$$\boxed{r(\theta)=\frac{\eta}{1+e\cos(\theta-\theta_{0})}}$$
This is the general expression for a [[conic]] (the geometric shape), where $e$ is the eccentricity. When $0\leq e< 1$ we get an ellipse ($E_{1}$ and $E_{2}$), when $e=1$ we get a parabola ($E_{3}$) and for $e>1$ we get a hyperbole ($E_{4}$).
#### Periodicity
Assume the orbit is periodic, like that of Earth around the same or something more complicated. One can ask if the motion $r(t)$ draws a closed curve or not. The curve is closed if, after one or more full rotations, the object goes back to its starting point. The way we define it mathematically is by calling $\Delta \theta$ the variation of $\theta$ over a full rotation (or [[period]] if you prefer). For the curve to be closed, $\Delta \theta$ must eventually be a full $360°\ (2\pi)$ rotation, at which point it will have completed its cycle. For this to be true, $2\pi$ must be a multiple of $\Delta \theta$, which is the same as asking that their ratio is rational:
$$\text{An orbit is closed if } \frac{2\pi}{\Delta \theta}\in \mathbb{Q}$$
We can calculate $\Delta \theta$ as
$$\Delta \theta=2 \frac{l}{\sqrt{ 2m }}\int_{r_\text{min}}^{r_\text{max}} \frac{dr'}{r'^{2}\sqrt{ E-V_\text{eff}(r') }}$$
where $r_\text{min}$ and $r_\text{max}$ are respectively the shortest and furthest distance to the central body (called **perigee** and **apogee** for the Earth-Sun system).
#### Unbound motion
The other case is that the motion is unbounded, with no periodicity. It comes from infinity ($r(t)\to-\infty$) and goes to infinity ($r(t)\to +\infty$) at infinite times ($t=\pm \infty$). At the edges, the angle stops changing, since
$$\lim_{ r \to \pm\infty } \dot{\theta}=\lim_{ r \to \pm \infty } \frac{l}{mr^{2}}=0$$
This gives the boundary conditions to solve for $\theta(t)$, which at the edges must therefore approach some constants $\theta_{\pm}$. Although we can no longer define the variation $\Delta \theta$ over a period, we can define the variation over all time, which is nothing other than the difference
$$\Delta \theta=\theta_{+}-\theta_{-}$$
which is known in this context as the **scattering angle** of the body. It's how much the body gets diverted off its original course due to the effect of a central gravitating body. We can calculate it as
$$\Delta \theta=2 \frac{l}{\sqrt{ 2m }}\int_{r_\text{min}}^{\infty} \frac{dr'}{r'^{2}\sqrt{ E-V_\text{eff}(r') }}$$
#### Solving for angle
We have already solved the system in terms of distance compared to angle of rotation. Now we want to do the opposite: find the angle compared to the distance, so the inverse. On paper, we already have the equation:
$$\theta(r)=\theta_{0}+ \int_{r_{0}}^{r} \frac{l}{\sqrt{ 2m }} \frac{dr'}{r'^{2}\sqrt{ E+ \frac{k}{r}- \frac{l^{2}}{2mr'^{2}} }}$$
In practice, we need to solve this, and it certainly does not look like a gentle integral. Luckily, this *can* be solved, it's just not very easy. We'll do it step-by-step:
$$\begin{align}
\theta(r)-\theta_{0}&=\int_{r_{0}}^{r} \frac{d\rho}{\rho ^{2}\sqrt{ \frac{2mE}{l^{2}}+ \frac{2mk}{l^{2}\rho}- \frac{1}{\rho ^{2}} }} \\
\left( \frac{1}{\eta}\equiv \frac{mk}{l^{2}} \right)&=\int_{r_{0}}^{r} \frac{d\rho}{\rho ^{2}\sqrt{ \frac{2E}{\eta k}+ \frac{2}{\eta \rho}- \frac{1}{\rho ^{2}} }} \\
\left( \text{add/remove } \frac{1}{\eta ^{2}} \right)&=\int_{r_{0}}^{r} \frac{d\rho}{\rho ^{2}\sqrt{ \frac{2E}{\eta k}+ \frac{2}{\eta \rho}- \frac{1}{\rho ^{2}}+ \frac{1}{\eta ^{2}}- \frac{1}{\eta ^{2}}}} \\
&=\int_{r_{0}}^{r} \frac{d\rho}{\rho ^{2}\sqrt{ \frac{2E}{\eta k}+ \frac{1}{\eta ^{2}} - \left( \frac{1}{\eta}- \frac{1}{\rho} \right)^{2}}} \\
&=\int_{r_{0}}^{r} \frac{d\rho}{\rho ^{2}\sqrt{ \frac{1}{\eta ^{2}}\left[ \left( 1+ \frac{2E\eta}{k} \right) - \left( 1- \frac{\eta}{\rho} \right)^{2}\right] }} \\
\left( e= \sqrt{ 1+ \frac{2E\eta}{k} } \right)&=\int_{r_{0}}^{r} \frac{d\rho}{\rho ^{2}\sqrt{ \frac{1}{\eta ^{2}}\left[ e^{2} - \left( 1- \frac{\eta}{\rho} \right)^{2}\right] }} \\
&=\int_{r_{0}}^{r} \frac{d\rho}{\rho ^{2}\sqrt{ \frac{1}{\eta ^{2}}\left[ e^{2} - e^{2}\left( \frac{\eta}{\rho e} - \frac{1}{e}\right)^{2}\right] }} \\
&=\frac{\eta}{e}\int_{r_{0}}^{r} \frac{d\rho}{\rho ^{2}\sqrt{ \left[ 1- \left( \frac{\eta}{\rho e} - \frac{1}{e}\right)^{2}\right] }} \\
&=\ldots
\end{align}$$
(TODO: Finish this, mid lession 23/04/2025)
#### Solving with a constant of motion
There is yet another way of solving for motion in this system, and it requires finding out a constant of motion. We already know of angular momentum, which is constant in *any* central potential problem, but in the specific case of a Keplerian potential, we have another[^3]:
$$\mathbf{C}=\mathbf{p}\times \mathbf{A}-mk \frac{\mathbf{r}}{r}\qquad\left( \text{constant when }V(r)=- \frac{k}{r} \right)$$

> [!info] Proof
> We want to write $\mathbf{C}$ in a way that we can analyze. Recall that $\mathbf{p}=m \dot{\mathbf{r}}$, so we should start by looking for $\dot{\mathbf{r}}$. The position vector of a body is given by $\mathbf{r}(t)=r(t)\mathbf{e}_{r}(t)$ in some basis where $\mathbf{e}_{r}$ is a unit vector that always follows the body (like, say, polar coordinates). In terms of Cartesian coordinates, this vector is $\mathbf{e}_{r}=\cos \theta\ \mathbf{e}_{x}+\sin \theta\ \mathbf{e}_{y}$, for some time-dependent angle $\theta\equiv \theta(t)$. It varies in time as
> $$\begin{align}
> \dot{\mathbf{e}}_{r}&=- \dot{\theta}\sin \theta\ \mathbf{e}_{x}+ \dot{\theta}\cos \theta\ \mathbf{e}_{y} \\
> &=\dot{\theta}(-\sin \theta\ \mathbf{e}_{y}+\cos \theta\ \mathbf{e}_{y}) \\
> &=\dot{\theta}\mathbf{e}_{\theta}
> \end{align}$$
> where we defined $\mathbf{e}_{\theta}\equiv-\sin \theta\ \mathbf{e}_{x}+\cos \theta\ \mathbf{e}_{y}$.
> 
> The derivative of the position vector then is
> $$\dot{\mathbf{r}}=\dot{r} \mathbf{e}_{r}+r \dot{\mathbf{e}}_{r}=\dot{r}\mathbf{e}_{r}+r \dot{\theta}\mathbf{e}_{\theta}$$
> Recalling that $\mathbf{A}=l \mathbf{e}_{z}$, and noticing that $\{ \mathbf{e}_{r},\mathbf{e}_{\theta},\mathbf{e}_{z} \}$ is an [[Orthonormality|orthonormal]] triad ([[cylindrical coordinates]], actually), we can put this in $\mathbf{C}$ to find
> $$\begin{align}
> \mathbf{C}&=ml(\dot{r}\mathbf{e}_{r}+r \dot{\theta}\mathbf{e}_{\theta})\times \mathbf{e}_{z}-mk\mathbf{e}_{r} \\
> &=-ml \dot{r}\mathbf{e}_{\theta}+mlr \dot{\theta}\mathbf{e}_{r}- mk\mathbf{e}_{r} \\
> &=-ml \dot{r}\mathbf{e}_{\theta}+(mlr \dot{\theta}-mk)\mathbf{e}_{r}
> \end{align}$$
> since $\mathbf{e}_{r}\times \mathbf{e}_{z}=-\mathbf{e}_{\theta}$ and $\mathbf{e}_{\theta}\times \mathbf{e}_{z}=\mathbf{e}_{r}$. We can now look for the time derivative, which in theory should be zero:
> $$\begin{align}
> \dot{\mathbf{C}}&=-ml \ddot{r}\mathbf{e}_{\theta}+ 2ml \dot{r}\dot{\theta}\mathbf{e}_{r}+mlr \ddot{\theta}\mathbf{e}_{r}+mlr \dot{\theta}^{2}\mathbf{e}_{\theta}-mk \dot{\theta}\mathbf{e}_{\theta} \\
> &=m\mathbf{e}_{\theta}\left[ -l\left( - \frac{k}{mr^{2}} + \frac{l^{2}}{m^{2}r^{3}}\right)+ rl \frac{l^{2}}{m^{2}r^{4}} - k \frac{l}{mr^{2}}\right] \\
> &+m\mathbf{e}_{r}\left[ 2l \dot{r} \frac{l}{mr^{2}} + lr \left( - \frac{2l}{mr^{3}} \dot{r} \right)\right] \\
> &=0
> \end{align}$$
> As hoped, $\mathbf{C}$ does not change.

Our system then has not one, but *two* constants of motion, $\mathbf{A}(r,\theta,\dot{r},\dot{\theta})\equiv \mathbf{A}_{0}$ and $\mathbf{C}(r,\theta,\dot{r},\dot{\theta})\equiv \mathbf{C}_{0}$. We'll choose a frame of reference in which $\mathbf{A}_{0}=l\mathbf{e}_{z}$ and $\mathbf{C}_{0}=a\cos \theta_{0}\ \mathbf{e}_{x}+a\sin \theta_{0}\ \mathbf{e}_{y}$. In this frame, we have three equations in four variables:
$$\begin{cases}
A_{z}(r,\theta,\dot{r},\dot{\theta})&=l \\
C_{x}(r,\theta,\dot{r},\dot{\theta})&=a\cos \theta_{0} \\
C_{y}(r,\theta,\dot{r},\dot{\theta})&=a\sin \theta_{0}
\end{cases}$$
We can therefore determine three of the four unknowns, and we can express the fourth in terms of the other ones. We'll choose to find $\theta$ with respect to $r$, $\dot{r}$ and $\dot{\theta}$. Substituting known values, we get
$$\left\{\begin{align}
&mr^{2}\dot{\theta}=l  \\
&ml \dot{r}\sin \theta+mlr \dot{\theta}\cos \theta-km\cos \theta=a\cos \theta_{0} \\
&-ml \dot{r}\cos \theta+mlr \dot{\theta}\sin \theta-km\sin \theta=a\sin \theta_{0}
\end{align}\right.$$
The first yet again yields $\dot{\theta}=l/mr^{2}$, from which we get
$$\left\{\begin{align}
&ml \dot{r}\sin \theta+l^{2} \frac{1}{r}\cos \theta=km\cos \theta+a\cos \theta_{0} \\
&-ml \dot{r}\cos \theta+l^{2} \frac{1}{r}\sin \theta=km\sin \theta+a\sin \theta_{0}
\end{align}\right.$$
which again leads to
$$\frac{l^{2}}{r}=km+ a(\cos \theta \cos \theta_{0}+\sin \theta \sin \theta_{0})\quad\to \quad \frac{1}{r}=\underbrace{ \frac{km}{l^{2}} }_{ 1/\eta }+ \frac{a}{l^{2}}\cos(\theta-\theta_{0})$$
and finally
$$r(\theta)=\frac{\eta}{1+ \frac{a\eta}{l^{2}}\cos(\theta-\theta_{0})}$$
This is our conic equation that we found by "brute force" above, except we did not have to solve a singular ODE this time around. This is the benefit of using constants: they turn complicated differential equations into linear algebraic equations that can be solved with usual linear algebra.
### Solving for motion in time
For now, we've essentially solved a problem of geometry. We found that the trajectory is conic and by tracing the values of $r(\theta)$ for all $\theta \in[0,2\pi[$ we can draw the plot. This is useful in its own right, but often what we are looking for is the movement itself: we need dynamics. Basically, we are looking for $r(t)$ and $\theta(t)$ instead of $r(\theta)$ or $\theta(r)$. There's some ways we can go about this. To start, we know that
$$\dot{r}=\sqrt{ \frac{2}{m}(E-V_\text{eff}(r)) }$$
This leads to
$$t(r)=\sqrt{ \frac{m}{2} }\int_{r_{0}}^{r} \frac{dr'}{\sqrt{ \frac{k}{r'}- \frac{l^{2}}{2mr'^{2}} +E}}$$
which we can (at least in principle) invert to get $r(t)$. Another way to go about this is starting from
$$\dot{\theta}=\frac{d\theta}{dt}=\frac{l}{mr^{2}}\quad\to \quad \frac{dt}{d\theta}=\frac{mr(\theta)^{2}}{l} $$
(this is assuming that $\theta$ is smooth enough to permit this kind of inversion, but realistically any function $\theta$ not smooth enough for it yields unphysical motion (read: teleportation or infinite acceleration), so we allow it). This leads to
$$t(\theta)=\frac{m}{l}\int_{\theta_{0}}^{\theta} \frac{\eta ^{2}}{(1+e\cos(\theta'-\theta_{0}))^{2}}d\theta'$$
for some constant $\theta_{0}$. This can again be inverted to yield $\theta(t)$.

> [!example] Parabola dynamics
> To illustrate this problem, we'll consider the simple case of a parabola, for which $e=1$ and $\theta_{0}=0$. We'll solve for $\theta(t)$, and so we start from $t(\theta)$.
> $$\begin{align}
> t(\theta)&=\frac{l^{3}}{mk^{2}}\int_{0}^{\theta} \frac{1}{4} \frac{d\theta'}{(1+\cos \theta')^{2}}=\frac{l^{3}}{4mk^{2}}\int_{0}^{\theta} \frac{d\theta'}{\left( \cos \frac{\theta'}{2} \right)^{2}\left( \cos \frac{\theta'}{2} \right)^{2}} \\
> &=\frac{l^{3}}{2mk^{2}}\int_{0}^{\tan \theta/2}(1+x^{2})dx=\frac{l^{3}}{2mk^{2}}\left.{\left( x+ \frac{x^{3}}{3} \right)}\right|_{0}^{\tan \theta/2} \\
> &=\frac{l^{3}}{2mk^{2}}\left( \tan \frac{\theta}{2}+ \frac{1}{3}\tan ^{3} \frac{\theta}{2}\right)
> \end{align}$$
> where we substituted $x=\tan \theta'/2$, which leads to $dx=\frac{1}{\cos ^{2} \frac{\theta'}{2}} \frac{d\theta'}{2}=\left( 1+\tan \frac{\theta'}{2} \right) \frac{d\theta'}{2}$. At angle $\theta=0$, we get $t=0$, so the system starts there. At $\theta\to \pm \pi$, we go to infinite times, $t\to\pm \infty$, so $\pm \pi$ are asymptotes. We can correctly gather that our object starts at "the bottom" of the parabola, started off at one extremum far back in time, and will end up at the other edge far in the future. As for the motion itself, we would need to invert $t(\theta)$ into $\theta(t)$, but needless to say, that's not really doable manually. Get a computer to do it numerically for you.

[^1]: Unfortunately, both common letters for angular momentum, $L$ and $M$, are taken here so we'll use the less orthodox $\mathbf{A}$ here (it stands for "angular").

[^2]: Mathematically, this is a [[level set]] of codimension $2$.

[^3]: I am truly running out of letters here. Remember that $\mathbf{A}$ was angular momentum. I'll use $\mathbf{C}$ now because it's the initial of **C**onstant.
