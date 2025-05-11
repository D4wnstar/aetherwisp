---
wiki-publish: true
---
The **Laplacian** $\nabla^{2}$ is a differential [[operatore|operator]] defined as the [[divergence]] of the [[gradient]] of a scalar-valued function in Euclidean space. The canonical form is defined in [[Cartesian coordinates]] and, given a twice [[Differential|differentiable]] function $f:\mathbb{R}^{3}\to\mathbb{R}$, is:
$$\nabla^{2}f=\nabla\cdot\nabla f=\left(\frac{\partial ^{2}}{\partial x^{2}} + \frac{\partial ^{2}}{\partial y^{2}} + \frac{\partial ^{2}}{\partial z^{2}}\right)f$$
which is the sum of all non-mixed second derivatives of the function $f$. In an arbitrary dimensional space of (finite) dimension $N$ we have
$$\nabla^{2}f=\sum\limits_{i=1}^{N}\frac{\partial ^{2}f}{\partial x_{i}^{2}}$$
### Polar coordinates
The Laplacian in polar coordinates $(r,\theta)$ is
$$\nabla^{2}f=\frac{\partial ^{2}f}{\partial r^{2}} + \frac{1}{r}\frac{\partial f}{\partial r}+ \frac{1}{r^{2}}\frac{\partial ^{2}f}{\partial \theta^{2}}$$
with $r$ the distance from the center and $\theta$ the angle of rotation.
### Cylindrical coordinates
The Laplacian in cylindrical coordinates $(r,\varphi,z)$ is
$$\nabla^{2}f=\frac{1}{r}\frac{\partial }{\partial r}\left(r \frac{\partial f}{\partial r}\right)+ \frac{1}{r^{2}}\frac{\partial ^{2}f}{\partial \varphi^{2}}+ \frac{\partial ^{2}f}{\partial z^{2}}$$
with $r$ the radial distance, $\varphi$ the azimuthal angle and $z$ the height.
### Spherical coordinates
The Laplacian in spherical polar coordinates $(r,\theta,\phi)$ is
$$\nabla^{2}f=\frac{1}{r^{2}}\frac{\partial }{\partial r}\left(r^{2}\frac{\partial f}{\partial r}\right)+ \frac{1}{r^{2}\sin\theta}\frac{\partial }{\partial \theta}\left(\sin\theta \frac{\partial f}{\partial \theta}\right)+ \frac{1}{r^{2}\sin^{2}\theta}\left(\frac{\partial ^{2}f}{\partial \phi^{2}}\right)$$
with $r$ the radial distance, $\theta$ the azimuthal angle and $\phi$ the zenith angle.