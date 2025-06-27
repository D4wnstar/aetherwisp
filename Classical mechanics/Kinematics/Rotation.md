---
wiki-publish: true
---
A **rotation** is a circular movement of an object around a central line, known as the **axis of rotation**. A rotation $R(\alpha)$ in $\mathbb{R}^{N}$ is a [[Operatore lineare|linear operator]] parameterized by a real value, typically interpreted as the angle of rotation and denoted $\theta$ or $\alpha$. It is also a [[transformation]].

In the context of a [[rigid body]], it is a movement that maintains at least one point fixed. A rotation where the axis passes through an object's [[center of mass]] is called a *spin* rotation, whereas a rotation around an axis completely outside of the body is called a *revolution* (or *orbit*). In this case, the axis is called the **axis of revolution**.

Rotations form a [[group]] with interesting properties. Since rotations are, geometrically speaking, planar operations, the most fundamental group is the one in $\mathbb{R}^{2}$. Here they form a group known as
$$SO(2)=\{ R\in M_{2}(\mathbb{R})\ | \ RR^{T}=R^{T}R=\hat{\mathbf{1}} \text{ and } \det R=1\}$$
where $M_{2}(\mathbb{R})$ is the [[set]] of all real $2\times 2$ matrices. It is called the (two-dimensional) [[special orthogonal group]][^1]. It can also be written as $SO(2)=\{ R(\alpha)\ |\ \alpha \in[0,2\pi[\  \}$ and is the group of all [[Symmetric matrix|antisymmetric matrices]] in $\mathbb{R}^{2}$. For rotations in $\mathbb{R}^{N}$, they form the group
$$SO(N)=\{ R\in M_{N}(\mathbb{R})\ | \ RR^{T}=R^{T}R=\hat{\mathbf{1}} \text{ and } \det R=1\}$$
### Properties
- They are [[Operatore lineare|linear operators]].
- They are [[Symmetric matrix|antisymmetric]]: $R(\alpha)^{T}R(\alpha)=R(\alpha)R^{T}(\alpha)=\mathrm{I}$, where $\mathrm{I}$ is the [[identity matrix]].
- They have unit [[determinant]]: $\det R(\alpha)=1$.
- Given a vector $\mathbf{v}\in \mathbb{R}^{N}$, the application of a rotation $R(\alpha)$ rotates it by an angle $\alpha$ with respect to its previous orientation.
### Matrix representation
Being linear operators, rotations can be represented through square matrices. This is a particularly convenient form in more theoretical math, especially when [[Operatore|operator]] theory can be used. Given a vector $(x,y)$ in a plane, a rotation about the origin by an angle $\theta>0$ is the vector $(x',y')$ given by
$$x'=\cos(\theta)x-\sin(\theta)y, \quad y'=\sin(\theta)x+\cos(\theta)y$$
which can be derived using plain trigonometry. The rotation is counterclockwise (by convention). These equations can be written in matrix form as
$$\boxed{\begin{pmatrix}x' \\ y'\end{pmatrix}=\begin{pmatrix}\cos\theta & -\sin\theta \\ \sin\theta & \cos\theta\end{pmatrix}\begin{pmatrix}x \\ y\end{pmatrix}}$$
In three dimensions, a rotation about the $z$ axis can be trivially defined as
$$\boxed{\begin{pmatrix}x' \\ y' \\ z'\end{pmatrix}=\begin{pmatrix}\cos\theta & -\sin\theta & 0 \\ \sin\theta & \cos\theta & 0 \\ 0 & 0 & 1\end{pmatrix}\begin{pmatrix}x \\ y \\ z\end{pmatrix}}$$

The 3D rotation matrix columns can be represented in the standard $\mathbb{R}^{3}$ [[basis]] $\{\mathbf{i},\mathbf{j},\mathbf{k}\}$:
$$R_{0}\mathbf{i}=\begin{pmatrix}c \\ s \\ 0\end{pmatrix}=c\mathbf{i}+s\mathbf{j}, \quad R_{0}\mathbf{j}=\begin{pmatrix}-s \\ c \\ 0\end{pmatrix}=-s\mathbf{i}+c\mathbf{j}, \quad R_{0}\mathbf{k}=\begin{pmatrix}0 \\ 0 \\ 1\end{pmatrix}=\mathbf{k}$$
where $c=\cos\theta$ and $s=\sin\theta$. Consider a right-handed orthonormal set $\{\mathbf{a},\mathbf{b},\mathbf{d}\}$. $R_{0}$ is a rotation in this basis. The matrix $R_{1}$ that represents a rotation in the standard basis will transform $\mathbf{a}$, $\mathbf{b}$ and $\mathbf{d}$ with
$$R_{1}\mathbf{a}=c\mathbf{a}+s\mathbf{b}, \quad R_{1}\mathbf{b}=-s\mathbf{a}+c\mathbf{b}, \quad R_{1}\mathbf{d}=\mathbf{d}$$
and in matrix form
$$R_{1}(\begin{array}{c|c}\mathbf{a} & \mathbf{b} & \mathbf{d}\end{array})=(\begin{array}{c|c}c\mathbf{a}+s\mathbf{b} & -s\mathbf{a}+c\mathbf{b} & \mathbf{d}\end{array})=(\begin{array}{c|c}\mathbf{a} & \mathbf{b} & \mathbf{d}\end{array})\begin{pmatrix}c & -s & 0 \\ s & c & 0 \\ 0 & 0 & 1\end{pmatrix}=(\begin{array}{c|c}\mathbf{a} & \mathbf{b} & \mathbf{d}\end{array})R_{0}$$
Calling $P=(\begin{array}{c|c}\mathbf{a} & \mathbf{b} & \mathbf{d}\end{array})$, we can see that the rotation matrices are [[matrice simile|similar]]:
$$R_{1}P=PR_{0} \quad \Rightarrow \quad R_{0}=P^{-1}R_{1}P=P^{T}R_{1}P$$
where $P^{-1}=P^{T}$ comes from antisymmetry. We can also solve for
$$R_{1}=PR_{0}P^{T}$$
which gives us
$$R_{1}=c(\mathbf{a}\mathbf{a}^{T}+\mathbf{b}\mathbf{b}^{T})+s(\mathbf{b}\mathbf{a}^{T}-\mathbf{a}\mathbf{b}^{T})+\mathbf{d}\mathbf{d}^{T}\tag{1}$$
where all the $\mathbf{x}\mathbf{x}^{T}$ are $3\times3$ matrices. This allows us to calculate $R_{1}$, though at the cost of having to define $\mathbf{a}$ and $\mathbf{b}$. Still, there is a more convenient form that can be derived to remove this dependency as, intuitively, a rotation is independent of which vectors on the plane you refer it to.

The vector $\mathbf{v}$ that's being rotated is represented in $\{\mathbf{a},\mathbf{b},\mathbf{d}\}$ as a [[linear combination]] of the basis vectors:
$$\mathbf{v}=(\mathbf{a}\cdot \mathbf{v})\mathbf{a}+(\mathbf{b}\cdot\mathbf{v})\mathbf{b}+(\mathbf{d}\cdot\mathbf{v})\mathbf{d}=\alpha\mathbf{a}+\beta\mathbf{b}+\delta\mathbf{d}\tag{2}$$
A couple of useful vectors are
$$\mathbf{d}\times\mathbf{v}=-\beta\mathbf{a}+\alpha\mathbf{b}, \quad \mathbf{d}\times(\mathbf{d}\times\mathbf{v})=-\alpha\mathbf{a}-\beta\mathbf{b}$$
The first one can be written as a matrix multiplied by a vector
$$\mathbf{d}\times\mathbf{v}=\begin{pmatrix}d_{1} \\ d_{2} \\ d_{3}\end{pmatrix}\times\begin{pmatrix}v_{1} \\ v_{2} \\ v_{3}\end{pmatrix}=\begin{pmatrix}d_{2}v_{3}-d_{3}v_{2} \\ d_{3}v_{1}-d_{1}v_{3} \\ d_{1}v_{2}-d_{2}v_{1}\end{pmatrix}=\begin{pmatrix}0 & -d_{3} & d_{2} \\ d_{3} & 0 & -d_{1} \\ -d_{2} & d_{1} & 0\end{pmatrix}\begin{pmatrix}v_{1} \\ v_{2} \\ v_{3}\end{pmatrix}=D\mathbf{v}\tag{3}$$
The matrix $D$ is [[Symmetric matrix|antisymmetric]]. We can then also say $\mathbf{d}\times(\mathbf{d}\times\mathbf{v})=D^{2}\mathbf{v}$. This is (one of) the matrix representation(s) of the [[Vector product|cross product]].

Using $(2)$ and the unitary matrix $I$ we can find
$$I\mathbf{v}=\mathbf{v}=\ldots=(\mathbf{a}\mathbf{a}^{T}+\mathbf{b}\mathbf{b}^{T}+\mathbf{d}\mathbf{d}^{T})\mathbf{v}$$
which means
$$I=\mathbf{a}\mathbf{a}^{T}+\mathbf{b}\mathbf{b}^{T}+\mathbf{d}\mathbf{d}^{T}$$
Similarly, we have
$$D\mathbf{v}=\mathbf{d}\times\mathbf{v}=\ldots=(\mathbf{b}\mathbf{a}^{T}-\mathbf{a}\mathbf{b}^{T})\mathbf{v}$$
and so
$$D=\mathbf{b}\mathbf{a}^{T}-\mathbf{a}\mathbf{b}^{T}$$
Finally, we have
$$D^{2}\mathbf{v}=\mathbf{d}\times(\mathbf{d}\times\mathbf{v})=\ldots=(\mathbf{d}\mathbf{d}^{T}-I)\mathbf{v}$$
and so
$$D^{2}=\mathbf{d}\mathbf{d}^{T}-I$$
We can combine all these relations to find $R_{1}$ from $(1)$:
$$\boxed{R_{1}=I+\sin\theta D+(1-\cos\theta)D^{2}}\tag{4}$$
In this form, the rotation matrix is independent from the choice of $\mathbf{a}$ and $\mathbf{b}$ when applied to a vector. In fact
$$R_{1}\mathbf{v}=I\mathbf{v}+sD\mathbf{v}+(1-c)D^{2}\mathbf{v}=\mathbf{v}+s\mathbf{d}\times\mathbf{v}+(1-c)\mathbf{d}\times(\mathbf{d}\times\mathbf{v})$$
### Rotation vector spaces
It is possible to take the exponential of a matrix by using the [[serie|series]] definition
$$\exp(x)=\sum_{n=0}^{\infty} \frac{x^{n}}{n!}$$
This has some interesting effects in the context of rotations. Consider the most general antisymmetric $2\times 2$ matrix:
$$\mathrm{A}=\begin{pmatrix}
0 & -\alpha \\
\alpha & 0
\end{pmatrix}=\alpha \begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}=\alpha \mathrm{E}$$
The exponential is
$$\begin{align}
\exp \mathrm{A}&=\mathrm{I}+\sum_{n=1}^{\infty} \frac{\mathrm{A}^{n}}{n!} \\
&=\sum_{n=0}^{\infty} \frac{\mathrm{A}^{2m}}{(2m)!}+\sum_{m=0}^{\infty} \frac{\mathrm{A}^{2m+1}}{(2m+1)!} \\
&=\mathrm{I}\underbrace{ \sum_{m=0}^{\infty} \frac{(-1)^{m}\alpha^{2m}}{(2m)!} }_{ \cos \alpha }+\mathrm{E}\underbrace{ \sum_{m=0}^{\infty} \frac{(-1)^{m}\alpha^{2m+1}}{(2m+1)!} }_{ \sin \alpha }
\end{align}$$
where we used that $\mathrm{A}^{2m}=(-1)^{m}\alpha^{2m}\mathrm{I}$ and $\mathrm{A}^{2m+1}=\mathrm{A}^{2m}\mathrm{A}=(-1)^{m}\alpha^{2m+1}\mathrm{E}$ and the [[sine and cosine series]]. As such, in the most general case, the exponential of an antisymmetric matrix is
$$\exp \mathrm{A}=\cos \alpha \ \mathrm{I}+\sin \alpha\  \mathrm{E}=\begin{pmatrix}
\cos \alpha & -\sin \alpha \\
\sin \alpha & \cos \alpha
\end{pmatrix}=R(\alpha)$$
Evidently, all (finite) rotations are exponentials of the antisymmetric matrix $\mathrm{E}$, weighed by some factor $\alpha$. We can therefore represent them as
$$\boxed{R(\alpha)=e^{\alpha \mathrm{E}}}$$
Since all rotations are exponentials of $\mathrm{E}$, we say that $\mathrm{E}$ is the **generator** of $SO(2)$. In fact, antisymmetric matrices form a [[vector space]] (sum and scalar multiplication are both defined and closed) and $\mathrm{E}$ forms a [[basis]] of this space. Thus, any rotation is also a [[linear combination]] of basis elements. In 2D the basis is just $\{ \mathrm{E} \}$, but in $N$-dimensional spaces this provides an easy extension of the definition of rotation: just add more elements to the basis so that it generates $SO(N)$.

The number of generators, that is elements in the basis, is found to be $N(N-1)/2$. In $N=3$ we have $3$ generators and these are
$$\mathrm{E}_{1}=\begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & -1 \\
0 & 1 & 0
\end{pmatrix},\quad \mathrm{E}_{2}=\begin{pmatrix}
0 & 0 & 1 \\
0 & 0 & 0 \\
-1 & 0 & 0
\end{pmatrix},\quad \mathrm{E}_{3}=\begin{pmatrix}
0 & -1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}$$
A generic infinitesimal rotation $\Omega$ is given by
$$\boxed{\Omega=\sum_{i=1}^{3} \omega_{i}\mathrm{E}_{i}=\begin{pmatrix}
0 & -\omega_{3} & \omega_{2} \\
\omega_{3} & 0 & -\omega_{1} \\
-\omega_{2} & \omega_{1} & 0
\end{pmatrix}}$$
For example, the rotation $R_{3}$ is given by the exponential of $\mathrm{E}_{3}$
$$R_{3}=e^{ \omega_{3}\mathrm{E}_{3} }=\exp\begin{pmatrix}
0 & -\omega_{3} & 0 \\
\omega_{3} & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}=\begin{pmatrix}
\cos \omega_{3} & -\sin \omega_{3} & 0 \\
\sin \omega_{3} & \cos \omega_{3} & 0 \\
0 & 0 & 1
\end{pmatrix}$$
But this is just a 2D rotation around an axis, specifically around the $z$ axis. The same can be found for $R_{1}$ and $R_{2}$ too, which end up being rotations around the $x$ and $y$ axes. Evidently, then, $R_{i}$ is the rotation around the $i$-th axis. A *generic* rotation can then be described as a [[linear combination]] of basis rotations, just like how a vector is a linear combination of basis vectors (again, rotations constitute a vector space).
$$\boxed{R=e^{ \sum_{i=1}^{N}\omega_{i}\mathrm{E}_{i} }=\prod_{i=1}^{N} e^{\omega_{i}\mathrm{E}_{i}}}$$
Intuitively, this makes sense: rotating something on a "diagonal" is like rotating it "horizontally" and then "vertically".

Look for a moment at the $\mathrm{E}$ basis matrices. They all have the same blueprint: antisymmetric, all zeros on the diagonal and exactly a single pair of $1$ and $-1$, with one matrix for every entry outside of the diagonal. For one, this gives proof on why the number of basis elements is what it is: the number of nondiagonal entries in an $N\times N$ matrix is precisely $N(N-1)/2$. But more than that, it gives us a way to formalize how this basis is built, which is through the [[Tensore di Levi-Civita|Levi-Civita tensor]] $\epsilon_{ijk}$. For instance, in 3D each basis matrix $i$ is defined by its elements $(\mathrm{E}_{i})_{jk}=-\epsilon_{ijk}$. A generic rotation basis then is just the application of the Levi-Civita tensor in whatever dimension you need.

Infinitesimal rotations are hence defined in a similar manner. In 3D:
$$\boxed{\Omega_{ij}=-\sum_{k=1}^{3} \epsilon_{ijk}\omega_{k}}$$
This permits a more refined analysis of what infinitesimal rotations even do. The variation of a vector $v$ subject to such a rotation must then be
$$\delta v_{i}=\sum_{j=1}^{3} \Omega_{ij}v_{j}=-\sum_{j,k=1}^{3} \epsilon_{ijk}\omega_{k}v_{j}=\sum_{j,k=1}^{3} \epsilon_{ikj}\omega_{k}v_{j}=(\boldsymbol{\omega}\times \mathbf{v})_{i}$$
using $\epsilon_{ijk}=-\epsilon_{ikj}$ and the tensor definition of the [[vector product#Tensor representation|vector product]]. Putting components together we can say that, in general, $\boldsymbol{\omega}\times \mathbf{v}$ is the variation of $\mathbf{v}$ under an infinitesimal rotation of angle $\lvert \boldsymbol{\omega} \rvert$ around an axis parallel to $\boldsymbol{\omega}$. The [[norm]] of this variation is
$$\lvert \delta \mathbf{v} \rvert =\lvert \boldsymbol{\omega}\times \mathbf{v} \rvert =\lvert \boldsymbol{\omega} \rvert \lvert \mathbf{v} \rvert \sin \theta=\lvert \boldsymbol{\omega} \rvert \lvert \mathbf{v}_{\perp} \rvert $$

To further analyze $\mathrm{E}_{i}$, we can calculate the [[commutator]] between the $\mathrm{E}_{i}$ and $\mathrm{E}_{j}$:
$$[\mathrm{E}_{i},\mathrm{E}_{j}]=\mathrm{E}_{i}\mathrm{E}_{j}-\mathrm{E}_{j}\mathrm{E}_{i}$$
We need to figure out the product between these matrices:
$$(\mathrm{E}_{i}\mathrm{E}_{j})_{mn}=\sum_{k=1}^{3} (\mathrm{E}_{i})_{mk}(\mathrm{E}_{j})_{kn}=\sum_{k=1}^{3} \epsilon_{imk}\epsilon_{ikn}=-\sum_{k=1}^{3} \epsilon_{imk}\epsilon_{jnk}=-(\delta_{ij}\delta_{mn}-\delta_{in}\delta_{mj})$$
using the [[Delta di Dirac|Dirac delta]]. The commutator components then are
$$([\mathrm{E}_{i},\mathrm{E}_{j}])_{mn} = (\mathrm{E}_{i}\mathrm{E}_{j})_{mn} - (\mathrm{E}_{j}\mathrm{E}_{i})_{mn} = -\left(\delta_{ij}\delta_{mn} - \delta_{in}\delta_{mj}\right) + \left(\delta_{ji}\delta_{mn} - \delta_{jn}\delta_{mi}\right)$$
Simplify:
$$
[\mathrm{E}_{i},\mathrm{E}_{j}]_{mn} = \delta_{in}\delta_{mj} - \delta_{jn}\delta_{mi} = \sum_{k=1}^{3} \epsilon_{ijk} (\mathrm{E}_k)_{mn}
$$
You can verify that each component $[\mathrm{E}_i, \mathrm{E}_j]_{mn}$ is actually an entry of $\mathrm{E}_k$ weighted by $\epsilon_{ijk}$. In particular, the commutator simplifies to:
$$\boxed{[\mathrm{E}_{i},\mathrm{E}_{j}] = \sum_{k=1}^{3} \epsilon_{ijk} \mathrm{E}_{k}}$$
This gives a compact formula for the commutator of the generators of rotation. This might seem insignificant, but the fact is that we now have a well-behaved commutator in the vector space of rotations. This means that it's not any old vector space, but specifically it's a [[Lie algebra]]. This provides access to all of the machinery specific to Lie algebras and helps to study the special orthogonal groups such as $SO(3)$.
### Conservation of angular momentum
Rotations have a connection of fundamental importance to the conservation of [[angular momentum]]. We'll use the [[Lagrangian]] formalism for this proof, but this fact is true in general regardless of formalism.

Consider a 3D rotation $R$ around an axis parallel to $\boldsymbol{\omega}$ and write it as the exponential of a linear combination of generators as above:
$$R=\exp\left( \alpha \sum_{i=1}^{3} \hat{\boldsymbol{\omega}}_{i}\mathrm{E}_{i} \right)$$
where $\hat{\boldsymbol{\omega}}=\boldsymbol{\omega}/\lvert \boldsymbol{\omega} \rvert$. We define the [[coordinate transformation]]
$$\varphi(q,\alpha)=e^{\alpha \sum_{i=1}^{3} \hat{\boldsymbol{\omega}}_{i}\mathrm{E}_{i}}\mathbf{q}$$
We can take the derivative of this in $\alpha$ to find
$$\frac{ \partial \varphi }{ \partial \alpha }(q,\alpha)=\left( \sum_{i=1}^{3} \hat{\boldsymbol{\omega}}_{i}\mathrm{E}_{i} \right)e^{\alpha \sum_{i=1}^{3} \hat{\boldsymbol{\omega}}_{i}\mathrm{E}_{i}}\mathbf{q}$$
The sum in parenthesis is an infinitesimal rotation. When evaluated in $\alpha=0$ we get
$$\frac{ \partial \varphi }{ \partial \alpha } (q,0)=\left( \sum_{i=1}^{3} \hat{\boldsymbol{\omega}}_{i}\mathrm{E}_{i} \right)\mathbf{q}$$
Now, assuming the Lagrangian $\mathcal{L}(\mathbf{q}, \dot{\mathbf{q}})$ is [[Transformation invariance|invariant]] under this rotation, we can invoke [[Nöther's theorem]] to guarantee the existence of a [[constant of motion]]:
$$\sum_j \frac{\partial \mathcal{L}}{\partial \dot{q}_j}\frac{\partial \varphi_j}{\partial \alpha} (q, 0)$$
Substituting $\frac{ \partial \varphi }{ \partial \alpha } (q,0)$ gives
$$\sum_{j, k}  \frac{\partial \mathcal{L}}{\partial \dot{q}_j}  \left( \sum_{i=1}^{3} \hat{\boldsymbol{\omega}}_i  (\mathrm{E}_i)_{jk} q_k \right)$$
This can be rearranged as
$$\sum_{i=1}^{3} \hat{\boldsymbol{\omega}}_i  \sum_{j, k}  p_j (\mathrm{E}_i)_{jk} q_k$$
Here, $p_j = \frac{\partial \mathcal{L}}{\partial \dot{q}_j}$ is the [[Conjugate momenta|conjugate momentum]] and $(\mathrm{E}_i)_{jk}$ is the $j, k$-th component of the $i$-th rotation generator.

In vector form, recognize that
$$\sum_{j, k} p_j (\mathrm{E}_i)_{jk} q_k = \mathbf{p}^T \mathrm{E}_i \mathbf{q} = (\mathbf{p} \times \mathbf{q})_i = (\mathbf{L})_i$$
where $\mathbf{L}$ is the angular momentum. The conserved quantity becomes:
$$\sum_{i=1}^{3} \hat{\boldsymbol{\omega}}_i L_i = \hat{\boldsymbol{\omega}} \cdot \mathbf{L} = L_\omega$$
which is the projection of the total angular momentum onto the rotation axis $\hat{\boldsymbol{\omega}}$.

This is an universally important fact: if the Lagrangian (or [[Hamiltonian]] for that matter) is invariant under rotation on an axis, then angular moment is conserved on that axis. This is true *always* as long as rotation invariance persists and in fact, for [[Physical system|isolated systems]], there is no restriction on what the axis is, which means that *all* angular momentum is conserved in such a system. This is one of the several important manifestations of Nöther's theorem.
### Specific cases
#### Circular motion
If the axis $\mathbf{D}$ is fixed and the distance is a constant $r_{0}$, the coordinate system can be chosen to be [[Polar coordinates]] or [[Cylindrical coordinates]] depending on dimensions. If cylindrical, the plane of rotation should be the plane of reference, with the axis of rotation being the $z$-axis.

A set of [[Orthonormality|orthonormal]] axes can be chosen with the [[Cartesian coordinates|Cartesian]] tangent-normal [[Moving frame]]. Call $\mathbf{\xi}$ and $\mathbf{\eta}$ these two axes, potentially with $\mathbf{D}$ as the third if in 3D. Therefore, the position unit vector of the rotating object is $\mathbf{R}=\mathbf{\xi}\sin\theta+\mathbf{\eta}\sin\theta$. In this system, **angular speed** is $\sigma(t)=\dot{\theta}(t)$, **angular velocity** is $\mathbf{w}(t)=\sigma(t)\mathbf{D}=\dot{\theta}(t)\mathbf{D}$ and **angular acceleration** is $\mathbf{\alpha}(t)=\dot{\sigma}(t)\mathbf{D}=\ddot{\theta}(t)\mathbf{D}$.

The position therefore changes like
$$\boxed{\mathbf{r}(t)=r_{0}\mathbf{R}(t)+h_{0}\mathbf{D}}$$
where $h_{0}$ is the height of the movement above the plane $\mathbf{D}\cdot\mathbf{r}=0$ if in 3D. The velocity therefore is $\mathbf{v}(t)=r_{0}\sigma\mathbf{P}=r_{0}\sigma\mathbf{D}\times\mathbf{R}=\mathbf{w}\times\mathbf{r}$, so
$$\boxed{\mathbf{v}(t)=\mathbf{w}\times\mathbf{r}}$$
so the tangential velocity can be derived from the angular velocity if the position is known. The acceleration then is $\mathbf{a}(t)=-r_{0}\sigma^{2}\mathbf{R}+r_{0}\ddot{\theta}\mathbf{P}=-r_{0}\sigma^{2}\mathbf{R}+r_{0}\dot{\sigma}\mathbf{D}\times\mathbf{R}=-r_{0}\sigma^{2}\mathbf{R}+\alpha\times\mathbf{r}$, so
$$\boxed{\mathbf{a}(t)=-r_{0}\sigma^{2}\mathbf{R}+\alpha\times\mathbf{r}}$$
where $-r_{0}\sigma^{2}\mathbf{R}$ is the **centripetal acceleration** and $\mathbf{\alpha}\times\mathbf{r}$ is the **tangential acceleration**.
#### Moving axis
If the axis $\mathbf{D}(t)$ is moving, let's consider the static axis case in a bit more detail before. We can define an antisymmetric matrix for any vector $\mathbf{u}$ as
$$C(\mathbf{u})=\begin{pmatrix}0 & -u_{3} & u_{2} \\ u_{3} & 0 & -u_{1} \\ -u_{2} & u_{1} & 0\end{pmatrix}$$
This is the matrix representation of the [[Vector product|cross product]], $C(\mathbf{u})\mathbf{r}=\mathbf{u}\times\mathbf{r}$ thanks to $(3)$, and thanks to $(4)$ we can say[^2]
$$R(t)=I+C(\mathbf{D})\sin(\theta(t))+C(\mathbf{D})^{2}(1-\cos(\theta(t)))$$
Linear velocity is worked out as
$$\dot{\mathbf{r}}=\mathbf{v}=\mathbf{w}(t)\times \mathbf{r}(t)=C(\mathbf{w}(t))\mathbf{r}(t)$$
If we differentiate $\mathbf{r}$ directly, we get
$$\mathbf{v}=\dot{R}(t)r_{0}=\dot{R}(t)R^{T}R\mathbf{r}_{0}=(\dot{R}(t)R^{T})\mathbf{r}(t)\tag{5}$$
Therefore
$$C(\mathbf{w}(t))=(\dot{R}(t)R^{T})$$
or
$$\dot{R}(t)=C(\mathbf{w}(t))R(t)\tag{6}$$
$(5)$ and $(6)$ equations tell us the rate of change for the rotation in terms of the current rotation and angular velocity.

Equipped with these, let's consider an actually moving axis $\mathbf{D}(t)$. Using $(4)$, the rotation matrix corresponding to this vector for angle of rotation $\theta(t)$ is
$$R(t)=I+C(\mathbf{D}(t))\sin(\theta(t))+C(\mathbf{D}(t))^{2}(1-\cos(\theta(t)))\tag{7}$$
which acts like
$$\boxed{\mathbf{r}(t)=R(t)\mathbf{r}_{0}}$$
The linear velocity is given by $(5)$.

For a rotation matrix, $I=RR^{T}$, so taking the time derivative
$$0=\dot{R}R^{T}+R\dot{R}^{T}=\dot{R}R^{T}+(\dot{R}R^{T})^{T} \quad \Rightarrow \quad(\dot{R}R^{T})^{T}=-\dot{R}R^{T}$$
which means $S(t)=\dot{R}(t)R^{T}(t)$ is antisymmetric and because of that we can write $S(t)=A(\mathbf{w}(t))$.

The angular velocity can be calculated using $R(t)$ from $(7)$ and then calculating $\dot{R}R^{T}$. Using $C(\mathbf{D})^{3}=-C(\mathbf{D})$ we can prove
$$\boxed{\mathbf{w}=\dot{\theta}\mathbf{D}+\sin\theta\dot{\mathbf{D}}+(\cos\theta-1)\dot{\mathbf{D}}\times\mathbf{D}}$$
As $\mathbf{D}$ is a unit vector, the triad $\{\mathbf{D},\dot{\mathbf{D}},\dot{\mathbf{D}}\times\mathbf{D}\}$ forms an orthonormal basis. The angular velocity is expressed in this basis.

[^1]: Technically, $SO(2)$ is a specification for matrices in general, but the only matrices that satisfy these conditions are rotations.
[^2]: Here $\mathbf{D}$, which is a unit vector, should not be confused with $D$ from $(4)$, which is a matrix. The usage of the same letter is an unfortunate coincidence.