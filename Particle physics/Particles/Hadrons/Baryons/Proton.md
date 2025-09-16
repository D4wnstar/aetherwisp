---
wiki-publish: true
aliases:
  - antiproton
---
The **proton** $p$ is a [[baryon|baryonic]] [[hadron]] with positive [[electric charge]]. It is one of the two components of the [[Atomic nucleus|nucleus]] and therefore a fundamental part of [[matter]]. It is a [[baryon]] composed of two [[up quark|up quarks]] and one [[down quark]]. Its [[antiparticle]] is the **antiproton** $\bar{p}$.

| Property            | Value                                            |
| ------------------- | ------------------------------------------------ |
| [[Mass]]            | 938 [[Electronvolt\|MeV]]/[[Speed of light\|c]]² |
| [[Electric charge]] | 1 [[Elementary charge\|e]]                       |
| [[Spin]]            | 1/2                                              |
| [[Parity]]          | +                                                |
| [[Baryon number]]   | 1                                                |
| [[Strangeness]]     | 0                                                |
| [[Mean lifetime]]   | Stable                                           |
## Discoveries
### The antiproton
In 1955, the only particles that were known were the [[electron]], proton, [[neutron]], [[electron|positron]], both [[muon|muons]] and all three [[pion|pions]]. According to the [[Dirac equation]], all particles stood to have an antiparticle partner, something that seemed to be true given that the electron, muon and pion were all found to be have one. The only missing ones were the antiproton and antineutron. The antineutron would have to wait longer due to the inconvenience on electric neutrality, but they were assumed to be part of primary [[Cosmic ray|cosmic rays]].

The antiproton discovery was lead by Italian physicist Emilio Segrè and American physicist Owen Chamberlain at the **Bevatron** proton [[synchrotron]] in the US. The name "Bevatron" comes from "BeV", which at the time was a uniquely American spelling of [[Electronvolt|GeV]] (billion-electronvolts instead of gigaelectronvolts).

The goal of the experiment was to collide protons with a stationary copper target in the hopes of detecting the theoretically-possible [[Particle scattering|scattering]]
$$p+p\to p+p+p+\bar{p}$$
The issue wasn't getting the reaction itself to work (it's not *impossibly* rare): the issue was creating a [[detector]] that could distinguish $p$ and $\bar{p}$. Specifically, proton-proton collisions have a *very* large number of possible outcomes, the most common of which include the pion. For instance, the reaction
$$p+p\to \pi^{+}+\pi^{+}+\pi^{+}+\pi^{-}$$
is $10^{5}$ times more [[Probability|probable]] than the one we're looking for. If we were to rely on electric charge alone, then the swarm of $\pi^{-}$ (same charge of $-e$) would get in the way.

The solution was exploiting [[threshold energy]]. For the reaction we want, the threshold energy is
$$K_{p}=\frac{(4m_{p})^{2}-(2m_{p})^{2}}{2m_{p}}=6.53\text{ GeV}$$
If the energy of the projectile proton is *just* about $K_{p}$, the three produced protons and one antiproton would have considerably lower [[kinetic energy]] and thus speed than the pions. This difference can be used to differentiate the two.

Two detectors were used in the process:
1. A [[Tempo di volo|time of flight]] detector was used to measure the speed of the passing particle.
2. A [[Cherenkov radiation]] detector was placed shortly after to detect [[photon]] emission from particles going over the Cherenkov speed threshold, carefully designed to only activate the kind of speeds pions were expected to go at, but not those of antiprotons.

:::image
![[BevatronAntiprotonApparatus.png|400]]
An Italian diagram of the Bevatron apparatus. *Red*: Copper target. *Green*: Deflection magnets. *Yellow*: TOF detectors. *Pink*: Focusing magnets. *Light blue*: Cherenkov counters.
:::

Magnets were place in the middle to curve the beam, which automatically took care of getting rid of all positive charges. In short:
1. Protons hit the lead target and make a ton of noise ($p,\bar{p},\pi^{\pm},\pi^{0}$).
2. Positive and neutral particles ($p,\pi^{+},\pi^{+}$) are gotten rid of by a magnetic field. This leaves only $\bar{p}$ and $\pi^{-}$.
3. Time of flight detectors measure the speeds of the two, which we compare to expected values for $\bar{p}$ and $\pi^{-}$.
4. Cherenkov radiation further determines if incoming particles pass a certain speed  threshold, which only $\pi^{-}$.

Running the experiment, Segrè and Chamberlain detected about 60 events that met all expectations, a number coincidentally $10^{5}$ lower than pion detections: just like theory suggested. This provided empirical evidence that $\bar{p}$ did in fact exist.