---
wiki-publish: true
---
**Body coordinates** are a set of coordinates that measure the position of a point on a body from the perspective of the body itself, as opposed to the origin used in [[World coordinates]]. Given a point [[Particle|particle]] $\mathcal{P}$, its body coordinates are $\mathcal{B}(t;\mathcal{P})$. The perspective used is here is called the **body observer**, which stands at the **body origin** with its own set of axes called the **body axes**, which are assumed to form a right-handed [[Orthonormality|orthonormal]] set. Assuming the body is in motion, the body axes are a [[Moving frame]].

For a [[Rigid body]], the vector $\mathcal{B}(t;\mathcal{P})$ is time-independent.
### Relation to world coordinates
If $\mathcal{C}$ is what the world observer sees as the body origin at time 0, at time $t$ it sees $\mathcal{X}(t;\mathcal{C})$. The body observer sees no difference, as the coordinates are centered around the body at any given time. The world observer also sees the body axes as orthonormal vectors; let's call these $\mathbf{U}_{i}(t)$ with $i=0,1,2$. These can be stored in a [[Rotation]] block matrix $R(t)=\begin{array}{c|c}(\mathbf{U}_{0}(t) & \mathbf{U}_{1}(t) & \mathbf{U}_{2}(t))\end{array}$.

The (relative) distance between the body origin $\mathcal{C}$ and the point $\mathcal{P}$ is
$$\mathbf{r}(t;\mathcal{C})=\mathcal{X}(t;\mathcal{P})-\mathcal{X}(t;\mathcal{C})=R(t)\mathcal{B}(t;\mathcal{P})$$
therefore we can find the point in the world from the body coordinates as
$$\boxed{\mathcal{X}(t;\mathcal{P})=\mathcal{X}(t;\mathcal{C})+\mathbf{r}(t;\mathcal{P})=\mathcal{X}(t;\mathcal{C})+R(t)\mathcal{B}(t;\mathcal{P})\tag{1}}$$
Note that the rotation acts as a basis change between body and world.

![[Graph Relative distance from body point|80%|center]]

Consider a time-varying vector in the body system $\mathbf{\xi}(t)=R(t)\mathbf{s}(t)$. The body coordinates $\mathbf{s}(t)$ vary with time because $\mathbf{\xi}(t)$ does. The time derivative is
$$\frac{d\mathbf{\xi}}{dt}=R \frac{d\mathbf{s}}{dt}+\dot{R}\mathbf{s}=R \frac{d\mathbf{s}}{dt}+\dot{R}R^{T}\mathbf{\xi}=\frac{D\mathbf{\xi}}{Dt}+\mathbf{w}\times\mathbf{\xi}\tag{2}$$
where $\dot{R}R^{T}$ is the matrix representation of the [[Vector product|cross product]] for the angular velocity, $C(\mathbf{w})$. We also define
$$\frac{D\mathbf{\xi}}{Dt}=R \frac{d\mathbf{s}}{dt}$$
which measure the rate of change of $\mathbf{\xi}$ relative to body coordinates. The usage of $D$ instead of $d$ for the derivative is meant to show the difference in [[frame of reference]]. $d\mathbf{\xi}/dt$ is change for the world observer, $D\mathbf{\xi}/Dt$ is change for the body observer. The difference between the two is the term $\mathbf{w}\times\mathbf{\xi}$, which goes unseen by the body observer as it rotates alongside the object.

The body origin as seen in world coordinates has a velocity of $\mathbf{v}_{ori}=d\mathcal{X}(t;\mathcal{C})/dt$ and an acceleration $\mathbf{a}_{ori}=d^{2}\mathcal{X}(t;\mathcal{C})/dt^{2}$. Differentiating $(1)$ gives us the world velocity for a point $\mathcal{P}$ $\mathbf{v}_{wor}=d\mathcal{X}(t;\mathcal{P})/dt$, which is related to the body coordinates like
$$\mathbf{v}_{wor}=\mathbf{v}_{ori}+R \frac{d\mathcal{B}}{dt}+\dot{R}\mathcal{B}=\mathbf{v}_{ori}+ \frac{D\mathbf{r}}{Dt}+\mathbf{w}\times\mathbf{r}$$
where $\mathbf{w}$ is the angular velocity of the body at time $t$ in world coordinates. For convenience, we can write $D\mathbf{r}/Dt=\mathbf{v}'$. So we have
$$\boxed{\mathbf{v}_{wor}= \mathbf{v}'+\mathbf{v}_{ori}+\mathbf{w}\times\mathbf{r}}$$
The terms are
- $\mathbf{v}'$ is the velocity of $\mathcal{P}$ as seen from the body.
- $\mathbf{v}_{ori}$ is the translational velocity of the body origin as seen from the world.
- $\mathbf{w}\times\mathbf{r}$ is the velocity due to the rotation of the body axes.

The last two terms are sometimes combined in a single term $\mathbf{v}_{drag}$ called **drag velocity**, which gives us
$$\mathbf{v}_{wor}=\mathbf{v}'+\mathbf{v}_{drag}$$

The world acceleration $\mathbf{a}_{wor}$ is obtained by further time derivation:
$$\mathbf{a}_{wor}=\mathbf{a}_{ori}+ \frac{d}{dt}\frac{D\mathbf{r}}{Dt}+ \frac{d}{dt}(\mathbf{w}\times\mathbf{r})$$
$D\mathbf{r}/Dt$ is in body coordinates, so we can apply $(2)$ to its derivative (the middle term):
$$\frac{d}{dt} \frac{D\mathbf{r}}{Dt}=\frac{D}{Dt} \frac{D\mathbf{r}}{Dt}+\mathbf{w}\times \frac{D\mathbf{r}}{Dt}=\frac{D^{2}\mathbf{r}}{Dt^{2}}+\mathbf{w}\times \frac{D\mathbf{r}}{Dt}$$
$\mathbf{w}\times\mathbf{r}$ is also in body coordinates, so we can do the same thing:
$$\frac{d}{dt}(\mathbf{w}\times\mathbf{r})=\frac{D(\mathbf{w}\times\mathbf{r})}{Dt}+\mathbf{w}\times(\mathbf{w}\times\mathbf{r})=\mathbf{w}\times \frac{D\mathbf{r}}{Dt}+ \frac{D\mathbf{w}}{Dt}\times\mathbf{r}+\mathbf{w}\times(\mathbf{w}\times\mathbf{r})$$
Since $\mathbf{w}\times\mathbf{w}=0$, we have $D\mathbf{w}/Dt=d\mathbf{w}/dt$ from $(2)$. Combining all the equations above, writing angular acceleration as $\mathbf{\alpha}=D\mathbf{w}/Dt$ and $D^{2}\mathbf{r}/Dt^{2}=\mathbf{a}'$, we have the expression for world acceleration:
$$\boxed{\mathbf{a}_{wor}=\mathbf{a}'+\mathbf{a}_{ori}+ \mathbf{w}\times(\mathbf{w}\times\mathbf{r})+ \mathbf{\alpha}\times\mathbf{r}+ 2\mathbf{w}\times \mathbf{v}'}$$
where the terms are
- $\mathbf{a}'$ is the acceleration of $\mathcal{P}$ as seen from the body.
- $\mathbf{a}_{ori}$ is the translational acceleration of the body origin.
- $\mathbf{w}\times(\mathbf{w}\times\mathbf{r})$ is the centripetal acceleration due to the rotation of the body axes.
- $\mathbf{\alpha}\times\mathbf{r}$ is the tangential acceleration due to angular acceleration.
- $2\mathbf{w}\times \mathbf{v}'$ is the **Coriolis acceleration**.

The middle three can be combined in a single term $\mathbf{a}_{drag}$ called **drag acceleration**, which gives us
$$\mathbf{a}_{wor}=\mathbf{a}'+\mathbf{a}_{drag}+\mathbf{a}_{Cor}$$
