An **inclined plane** is, physically speaking, a [[Physical system|system]] composed of a plane tilted at some angle compared to another plane. It is often used as a simple system demonstrating the effects of a normal [[force]] and the application of [[friction]].
### In analytical mechanics
The inclined plane can be analyzed in a more modern manner by using analytical mechanics.

![[Diagram Inclined plane|80%]]

#### Frictionless plane
It is easiest to start by ignoring friction. The surface of the plane is of course our [[constraint]] of reaction $\Phi$. Since the point mass can only move up and down the surface, we really only need one [[Generalized coordinates|generalized coordinate]], $q$, to describe this motion. The [[coordinate transformation]] from $\mathbb{R}^{2}$ to our [[configuration space]] (which is just the line the inclined plane stands on) is then simply given by
$$x=q\cos \theta,\quad y=h-q\sin \theta\tag{1}$$
We can immediately find the derivative of $\mathbf{r}=(x,y)=(q\cos \theta,h-q\sin \theta)$:
$$\frac{ \partial \mathbf{r} }{ \partial q } =(\cos \theta,-\sin \theta)$$
Our gravitational force is just $\mathbf{F}=(0,-mg)$, which sets up the constrained [[Newton's laws|Newton's second law]]:
$$m \ddot{\mathbf{r}}=\mathbf{F}+\Phi$$
We are going to project this equation on the axis of the inclined plane, given by $\partial \mathbf{r}/\partial q$, so that we get two scalar equations that we can solve separately instead of a single vector one. To do so, we just need to take the [[scalar product]] of the above equation with $\partial \mathbf{r}/\partial q$:
$$(\mathbf{F}+\Phi-m \ddot{\mathbf{r}})\cdot \frac{ \partial \mathbf{r} }{ \partial q } =0$$
Before doing any math, we can immediately tell that $\Phi$ vanishes. This is because the frictionless plane is an *ideal* constraint and $\Phi$ is always perpendicular to $\partial \mathbf{r}/\partial q$, so that term is guaranteed to vanish[^1]. This is precisely what allows us to solve the system while completely ignoring the constraint reaction: we just need to find the configuration space and project our equation over that. Now we can proceed with the calculation:
$$(F_{x}-m\ddot{x},F_{y}-m\ddot{y})\begin{pmatrix}
\cos \theta \\
-\sin \theta
\end{pmatrix}=0$$
We need to know what $\ddot{x}$ and $\ddot{y}$. Thankfully, we know what $x$ and $y$ are in terms of $q$ from $(1)$, so we can just do the derivatives:
$$\dot{x}=\dot{q}\cos \theta,\quad \ddot{x}=\ddot{q}\cos \theta,\quad \dot{y}=-\dot{q}\sin \theta,\quad \ddot{y}=-\ddot{q}\sin \theta$$
We also know what $F_{x}$ and $F_{y}$ are, so that's all we need:
$$\begin{align}
(-m \ddot{q}\cos \theta,-mg+m\ddot{q}\sin \theta)\begin{pmatrix}
\cos \theta \\
-\sin \theta
\end{pmatrix}&=-m \ddot{q}\cos ^{2}\theta+mg\sin \theta-m \ddot{q}\sin ^{2}\theta \\
&=mg\sin \theta-m \ddot{q} \\
&=0
\end{align}$$
The equation
$$m(g\sin \theta-\ddot{q})=0$$
is identical to the classical solution using Newtonian mechanics. The system is solved by the gravitational acceleration projected onto the inclined plane minus the acceleration of the object itself. The actual trajectory is given by the solution to the [[Ordinary differential equation|ODE]]
$$\ddot{q}=g\sin \theta$$
which yields
$$\dot{q}(t)=\int \ddot{q}dt=g\sin \theta \int dt=g\sin \theta\ t +v_{0}$$
and
$$q(t)=\int \dot{q}dt=g\sin \theta \int tdt+\int v_{0}dt=\frac{1}{2}g\sin \theta\ t^{2}+v_{0}t+q_{0}$$
$q(t)$ is the motion of the point mass. It contains all of the information on the trajectory of motion under the equation
$$\boxed{q(t)=q_{0}+v_{0}t+ \frac{1}{2}g\sin \theta\ t^{2}}$$
If we want to use it in a different, more realistic coordinate system, we can just substitute $q(t)$ inside of an appropriate coordinate transformation and we're done. For instance, if we want to see motion in the Cartesian $xy$ coordinates, we just put $q(t)$ in $(1)$:
$$\boxed{\begin{align}
x(t)&=q_{0}\cos \theta+v_{0}\cos \theta\ t+ \frac{1}{2}g\sin \theta \cos \theta\ t^{2} \\
y(t)&=h- q_{0}\sin \theta-v_{0}\sin \theta\ t- \frac{1}{2}g\sin ^{2} \theta\ t^{2}
\end{align}}$$
With appropriate boundary conditions $q_{0}$ and $v_{0}$, motion is solved.

[^1]: If we add friction to the system, this is no longer true.
