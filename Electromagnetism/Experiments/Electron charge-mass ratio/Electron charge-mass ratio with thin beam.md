---
hl-publish: true
---
This experiment, dating to the late 1800s, measures the [[electron]]'s [[Electric charge|charge]] to [[mass]] ratio $e/m_{e}$ by tracing a thin, wire-like stream of electrons and using the deviations in its trajectory to determine the ratio from known forces.

The experimental apparatus consists of a spherical glass ampule. It's essentially a modified [[cathode ray tube]], but instead of the [[electron gun]] being on one end aimed at a phosphor screen on the other, the gun is near the center of the ampule, aimed tangentially to the sphere's surface. Like a CRT, the ampule has all of its internal atmosphere evacuated during construction to leave as little gas inside as possible. Unlike a CRT, a small bit of of neon is reinserted in the ampule, to a [[pressure]] of about $10^{-5}\text{ bar}$ and then permanently sealed. The electrons shot by the gun collide with the neon [[Molecule|molecules]] in the rarefied atmosphere, causing them to excite and quickly de-excite by emitting a [[photon]]. The first excitation energy of neon molecules has energy that falls within the visible range of [[Electromagnetic radiation|light]], specifically in the yellow-orange range. This glow is visible to the naked eye and traces the path of the electrons. Through this wire-like glowing beam, we can extract information about electrons.

Every [[Particle scattering|collision]] between electrons and neon molecules causes a bit of degradation in the [[kinetic energy]] of the beam. As such, we would formally need to consider *how* much energy is lost (or, rather, transferred) per unit distance to respect energy conservation. However, as long as the collisions are rare, we can take the energy loss to be negligible compared to the total and count the electron kinetic energy as a constant, which simplifies the treatment greatly.[^1] The next question then is: how rarefied does the neon need to be to justify this assumption? Using the [[ideal gas]] law, we know that an [[Avogadro number]] of particles at [[standard temperature and pressure|STP]] ($P=1.013\text{ bar}$ and $T=273.15\text{ K}$) occupies $V=22.4\times10^{3}\text{ cm}^{3}$ of space. At our pressure of $10^{-5}\text{ bar}$ and temperature of around $293\text{ K}$, this figure becomes about
$$\frac{N}{V}=\frac{P}{k_{B}T}=3.6\times 10^{14}\text{ Ne molecules/cm}^{3}$$
Using more sophisticated [[cross section]] arguments, this number can be use to determine that there are only a few collisions per centimeter, each transferring only a small amount of kinetic energy. Thus, the approximation is quantitatively sound and we can consider the kinetic energy, and more importantly the speed, to be a [[constant of motion]], at least to the resolution that the thickness of the neon trace allows us to measure.

We now need to determine what forces are applied on the electrons. The [[Lorentz force]] is
$$\mathbf{F}=e\mathbf{E}+e\mathbf{v}\times \mathbf{B}$$
so we need the [[Electric field|electric]] and [[magnetic field|magnetic fields]] working on the beam. The local component of magnetic field, $\mathbf{B}_\text{local}$, can be problematic, as it is affected to a significant degree by the surrounding devices. To reduce the effect, it is recommended that the direction of the local field is measured with some tool (like a compass) and that the beam is aligned with this direction. The [[vector product]] $\mathbf{v}\times \mathbf{B}_\text{local}$ hence vanishes and the local magnetic field may be ignored, under the assumption that the alignment is precise.

We can now place two Helmholtz coils surrounding the glass ampule. An [[electric current]] runs through these coils to produce a controlled, constant magnetic field $\mathbf{B}_\text{coils}$. We want to place the coils such that $\mathbf{B}_\text{coils}$ is orthogonal to the beam: this maximizes the vector product to leave a simple multiplication: $\mathbf{v}\times \mathbf{B}_\text{coils}=vB_\text{coils}\hat{\mathbf{r}}$, where $\hat{\mathbf{r}}=\hat{\mathbf{v}}\times \hat{B}_\text{coils}$.

We can assume that there is no ambient electric field on the beam (this is only partly true, though; more on this below). As such, there is no electric field at all on the beam, so $e\mathbf{E}=0$. We are then left with a very simple relation for circular motion:
$$\mathbf{F}=m_{e}\mathbf{a}=evB_\text{coils}\hat{\mathbf{r}}$$
The kinematics are of a circular trajectory are well-known to be
$$\mathbf{a}=- \frac{v^{2}}{r}\hat{\mathbf{r}}$$
and so we find
$$evB_\text{coils}\hat{\mathbf{r}}=-m_{e} \frac{v^{2}}{r}\hat{\mathbf{r}}$$
The directions are always the same, so we can consider the [[scalar]] part alone. With some rearrangement we hence find:
$$\frac{e}{m_{e}}= \frac{v}{rB_\text{coils}}\tag{1}$$
Calculating this is our end goal. However, the electron speed $v$ isn't easy to measure, so we need a different quantity from which we can indirectly get $v$. We know $v$ is pretty much entirely due to the electron gun, which operates at an acceleration [[electric potential|potential]] $V_\text{acc}$. This is transformed into kinetic energy through
$$\frac{1}{2}m_{e}v^{2}=eV_\text{acc}\quad\Rightarrow \quad v^{2}=\frac{e}{m_{e}}2V_\text{acc}\tag{2}$$
Taking the square of $(1)$ allows us to find
$$v^{2}=\frac{e^{2}r^{2}B_\text{coils}^{2}}{m_{e}^{2}}$$
Equating this with $(2)$ leads to
$$\frac{e}{m_{e}}2V_\text{acc}=\frac{e^{2}r^{2}B_\text{coils}^{2}}{m_{e}^{2}}$$
and hence
$$\boxed{\frac{e}{m_{e}}=\frac{2V_\text{acc}}{r^{2}B_\text{coils}^{2}}}$$
This is our definitive formula, entirely comprised of quantities we can measure empirically:
- $V_\text{acc}$ is the potential that we use to power the electron gun. This is chosen manually through the laboratory power supply.
- $B_\text{coils}$ is the magnetic field of the coils. We don't set this directly, but we do set the quantities that make it, most importantly the [[electric current]] coursing through the coils. The exact formula depends on the size, shape, number of loops and material of the coils and is likely to be quite complicated. It can also be measured separately using a [[magnetometer]].
- $r$ is the curvature radius of the beam. If the magnetic field is strong enough, the beam will curve enough to never exit the ampule and draw a full circle, which makes it easier to measure as it just becomes the radius of that circle. Ampules designed for this experiment include measuring ticks on the inside specifically made to measure this visually. Be careful of parallax errors.

As usual, it is best to repeat this measurement in several different configurations, with different voltages and magnetic field intensities in order to construct a richer dataset.

A few notes:
- Small radii are problematic because the electrons will make a small loop near the electron gun. The gun uses a pretty strong electric field which tends to escape the gun's volume, so it is likely that the "no electric field" approximation no longer works here.
- Overly large radii are also problematic because the electrons won't make a full loop and will escape the glass ampule. Besides not being visible outside the ampule and thus hard to measure, they also electrically charge the glass, which can be unsafe.
- The electron gun can have fringe fields that mess with the beam even outside of small radii. It's unlikely you can do much about this without changing the gun itself (besides maybe reducing $V_\text{acc}$), but it's worth keeping in mind as a possible source of [[Systematic error|systematic errors]].
- The device should remain still for the entire experiment. Moving it breaks the alignment with the Earth's magnetic field and changes the behavior of the beam.

[^1]: If you are curious about particle beam energy degradation through matter, see [[Stopping power]].
