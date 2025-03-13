Consider a [[point mass]] of [[mass]] $m$ present at some point $\mathbf{r}$ in space.

![[Plot Point mass system|50%]]

The position vector $\mathbf{r}$ is composed of three numbers that show the position of the point mass in any [[basis]] of preference. For instance, in [[Cartesian coordinates]], it is
$$\mathbf{r}=\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}$$
but the choice of coordinate is not binding: all of them are equal and one can freely jump from one to another by way of a [[coordinate transformation]]. The motion of the point in space is given by the time dependence of $\mathbf{r}$ on time $t$:
$$\mathbf{r}(t)=\begin{pmatrix}
x(t) \\
y(t) \\
z(t)
\end{pmatrix}$$
which is now a [[curve]] function $\mathbf{r}:\mathbb{R}\to \mathbb{R}^{3}$ that sends $t$ to $\mathbf{r}(t)$.

The coordinate transformation that we would need to convert between coordinates is a function from $\mathbb{R}^{3}$ to $\mathbb{R}^{3}$ that sends $(x,y,z)$ to $(q_{1},q_{2},q_{3})$. Importantly, it  must be invertible, which is like saying that the [[determinant]] of its [[Jacobian]] is nonzero:
$$\det \begin{pmatrix}
\frac{ \partial x }{ \partial q_{1} } & \frac{ \partial x }{ \partial q_{2} } & \frac{ \partial x }{ \partial q_{3} }   \\
\frac{ \partial y }{ \partial q_{1} } & \frac{ \partial y }{ \partial q_{2} } & \frac{ \partial y }{ \partial q_{3} }   \\
\frac{ \partial z }{ \partial q_{1} } & \frac{ \partial z }{ \partial q_{2} } & \frac{ \partial z }{ \partial q_{3} }  
\end{pmatrix}\neq 0$$
For this to be true, the three columns[^1] must be [[Linear independence|linearly independent]]. The columns are given by
$$\frac{ \partial \mathbf{r} }{ \partial q_{1} }, \quad \frac{ \partial \mathbf{r} }{ \partial q_{2} } ,\quad \frac{ \partial \mathbf{r} }{ \partial q_{3} } $$
But three linearly independent vectors always form a basis of $\mathbb{R}^{3}$. Also, recall that derivatives can be geometrically interpreted as the tangent line at any point on the graph of the thing you are taking the derivative of. So, what we have here is a basis made up of tangents to the position vector.

The main benefit of using such an odd basis is that it comes in very handy in so called **constrained systems**, systems that are constrained to move only in a very particular part of space. Next up is showing why this is true.
### Surfaces
A [[surface]] $Q$ can be described in one of two ways.

One way is, given a [[vector field]] $f(x,y,z)$, the surface is the locus of all points where $f(x,y,z)=0$. $f$ must be smooth and such that the [[gradient]] $\nabla f\neq 0$ for all points on the surface.

The other way is using a parameterization of two parameters, which are coordinates on the surface. The coordinates $\mathbf{r}$ in $\mathbb{R}^{3}$ may be given by the $\mathbb{R}^{2}$ coordinates on the surface $(q_{1},q_{2})$ by
$$x=x(q_{1},q_{2}),\quad y=y(q_{1},q_{2}),\quad z=z(q_{1},q_{2})$$
For instance, a [[palla|ball]] of unit radius in $\mathbb{R}^{3}$  is defined with method 1 by $x^{2}+y^{2}+z^{2}=1$. With method 2, since we know the radius, we can use angular dependencies in [[spherical coordinates]] to state:
$$x=x(\theta,\phi)=\cos \theta \sin \phi,\quad y=y(\theta,\phi)=\sin \theta \sin \phi,\quad z=z(\theta,\phi)=\cos \phi$$

We have successfully reduced the dimensions we work with from 3 to 2 by relying on knowledge about the problem at hand. We want to describe how things move on this surface. To do so, we need the tangents to any point so we can express the idea of movement in a given direction. For a start, take some point on the surface, say $P=(q_{1}^{*},q_{2}^{*})$. There are infinite possible tangents passing through this point and as a whole they form a set that we call **[[tangent space]]**, denoted $T_{P}Q$, which is a two-dimensional [[vector space]]. Great, now what? Well, remember that before we found a universal basis made of tangents. Since that applies anywhere in space, the same argument works just as well over this surface, just instead of ending up with three vectors we only need two:
$$\frac{ \partial \mathbf{r} }{ \partial q_{1} } ,\quad \frac{ \partial \mathbf{r} }{ \partial q_{2} } $$
Since these are linearly independent tangents to the surface (specifically, tangents to the $q_{1}$ and $q_{2}$ axes), they make up a perfectly legitimate basis to the tangent space. Any element of $T_{P}Q$, then, is a sum of these two. We call each element of $T_{P}Q$ **virtual displacement**, since it represents an infinitesimal change in location over the surface, and we denote it $\delta \mathbf{r}$. We are allowed to write
$$\delta \mathbf{r}=\sum_{i=1}^{2} \delta q_{i}\frac{ \partial \mathbf{r} }{ \partial q_{i} } ,\quad \delta q_{i}\in \mathbb{R}$$
### Curves
Just like a surface, a [[curve]] $Q$ can be described in two ways.

One is, again given a vector field $f(x,y,z)$, the locus of points where
$$\begin{cases}
f_{1}(x,y,z)=0 \\
f_{2}(x,y,z)=0
\end{cases}$$
We now have two conditions because we need to reduce dimensionality by 2, from 3 to 1.

The other method is again parameterization, this time with only one parameter $q$. A simple example is a circumference of unit radius. Method 1 gives us
$$\begin{cases}
z=0 \\
x^{2}+y^{2}=1
\end{cases}$$
Method 2 instead gives
$$\begin{cases}
x=\cos \theta \\
y=\sin \theta \\
z=0
\end{cases}$$
The same argument about tangent spaces, tangents on a point, etc. works just as well here, except $T_{P}Q$ is now a one dimensional space, so the concept of vector becomes kind of obsolete.
### In general
Why stop at surfaces and curves? In this entire discussion there has never really been a reason to start from 3D space. We just did so because it's the space we live in and the one that's easiest to imagine. But really, any number of dimensions will do and we can constrain our motion to a lesser dimensional space. Say then we are in an $n$-dimensional space. Our position vector is determined by $\mathbf{r}(q_{1},\ldots,q_{n})$. In this context, the number $n$ is called the **number of degrees of freedom** and it represents the number of separate axes we can move on in space[^2]. The binding we introduce defines a lesser dimensional space $Q$ that we call **[[configuration space]]**, which is a subset of $\mathbb{R}^{n}$ that filters only the coordinates which are actually reachable by the system, deleting all the other ones since they are unnecessary. It is really the configuration space that does all the heavy lifting in describing motion in the most efficient way possible. Of course, motion still "really" happens in $\mathbb{R}^{n}$, but *mathematically* we can show the same thing using configuration space. This makes for way easier solutions for systems we already understand intuitively by getting the most out of our *a priori* knowledge. Once we solve motion in configuration space, it's only a matter of converting back to $\mathbb{R}^{n}$ to get the answer.
### Moving
For now we've only talked about describing where a point is in space. It's not moving yet, so let's give it the push it needs. Since it's the most intuitive, we'll go back to $\mathbb{R}^{3}$ from now on, but it all works for $n$ dimension too. The **velocity** of a point mass is a vector in $\mathbb{R}^{3}$. If the point is bound to $Q$, then the velocity is specifically found in $T_{P}Q$. We can therefore interpret $T_{P}Q$ in the following way:
$$T_{P}Q=\{ \text{set of all possible velocities that a point found in }P\text{ and bound to }Q\text{ can have} \}$$

[^1]: Or rows, although columns are easier to work with here.

[^2]: Of course, this is literally just the definition of an $n$-dimensional space and basis. It's just a difference in terminology that's a bit more intuitive for physics as opposed to pure mathematics.
