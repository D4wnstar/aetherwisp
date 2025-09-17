---
wiki-publish: true
---
A **magnetic spectrometer** is a [[detector]] designed to measure the [[Linear momentum|momentum]] of a [[Electric charge|charged]] [[particle]] from the [[curvature]] of its trajectory in a uniform [[magnetic field]]. It is often paired with at least one speed-measuring instrument to find the particle's [[mass]] from $m=p/v$.

A magnetic spectrometer typically consists of a magnet and a series of sub-detectors that track the motion of the particle as it passes through the apparatus. Its exact shape and components vary widely depending on the experiment and intended use case.
### Operation
The dynamics of the particle are determined by the [[Lorentz force]], specifically a purely magnetic force:
$$\mathbf{F}=q\mathbf{v}\times \mathbf{B}$$
$q$ is the charge of the particle, $\mathbf{v}$ is its velocity and $\mathbf{B}$ is the magnetic field we are applying. If the velocity has a single component that is [[Orthogonality|orthogonal]] to $\mathbf{B}$, then its trajectory is a [[circumference]] of radius
$$R=\frac{p}{qB}\quad\Rightarrow \quad p=qBR$$
Expressing momentum in [[Electronvolt|GeV]]/[[Speed of light|c]], magnetic field in $\text{T}$ and the radius in $\text{m}$, then using [[natural units]], we can manipulate the units to get rid of the charge explicitly
$$p=0.3BR$$
To trace the trajectory [[circular arc|arc]] we'll need at least three detectors, one at the entrance, one at the exit and one in an intermediate point.

:::image
![[Diagram Sagitta method]]
A magnetic spectrometer schematic. The colored background is the apparatus where the magnetic field is. The blue line is the particle's trajectory arc, the purple dots are the detectors and the red line is the sagitta of the arc.
:::

We'll use the [[sagitta]] of the arc as a reference point:
$$s=R-R\cos\left( \frac{\theta}{2} \right)=R\left( 1-\cos\left( \frac{\theta}{2} \right) \right)=2R\sin ^{2}\left( \frac{\theta}{4} \right)$$
by using the half-angle formula. We'll use the small-angle approximation of the sine ($\sin \theta \simeq \theta$) and further $\theta \simeq L/R$ to say
$$\sin \frac{\theta}{4}\simeq \frac{\theta}{4}\simeq \frac{L}{4R}= \frac{0.3}{4} \frac{LB}{p}$$
and so, substituting $R=p/0.3B$,
$$s=2 \frac{p}{0.3B} \left( \frac{0.3}{4} \frac{LB}{p} \right)^{2}=2 \frac{p}{0.3B} \frac{0.3^{2}}{16} \frac{L^{2}B^{2}}{p^{2}}=\frac{0.3}{8} \frac{BL^{2}}{p}$$
Then, $p$ is
$$\boxed{p=\frac{0.3}{8} \frac{BL^{2}}{s}}$$
$B$, $L$ and $s$ are all known by the blueprint of the detector. The error on this measurement is mostly a sagitta problem, as $B$ and $L$ are measurable with very high precision. Then, the relative [[standard deviation]] is
$$\boxed{\frac{\sigma_{p}}{p}=\frac{\sigma_{s}}{s}=\frac{8}{0.3} \frac{p}{BL^{2}}\sigma _{s}}$$
The resolution improves as the field gets stronger and, especially, as the detector gets larger. It worsens for large momenta. The easiest answer would be to just make the thing bigger, but besides costs and the simple problem of fitting the instrument somewhere usable, this result is valid only in the small angle approximation: a bigger instrument might very well go out of range for this approximation and invalidate the formula, so care is needed on how $L$ and $B$ are modified.

Now, we need to figure out the sagitta itself. If we call $x_{1},x_{2},x_{3}$ the points where a particle is found by the detectors from left to right, the sagitta is
$$s=x_{2}- \frac{x_{1}+x_{2}}{2}$$
The error on this is
$$\sigma_{s}=\sqrt{ \frac{3}{2} }\sigma_{x}$$
Therefore the momentum error is
$$\boxed{\frac{\sigma_{p}}{p}=\sqrt{ \frac{3}{2} } \frac{8}{0.3} \frac{p}{BL^{2}}\sigma_{x}}$$
The precision of the momentum measurements depends on how precisely the detectors can locate the particle within their range, which is fundamentally an engineering problem.

> [!example]-
> An example spectrometer might detect a $1\text{ GeV/c}$ particle, have a $1\text{ T}$ field, width equal to $1\text{ m}$ and spatial resolution $\sigma_{x}=200\ \mu\text{m}$. This particular machine would have a relative standard deviation of $\sigma_{p}/p \simeq 6\times10^{-3}$.