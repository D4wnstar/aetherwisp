---
wiki-publish: true
---
A **rigid body** is a solid body that cannot be deformed. Given any two points on the object, the distance in between them remains the same at all times. The [[Center of mass]] of a rigid body always remains in the same place with respect to the body's points. A rigid body can be either a system of [[particella|particles]] or a continuum of mass.

If the body is a system of particles, we can describe a rigid body as $N$ [[point mass|point masses]] bound by the condition $\lvert \mathbf{r}_{i}-\mathbf{r}_{j} \rvert=\text{const}$, for any $i,j=1,\ldots,N$ representing a point mass.
### Analytical mechanics
We can treat a rigid body in a more formal, accurate manner through analytical mechanics. Firstly, the condition that the distance between points cannot change is a [[constraint]]. Secondly, a rigid body has exactly six [[degrees of freedom]]: three translational and three rotational. The former describe the *position* of (a point of) the body with respect to the [[frame of reference]] in use, whereas the latter describe the *orientation* of the body, defined as the difference between a Cartesian triad attached to the object (a [[moving frame]]) and the reference triad.

The change in position is pretty straight-forward. The change of orientation is a little more complicated. In an infinitesimal time $\delta t$, the moving triad $\{ \mathbf{e}_{1},\mathbf{e}_{2},\mathbf{e}_{3} \}$ is subject to an infinitesimal [[rotation]] $\Omega$. For any given vector $\mathbf{u}$ moving alongside the body, its variation in time due to the rotation is
$$\delta \mathbf{u}=\Omega \mathbf{u}\delta t$$
Since $\Omega$ is an [[Matrice simmetrica|antisymmetric matrix]], this operation is equivalent to claiming that there exists some vector $\boldsymbol{\omega}$ such that $\delta \mathbf{u}=\boldsymbol{\omega}\times \mathbf{u}\ \delta t$. By """dividing""" through with $\delta t$, we can find the time derivative of $\mathbf{u}$:
$$\dot{\mathbf{u}}=\boldsymbol{\omega}\times \mathbf{u}$$
The vector $\boldsymbol{\omega}$ is, of course, interpreted as the angular velocity of rotation. Since $\mathbf{u}$ is any vector attached to the object, the [[basis]] $\{ \mathbf{e}_{1},\mathbf{e}_{2},\mathbf{e}_{3} \}$ also changes according to this equation
$$\dot{\mathbf{e}}_{i}=\boldsymbol{\omega}\times \mathbf{e}_{i},\quad i=1,2,3$$
In fact, if we know the changes in unit vectors, we can even invert this relation to find $\boldsymbol{\omega}$:
$$\boldsymbol{\omega}=\frac{1}{2}\sum_{i=1}^{3} \mathbf{e}_{i}\times \dot{\mathbf{e}}_{i}$$
Knowing $\boldsymbol{\omega}$, we can move on to the [[angular momentum]] of the body:
$$\mathbf{L}_{0}=\sum_{i=1}^{N}m_{i}\mathbf{r}_{i}\times \mathbf{v}_{i}=\sum_{i=1}^{N} m_{i}\mathbf{r}_{i}\times(\boldsymbol{\omega}\times \mathbf{r}_{i})\equiv \mathcal{I}\boldsymbol{\omega} $$
where the $0$ on $\mathbf{L}_{0}$ denotes that the angular momentum is for a point attached to the object, $\mathbf{v}=\dot{\mathbf{r}}=\boldsymbol{\omega}\times \mathbf{r}$. The last value $\mathcal{I}$ is something we just defined: we call it the **[[Moment of inertia|inertia tensor]]** and it acts as a sort of "rotational mass". In fact, just like the [[linear momentum]] is [[mass]] times linear velocity, the angular momentum is "rotational mass" (i.e. inertia tensor) times angular velocity: $\mathbf{p}=m\mathbf{v}\to \mathbf{L}=\mathcal{I}\boldsymbol{\omega}$. Note however, that $\mathcal{I}$ is not a [[scalar]], it is a [[tensor]], a three-dimensional second-order one to be specific. In other words, it is a $3\times 3$ [[matrix]], with *nine* components, split across the axes.

We can use this knowledge to describe rotational motion. If the axis of rotation is constant, say $\mathbf{e}_{3}=\mathbf{e}_{z}$, our angular velocity becomes
$$\boldsymbol{\omega}=\frac{1}{2}(\mathbf{e}_{1}\times \dot{\mathbf{e}}_{1}+\mathbf{e}_{2}\times \dot{\mathbf{e}}_{2})$$
since $\dot{\mathbf{e}}_{3}=0$. The basis vectors are
$$\mathbf{e}_{1}=\begin{pmatrix}
\cos \theta  \\
\sin \theta
\end{pmatrix},\qquad \mathbf{e}_{2}=\begin{pmatrix}
-\sin \theta \\
\cos \theta
\end{pmatrix}$$
with derivatives
$$\dot{\mathbf{e}}_{1}=\dot{\theta}\begin{pmatrix}
-\sin \theta \\
\cos \theta
\end{pmatrix}=\dot{\theta}\mathbf{e}_{2},\qquad \dot{\mathbf{e}}_{2}=-\dot{\theta}\begin{pmatrix}
\cos \theta \\
\sin \theta
\end{pmatrix}=-\dot{\theta}\mathbf{e}_{1}$$
Hence
$$\boldsymbol{\omega}=\frac{1}{2}\dot{\theta}(\mathbf{e}_{1}\times \mathbf{e}_{2}-\mathbf{e}_{2}\times \mathbf{e}_{1})=\dot{\theta}\mathbf{e}_{1}\times \mathbf{e}_{2}=\dot{\theta}\mathbf{e}_{3}$$
But $\mathbf{e}_{3}$ is constant, so the direction of the angular velocity does not change (of course). With this, we can find the [[kinetic energy]] of rotation:
$$T=\frac{1}{2}\boldsymbol{\omega}\cdot \mathcal{I}\boldsymbol{\omega}=\frac{1}{2}\dot{\theta}^{2}\mathbf{e}_{3}\cdot \mathcal{I}\mathbf{e}_{3}=\frac{1}{2}I_{3}\dot{\theta}^{2}$$
Mix it with a potential energy of choice and you have a [[Lagrangian]] to solve for motion.

(TODO: Finish this, lesson 30/04/2025)