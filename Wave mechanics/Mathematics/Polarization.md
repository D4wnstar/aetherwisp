---
wiki-publish: true
aliases:
  - polarized
---
The **polarization** of a [[transverse wave]] is the set of independent axes that it can oscillate in. It may also refer to the individual axis the wave oscillates on, or even just the property of having such an axis.

Polarization arises because real space is three-dimensional, but the direction of propagation is only one axis. As such, there are always two remaining axes that are always [[Orthogonality|orthogonal]] to the direction of propagation and the space in which the transverse wave can oscillate in is therefore a [[plane]]. The direction of oscillation is a [[Vector space|vector]] in this two-dimensional space and may thus be expressed as a [[linear combination]] of the [[basis]] vectors of this plane. These basis vectors are called the **polarization states** of the wave and their ([[Normalization|normalized]]) linear combination is the **polarization vector** $\hat{\mathbf{n}}$ (also $\hat{\varepsilon}$ sometimes). The polarization vector uniquely determines the axis of oscillation.

The polarization vector can be used to define the plane of oscillation using the orthogonality condition. Say the wave is traveling on an axis determined by its [[Wavenumber|wavevector]] $\mathbf{k}$. The wave oscillates on the plane perpendicular to $\mathbf{k}$, identified by
$$\hat{\mathbf{n}}\cdot \hat{\mathbf{k}}=0$$

The polarization of a transverse wave is not guaranteed. It may be possible for the polarization vector of the wave to vary extremely fast and show chaotic behavior, so that it may as well be considered completely [[Random variable|random]]. This is the case for sunlight and more generally [[thermal radiation]]. In this case, the wave is said to be **unpolarized**.
### Polarization bases
The polarization states form the basis of the oscillation plane. As such, *any* such basis works well for describing polarization. In practice, some bases are better than others, namely two of them.

On one hand, you can use [[Cartesian coordinates]]. Just pick the canonical basis $\{ \hat{\mathbf{x}},\hat{\mathbf{y}} \}=\{ (1,0),(0,1) \}$ and you get what's called **linear polarization**, called so because it is most convenient to describe oscillations in a straight line (think of a rope going up and down: that's linear polarization). The polarization vector then is
$$\hat{\mathbf{n}}=\cos \theta\ \hat{\mathbf{x}}+\sin \theta\ \hat{\mathbf{y}}$$
where $\theta$ is called the **polarization angle**.

On the other hand, you can describe oscillations as something closer to rotations. If this seems weird, imagine the wave as a corkscrew moving forward with the pointy end aimed forward. Instead of going up or down, you follow the surface of the corkscrew, which makes you *rotate*. Alternatively, it's like walking up a spiral staircase. You are "propagating" upwards, but also rotating around the direction of propagation (the column at the center of the stairs). This is called **circular polarization**.

:::image
![[CircularPolarization.gif]]
An example of a circularly polarized wave.
By Dave3457 - Own work, Public Domain, from [Wikipedia](https://commons.wikimedia.org/w/index.php?curid=9862801).
:::

Intuitively, you can probably guess what the basis is: it's clockwise $(+)$ and counter-clockwise $(-)$ [[rotation|rotations]]. These are also called right- and left-circular polarization. The cleanest way to represent these states is through complex numbers:
$$\{ \hat{\mathbf{e}}_{+},\hat{\mathbf{e}}_{-} \}=\left\{  \frac{\hat{\mathbf{x}}+i\hat{\mathbf{y}}}{\sqrt{ 2 }}, \frac{\hat{\mathbf{x}}-i\hat{\mathbf{y}}}{\sqrt{ 2 }} \right\}$$
Again, the polarization vector is some linear combination of these. Though less intuitive, circular polarization actually appears several times in physics. For instance, in quantum optics, the [[spin]] of a [[Photon]] *is* its polarization, so it is most natural to express spin as a rotation. Also, linear polarizations can be seen as a subtype of circular ones, where two rotations superimpose and perfectly cancel each other out, leaving only a linear oscillation.