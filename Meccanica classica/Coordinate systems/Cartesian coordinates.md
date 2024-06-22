---
aliases:
  - moving frame
---
**Cartesian coordinates** are a system of coordinates defined by an [[Ortogonalità|orthonormal]] [[base|basis]] where any given point in space is determined by a set of real numbers, called **coordinates**, that represent the distance between the point and a basis vector.
### Motion
#### Planar motion
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
Since differentiating the components of a unit vector is equivalent to rotating it 90° counterclockwise, the normal vector is $\pi/2$ from the tangent vector, as expected. The tangent and normal vectors form a Cartesian basis that moves with the particle, with its origin determined by the origin vector $\mathbf{r}(t)$. These three vectors form a **moving frame**
$$\{\mathbf{r}(t), \mathbf{T}(t),\mathbf{N}(t)\}$$

Velocity and acceleration can be expressed in the moving frame as
$$\mathbf{v}=|\mathbf{v}|\mathbf{T}=\dot{s} \mathbf{T}, \quad \mathbf{a}=\dot{\mathbf{v}}=\ddot{s}\mathbf{T}+\dot{s}^{2} \kappa \mathbf{N}$$
where $\kappa$ is the [[curvature]] of the curve at arc length $s$. The first component in the acceleration is called **tangential acceleration** and the second **centripetal acceleration**.

These are valid:
$$\frac{d\mathbf{T}}{ds}=\frac{d\phi}{ds}(-\sin\phi,\cos\phi)=\kappa \mathbf{N}(s), \quad \frac{d\mathbf{N}}{ds}=\frac{d\phi}{ds}(-\cos\phi,-\sin\phi)=-\kappa \mathbf{T}$$
which can be expressed in matrix notation as
$$\begin{pmatrix} \frac{d\mathbf{T}}{ds} \\ \frac{d\mathbf{N}}{ds}\end{pmatrix}=\begin{pmatrix}0 & \kappa \\ -\kappa & 0\end{pmatrix}\begin{pmatrix}\mathbf{T} \\ \mathbf{N}\end{pmatrix}$$
where the curvature matrix is [[Matrice simmetrica|antisymmetric]].