---
wiki-publish: true
aliases:
  - monochromatic plane wave
  - sinusoidal plane wave
  - sine wave
---
A **plane wave** is a [[wave]] whose [[wavefront]] is a [[plane]] everywhere. The simplest and most important form of plane wave is a **monochromatic** or **sinusoidal plane wave** (often just called a **sine wave**), whose general equation is
$$u(\mathbf{r},t)=A\sin(\mathbf{k}\cdot \mathbf{r}-\omega t+\varphi)$$
where
- $A$ is constant interpreted as the [[Wave equation|amplitude]] of the wave.
- $\mathbf{k}$ is the [[Wavenumber|wavevector]]. This is constant in a monochromatic wave.
- $\omega$ is the [[Frequency|angular frequency]]. This is constant in a monochromatic wave.
- $\varphi$ is the [[phase]].

Often, the sine wave is given as a complex wave using complex exponentials:
$$\tilde{u}(\mathbf{r},t)=Ae^{i[\mathbf{k}\cdot \mathbf{r}-\omega t+\varphi]}$$
This is achieved by adding a new imaginary term to the sine wave and then using [[Euler's formula]]. The [[real and imaginary parts|real part]] of the complex wave is the previous equation: $\text{Re}[\tilde{u}(\mathbf{r},t)]=u(\mathbf{r},t)$. The benefit of this formulation is that it's often a lot easier to work with complex exponentials that it is to deal with sines and cosines. The constant part of this representation, $Ae^{i\varphi}$, is called a [[phasor]].

The importance of plane waves comes from the fact that every wave can be seen as being locally plane at small enough scales, due to any geometric [[surface]] being approximately plane for small enough regions. The importance of *sine waves* in particular is different though. It comes from the field of Fourier analysis, where the [[Fourier series]] guarantees that, under some conditions, almost any function can be represented as a (possibly infinite) sum of sines. As such, pretty much any wave can be rewritten as a big sum of sine waves and so, by just knowing how these work, we know in principle how *any* wave works.
### Definition
The condition for a plane wave is that the wavefront must be a plane at any given time. To start, consider a plane [[surface]] oriented in no particular way in three dimensional space. Call $\mathbf{k}$ the normal vector to the surface, $\mathbf{r}$ and $\mathbf{r}_{0}$ vectors pointing to two points on the surface.

![[Diagram Plane wave condition|70%]]

In [[Cartesian coordinates]] we can represent the vectors as
$$\mathbf{r}=x \hat{\mathbf{x}}+y \hat{\mathbf{y}}+ z \hat{\mathbf{z}},\qquad\mathbf{r}_{0}=x_{0} \hat{\mathbf{x}}+y_{0} \hat{\mathbf{y}}+ z_{0} \hat{\mathbf{z}}$$
Their difference is
$$\mathbf{r}-\mathbf{r}_{0}=(x-x_{0}) \hat{\mathbf{x}}+(y-y_{0}) \hat{\mathbf{y}}+ (z-z_{0}) \hat{\mathbf{z}}$$
For the surface to be a plane, the difference must always be [[Orthogonality|perpendicular]] to the normal (and so parallel to the plane). Our condition then is
$$(\mathbf{r}-\mathbf{r}_{0})\cdot \mathbf{k}=0$$
so
$$(x-x_{0})k_{x} \hat{\mathbf{x}}+(y-y_{0})k_{y} \hat{\mathbf{y}}+ (z-z_{0})k_{z} \hat{\mathbf{z}}=0$$
We can regroup the terms as
$$\underbrace{ xk_{x} \hat{\mathbf{x}}+yk_{y} \hat{\mathbf{y}}+zk_{z}\hat{\mathbf{z}} }_{ \mathbf{r}\cdot \mathbf{k} }-\underbrace{ (x_{0}k_{x} \hat{\mathbf{x}}+y_{0}k_{y} \hat{\mathbf{y}}+z_{0}k_{z} \hat{\mathbf{z}}) }_{ \mathbf{r}_{0}\cdot \mathbf{k}\equiv a }=0$$
With this, we get
$$\boxed{\mathbf{r}\cdot \mathbf{k}=a=\text{constant}}$$
The connection to waves should be readily apparent now: a wave is plane if the position vector is always orthogonal to the [[Wavenumber|wavevector]].