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
### Integral form of first law
Ohm's first law can also be represented in integral form, which has the benefit of being applicable to all materials regardless of shape (and so not just wires). Let's consider a [[conductor]] of any shape being traversed by a certain current density $\mathbf{J}$. Let's also consider a tiny cylinder aligned with $\mathbf{J}$ of height $l$ and cross-section $dS$. Using Ohm's second law, the resistance of the cylinder is
$$R=\rho_{R} \frac{dl}{dS}$$
There's also a potential difference $dV$ between the top and bottom of the cylinder, so we can also apply the first law to it
$$dV=RdI=\rho_{R} \frac{dl}{dS}dI$$
But $dV=E\ dl$ and $dI=J\ dS$ (with $E$ the [[electric field]] described by that potential) so if we plug these in we get
$$E\ \cancel{ dl }=\rho_{R} \frac{\cancel{ dl }}{\cancel{ dS }}J\cancel{ dS }$$
$$E=\rho_{R}J$$
But these two have the same direction (locally), so we can extend this to vector form
$$\boxed{\mathbf{E}=\rho_{R}\mathbf{J}}$$
and also in an inverse form
$$\boxed{\mathbf{J}=\sigma_{C}\mathbf{E}}$$
where $\sigma_{C}=1/\rho_{R}$ is the [[electrical conductivity]] of the material. This is an important relation because it shows that ohmic conductors show linear behavior regarding current flow when subject to electric fields.