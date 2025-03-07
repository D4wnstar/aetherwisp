The **Foucault pendulum** is a type of pendulum designed to prove the rotation of the Earth. It consists of a mass $m$ attached to a wire of length $L$ of negligible mass. The other end of the wire is attached to some point $\mathcal{O}$, which is assumed to be [[Friction|frictionless]]. The only forces that act on the pendulum are [[Interazione gravitazionale|gravity]] and wire tension.

![[Focault Pendulum Schema.png]]

The Earth is rotating at an angular velocity $\vec{w}$ and the axis of rotation is on the line between the center of the Earth $\mathcal{C}$ and the north pole. The [[base|basis]] in the Earth's [[frame of reference]] is made of $\hat{k}$, going from $\mathcal{O}$ to $\mathcal{C}$, $\hat{j}$, anywhere on the plane $\vec{w}$ resides on, and $\hat{i}$, which is the [[Vector product|cross product]] of the two. For the movement of the weight, which we can assume to be a point mass, we use another frame centered in $\mathcal{O}$ using [[Spherical coordinates]]. This is a [[Moving frame]] due to the rotation of the Earth. The position of the weight is $\vec{r}=L\hat{R}(\theta,\phi)$, where $\theta$ is the angle from $\hat{i}$ in the $\hat{i}\hat{j}$-plane and $\phi$ is the angle from $\hat{k}$. The angular velocity in the Earth frame is
$$\vec{w}=\omega[(\cos\lambda)\hat{j}-(\sin\lambda)\hat{k}]$$
where $\omega$ is the angular speed and $\lambda$ is the latitude measured from the equator.

Now, the movement of the Earth is actually rather complicated if you take every little detail into account. Fortunately, most factors have little to no effect on the pendulum, so we can approximate many things. In particular:
- We assume the timescale of the measurements to be small. This allows us to consider the Earth's movement in orbit to be approximately linear and therefore its frame as an inertial frame.
- We assume the angular velocity to be constant.
- We set the number of seconds in a day to be exactly 86,400.
- We set the radius of the Earth to be 6440 kilometers.
- Since the pendulum is on the surface, the term $\vec{w}\times(\vec{w}\times\vec{r})$ is vanishingly small $\sim10^{-5}$, so we set it to zero.

Call the gravitational acceleration $g$. The force of gravity is $\vec{F}=mg\hat{k}$ and the tension in the wire is $\vec{T}=-m\tau\hat{R}$ for some scalar $\tau>0$. The equation of motion for the pendulum therefore is
$$\frac{D^{2}\vec{r}}{Dt^{2}}=-2\vec{w}\times \frac{D\vec{r}}{Dt}+g\hat{k}-\tau\hat{R}$$
We know the form of velocity and acceleration in spherical coordinates; we have
$$\frac{D\vec{r}}{Dt}=L[(\dot{\theta}\sin\phi)\hat{P}-\dot{\phi}\hat{Q}]$$
and
$$\frac{D^{2}\vec{r}}{Dt^{2}}=L[(\ddot{\theta}\sin\phi+2\dot{\theta}\dot{\phi}\cos\phi)\hat{P}+(\dot{\theta}^{2}\sin\phi\cos\phi-\ddot{\phi})\hat{Q}+(\dot{\phi}^{2}+\dot{\theta}^{2}\sin^{2}\phi)\hat{R}]$$
We can substitute these in the differential equation above to obtain three equations, one for each unit basis vector $\hat{P}$, $\hat{Q}$ and $\hat{R}$. In order:
$$L(\ddot{\theta}\sin\phi+2\dot{\theta}\dot{\phi}\cos\phi)=\hat{P}\cdot \frac{D^{2}\vec{r}}{Dt^{2}}=\ldots=2L\omega\dot{\phi}(-\cos\lambda\sin\theta\sin\phi+\sin\lambda\cos\phi)$$
Canceling the $L$s we have the first equation of motion
$$\boxed{\ddot{\theta}\sin\phi+2\dot{\theta}\dot{\phi}\cos\phi=2\omega\dot{\phi}(-\cos\lambda\sin\theta\sin\phi+\sin\lambda\cos\phi)}\tag{1}$$
Then:
$$L(\dot{\theta}^{2}\sin\phi\cos\phi-\ddot{\phi})=\hat{Q}\cdot \frac{D^{2}\vec{r}}{Dt^{2}}=\ldots=2L\omega\dot{\theta}\sin\phi(-\cos\lambda\sin\theta\sin\phi+\sin\lambda\cos\phi)+g\sin\phi$$
Again, canceling the $L$s gives us
$$\boxed{\dot{\theta}^{2}\sin\phi\cos\phi-\ddot{\phi}=2\omega\dot{\theta}\sin\phi(-\cos\lambda\sin\theta\sin\phi+\sin\lambda\cos\phi)+ \frac{g}{L}\sin\phi}\tag{2}$$
Finally:
$$-L(\dot{\phi}^{2}+\dot{\theta}^{2}\sin^{2}\phi)=\hat{R}\cdot \frac{D^{2}\vec{r}}{Dt^{2}}=\ldots=2L\vec{w}\cdot[\dot{\phi}\hat{P}+\dot{\theta}\sin\phi\hat{Q}]+g(\hat{k}\cdot\hat{R})-\tau$$
If we extract $\tau$ out of this we get
$$\boxed{\tau=L[\dot{\phi}^{2}+\dot{\theta}^{2}\sin^{2}\phi+2\dot{\phi}(\vec{w}\cdot\hat{P})+2\dot{\theta}\sin\phi(\vec{w}\cdot\hat{Q})]+g(\hat{k}\cdot\hat{R})}\tag{3}$$
This isn't actually an equation for motion: what this tells us is that the scalar in the wire's tension needs to satisfy this equation in order to have static equilibrium. Motion is entirely determined by $(1)$ and $(2)$.