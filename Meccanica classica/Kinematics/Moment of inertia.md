The **moment of inertia** $I$ is a quantity that determines how difficult it is to accelerate or decelerate a body in a [[Rotation|rotational]] motion. It is the rotational analog of mass. For a system of $N$ [[Particella|particles]] of mass $m_{i}$ rotating around the origin at a distance $r_{i}$, it is
$$I=\sum\limits_{i=1}^{N}m_{i}r_{i}^{2}$$
and for a continuum of mass
$$I=\int_{M}r^{2}dm$$
where $r$ in this case is the distance from the infinitesimal mass element $dm$ and $M$ is the distribution of mass. It can also be expressed in terms of mass density in various dimensions:
$$I=\int_{L}r^{2}\lambda(x)\ dx, \quad I=\iint_{S}||\vec{r}||^{2}\sigma(x,y)\ dxdy, \quad I=\iiint_{V}||\vec{r}||^{2}\rho(x,y,z)\ dxdydz$$
where $L$, $S$ and $V$ represent a length of wire, a surface and a volume.

The moment of inertia around the [[center of mass]] $\vec{r}_{C}$ is
$$I_{C}=\sum\limits_{i=1}^{N}m_{i}||\vec{r}_{i}-\vec{r}_{C}||^{2}; \quad I_{C}=\int_{M}||\vec{r}-\vec{r}_{C}||^{2}\ dm$$
### Huygens-Steiner theorem
The **Huygens-Steiner theorem** states that any moment of inertia around a given axis can be expressed as the sum of two parts:
1. the moment of inertia around the center of mass
2. the product of the total mass $M$ and the square of the distance $d$ between the center of mass and the axis of rotation

In symbols, this means
$$I=I_{C}+Md^{2}$$
This is valid for every possible axis of rotation. In case the axis passes through the origin, this can be conveniently reversed to indirectly find the moment of inertia around the center of mass $\vec{r}_{C}$:
$$I_{C}=I_{0}-M||\vec{r}_{C}||^{2}$$
where $I_{0}$ is the moment of inertia about the origin.
### Products of inertia and the inertia tensor
A **product of inertia** is quantity similar to a moment of inertia, but split between different axis. Given two axes $x$ and $y$, the product of inertia for a point mass that is distant $r_{x}$ and $r_{y}$ from these axes is
$$I_{xy}=mr_{x}r_{y}$$
as opposed to the moments of inertia about $x$ and $y$, which would be
$$I_{xx}=mr_{x}^{2}, \quad I_{yy}=mr_{y}^{2}$$
which shows that the moment of inertia is really just a special case of the product of inertia. The products are calculated using sums and integrals for extended systems in the same way as the moments.

It is possible to collect all of these in a [[Matrice simmetrica|symmetric matrix]] called the **inertia tensor**. In three dimensions, it is
$$J=\begin{pmatrix}I_{xx} & -I_{xy} & -I_{xz} \\ -I_{xy} & I_{yy} & -I_{yz} \\ -I_{xz} & -I_{yz} & I_{zz}\end{pmatrix}$$
This is valuable as it allows for the calculation of the moment of inertia around any arbitrarily oriented axis, not just the [[frame of reference]] axes. In fact, given an axis sitting on a generic direction determined by the unit vector $\hat{d}$, the moment of inertia around that axis is
$$I_{d}=\hat{d}^{T}J\hat{d}$$
It's also trivial to calculate the angular momentum for a particle using it, provided the angular velocity is known:
$$\vec{L}=\vec{r}\times m\vec{v}=m\vec{r}\times(\vec{w}\times\vec{r})=m(||\vec{r}||^{2}\mathbf{I}-\vec{r}\vec{r}^{T})\vec{w}=J\vec{w}$$
(note that $\mathbf{I}$ is the identical matrix here, not the moment of inertia). Here the inertia tensor comes from
$$J=m(||\vec{r}||^{2}\mathbf{I}-\vec{r}\vec{r}^{T})=m\begin{pmatrix}y^{2}+z^{2} & -xy & -xz \\ -xy & x^{2}+z^{2} & -yz \\ -xz & -yz & x^{2}+y^{2}\end{pmatrix}$$
This way of deriving the angular momentum is remarkable because it is a direct rotational equivalent of the linear momentum formula:
$$\begin{align}
\vec{p}&=m\vec{v} \\
\vec{L}&=J\vec{w}
\end{align}$$
The only differences are that the linear velocity becomes angular velocity and the mass becomes the inertia tensor, which for this reason is also sometimes called the **mass matrix**. Similarly, the moment of force is
$$\vec{M}=\vec{r}\times m\vec{a}=m\vec{r}\times(-\sigma^{2}\vec{r}+\vec{\alpha}\times\vec{r})=m\vec{r}\times(\vec{\alpha}\times\vec{r})=m(||\vec{r}||^{2}\mathbf{I}-\vec{r}\vec{r}^{T})\vec{\alpha}=J\vec{\alpha}$$
which is itself a direct rotational equivalent of force:
$$\begin{align}
\vec{F}&=m\vec{a} \\
\vec{M}&=J\vec{\alpha}
\end{align}$$
### Eigenvalues of the inertia tensor
Being a matrix, it's possible to set up an [[Equazione agli autovalori|eigenvalue equation]] for $J$:
$$J\vec{e}=\mu\vec{e}$$
The eigenvalues $\mu$ are known as the **principal moments of inertia** and the eigenvectors $\vec{e}$ are knows as the **principal directions of inertia**. We can [[diagonalizzazione|diagonalize]] the matrix like so:
$$P=R^{T}JR$$
where $P$ is the diagonal representation of $J$. As usual, its columns are the eigenvectors $\vec{e}$. Now, let's consider the moment of force is [[body coordinates]]:
$$\vec{M}=\frac{d\vec{L}}{dt}=\frac{D\vec{L}}{Dt}+\vec{w}\times\vec{L}=\frac{D(J\vec{w})}{Dt}+\vec{w}\times(J\vec{w})=J \frac{D\vec{w}}{Dt}+\vec{w}\times(J\vec{w})=$$
$$=J \frac{d\vec{w}}{dt}+\vec{w}\times(J\vec{w})$$
In the specific case the body axes are equal to the [[base|basis]] in which $J$ is diagonal (i.e. the principal directions of inertia), then we can write
$$\boxed{\vec{M}=P \frac{d\vec{w}}{dt}+\vec{w}\times(P\vec{w})}$$
This is called **Euler's equation of motion** and is functionally equivalent to the second [[Cardinal equations of mechanics|cardinal equation of mechanics]].