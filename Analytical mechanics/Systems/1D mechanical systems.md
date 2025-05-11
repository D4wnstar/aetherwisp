---
wiki-publish: true
---
One-dimensional mechanical [[Physical system|systems]] are of particular interest in physics. Their general [[ordinary differential equation]] is
$$m\ddot{x}=F(x,\dot{x},t)$$
where $m$ is the [[mass]], $x$ is the position, $\dot{x}=v$ is velocity, $\ddot{x}=a$ is acceleration, $t$ is time and $F$ is a [[force]].
### Autonomous and conservative systems
Many systems of interest are autonomous and do not depend on time $t$ explicitly. They also often obey a [[Vector field|conservative force]], which never depends on $\dot{x}$. In these cases, the ODE simplifies to
$$m\ddot{x}=F(x)$$
For future simplicity, we set $f(x)=F(x)/m$, which yields
$$\ddot{x}=f(x)$$
or in system form
$$\begin{cases}
\dot{x}=v \\
\dot{v}=f(x)
\end{cases}\tag{1}$$
Since the system is conservative, there exists a [[potential]] $V(x)$ such that $F(x)=-V'(x)$ called the [[potential energy]]. The sum of this potential energy with the [[kinetic energy]] (the total mechanical [[energy]] of the system $E$) is always a [[constant of motion]]:
$$E(x,v)=\frac{1}{2}mv^{2}+V(x)$$
All trajectories that the system takes in its own [[phase space]] lie on a constant [[curve]] defined by the constant energy. Given some starting conditions $x_{0}$ and $v_{0}$, these two uniquely determine the energy curve and therefore the trajectory of the system over time.

> [!example] Free particle
> The [[free particle]] is the easiest case: the potential is always zero, $V(x)=0$. Thus our energy is $E(x,v)=\frac{1}{2}mv^{2}$. The ODE becomes $\ddot{x}=0$, which solves to $x(t)=at+b$ for some constants $a>0$ and $b>0$. Since $v$ is constant, the curve determined by $E$ is actually just an oriented straight line following the sign of $v$.

> [!example] Harmonic oscillator
> The [[harmonic oscillator]] is the other major case. The energy is given by
> $$E(x,v)=\frac{1}{2}mv^{2}+ \frac{1}{2}m\omega ^{2}x^{2}$$
> We can reorder this to read
> $$\frac{v^{2}}{2E/m}+ \frac{x^{2}}{2E/m\omega ^{2}}=1$$
> which is the equation of an [[ellipse]] parameterized by $x$ and $v$, with axes given by the energy, the mass and the frequency.
>
> ![[Plot Trajectories of a harmonic oscillator|80%]]
> 
> Let's look for the tangent line for any point on the ellipse, call it $y=f(x)$. In a point $x_{0}$, it is of course a line, so $y=f'(x_{0})x+q$. But $f'(x_{0})$ is the tangent function $\tan(\alpha)$ for an angle $\alpha$. This angle is somewhat cryptic: thankfully, we can bypass it with calculus. The tangent at a point on a graph is just the derivative of the function being plotted. Since we are plotting $v$ against $x$, we have
> $$\tan \alpha=\frac{dv}{dx}(x_{0})=\frac{\dot{v}(t(x_{0}))}{\dot{x}(t(x_{0}))}=\frac{f(x_{0})}{v(x_{0})}$$
> using the [[chain rule]] and $(1)$. One important consequence is that $v$ can be equal to zero sometimes. In these cases, unless $f(x)$ also goes to zero in that point, the function blows up to infinity: $\alpha$ is exactly $\pi/2$ and the tangent is vertical (in the sense that it is aligned with the $v$ axis). If $f(x)$ does go to zero, the behavior depends on the shape of $f$ and may very well not blow up. This should ring a bell: the set of all zeros of $f$ is the set of all [[Equilibrium point|equilibrium points]] of the system.
> 
> Recall also that trajectories must be continuous: a physical object can't just teleport to a different location or discontinuously change its speed. As such, the presence of a discontinuity in the change of $v$ over $x$ in a certain point $x_{0}$ means that $x_{0}$ is *impassable*. It's a hard wall. What happens there is that the system "bounces back". It will slow down to a stop (continuously!) and invert direction. In fact, these points have a special name to represent this behavior: **[[inversion point|inversion points]]**. As such, any time the system reaches zero speed, unless it does so in a point of equilibrium, it will always invert direction and go back to where it came from. If it is an equilibrium point, it will instead stop right there and stay still until it is perturbed again.
### Qualitative analysis
Systems of this kind require solving a second order ODE. These ODEs aren't terribly difficult in some simple cases, but can spiral out of control in more complex situations. It would be nice if we could simplify it all so that we only need to solve a first order ODE instead, which is pretty much trivial in comparison.

For motivation, consider the usual free particle. Our [[constant of motion]] is [[linear momentum]] $I(x,v)=mv$. Let's think of this quantity geometrically. This equation is defining the locus of all points for which $I(x,v)=I_{0}=mv$. If we invert it, we get $v=\dot{x}=I_{0}/m$. We can get $x(t)$ out of this by simple integration:
$$\int \dot{x}dt=\frac{I_{0}}{m}\int dt\quad\to \quad x(t)=\frac{I_{0}}{m}t+x_{0}$$
But hold on. We just solved the system, without even *touching* the ODE. The constant of motion was all that we needed and the solution was an immediate integral. Of course, this requires to know the constant of motion in some way, but if we do know it, we get to skip a ton of work and get an equally valid result.

Now that we have an end goal, let's extend this method to any mechanical system. As always, the most reliable constant of motion in the universe is total energy:
$$E(x,v)=T(v)+V(x)=\frac{1}{2}m v^{2}+V(x)$$
Reorder now to isolate $v$:
$$v=\dot{x}=\pm \sqrt{ \frac{2}{m}(E-V(x)) }$$
This equation implies a relation between $t(x)$ and $\frac{dt}{dx}$. We have
$$\frac{dt(x)}{dx}=\frac{1}{\dot{x}}=\frac{1}{\sqrt{ \frac{2}{m}(E-V(x)) }}$$
Integrate over $dx$ and we get
$$t(x)=t(x_{0})+\int_{x_{0}}^{x} \frac{dx'}{\sqrt{ \frac{2}{m}(E-V(x')) }}$$
If we manage to solve this integral and then invert $t(x)$ to $x(t)$, we will have solved the system through its energy. Of course, before we proceed we need to know the potential $V(x)$, so we can't find a universal solution for all systems. Let's tackle the integral then for the harmonic oscillator.

> [!example] Harmonic oscillator
> The potential is $V(x)=\frac{1}{2}mv^{2}$. The integral therefore is
> $$\begin{align}
> t(x)-t(x_{0})&=\int_{x_{0}}^{x} \frac{dx'}{\sqrt{ \frac{2}{m}E- \omega ^{2}x'^{2} }} \\
> &=\frac{1}{\sqrt{ \frac{2E}{m} }}\int_{x_{0}}^{x} \frac{dx'}{\sqrt{ 1- \frac{m\omega ^{2}}{2E}x'^{2} }} \\
\left( x\to y^{2}=\frac{m\omega ^{2}}{2E}x'^{2} \right)&=\frac{1}{\omega}\int_{\sqrt{ m\omega/2E }\ x_{0}}^{\sqrt{ m\omega ^{2}/2E }\ x} \frac{dy}{\sqrt{ 1-y^{2} }} \\
> &=\frac{1}{\omega}\arcsin\left( \sqrt{ \frac{m\omega ^{2}}{2E} }x \right)- \frac{1}{\omega}\arcsin\left( \sqrt{ \frac{m\omega ^{2}}{2E} }x_{0} \right)
> \end{align}$$
> Invert this using trigonometric properties of the arcsine to get
> $$x(t)=\sqrt{ \frac{2E}{m\omega ^{2}} }\sin(\omega t-\varphi_{0})$$
> where $\varphi_{0}$ is a constant term that absorbs $x_{0}$. This is a [[harmonic wave]].
#### Behavior around maxima
Interesting behavior happens near maxima of $x$. Call one such maximum $x_\text{max}$. Then our energy is $E=V(x_\text{max})$ and our integral looks like
$$t(x_\text{max})=t(x_{0})+\int_{x_{0}}^{x_\text{max}} \frac{dx'}{\sqrt{ \frac{2}{m}(E-V(x')) }}\simeq t(x_{0})+\int_{\xi_{0}}^{0} \frac{d\xi}{\sqrt{ \frac{2V'(x_\text{max})}{m} \xi}}$$
where $\lvert x_\text{max}-x_{0} \rvert\ll 1$ and so $\lvert x_\text{max}-x' \rvert\ll 1$. We can approximate the potential with a [[Serie di Taylor|Taylor series]]:
$$V(x')=\underbrace{ V(x_\text{max}) }_{ E }+ V'(x_\text{max})_{ 0 }(x'-x_\text{max})+\ldots$$
If we truncate at the first order and plug this in the square root we see
$$\sqrt{ \frac{2}{m}(E-V(x)) }\simeq \sqrt{ \frac{2}{m} }\sqrt{ V'(x_\text{max}) }\sqrt{ x_\text{max}-x' }$$
Our integral then is
$$t(x_\text{max})\simeq t(x_{0})+\int_{\xi_{0}}^{0} \frac{d\xi}{\sqrt{ \frac{2V'(x_\text{max})}{m} \xi}}$$
This integral is finite (although the value itself may be very complicated).

Something similar can be seen in a maximum of $V$. Call one such maximum $c$. Then our energy is $V(c)=E$ and our integral looks like
$$t(c)=t(x_{0})+\int_{x_{0}}^{c} \frac{dx'}{\sqrt{ \frac{2}{m}(E-V(x')) }}$$
where $\lvert x'-c \rvert\ll 1$. We can again approximate the potential with a Taylor series:
$$V(x')=\underbrace{ V(c) }_{ E }+\underbrace{ V'(c) }_{ 0 }(x'-c)+ \frac{1}{2}V''(c)(x'-c)^{2}+\ldots$$
If we stop at the second order and plug this into the integral we get
$$t(c)\simeq t(x_{0})+ \frac{1}{\sqrt{ \frac{-V''(c)}{m} }}\int_{0}^{c-x_{0}} \frac{d\xi}{\xi}=\infty$$
This integral unfortunately diverges always.
#### Behavior on closed loops
(TODO: Lesson of 12/03/25, towards the end)