---
wiki-publish: true
---
The **photoelectric effect** is a phenomenon in which [[electromagnetic radiation]] is absorbed by a material, leading to the [[ionization]] of an [[atom]] and the emission of a free [[electron]]. The incident [[electromagnetic wave]] ([[Photon]]) transfers enough [[kinetic energy]] to a [[electron shell model|valence electron]] to overcome its [[binding energy]] and break it out of the atom's [[potential energy|potential]] well.
### Mechanism
The photoelectric effect is best explained in the language of [[particle]] physics. The process can be schematized as
$$\gamma + \ce{X} \rightarrow \ce{X}^{+} + e^{-}$$
with $\ce{X}$ the [[chemical element]] involved. The photon must have more energy $E_{\gamma}$ than the binding energy of the electron $B_{e}$ for this process to occur. The electron will then have kinetic energy equal to the difference:
$$K_{e^{-}}=E_{\gamma}-B_{e}$$
In valence electron, $B_{e}$ is often 10-20 [[Electronvolt|eV]] so depending on the photon energy, it's likely it can be ignored. In that case, the electron picks up all of the photon's energy.

> [!quote]- In the vacuum
> The photoelectric effect cannot occur in the vacuum as that would violate [[invariant mass]] conservation. The process would be
> $$\gamma+e^{-}\to e^{-}$$
> The invariant mass $m_{0}$ in the start state is (in [[natural units]]):
> $$m_{0}^{2}=E^{2}-p^{2}=(m_{e}+E_{\gamma})^{2}-E_{\gamma}^{2}=m_{e}^{2}+E_{\gamma}^{2}+2m_{e}E_{\gamma}-E_{\gamma}^{2}=m_{e}^{2}+2m_{e}E_{\gamma}$$
> This must remain the same in the end state. But the only particle left is the electron, so the invariant mass in the end must be equal to electron's rest mass
> $$m_{0}^{2}=m_{e}^{2}$$
> Since $m_{e}^{2}+2m_{e}E_{\gamma}\neq m_{e}^{2}$, invariant mass is not conserved and this process is forbidden. The reason why it's allowed in matter is because the atom can recoil to conserve the energy.

The photoelectric [[cross section]] of a homogeneous material can be found to be
$$\sigma_{\text{PE}}\propto\left(\frac{m_{e}c^{2}}{E_{\gamma}}\right)^{3}Z^{5}$$
where $Z$ is the [[Atom|atomic number]] of the atom. The extreme dependence on the atomic number is immediately apparent: a fifth-power! Heavy atoms are then enormously more likely to be subject to the photoelectric effect. Meanwhile, from the inverse dependence on photon energy, we can deduce that this effect is prevalent only at low energies[^1]. The ideal condition to make the photoelectric effect occur is low-energy photons striking heavy atoms.

It's interesting to note that the cross section also depends specifically on the ratio between electron [[Relativistic energy|rest energy]] and photon energy.
### In quantum mechanics
Einstein's discovery and explanation of the photoelectric effect had a profound impact in confirming Planck's quantum theory. Assuming the photon energy is indeed $\hbar \omega$ as per the [[Planck formula]], it is possible to measure the [[Electric potential|electric potential]] needed to prevent an electron from moving from the negative to the positive pole of a circuit (cathode to anode). The relation is
$$\hbar \omega - W = -eV_\text{stop}$$
where $V_\text{stop}$ is the potential needed to stop the electron. It is found that $V_\text{stop}$ is zero up to a threshold frequency $\omega_{0}$, beyond which the potential increases linearly, exactly confirming the formula above. This confirms that the energy of an electron is correctly described by the [[Planck constant]], which was found to have the same value originally postulated by Planck.
### In detectors
The photoelectric effect can also be useful in [[Detector|detectors]]. Like all electrically neutral particles, photons can be difficult to detect using traditional techniques. The usual method for detecting neutral particle is to make them interact with a charged particle and then measure the charged particle. The photoelectric effect ends up being a rather convenient method for photon detection, as electrons are extremely well known and stable.

If the detector is thick enough to stop the freed electron, all of its energy can be transferred to the detector for measurement. Since a photon is [[mass|massless]], this energy *is* the photon's energy (barring the binding energy that, as we said, is quite small). The measurements then depict a [[Gaussian distribution]] with a peak around $E_{\gamma}=\hbar \omega$ (due to detector noise).

[^1]: At higher energies [[Compton scattering]] starts to dominate.
