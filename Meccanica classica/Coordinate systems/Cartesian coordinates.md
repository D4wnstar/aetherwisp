**Cartesian coordinates** are a system of coordinates defined by an [[Ortogonalità|orthonormal]] [[base|basis]] where any given point in space is determined by a set of real numbers, called **coordinates**, that represent the distance between the point and a basis vector.
### Motion
#### Planar motion (2D)
Motion of a [[Particella|particle]] in two dimensional Cartesian coordinates can be represented like
$$\mathbf{r}(t)=x(t)\hat{i}+y(t)\hat{j}$$
with $\hat{i}$ and $\hat{j}$ being the basis vectors $(1,0)$ and $(0,1)$. The velocity is
$$\mathbf{v}(t)=\dot{\mathbf{r}}=\dot{x}\hat{i}+\dot{y}\hat{j}$$
and acceleration
$$\mathbf{a}(t)=\dot{v}=\ddot{r}=\ddot{x}\hat{i}+\ddot{y}\hat{j}$$

Given a trajectory [[curva|curve]] $s(t)$, a tangent unit vector an be defined for each point as
$$\mathbf{T}(t)=\frac{\mathbf{v}}{|\mathbf{v}|}=(\cos(\phi(t)), \ \sin(\phi(t)))$$
and also a normal vector by differentiating each component
$$\mathbf{N}(t)=(-\sin(\phi(t)),\ \cos(\phi(t)))$$
Since differentiating the components of a unit vector is equivalent to [[rotation|rotating]] it 90° counterclockwise, the normal vector is $\pi/2$ from the tangent vector, as expected[^1]. The tangent and normal vectors form a Cartesian basis that moves with the particle, with its origin determined by the origin vector $\mathbf{r}(t)$. These three vectors form a [[moving frame]]
$$\{\mathbf{r}(t), \mathbf{T}(t),\mathbf{N}(t)\}$$

![[Graph 2D Cartesian coordinates|center]]

Velocity and acceleration can be expressed in the moving frame as
$$\mathbf{v}=|\mathbf{v}|\mathbf{T}=\dot{s} \mathbf{T}, \quad \mathbf{a}=\dot{\mathbf{v}}=\ddot{s}\mathbf{T}+\dot{s}^{2} \kappa \mathbf{N}$$
where $\kappa$ is the [[curvature]] of the curve at arc length $s$. The first component in the acceleration is called **tangential acceleration** and the second **centripetal acceleration**.

These are valid:
$$\frac{d\mathbf{T}}{ds}=\frac{d\phi}{ds}(-\sin\phi,\cos\phi)=\kappa \mathbf{N}(s), \quad \frac{d\mathbf{N}}{ds}=\frac{d\phi}{ds}(-\cos\phi,-\sin\phi)=-\kappa \mathbf{T}$$
which can be expressed in matrix notation as
$$\begin{pmatrix} \frac{d\mathbf{T}}{ds} \\ \frac{d\mathbf{N}}{ds}\end{pmatrix}=\begin{pmatrix}0 & \kappa \\ -\kappa & 0\end{pmatrix}\begin{pmatrix}\mathbf{T} \\ \mathbf{N}\end{pmatrix}$$
where the curvature matrix is [[Matrice simmetrica|antisymmetric]].
#### Spatial motion (3D)
In three dimension, the position vector becomes
$$\mathbf{r}(t)=x(t)\hat{i}+y(t)\hat{j}+z(t)\hat{k}$$
with $\hat{i}=(1,0,0)$, $\hat{j}=(0,1,0)$ and $\hat{k}=(0,0,1)$ as the basis vectors. The velocity then is
$$\mathbf{v}(t)=\dot{\mathbf{r}}=\dot{x}\hat{i}+\dot{y}\hat{j}+z\hat{k}$$
and acceleration
$$\mathbf{a}(t)=\dot{v}=\ddot{r}=\ddot{x}\hat{i}+\ddot{y}\hat{j}+\ddot{z}\hat{k}$$

Given a trajectory curve $s(t)$, the tangent vector can be defined as
$$\mathbf{T}(t)=\frac{\mathbf{v}}{|\mathbf{v}|}$$
In three dimensions, there are infinitely possible normal vectors to $\mathbf{T}$, which are all the unit vector on the plane perpendicular to $\mathbf{T}$. Conventionally, the normal vector is chosen by seeing that $d\mathbf{T}/ds$ is perpendicular to $\mathbf{T}$ (by virtue of being a unit vector) and the normal vector is just, given the curvature $\kappa(s)$,[^2]
$$\frac{d\mathbf{T}}{ds}=\kappa(s)\mathbf{N}(s)$$
The curvature can also be computed as
$$\kappa=\sigma \frac{|\mathbf{v}\times\mathbf{a}|}{|\mathbf{v}|^{3}}$$
where $\sigma=\pm1$ is a sign parameter designed to keep the normal vector continuous. Thus, we can write
$$\mathbf{N}=\frac{\sigma(\mathbf{v}\times\mathbf{a})\times\mathbf{v}}{|\mathbf{v}\times\mathbf{a}||\mathbf{v}|}$$
The third and final basis vector can be taken as the [[prodotto vettoriale|cross product]] of tangent and normal like
$$\mathbf{B}=\mathbf{T}\times\mathbf{N}$$
called the **binormal vector**. These three, plus the position vector, make a moving frame:
$$\{\mathbf{r}(t);\mathbf{T}(t),\mathbf{N}(t),\mathbf{B}(t)\}$$

As $\mathbf{B}$ is perpendicular to both $\mathbf{T}$ and $\mathbf{N}$, we can write
$$0=\frac{d\mathbf{B}}{ds}\cdot\mathbf{T}+\mathbf{B}\cdot \frac{d\mathbf{T}}{ds}=\frac{d\mathbf{B}}{ds}\cdot\mathbf{T}+\kappa \mathbf{B}\cdot \mathbf{N}=\frac{d\mathbf{B}}{ds}\cdot\mathbf{T}$$
Differentiating by $s$ and diving by 2 we obtain
$$0=\mathbf{B}\cdot \frac{d\mathbf{B}}{ds}$$
which, when combined with the last equation, tells us that the derivative of $\mathbf{B}$ is perpendicular to both $\mathbf{B}$ and $\mathbf{T}$. It must therefore be parallel to $\mathbf{N}$, so
$$\frac{d\mathbf{B}}{ds}=-\tau\mathbf{N}$$
where $\tau$ is the [[torsion]] of the curve. The minus sign is conventional. We can also compute
$$\frac{d\mathbf{N}}{ds}=\mathbf{B}\times \frac{d\mathbf{T}}{ds}+ \frac{d\mathbf{B}}{ds}\times \mathbf{T}=\kappa\mathbf{B}\times\mathbf{N}-\tau\mathbf{N}\times\mathbf{T}=-\kappa\mathbf{T}+\tau\mathbf{B}$$
The three derivatives can be put into a matrix:
$$\begin{pmatrix}\dot{\mathbf{T}} \\ \dot{\mathbf{N}} \\ \dot{\mathbf{B}}\end{pmatrix}=\begin{pmatrix}0 & \kappa & 0 \\ -\kappa & 0 & \tau \\ 0 & -\tau & 0\end{pmatrix}\begin{pmatrix}\mathbf{T}(s) \\ \mathbf{N}(s) \\ \mathbf{B}(s)\end{pmatrix}$$
which is also [[Matrice simmetrica|antisymmetric]].

[^1]: A rotation by $-\pi/2$ is completely equivalent and would end up with a clockwise-rotation system. A $\pi/2$ rotation gives a counterclockwise-rotating system. It's convention to use the counterclockwise form.
[^2]: Like in the 2D case, there are actually two possibilities, $\mathbf{N}$ and $-\mathbf{N}$. If the curve is planar, we can just pick the counterclockwise direction again. If it's nonplanar, this reasoning cannot apply and the choice should be made to keep $\mathbf{N}$ continuous (if possible).