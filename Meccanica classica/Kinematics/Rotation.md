A **rotation** is a [[rigid body]] movement that maintains at least one point fixed. It is the circular movement of an object around a central line, known as the **axis of rotation**. A rotation where the axis passes through an object's [[center of mass]] is called a [[spin]] rotation, whereas a rotation around an axis completely outside of the body is called a [[revolution]] (or *orbit*). In this case, the axis is called the **axis of revolution**.
## Matrix representation
Rotations can be represented through square matrices. This is a particularly convenient form in more theoretical math, especially when [[Operatore|operator]] theory can be used. Given a vector $(x,y)$ in a plane, a rotation about the origin by an angle $\theta>0$ is the vector $(x',y')$ given by
$$x'=\cos(\theta)x-\sin(\theta)y, \quad y'=\sin(\theta)x+\cos(\theta)y$$
which can be derived using plain trigonometry. The rotation is counterclockwise. These equations can be written in matrix form as
$$\boxed{\begin{pmatrix}x' \\ y'\end{pmatrix}=\begin{pmatrix}\cos\theta & -\sin\theta \\ \sin\theta & \cos\theta\end{pmatrix}\begin{pmatrix}x \\ y\end{pmatrix}}$$
In three dimensions, the rotation about an axis can be trivially extended as
$$\boxed{\begin{pmatrix}x' \\ y' \\ z'\end{pmatrix}=\begin{pmatrix}\cos\theta & -\sin\theta & 0 \\ \sin\theta & \cos\theta & 0 \\ 0 & 0 & 1\end{pmatrix}\begin{pmatrix}x \\ y \\ z\end{pmatrix}}$$

The 3D rotation matrix columns can be represented in the standard $\mathbb{R}^{3}$ [[base|basis]] $\{\mathbf{i},\mathbf{j},\mathbf{k}\}$:
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

The vector $\mathbf{v}$ that's being rotated is represented in $\{\mathbf{a},\mathbf{b},\mathbf{d}\}$ as linear combination of the basis vectors:
$$\mathbf{v}=(\mathbf{a}\cdot \mathbf{v})\mathbf{a}+(\mathbf{b}\cdot\mathbf{v})\mathbf{b}+(\mathbf{d}\cdot\mathbf{v})\mathbf{d}=\alpha\mathbf{a}+\beta\mathbf{b}+\delta\mathbf{d}\tag{2}$$
A couple of useful vectors are
$$\mathbf{d}\times\mathbf{v}=-\beta\mathbf{a}+\alpha\mathbf{b}, \quad \mathbf{d}\times(\mathbf{d}\times\mathbf{v})=-\alpha\mathbf{a}-\beta\mathbf{b}$$
The first one can be written as a matrix multiplied by a vector
$$\mathbf{d}\times\mathbf{v}=\begin{pmatrix}d_{1} \\ d_{2} \\ d_{3}\end{pmatrix}\times\begin{pmatrix}v_{1} \\ v_{2} \\ v_{3}\end{pmatrix}=\begin{pmatrix}d_{2}v_{3}-d_{3}v_{2} \\ d_{3}v_{1}-d_{1}v_{3} \\ d_{1}v_{2}-d_{2}v_{1}\end{pmatrix}=\begin{pmatrix}0 & -d_{3} & d_{2} \\ d_{3} & 0 & -d_{1} \\ -d_{2} & d_{1} & 0\end{pmatrix}\begin{pmatrix}v_{1} \\ v_{2} \\ v_{3}\end{pmatrix}=D\mathbf{v}\tag{3}$$
The matrix $D$ is [[Matrice simmetrica|antisymmetric]]. We can then also say $\mathbf{d}\times(\mathbf{d}\times\mathbf{v})=D^{2}\mathbf{v}$.

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
## Specific cases
### Circular motion
If the axis $\mathbf{D}$ is fixed and the distance is a constant $r_{0}$, the coordinate system can be chosen to be [[polar coordinates]] or [[cylindrical coordinates]] depending on dimensions. If cylindrical, the plane of rotation should be the plane of reference, with the axis of rotation being the $z$-axis.

A set of [[Ortonormalità|orthonormal]] axes can be chosen with the [[Cartesian coordinates|Cartesian]] tangent-normal [[moving frame]]. Call $\mathbf{\xi}$ and $\mathbf{\eta}$ these two axes, potentially with $\mathbf{D}$ as the third if in 3D. Therefore, the position unit vector of the rotating object is $\mathbf{R}=\mathbf{\xi}\sin\theta+\mathbf{\eta}\sin\theta$. In this system, **angular speed** is $\sigma(t)=\dot{\theta}(t)$, **angular velocity** is $\mathbf{w}(t)=\sigma(t)\mathbf{D}=\dot{\theta}(t)\mathbf{D}$ and **angular acceleration** is $\mathbf{\alpha}(t)=\dot{\sigma}(t)\mathbf{D}=\ddot{\theta}(t)\mathbf{D}$.

The position therefore changes like
$$\boxed{\mathbf{r}(t)=r_{0}\mathbf{R}(t)+h_{0}\mathbf{D}}$$
where $h_{0}$ is the height of the movement above the plane $\mathbf{D}\cdot\mathbf{r}=0$ if in 3D. The velocity therefore is $\mathbf{v}(t)=r_{0}\sigma\mathbf{P}=r_{0}\sigma\mathbf{D}\times\mathbf{R}=\mathbf{w}\times\mathbf{r}$, so
$$\boxed{\mathbf{v}(t)=\mathbf{w}\times\mathbf{r}}$$
so the tangential velocity can be derived from the angular velocity if the position is known. The acceleration then is $\mathbf{a}(t)=-r_{0}\sigma^{2}\mathbf{R}+r_{0}\ddot{\theta}\mathbf{P}=-r_{0}\sigma^{2}\mathbf{R}+r_{0}\dot{\sigma}\mathbf{D}\times\mathbf{R}=-r_{0}\sigma^{2}\mathbf{R}+\alpha\times\mathbf{r}$, so
$$\boxed{\mathbf{a}(t)=-r_{0}\sigma^{2}\mathbf{R}+\alpha\times\mathbf{r}}$$
where $-r_{0}\sigma^{2}\mathbf{R}$ is the **centripetal acceleration** and $\mathbf{\alpha}\times\mathbf{r}$ is the **tangential acceleration**.
### Moving axis
If the axis $\mathbf{D}(t)$ is moving, let's consider the static axis case in a bit more detail before. We can define an antisymmetric matrix for any vector $\mathbf{u}$ as
$$A(\mathbf{u})=\begin{pmatrix}0 & -u_{3} & u_{2} \\ u_{3} & 0 & -u_{1} \\ -u_{2} & u_{1} & 0\end{pmatrix}$$
This matrix has the property $A(\mathbf{u})\mathbf{r}=\mathbf{u}\times\mathbf{r}$ thanks to $(3)$, and thanks to $(4)$ we can say[^1]
$$R(t)=I+A(\mathbf{D})\sin(\theta(t))+A(\mathbf{D})^{2}(1-\cos(\theta(t)))$$
Linear velocity is worked out as
$$\dot{\mathbf{r}}=\mathbf{w}(t)\times \mathbf{r}(t)=A(\mathbf{w}(t))\mathbf{r}(t)$$
If we differentiate $\mathbf{r}$ directly, we get
$$\dot{\mathbf{r}}=\dot{R}(t)r_{0}=\dot{R}(t)R^{T}R\mathbf{r}_{0}=(\dot{R}(t)R^{T})\mathbf{r}(t)\tag{5}$$
Therefore
$$A(\mathbf{w}(t))=(\dot{R}(t)R^{T})$$
or
$$\dot{R}(t)=A(\mathbf{w}(t))R(t)\tag{6}$$
$(5)$ and $(6)$ equations tell us the rate of change for the rotation in terms of the current rotation and angular velocity.

Equipped with these, let's consider an actually moving axis $\mathbf{D}(t)$. Using $(4)$, the rotation matrix corresponding to this vector for angle of rotation $\theta(t)$ is
$$R(t)=I+A(\mathbf{D}(t))\sin(\theta(t))+A(\mathbf{D}(t))^{2}(1-\cos(\theta(t)))\tag{7}$$
which acts like
$$\boxed{\mathbf{r(t)}=R(t)\mathbf{r}_{0}}$$
The linear velocity is given by $(5)$.

For a rotation matrix, $I=RR^{T}$, so taking the time derivative
$$0=\dot{R}R^{T}+R\dot{R}^{T}=\dot{R}R^{T}+(\dot{R}R^{T})^{T} \quad \Rightarrow \quad(\dot{R}R^{T})^{T}=-\dot{R}R^{T}$$
which means $S(t)=\dot{R}(t)R^{T}(t)$ is antisymmetric and because of that we can write $S(t)=A(\mathbf{w}(t))$.

The angular velocity can be calculated using $R(t)$ from $(7)$ and then calculating $\dot{R}R^{T}$. Using $A(\mathbf{D})^{3}=-A(\mathbf{D})$ we can prove
$$\boxed{\mathbf{w}=\dot{\theta}\mathbf{D}+\sin\theta\dot{\mathbf{D}}+(\cos\theta-1)\dot{\mathbf{D}}\times\mathbf{D}}$$
As $\mathbf{D}$ is a unit vector, the triad $\{\mathbf{D},\dot{\mathbf{D}},\dot{\mathbf{D}}\times\mathbf{D}\}$ forms an orthonormal basis. The angular velocity is expressed in this basis.

[^1]: Here $\mathbf{D}$, which is a unit vector, should not be confused with $D$ from $(4)$, which is a matrix. The usage of the same letter is an unfortunate coincidence.