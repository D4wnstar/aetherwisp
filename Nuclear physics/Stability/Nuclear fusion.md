---
wiki-publish: true
---
**Nuclear fusion** is the process by which two [[Atomic nucleus|atomic nuclei]] fuse together, creating a new combined nucleus. Spontaneous nuclear fusion is an extremely high-[[energy]] process, generally requiring very high [[temperature|temperatures]] and [[pressure|pressures]] to occur, but it is ultimately responsible for the [[nucleosynthesis]] of most [[chemical element|chemical elements]] below iron.
## Energy
Nuclear fusion is not always spontaneous even in extreme conditions. The process is energetically advantageous as long as the [[binding energy]] per [[Atomic nucleus|nucleon]] of the daughter nucleus is greater than that of the parent nuclei. This holds up to iron ($A\simeq56$). In other words, the [[Q value]] of fusion is positive in all cases that lead to a fused nucleus with $A\simeq 56$ or less. Above this threshold, the $Q$ value goes negative and the process stops being spontaneous, irrespective of ambient conditions.

It is still possible for fusion to produce nuclei heavier than iron, meaning when the $Q$ value is negative, but it requires an external energy input. As such, this kind of nuclear fusion is rare, short-lived and often explosive, typically occurring in events like [[Supernova|supernovae]].
## Processes
Nuclear fusion can occur in several ways, depending on the feedstock that activates it. In the following, it is assumed that fusion is occurring in a gas cloud at temperature $T$, such as within the core of a [[star]].
### Proton–proton chain
The simplest process is the **proton-proton chain** (or **PP chain**) and occurs at relatively low temperatures and pressures. It consists of fusing four proton atoms into a helium atom, via the chain of nuclear reactions
$$\ce{_{1}^{1}H + _{1}^{1}H -> ^{2}_{1}D + e^{+} + \nu_{e}}$$
$$\ce{_{1}^{2}D + _{1}^{1}H -> ^{3}_{2}He + \gamma}$$
$$\ce{^{3}_{2}He + _{2}^{3}He -> ^{4}_{2}He + _{1}^{1}H + _{1}^{1}H}$$
where $e^{+}$ is a [[Electron|positron]] and $\nu_{e}$ is an [[Neutrino|electronic neutrino]]. The chain involves neutrinos, which have extremely small [[Cross section|cross sections]] and thus dampen the efficiency of the rest of the cycle.

This is the type of process that stars use for most of their lives, as well as the primordial stars created shortly after the [[Big Bang]]. The mass–energy conversion efficiency of this process is $\epsilon\propto\rho T^{4}$[^1] and is about 0.7 %.
### CNO cycle
Another process is the **CNO cycle**, which also uses other elements such as nitrogen, oxygen or carbon, but only as catalysts. In fact, the net amount of these elements before and after the cycle is the same. The CNO cycle requires higher pressure and temperatures, but it is many orders of magnitude more efficient than the proton–proton chain. The efficiency of this process is $\epsilon\propto\rho T^{17}$.

Both processes coexist in almost all stars, provided that their [[metallicity]] is sufficiently high, but usually one dominates over the other. For stars with central temperatures $<2\times10^{7}\,\mathrm{K}$ the PP chain usually dominates, above which the CNO cycle dominates.
### Triple-alpha cycle
A much more energetic process is the **$3\alpha$ cycle**, which involves three $^{4}\mathrm{He}$ nuclei and an intermediate reaction with $^{8}\mathrm{Be}$ to form a $^{12}\mathrm{C}$ nucleus. This is a three-body cycle and therefore depends on the cube of the density, not the square. It holds that $\epsilon\propto\rho^{2}T^{40}$.
### Other cycles
There are further cycles for heavier atoms, which are triggered if the star’s temperature is sufficiently high. In order
$$\text{hydrogen}\;\rightarrow\;\text{helium}\;\rightarrow\;\text{carbon}\;\rightarrow\;\text{neon}\;\rightarrow\;\text{oxygen}\;\rightarrow\;\text{silicon}$$
Burning silicon produces nickel, which [[Nuclear decay|decays]] into iron and is therefore an inefficient reaction that consumes more energy than it produces, which is why the chain stops there.
## Minimum conditions
Consider two charged particles $q_{1}$ and $q_{2}$ of mass $m$ colliding with each other at velocity $v$. The minimum distance they can reach due to the potential barriers is given by the [[Electromagnetism|Coulomb law]]
$$r=\frac{2q_{1}q_{2}}{mv^{2}}$$
(in the cgs system the term $4\pi\epsilon_{0}$ does not appear). To bring this distance below the nuclear radius ($\sim10^{-15}\,\mathrm{m}$), the velocities would have to be enormous. They are so high, in fact, that they are not even found in the center of a star such as the Sun.

Fortunately, quantum mechanics allows a way to bypass the potential barrier: **quantum tunnelling**. For an electromagnetic barrier of this kind, the transmission probability is
$$P_{\text{tunnel}}\propto\exp\!\left(- \frac{2\pi^{2}r}{\lambda}\right)$$
with $\lambda$ the [[de Broglie formula|de Broglie wavelength]]. Since $\lambda$ decreases with $p$ and therefore with $v$, this probability increases with increasing velocity.

In the context of stars, or any gas at a certain temperature $T$, we can assume that the velocities of the stellar nuclear particles are distributed according to a [[Maxwell-Boltzmann distribution]]. The probability of having a sufficiently high velocity is shown to have the form
$$P_{\text{maxwell}}\propto\exp\!\left(- \frac{mv^{2}}{2k_{B}T}\right)$$
with $k_{B}$ the [[Boltzmann constant|Boltzmann constant]]. The probability of total fusion is therefore the product $P_{\text{tunnel}}P_{\text{maxwell}}$. It is shown that the probability is maximized for velocities
$$v=\left(\frac{2\pi q_{1}q_{2}k_{B}T}{\hbar m}\right)^{1/3}$$
with $\hbar$ the [[Planck constant|reduced Planck constant]]. The minimum conditions to ignite a fusion reactor in the core are then
$$\boxed{P_{\text{reaz}}\propto \exp\!\left(- \left( \frac{T}{T_{0}} \right)^{-1/3}\right)}$$
$$T_{0} = \left( \frac{3}{2} \right)^{3}\left( \frac{4\pi^{2}q_{1}q_{2}}{h} \right)^{2}\left( \frac{m}{k_{B}} \right)$$
where $T_{0}$ is a scaling temperature. $m$ in this case is the reduced mass $m=m_{1}m_{2}/(m_{1}+m_{2})$, because the nucleus is composed of different particles (hydrogen, helium, etc…).
### Considerations
From this equation some considerations can be made:
- $T_{0}$ grows as $m(q_{1}q_{2})^{2}$, which means it grows as $AZ^{4}$ in terms of [[Atom|atomic mass number]] and [[Atom|atomic number]]. The minimum temperature rises very rapidly using atoms heavier than hydrogen.
- Even for hydrogen $T_{0}$ is very high: with $q_{1}=q_{2}=e$ and $m=m_{p}/2$ one has $T_{0}=3.8\times10^{10}\,\mathrm{K}$. Few stars have such high internal temperatures. The Sun, for example, has an internal temperature of $1.5\times10^{7}\,\mathrm{K}$. Fusion therefore occurs with very low probability and, therefore, very slowly.
- The reaction efficiency grows very rapidly with temperature. Higher-temperature reactors will produce exponentially more energy than lower-temperature reactors.
## Element formation
In the context of astrophysics and cosmology, it is convenient to classify the elements of the periodic table by their origin. The very light elements, $H$, $^{2}\mathrm{H}$, $^{3}\mathrm{He}$, $^{4}\mathrm{He}$ and $^{7}\mathrm{Li}$ all have **cosmological origin** and thus exist since the Big Bang. These are the elements that initiate stellar nuclear fusion.

Elements are then defined as **primary elements** those that are created by nuclear fusion directly from cosmological origin elements, while **secondary elements** are those created from already existing heavier elements (such as the primary elements produced by less energetic cycles). For example, $^{4}\mathrm{He}$ is a primary element (in addition to being cosmological) because it is produced from $^{1}\mathrm{H}$ in the PP chain, while $^{14}\mathrm{N}$ is a secondary element because it is produced from $^{12}\mathrm{C}$ in the CNO cycle.

Secondary elements are pushed up to around $^{56}\mathrm{Fe}$, beyond which spontaneous nuclear fusion does not occur. Consequently, heavier elements must be formed through more energetic and efficient processes, such as the [[s-process]] or the [[r-process]], or faster and more violent, such as a [[Supernova|Supernova]].

[^1]: If the generation of total energy depends on $\rho^{2}$, as is usually the case, the generation of energy per unit mass $\epsilon$ depends only on $\rho$.