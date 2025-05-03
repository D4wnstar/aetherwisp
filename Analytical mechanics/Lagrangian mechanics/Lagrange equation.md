---
aliases:
  - Lagrangian system
---
The **Lagrange equation** is a second order[^1] differential equation that finds the motion of a [[Physical system|system]] from its [[energy]]:
$$\frac{d}{dt} \frac{ \partial T }{ \partial \dot{q}_{j} }(q(t),\dot{q}(t),t)- \frac{ \partial T }{ \partial q_{j} } (q(t),\dot{q}(t),t)=Q_{j} $$
Here $T$ is the [[kinetic energy]], $q(t)$ is the motion using [[generalized coordinates]] $q_{j}$ and $Q_{j}$ are the [[generalized force|generalized force]]. The value $j=1,\ldots,n$ depends on the [[degrees of freedom]] $n$ of the system.

If the system is subject to [[Vector field|conservative forces]] and can be written in terms of a [[potential]] $V$, we can further define the **[[Lagrangian]]** $L=T-V$ to rewrite the equation as
$$\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{i} }(q(t),\dot{q}(t),t)-\frac{ \partial L }{ \partial q_{i} } (q(t),\dot{q}(t),t)=0 $$
A [[dynamical system]] whose equations of motion can be written in this form is said to be a **Lagrangian system**.

The benefit of using a set of Lagrange equations over a set of [[Newton's laws|Newton's second laws]] is that they allow picking a parameterization of the [[Constraint|constraints]] such that the constraint forces vanish. The equations that are left can then be solved algorithmically by [[Differential|differentiation]], which is typically far easier than what would be necessary with Newton's laws and can also be offloaded to a computer for numerical differentiation.
### Validity
This equation is correct *point-wise*, for each $t\in \mathbb{R}^{+}$, and for this reason it is said that the Lagrange equation describes motion **locally** (as opposed to globally). See [[Global motion]].
### Kinetic energy
The general form of the Lagrange equation is in terms of kinetic energy. Fortunately, we have a very general expression for it
$$T(q,\dot{q},t)= \frac{1}{2}\sum_{j,k=1}^{n}a_{jk}(q,t)\dot{q}_{j}\dot{q}_{k}+\sum_{l=1}^{n}  b_{l}(q,t)q̇_{l} + \frac{1}{2}c(q,t)$$
See [[Kinetic energy#In analytical mechanics]] for the derivation. We can substitute this into the Lagrange equation and take the derivatives directly. Starting from the derivative in $q_{m}$ we get
$$\frac{ \partial T }{ \partial q_{m} } =\frac{1}{2}\sum_{j,k=1}^{n} \frac{ \partial a_{jk} }{ \partial q_{m} } \dot{q}_{j}\dot{q}_{k}+\sum_{l=1}^{n} \frac{ \partial b_{l} }{ \partial q_{m} } \dot{q}_{l}+ \frac{1}{2}\frac{ \partial c }{ \partial q_{m} } $$
As for the other derivative, it's a little more complicated:
$$\frac{ \partial T }{ \partial \dot{q}_{m} } =\frac{1}{2}\sum_{j,k=1}^{n} a_{jk}\underbrace{ \frac{ \partial \dot{q}_{j} }{ \partial \dot{q}_{m} } }_{ \delta_{jm} }\dot{q}_{k}+ \frac{1}{2}\sum_{j,k=1}^{n} a_{jk}\dot{q}_{j}\underbrace{ \frac{ \partial \dot{q}_{k} }{ \partial \dot{q}_{m} } }_{ \delta_{km} } +\sum_{l=1}^{n} b_{l}\underbrace{ \frac{ \partial \dot{q}_{l} }{ \partial \dot{q}_{m} } }_{ \delta_{lm} } =\ldots$$
where we used [[Kronecker delta|Kronecker deltas]]. These allows us to cut down on the sums:
$$\ldots=\frac{1}{2}\sum_{k=1}^{n} a_{mk}\dot{q}_{k}+ \frac{1}{2}\sum_{j=1}^{n} a_{jm}\dot{q}_{j}+b_{m}=\ldots$$
If we rename the second sum's index from $j$ to $k$ and remember that the [[matrix]] $a$ is [[Matrice simmetrica|symmetric]], we can write $a_{jm}\to a_{km}=a_{mk}$, which leads to the exact same sum as the first. Summing the two we get
$$\ldots=\sum_{k=1}^{n} a_{mk}(q,t)\dot{q}_{k}+b_{m}(q,t)$$
We now need to take the time derivative:
$$\frac{d}{dt} \frac{ \partial T }{ \partial \dot{q}_{m} } =\sum_{k,h=1}^{n} \frac{ \partial a_{mk} }{ \partial q_{h} } \dot{q}_{h}\dot{q}_{k}+\sum_{k=1}^{n} a_{mk}\ddot{q}_{k}+\sum_{h=1}^{n} \frac{ \partial b_{m} }{ \partial q_{h} } \dot{q}_{h}$$
Note that the highest derivative of $q$ is the second, in $\ddot{q}_{k}$. This confirms that the Lagrange equation is a second order differential equation.

All of the partial derivatives of $a$, $b$ and $c$, alongside the generalized force $Q_{j}$ are functions of $q$ and $\dot{q}$ composed with motion, so the whole differential equation can be written as
$$\sum_{k=1}^{n} a_{mk}(q(t),t)\ddot{q}_{k}(t)=f_{m}(q(t),\dot{q}(t),t)$$
where $f_{m}$ is a function that includes everything other than the $a_{mk}$ term. This is still a second order differential equation, just implicitly so since $\ddot{q}$ is "trapped" inside the sum. The left hand side now reads as a matrix product between the matrix $\mathrm{a}$ and the vector $\ddot{\mathbf{q}}$, so we can write
$$\mathrm{a}\ddot{\mathbf{q}}=f$$
To continue, we'll apply the [[Invertible matrix|inverse matrix]] of $\mathrm{a}$ on both sides: $\mathrm{a}^{-1}\mathrm{a}\ddot{\mathbf{q}}=\mathrm{a}^{-1}f$. Since $\mathrm{a}^{-1}\mathrm{a}=1$, we get
$$\boxed{\ddot{\mathbf{q}}=\mathrm{a}^{-1}f(q,\dot{q},t)}$$
We now have the same equation in explicit form. What this tells us is that we can, at least in principle, find the motion from the inverse of the kinetic matrix applied onto a (vector-valued) function $f$. Our next step then is to better understand what $f$ is.
### Examples
> [!example] Harmonic oscillator
> As always, the [[harmonic oscillator]] is the test bench for everything, and we'll use it to check if the Lagrange equation really works. The kinetic energy is simply $T(q,\dot{q},t)=\frac{1}{2}m \dot{q}^{2}$. The potential is also well known to be $V(q,t)=\frac{1}{2}m\omega ^{2}q^{2}$. The Lagrangian then is
> $$L(q,\dot{q},t)=\frac{1}{2}m\dot{q}^{2}- \frac{1}{2}m\omega ^{2}q^{2}$$
> If the Lagrange equation is to be believed, this quantity contains the entire dynamics of the system, which we can extract by solving its Lagrange equations. To find it, we'll need some derivatives:
> $$\frac{ \partial L }{ \partial q } =-m\omega ^{2}q,\quad \frac{ \partial L }{ \partial \dot{q} } =m \dot{q}$$
> We now need to compose these with motion and take the time derivative of the second:
> $$\frac{ \partial L }{ \partial q } (q(t),\dot{q}(t),t)=-m\omega ^{2}q(t),\quad\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q} }(q(t),\dot{q}(t),t) =\frac{d}{dt} (m\dot{q}(t))=m\ddot{q}(t)$$
> Hence the equation
> $$\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q} } -\frac{ \partial L }{ \partial q }=0 \quad\Rightarrow \quad m\ddot{q}+m\omega ^{2}q=0\quad\Rightarrow \quad \ddot{q}=-\omega ^{2}q$$
> which is the well known harmonic oscillator equation.

> [!example] Spherical pendulum
> We'll now use another oscillating system: a spherical pendulum, which is a [[simple pendulum]] that's constrained to remain on a sphere, instead of a circle. In plain English, it's a pendulum that swings in 2D. The position vector $\mathbf{r}(q)$ only needs two free coordinates, as that's the minimum to identify a point on a [[surface]] (which a sphere is). We'll use the angles $\theta$ and $\phi$ on a sphere of radius $R$.
> ![[Diagram Spherical pendulum]]
> 
> We want to express $x,y,z$ in terms of $\theta,\phi$. This is just the usual [[coordinate transformation]] from [[spherical coordinates]]:
> $$x=R\sin \theta \cos \phi,\quad y=R\sin \theta \sin \phi,\quad z=R\cos \theta$$
> The velocity vector $\mathbf{v}=(\dot{x},\dot{y},\dot{z})$ is also easy to find:
> $$\dot{x}=R\cos \theta \cos \phi \dot{\theta}-R\sin \theta \sin \phi \dot{\phi},\quad y=R\cos \theta \sin \phi \dot{\theta}+R\sin \theta \cos \phi \dot{\phi},\quad z=-R\sin \theta \dot{\theta}$$
> This is enough to find the kinetic energy
> $$\begin{align}
> T&=\frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2}) \\
> &=\frac{1}{2}m[(R^{2}\cos ^{2}\theta \cos ^{2}\phi \dot{\theta}^{2}-\cancel{ 2R^{2}\dot{\theta}\dot{\phi}\cos \theta \cos \phi \sin \theta \sin \phi }+R^{2}\sin ^{2}\theta \sin ^{2}\phi \dot{\phi} ^{2}) \\
> &\qquad \quad+(R^{2}\cos ^{2}\theta \sin ^{2}\phi \dot{\theta}^{2}+\cancel{ 2R^{2}\dot{\theta}\dot{\phi}\cos \theta \sin \phi \sin \theta \cos \phi }+R^{2}\sin ^{2} \theta \cos ^{2}\phi \dot{\phi}^{2}) \\
> &\qquad \quad+(R^{2}\sin ^{2}\theta \dot{\theta}) ] \\
> &=\frac{1}{2}m[R^{2}\sin ^{2}\theta \dot{\phi}^{2}+R^{2}\dot{\theta }^{2}]
> \end{align}$$
> where we used $\sin ^{2}x+\cos ^{2}x=1$. Remember that this quantity needs to be equal to
> $$T=\frac{1}{2}\sum_{j,k=1}^{n} a_{jk}\dot{q}_{j}\dot{q}_{k}$$
> In our case, $n=2$ and $q_{1}=\phi$ and $q_{2}=\theta$, so
> $$T=\frac{1}{2}(a_{11}\dot{\phi}^{2}+a_{12}\dot{\phi}\dot{\theta}+a_{21}\dot{\theta}\dot{\phi}+a_{22}\dot{\theta}^{2})$$
> The two off-diagonal mixed terms must evidently be null, whereas the diagonal terms must be $mR^{2}\sin ^{2}\theta$ and $mR^{2}$ respectively. The kinetic matrix then is
> $$\mathrm{a}=\begin{pmatrix}
> mR^{2}\sin ^{2}\theta & 0 \\
> 0 & mR^{2}
> \end{pmatrix}$$
> This is a function of $q$, since it depends on $\theta$.
>
> We now need the potential energy. For a pendulum, it's just gravity, so $V=mgz=mgR\cos \theta$. With both kinds of energies determined, we are ready to write the Lagrangian:
> $$L(\phi,\dot{\phi},\theta,\dot{\theta})=\frac{1}{2}mR^{2}(\sin ^{2}\theta \dot{\phi}^{2}+\dot{\theta}^{2})-mgR\cos \theta$$
> Through this, we get to the two Lagrange equation we need (one in $\theta$ and one in $\phi$). Firstly, let's differentiate $L$.
> $$\frac{ \partial L }{ \partial \theta }=mR^{2}\sin \theta \cos \theta \phi ^{2}+mgR\sin \theta,\quad\frac{ \partial L }{ \partial \dot{\theta} } =mR^{2}\dot{\theta},\quad \frac{d}{dt} \frac{ \partial L }{ \partial \dot{\theta} } =mR^{2}\ddot{\theta}$$
> which leads to
> $$mR^{2}\ddot{\theta}=mR^{2}\sin \theta \cos \theta \phi ^{2}+mgR\sin \theta$$
> Dividing through by $mR^{2}$ we get
> $$\ddot{\theta}=\sin \theta \cos \theta \phi ^{2}+ \frac{g}{R}\sin \theta$$
> Doing the same thing for $\phi$ gives
> $$\frac{ \partial L }{ \partial \phi } =0,\quad \frac{ \partial L }{ \partial \dot{\phi} } =mR^{2}\sin ^{2}\theta \dot{\phi},\quad \frac{d}{dt} \frac{ \partial L }{ \partial \dot{\phi} } =2mR^{2}\sin \theta \cos \theta \dot{\theta}\dot{\phi}+mR^{2}\sin ^{2}\theta \ddot{\phi}$$
> and so
> $$mR^{2}\sin ^{2}\theta \ddot{\phi}=-2mR^{2}\sin \theta \cos \theta \dot{\theta}\dot{\phi}$$
> Dividing through by $mR^{2}\sin ^{2}\theta$ gives
> $$\ddot{\phi}=-2\cot \theta \dot{\theta}\dot{\phi}$$
> When solved, these two equations provide the motion in both coordinates. We can then use the coordinate transformation to convert to $x,y,z$.

> [!example] Spring pendulum
> In this example, we'll analyze how a spring interacts with gravity. Consider a point mass attached to the $x$ axis by a spring of some elastic constant that always remains exactly vertical. Gravity pulls the mass down. Crucially, the spring is allowed to slide over the $x$ axis: thing of it like a clothes hanger on a metal pipe of sorts.
> 
> ![[Diagram Spring pendulum]]
> 
> We'll use [[polar coordinates]], with a distance $l$ and an angle $q$. The coordinate transformation back to $x$ and $y$ is $x=l\sin q$ and $y=-l\cos q$. Their derivatives are $\dot{x}=l\cos q\dot{q}$ and $\dot{y}=l\sin q\dot{q}$, which leads to kinetic energy
> $$T=\frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2})=\frac{1}{2}m(l^{2}\cos ^{2}q \dot{q}^{2}+l^{2}\sin ^{2}q \dot{q}^{2})=\frac{1}{2}ml^{2}\dot{q}^{2}$$
> The potential energy is a mix of gravitational and elastic potential:
> $$V(y)=mgy+ \frac{1}{2}ky^{2}=-mgl\cos q+ \frac{1}{2}kl^{2}\cos ^{2} q$$
> The Lagrangian is the usual $L=T-V$, but here it's more interesting to look at [[equilibrium point|equilibrium points]]. To find them, we need to find [[Punto critico|stationary points]] of the potential:
> $$V'(q)=mgl\sin q-kl^{2}\cos q\sin q=kl^{2}\sin q\left[ \frac{mg}{kl}-\cos q \right]$$
> This nullifies at $\sin q=0$, which means $q=0,\pi$. Alternatively, it nullifies for $\cos q=mg/kl$, which means $q=\arccos(mg/kl)$. Well, sort of. The arccosine is only defined in $[-1,1]$, so we can't allow $mg/kl$ to have any value. Such an equilibrium point *only* exists if $mg/kl\leq1$ (it's $>0$ because $m,g,k,l$ are all $>0$). To find which of these are minima, we need the second derivative:
> $$\begin{align}
> V''(q)&=mgl\cos q-kl^{2}\cos ^{2}q+kl^{2}\sin ^{2}q \\
> &=mgl\cos q-2kl^{2}\cos q+kl^{2}
> \end{align}$$
> For our guess in $q=0$ we see
> $$V''(0)=mgl-kl^{2}=\left( \frac{mg}{kl}-1 \right)kl^{2}$$
>  $mg/kl>1$, the $V''(0)>0$ and the point is stable. Else it is unstable. If $mg/kl=1$, $V''(0)=0$, which gives us no information on the point. We'd need the third derivative, or some other information about the point, which is beyond the interest of this example.
> 
> The guess $q=\pi$ leads to $V''(\pi)=-mgl-kl^{2}$ which is $<0$ everywhere, so it's never stable.
> 
> Now, as for the arccosine point, we can qualitatively analyze $mg/kl$. Since $g$ doesn't change and $m$ is not part of the construction, we'll look at $k$ and $l$. If the spring constant is very small ($k\ll 1$, and thus the string "pulls" very little), this value is very large, and so never $<1$. This tells us that this equilibrium point is reliant on a strong enough spring, or alternatively a very large pendulum ($l\gg 1$). In fact, if we look at the actual contraption, you'll see that the gravitational force applied to the point mass is going downwards (since $\mathbf{g}$ is also going downwards), but the spring response is going in the exact opposite direction, upwards. If the spring response is strong enough (read: $k$ is big), then it can fully cancel out $g$ and leave no force left, thus leaving the system at rest. But again, this can only happen if the spring is strong enough to counteract gravity; anything weaker and it'll be overcome.
> 
>Quantitatively, we'll check the potential. Call the two possible equilibrium points $q^{*}=\arccos(mg/kl)$ and $-q^{*}$:
> $$\begin{align}
> V''(\pm q^{*})&=mgl \frac{mg}{kl}-2kl^{2} \left( \frac{mg}{kl} \right)^{2}+kl^{2} \\
> &=\frac{(mg)^{2}}{k}- 2 \frac{(mg)^{2}}{k}+kl^{2} \\
> &=\frac{(kl)^{2}- (mg)^{2}}{k} \\
> &=\frac{(kl-mg)(kl+mg)}{k}> 0
> \end{align}$$
> This is because if these points exist, then $mg/kl<1$, which means $mg<kl$ and so $kl-mg>0$. So if the points exists, they are always stable. In summary:
> 
> $$\begin{array}{c|c}
>  & \frac{mg}{kl}<1 & \frac{mg}{kl}>1 \\
> q=0 & \text{unstable} & \text{stable} \\
> q=\pi & \text{unstable} & \text{unstable} \\
> q^{*} & \text{stable} & - \\
> -q^{*} & \text{stable} & -
> \end{array}$$
> 
> When plotted, they look like this:
> 
> ![[Plot Spring pendulum equilibrium points|80%]]
> 
> The two $q^{*}$ points split in the middle as the parameter $mg/kl$ goes lower. This shape is called a **bifurcation** and this graph allows us to get an idea of how the potential looks like by tracing a vertical line anywhere in the graph to fix any one $mg/kl$. Since stable points are potential minima and unstable ones are potential maxima, our potential has two behaviors. When $mg/kl\geq1$, it's a rather typical parabola, with maxima at $q=\pm \pi$ and minima at $q=0$; about what you'd expect from the usual pendulum. But when the spring gets rigid enough, $mg/kl<1$ and we start to see the characteristic behavior of this pendulum. The vertical is no longer a stable equilibrium point, so the two new "oblique" equilibrium points $\pm q^{*}$ come in as the "replacement" minima. This gives the potential *two* valleys with an additional central peak at $q=0$.

[^1]: $q(t)$ and $\dot{q}(t)$ are implicit in $T$, whereas $\ddot{q}(t)$ appears when taking the time derivative in the first term.
