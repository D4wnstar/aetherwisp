---
wiki-publish: true
aliases:
  - resonance particle
---
A **particle resonance** is a sharp, localized peak in the [[cross section]] of a [[particle scattering]] associated with the presence of an extremely short-lived [[particle]] simply called a **resonance particle**. The phenomenon is described by the [[Breit-Wigner distribution]].

Resonances are incredibly short-lived, usually no more than $10^{-23}$ seconds of [[mean lifetime]].
### History and discovery
As experimental instrumentation became better and better throughout the 20th century, measurements became quite precise, leading to the discovery of many new, quite curious particles. For instance, consider the [[particle scattering]]
$$\pi^{-}+p\to X\to \pi^{-}+p$$
between a negative [[pion]] and a [[proton]]. The end result is itself, meaning it's an elastic scattering, but there appeared to be an intermediate result. This was noticed due to an anomalous peak in the [[cross section]] of this interaction as a function of the [[invariant mass]]. There just happened to be an amount of energy that was *just right* to make the cross section spike to a much higher value: a [[resonance]].

![[Plot Pion-proton resonance]]

This peak of cross section indicated the presence of a new particle that was interacting as an intermediate piece. We don't *see* it, but we know it must be there. The [[mean lifetime]] must therefore be minuscule[^1].

When this was discovered, theorists started doing math. They found that the peak could be expressed as a correction of the usual [[Stationary state|energy eigenstate]] $E_{n}$:
$$E_{n}- \frac{i\Gamma}{2}\quad \text{where}\quad \Gamma=\frac{\hbar}{\tau}$$
The quantity $\Gamma$ was called the **[[Breit-Wigner distribution|resonance width]]** or **decay width**. This name will be clearer later. $\tau$ is the mean lifetime of the particle associated with the resonance. Clearly then, tiny lifetimes meant huge deviations ($\Gamma$ is measured in [[Electronvolt|GeV]] for a reason). This specific distribution could be described by a local [[Breit-Wigner distribution]]
$$P(E)=\frac{1}{2\pi} \frac{\Gamma}{(E-E_{n})^{2}+ \Gamma ^{2}/4}$$
Then, $\Gamma$ represents the width of the distribution, which explains the "width" part. In a resonance, $E_{n}=M_{0}c^{2}$ is the [[Relativistic energy|rest energy]] of the resonance particle. The "decay" part is because $\Gamma$ also essentially represents a "cross section of decay", meaning it shows how likely the decay of a particle is. Since $\Gamma$ spikes around resonances, it should be no one's surprise that they decay incredibly fast. In fact, we can apply the [[Fermi golden rule|second Fermi golden rule]] to it too
$$\Gamma \propto \frac{2\pi}{\hbar}\lvert \braket{ \psi_{f} | \mathcal{M}_{fi} | \psi_{i} }  \rvert^{2}\rho(E) $$
It can hence be used as a description of the instability of a particle. In this way, it echoes the [[Radioactive decay law|decay constant]] of nuclear physics. In fact, just like the decay constant, we can have a "total" decay width as the sum of all "partial" decay width of all possible decays:
$$\Gamma=\sum_{i}\Gamma_{i}$$
The ratio of a partial decay width and the total decay width is the formal, theoretical definition of the [[branching ratio]] for particles:
$$\text{BR}_{i}=\frac{\Gamma_{i}}{\Gamma}$$
Now that we know what a particle "looks like" mathematically, we can start doing things in reverse: get in the laboratory and scan the energy spectrum by manipulating the energies involved until you find spikes. When you do, a decay's preferred energy. Do this over a large number of energies and you'll find many, many peaks and valleys corresponding to all possible decays of the particle. Sum them all and you've got the total decay width.

This method is incredibly powerful. Since the Breit-Wigner distribution was discovered, it has become been the primary tool for new particle discovery, as resonances don't lie. In fact, even the famous [[Higgs boson]] was discovered through a resonance peak! In fact, it worked *too* well. From the '60s on, a *lot* of new particles were discovered and it started to get overwhelming. Particle physicists were essentially building up a new periodic table of particles (jokingly called the **particle zoo**) and seemed to be way too complex for all of these particles to be elementary. We needed a new way to categorize these and see if there was a common ground between most or all of them. This is what led Murray Gell-Mann down the [[eightfold way]].

[^1]: The particle $X$ is the neutral [[delta resonance]] $\Delta^{0}$, with an invariant mass of about 1232 MeV.