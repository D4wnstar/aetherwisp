---
aliases:
  - Ohm's first law
  - Ohm's second law
---
**Ohm's laws** are a set of two experimentally-determined laws that describe the [[electric potential]] difference and [[electrical resistance]] of a closed circuit made of thin wires:
$$(1)\quad\Delta V=RI, \qquad R=\rho_{R}\frac{l}{S}\quad(2)$$
In the first law, $\Delta V$ is the potential difference calculated between the point of highest and lowest potential. In a circuit, these would be the connections to a battery or generator. $R$ is the resistance and $I$ is the [[electric current]] running through the wire. 

The second law is applicable only to homogeneous wires. $l$ is the length of the wire and $S$ is its cross-section. $\rho_{R}$ is the [[electrical resistivity]], which depends on the properties of the material it's made of.

A material that obeys Ohm's laws is said to be ohmic.

There is also a much more general and physically meaningful form that applies to all matter and reduces to the forms above in the specific case of wires:
$$\mathbf{J}=\sigma_{C}\mathbf{f}$$
where $\mathbf{f}$ is the force per unit charge and $\sigma_{C}$ is the [[electrical conductivity]] of the material. For most electromagnetic forces, $\mathbf{f}$ is just the [[electric field]] $\mathbf{E}$:
$$\mathbf{J}=\sigma_{C}\mathbf{E}$$
### Differential form of first law
Ohm's first law can also be represented in integral form, which has the benefit of being applicable to all materials regardless of shape (and so not just wires). Let's consider a [[conductor]] of any shape being traversed by a certain current density $\mathbf{J}$. Let's also consider a tiny cylinder aligned with $\mathbf{J}$ of height $l$ and cross-section $dS$. Using Ohm's second law, the resistance of the cylinder is
$$R=\rho_{R} \frac{dl}{dS}$$
There's also a potential difference $dV$ between the top and bottom of the cylinder, so we can also apply the first law to it
$$dV=RdI=\rho_{R} \frac{dl}{dS}dI$$
But $dV=E\ dl$ and $dI=J\ dS$ (with $E$ the electric field described by that potential) so if we plug these in we get
$$E\ \cancel{ dl }=\rho_{R} \frac{\cancel{ dl }}{\cancel{ dS }}J\cancel{ dS }$$
$$E=\rho_{R}J$$
But these two have the same direction (locally), so we can extend this to vector form
$$\boxed{\mathbf{E}=\rho_{R}\mathbf{J}}$$
and also in an inverse form
$$\boxed{\mathbf{J}=\sigma_{C}\mathbf{E}}$$
where $\sigma_{C}=1/\rho_{R}$ is the electrical conductivity of the material. This is an important relation because it shows that ohmic conductors show linear behavior regarding current flow when subject to electric fields.

This is actually a specific case of the more general law, however. The current density depends on the *force per unit charge* $\mathbf{f}$, not on the electric field directly:
$$\mathbf{J}=\sigma_{C}\mathbf{f}$$
It just so happens that usually the electric field is the only *relevant* field pushing the charges around, but in general, for electromagnetic forces, there will be a magnetic contribution too:
$$\boxed{\mathbf{J}=\sigma_{C}(\mathbf{E}+\mathbf{v}\times \mathbf{B})}$$
The reason the former formula is still mostly correct is because the charges are often moving rather slowly within circuitry, which makes the magnetic forces minimal in comparison to the electric ones. In [[plasma|plasmas]] however, the second term is usually not negligible.
#### Consequences
Say you have a piece of ohmic material that's being traversed by a *steady* current. We know that the [[divergence]] of the electric field is zero, so
$$\nabla\cdot\mathbf{E}=\frac{1}{\sigma_{C}}\nabla\cdot\mathbf{J}=0$$
This is true only if the conductivity is constant, that is, uniform over the material. What this means is that, *inside* of a material of uniform conductivity subject to a steady current, [[Laplace's equation]] still holds and may be used to calculate the potential. It is not in general true *outside*.
### Relation to temperature
Most materials, when heated, expand in size (some materials shrink, but the discussion applies to them too). Since the second law is dependent on the geometry of the material, it is indirectly dependent on temperature too. When a material expands, $l$ increases, but so does the cross-section $S$. In the specific case of a wire, the ratio $l/S$ tends to remain constant (or approximately so), which means Ohm's second law is mostly temperature-independent for wires. This does not hold for other shapes.

The exact expression of resistivity with respect to temperature is extremely complicated and the domain of statistical mechanics. At a high level, we can use a [[serie|series expansion]] like
$$\rho(\theta)\simeq\rho_{\theta_{0}}[1+\alpha(\theta-\theta_{0})]$$
where $\rho_{\theta_{0}}$ is the resistivity at reference temperature $\theta_{0}$. $\alpha$ is a constant that depends on the material. The scale of temperature is generally arbitrary, but Celsius is the usual (Kelvins are asymmetric as there is no negative absolute temperature, which makes them harder to work with). The reference temperature is also arbitrary: in physics choosing 0°C is common, whereas in chemistry and engineering 20°C is more typical.