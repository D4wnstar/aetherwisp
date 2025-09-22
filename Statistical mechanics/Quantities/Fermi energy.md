---
wiki-publish: true
aliases:
  - Fermi momentum
  - Fermi velocity
  - Fermi wavevector
  - Fermi temperature
---
The **Fermi energy** $E_{F}$ is the [[energy]] of the highest occupied [[stato|state]] of a [[Physical system|system]] of [[Fermion|fermions]] at zero [[temperature]]. It corresponds to the zero-temperature [[chemical potential]] of the system, so that $\mu=E_{F}$ when $T=0$. At nonzero temperatures, thermal effects add energy to the fermions, so the Fermi energy is no longer well-defined. However, for temperatures far below the Fermi temperature (see below), it remains a good approximation, $\mu\simeq E_{F}$.

Since energy determines a [[Surface|surface]] in [[phase space]], the Fermi energy surface divides occupied states (inside) from unoccupied ones (outside). It is known as the [[Fermi surface]].
### Explanation
The [[Pauli exclusion principle]] prevents multiple fermions from occupying the same state. This causes the fermions to be "pushed apart" in different states, despite there not being any repulsive [[Potential|potential]]. This inherent repulsive behavior is characteristic of fermions. Because of this repulsion, even at zero temperature, most fermions will be in excited states, as there can only be one in the ground state. This gives fermionic systems a certain irreducible amount of energy that cannot be removed even at zero temperature. The energy of the highest occupied state at zero temperature is known as the **Fermi energy**. This quantity can be derived from purely mathematical considerations.
### Related quantities
Several quantities can be derived from the Fermi energy. The **Fermi momentum** is $p_{F}=\sqrt{ 2mE_{F} }$, the **Fermi velocity** is $v_{F}=p_{F}/m$, the **Fermi wavevector** is $k_{F}=p_{F}/\hbar$. These are the [[Linear momentum|momentum]], velocity and [[Wavenumber|wavevector]] of the highest energy particle in the Fermi gas (i.e. the one whose [[kinetic energy]] is the Fermi energy). The wave vector can also be expressed from the particle density $n=N/V$ directly as $k_{F}=(3\pi ^{2}n)^{1/3}$.

The **Fermi temperature** is defined as $T_{F}=E_{F}/k_{B}$, where $k_{B}$ is the [[Boltzmann constant]]. It can be thought of as the temperature at which thermal effects become significant compared to quantum effects (specifically the Pauli exclusion principle). It is a useful metric to determine how "sharp" the [[Fermi-Dirac distribution]] is. At $T\ll T_{F}$, it is almost a [[Heaviside step function]] across $E_{F}$, but when $T\gg T_{F}$, it broadens to the point that there is no clear boundary and becomes indistinguishable from the [[Maxwell-Boltzmann statistic]].

:::image
![[Fermi-Dirac distribution at low temperatures.png]]
The Fermi-Dirac distribution at zero and low temperatures. From David Tong's lecture notes on statistical physics.
:::

Since the Pauli exclusion principles causes zero- and low-temperature fermions to be subject to [[degenerate pressure]], $T_{F}$ is also sometimes known as the **degeneracy temperature**, which is particularly important in later stages of [[Evoluzione stellare|stellar evolution]] when [[Stella|stars]] collapse into [[Nana bianca|white dwarfs]] (degenerate [[Electron|electron]] gas) or [[Stella di neutroni|neutron stars]] (degenerate [[neutron]] gas). This temperature is not necessarily very low: for instance, for electrons in metals, it is typically in the range of $\sim 10^{4}$ kelvins. In neutron stars, it is $>10^{7}$ kelvins.