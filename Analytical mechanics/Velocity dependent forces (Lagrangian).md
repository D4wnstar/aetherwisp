Let $T(q,\dot{q},t)$ be the [[kinetic energy]] and $V(q,\dot{q},t)$ a [[potential energy]]. Then
$$\frac{d}{dt} \frac{ \partial T }{ \partial \dot{q}_{n} } (q(t),\dot{q}(t),t)-\frac{ \partial T }{ \partial q_{n} } (q(t),\dot{q}(t),t)=Q_{n}(q(t),\dot{q}(t),t)$$
where $Q_{n}$ is a [[generalized force]] equal to
$$Q_{n}=-\frac{ \partial V }{ \partial q_{n} } (q,t)+\frac{d}{dt} \frac{ \partial V }{ \partial \dot{q}_{n} } (q,t)$$
The [[Lagrangian]] is $L=T-V$ and we have
$$\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{n} }-\frac{ \partial L }{ \partial q_{n} }=0  $$
If
$$Q_{n}(q(t),\dot{q}(t),t)=\frac{d}{dt} \frac{ \partial V }{ \partial \dot{q}_{n} } (q(t),\dot{q}(t),t)-\frac{ \partial V }{ \partial q_{n} } (q(t),\dot{q}(t),t)$$
where $V(q,\dot{q},t)$ is a velocity-dependent potential. These arise, for instance, in [[drag]], the [[Lorentz force]] or apparent forces like the Coriolis force. Let's start for the last one.

> [!example] Coriolis force
> The Coriolis force is defined as $\mathbf{F}=2m \dot{\mathbf{q}}\times \boldsymbol{\omega}$. $\boldsymbol{\omega}$ is assumed to be constant. The $j$-th component is determined by the potential by
> $$F_{j}=\frac{d}{dt} \frac{ \partial V }{ \partial \dot{q}_{j} } -\frac{ \partial V }{ \partial q_{j} } $$
> The potential is $V(q,\dot{q})=-m(\dot{\mathbf{q}}\times \boldsymbol{\omega})\cdot \mathbf{q}$[^1]. Before we take the derivatives, we should expand the mixed product. The [[scalar product]] of a [[cross product]] in general is
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
> Another typical case is a [[free particle]] in an inertial [[frame of reference]]. Since there is no potential, Lagrangian is just the kinetic energy:
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

If $\mathbf{B}$ is constant, then we want to find what kind of $\mathbf{A}$ leads to a constant $\nabla\times \mathbf{A}$. If $\mathbf{B}$ is entirely on the $z$ axis, we have
$$\mathbf{B}=\begin{pmatrix}
0 \\
0 \\
B
\end{pmatrix},\qquad \mathbf{A}=\frac{1}{2}\begin{pmatrix}
-B_{y} \\
B_{x} \\
0
\end{pmatrix}$$
In fact, the curl of $\mathbf{A}$ is
$$\nabla\times \mathbf{A}=\det\begin{pmatrix}
\mathbf{e}_{1} & \partial_{x} & - \frac{B_{y}}{2} \\
\mathbf{e}_{2} & \partial_{y} &  \frac{B_{x}}{2} \\
\mathbf{e}_{3} & \partial_{z} & 0
\end{pmatrix}=\left( \frac{B}{2}+ \frac{B}{2} \right)\mathbf{e}_{3}=\begin{pmatrix}
0 \\
0 \\
B
\end{pmatrix}$$
The Lagrangian is
$$L=\frac{m}{2}(\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2})+ \frac{e}{2}B(x \dot{y}-y \dot{x})=\frac{m}{2}(\dot{r}^{2}+r^{2}\dot{\varphi}^{2}+\zeta ^{2})+ \frac{e}{2}B^{2}\dot{\varphi}$$
where we also switched to [[cylindrical coordinates]].



[^1]: For instance, for a centrifugal force we have $V(q)=- \frac{1}{2}m\omega ^{2}d^{2}(q)$. 
