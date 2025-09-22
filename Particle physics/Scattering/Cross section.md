---
wiki-publish: true
aliases:
  - geometric cross section
  - differential cross section
  - Mott cross section
  - scattering center
---
The **cross section** $\sigma$ is a measure of the [[probability]] that a specific reaction will occur during a [[particle scattering|collision]] between two [[Particle|particles]]. It is *not* the probability itself. The cross section is a surface area, generally measured in [[barn]], that loosely represents the physical size of the target that an incident particle must hit in order for a collision to happen. The bigger the area, the more likely the collision.

The cross section is to an extent dependent on the [[kinetic energy]] of the particles that are colliding (more energy = higher cross section), but the most important factor is the [[fundamental interaction]] that's involved in the collision. Just knowing what interaction is involved is enough to provide an order-of-magnitude estimate of the cross section. For instance, [[strong interaction]] scatterings generally have $\sigma\sim10^{-27}\text{ m}^{2}=10\text{ b}$.

Some real-world geometric cross section values relevant in experimental physics:
- Proton-proton collision at 10 [[Electronvolt|GeV]]: $\sigma_{pp}(10\text{ GeV})\sim40\text{ mb}$.
- Proton-proton collision at 13 TeV: $\sigma_{pp}(13\text{ TeV})\sim110\text{ mb}$. 30 mb is elastic and 80 mb is inelastic. As of 2025, this is the peak energy in the Large Hadron Collider at CERN.
- Neutrino-proton collision at 10 GeV: $\sigma_{\nu p}(10\text{ GeV})\sim70\text{ fb}$.

Cross section is particularly significant to measure the [[Radioactive decay law|rate of production]] (in this case, frequency of collisions) in a [[particle accelerator]]: $R=N_{0}\sigma I$, where $N_{0}$ is the number of particles in the target and $I$ is the incident flux from the beam.
## Kinds
The definition of cross section is somewhat vague and allows for a number of interpretations. There are a handful of different kinds of cross sections that are worth knowing.
### Geometric cross section
**Geometric cross section** is the most basic kind of cross section. Consider a rectangular target of thickness $d$ and surface area $A$.

![[Diagram Cross section geometric|center]]

Now fire a beam at the target. Assume the size of the beam is large enough to cover the whole target. The beam contains point-like particles $a$ moving at velocity $\mathbf{v}_{a}$ with volume density $n_{a}$. Meanwhile, the target is made up of $N_{b}$ particles (say, [[atom|atoms]]) of volume density $n_{b}$. We call them **scattering centers** (the blue circles in the figure, assumed non-overlapping) and they are not point-like: their surface area perpendicular to the beam is called **geometric cross section** $\sigma_{b}$. When a incoming projectile hits a scattering center, it scatters. This section can be determined experimentally by measuring the number of particles being fired and how many of them scatter.

It's assumed that a scattering removes the particle from the beam, either because it's absorbed or simply because it's deflected away. As such, the number of scatterings is equal to the difference between beam particles going in and coming out of the target. Let $\dot{N}$ be the number of scatterings per unit time, called total count rate. The [[flux]] incident on the target area, that is, the number of particles hitting the target per unit time, is
$$\Phi_{a}=\frac{\dot{N}_{a}}{A}=n_{a}v_{a}\tag{1}$$
where $\dot{N}_{a}$ is the number of particles being input by the beam per unit time. The scattering rate then is
$$\dot{N}=\Phi_{a}N_{b}\sigma_{b}\tag{2}$$
where $N_{b}\sigma_{b}$ is the total surface of all scattering centers. $N_{b}$ can be expressed as $N_{b}=n_{b}Ad$. Inverting, we get the geometric cross section:
$$\boxed{\sigma_{b}=\frac{\dot{N}}{\Phi_{a}N_{b}}}$$
Geometric cross section can be divided elastic and inelastic components, each representing the probability of that kind of scattering. Their sum is the total cross section:
$$\sigma_{\text{tot}}=\sigma_{\text{el}}+\sigma_{\text{an}}$$
### Differential cross section
More often than not, due to limitations in the [[detector]] equipment, only a small fraction of all possible reactions are available. This suggests the usage of a more versatile form of cross section compared to the total geometric one.

Consider some detector of area $A_{D}$ at a distance $r$ and angle $\theta$ from the beam.

![[Diagram Cross section differential|center]]

The detector subtends a [[solid angle]] $\Delta\Omega=A_{D}/r^{2}$. The total count rate $\dot{N}$ depends will depend on the cross section, of course, but specifically for the cross section of an event that leads to the emission of a particle in that solid angle, since those are the only ones that'll be detected. To express this concept, we introduce the **differential cross section**
$$\frac{d\sigma}{d\Omega}$$
which is the cross section per unit solid angle. The total count rate will hence be proportional to the differential cross section over the subtended solid angle[^1]:
$$\dot{N}=\mathcal{L} \frac{d\sigma}{d\Omega}\Delta\Omega$$
where $\mathcal{L}$ is the [[Luminosity (particle)|luminosity]] of the beam-target pair.

We can go a step further: if we can also measure the [[energy]] of the collision, we can differentiate *again* and find the cross section per unit solid angle per unit energy:
$$\frac{d^{2}\sigma}{d\Omega dE'}$$
where $E'$ is the energy of the scattering product being detected (as opposed to $E$, the energy at the collision vertex itself). The total cross section is then the integral over both a whole [[sphere]] and the entire range of possible output energy:
$$\sigma_{tot}(E)=\int_{0}^{E'_{max}}\oint_{\text{sphere}} \frac{d^{2}\sigma}{d\Omega dE'}d\Omega dE'$$
### Mott Cross Section
The Mott cross section accounts for the [[spin]] of the electron and nucleus and their influence on scattering. It is given by
$$\left(\frac{d\sigma}{d\Omega}\right)_{\text{Mott}}=\left(\frac{d\sigma}{d\Omega}\right)_{\text{Rutherford}}\left[1-\beta^{2}\sin^{2}\left(\frac{\theta}{2}\right)\right]$$
where $\beta=v/c$. In the limit of negligible nuclear recoil and $\beta \rightarrow 1$:
$$\left(\frac{d\sigma}{d\Omega}\right)_{\text{Mott}}=\left(\frac{d\sigma}{d\Omega}\right)_{\text{Rutherford}}\cos^{2}\left(\frac{\theta}{2}\right)$$

The Mott cross section decreases more rapidly than the Rutherford cross section as $\theta$ increases.
## Theoretical prediction
The kinds of cross section presented above are shown in a very experimental-first light. However, cross section can, with some difficulty, be predicted from purely theoretical principles.

The interaction is described by a [[Hamiltonian]] $H_\text{int}$. The [[Physical system|system]] begins in a state $\psi_{i}$ and ends in a state $\psi_{f}$. The [[probability amplitude]] of this [[state transition]] is given by the [[matrix element]]
$$\mathcal{M}_{fi}=\langle \psi_{f}|H_{\text{int}}|\psi_{i}\rangle=\int\psi_{f}^{*}H_{\text{int}}\psi_{i}\ dE$$
Each particle occupies a volume $h^{3}$ in [[phase space]], using the [[Planck constant]], because of the [[Disuguaglianza di Heisenberg|uncertainty principle]]. Say the particle occupies a spatial volume $V$ and a momentum volume given by the thin spherical shell $p$ to $p+dp$, which yields $4\pi p^{2}dp$. Then, the total number of states this particle can be in is
$$dn(p)=\frac{4\pi p^{2}dp}{h^{3}}V$$
The energy is given by $dE=vdp$, so the final density of states is
$$g(E)=\frac{dn(E)}{dE}= \frac{4\pi p^{2}}{vh^{3}}V$$
These quantities allow us to find the reaction rate $W$ through **Fermi's second golden rule**:
$$W=\frac{2\pi}{\hbar}|\mathcal{M}_{fi}|^{2}g(E)$$
The reaction rate is normalized for one target particle, so using our former notation we can write it as
$$W=\frac{\dot{N}}{N_{a}N_{b}}$$
Using $(1)$ and $(2)$ this becomes
$$W=\frac{\sigma v_{a}}{V}$$
where $V=N_{a}/n_{a}$. Equating this with Fermi's golden rule lets us solve for $\sigma$:
$$\boxed{\sigma=\frac{2\pi}{\hbar v_{a}}|\mathcal{M}_{fi}|^{2}g(E)V}$$

[^1]: This is assuming that the differential cross section is constant over the solid angle. If not, integrate over $d\Omega$ instead.
