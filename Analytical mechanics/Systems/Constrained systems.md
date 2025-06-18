---
wiki-publish: true
---
Many mechanical [[Physical system|systems]] are subject to one or more [[Constraint|constraints]] that reduce the degree to which the system is allowed to move. This information is often known in advance of solving the system, such as the length of the rod of a [[simple pendulum]], and can be used to diminish the amount of variables that we need to describe the motion of the system. Most of what's necessary to make use of these constraint comes from differential geometry, which allows us to manipulate the [[Vector space|vector spaces]] of the system to restrict them to only the things that we strictly need.

To start, consider a [[point mass]] of [[mass]] $m$ at some point $\mathbf{r}$ in space.

![[Plot Point mass system|50%]]

The position vector $\mathbf{r}$ is composed of three numbers that show the position of the point mass in any [[basis]] of preference. For instance, in [[Cartesian coordinates]], it is
$$\mathbf{r}=\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}$$
but the choice of coordinate is not binding: all of them are equal and one can freely jump from one to another by way of a [[coordinate transformation]]. We only care about [[generalized coordinates]]. The motion of the point in space is given by the time dependence of $\mathbf{r}$ on time $t$:
$$\mathbf{r}(t)=\begin{pmatrix}
x(t) \\
y(t) \\
z(t)
\end{pmatrix}$$
which is now a [[curve]] function $\mathbf{r}:\mathbb{R}\mapsto \mathbb{R}^{3}$ that sends $t$ to $\mathbf{r}(t)$.

The coordinate transformation that we would need to convert between coordinates is a function from $\mathbb{R}^{3}$ to $\mathbb{R}^{3}$ that sends $(x,y,z)$ to $(q_{1},q_{2},q_{3})$. Importantly, it must be invertible, which is like saying that the [[determinant]] of its [[Jacobian]] must be nonzero:
$$\det \begin{pmatrix}
\frac{ \partial x }{ \partial q_{1} } & \frac{ \partial x }{ \partial q_{2} } & \frac{ \partial x }{ \partial q_{3} }   \\
\frac{ \partial y }{ \partial q_{1} } & \frac{ \partial y }{ \partial q_{2} } & \frac{ \partial y }{ \partial q_{3} }   \\
\frac{ \partial z }{ \partial q_{1} } & \frac{ \partial z }{ \partial q_{2} } & \frac{ \partial z }{ \partial q_{3} }  
\end{pmatrix}\neq 0$$
For this to be true, the three columns[^1] must be [[Linear independence|linearly independent]]. The columns are given by
$$\frac{ \partial \mathbf{r} }{ \partial q_{1} }, \quad \frac{ \partial \mathbf{r} }{ \partial q_{2} } ,\quad \frac{ \partial \mathbf{r} }{ \partial q_{3} } $$
But three linearly independent vectors always form a basis of $\mathbb{R}^{3}$, which makes this a basis. Also, recall that derivatives can be geometrically interpreted as the tangents to the function you are taking the derivative of. So what we have here is a basis made up of tangents to the position vector.

The main benefit of using such an odd basis is that it comes in very handy in so called **constrained systems**, systems that are constrained to move only in a very particular part of space. Let's see why this is true.
### Surfaces
A [[surface]] $Q$ can be described in one of two ways.
1. One way is, given a [[vector field]] $f(x,y,z)$, the surface is the locus of all points where $f(x,y,z)=0$. $f$ must be smooth and such that the [[gradient]] $\nabla f\neq 0$ for all points on the surface.
2. The other way is using a parameterization of two parameters, which are coordinates on the surface. The coordinates $\mathbf{r}$ in $\mathbb{R}^{3}$ may be given by the $\mathbb{R}^{2}$ coordinates on the surface $(q_{1},q_{2})$ by
$$x\equiv x(q_{1},q_{2}),\quad y\equiv y(q_{1},q_{2}),\quad z\equiv z(q_{1},q_{2})$$

For instance, a [[palla|ball]] of unit radius in $\mathbb{R}^{3}$  is defined with method 1 by $x^{2}+y^{2}+z^{2}-1=0$. With method 2, since we know the radius, we can use angular part of [[spherical coordinates]] to state:
$$x\equiv x(\theta,\phi)=\cos \theta \sin \phi,\quad y\equiv y(\theta,\phi)=\sin \theta \sin \phi,\quad z\equiv z(\theta,\phi)=\cos \phi$$

We have successfully reduced the dimensions we work with from 3 to 2 by relying on knowledge about the problem at hand. We want to describe how things move on this surface. To do so, we need the tangents to any point so we can express the idea of movement in a given direction. For a start, take some point on the surface, say $P=(q_{1}^{*},q_{2}^{*})$. There are infinite possible tangents passing through this point and as a whole they form a set that we call **[[tangent space]]**, denoted $T_{P}Q$, which is a two-dimensional [[vector space]]. Great, now what? Well, remember that before we found a universal basis made of tangents. Since that applies anywhere in space, the same argument works just as well over this surface, just instead of ending up with three vectors we only need two:
$$\frac{ \partial \mathbf{r} }{ \partial q_{1} } ,\quad \frac{ \partial \mathbf{r} }{ \partial q_{2} } $$
Since these are linearly independent tangents to the surface (specifically, tangents to the $q_{1}$ and $q_{2}$ axes), they make up a perfectly legitimate basis to the tangent space. Any element of $T_{P}Q$, then, is a sum of these two. We call each element of $T_{P}Q$ **[[virtual displacement]]**, since it represents an infinitesimal change in location over the surface, and we denote it $\delta \mathbf{r}$. We are allowed to write
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
Why stop at surfaces and curves? In this entire discussion there has never really been a reason to start from 3D space. We just did so because it's the space we live in and the one that's easiest to imagine. But really, any number of dimensions will do and we can constrain our motion to a lesser dimensional space. Say then we are in an $n$-dimensional space where usual geometry holds at least locally: a [[differentiable manifold]]. Our position vector is determined by $\mathbf{r}(q_{1},\ldots,q_{n})$. In this context, the number $n$ is called the number of **[[degrees of freedom]]** and it represents the number of separate axes we can move on in space[^2]. The binding we introduce defines a lesser dimensional space $Q$ that we call **[[configuration space]]**, which is a subset of $\mathbb{R}^{n}$ that filters only the coordinates which are actually reachable by the system, deleting all the other ones since they are unnecessary. It is really the configuration space that does all the heavy lifting in describing motion in the most efficient way possible. Of course, motion still "really" happens in $\mathbb{R}^{n}$, but *mathematically* we can show the same thing using configuration space. This makes for easier solutions for systems we already understand intuitively by getting the most out of our *a priori* knowledge. Once we solve motion in configuration space, it's only a matter of converting back to $\mathbb{R}^{n}$ to get the answer.
### Moving
For now we've only talked about describing where a point is in space. It's not moving yet, so let's give it the push it needs. Since it's the most intuitive, we'll go back to $\mathbb{R}^{3}$ from now on, but it all works for $n$ dimension too. The **velocity** of a point mass is a vector in $\mathbb{R}^{3}$. If the point is bound to $Q$, then the velocity is specifically found in $T_{P}Q$. We can therefore interpret $T_{P}Q$ in the following way:
$$T_{P}Q=\{ \text{set of all possible velocities that a mass found in }P\text{ and bound to }Q\text{ can have} \}$$
### Multiple particles
Everything we've said up until now is in reference to a single point mass. What if we have $N$ of them, all constrained? Let's start with a definition: a constraint is said to be **holonomic** if it can be expressed as a function of generalized coordinates and potentially time that is set to zero: $f(q_{1},\ldots,q_{N},t)=0$. A system of $N$ point masses is said to be holonomic if all its $r$ constraints are holonomic $(0< r< N)$. In this case, the $r$ equations to satisfy are $f^{(r)}(q_{1},\ldots,q_{N},t)=0$.

The coordinates of the points are $\mathbf{r}_{1},\ldots,\mathbf{r}_{N}$, for a total of $3N$ unconstrained degrees of freedom (we're assuming the particles are in $\mathbb{R}^{3}$ here, i.e. the "real world"). Given $r$ constraints, the constrained degrees of freedom are $n=3N-r$. Our system is then solved by only $n$ equations, not $3N$. Our goal is to find a parameterization (i.e. a coordinate transformation) such that we can solve the $n$ constrained equations and then convert them to the full $3N$ unconstrained coordinates.

> [!example] Circular constraint
> We'll start with a simple example with just two point masses, $P_{1}$ and $P_{2}$. $P_{1}$ is constrained to a circumference of radius $R$ on the $xy$ plane and $P_{2}$ is constrained to $P_{1}$ by a rigid rod of length $L$ so that when $P_{1}$ moves, $P_{2}$ gets dragged along with it. The rod is attached to $P_{1}$ in such a way that's free to swivel, so while the length of the rod is constant, its direction is not.
> ![[Plot Two bound point masses]]
> We have six coordinates here to solve, $(x_{1},y_{1},z_{1},x_{2},y_{2},z_{2})$. So what are our constraints? Well, we know $P_{1}$ is stuck on the $xy$ plane, so $f^{(1)}:z_{1}=0$ and $f^{(2)}:x_{1}^{2}+y_{1}^{2}-R^{2}=0$ everywhere. Similarly, since $P_{1}$ and $P_{2}$ are joint, their coordinates are bound by $f^{(3)}:(x_{1}-x_{2})^{2}+(y_{1}-y_{2})^{2}+(z_{1}-z_{2})^{2}-L^{2}=0$. We have three (holonomic) constraints then, which means that we only need to solve for $n=3N-r=6-3=3$ free coordinates.
> 
> We can check if the constraints are really independent from each other by looking for the gradients of the constraints:
> $$\nabla f^{(1)}=\begin{pmatrix}
> 2x_{1} \\
> 2y_{1} \\
> 0 \\
> 0 \\
> 0 \\
> 0
> \end{pmatrix}\qquad \nabla f^{(2)}=\begin{pmatrix}
> 0 \\
> 0 \\
> 1 \\
> 0 \\
 0 \\
> 0
> \end{pmatrix}\qquad \nabla f^{(3)}=\begin{pmatrix}
> 2(x_{1}-x_{2}) \\
> 2(y_{1}-y_{2}) \\
> 2(z_{1}-z_{2}) \\
> 2(x_{2}-x_{1}) \\
> 2(y_{2}-y_{1}) \\
> 2(z_{2}-z_{1})
> \end{pmatrix}$$
> These are [[Linear independence|linearly independent]], which confirms that these are three distinct constraints. Now that we know for fact that we only need $n=3$ free coordinates, we attempt to look for a valid parameterization. The logic here is that we only need to know the angle of $P_{1}$ on its circumference to know where it is (the radius is constant so angle is sufficient), and then we can use the remaining two to locate $P_{2}$. $P_{2}$ is shifted from $P_{1}$ and since we are in three dimensions, we need three coordinates to determine this shift. Luckily we already know one, $L$, and the conveniently have two free coordinates that we can assign the other two. What we make these coordinates represent is a bit arbitrary so long it works, but since we're already using angles for $P_{1}$, we may as well use angles for $P_{2}$. In fact, since the length of the rod is constant, $P_{2}$ always lies on a sphere of radius $L$ centered on $P_{1}$. We can therefore use the angular part of [[spherical coordinates]] to uniquely identify the location of $P_{2}$, if we know $P_{1}$. We now have our three coordinates $q_{1},q_{2},q_{3}$, which are shown in the figure below:
> ![[Plot Two bound point masses 2]]
> Armed with this knowledge, we want to convert this geometric reasoning into formulas. Fortunately, it's just a matter of using [[polar coordinates]] for $P_{1}$ and summing spherical coordinates on top of them for $P_{2}$:
> $$\begin{align}
> x_{1}&=R\cos q_{1} \\
> y_{1}&=R\sin q_{1} \\
> z_{1}&=0 \\
> x_{2}&=R\cos q_{1}+L\sin q_{2}\cos q_{3} \\
> y_{2}&=R\sin q_{1}+L\sin q_{2}\sin q_{3} \\
> z_{2}&=l\cos q_{2}
> \end{align}$$
> That's it. We reduced a six variable problem into a three variable one by using three separate constraints. We have developed a coordinate transformation from $(q_{1},q_{2},q_{3})$ to $(x_{1},y_{1},z_{1},x_{2},y_{2},z_{2})$. Now it's "just" a matter of solving motion for $q_{1},q_{2},q_{3}$ and the plug in the transformation. That's not to say that it's necessarily *easy*, but it's certainly *easier*.
> 
> One last thing we can do is figure out the velocity, although for $\mathbf{w}=(q_{1},q_{2},q_{3})$. Mind you, this velocity is not in "real space", it is in configuration space. The components are the partial derivatives in each coordinate:
> $$\frac{ \partial \mathbf{w} }{ \partial q_{1} } =\begin{pmatrix}
> -R\sin q_{1} \\
> R\cos q_{1} \\
> 0 \\
> -R\sin q_{1} \\
> R\cos q_{1} \\
> 0
> \end{pmatrix}\qquad \frac{ \partial \mathbf{w} }{ \partial q_{2} } =\begin{pmatrix}
> 0 \\
> 0 \\
> 0 \\
> L\cos q_{2}\cos q_{3} \\
> L\cos q_{2}\sin q_{3} \\
> -L\sin q_{2}
> \end{pmatrix}\qquad \frac{ \partial \mathbf{w} }{ \partial q_{3} } =\begin{pmatrix}
> 0 \\
> 0 \\
> 0 \\
> -L\sin q_{2}\sin q_{3} \\
> L\sin q_{2}\cos q_{3} \\
> 0
> \end{pmatrix}$$
> 
> The trajectories of $P_{1}$ and $P_{2}$ now are fully determined as functions of the constrained coordinates: $\mathbf{r}_{1}(q_{1}(t),q_{2}(t),q_{3}(t))$ and $\mathbf{r}_{2}(q_{1}(t),q_{2}(t),q_{3}(t))$. The real velocities are then the time [[Differential|total derivatives]] of these: $\mathbf{v}_{1}(t)=\dot{\mathbf{r}}_{1}(t)=\frac{d}{dt}\mathbf{r}_{1}(q_{1}(t),q_{2}(t),q_{3}(t))$ and $\mathbf{v}_{2}(t)=\dot{\mathbf{r}}_{2}(t)=\frac{d}{dt}\mathbf{r}_{2}(q_{1}(t),q_{2}(t),q_{3}(t))$. The [[stato|state]] of the system is fully determined by $\mathbf{r}_{1}$, $\mathbf{r}_{2}$, $\mathbf{v}_{1}$ and $\mathbf{v}_{2}$.


[^1]: Or rows, although columns are much more meaningful here.

[^2]: Of course, this is literally just the definition of an $n$-dimensional vector space and basis. The difference is a bit more refined, in that differentiable manifolds behave like vector spaces only *locally*, not *globally*.
