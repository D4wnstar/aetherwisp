**Cylindrical coordinates** are a three-dimensional set of coordinates where each point in space is determined by an angle $\theta$ from a reference direction on a reference plane, the distance $r$ from the plane's normal vector and the distance $z$ from the plane itself (the "height"), where $\theta\in[0,2\pi[$.

![[Graph Cylindrical coordinates|80%|center]]


### Relation to Cartesian coordinates
Cylindrical coordinates $(r,\theta,z)$ can be converted to [[Cartesian coordinates]] $(x,y,z)$ by doing
$$x=r\cos\theta, \quad y=r\sin\theta, \quad z=z$$
To convert an integral from Cartesian to cylindrical, we find the [[determinant]] of the [[Jacobian]] of the conversion [[diffeomorphism]] $\sigma(x,y,z)=(r\cos \theta,r \sin \theta,z)$, which is $\det J\sigma=r$. As such
$$\iiint dxdydz=\iiint r\ drd\theta dz$$
### Motion
A unit vector in the $xy$-plane is $\mathbf{R}=(\cos\theta,\sin\theta,0)$. A perpendicular vector is simply $\mathbf{P}=(-\sin\theta,\cos\theta,0)$, a [[Rotation]] by $\pi/2$. The vertical direction $\mathbf{k}=(0,0,1)$ is the last vector in the [[basis]], which means that the [[Moving frame]] is
$$\{\mathbf{r}(t);\mathbf{R}(t),\mathbf{P}(t),\mathbf{k}\}$$
(note that $\mathbf{k}$ is constant).

The position of a point is
$$\mathbf{r}=r\mathbf{R}+z\mathbf{k}$$
The velocity is
$$\mathbf{v}=\dot{\mathbf{r}}=\dot{r}\mathbf{R}+r\dot{\theta}\mathbf{P}+\dot{z}\mathbf{k}$$
and the acceleration
$$\mathbf{a}=\dot{\mathbf{v}}=(\ddot{r}-r\dot{\theta}^{2})\mathbf{R}+(r\ddot{\theta}+2\dot{r}\dot{\theta})\mathbf{P}+\ddot{z}\mathbf{k}$$
The $\mathbf{R}$ and $\mathbf{P}$ components are identical to those in [[Polar coordinates]]. The [[Matrice simmetrica|antisymmetric]] derivative matrix is
$$\begin{pmatrix}\dot{\mathbf{R}} \\ \dot{\mathbf{P}} \\ \dot{\mathbf{k}}\end{pmatrix}=\begin{pmatrix}0 & \dot{\theta} & 0 \\ -\dot{\theta} & 0 & 0 \\ 0 & 0 & 0\end{pmatrix}\begin{pmatrix}\mathbf{R} \\ \mathbf{P} \\ \mathbf{k}\end{pmatrix}$$
