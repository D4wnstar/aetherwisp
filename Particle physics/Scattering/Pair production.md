---
wiki-publish: true
aliases:
  - electromagnetic shower
---
The **pair production** is a high-[[energy]] phenomenon in which an [[Electric charge|electrically neutral]] [[boson]] "decays" to simultaneously generate a [[Particle|particle]] and its [[Antiparticle|antiparticle]]. Though it may look like one, pair production is not a type of [[particle decay]], but rather a [[particle scattering]]. This is because pair production must be "activated": it requires the input of an external field like an [[Electromagnetism|electromagnetic field]] in order to happen, as it is necessary to conserve [[invariant mass]]. As such, it only occurs in matter and is a form of [[radiation-matter interaction]].
### Electron-positron pair production
The most common type of pair production is a [[photon]] scattering into an [[electron]]-[[Electron|positron]] pair. The particle process is
$$\ce{X}+\gamma\to \ce{X}+e^{-}+e^{-}$$
where $\ce{X}$ is an [[atom]], [[Atomic nucleus|nucleus]] or generally some charged object that can provide an electromagnetic field to trigger the production and take some recoil to conserve energy. Assuming the recoil's energy is negligible due to the large [[mass]] of $\ce{X}$, we can say that all of the photon's energy is transferred into the pair. Since electrons are not massless, must at the very least carry two electron [[Relativistic energy|rest energies]] worth of energy to create the two:
$$E_{\gamma}\geq2m_{e}c^{2}$$
Then, $2m_{e}c^{2}$ is the [[threshold energy]] of the process. If the mass of $\ce{X}$ can't be ignored (call it $M$), then the threshold is increased to
$$E_\text{tr}=2m_{e}c^{2}\left( 1+ \frac{m}{M} \right)$$

:::image
![[Feynman diagram Pair production electron-positron|80%|center]]
[[Feynman diagram]] of the electron-positron pair production. Note the influence of the external atom/nucleus.
:::

The [[cross section]] of pair production can be quite complicated if calculated properly through quantum electrodynamics. The general behavior is that it is zero beneath the threshold energy (of course), then increases rapidly until it starts to slow down. Eventually the growth nearly stops and moves asymptotically towards a top value.

:::
![[Diagram Pair production cross section]]
The cross section of electron-positron pair production.
:::

Electron-positron pair production cross section is known to go like $\sim Z^{2}$, meaning larger helper atoms/nuclei $\ce{X}$ make pair production quadratically more likely.
#### In detectors
Pair production is a useful process to use in a [[detector]] to detect high-energy photons. The energy of the pair products is deterministic, meaning it's guaranteed to be half-and-half of the photon's original energy. Thus, the electrons can be measured by any conventional detector for charged particles and, if both are detected simultaneously in close proximity, it is possible to determine that they must've come from a pair production. Then, the sum of the kinetic and rest energies of the pair gives the photon energy:
$$E_{\gamma}=E_{e^{-}}+E_{e^{+}}=2m_{e}c^{2}+K_{e^{-}}+K_{e^{+}}$$
#### Cascade processes
Pair production has a notable relation to [[bremmstrahlung]]. In matter, it is possible to prove that [[Beer-Lambert law|Beer-Lambert absorption coefficient]] $\mu _\text{PP}$ due to pair production is related to its [[Stopping power|radiation length]] $L_{R}$ by
$$\mu _\text{PP}=\frac{7}{9} \frac{1}{L_{R}}$$
The absorption coefficient is the inverse of a mean path length
$$\lambda _\text{PP}=\frac{1}{\mu _\text{PP}}=\frac{9}{7}L_{R}$$
Recall what $\lambda _\text{PP}$ and $L_{R}$ mean:
- $\lambda _\text{PP}$ is the distance over which a beam of photons is suppressed by a factor of $1/e$ due to pair production.
- $L_{R}$ is the distance over which an electron reduces its energy by a factor of $1/e$ due to bremmstrahlung.

The two things are clearly related, both being absorption coefficients for one of the two elements involved in the process. But more importantly, they are almost equal. As a crude approximation, we can say $9/7\simeq 1$ and
$$\lambda_{PP}\simeq L_{R}=\lambda$$
In this context, the photons lose energy at the same rate as the electrons/positrons. This is an interesting because think of what this means:
1. The original photon travels $\lambda$ and pair produces an electron-positron pair.
2. The electron and positron separately travel $\lambda$ and emit a high-energy photon due to bremmstrahlung.
3. The photon travels $\lambda$ and pair produces an electron-positron pair.
4. The pair products travel $\lambda$ and emit a high-energy photon due to bremmstrahlung.
5. And so on.

Basically, a chain reaction occurs were a pair production leads to bremmstrahlung, which leads to pair production. Since each pair duplicates the number of particles in the mix, this *exponentially* escalates the number of photons/electrons that are scattering. This rapid formation of a great number of particles from just a photon is called an **electromagnetic shower**.

This chain reaction goes on until energy has been diluted enough to no longer support pair production. Indeed, since energy is conserved, the entire shower shares the original photon's energy. At every generation, the energy is split in half and, eventually, it'll drop below the threshold energy and block the process.

Assuming the initial photon energy $E_{\gamma}$ is $E_{0}$, the first created particles will have equally shared energies $E_{0}/2$. After $t$ radiation lengths, the shower consists of $N(t)=2^{t}$ particles, each with energy $E_{0}/2^{t}$. The maximum number of radiation lengths must be $t_\text{max}=x_\text{max}/L_{R}$, which provides the physical distance $x_\text{max}$ at which the shower stops. The energy of the final generation of the cascade will be
$$E(t_\text{max})=E_{C}=\frac{E_{0}}{2^{t_\text{max}}}\quad \Rightarrow \quad t_\text{max}=\frac{ 1}{\ln 2}\ln\left( \frac{E_{0}}{E_{C}} \right)$$
and so
$$\boxed{x_\text{max}=\frac{L_{R}}{\ln2}\ln\left( \frac{E_{0}}{E_{C}} \right)}$$
The maximum distance increases logarithmically with the original photon energy. This is nice because it means that showers are relatively limited in size and don't grow to huge proportions in high energy phenomena. This is useful for detectors that need to measure these, as they can be relatively compact (just a few radiation lengths, in general). These detectors can be used as [[calorimeter|calorimeters]] to measure high-energy photons and electrons.