---
wiki-publish: true
aliases:
  - Wu experiment
---
**Parity** $\hat{P}$ is a [[transformation]] that inverts a spatial coordinates of a [[Physical system|system]]. It is a [[Symmetry|discrete symmetry]]. It operates over a [[Vector space|vector]] as
$$\hat{P}:(x,y,z) \mapsto (-x,-y,-z)\quad\text{or equivalently}\quad \hat{P}:\mathbf{r}\mapsto-\mathbf{r}$$
It is a specular reflection about the origin.

Parity is a [[unit operator]]: $\hat{P}^{2}=\hat{\mathbf{1}}$. Its [[Equazione agli autovalori|eigenvalues]] are therefore $P=\pm1$. These eigenvalues are generally called **even** (+1) and **odd** (-1).
### Quantities
Quantities can be assigned a parity depending on whether the function that governs is even or odd. Here are a few important ones:
- [[Linear momentum]] is odd.
- [[Angular momentum]] is even.
- [[Spin]] is even.
- [[Helicity]] is odd.

As a rule of thumb, [[scalar|scalars]] are even (e.g. spin) and vectors are odd (e.g. linear momentum). [[Pseudovector|Pseudovectors]] (e.g. angular momentum) are instead even, which is why they're called pseudovectors in the first place. [[pseudoscalar|Pseudoscalars]] (e.g. helicity) are odd.
### In particle physics
As in [[#Quantities]], each [[Fundamental interaction|fundamental interaction]] can assigned a parity by seeing if the laws that govern that force are even or odd:
- [[Electromagnetism]] is even (because [[Maxwell's equations]] are).
- [[Weak interaction]] actually violates parity symmetry and is therefore weird. See [[#Wu experiment]] below.

Parity can also be assigned to individual [[particle|particles]] by seeing their [[wavefunction]] is even or odd[^1]. This function may be either even ($\psi(\mathbf{r})=\psi(-\mathbf{r})$) or odd ($\psi(\mathbf{r})=-\psi(-\mathbf{r})$). This is the **intrinsic parity** of the particle. The parity of a system of many particles is the product of all individual parities: $P_\text{tot}=\prod_{i} P_{i}$.
#### Wu experiment
In the 1940s, physicists where wracking their head over a weird phenomenon. Two known particles, $\Theta$ and $\tau$, seemed to have the same [[mass]] and [[mean lifetime]][^2]. This suggested the idea that they're actually the same thing, but they [[Particle decay|decayed]] in different ways, specifically ways that were incompatible with each other:
$$\Theta^{+}\to \pi^{+}+\pi^{0},\qquad \tau^{+}\to \pi^{+}+\pi^{+}+\pi^{-}$$
(detected in [[Cloud chamber|cloud chambers]]). These were [[Weak interaction|weak force]] decays, but the issue is that they end [[parity]] of these was different. The $\Theta^{+}$ decayed into $P=(-1)^{2}=1$ and the $\tau^{+}$ decay into $P=(-1)^{3}=-1$. Alright, so different particles then?

Well, there's a huge hole here, and it's called [[CPT theorem]]. This theorem, already proven at the time, showed that this sharing of mass and mean lifetime should not be possible. So, same particle then? But that would mean weak decay violates parity conservation. This question was called the **$\Theta$-$\tau$ puzzle**.

The solution would come in 1956 thanks to Chinese American physicist Wú Jiànxióng. The experiment wanted to show that weak decay does, in fact, violate parity conservation. To do so, the parity of unstable cobalt-60 nuclei would be measured before and after a [[Beta decay|beta minus decay]]:
$$\ce{^{60}Co}\to \ce{^{60}Ni^{**}}+e^{-}+\bar{\nu}_{e}$$
followed up by nickel-60's double [[gamma decay]]:
$$\ce{^{60}Ni^{**}}\to \ce{^{60}Ni^{*}}+\gamma\to \ce{^{60}Ni}+\gamma+\gamma$$
which gives two high-energy photons. Where the [[electron]] gets shot to is the key. Its direction of emission depends on the polarization state of the nucleus, but this is affected by the parity of the nucleus. If parity is conserved, the number of electrons "up" the polarization axis should be identical to the one "down" it. If it's violated, this does not need to be true. This difference (or lack thereof) is the point of the measurement.

The photons aren't strictly necessary, but measuring their distribution too helps to determine that cobalt is truly polarized (spatial distribution depends on the polarization) to rule out a cause for error. We know EM interaction conserves parity, so this is true regardless of the experiment's results.

:::image
![[Wu_Exp_Parity_transformation.png|500]]
$j$ is the polarization axis. This show emission of an electron, but principle is the same.
By nagualdesign - Own work, made using reference. CC0, from [Wikipedia](https://commons.wikimedia.org/w/index.php?curid=97671385).
:::

The nuclei were polarized with a uniform [[magnetic field]] ([[temperature]] was also kept near zero to prevent [[random]] thermal breaking of alignment). In this environment, polarization goes like
$$\mathbf{P}\propto \exp\left( \frac{\mu B}{k_{B}T} \right)$$
where $\mu$ is [[permeability]] and $k_{B}$ is the [[Boltzmann constant]].  There's a couple complications:
1. This polarization must be kept up for the entire duration of the experiment, meaning for as long as decay measurements are taken.
2. Despite very low temperatures ($T\sim 0.01\text{ K}$), magnetic fields need to be intense ($B\sim 10\text{ T}$). This is because we're polarizing the *nucleus*! Protons are kept still by the [[Strong interaction|strong force]], which is harder to overcome than electromagnetism.

The solution to both of these is **[[adiabatic demagnetization]]**. The cobalt is covered in a thin layer of [[Paramagnet|paramagnetic]] salt. An initial magnetic field is applied and then waned. While it wanes, the cobalt transfers [[heat]] to the salt, which favors the polarization by reducing temperature even further. A second magnetic field is then applied to do the actual polarization. This measurement is conducted with the magnetic field alternating directions to check for emission both ways and see any (if any) differences.

:::image
![[Wu-Experiment_(English).png|500]]
Apparatus of the Wu experiment.
*By Pen88, with English translation by Stigmatella aurantiaca - Derived from Wu-Experiment_wikipedia by Pen88 on the German Wikipedia, substituting the German legends with English legends., CC BY-SA 3.0, from English [Wikipedia](https://commons.wikimedia.org/w/index.php?curid=29895892).*
:::

[[Detector|Detectors]] were located on both (almost) parallel and perpendicular to the polarization axis in order to measure emission distribution by counting the number of detections. Their counts revealed the truth: there *was* an anisotropy in the electron emission! Changing the polarization did change have an effect, which cannot be explained if parity is conserved. Thus, the weak force must violate parity conservation. As further confirmation, photons were correctly found to not care about polarization, as their distribution did not change.

This solves the $\Theta$-$\tau$ puzzle: $\Theta$ and $\tau$ are the same thing. Later, we'd name it $K^{+}$, the positive [[kaon]].

[^1]: This statement is somewhat loose actually. Suffice to say that QFT provides better reasoning for this association.

[^2]: This $\tau$ is not the [[lepton]] of the [[tau|same name]]. This was before the tau lepton was discovered.
