---
wiki-publish: true
aliases:
  - Lagrangian system
---
The **Lagrange equation** is a second order[^1] differential equation that finds the motion of a [[Physical system|system]] from its [[energy]]:
$$\frac{d}{dt} \frac{ \partial T }{ \partial \dot{q}_{j} }(q(t),\dot{q}(t),t)- \frac{ \partial T }{ \partial q_{j} } (q(t),\dot{q}(t),t)=Q_{j} $$
Here $T$ is the [[kinetic energy]], $q(t)$ is the motion in [[generalized coordinates]] $q_{j}$ and $Q_{j}$ are the [[generalized force|generalized forces]]. The value $j=1,\ldots,n$ depends on the [[degrees of freedom]] $n$ of the system.

If the system is subject to [[Vector field|conservative forces]] and can be written in terms of a [[potential]] $V$, we can further define the **[[Lagrangian]]** $L=T-V$ to rewrite the equation as
$$\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{i} }(q(t),\dot{q}(t),t)-\frac{ \partial L }{ \partial q_{i} } (q(t),\dot{q}(t),t)=0 $$
A [[dynamical system]] whose equations of motion can be written in this form is said to be a **Lagrangian system**.

The benefit of using a set of Lagrange equations over a set of [[Newton's laws|Newton's second laws]] is that they allow picking a parameterization of the [[Constraint|constraints]] such that the constraint forces vanish. The equations that are left can then be solved algorithmically by [[Differential|differentiation]], which is typically far easier than what would be necessary with Newton's laws and can also be offloaded to a computer for numerical differentiation.
### Validity
This equation is correct *point-wise*, for each $t\in \mathbb{R}^{+}$, and for this reason it is said that the Lagrange equation describes motion **locally** (as opposed to globally). See [[Global motion]].
### Velocity-dependent forces
Many [[force|forces]] do not depend on velocity. Examples including the force applied by gravity or the spring pullback force. In these cases, the generalized forces, which inherits arguments from the regular forces, also do not. In other cases though, such as [[friction]] or the [[Lorentz force]], the forces depend explicitly on velocity and the signature becomes $Q_{j}\equiv Q_{j}(q(t),\dot{q}(t),t)$ with the force itself being
$$Q_{j}=\frac{d}{dt} \frac{ \partial V }{ \partial \dot{q}_{j} } (q,t)-\frac{ \partial V }{ \partial q_{j} } (q,t)$$
See the examples below on the Coriolis force, inertial frames and electromagnetic forces for practical results on this.
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

> [!example] Coriolis force
> The Coriolis force is defined as $\mathbf{F}=2m \dot{\mathbf{q}}\times \boldsymbol{\omega}$. $\boldsymbol{\omega}$ is assumed to be constant. The $j$-th component is determined by the potential by
> $$F_{j}=\frac{d}{dt} \frac{ \partial V }{ \partial \dot{q}_{j} } -\frac{ \partial V }{ \partial q_{j} } $$
> The potential is $V(q,\dot{q})=-m(\dot{\mathbf{q}}\times \boldsymbol{\omega})\cdot \mathbf{q}$[^2]. Before we take the derivatives, we should expand the mixed product. The [[scalar product]] of a [[cross product]] in general is
> $$\begin{align}
> (\mathbf{a}\times \mathbf{b})\cdot \mathbf{c}&=\left( \sum_{i,j,k=1}^{3} \epsilon_{ijk}a_{i}b_{j}\mathbf{e}_{k} \right)\cdot\left( \sum_{l}c_{l}\mathbf{e}_{l}  \right) \\
> &=\sum_{i,j,k=1}^{3} \epsilon_{ijk}a_{i}b_{j}c_{l}\underbrace{ \mathbf{e}_{k}\cdot \mathbf{e}_{j} }_{ \delta_{kj} } \\
> &=\sum_{i,j,k=1}^{3} \epsilon_{ijk}a_{i}b_{j}c_{k} \\
> &=\sum_{i,j,k=1}^{3} \epsilon _{jki}b_{j}c_{k}a_{i} \\
> &=\mathbf{a}\cdot (\mathbf{b}\times \mathbf{c})
> \end{align}$$
> using the [[Tensore di Levi-Civita|Levi-Civita tensor]] and the [[Kronecker delta]]. Now we can rewrite the potential as
> $$V(q,\dot{q})=-m \dot{\mathbf{q}}\cdot(\boldsymbol{\omega}\times \mathbf{q})=-m [\dot{q}_{1}(\boldsymbol{\omega}\times \mathbf{q})_{1}+\dot{q}_{2}(\boldsymbol{\omega}\times \mathbf{q})_{2}+\ldots]$$
> The derivatives over the motion are
> $$\frac{ \partial V }{ \partial \dot{q}_{j} } =-m(\boldsymbol{\omega}\times \mathbf{q})_{j}\quad\to \quad \frac{d}{dt} \frac{ \partial V }{ \partial \dot{q}_{j} } =-m(\boldsymbol{\omega}\times \dot{\mathbf{q}})=m(\dot{\mathbf{q}}\times \boldsymbol{\omega})_{j}$$
> and also
> $$\frac{ \partial V }{ \partial q_{j} } =-m(\dot{\mathbf{q}}\times \boldsymbol{\omega})_{j}$$
> So if we plug these in the definition of the force components we get
> $$F_{j}=2m(\dot{\mathbf{q}}\times \boldsymbol{\omega})_{j}$$
> which is exactly our Coriolis force.

> [!example] 3D free particle in an inertial frame of reference
> Another typical case of velocity dependence is a [[free particle]] in an inertial [[frame of reference]]. Since there is no potential, Lagrangian is just the kinetic energy:
> $$L(x,y,z,\dot{x},\dot{y},\dot{z})=\frac{m}{2}(\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2})$$
> The issue here figuring out the motion relative to the moving frame. Normally, this would require a lot of imagination and lengthy mathematics to try to understand the relative motion. The benefit of Lagrangian mechanics is that no such thing is needed: since frame changes lead to apparent forces, the process of figuring this out is identical to any other force and is just a matter of applying the usual mathematical algorithm; no fancy methods required.
>
> Since it's inertial, the frame must move at a constant velocity. In our case, we set it to uniform circular motion of [[Frequency|angular frequency]] $\omega$ on the $xy$ plane, such that the [[coordinate transformation]] is
> $$x=q_{1}\cos \omega t-q_{2}\sin \omega t,\quad y=q_{1}\sin \omega t-\cos \omega t,\quad z=q_{3}$$
> The Lagrangian is dependent only on the derivatives, so we find those
> $$\begin{align}
> \dot{x}&=\dot{q}_{1}\cos \omega t-\dot{q}_{2}\sin \omega t-q_{1}\omega \sin \omega t-q_{2}\omega \cos \omega t \\
> \dot{y}&=\dot{q}_{1}\sin \omega t+\dot{q}_{2}\cos \omega t+q_{1}\omega \cos \omega t-q_{2}\omega \sin \omega t \\
> \dot{z}&=\dot{q}_{3}
> \end{align}$$
> We now add these in the Lagrangian equation. As you might imagine, this leads to a really complicated expression due to the squares. Thankfully, we can use some trigonometry to delete some terms before we even write them. For one, $\cos ^{2}\theta+\sin ^{2}\theta=1$ merges several terms and $\cos ^{2}\theta-\sin ^{2}\theta=$; you can see these stacked on top of each other in $\dot{x}$ and $\dot{y}$. In the end, we get
> $$L(\dot{x},\dot{y},\dot{z})=\frac{m}{2}(\dot{q}^{2}_{1}+\dot{q}^{2}_{2}+\dot{q}^{2}_{3})+ \frac{m}{2}\omega ^{2}(q_{1}^{2}+q_{2}^{2})-m \dot{q}_{1}q_{2}\omega+m \dot{q}_{2}q_{1}\omega$$
> The last two terms can be rewritten to be more meaningful using a cross product:
> $$-m \dot{q}_{1}q_{2}\omega+m \dot{q}_{2}q_{1}\omega=m\omega(q_{1} \dot{q}_{2}-q_{2} \dot{q}_{1})=m\omega(\mathbf{q}\times \dot{\mathbf{q}}_{3})$$
> The final result is
> $$L(\dot{x},\dot{y},\dot{z})=\frac{m}{2}(\dot{q}^{2}_{1}+\dot{q}^{2}_{2}+\dot{q}^{2}_{3})+ \frac{m}{2}\omega ^{2}(q_{1}^{2}+q_{2}^{2})-m\omega(\mathbf{q}\times \dot{\mathbf{q}})$$

> [!example] Electromagnetic forces
> The [[Lorentz force]] is dependent on speed when an [[electric charge]] moves through a [[magnetic field]] is present. The force is
> $$\mathbf{F}=e(\mathbf{E}+\dot{\mathbf{q}}\times \mathbf{B})$$
> for a charge $e$ (we're not using $q$ to avoid overwriting the generalized coordinate). The [[electric field]] is in general
> $$\mathbf{E}=-\left( \nabla \phi+\frac{ \partial \mathbf{A} }{ \partial t }  \right)$$
> and the magnetic field is
> $$\mathbf{B}=\nabla\times \mathbf{A}$$
> where $\phi$ is the [[electric potential]] (not to be confused with $V$ the potential *energy*) and $\mathbf{A}$ is the [[magnetic vector potential]].
> 
> The potential energy is given by
$$V(q,\dot{q})=e\phi-e \dot{\mathbf{q}}\cdot \mathbf{A}$$
> Now we have everything we need to find the force:
> $$\begin{align}
> F_{n}&=\frac{d}{dt} \frac{ \partial V }{ \partial \dot{q}_{n} } -\frac{ \partial V }{ \partial q_{n} }  \\
> &=\frac{d}{dt} (-eA_{n}(q,t))-e\frac{ \partial \phi }{ \partial q_{n} } +e \dot{\mathbf{q}}\cdot \frac{ \partial \mathbf{A} }{ \partial q_{n} }  \\
> &=-e\frac{ \partial A_{n} }{ \partial t } -e\sum_{k=1}^{3} \frac{ \partial A_{n} }{ \partial q_{k} } \dot{q}_{k}-e\frac{ \partial \phi }{ \partial q_{n} } +e\sum_{l=1}^{3} \dot{q}_{l} \frac{ \partial A_{l} }{ \partial q_{n} }  \\
> &=-e\left( \frac{ \partial \phi }{ \partial q_{n} } +\frac{ \partial A_{n} }{ \partial t }  \right)+e\sum_{l=1}^{3} \dot{q}_{l}\frac{ \partial A_{l} }{ \partial q_{n} } -e\sum_{k=1}^{3} \dot{q}_{k}\frac{ \partial A_{n} }{ \partial q_{k} } 
> \end{align}$$
> This is kind of a mess: ideally there's some vector operations to compress this into. In fact, if this is to be equal to the Lorentz force, then the last two terms must end up being $e(\dot{\mathbf{q}}\times(\nabla\times \mathbf{A}))_{n}$. Using the shorthand $\frac{ \partial A_{j} }{ \partial q_{i} }\equiv\partial_{i}A_{j}$, we find that
> $$\begin{align}
> -[(\nabla\times \mathbf{A})\times \dot{\mathbf{q}}]_{n}&=-\sum_{l,m=1}^{3} \left( \sum_{i,j=1}^{3} \epsilon_{lij} \partial_{i}A_{j} \right)\dot{q}_{m}\epsilon_{nlm} \\
> &=\sum_{m,i,j=1}^{3} \partial_{i}A_{j}\dot{q}_{m}\sum_{l=1}^{3} \underbrace{ \epsilon_{lij}\epsilon_{lnm} }_{ \delta_{in}\delta_{jm}-\delta_{im}\delta_{jn} } \\
> &=\sum_{m,i,j=1}^{3} \partial_{i}A_{j}\dot{q}_{m}\delta_{in}\delta_{jm}-\sum_{m,i,j=1}^{3} \partial_{i}A_{j}\dot{q}_{m}\delta_{im}\delta_{jn} \\
> &=\ldots
> \end{align}$$
> Here we use the Kronecker deltas to delete some indexes. $i$ and $j$ vanish, leaving only $n$ and $m$. The last step is
> $$\ldots=\sum_{m=1}^{3} \dot{q}_{m}\frac{ \partial A_{n} }{ \partial q_{m} } -\dot{q}_{n}\frac{ \partial A_{m} }{ \partial q_{n} }$$
> which are the terms above.
> 
> The Lagrangian can then be written in general as
> $$L=\frac{m}{2}\dot{\mathbf{q}}^{2}-e\phi(q,t)+e \dot{\mathbf{q}}\cdot \mathbf{A}(q,t)$$
> which is a [[Lagrange equation]] of the form $m \ddot{q}=\mathbf{F}$.
> 
> If $\mathbf{B}=0$, then $\nabla\times \mathbf{A}=0$ and $\mathbf{E}=-\nabla \phi$. Since the vector potential is now irrotational, it can also be expressed by a potential, say $\chi$, as $\mathbf{A}=\nabla \chi$. (TODO: Finish this, end of lesson 26/03/2025; gauge transformation).
> 
> If $\mathbf{B}$ is constant, then we want to find what kind of $\mathbf{A}$ leads to a constant $\nabla\times \mathbf{A}$. If $\mathbf{B}$ is entirely on the $z$ axis, we have
> $$\mathbf{B}=\begin{pmatrix}
> 0 \\
> 0 \\
> B
> \end{pmatrix},\qquad \mathbf{A}=\frac{1}{2}\begin{pmatrix}
> -B_{y} \\
> B_{x} \\
> 0
> \end{pmatrix}$$
> In fact, the curl of $\mathbf{A}$ is
> $$\nabla\times \mathbf{A}=\det\begin{pmatrix}
> \mathbf{e}_{1} & \partial_{x} & - \frac{B_{y}}{2} \\
> \mathbf{e}_{2} & \partial_{y} &  \frac{B_{x}}{2} \\
> \mathbf{e}_{3} & \partial_{z} & 0
> \end{pmatrix}=\left( \frac{B}{2}+ \frac{B}{2} \right)\mathbf{e}_{3}=\begin{pmatrix}
> 0 \\
> 0 \\
> B
> \end{pmatrix}$$
> The Lagrangian is
> $$L=\frac{m}{2}(\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2})+ \frac{e}{2}B(x \dot{y}-y \dot{x})=\frac{m}{2}(\dot{r}^{2}+r^{2}\dot{\varphi}^{2}+\zeta ^{2})+ \frac{e}{2}B^{2}r^{2}\dot{\varphi}$$
> where we also switched to [[cylindrical coordinates]].

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
[^2]: For instance, for a centrifugal force we have $V(q)=- \frac{1}{2}m\omega ^{2}d^{2}(q)$. 
