---
wiki-publish: true
aliases:
  - kinetic matrix
---
**Kinetic energy** is a form of [[energy]] that an object gains due to motion. For a [[point mass]] of [[mass]] $m$, velocity $\mathbf{v}$ and [[linear momentum]] $\mathbf{p}=m\mathbf{v}$, it is
$$K=\frac{1}{2}m\lvert \mathbf{v} \rvert^{2} =\frac{\lvert \mathbf{p} \rvert ^{2}}{2m}$$
In many cases, such as an extended object like a [[rigid body]], the kinetic energy also likely includes other contributions, such as rotational energy, vibrational energy and so on. For instance, if the point mass it also [[Rotation|rotating]] around an axis, it also gains additional rotational kinetic energy, which is described in the simplest form through the [[Moment of inertia|inertia tensor]] $\mathcal{I}$ as
$$T=\frac{1}{2}\boldsymbol{\omega}\times \mathcal{I}\boldsymbol{\omega}$$
 In a system of $N$ point masses, it is simply the sum of all individual kinetic energies:
$$K=\frac{1}{2}\sum_{i=1}^{N} m_{i}\lvert \mathbf{v}_{i} \rvert ^{2}$$
The sum of kinetic and [[potential energy]] is called the **mechanical energy** of the body or [[Physical system|system]].
### In analytical mechanics
Kinetic energy naturally comes up quite often in analytical mechanics. In this context, a few additional details are useful to know:
- it depends on the [[stato|state]] of the body, that is, it is a function of both [[generalized coordinates]], their velocities and (possibly) time: $(q_{1},\ldots,q_{n},\dot{q}_{1},\ldots,\dot{q}_{n},t)\equiv(q,\dot{q},t)$ where $n$ is the number of [[degrees of freedom]] the body has;
- it is a [[dynamical variable]] of the form $T:\mathbb{R}^{2n+1}\to \mathbb{R},\ (q,\dot{q},t)\to T(q,\dot{q},t)$.

For consistency with typical notation, we'll use $\mathbf{r}_{i}(q,t)$ and $\mathbf{v}_{i}(q,\dot{q},t)$ as the position and velocity of the $i$-th point mass in a system of $N$ of them, each with $n$ degrees of freedom. Generalized velocities are given as the [[Differential|total derivative]] of $\mathbf{r}$ in time:
$$\mathbf{v}_{i}(q,\dot{q},t)=\sum_{j=1}^{n} \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} }(q,t) \dot{q}_{j}+\frac{ \partial \mathbf{r}_{i} }{ \partial t } (q,t) $$
(If the velocity is not explicitly dependent on time, the last term disappears.) Since $\lvert \mathbf{v} \rvert^{2}=\mathbf{v}\cdot \mathbf{v}$, the kinetic energy then is
$$\begin{align}
T&=\frac{1}{2}\sum_{i=1}^{N} m_{i}\left( \sum_{j=1}^{n} \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } \dot{q}_{j} +\frac{ \partial \mathbf{r}_{i} }{ \partial t } \right)\cdot\left( \sum_{k=1}^{n} \frac{ \partial \mathbf{r}_{i} }{ \partial q_{k} } \dot{q}_{k} +\frac{ \partial \mathbf{r}_{i} }{ \partial t } \right) \\
&=\frac{1}{2}\sum_{i=1}^{N} m_{i}\left( \sum_{j,k=1}^{n} \dot{q}_{j}\dot{q}_{k}\frac{ \partial \mathbf{r}_{j} }{ \partial q_{j} }\cdot \frac{ \partial \mathbf{r}_{k} }{ \partial q_{k} } +2\sum_{l=1}^{n} \dot{q}_{l}\frac{ \partial \mathbf{r}_{i} }{ \partial q_{l} } \cdot \frac{ \partial \mathbf{r}_{i} }{ \partial t }  +\frac{ \partial \mathbf{r}_{i} }{ \partial t } \cdot \frac{ \partial \mathbf{r}_{i} }{ \partial t }  \right) \\
&=\frac{1}{2}\sum_{j,k=1}^{n} \underbrace{ \left( \sum_{i=1}^{N} m_{i} \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } \cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{k} } \right) }_{\equiv a_{jk}(q,t) }\dot{q}_{j}\dot{q}_{k}+ \sum_{l=1}^{n} \underbrace{ \left( \sum_{i=1}^{N} m_{i}\frac{ \partial \mathbf{r}_{i} }{ \partial q_{l} }\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial t } \right) }_{ \equiv b_{l}(q,t) }\dot{q}_{l}+ \frac{1}{2}\underbrace{ \sum_{i=1}^{N} m_{i}\frac{ \partial \mathbf{r}_{i} }{ \partial t } \cdot \frac{ \partial \mathbf{r}_{i} }{ \partial t } }_{ \equiv c(q,t) } 
\end{align}$$
In the second step, we just computed the [[scalar product]]. In the third step, we opened up the brackets and inverted the order of the sums in each of the three steps, then defined some convenience functions to show how those terms are fully determined by their indexes. Of note is that $a_{jk}$ is quadratic (second order) with respect to $\dot{q}$, $b_{l}$ is linear (first order) and $c$ is constant (zeroth order). We can identify these three separate scaling behaviors with three energy terms:
$$T=T_{2}+T_{1}+T_{0}$$
where the subscript denotes the order of the term. These are
$$\begin{align}
T_{2}&=\frac{1}{2}\sum_{j,k=1}^{n}a_{jk}(q,t)\dot{q}_{j}\dot{q}_{k} \\
T_{1}&=\sum_{l=1}^{n} b_{l}(q,t)\dot{q}_{l} \\
T_{0}&=\frac{1}{2}c(q,t)
\end{align}$$
Of the three, $T_{2}$ is the most interesting, because if $\mathbf{r}$ is not explicitly time-dependent, $\mathbf{r}=\mathbf{r}(q)$, then of course $\partial \mathbf{r}_{i}/\partial t=0$ for all $i$. But this implies that $b_{l}(q,t)=0$ and $c(q,t)=0$ everywhere, which deletes the $T_{1}$ and $T_{0}$ terms. In such a case, the kinetic energy is uniquely determined by $T_{2}$:
$$T=T_{2}\qquad(\text{if }\mathbf{r}=\mathbf{r}(q))$$
This occurs, for instance, if motion is subject to fixed [[Constraint|constraints]], which are a common and useful situation in mechanics.

> [!example] Cylindrical motion
> As an example of how to find the kinetic energy in different coordinate systems, we'll consider a point mass in [[cylindrical coordinates]] for which
> $$x=r\cos \theta,\quad y=r\sin \theta,\quad z=\zeta$$
> (we use $\zeta$ instead of $z$ in cylindrical coordinates just for clarity). We'll want to find velocity in terms of cylindrical ones, so we use
> $$\mathbf{v}(q,\dot{q})=\sum_{i=1}^{3} \frac{ \partial \mathbf{r} }{ \partial q_{i} } \dot{q}_{i}$$
> where $\mathbf{r}=(x,y,z)$ and $q_{i}=r\cos \theta,r\sin \theta,\zeta$. Written out in full:
> $$\mathbf{v}(q,\dot{q})=\frac{ \partial \mathbf{r} }{ \partial r } \dot{r}+\frac{ \partial \mathbf{r} }{ \partial \theta } \dot{\theta}+\frac{ \partial \mathbf{r} }{ \partial \zeta } \dot{\zeta}$$
> On the $x$ axis
> $$v_{x}=\frac{ \partial x }{ \partial r } \dot{r}+\frac{ \partial x }{ \partial \theta } \dot{\theta}+\frac{ \partial x }{ \partial \zeta } \dot{\zeta}=\cos \theta\ \dot{r}-r\sin \theta \ \dot{\theta}$$
> On the $y$ axis
> $$v_{y}=\frac{ \partial y }{ \partial r } \dot{r}+\frac{ \partial y }{ \partial \theta } \dot{\theta}+\frac{ \partial y }{ \partial \zeta } \dot{\zeta}=\sin \theta\ \dot{r}+r\cos \theta \ \dot{\theta}$$
> On the $z$ axis
> $$v_{z}=\frac{ \partial z }{ \partial r } \dot{r}+\frac{ \partial z }{ \partial \theta } \dot{\theta}+\frac{ \partial z }{ \partial \zeta } \dot{\zeta}=\dot{\zeta}$$
> So our velocity expressed in cylindrical coordinates is
> $$\mathbf{v}=(\cos \theta \dot{r}-r\sin \theta \dot{\theta},\sin \theta \dot{r}+r\cos \theta \dot{\theta},\dot{\zeta})$$
> Our kinetic energy must therefore be
> $$\begin{align}
> T&=\frac{1}{2}m\lvert \mathbf{v} \rvert ^{2}=\frac{1}{2}m(v^{2}_{x}+v^{2}_{y}+v^{2}_{z}) \\
> &=\frac{m}{2}[\cos ^{2}\theta \dot{r}^{2}+r^{2}\sin ^{2}\theta \dot{\theta}^{2}-2r \dot{r}\dot{\theta}\cos \theta \sin \theta \\
> &\qquad +\sin ^{2}\theta \dot{r}^{2}+r^{2}\cos ^{2}\theta \dot{\theta}^{2}+2r \dot{r}\dot{\theta}\cos\theta \sin \theta+\dot{\zeta}^{2}]
> \end{align}$$
> Recalling that $\sin ^{2}\theta+\cos ^{2}\theta=1$, I hope that you can see that the first two columns simplify greatly whereas the third column cancels out. We are left with
> $$T=\frac{m}{2}(\dot{r}^{2}+r^{2}\dot{\theta}^{2}+\dot{\zeta}^{2})$$
#### The kinetic matrix
Let's now focus our attention to just the term $T_{2}$ and more specifically $a_{jk}(q,t)$. This quantity is known as the **kinetic matrix**, because it is, in fact, a matrix. If we write $T_{2}$ as
$$T_{2}=\sum_{j=1}^{n} \dot{q}_{j}\sum_{k=1}^{n}a_{jk}\dot{q}_{k} =\dot{\mathbf{q}}_{j}\cdot \mathrm{a}\,\dot{\mathbf{q}}_{k}$$
we can see that $\mathrm{a}$ has the shape of a matrix and $a_{jk}$ are its components. It has a few interesting properties:
- it is [[Matrice simmetrica|symmetric]], $a_{jk}=a_{kj}$. This follows from being defined by a real scalar product.
- it is [[Matrix sign definitions|positive definite]], that is, $\mathbf{v}\cdot \mathrm{a}\,\mathbf{v}>0$ for all $\mathbf{v}\neq 0\in \mathbb{R}^{n}$.
- it is [[Invertible matrix|invertible]], since it is positive definite.
