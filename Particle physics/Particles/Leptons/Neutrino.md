---
wiki-publish: true
aliases:
  - electronic neutrino
  - muonic neutrino
  - tau neutrino
---
A **neutrino** is a [[lepton]] characterized by exceptionally low interactivity. As the name suggests, they are [[Electric charge|electrically neutral]], so [[electromagnetism]] is out. All leptons don't [[Strong interaction|strong interact]], so that's also out. [[Gravity]] is largely unusable with [[particle|particles]] in general due to how weak it is, so that's out too. As such, neutrinos only [[Weak interaction|weak interact]], giving minuscule [[Cross section|cross sections]] to processes where they are involved as reagents. For instance, a neutrino-[[proton]] collision at 10 [[Electronvolt|GeV]] has a cross section of only 70 *[[Barn|femtobarns]]*.

Neutrinos come in three [[flavor|flavors]], one for each lepton proper: **electronic neutrino**, **muonic neutrino** and **tau neutrino**.
## Discoveries
### The electronic neutrino
An indication of the electronic neutrino came from [[Beta decay|beta minus decay]]
$$n\to p+e^{-}$$
The [[neutron]], [[proton]] and [[electron]] were all well-known at the time, but something was missing. For one, if this was truly the reaction, the [[energy]] spectrum of the electron would essentially be a [[Dirac delta]] (barring experimental error and the [[Disuguaglianza di Heisenberg|uncertainty principle]] of course). This is because it would a simple [[Particle decay|back-to-back decay]] from rest, in which we know the [[kinetic energy]] of the products is rigidly defined by the [[mass|masses]] involved. And yet, experiments kept showing a diffuse energy [[Probability distribution|distribution]] instead, suggesting that this was in fact a three-body decay, where energy of the products is not well-defined. Still, this third particle eluded all detection. Also, [[spin]] was not conserved in this reaction since all three particles involved had spin 1/2, meaning the input was 1/2 and the output was either 0 or 1.

In 1930, German physicist Wolfgang Pauli (of [[Pauli exclusion principle]] fame) hypothesized the existence of this particle, and that for it to exist and yet remain unmeasured it would need to be both chargeless and either massless or have such tiny mass it might as well be. This would've made it essentially undetectable at the time. It would've also had spin 1/2 to conserve total spin.

Enrico Fermi and Edoardo Amaldi learnt of the proposal and, in a conversation, jokingly called it a "**neutrino**" (lit. "small neutron"), a term that Fermi went on to popularize. The reaction would've then involved an antineutrino:
$$n\to p+e^{-}+\bar{\nu}$$
Fermi went on to explain the theory of this decay. He though of it as a four-way contact interaction, meaning no [[force carrier]] needed to exist. The neutron morphs into the proton and an electron and antineutrino are created and emitted as byproducts. The reaction rate would be given by [[Fermi golden rule|Fermi's second golden rule]]
$$W=\frac{2\pi}{\hbar} \frac{G_{F}^{2}}{\Omega ^{2}}\lvert \mathcal{M}_{fi} \rvert ^{2}\rho$$
where $G_{F}$ is the weak interaction's [[coupling constant]] (also called **Fermi constant** in honor of this), $\Omega$ is the volume of the [[Atomic nucleus|nucleus]], $\mathcal{M}_{fi}$ is the [[matrix element]] of the [[state transition]] and $\rho$ is the particles' energy distribution in the final state.

Still, all this math didn't solve the practical problem of discovering the thing, but it did confirm that doing so would not be easy. Theoretical reaction rates, and so cross sections, implied that absorbers would've needed to be somewhat big in order to guarantee interactions. Several light years across, to be specific. The approach was then to shoot as many particles as possible at *really* dense absorbers with [[detector|detectors]] and hope for luck to be on science's side. The reaction to use was
$$\bar{\nu}+p\to e^{+}+n\tag{1}$$
so a positron and neutrons needed to be detected simultaneously to confirm presence.

The winning experiment was due to American physicists Clyde Cowan and Frederick Reines (1956), whose idea was to use uranium in a high-[[power]] (megawatt-range) nuclear reactor[^1] which produced some $10^{20}$ antineutrino per second per centimeter. They made these antineutrinos collide with a dense target of two tanks of water and cadmium chloride with [[scintillator|scintillators]] ([[Photon]] detectors) in the middle. The process was this
1. The positrons from the reaction would collide with normal electrons in water, [[annihilation|annihilate]] and produce two high-energy photons ($e^{+}+e^{-}\to \gamma+\gamma$).
2. The neutrons would be captured by the cadmium chloride (cadmium is a very good neutron absorber), which would cause the emission of a photon with an expected delay of about one microsecond.

The experiment was ran and both these phenomena were detected, at precisely that interval. This was sufficient evidence that the antineutrino needed to exists. Since particle-antiparticle symmetry has never been broken, this also proved the existence of the neutrino itself.
### The muonic neutrino
All was well and good, except for one detail. When [[muon|muons]] were involved, neutrinos were also known to be created. It's fair to assume that this neutrino is the same neutrino as the beta decay. But that would end up not being true, for the neutrino of the muon was just a bit different from that of the electron.

Proof came from Italian physicist Bruno Pontecorvo in 1959. The idea of his experiment was that neutrinos coming from muons, when interacting, could only produce muons. Meanwhile, neutrinos for electrons could only make electrons. A proton beam would be shot at some target, causing the numerous particle interactions between protons that most often lead to [[pion|pions]]. The pions would then decay into muons alongside antineutrinos of the muon kind. Then, if the muon neutrinos really are different, the decaying muons must obey
$$\mu^{-}\to e^{-}+\bar{\nu}_{e}+\nu_{\mu}\tag{2}$$
where the new subscript on $\bar{\nu}$ indicates the kind (or **flavor**) of the neutrino. This reaction can only happen if the electron and muon conserve different quantities, otherwise we'd just have $\mu^{-}\to e^{-}$. But this latter reaction was not detected, as the number of muons, electrons and neutrinos did not line up with what we'd expect if it were true. Thus, it must have been $(2)$ that was happening.

To quantify the conservation, the [[lepton number]] was split in two families: electronic and muonic, each of which was conserved, but *independently*.
### The tau neutrino
Of all interactions, there was one that was leaving scientists confused. It was the collision of an electron-positron beam:
$$e^{-}+e^{+}\to e^{\pm}+\mu^{\mp}+X$$
The weird part was that, while electrons and muons were detected just fine, there was still an energy problem. The energy before and after the collision always failed to be conserved, always missing a piece that just wasn't explained by the mass and kinetic energies of $e^{\pm}$ and $\mu^{\mp}$. So, physicists thought that there undetected particle in there that were carrying the energy difference with it but was failing detection.

Being a reaction of leptons, it was readily assumed that the missing pieces were the known neutrinos. For instance:
$$e^{-}+e^{+}\to e^{-}+\mu^{+}+\bar{\nu}_{e}+\nu_{\mu}$$
But the problem is that even *this* was losing energy. The solution was to admit the existence of another neutral, hard-to-detect particle, a third lepton and its neutrino: the **[[tau]]** $\tau^{\pm}$ and the **tau neutrino** $\nu_{\tau}/\bar{\nu}_{\tau}$. The reaction could instead be
$$e^{-}+e^{+}\to\tau^{+}+\tau^{-}$$
and the taus would decay into
$$\tau^{+}\to \mu^{+}+\bar{\nu}_{\mu}+\bar{\nu}_{\tau},\qquad \tau^{-}\to e^{-}+\bar{\nu}_{e}+\nu_{\tau}$$
thus leading to the original decay, with *four* extra neutrinos:
$$e^{-}+e^{+}\to e^{-}+\mu^{+}+\bar{\nu}_{e}+\nu_{\mu}+\nu_{\tau}+\bar{\nu}_{\tau}$$
For this proposal to make sense, the tau needed a mass of about 1777 MeV in order for energy to be conserved, almost double that of the proton, but a [[mean lifetime]] so tiny ($\sim10^{-20}\text{ s}$) it was all but impossible to detect. This tau would carry the third lepton number and fix the reaction. The issue was proving that it existed. The tau's mass would later be identified at the DESY [[synchrotron]] in Hamburg and the SPEAR in Stanford.

[^1]: Not before proposing the idea of instead just setting off a 20 kiloton nuke nicknamed "El Mostro" and measuring that.
