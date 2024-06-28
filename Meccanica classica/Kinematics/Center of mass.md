The **center of mass** is the imaginary point in space related to a system of $n$ [[Particella|particles]] defined by the position vector
$$\vec{r}_{C}=\frac{\sum\limits_{i=1}^{n}m_{i}\vec{r}_{i}}{\sum\limits_{i=1}^{n}m_{i}}=\frac{1}{M}\sum\limits_{i=1}^{n}m_{i}\vec{r}_{i}$$
with $M=\sum\limits_{i} m_{i}$ the total mass of the system. In case of a mass continuum, it is defined as
$$\vec{r}_{C}=\frac{\int \vec{r}\ dm}{\int dm}=\frac{1}{M}\int \vec{r}dm$$
Moreover, if the system is homogeneous and has a constant density $\rho$, then its center of mass is dependent only on the geometry of the body:
$$\vec{r}_{C}=\frac{1}{V}\int\vec{r}\ dV$$
with $V$ the volume of the body.

The center of mass is the point in space for which the moment of force about it is zero. The center of mass does not need to be part of the object itself.
### Specific forms
The formulas above are completely generic and work in any case. It is convenient to solve the equations for common mass continuum systems in one, two and three dimensions.
#### One dimension (wire)
A one-dimensional mass continuum can be thought of as a wire from $a$ to $b$. Give this wire a linear mass density $\lambda(x)$. The center of mass $x_{C}$ is
$$x_{C}=\frac{\int_{a}^{b}\lambda(x)x\ dx}{\int_{a}^{b}\lambda(x)\ dx}$$
If the material is homogeneous, $\lambda(x)$ is constant and we get
$$x_{C}=\frac{b+a}{2}$$
which is the midpoint of the wire.
#### Two dimensions (plate)
A two-dimensional mass continuum can be thought of as a plate of area $A$. Give this plate a surface mass density $\sigma(x,y)$. The center of mass $\vec{r}_{C}$ is
$$\vec{r}_{C}=\frac{\iint_{A}\sigma(x,y)\vec{r}\ dxdy}{\iint_{A}\sigma(x,y)\ dxdy}$$
#### Two dimensions (wire)
It's possible to have a one-dimensional wire in two-dimensional space. In this case, we can extend the one dimensional case by parameterizing the [[curva|curve]] it sits on. Consider the wire as a continuous and differentiable curve $s(t)=(x(t),y(t))$, with $t\in[a,b]$. The linear density is expressed in terms of the arc length $\lambda(s)$ or, alternatively, in terms of the parameter $\bar{\lambda}(t)$. The unit of arc length $ds$ is expressed in terms of the rate of change of position on the arc
$$ds=\left|\left|\frac{d\vec{s}}{dt}\right|\right|dt=\sqrt{\left(\frac{dx}{dt}\right)^{2}+\left(\frac{dy}{dt}\right)^{2}}dt=\sqrt{\dot{x}^{2}+\dot{y}^{2}}\ dt$$
which means that the center of mass is
$$\vec{r}_{C}=\frac{(\int x(t)\lambda(t)ds, \int y(t)\lambda(t)ds)}{\int \lambda(t)ds}$$
or in terms of $t$
$$\vec{r}_{C}=\frac{(\int x(t)\lambda(t)\sqrt{\dot{x}^{2}+\dot{y}^{2}}\ dt,\  \int y(t)\lambda(t)\sqrt{\dot{x}^{2}+\dot{y}^{2}}\ dt)}{\int \lambda(t)\sqrt{\dot{x}^{2}+\dot{y}^{2}}\ dt}$$
#### Three dimensions (volume)
A three-dimensional continuum is a volume $V$. Give this volume a volume mass density $\rho(x,y,z)$. The center of mass $\vec{r}_{C}$ is
$$\vec{r}_{C}=\frac{\iiint_{V}\rho(x,y,z)\vec{r}\ dxdydz}{\iiint_{V}\rho(x,y,z)\ dxdydz}$$
#### Three dimensions (sheet)
Like in the two-dimensional wire case above, we can have two-dimensional sheet in three-dimensional space. We can parameterize this as a [[Superficie|surface]] $\Phi:\Omega\subset \mathbb{R}^{3}\rightarrow\mathbb{R}^{2}$ with $\Omega=[a,b]\times[c,d]$ and $\Phi(u,v)=(x(u,v),y(u,v),z(u,v))$, with the surface unit defined as
$$d\Phi=\left|\frac{\partial \Phi}{\partial u}\times\frac{\partial \Phi}{\partial v}\right|dudv$$
Given a volume mass density $\rho(x,y,z)$, the center of mass $\vec{r}_{C}$ is
$$\vec{r}_{C}=\frac{\iint_{\Omega}\rho(\Phi(u,v))\Phi(u,v)\ d\Phi}{\iint_{\Omega}\rho(\Phi(u,v))\ d\Phi}$$
or in terms of each component
$$\vec{r}_{C}=\frac{(\iint_{\Omega}\rho(\Phi(u,v))x(u,v)\ d\Phi, \iint_{\Omega}\rho(\Phi(u,v))y(u,v)\ d\Phi, \iint_{\Omega}\rho(\Phi(u,v))z(u,v)\ d\Phi)}{\iint_{\Omega}\rho(\Phi(u,v))\ d\Phi}$$
#### Three dimensions (wire)
The same can be said about a wire in three dimensions. We can parameterize it as a curve $\gamma(t):I \rightarrow \mathbb{R}^{3}$ with $I=[a,b]$ and $\gamma(t)=(x(t),y(t),z(t))$. The surface unit is
$$d\gamma=\left|\left|\frac{d\gamma}{dt}\right|\right|dt=\sqrt{\left(\frac{dx}{dt}\right)^{2}+\left(\frac{dy}{dt}\right)^{2}+\left(\frac{dz}{dt}\right)^{2}}dt=\sqrt{\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2}}\ dt$$
Given a volume mass density $\rho(x,y,z)$, the center of mass $\vec{r}_{C}$ is
$$\vec{r}_{C}=\frac{\int_{I}\rho(\gamma(t))\gamma(t)\ d\gamma}{\int_{I}\rho(\gamma(t))\ d\gamma}$$
### Center of mass theorems
The center of mass theorems are three results that characterize the center of mass.
#### First theorem
Given a system of particles or a mass continuum, the linear momentum can be considered as being entirely contained within the center of mass, which can be seen as an imaginary point mass:
$$\vec{Q}=M\vec{v}_{C}$$
where $\vec{v}_{C}$ is the velocity of the center of mass. As usual, if no external force is applied on the system, this momentum is conserved.
#### Second theorem
Assuming the total mass $M$ of the system/continuum is constant, the center of mass moves as if it where a point mass with the total external force applied onto it:
$$\vec{F}^{(e)}=M\vec{a}_{C}$$
where $\vec{a}_{C}$ is the acceleration of the center of mass.
#### Third theorem
Given an axis of rotation $\Omega$, the angular momentum of the system about that axis can be calculated as the sum of the angular moment about the center of mass, plus the additional term $\vec{r}_{C}\times\vec{Q}$:
$$\vec{L}_\Omega=\vec{L}_{C}+\vec{r}_{C}\times\vec{Q}$$
where $\vec{r}_{C}$ is the position of the center of mass and $\vec{Q}$ is its linear momentum from the first theorem. This formula can also be generalized to a moving inertial [[frame of reference]] as the angular momentum is constant between inertial frames. Thus, given two frames $S$ and $S'$, where $S'$ is in translational motion at constant speed, the previous formula becomes
$$\vec{L}_\Omega=\vec{L}'_{C}+\vec{r}_{C}\times\vec{Q}$$
where the angular momentum about the center is calculated is $S'$, whereas the total momentum is in $S$. This allows us to decouple the system's angular momentum from any given inertial frame. This form is called **König's theorem for angular momentum**.
#### König's theorem for kinetic energy
As an additional result, the kinetic energy of a system can be expressed entirely through the center of mass. Consider two inertial frames, $S$ and $S'$, where $S$ is fixed and $S'$ is centered in the center of mass and is in translational motion at constant velocity $\vec{v}_{C}$ with respect to $S$. The kinetic energy of a system is
$$K=K'+K_{C}=K'+\frac{1}{2}M||\vec{v}_C ||^{2}$$
where $K'$ is the kinetic energy of the system in $S'$ and $K_{C}$ is the kinetic energy of the center of mass in $S$.