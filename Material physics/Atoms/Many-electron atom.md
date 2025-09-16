---
wiki-publish: true
---
The **many-electron atom** is a [[physical system]] modeling an [[atom]] with an arbitrary number of [[Electron|electrons]] around and arbitrary [[Atomic nucleus|nucleus]]. It is an extension of the [[two-electron atom]] and the [[hydrogen atom]]. The [[Hamiltonian]] of the system is
$$H=\sum_{i=1}^{N}\underbrace{ \left[  - \frac{\hbar^{2}}{2m}\nabla ^{2}_{\mathbf{r}_{i}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{i}} \right] }_{ \text{Individual electrons} }+\sum_{i>j} \underbrace{ \frac{e^{2}}{4\pi \varepsilon_{0}r_{ij}} }_{ e-e\text{ interaction} } $$
where the sum over $i>j$ is indexed that way to avoid double-counting [[Electromagnetism|electromagnetic interactions]] between electrons.
## Central field approximation
With two electrons, the perturbative approximation was rather poor and required a more accurate treatment (namely, the [[variational method]]). As you add more electrons, it becomes even worse. Our approach is to try and enforce a central symmetry and split that Hamiltonian into a central term $H_{C}$ and an "everything else" term $H_{1}$, the latter of which is ideally much smaller and can be ignored:
$$H=H_{C}+H_{1}$$
The logical backing to this proposal is that, despite the additional electrons, the nucleus still acts as the central attractor of the system and that the electron-electron repulsive interactions have a central component. This model is called the **central field approximation** and was proposed by Hartree and Slater. It is an independent particle model where each electron moves in an *effective*, spherically-symmetrical [[potential]], representing both the central nuclear attraction and the *average* of the electron-electron repulsive interactions.

The effect of the repulsion is to *screen* (i.e. reduce) the central attraction to the nucleus and because of this, the electron-electron interaction term must have a strong central component to it. We can write this term as $\sum_{i}S(r_{i})$, where $S(r_{i})$ is called the **screening**. As such, if we *only* consider this central component (and use [[atomic units]]), we can broadly approximate the system's effective potential as
$$V(r)=- \frac{Z}{r}+S(r)$$
We can begin our investigation by figuring out what happens at the extremes: really far and really close to the nucleus.

Say an electron $r_{i}$ is very far from the nucleus but not that far from the other electrons. Mathematically, this means $r_{ij}\simeq r_{i}$ and $1/r_{ij}\simeq1/r_{i}$. In this case, the electron moves in a potential that is approximately given by
$$V(r)=- \frac{Z}{r_{i}}+\sum_{j=1}^{N-1} \frac{1}{r_{i}} =- \frac{Z-N+1}{r_{i}}\tag{1}$$
which corresponds to the Coulomb potential of the nucleus, screened by all the other $N-1$ electrons. In a neutral atom, where $Z=N$, it becomes as simple as it gets
$$V(r)=- \frac{1}{r_{i}}\tag{2}$$

Say now our electron $r_{i}$ is very close to the nucleus. When this happens, the screening becomes less pronounced and the central attraction takes over. In this regime, $r_{ij}\simeq r_{j}$ and the potential is approximately
$$V(r)- \frac{Z}{r_{i}}+\left\langle  \sum_{j=1}^{N-1} \frac{1}{r_{j}}  \right\rangle=- \frac{Z}{r_{i}}+C \tag{3}$$
where $\langle  \rangle$ denotes an average over the $r_{j}$ distances of all the other $N-1$ electrons and $C$ is a constant.

These limits are qualitatively interesting, but they also provide boundary conditions for further, more refined potentials. Any and all effective potentials that we employ must satisfy $(1)$ for $r\to \infty$ (and $(2)$ for neutral atoms) and $(3)$ for $r\to0$. The issue now is figuring out what happens outside of the extremes, which is everything but easy.

It should be noted that a central potential is fundamentally incompatible with a complete description of the many-electron atom. This is because the nature of the electron repulsion is dependent on the dynamics of the system: position is undefined in quantum mechanics, but the charge distribution is, and the repulsion must of course be directly dependent on the geometry of this distribution, which changes over time. A central potential enforces a static spherical distribution, so even with a perfect search algorithm, there is no "exact" central potential. Because of this, this kind of solution is mostly useful in the ground state and the first few excited state; anything more and it starts to show cracks. Fortunately, even these few states are more than enough to capture the essence of the system and see much of the complex behavior of the many-electron atom.
### Searching for the intermediate potential
Finding an actual expression for the potential is unfortunately not really feasible. We have boundary conditions ($(1)$, $(2)$ and $(3)$), but for intermediate potentials we hit a wall. Luckily, not all hope is lost and there's two paths we can take: either rely on clever approximations to get a decent analytical solution or get a computer to brute force the solution through clever programming.

Analytically one can use the Thomas-Fermi model (see below). Otherwise, on a computer the [[Hartree-Fock method]] is a classic algorithm to find the wavefunctions by progressively making the solution more precise at each step.
### Unperturbed eigenfunctions
Let's try our hand at finding eigenfunctions for the unperturbed central Hamiltonian
$$H_{C}=\sum_{i=1}^{N} \left[ - \frac{\hbar^{2}}{2m}\nabla ^{2}_{r_{i}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{i}} \right]+V_{C}(r)$$
where $V_{C}(r)$ is our central potential. The [[Equazione di Schrödinger|Schrödinger equation]] is
$$H_{C}\psi_{C}=\left[ \sum_{i=1}^{N} \left(  - \frac{\hbar^{2}}{2m}\nabla ^{2}_{r_{i}}  \right)+ V(r_{i}) \right]\psi_{C}=E_{C}\psi_{C}$$
where we combined the central potential with the nuclear attraction term into $V(r_{i})$. [[separation of variables|Separate the variables]] and you get $N$ independent equations, one for each electron, that combine to make a total eigenfunction like
$$\psi_{C}=u_{a_{1}}(\mathbf{r}_{1})u_{a_{2}}(\mathbf{r}_{2})\ldots u_{a_{N}}(\mathbf{r}_{N})$$
where each $u_{a_{i}}(\mathbf{r}_{1})$ are the individual electron wavefunctions, corresponding to their [[orbital|orbitals]]. Each orbital is, in [[spherical coordinates]] and like in the [[Hydrogen atom|hydrogenic atom]], a mix of a radial and angular part like
$$u_{nlm}(\mathbf{r})=R_{nl}(r)Y_{lm}(\theta,\phi)$$
where $m\equiv m_{l}$. The meaning of the [[Numero quantico|quantum numbers]] is the same as the ones in the hydrogenic atom. The angular part is as always independent from a central potential, so it's just the same old [[Spherical harmonics]]. The radial part is, however, not the same and needs to be solved again, according to
$$\left[ - \frac{\hbar^{2}}{2m}\left( \frac{1}{r^{2}} \frac{d}{dr}\left( r^{2} \frac{d}{dr} \right)- \frac{l(l+1)}{r^{2}} \right)- V_{C}(r) \right]R_{nl}(r)=E_{nl}R_{nl}(r)$$
Note how the energy eigenvalues now depend on $l$ too, not just $n$. To get the total energy of all electrons, just sum the individual ones:
$$E_{C}=\sum_{i=1}^{N} E_{n_{i}l_{i}}$$
### Adding spin
We can reintroduce spin by multiplying the orbital [[funzione d'onda|wavefunction]] by the spin component of the wavefunction
$$u_{nlmm_{s}}(q)=u_{nlm}(\mathbf{r})\chi_{1/2,m_{S}}$$
with the fourth quantum number $m_{S}$.

Our next goal is to use the single-electron wavefunctions to construct a total $N$-electron wavefunction $\Psi_{C}(q_{1},\ldots,q_{N})$ that is antisymmetric with respect to particle exchange. To do so, we'll denote the set of four quantum numbers corresponding to the given independent particle state with the letters $\alpha,\beta,\ldots,\nu$. The total wavefunction $\Psi_{C}$ describing an atom in which one electron is in a state $\alpha$, another is in a state $\beta$, etc. is given by the [[determinant]] of an $N\times N$ matrix:
$$\Psi_{C}(q_{1},q_{2},\ldots,q_{n})=\frac{1}{\sqrt{ N! }}\begin{vmatrix}
u_{\alpha}(q_{1}) & u_{\beta}(q_{1}) & \ldots & u_{v}(q_{1}) \\
u_{\alpha}(q_{2}) & u_{\beta}(q_{2}) & \ldots & u_{v}(q_{2}) \\
\vdots \\
u_{\alpha}(q_{N}) & u_{\beta}(q_{N}) & \ldots & u_{v}(q_{N})
\end{vmatrix}$$
This is called the **[[Slater determinant]]**. This makes the wavefunction naturally antisymmetric since swapping rows or columns changes the sign of the determinant. The energy eigenvalue $E_{C}$ of the unperturbed central field corresponding to a given Slater determinant is the sum of the energy of each $N$ state in the determinant. If two rows or columns are identical, then the determinant is, as usual, zero. But since those are determined by the quantum numbers, if any two electrons have the same set of quantum numbers, then the wavefunction is zero. It cannot exists, and we expect it to not exist because it's mandated by the Pauli exclusion principle: two electrons cannot possibly have the same state at the same time.

> [!example] Helium ground state
> The ground state of the neutral helium atom has two electrons, both in the $1s$ orbitals, with opposite spins. We therefore have two single-particle wavefunctions $u_{100\uparrow}$ and $u_{100\downarrow}$. The full wavefunction is given by the Slater determinant
> $$\Psi(q_{1},q_{2})=\frac{1}{\sqrt{ 2! }}\begin{vmatrix}
> u_{100\uparrow }(\mathbf{r}_{1}) & u_{100\downarrow }(\mathbf{r}_{1}) \\
> u_{100\uparrow }(\mathbf{r}_{2}) & u_{100\downarrow }(\mathbf{r}_{2})
> \end{vmatrix}$$
### Thomas-Fermi model
The Thomas-Fermi model of the many-electron atom uses a [[Fermi gas]] to represent the system in the context of a central potential. It is a relatively simple model, but does not provide particularly good results.

The idea is that the electrons (the "gas particles") are considered as being confined into a finite region of space by the central potential. The electron cloud screens part of the nuclear charge and the total energy ends up being
$$E_{\text{max}}=E_{F}+V(r)<0$$
where $E_{F}$ is the [[Fermi energy]] of the gas. Writing $E_{F}$ in terms of the [[Fermi energy|Fermi wavevector]] $k_{F}$
$$E_{F}=\frac{\hbar^{2}k_{F}^{2}}{2m}=\frac{\hbar^{2}}{2m}(3\pi \rho)^{2/3}$$
gives
$$k_{F}\equiv k_{F}(r)=\sqrt{ \frac{2m}{\hbar ^{2}}[E_{\text{max}}-V(r)] }$$
and extracting $\rho$ from $k_{F}=(3\pi \rho)^{1/3}$ gives the electron density
$$\rho(r)=\begin{cases}
\frac{1}{3\pi ^{2}}\left( \frac{2m}{\hbar ^{2}} \right)^{3/2}[E_{\text{max}}-V(r)]^{3/2} &\text{if }V(r)\leq E_\text{max} \\
0&\text{if }V(r)>E_\text{max}
\end{cases}$$
The potential produced by this electron distribution can be shown to be
$$V(r)=- \frac{Ze^{2}}{4\pi \varepsilon_{0}r}\chi(r)$$
where $\chi(r)$ is a dimensionless function that is the solution to the non-linear [[Ordinary differential equation|ordinary differential equations]]
$$\frac{d^{2}\chi}{dr^{2}}=\frac{1}{\sqrt{ r }}\chi^{3/2}\quad\text{if }\chi\geq 0,\qquad \frac{d^{2}\chi}{dr^{2}}=0\quad\text{if }\chi< 0$$
The function is actually entirely determined by the left equation, called the **Thomas-Fermi equation**. It has boundary condition $\chi(0)=1$. It has at most one other zero between $0$ and $+\infty$ found at a point $r_{0}$, which we can interpret as the "edge" of the atom in this description. The lack of a second boundary condition means that there are actually infinite functions $\chi$ that can satisfy the Thomas-Fermi equation, and these can be classified in three types: $\chi$ for neutral atoms, $\chi$ for positive ions ($N<Z$)[^1] and $\chi$ for neutral atoms under [[pressure]]. See *Bransden & Joachaim, Chapter 7.3* for an actual proof and discussion.

The Thomas-Fermi model provides good results for intermediate $r$ and can be useful to estimate atomic properties which only depend on the average distance $r$ from the nucleus.
### Hartree-Fock method
The [[Hartree-Fock method]] is another method used to describe the central potential of the many-electron atom, but unlike the Thomas-Fermi model, it is built on the [[variational method]] and the enforcement of antisymmetry in the total state.
### Relativistic corrections
The central potential model above, no mention is ever made of [[Lorentz transformation|relativistic]] behavior. Like in the [[Hydrogen atom#The fine structure|fine structure of the hydrogen atom]], we can attempt to fix the solution retroactively by adding additional relativistic corrections to the model with non-central terms.

We'll consider the Hamiltonian for the electrostatic energy
$$H_{1}=\sum_{i>j} \frac{e^{2}}{4\pi \varepsilon_{0}r_{ij}}-\sum_{i=1}^{N} V_{C}(r_{i})$$
which is the piece that we originally discarded when we split the total Hamiltonian in $H=H_{C}+H_{1}$. We will also consider the spin-orbit interaction given by the Hamiltonian
$$H_{2}\equiv \sum_{i}\xi(\mathbf{r}_{i})\mathbf{L}_{i}\cdot \mathbf{S}_{i}\quad \text{where }\xi(\mathbf{r}_{i})=\frac{1}{2m^{2}c^{2}} \frac{1}{r_{i}} \frac{dV(r_{i})}{dr_{i}}$$
We'll use [[Teoria delle perturbazioni|perturbation theory]] to describe the effects of these corrections, though not in all cases. For the sake of simplicity, we will assume that one of these Hamiltonians is much larger than the other: either $H_{1}\gg H_{2}$ or $H_{2}\gg H_{1}$. This is because the case where both are of comparable magnitude, called **intermediate coupling**, is considerably more difficult to solve.

The former case, $H_{1}\gg H_{2}$ is not uncommon, as it arises in atoms with small or intermediate values of $Z$. It is called **L-S coupling**. The latter case, $H_{2}\gg H_{1}$, arises in atoms with large $Z$ and is known as **j-j coupling**.
#### L-S coupling
This correction is reminiscent of the spin-orbit coupling of the fine structure, where the interaction between orbital momentum and spin was investigated. This correction is the application of that coupling to all the electrons around the nucleus. Since $H_{1}\gg H_{2}$, we'll ignore $H_{2}$.

The [[Momento angolare quantistico|angular momenta]] and spin of the electrons all sum to give a *total* angular momentum $\mathbf{L}$ and a total spin $\mathbf{S}$. $H_{1}$ [[Commutator|commutes]] with both $L$ and $S$ (since it is independent of $m_{l}$ and $m_{s}$) and thus all associated energy levels will have [[Degenerazione|degeneracy]] $(2L+1)(2S+1)$. The energy levels associated with these quantum numbers are called **terms** and are denoted as $^{2S+1}L$, where $L$ uses the [[spectroscopic notation]] letters, except as uppercase instead of lowercase. For instance, $^{2}P$ or $^{4}S$. Due to the Pauli exclusion principle, not all terms are valid.

For an example, consider the neutral lithium atom. It has three electrons and six possible states (combinations of $L=0,\pm1$ and $s=\pm 1/2$). There are $\begin{pmatrix}3 \\ 6\end{pmatrix}=20$ possible ways of setting up the system. However, there are only *three* possible terms: $^{4}S$, with degeneracy $d=4$; $^{2}D$, with degeneracy $d=10$; and $^{2}P$, with degeneracy $d=6$.
#### j-j coupling
For heavy atoms (high $Z$), the spin-orbit energy $H_{2}$ is much larger than $H_{1}$, so we'll ignore the latter. The effect of $H_{2}$ is to partly remove the degeneracy in the energy levels $E_{nl}$ by splitting every level with $l\neq 0$. The energy levels now also depend on the total angular momentum $j=l+s$ as $E\equiv E_{nlj}$ and now have degeneracy $d=2j+1$, with states $\ket{u_{nlj}}$. The total state of the system is built by selecting the $u_{nlj}$ such that they are antisymmetrical. The total energy will be
$$E=\sum_{i} E_{n_{i}l_{i}j_{i}}$$
In this case, it's typical to use an altered notation that omits references to $L$ and $S$ specifically in favor of just referencing $J$ directly through $j_{1},\ldots,j_{N}$, which are the total angular momenta of each individual electron.

[^1]: This theory is not capable of handling negative ions ($N>Z$).
