A **magnetic dipole** is a tiny [[electric current]] loop. If the size of the loop is infinitesimal, the dipole is said to be **perfect**, otherwise it is **physical**. They are characterized by a [[magnetic dipole moment]]. It is the magnetic analog of the [[electric dipole]].
### Under a magnetic field
Consider a rectangular magnetic dipole of sides $a$ and $b$ subject to a uniform [[magnetic field]] $\mathbf{B}$. Any loop can be built up from an infinite number of arbitrarily small rectangles (a [[Riemann sum]]), so this discussion can be extended without loss of generality to any shape of the loop. For simplicity, center the loop at the origin and, using [[Cartesian coordinates]], tilt the loop by an angle $\theta$ from the $z$ axis towards the $y$ axis. Let $\mathbf{B}$ be in the $z$ direction.

![[Schema Magnetic dipole rotation|100%]]

The forces on the sloping sides cancel out (they stretch the loop, but they don't rotate it). The forces horizontal to the loop $\mathbf{F}$ also cancel each other out linearly, but not rotationally. They apply a moment of force
$$\mathbf{N}=aF\sin \theta\ \hat{\mathbf{x}}$$
The magnitude of these forces is
$$F=IbB$$
and therefore
$$\mathbf{N}=IabB\sin \theta\ \hat{\mathbf{x}}=mB\sin \theta\ \hat{\mathbf{x}}$$
or
$$\boxed{\mathbf{N}=\mathbf{m}\times \mathbf{B}}$$
where $m=Iab$ is the magnetic dipole moment. This moment of force is exact on any magnetic dipole if the field is uniform. If it is not uniform, it is exact only for perfect dipoles, which have no spatial extension and therefore ignore the fact that it's not uniform.

This torque tends to align the dipole in the direction of the magnetic field and accounts for [[Paramagnet|paramagnetism]]. It might seem then that paramagnetism is the only form of magnetism, as there's nothing here to account for the existence of a [[diamagnet]]. However, the magnetic dipole in matter is given by [[spin|spinning]] [[Elettrone|electrons]] and these, due to the [[Pauli exclusion principle|Pauli exclusion principle]], tend to pair up with electrons of opposite spin, canceling each other out magnetically. Thus, this rotation is only observed in [[Atomo|atoms]] with odd number of electrons. Even here, the alignment can be broken by thermal collisions.

If the field is uniform, the force over the current loop is zero:
$$\mathbf{F}=I\oint d\mathbf{I}\times \mathbf{B}=I\left( \oint \mathbf{dI} \right)\times \mathbf{B}=\mathbf{0}$$
but if the field is non-uniform, for a perfect dipole of magnetic moment $\mathbf{m}$ we have
$$\boxed{\mathbf{F}=\nabla(\mathbf{m}\cdot \mathbf{B})}$$
### Radiation
If the current going through the dipole loop is alternating, the dipole moment becomes variable. The magnetic field starts to vary, induces and [[electric field]] and we get the emission of [[electromagnetic wave|electromagnetic waves]].

For a simple model, let's assume the dipole is a circular loop of radius $b$ that the current is alternating in a sinusoidal fashion:
$$I(t)=I_{0}\cos(\omega t)$$
The dipole moment becomes
$$\mathbf{m}(t)=\pi b^{2}I(t)\hat{\mathbf{z}}=m_{0}\cos(\omega t)\hat{\mathbf{z}}$$
by setting the dipole axis on the $z$ axis and calling $m_{0}\equiv \pi b^{2}I_{0}$.

![[Diagram Magnetic dipole radiation]]

