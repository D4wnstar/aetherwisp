---
wiki-publish: true
---
A **molecule** is a bound [[Physical system|system]] of at least two [[Nucleo atomico|atomic nuclei]] and their [[electron|electrons]]. Molecules containing two nuclei are said to be **diatomic**, whereas ones containing more than two are said to be **polyatomic**. The [[stato|states]] in which the electrons are in are called [[molecular orbital|molecular orbitals]].

Compared to the study of [[atom|atoms]], the study of molecules is greatly complicated by the motion and interaction of the nuclei. Luckily however, much of this problem is lifted since the [[mass]] of the nuclei is considerably larger than that of the electrons, thus causing the nuclear states to be less significant overall. A ballpark estimate using the [[Frequency|angular frequencies]] of electron excitations $\omega_{e}$ and nuclear vibrations $\omega_{N}$ (more on this below) leads to a ratio $\omega_{N}/\omega_{e}\sim 10^{-3}\textendash10^{-5}$, several orders of magnitude less. This is the logical basis for the common framework in which much of molecular physics is developed: the [[Born-Oppenheimer approximation]].

Moreover, not all electrons are bound to the nucleus with the same strength. Electrons in complete [[electron shell model|shells]] are bound to the nucleus much more strongly than electrons in the incomplete outermost shell, broadly speaking difference between $\sim 10\text{ eV}$ and $\sim 1\text{ eV}$. As such, only the outer electrons, the *valence* electrons, are assumed to take part in molecular bonding.

Some nomenclature: molecular orbitals are generally abbreviated as **MO**, while atomic ones as **AO**. The highest-energy occupied molecular orbital is called **HOMO** and the lowest-energy unoccupied molecular orbital is called **LUMO**. The **excitation energy** of a molecule is given by the energy difference between LUMO and HOMO: $\Delta E\equiv E_{\text{LUMO}}-E_\text{HOMO}$.
### Symmetries in diatomic molecules
Diatomic homonuclear[^1] molecules are certainly the easiest case to deal with, in part due to the [[symmetry|symmetries]] that they present. To illustrate these, call $z$ the axis defined by the line between the two nuclei (the **bond axis**) and $\mathbf{L}$ the [[Momento angolare quantistico|quantum angular momentum]] of [[electron|electrons]] in a certain state. The projection of $\mathbf{L}$ on the $z$ axis and more so its [[Equazione agli autovalori|eigenvalues]] $M_{z}$
$$L_{z}\psi=\hbar M_{z}\psi,\quad M_{z}=0,\pm1,\pm2,\ldots$$
are a symmetry.

Just like how we use the [[spectroscopic notation]] letters to denote the angular states $l$ of atoms, we also use letters to denote the values of $M_{z}$ for molecular states. For molecular orbitals, we use $\Sigma,\Pi,\Delta$ and $\Phi$. For single-electron orbitals, we use their lowercase equivalents: $\sigma,\pi,\delta$ and $\phi$.

Another symmetry is with respect to the plane passing through the bond axis, such as the $xz$ plane or the $yz$ plane. [[Parità|Parity]] is symmetric about this plane[^2]. For instance, if we consider the $xz$ plane, the parity [[transformation]] $A_{y}:y\mapsto -y$ one the $y$ axis is a symmetry (in other words, the $y$ axis looks the same on both sides of the $xz$ plane; it's mirrored). Note that $L_{z}$ and $A_{y}$ do not commute, $[L_{z},A_{y}]\neq 0$. Specifically, applying $A_{y}$ maps $M_{z}$ to $-M_{z}$. This implies that, for any $M_{z}>0$, the states $\pm M_{z}$ have the same [[energy]].

One last symmetry is again parity, but with respect to the coordinate $r$. The transformation $A_{r}:r\mapsto-r$ is a symmetry.

So we have three symmetries: $L_{z}$, $A_{y}$ and $A_{r}$. The eigenvalues of these help to uniquely identify a state in a molecular system. Given a molecular orbital, say $\Pi$, we typically write these numbers around the orbital's letter, like so
$$1\Pi^{+}_{g}$$
The left number is $M_{z}$. The top right is the $y$ parity. Recall that the parity operator only has two eigenvalues, $\pm 1$, and we denote these as $+$ and $-$, with hopefully obvious meaning. Similarly $r$ parity (bottom right) also has two values, but to distinguish them from the $y$ parity, we use the initials of two German terms: *gerade* and *ungerade*, literally meaning even or odd respectively.

The real value of symmetries is that, broadly speaking, only atomic orbitals of similar energy and symmetry can combine to form molecular orbitals. This allows us to intuitively select which orbitals would combine with which by knowing both their energy (the eigenvalue of the orbital) and symmetries (the angular momentum $l$). The figure below shows a few examples of atomic orbital that can bond and the molecular orbitals that they create.

![[Diagram Molecular orbital symmetries|100%]]

#### von Neumann-Wigner non-crossing rule
When it comes to diatomic molecules, there's a useful rule regarding symmetries that relies on the fact that the electronic terms only rely on the internuclear distance $R$.

> [!info] von Neumann-Wigner non-crossing rule
> Electronic states, represented by their potentials $E(R)$, that have the same symmetries never cross when varying internuclear distance $R$. In other words, given two distinct electronic states $E_{1}(R)$ and $E_{2}(R)$, there does *not* exist an $R_{C}$ for which $E_{1}(R_{C})=E_{2}(R_{C})$.
#### Examples
> [!example] Lithium hydride
> Lithium hydride $\text{LiH}$ is a heteronuclear molecule with four total electron, three from lithium and one from hydrogen. An isolated, neutral lithium atom has ground state $1s^{2}2s$. The ground state of hydrogen is as usual $1s$. The $1s^{2}$ shell in lithium is complete, so we can imagine it will not bond in any way. The technical reason is that only orbitals of similar energy are likely to bond. The energies involved here are
> $$E_{1s,\text{Li}}\simeq-67\text{ eV},\quad E_{2s,\text{Li}}\simeq-5.4\text{ eV},\quad E_{1s,\text{H}}\simeq-13.6\text{ eV}$$
> As such, lithium's $1s$ is way out of range in terms of energy. Meanwhile, lithium's $2s$ and hydrogen's $1s$ are similar enough that they'll probably bond.
> 
> The lowest energy electronic state (i.e. molecular orbital) is designated as $1\sigma$ and is essentially just the atomic orbital for the inner shell of lithium. The other states do participate in bonding. We have a $2s$ on lithium and a $1s$ on hydrogen, both of which have similar enough energy, same angular momentum number $l=s$ and same magnetic number $m=0$. This makes them prime material for a bond. They combine to form two possible molecular orbitals (top row of the figure above): a bonding $\sigma_{g}$ orbital (lower energy than both $1s(\text{H})$ and $2s(\text{Li})$) and an antibonding $\sigma_{u}$ orbital (higher energy). Hence, the electrons spontaneously occupy the bonding $\sigma_{g}$ first, completely filling it. There are no electrons left to occupy the antibonding $\sigma_{u}$, so it remains empty. The result is a fully bonding $2\sigma$ orbital.
> 
> Or, it would be if the situation wasn't a little more complicated. Through the usage of the [[variational method]], it can be proven that the lowest energy molecular orbital is actually created not by the lithium $2s$ orbital, but by a [[linear combination]] of the $2s$ and $2p_{z}$ orbitals. This combination of orbitals with different angular momentum is known as **[[orbital hybridization]]**, and it occurs when $ns$ and $np$ orbitals are close in energy. Since they're so close, the chance that the electron ends up in $np$ despite being higher energy is not *that* low and therefore should not be ignored in the LCAO. The result is called a **hybrid orbital**, in this case an $sp$ hybrid. Mathematically, each the hybrid is a superposition of the *three* atomic orbitals:
> $$\Phi_{\sigma}=c_{1}\psi_{1s(\text{H})}(\mathbf{r}_{\text{H}})+c_{2}\psi_{2s(\text{Li})}(\mathbf{r}_{\text{Li}})+c_{3}\psi_{2p_{z}(\text{Li})}(\mathbf{r}_{\text{Li}})$$
> Either way, it's still a $2\sigma$ bond.
> 
> The energy of hydrogen $1s$ is lower than lithium $2s$, so the bond (technically, its electron distribution) will be slanted towards hydrogen. As such, the bond will be *polar*, with a slightly more negative half on the hydrogen side and a slightly more positive part on the lithium side, leading to a permanent [[electric dipole]].

> [!example] $\text{C}\textendash\text{H}$
> The $\text{C}\textendash\text{H}$ molecule isn't a stable molecule. It's "unfinished" and need other atoms to have its orbitals completely filled. That said, it's interesting to talk about the individual carbon-hydrogen bond. The carbon's electron configuration is $1s^{2}2s^{2}2p^{2}$. Unlike lithium hydride, the carbon $2s$ orbital is *very* close in energy to the hydrogen $1s$ state. This causes it to participate in bonding even though it is fully filled (although the second carbon *shell* is not fully filled, as it's missing four electrons in $2p$). Thus, the bond form an $sp$ hybrid like in $\text{LiH}$. The dipole term here is stronger.

> [!example] Hydrogen fluoride
> Hydrogen fluoride $\text{HF}$ is largely similar to $\text{LiH}$, but the energy of the fluoride's $2s$ is far lower than the hydrogen's $1s$. As such, the bond is still a hybrid $sp$, but the electric dipole term is *very* pronounced, making it an ionic bond.

> [!example] Methane
> Methane $\text{CH}_{4}$ complicates things by not being diatomic. The carbon electron configuration is $1s^{2}2s^{2}2p^{2}$, but in this case, it's worth noting that the exited state $1s^{2}2s^{2}2p^{3}$ is very close in energy. This is important because carbon bonds much more easily in this state. Here, since there's one electron each in $2s$, $2p_{x}$, $2p_{y}$ and $2p_{z}$, these can all hybridize together to form four hybrid $sp^{3}$ bond to four different external electrons. This is precisely what happens in methane, where the four external electrons are given by the four hydrogens. The shape formed by the bonds is a square pyramid, as that is the form that keeps the electrons most far away from each other, thus leading to a electric potential minimum.

> [!example] Ethylene
> Ethylene $\text{C}_{2}\text{H}_{4}$ is interesting because it is the first molecule in this sequence to create $\pi$ bonds. Assume that both carbons are in the excited state as per methane. We now have four bonds to make. It's pretty clear that we'll get some bonds between the carbons and the hydrogens, but the carbons also bond between each other. Specifically, their $2p_{z}$ orbitals connect in a $\sigma$ bond. Then, one perpendicular $2p$ orbital ($2p_{x}$ or $2p_{y}$) takes two hydrogen $1s$ to make a $\sigma$ bond with each, whereas the other connects to the corresponding orbital on the other carbon, creating a bond between two $2p$ orbitals: a $\pi$ bond. The result is that each carbon is bonded once to two hydrogens, but *twice* to the other carbons. This phenomenon is called a **double bond** ($\sigma+\pi$),

> [!example] Acetylene
> Acetylene $\text{C}_{2}\text{H}_{2}$ is similar to ethylene, but with two fewer hydrogens. Since the electrons need to go *somewhere*, they end up bonding with the other carbon, mostly by lack of options. This means that the carbons now have bonds with their $1s$ ($\sigma$), their $2p_{z}$ ($\pi$) and now another $2p$, say $2p_{y}$ ($\pi$). The remaining $2p_{x}$ in each carbon bonds with the hydrogen $1s$. The carbons are now bonded *three times*: this is called a **triple bond** ($\sigma+\pi+\pi$).
### Nuclear motion
In the [[Born-Oppenheimer approximation]], the nuclei are assumed to be stationary. This makes calculations a lot more feasible while keeping the error margin relatively small. That said, an error is an error, and we can do better. To reintroduce the nuclear kinetic terms, we can use the [[Equazione di Schrödinger|Schrödinger equation]] their motion:
$$\left[ - \frac{\hbar^{2}}{2\mu}\nabla ^{2}_{R}+E_{q}(\mathbf{R}) \right]F(\mathbf{R})=E_\text{tot}F(\mathbf{R})$$
where $\mu$ is the reduced mass of the system and $E_{q}(\mathbf{R})$ is the central potential. $F(\mathbf{R})$ is the wavefunction we're looking for. Now, outside of breaking the bond itself, there's only two things that nuclei can do: rotate and oscillate. Rotations must have their own angular quantum number $J$, whereas oscillations, referred to as *vibrations* in this context, will have a quantum number $v$. If we break $F(\mathbf{R})$ up into [[spherical coordinates]]
$$F(\mathbf{R})=\frac{\mathscr{F}_{vJ}(R)}{R}Y_{Jm_{J}}(\theta,\phi)$$
where $Y_{Jm_{J}}(\theta,\phi)$ are the [[spherical harmonics]], we find ourselves in a central symmetry problem, whose radial part is determined by
$$\left[ - \frac{\hbar^{2}}{2\mu} \frac{d^{2}}{dR^{2}}+ \frac{\hbar^{2}}{2\mu R^{2}}J(J+1)+E_{q}(R) \right]\mathscr{F}_{vJ}(R)=E_{svJ}\mathscr{F}_{vJ}(R)$$
The additional $s$ quantum number in $E_{svJ}$ is because of electron repulsion. If the molecule is stable, we can expand the electron repulsion energy $E_{s}$ in a [[Taylor series]] about its minimum $R_{0}$:
$$E_{s}(R)\simeq E_{s}(R_{0})+ \frac{1}{2}k(R-R_{0})^{2}$$
It can be found that the energy of a diatomic molecule is given by the simple sum
$$E_{svJ}=E_{s}(R_{0})+E_{v}+E_{r}$$
where $E_{v}$ and $E_{r}$ are **vibrational** and **rotational energies** of the molecule.

In the [[Oscillatore armonico quantistico|harmonic]] approximation, the vibrational energy is given by
$$\boxed{E_{v}=\hbar \sqrt{ \frac{k}{\mu} }\left( v+ \frac{1}{2} \right)}$$
The rotational energy on the other hand is
$$\boxed{E_{r}=\frac{\hbar^{2}}{2\mu R_{0}^{2}}J(J+1)}$$

These energies exist at quite different scales. Electron energy is in the order of a few [[Elettronvolt|electronvolts]], $\sim 1\textendash10\text{ eV}$, assuming the electrons are localized, with $R\sim\mathring{\text{A}}$. Vibrational energies are instead *much* higher, in the order of $\sim50\textendash 200\text{ eV}$. Rotational energies on the other hand are *tiny*, at merely $\sim 10^{-4}\text{ eV}$ in general.

As $v$ gets higher, the approximations on both the vibrational and rotational energy become progressively worse. To improve this, we can add corrective terms. For the vibrations, since we're assuming their harmonic, we add an extra nonlinear *anharmonic* term:
$$E_{v}=\omega\left( v+ \frac{1}{2} \right)-\omega \chi\left( v+ \frac{1}{2} \right)^{2}$$
where $\chi$ is known as the **anharmonic constant** and we set $\omega=\hbar \sqrt{ k/\mu }$ for brevity. The correction is most apparent for large $v$ and unimportant for small $v$.

A similar correction is applied to the rotational energy, but instead of considering anharmonic oscillations, we take the *centrifugal distorsion* into consideration:
$$E_{r}=BJ(J+1)-\Delta J^{2}(J+1)^{2}$$
where $\Delta$ is another constant. The idea is that the molecule is not rigid, but can be pulled and extended (hence the possibility of vibrational states). Thus, when rotating, the centrifugal force will tend to stretch the molecule out. This is why the first term is the energy for a **rigid rotator** and the second is the **centrifugal distorsion**. Just like the anharmonic correction, this is apparent for large $J$ and unimportant for small $J$.
### Spectra
The [[spectrum (electromagnetism)|spectrum]] of a molecule can be found in a similar manner to that of an atom, by determining which [[State transition|state transitions]] are allowed and categorizing them by the amount of energy that they emit. The energy emitted or absorbed during a state transition is
$$\hbar \omega=E_{f}-E_{i}$$
and the transition itself is described by a transition matrix element
$$M_{fi}=\braket{ \Psi_{fi} | \mathbf{D}| \Psi_{if} }\quad\text{where}\quad\mathbf{D}=-e\sum_{i}\mathbf{r}_{i}+e\sum_{j}z_{j}\mathbf{r}_{j} $$
$\mathbf{D}$ is the [[electric dipole moment]] of the molecule. We can break the wavefunction down into three parts much in the same way as energy:
$$\Psi=\Psi_{e}\Psi _{v}\Psi_{r}$$
with $e$, $v$ and $r$ representing the electronic, vibrational and rotational parts of the wavefunction.

The first state transitions to occur will be the rotational ones, since the energy of those states is so low. In particular, we can find the [[selection rule]]
$$\Delta J=\pm 1\quad\to \quad \hbar \omega=2B(J+1)$$
Vibrational transitions instead predict the absorption of a [[photon]] and the creation of a [[phonon]] that causes the vibration.

The emission and absorption spectra due to these effects are therefore quite molecule-dependent. On one hand, this is bad because it makes prediction of these spectra quite difficult. On the other hand, it is very convenient when measuring the spectrum of an existing substance: since the spectra are so unique, having access to one is an excellent way to uniquely identify a substance without even touching it. This is how, for instance, we're able to identify the chemical composition of distant [[stella|stars]] just by looking at them with a telescope.

[^1]: Homonuclear: both the nuclei in the diatomic molecule are identical. The opposite is heteronuclear, where they are different.

[^2]: But only for homonuclear molecules. The nuclei are identical, so mirroring makes no difference. If the molecule is heteronuclear, $A_{y}$ symmetry fails since mirroring would switch the positions of the evidently different nuclei. Similarly, $A_{r}$ parity also fails. $L_{z}$ symmetry still applies, however.
