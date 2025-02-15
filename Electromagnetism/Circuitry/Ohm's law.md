**Ohm's law** is a law that describes the [[electric potential]] difference and [[electrical resistance]] of a closed circuit made of thin wires:
$$\Delta V=RI \quad\text{where }\quad R=\rho\frac{l}{S}=\rho \int_{0}^{l} \frac{1}{S(s)}ds$$
$\Delta V$ is the potential difference calculated between the point of highest and lowest potential. In a circuit, these would be the connections to a battery or generator. $R$ is the resistance and $I$ is the [[electric current]] running through the wire. Specifically, it is a free current, not a bound current.

The resistance formula works for wires. $l$ is the length of the wire and $S$ is its cross-section. $\rho$ is the [[electrical resistivity]], which depends on the properties of the material it's made of. If the cross-section is constant throughout the length of the wire, it results in a trivial integration. $R$ is the total resistance of the entire wire.

There is also a much more general and physically meaningful form that applies to any linear, homogeneous and isotropic [[conductor]]:
$$\mathbf{J}=\sigma\mathbf{f}=\frac{1}{\rho}\mathbf{f}$$
where $\mathbf{f}$ is the force per unit charge, $\sigma$ is the [[electrical conductivity]] of the material and $\rho=1/\sigma$ is the [[electrical resistivity]]. For most electromagnetic forces, $\mathbf{f}$ is just the [[electric field]] $\mathbf{E}$:
$$\mathbf{J}=\sigma\mathbf{E}=\frac{1}{\rho} \mathbf{E}$$
This reduces to the above simpler form at the start when $\mathbf{E}$ is time-independent. If it is not, the [[curl]] of $\mathbf{E}$ is not zero and the field is no longer uniform inside the wire, which in turn means that the resistance becomes dependent on the frequency of $\mathbf{E}$.

A material that obeys Ohm's laws is said to be ohmic. Non-ohmic materials behave differently, namely their currents $\mathbf{J}$ typically do not point in the same direction as their produced field $\mathbf{E}$.
### Differential form of first law
Ohm's first law can also be represented in integral form, which has the benefit of being applicable to all ohmic conductors regardless of shape (and so not just wires). Let's consider a [[conductor]] of any shape being traversed by a certain current density $\mathbf{J}$. Let's also consider a tiny cylinder aligned with $\mathbf{J}$ of height $l$ and cross-section $dS$. Using Ohm's second law, the resistance of the cylinder is
$$R=\rho \frac{dl}{dS}$$
There's also a potential difference $dV$ between the top and bottom of the cylinder, so we can also apply the first law to it
$$dV=RdI=\rho \frac{dl}{dS}dI$$
But $dV=E\ dl$ and $dI=J\ dS$ (with $E$ the electric field described by that potential) so if we plug these in we get
$$E\ \cancel{ dl }=\rho \frac{\cancel{ dl }}{\cancel{ dS }}J\cancel{ dS }$$
$$E=\rho J$$
But these two have the same direction (locally), so we can extend this to vector form
$$\boxed{\mathbf{E}=\rho\mathbf{J}}$$
and also in an inverse form
$$\boxed{\mathbf{J}=\sigma\mathbf{E}}$$
where $\sigma=1/\rho$ is the electrical conductivity of the material. This is an important relation because it shows that ohmic conductors show linear behavior regarding current flow when subject to electric fields.

This is actually a specific case of the more general law, however. The current density depends on the *force per unit charge* $\mathbf{f}$, not on the electric field directly:
$$\mathbf{J}=\sigma\mathbf{f}$$
It just so happens that usually the electric field is the only *relevant* field pushing the charges around, but in general, for electromagnetic forces, there will be a magnetic contribution too, as given by the [[Lorentz force]]:
$$\boxed{\mathbf{J}=\sigma(\mathbf{E}+\mathbf{v}\times \mathbf{B})}$$
The reason the former formula is still mostly correct is because the charges are often moving rather slowly within circuitry, which makes the magnetic forces minimal in comparison to the electric ones. In [[plasma|plasmas]] however, the second term is usually not negligible.
#### Consequences
Say you have a piece of ohmic material that's being traversed by a *steady* current. We know that the [[divergence]] of the electric field is zero, so
$$\nabla\cdot\mathbf{E}=\frac{1}{\sigma}\nabla\cdot\mathbf{J}=0$$
As expected, Ohm's law obeys the continuity equation $\nabla\cdot\mathbf{J}=-\frac{ \partial \rho }{ \partial t }=0$. This is true only if the conductivity is constant, that is, uniform over the material. What this means is that, *inside* of a material of uniform conductivity subject to a steady current, [[Laplace's equation]] still holds and may be used to calculate the potential. It is not in general true *outside* and especially not on the interface between materials.

Furthermore, assume that the conductivity of this material is $\sigma \simeq 10^{7}\ (\Omega\text{m})^{-1}$, which is a typical value for metals. In the above equation, if we apply [[Gauss' law]] to the left hand side and the continuity equation to the right hand side we get
$$\frac{\rho}{\epsilon_{0}}=-\frac{1}{\sigma}\frac{ \partial \rho }{ \partial t } $$
which is a first order [[partial differential equation]] for charge density in time. Solving it and remembering that in a conductor, the charge density is entirely free, $\rho=\rho_{f}$, gives
$$\rho_{f}(\mathbf{r},t)=\rho_{f}(\mathbf{r},0)e^{-\sigma t/\epsilon_{0}}$$
Since we know $\sigma$, we know that $\sigma/\epsilon_{0}\simeq 10^{18}\text{ Hz}$. But this frequency gives the characteristic time in which the free charge density changes due to an external stimulus field. If it weren't obvious, this is an *extraordinarily high* frequency, which leads to extraordinarily short response times, in the order of $10^{-18}$ seconds. Outside of pretty extreme conditions[^1], times of this order are always negligible.

> [!success] Conductor response times
> Electromagnetic responses in an ohmic conductor are effectively instant.
### Relation to temperature
Most materials, when heated, expand in size (some materials shrink, but the discussion applies to them too). Since the second law is dependent on the geometry of the material, it is indirectly dependent on temperature too. When a material expands, $l$ increases, but so does the cross-section $S$. In the specific case of a wire, the ratio $l/S$ tends to remain constant (or approximately so), which means Ohm's second law is mostly temperature-independent for wires. This does not hold for other shapes.

The exact expression of resistivity with respect to temperature is extremely complicated and the domain of statistical mechanics. At a high level, we can use a [[serie|series expansion]] like
$$\rho(\theta)\simeq\rho_{\theta_{0}}[1+\alpha(\theta-\theta_{0})]$$
where $\rho_{\theta_{0}}$ is the resistivity at reference temperature $\theta_{0}$. $\alpha$ is a constant that depends on the material. The scale of temperature is generally arbitrary, but Celsius is the usual (Kelvins are asymmetric as there is no negative absolute temperature, which makes them harder to work with). The reference temperature is also arbitrary: in physics choosing 0°C is common, whereas in chemistry and engineering 20°C is more typical.

[^1]: Such as high energy [[photon]] beams like X rays and gamma rays. Even a metal wall can't fully stop a high energy [[electromagnetic wave]] because even $10^{-18}\text{ s}$ isn't fast enough to fully nullify it. This is why high energy waves can be very dangerous and nearly impossible to contain.
