---
wiki-publish: true
aliases:
  - gravity
  - gravitational potential
  - gravitational interaction
---
**Gravity**, more formally the **gravitational interaction**, is the [[fundamental interaction]] that governs the attraction between bodies with [[mass]]. The classical, Newtonian description of gravity states that it occurs through a [[gravitational field]] around a massive object. This force is described by the gravitational [[potential energy]]
$$U=-G \frac{m_{1}m_{2}}{r}$$
where $m_{1}$ and $m_{2}$ are the masses of the two interacting [[point mass|point masses]], $r$ is the distance between them and $G$ is the [[gravitational constant]]. The gravitational force is therefore
$$\mathbf{F}=-\nabla U=-G \frac{m_{1}m_{2}}{r^{2}}\hat{\mathbf{r}}$$
The modern theory of gravity is **general relativity**, which explains how the presence of mass curves [[spacetime]] and how gravitational forces are described through this curvature. It is currently not understood if and how gravity relates to quantum mechanics or if gravity is an exchange interaction mediated by a discrete elementary [[particle]] (a so-called *graviton*).

Gravity has infinite range, meaning it can affect objects at any distance.
### Coupling constant  
In the context of fundamental physics, gravity can be compared to the other three fundamental interactions. Starting from the gravitational constant, alongside the [[speed of light]] and the [[Planck constant|reduced Planck constant]], we can determine the [[Planck units]] of mass and length:
$$M_{P}=\sqrt{\frac{\hbar c}{G}}\simeq 1.2\times10^{19} \;\frac{\text{GeV}}{c^{2}}\simeq2.2\times 10^{-8}\text{ kg}$$
$$\lambda_{P}=\frac{\hbar}{M_{P}c}\simeq1.6\times10^{-35}\text{ m}$$
We can use this is as an order-of-magnitude estimate stating that the effects of gravity are negligible at scales far away from this units. For instance, it is fair to neglect the effects of gravity when dealing with objects of mass smaller than $M_{P}$ and farther than $\lambda_{P}$. It is only when masses start to exceed the Planck mass or distances start to be below the Planck length that gravity becomes significant.

Comparing the Planck mass with, for example, the mass of a [[proton]] $m_{p}=0.938$ GeV/c$^{2}$, we can see that protons are exceptionally light compared to the Planck mass. As such, it is fair to state that gravitational attraction of between protons is completely negligible unless the distance between them is *also* much smaller than $\lambda_{P}$.

As a general scale of "strength", we define the [[coupling constant]] of gravity as an dimensionless constant $\alpha_{G} \propto \mathcal{M}^{2}$, where $\mathcal{M}$ is a reference mass. The conventional definition of gravitational coupling constant is
$$\alpha_{G}(\mathcal{M}^{2})=\frac{G\mathcal{M}^{2}}{\hbar c}$$
When using the Planck mass this gives[^1]
$$\alpha_{G}(M_{P}^{2})=1$$
If we set $\mathcal{M}$ as the proton mass and compare it to the above, we get
$$\alpha_{G}(\sim1\text{ GeV})=\alpha_{G}(m_{p}^{2})=\frac{m_{p}^{2}}{M^{2}_{P}}\alpha_{G}(M_{P}^{2})\simeq10^{-39}$$
which is a tiny value. Indeed, this confirms the previous statement that gravity is negligible at scales much lower than $M_{P}$, not because the interaction ceases to exist, but because its strength in utterly tiny compared to the other interactions.

[^1]: Note that this value is down to convention. For instance, it may instead be set to $1/4\pi$ to mimic quantum electrodynamics equations, as $1/4\pi \simeq1/137=\alpha$, the [[fine-structure constant]]. What matters isn't the dimensionless coupling constant itself, but rather its ratio with the others. The value can be adjusted as long as all the other follow the same convention, thus ultimately canceling out the factor when taking their ratios.
