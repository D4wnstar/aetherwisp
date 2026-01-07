---
wiki-publish: true
---
This experiment, dating to the late 1800s, measures the [[electron]]'s [[Electric charge|charge]] to [[mass]] ratio $e/m_{e}$ by tracing a thin, wire-like stream of electrons and using the deviations in its trajectory to determine the ratio from known forces.

The experimental apparatus consists of a spherical glass ampule with a cylindrical outcropping. The cylinder houses the electrical parts of the instrument that create the electron stream. The ampule, during construction, has all of its internal atmosphere vacuumed out to leave as little gas inside as possible. In exchange, a small bit of of neon is inserted in the ampule, to a pressure of about $10^{-5}\text{ bar}$ and then permanently sealed. Meanwhile, a small electron blaster is placed inside the cylindrical part and connected to the outside to be powered later. This blaster can emit highly collimated streams of electrons of known energy (a few hundred [[Electronvolt|eV]], for example) that are directed towards the center of the ampule. These electrons collide with the neon [[Molecule|molecules]] in the rarefied atmosphere, causing them to excite and quickly de-excite by emitting a [[photon]]. These photons are visibile to the human eye as a yellow-orange glow that traces the path of the electrons. In other words, turning on the blaster generates a floating, glowing wire-like beam that starts from the blaster and traces the electron stream. We can use this to measure their trajectory and, if we know the forces that are applied to it, the intrinsic properties of the electrons[^1].

A couple of notes: every collision between electrons and neon molecules causes a bit of degradation in the [[energy]] of the beam. After all, the electron passes some of its energy to the atom during the collision. As such, we would formally need to consider *how* much energy is lost by unit distance to respect energy conservation. However, if the collisions are rare, we can take the energy loss to be negligible compared to the total, which simplifies the treatment greatly[^2]. The next question then is: how rarefied does the neon need to be to justify this assumption? Using the [[ideal gas]] law, we know that an [[Avogadro number]] of particles at $1.013\text{ bar}$ and $273.15\text{ K}$ occupies $22.4\times10^{3}\text{ cm}^{3}$ of space. At our pressure of $10^{-5}\text{ bar}$ and temperature of around $293\text{ K}$, this figure becomes about $3.6\times 10^{14}$ neon molecules per cubic centimeter. Using more sophisticated [[cross section]] arguments, this number can be use to determine that there are only a few collisions per centimeter, each moving only a small amount of [[kinetic energy]]. Thus, the approximation is sound and we can consider the kinetic energy, and more importantly the speed, to be constant.

We now need to determine what forces are applied on the electrons. The [[Lorentz force]] is
$$\mathbf{F}=e\mathbf{E}+e\mathbf{v}\times \mathbf{B}$$
so we need the [[Electric field|electric]] and [[magnetic field|magnetic fields]] working on the beam. The local component of magnetic field, $\mathbf{B}_\text{local}$, can be problematic, as it is affected to a significant degree by the surrounding devices. To reduce the effect, it is recommended that the direction of the local field is measured with some tool (like a compass) and that the beam is aligned with this direction. The [[vector product]] $\mathbf{v}\times \mathbf{B}_\text{local}$ hence vanishes and the local magnetic field may be ignored, under the assumption that the alignment is precise.

We can now place two Helmholtz coils surrounding the glass ampule. An [[electric current]] runs through these coils to produce a controlled magnetic field $\mathbf{B}_\text{coils}$ that is both constant and homogeneous. We want to place the coils such that $\mathbf{B}_\text{coils}$ is orthogonal to the beam: this maximizes the vector product to leave a simple multiplication: $\mathbf{v}\times \mathbf{B}_\text{coils}=vB_\text{coils}\hat{\mathbf{r}}$, where $\hat{\mathbf{r}}=\hat{\mathbf{v}}\times \hat{B}_\text{coils}$.

We can assume that there is no ambient electric field on the beam, since unlike the magnetic field, the Earth does not produce a constant electric field. We also avoid adding one of our own. As such, there is no electric field at all on the beam, so $e\mathbf{E}=0$. We are then left with a very simple relation for circular motion:
$$\mathbf{F}=m_{e}\mathbf{a}=evB_\text{coils}\hat{\mathbf{r}}$$
The kinematics are of a circular trajectory are well-known to be
$$\mathbf{a}=- \frac{v^{2}}{r}\hat{\mathbf{r}}$$
and so we find
$$evB_\text{coils}\hat{\mathbf{r}}=-m_{e} \frac{v^{2}}{r}\hat{\mathbf{r}}$$
The directions are always the same, so we can consider the scalar part alone. With some rearrangement we hence find:
$$\frac{e}{m_{e}}= \frac{v}{rB_\text{coils}}$$
Calculating this is our end goal. However, the electron speed $v$ isn't easy to measure, so we need a different quantity from which we can indirectly get $v$. This can be achieved by recalling the kinetic energy of a particle of charge $e$ being subject to an electromagnetic force. We express the force through its associated [[electric potential]] $V$ to get
$$\frac{1}{2}m_{e}v^{2}=eV\quad\Rightarrow \quad v^{2}=\frac{e}{m_{e}}2V$$
Note! This force is *not* the Lorentz force from before. It is the force that the electron blaster applies on the electrons to shoot them out. Taking the square of the previous formula allows us to find
$$v^{2}=\frac{e^{2}r^{2}B_\text{coils}^{2}}{m_{e}^{2}}$$
Equating these two forms of $v^{2}$ leads to
$$\frac{e}{m_{e}}2V=\frac{e^{2}r^{2}B_\text{coils}^{2}}{m_{e}^{2}}$$
and hence
$$\boxed{\frac{e}{m_{e}}=\frac{2V}{r^{2}B_\text{coils}^{2}}}$$
This is our definitive formula, entirely comprised of quantities we can measure empirically:
- $V$ is the potential (i.e., voltage) that we use to power the electron blaster. We know this because we choose it arbitrarily.
- $B_\text{coils}$ is the magnetic field of the coils. We don't set this directly, but we do set the quantities that make it, most importantly the [[electric current]] coursing through the coils. The exact formula depends on the size, shape, number of loops and material of the coils. It can also be measured separately using [[Hall effect]] sensors.
- $r$ is the curvature radius of the beam. If the magnetic field is strong enough, the beam will curve enough to never exit the ampule and draw a full circle, which makes it easier to measure as it just becomes the radius of that circle. The ampule may be built to contain a marked ruler to help measure this visually. Be careful of parallax errors.

As usual, it is best to repeat this measurement in several different configurations, with different voltages and magnetic field intensities in order to construct a richer dataset.

[^1]: If you are familiar with [[cathode ray tube|cathode ray tubes]], this might sound familiar. The basic mechanism is very similar and is indeed an early precursor to the cathode ray tubes.

[^2]: If you are curious about particle beam energy degradation through matter, see [[Stopping power]].
