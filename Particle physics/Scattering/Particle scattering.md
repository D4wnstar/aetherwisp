---
wiki-publish: true
---
**Particle scattering**, specifically in the context of particle physics, is [[scattering]] that occurs between [[particle|particles]]. Particles are considered to be [[quantum regime|quantum objects]], which makes this a form of quantum scattering, and often they are also considered to be [[Lorentz transformation|relativistic]]. As such, rigorously solving particle scattering behavior can be incredibly complex. Moreover, partly due to quantum physics and partly due to the minuscule scale, particle scattering is a largely [[random]] phenomenon, speaking of the [[probability]] of scattering more so than the certainty of it. Finally, due to [[wave-particle duality]], the participating particles can also be considered [[wave|waves]].

The typical particle scattering process (or reaction) looks like this:
$$a+b\to c+d$$
The letters represent the particles, with $a$ and $b$ being the incident particles and/or the target and $c$ and $d$ being the reaction products. $c$ and $d$ may very well be the same as $a$ and $b$, albeit in a different state. This is just an example of a two-particle interaction resulting in just as many particles. It's absolutely possible for there to be more inputs and outputs to the reaction, and for the number of inputs and outputs to differ from one another.

Particle scattering is ubiquitous. It's the foundation of many physical phenomena that we know, such as the color of the sky ([[Rayleigh scattering]]), and it is a fantastic experimental tool to probe the structure of particles, both as a whole and their internals. High-energy particle scattering is artificially created using a [[particle accelerator]], specifically a **collider**. In colliders specifically, you don't have a single incident particle. Rather, it's an entire **particle beam** being aimed at a **target**, with each particles in the beam being referred to as a **projectile**. The target maybe stationary or moving, with the most common moving targeting being another particle beam going in the opposite direction and made to collide.

Particles involved in scattering may be elementary particles like [[electron|electrons]], composite particles like [[proton|protons]] or even entire [[Atomic nucleus|nuclei]], [[atom|atoms]] or [[ion|ions]].

Particle scattering is often explained through [[Diagramma di Feynman|Feynman diagrams]], which are standardized schematic representations of particle scattering. Being entire diagrams, they can carry much more information than a simple mathematical representation, which is sorely needed given the complexity of many-particle interactions.
### Elastic scattering
Particle scattering is elastic when [[kinetic energy]] is conserved (but may be redistributed) and the incident particles do not change in the process. A typical elastic process reads
$$a+b \rightarrow a'+b'$$
where $a'$ and $b'$ are primed just for visual clarity, and are otherwise identical to $a$ and $b$. $b$ is assumed to remain in its ground state, but nevertheless absorb some [[Linear momentum|momentum]] through its recoil.

![[Diagram Particle scattering elastic|60%|center]]

In the context of using scattering for probing the structure of particles, the [[wavelength]] of the incident wave-particle must be smaller than the length scale of the target. We can determine a range by invoking the [[Disuguaglianza di Heisenberg|Heisenberg inequality]]
$$\Delta x\Delta p\geq \frac{\hbar}{2}$$
The momentum is provided by the [[de Broglie formula]]
$$\bar{\lambda}=\frac{\lambda}{2\pi}=\frac{\hbar}{p}\quad\Rightarrow \quad p=\frac{\hbar}{\bar{\lambda}}$$
where $\bar{\lambda}$ is the reduced de Broglie wavelength. If we take the error on momentum to be the same scale as the momentum itself ($p=\Delta p$, not unreasonable for such a small scale), we get
$$\Delta p=p=\frac{\hbar}{\bar{\lambda}}\geq \frac{\hbar}{2\Delta x}\quad\Rightarrow \quad \bar{\lambda}\leq2\Delta x$$
So the reduced wavelength must be in the order of the spatial uncertainty. Recalling that the energy of a wave $E=pc$, we can also write
$$E=pc\geq \frac{\hbar c}{2\Delta x}$$
If we take a $\Delta x$ of a few femtometers (typical radius of the atomic nucleus), we get something between 10 and 100 [[Electronvolt|MeV]]. If we go further and take the [[charge radius]] of an individual proton (0.84 fm) we get just over 100 MeV. To go even deeper and probe the internals of single protons, the energy needs to go even higher, in the order several GeV[^1].
### Inelastic scattering
Particle scattering becomes inelastic when the kinetic energy transferred from $a$ to $b$ results in $b$ [[State transition|transitioning]] into an excited state $b^{*}$. $b^{*}$ then [[particle decay|decays]] into its ground state, emitting a particle or splitting into two or more new particles. Here it splits into $c$ and $d$. In symbols:
$$a+b\ \rightarrow\ a'+b^{*}\ \to\ a'+c+d$$

![[Diagram Particle scattering inelastic 1|60%|center]]

In inelastic scattering, it's also possible for the projectile $a$ to be absorbed by the target $b$ in order to fuse into one or more new particles, such as this:
$$a+b\to c+d+e$$

![[Diagram Particle scattering inelastic 2]]

This is especially common in beam-on-beam collisions in particle colliders (it's also the end goal, generally speaking).

In an experimental setting, if the original projectile $a'$ is the only particle that's detected from the scattering, then it's said to be **inclusive**. If all of the scattering and decay products are detected, it's said to be **exclusive**. Of course, if the projectile is absorbed, the scattering can't be inclusive[^2].

[^1]: Unfortunately, I can't give a specific $\Delta x$ to prove this numerically. Protons are [[hadron|hadrons]]; that's to say they are made of [[Quark|quarks]]. So you might ask: how big is a quark? And the answer is: nothing at all. Quarks, to our understanding, have no size, they are point-like. All experimental data seems to suggest so. So the very concept of size and size uncertainty stops making sense at the quark scale. The best that I can give you is "less than 0.84 fm".

[^2]: If this terminology seems horribly confusing and in reverse, then I'm sorry. It's just how it was defined, and you are not alone in confusion. The terms are the way they are because they are talking about the *processes*, not the particles. In an inclusive product, you detect only one particle. As such, there's an entire host of possible scatterings that could lead to this outcome. Then, since you lack the information needed to pinpoint exactly what happened, you *include* all possible processes that could've happened. Similarly, if you manage to detect absolutely everything, then there's no room for debate: there's one and only one process that could've happened and you can *exclude* every other. You might ask why even bother with inclusive scatterings then. The answer is that sometimes you only care about one aspect of a scattering and can ignore everything else, but in many other cases, it's purely down to the fact that detecting subatomic particles is *incredibly hard*, so sometimes you just don't get to detect everything regardless of whether you like it or not. See [here](https://physics.stackexchange.com/questions/1217/whats-the-difference-between-inclusive-and-exclusive-decays) for a discussion.
