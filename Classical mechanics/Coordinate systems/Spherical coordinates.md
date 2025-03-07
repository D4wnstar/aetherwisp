**Spherical coordinates** are three-dimensional set of coordinates where each point in space is determined by the distance $\rho$ from the origin, the angle $\theta$ from a reference direction and the angle $\phi$ from another, perpendicular reference direction, where $\theta\in[0,2\pi[$ and $\phi\in[0,\pi[$.

![[Graph Spherical coordinates|50%|center]]

### Relation to Cartesian coordinates
[[Cartesian coordinates]] can be converted to spherical coordinates by doing
$$x=\rho\cos\theta\sin\phi, \quad y=\rho\sin\theta\sin\phi, \quad z=\rho\cos\phi$$
and viceversa
$$r=\sqrt{ x^{2}+y^{2}+z^{2} },\quad y=\arctan\left( \frac{\sqrt{x^{2}+y^{2} }}{z} \right),\quad z=\arctan\left( \frac{y}{x} \right)$$
To convert an integral from Cartesian to spherical, we find the [[determinant]] of the [[Jacobian]] of the conversion [[diffeomorphism]] $\sigma(x,y,z)=(\rho\cos\theta\sin\phi,\rho\sin\theta\sin\phi,\rho\cos\phi)$, which is $\det J\sigma=r^{2}\sin \phi$. As such
$$\iiint dxdydz=\iiint r^{2}\sin \phi\ drd\theta d\phi$$
### Motion
A unit vector in the unit sphere is $\mathbf{R}=(\cos\theta\sin\phi,\sin\theta\sin\phi,\cos\phi)$. A perpendicular vector is $\mathbf{P}=(-\sin\theta,\cos\theta,0)$. Another perpendicular vector is just obtained by the [[Vector product|cross product]] $\mathbf{Q}=\mathbf{R}\times\mathbf{P}=(-\cos\theta\cos\phi,-\sin\theta\cos\phi,\sin\phi)$, which completes the [[basis]]. The [[Moving frame]] is
$$\{\mathbf{r}(t);\mathbf{R}(t),\mathbf{P}(t),\mathbf{Q}(t)\}$$

The position of a point is
$$\mathbf{r}=\rho\mathbf{R}$$
The velocity is
$$\mathbf{v}=\dot{\mathbf{r}}=(\rho\dot{\theta}\sin\phi)\mathbf{P}+(-\rho\dot{\phi})\mathbf{Q}+\dot{\rho}\mathbf{R}$$
and the acceleration
$$\mathbf{a}=\dot{\mathbf{v}}=[(\rho\ddot{\theta}+2\dot{\rho}\dot{\theta})\sin\phi+2\rho\dot{\theta}\dot{\phi}\cos\phi]\mathbf{P}+[\rho(\dot{\theta}^{2}\sin\phi\cos\phi-\ddot{\phi})-2\dot{\rho}\dot{\phi}]\mathbf{Q}+\ $$
$$+\ [\ddot{\rho}-\rho(\dot{\phi}^{2}+\dot{\theta}^{2}\sin^{2}\phi)
]\mathbf{R}$$
The [[Matrice simmetrica|antisymmetric]] derivative matrix is
$$\begin{pmatrix}\dot{\mathbf{P}} \\ \dot{\mathbf{Q}} \\ \dot{\mathbf{R}}\end{pmatrix}=\begin{pmatrix}0 & \dot{\theta}\cos\phi & -\dot{\theta}\sin\phi \\ -\dot{\theta}\cos\theta & 0 & \dot{\phi} \\ \dot{\theta}\sin\phi & -\dot{\phi} & 0\end{pmatrix}\begin{pmatrix}\mathbf{P} \\ \mathbf{Q} \\ \mathbf{R}\end{pmatrix}$$
