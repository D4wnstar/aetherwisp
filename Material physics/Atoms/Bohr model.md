---
wiki-publish: true
---
The **Bohr model** is a classical model of the structure of the [[hydrogen atom]] developed in 1913. It accurately describes the experimental behavior of hydrogen and its [[Isotopo|isotopes]], but it is not a quantum model and is therefore not extendable to more complex systems, such as [[many-electron atom|atoms with more than one electron]].

![[Schema Modello di Bohr|50%|center]]
### Postulates
The Bohr model is a fundamentally classical description, which describes [[electron|electrons]] as "orbiting" the nucleus. We know now that this is not true due to the quantum nature of electrons, but at the time it was still uncertain. Despite this, the model is based on three postulates, which essentially "mimic" quantum behavior before said behavior was even fully understood[^1]:
1. Only a discrete set of [[circle|circular]] orbits is allowed. These orbits are called [[stationary state|stationary states]].
2. Electrons in stable orbits do not [[radiation|radiate]]. The emission or absorption of radiation is related solely to [[state transition|state transitions]] from one orbit to another.
3. The [[angular momentum]] of the circular orbits admits only discrete values, as given by the formula $L=n\hbar$, where $n\in \mathbb{N}$ and $\hbar$ is the [[Planck constant|reduced Planck constant]].

The origin of these postulates is the discrepancy between experiment and theory of the time regarding electron radiation. It was well known that accelerating [[Electric charge|charges]] emit [[electromagnetic radiation]], but it was also a fact that stable atoms presented no radiation whatsoever. Since orbiting electrons must have *some* acceleration (at least centripetal acceleration), the lack of radiation was concerning and highlighted some flaw in the theory. Moreover, the frequencies of light that were seen being emitted by the hydrogen atom were very specific discrete values. These issues would eventually be solved by quantum theory, but before then, Bohr set these postulates up to enforce the undeniable experimental evidence.
### Derivation
The model is essentially one charged particle (the electron) being attracted by [[Interazione elettromagnetica|Coulomb's law]] to another (the nucleus). The electron charge is the [[Elementary charge]] $-e$ and the nucleus has atomic number $Z$ (in case of actual hydrogen $Z=1$). Assuming the electron, of mass $m_{e}$, is orbiting at a distance $r$ with tangential speed $v$, the Coulomb force must match the centrifugal force[^2]:
$$\underbrace{\frac{Ze^{2}}{4\pi\varepsilon_{0}r^{2}}}_{\text{potential}}=\underbrace{\frac{m_{e}v^{2}}{r}}_{\text{kinematics}}$$
This is only true if the mass of the electron is much less than that of the nucleus, $m_{e}\ll m_\text{nucleus}$. This is because in this context, the electron is so light we can ignore its effects on the nucleus, which we assume to be stationary and unmoving (with respect to some [[frame of reference]]).

Postulate three says $L=m_{e}vr=n\hbar$, so with some rearrangement we can find the electrons speeds in the allowed orbits:
$$v=\frac{Ze^{2}}{4\pi\varepsilon_{0}n\hbar}$$
Substitute this back into the force equation above and we can extract the allowed radii $r$ for the orbits too:
$$\boxed{r=\frac{4\pi \varepsilon_{0}n^{2}\hbar ^{2}}{Ze^{2}m_{e}}}$$
For hydrogen ($Z=1$) in the ground state ($n=1$), the value we get is known as the **[[Bohr radius]]**:
$$\boxed{a_{0}=\frac{4\pi \varepsilon_{0}\hbar ^{2}}{e^{2}m_{e}}}$$
Knowing these, we can find the [[kinetic energy|kinetic]] and [[potential energy]] $T$ and $V$:
$$T=\frac{1}{2}m_{e}v^{2}=\frac{m_{e}}{2\hbar^{2}} \left(\frac{Ze^{2}}{4\pi\epsilon_{0}}\right)^{2}\left(\frac{1}{n^{2}}\right),\qquad V=- \frac{Ze^{2}}{4\pi \varepsilon_{0}r}=- \frac{m_{e}}{\hbar^{2}}\left(\frac{Ze^{2}}{4\pi\epsilon_{0}}\right)^{2}\left(\frac{1}{n^{2}}\right)$$
Sum these two and we get the total energy, called the **Bohr energy**:
$$\boxed{E=T+V=- \underbrace{\frac{m_{e}}{2\hbar^{2}}\left(\frac{Ze^{2}}{4\pi\epsilon_{0}}\right)^{2}}_{\text{Rydberg energy}}\left(\frac{1}{n^{2}}\right)=-\frac{E_\text{Ryd}}{n^{2}}}$$
The constant $E_\text{Ryd}$ is known as the [[Rydberg constant|Rydberg energy]]. In fact, this constant was discovered decades before by [[Parameter estimation|fitting]] purely experimental data and one immediate success of the Bohr model was exactly this: explaining precisely where the Rydberg constant comes from. Using this fact, we can find a theoretical expression for the Rydberg constant (setting $Z=1$ because it's only valid for hydrogen):
$$E_\text{Ryd}=hcR_{\infty}\quad\Rightarrow \quad R_{\infty}=\frac{E_\text{Ryd}}{hc}=\frac{1}{2\pi\hbar c} \frac{m_{e}}{2\hbar ^{2}} \left( \frac{e^{2}}{4\pi \varepsilon_{0}} \right)^{2}=\frac{m_{e}}{4\pi c\hbar ^{3}} \left( \frac{e^{2}}{4\pi \varepsilon_{0}} \right)^{2}$$
We call this version of the constant $R_{\infty}$, where the infinity symbol denotes that we are in the approximation of $m_{e}\ll m_\text{nucleus}$, which is like saying $m_\text{nucleus}\to \infty$ if we keep $m_{e}$ fixed. This is already a very good approximation of the real value, but we can do better by shedding the infinite nuclear mass.

If we instead claim that the nucleus has finite mass, we have to accept that it also (slightly) moves due to the attraction of the electron. As usual for many body systems, we look at the [[center of mass]], with reduced mass
$$\mu=\frac{m_{e}m_\text{nucleus}}{m_{e}+m_\text{nucleus}}$$
The proof won't be given here, but the system can be solved again with both bodies moving to find that the only difference between $R_{\infty}$ and this more precise $R_{M}$ is
$$R_{M}=\frac{\mu}{m_{e}}R_{\infty}$$
Basically, we just exchanged $m_{e}$ for $\mu$ is the formula. When setting $m_\text{nucleus}$ to the mass of the [[proton]], the value we get for $R_{M}$ is essentially perfect: just $0.003$% shy of the experimental value. 

The discovery of this origin for the Rydberg constant led to many more questions: why are the orbits and their energy quantized with an integer $n$? The answer would have to wait the development of quantum mechanics and the quantum model of the [[hydrogen atom]].

[^1]: I want to make it very clear here that this is *not* a quantum model. The fact that all of these postulates talk about (and link to) quantum concepts is entirely because Niels Bohr saw something that no one else in his time did. In fact, concepts such as "stationary state" and "discrete angular momentum" have been *coined* by Bohr specifically through this very model.

[^2]: They have to, otherwise the orbits won't be stable circles.