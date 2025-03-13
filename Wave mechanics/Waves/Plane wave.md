A **plane wave** is a [[wave]] whose [[wavefront]] is a plane everywhere. It is the most basic kind of wave and any wave can be seen as being locally plane at small enough scales.
### Conditions
The condition that the wavefront must be a plane at any given time gives us the mathematical backing to describe the wave with an equation. To start, consider a plane [[surface]] oriented in no particular way in three dimensional space. Call $\mathbf{k}$ the normal vector to the surface, $\mathbf{r}$ and $\mathbf{r}_{0}$ two vectors pointing to two points on the surface.

![[Diagram Plane wave condition|70%]]

In [[Cartesian coordinates]] we can represent the vectors as
$$\mathbf{r}=x \hat{\mathbf{x}}+y \hat{\mathbf{y}}+ z \hat{\mathbf{z}},\qquad\mathbf{r}_{0}=x_{0} \hat{\mathbf{x}}+y_{0} \hat{\mathbf{y}}+ z_{0} \hat{\mathbf{z}}$$
and their difference is
$$\mathbf{r}-\mathbf{r}_{0}=(x-x_{0}) \hat{\mathbf{x}}+(y-y_{0}) \hat{\mathbf{y}}+ (z-z_{0}) \hat{\mathbf{z}}$$
For the surface to be a plane, the difference must always be perpendicular to the normal. Our condition is
$$(\mathbf{r}-\mathbf{r}_{0})\cdot \mathbf{k}=0$$
so
$$(x-x_{0})k_{x} \hat{\mathbf{x}}+(y-y_{0})k_{y} \hat{\mathbf{y}}+ (z-z_{0})k_{z} \hat{\mathbf{z}}=0$$
We can regroup the terms as
$$\underbrace{ xk_{x} \hat{\mathbf{x}}+yk_{y} \hat{\mathbf{y}}+zk_{z}\hat{\mathbf{z}} }_{ \mathbf{r}\cdot \mathbf{k} }-\underbrace{ (x_{0}k_{x} \hat{\mathbf{x}}+y_{0}k_{y} \hat{\mathbf{y}}+z_{0}k_{z} \hat{\mathbf{z}}) }_{ \mathbf{r}_{0}\cdot \mathbf{k}\equiv a }=0$$
With this, we get
$$\boxed{\mathbf{r}\cdot \mathbf{k}=a=\text{constant}}$$
If we interpret $\mathbf{k}$ to be the [[wave vector]] of a plane wave with wavefront determined by the surface, the [[scalar product]] of the position vector and the wave vector must be constant everywhere.