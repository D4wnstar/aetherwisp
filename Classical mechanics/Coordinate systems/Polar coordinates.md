**Polar coordinates** are a two-dimensional set of coordinates where each point on the plane is determined by its distance from a reference point called the **pole** and its angle from a reference direction called the **polar axis**. The distance is called the **radial coordinate**, while the angle is called **angular coordinate** or sometimes **azimuth**.
### Relation to Cartesian coordinates
Polar coordinates $(r,\theta)$ can be converted to [[Cartesian coordinates]] $(x,y)$ by using the [[Coordinate transformation]]
$$\varphi:\mathbb{R}^{2}\to \mathbb{R}^{2},\qquad \varphi(r,\theta)=(r\cos \theta,r\sin \theta)=(x,y)$$
### Motion
The distance from the origin is represented as vector $\mathbf{r}$, with a unit vector $\mathbf{R}=\mathbf{r}/|\mathbf{r}|$ representing its axis. As a unit vector, $\mathbf{R}$ can be written like $\mathbf{R}=(\cos\theta,\sin\theta)$. $\mathbf{P}=(-\sin\theta,\cos\theta)$ is perpendicular to $\mathbf{R}$ and is just a [[Rotation]] by $\pi/2$ of it. The two vectors constitute a [[basis]], and with the position vector they form the [[Moving frame]]
$$\{\mathbf{r(t)};\mathbf{R}(t),\mathbf{P}(t)\}$$

![[Graph Polar coordinates|center]]

The derivatives of the frame are, in [[Matrice simmetrica|antisymmetric]] matrix form,
$$\begin{pmatrix}\dot{\mathbf{R}} \\ \dot{\mathbf{P}}\end{pmatrix}=\begin{pmatrix}0 & \dot{\theta} \\ -\dot{\theta} & 0\end{pmatrix}\begin{pmatrix}\mathbf{R} \\ \mathbf{P}\end{pmatrix}$$
The velocity is
$$\mathbf{v}=\dot{\mathbf{r}}=\frac{d}{dt}(r\mathbf{R})=\dot{r}\mathbf{R}+r\dot{\mathbf{R}}=\dot{r}\mathbf{R}+r\dot{\theta}\mathbf{P}$$
and the acceleration is
$$\mathbf{a}=\dot{\mathbf{v}}=\ddot{r}\mathbf{R}+\dot{r}\dot{\mathbf{R}}+ \frac{d}{dt}(r\dot{\theta})\mathbf{P}+r\dot{\theta}\dot{\mathbf{P}}=(\ddot{r}-r\dot{\theta}^{2})\mathbf{R}+(r\ddot{\theta}+2\dot{r}\dot{\theta})\mathbf{P}$$
