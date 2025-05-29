---
wiki-publish: true
aliases:
  - spontaneous emission
  - stimulated emission
---
A **two-level system** is a [[physical system]] with only two allowed [[energy]] levels. It is an idealized model that is useful to describe some phenomena, such as a [[qubit]], but it is not physically possible; see [[Microcanonical ensemble#Examples]] for an example of why.

This system is interesting because it highlights [[State transition|state transitions]] in the simplest possible system: you either go up to the higher-energy **excited state**, or go down to the lower-energy **ground state**. It is therefore useful to discuss the methods by which a system may undergo these transitions.
### Matter-radiation interaction
One notable use case is studying the impact of [[radiation]] on [[matter]] and how the two interact. Our two-level system can be seen as, for instance, a simplified form of an [[electron]] in an [[atom]], and radiation is taken to be [[Electromagnetic radiation|electromagnetic]]. We won't go over the exact details of interaction with the [[Electric field|electric]] and [[magnetic field|magnetic fields]]: we'll take for granted that absorption and emission are both quantized in the form of [[Photon|photons]].

![[Diagram Two-level system processes|100%]]

At a high level, there are three methods of interaction.
#### Spontaneous emission
At any given time, the excited state has a certain [[Probability|chance]] to de-excite spontaneously by releasing a photon. This process is called **spontaneous emission**. The energy of the photon is precisely the difference in energy between the excited and ground states:
$$\Delta E=\hbar \omega \quad\Rightarrow \quad \omega=\frac{\Delta E}{\hbar}$$
where $\omega$ is the [[Frequency|angular frequency]] of the photon, as given by the [[Planck formula]]. The amount of spontaneous emissions per unit time is given as
$$\dot{N}_{\text{exc}\to\text{gr}}(t)=A_{\text{exc}\to\text{gr}}N_\text{exc}(t)$$
where $A$ is some constant.
#### Absorption
A photon from the environment can be **absorbed** to cause the ground state to excite. The energy of the photon must be $\Delta E$. The amount of absorptions per unit time is given as
$$\dot{N}_{\text{gr}\to\text{exc}}(t)=B_{\text{gr}\to\text{exc}}N_\text{gr}(t)\rho(\omega)$$
where $B$ is some constant and $\rho$ is the density of energy states at frequency $\omega$.
#### Stimulated emission
Photons at a frequency $\omega$ from the environment can induce the emission of photons with the same frequency $\omega$ from the system. This process is called **stimulated emission**, and it is caused by [[resonance]]. The amount of stimulated emissions per unit time is given as
$$\dot{N}^{S}_{\text{exc}\to\text{gr}}(t)=B_{\text{exc}\to\text{gr}}N_{\text{exc}}(t)\rho(\omega)$$
where $B$ is a constant (different from absorption!) and $\rho$ has the same meaning as above.
### Equilibrium and spectrum
Assuming that the system is in [[thermal equilibrium]], we have
$$\dot{N}_{\text{gr}\to\text{exc}}(t)=\dot{N}_{\text{exc}\to\text{gr}}(t)+\dot{N}^{S}_{\text{exc}\to\text{gr}}(t)$$
or
$$B_{\text{gr}\to\text{exc}}N_{\text{gr}}(t)\rho(\omega)=A_{\text{exc}\to\text{gr}}\rho(\omega)+B_{\text{exc}\to\text{gr}}N_{\text{exc}}(t)\rho(\omega)$$
and so
$$\frac{N_{\text{exc}}(t)}{N_{\text{gr}}(t)}=\frac{B_{\text{gr}\to\text{exc}}\rho(\omega)}{B_{\text{exc}\to \text{gr}}\rho(\omega)+A_{\text{exc}\to\text{gr}}}$$

It can be proven that the ratio is exponential
$$\frac{N_{\text{exc}}(t)}{N_{\text{gr}}(t)}=e^{-\beta \hbar \omega}$$
where $\beta=1/k_{B}T$ with $k_{B}$ the [[Boltzmann constant]] and $T$ the [[temperature]]. Anyone who studied statistical mechanics will likely find this exponential very familiar: it's a Boltzmann factor. This then leads to
$$\rho(\omega)=\frac{A_{\text{exc}\to\text{gr}}}{B_{\text{gr}\to\text{exc}}e^{\beta \hbar \omega}-B_{\text{exc}\to \text{gr}}}$$
Now, if send temperature to infinity (equivalently, $\beta\to0$), the density of states should itself go to infinity (more thermal energy, more accessible states). But if $\beta\to 0$, then $e^{\beta \hbar \omega}\to1$, which means that the denominator in this limit is simply $B_{\text{gr}\to\text{exc}}-B_{\text{exc}\to\text{gr}}$. But if we want $\rho(\omega)$ to blow up to infinity and the numerator is a finite real constant, then it must be that the denominator tends to zero, hence
$$B_{\text{gr}\to\text{exc}}-B_{\text{exc}\to\text{gr}}=0\quad\Rightarrow \quad B_{\text{gr}\to\text{exc}}=B_{\text{exc}\to\text{gr}}\equiv B$$
Thus, the absorption and stimulated emission must be the same, with the temperature dependence being expressed by the Boltzmann factor $e^{\beta \hbar \omega}$. Here you can see why stimulated emission is necessary: we wouldn't be able to reconcile the high temperature behavior if it didn't exist. Renaming $A_{\text{exc}\to\text{gr}}\equiv A$, we call these two constants $A$ and $B$ the **[[Einstein coefficients]]**[^1].

With this knowledge, we can write
$$\rho(\omega)=\frac{A}{B}\left( \frac{1}{e^{\beta \hbar \omega}-1} \right)$$
and we need some way to figure out what the ration $A/B$ is. To do so, we'll expand the exponential with its [[Serie esponenziale|series]], up to the first two terms: $e^{\beta \hbar \omega}\simeq1+\beta \hbar \omega$. Then
$$\rho(\omega)\simeq \frac{A}{B} \frac{1}{\beta \hbar \omega}$$
This is a fine approximation for low frequencies. But another fine approximation for these frequencies is the classical Rayleigh-Jeans law:
$$\rho(\nu)d\nu=\frac{8\pi \nu ^{2}}{\beta c^{3}}d\nu$$
Converting to angular frequency ($\omega=\nu/2\pi$) yields
$$\rho(\omega)d\omega=\frac{\omega ^{2}}{\beta \pi ^{2}c^{3}}d\omega$$
We can thus state
$$\frac{\omega ^{2}}{\beta \pi ^{2}c^{3}}=\frac{A}{B} \frac{1}{\beta \hbar \omega}\quad\Rightarrow \quad \frac{A}{B}=\frac{\hbar\omega^{3}}{\pi ^{2}c^{3}}$$
and if we plug this back into $\rho(\omega)$, we get a familiar face:
$$\boxed{\rho(\omega)=\frac{\hbar \omega ^{3}}{\pi ^{2}c^{3}} \frac{1}{e^{\beta \hbar \omega}-1}}$$
This is the **Planck radiation law**, which was already found through the quantum statistical treatment of the [[black body]]. Here we found it (somewhat loosely) in an entirely abstract, general system by only looking at the microscopic behavior of matter. Not only does this confirm the validity of the quantum statistical treatment, it also validates the choice of three interaction methods from before.

Remember that this is only valid at thermal equilibrium: outside of equilibrium, we can't make our initial assumptions on balanced absorption and emission rates.

[^1]: It was Einstein who proposed the existence of stimulated emission.
