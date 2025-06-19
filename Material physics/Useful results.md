---
wiki-publish: true
---
### Hydrogen atom
**Hamiltonian**
$$\hat{H}=- \frac{\hbar^{2}}{2M}\nabla ^{2}_{R}- \frac{\hbar^{2}}{2m}\nabla^{2}_{r_{e}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{e}}$$
**Eigenvalues**
$$E_{n}=- \frac{e^{2}}{4\pi \varepsilon_{0}a_{0}} \frac{\mu}{m_{e}} \frac{Z^{2}}{2n^{2}},\qquad \text{degeneracy}=n^{2}\text{ (w/out fine structure)}$$
**Position eigenfunctions**
$$\psi_{nlm}(r,\theta,\phi)=- \sqrt{ \left( \frac{2Z}{na_{\mu}} \right)^{3} \frac{(n-l-1)!}{2n[(n+l)!]^{3}} }\left( \frac{2Z}{na_{\mu}} \right)^{l}e^{-Z/na_{\mu}}L_{n-l-1}^{2l+1}\left( \frac{2Z}{na_{\mu}} \right)Y_{lm}(\theta,\phi)$$
**Fine structure, relativistic kinetic energy**
$$H_{1}'=- \frac{1}{8} \frac{p^{4}}{m^{3}c^{2}},\qquad\Delta E_{1}=- E_{n} \frac{(Z\alpha)^{2}}{n^{2}}\left[ \frac{3}{4}- \frac{n}{l+1/2} \right]$$
**Fine structure, spin-orbit coupling**
$$H_{2}'=\frac{Ze^{2}}{8m^{2}c^{2}\pi \varepsilon_{0}r^{3}}\mathbf{L}\cdot \mathbf{S},\qquad \Delta E_{2}=\left\{\begin{align}
&-\frac{E_{n}}{2}\frac{(Z\alpha)^{2}}{ nl\left( l+ \frac{1}{2} \right)(l+1) }&\text{if }j=l+ \frac{1}{2} \\
&\frac{E_{n}}{2}\frac{(Z\alpha)^{2}}{ nl\left( l+ \frac{1}{2} \right)(l+1) }&\text{if }j=l- \frac{1}{2} \\
&0&\text{if }j=\frac{1}{2}
\end{align}\right.$$
**Fine structure, Darwin term**
$$H_{3}'=\frac{\pi \hbar^{2}}{2m^{2}c^{2}}\left( \frac{Ze^{2}}{4\pi \varepsilon_{0}} \right)\delta(\mathbf{r}), \qquad \Delta E_{3}=-E_{n} \frac{(Z\alpha)^{2}}{n}\quad\text{if }l=0\text{, no correction otherwise}$$
### Two-electron atom
**Hamiltonian**
$$\hat{H}=\underbrace{ - \frac{\hbar^{2}}{2m}\nabla ^{2}_{r_{1}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{1}} }_{ \text{Electron 1} }\underbrace{ - \frac{\hbar^{2}}{2m}\nabla ^{2}_{r_{2}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{2}} }_{ \text{Electron 2} }+ \underbrace{ \frac{e^{2}}{4\pi \varepsilon_{0}r_{12}} }_{ e-e\text{ interaction} }$$
**Singlet state** (antisymmetric, makes parastates)
$$\chi_{0,0}=\frac{1}{\sqrt{ 2 }}[\alpha(1)\beta(2)-\alpha(2)\beta(1)]$$
**Triplet states** (all symmetric, makes orthostates)
$$\begin{align}
\chi_{1,1}&=\alpha(1)\alpha(2) \\
\chi_{1,0}&=\frac{1}{\sqrt{ 2 }}[\alpha(1)\beta(2)+\alpha(2)\beta(1)] \\
\chi_{1,-1}&=\beta(1)\beta(2)
\end{align}$$
- **Parastates** are wavefunctions where the spin component is antisymmetric (spin singlet) and the spatial component is symmetric. In independent electron model: $\Psi _\text{para}(q_{1},q_{2})=A_{+}\psi_{+}^{0}(\mathbf{r}_{1},\mathbf{r}_{2})\chi_{0,0}(1,2)$
- **Orthostates** are wavefunctions where the spin component is symmetric (spin triplet) and the spatial component is antisymmetric. In independent electron model: $\Psi _\text{ortho}(q_{1},q_{2})=A_{-}\psi_{-}^{0}(\mathbf{r}_{1},\mathbf{r}_{2})\sum_{m_{S}}\chi_{1,m_{S}}(1,2)d_{m_{S}}$

**Energy eigenvalues in independent particle model** (same for both para and ortho)
$$E_{n_1, n_2} = - \frac{mZ^{2}}{2\hbar^{2}} \frac{ e^{4} }{(4 \pi \epsilon_{0})^{2}} \left( \frac{1}{n_{1}^{2}} + \frac{1}{n_{2}^{2}} \right)$$
**Fine structure, spin-orbit coupling**
$$\Delta E_{SO}=\frac{\xi}{2}[J(J+1)-L(L+1)-S(S+1)]$$
where $\xi$ is the coupling constant. Even without $\xi$, it is useful to know if splitting occurs.
### Many-electron atom
**Hamiltonian**
$$H=\sum_{i=1}^{N}\underbrace{ \left[  - \frac{\hbar^{2}}{2m}\nabla ^{2}_{\mathbf{r}_{i}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{i}} \right] }_{ \text{Individual electrons} }+\sum_{i>j} \underbrace{ \frac{e^{2}}{4\pi \varepsilon_{0}r_{ij}} }_{ e-e\text{ interaction} } $$
**Slater determinant**
$$\Psi_{C}(q_{1},q_{2},\ldots,q_{n})=\frac{1}{\sqrt{ N! }}\begin{vmatrix}
u_{\alpha}(q_{1}) & u_{\beta}(q_{1}) & \ldots & u_{v}(q_{1}) \\
u_{\alpha}(q_{2}) & u_{\beta}(q_{2}) & \ldots & u_{v}(q_{2}) \\
\vdots \\
u_{\alpha}(q_{N}) & u_{\beta}(q_{N}) & \ldots & u_{v}(q_{N})
\end{vmatrix}$$
where $u$ are single-electron eigenfunctions, $\boldsymbol{\alpha}..,\nu$ are sets of quantum numbers $(n,l,m,m_{s})$, $N$ is number of electrons.
**Fine structure**
$$H_{1}=\sum_{i>j} \frac{e^{2}}{4\pi \varepsilon_{0}r_{ij}}-\sum_{i=1}^{N} V_{C}(r_{i}),\quad H_{2}\equiv \sum_{i}\xi(\mathbf{r}_{i})\mathbf{L}_{i}\cdot \mathbf{S}_{i}\quad \text{where }\xi(\mathbf{r}_{i})=\frac{1}{2m^{2}c^{2}} \frac{1}{r_{i}} \frac{dV(r_{i})}{dr_{i}}$$
**L-S coupling**
Only when $H_{1}\gg H_{2}$ (small/medium $Z$). Uses term notation ($n^{2S+1}L_{J}$).
**j-j coupling**
Only when $H_{2}\gg H_{1}$ (high $Z$). Splits energy levels, which now depend on $j=l+s$ as $E_{nlj}$ with degeneracy $2j+1$.
### Hund's rules
**Hund's rules** are a set of rules that explain how [[electron|electrons]] organize around an [[atom]]. They were originally found empirically and then developed theoretically later on.
1. Complete [[electron shell model|electron shells]] have $L=S=0$. The values of $L$ and $S$ are determined exclusively by the incomplete shells.
2. Equivalent electrons (electrons with the same $l$) are arranged so as to maximize $S$ because states with higher multiplicity have lower [[energy|energies]].
3. Electrons are arranged so as to maximize $m_{L}=\sum m_{l}$.
4. In multiplets with subshells that are less than half filled, the term with *lowest* $j$ has the lowest energy. In multiplets with subshells that are more than half filled, the term with *highest* $j$ has the lowest energy.
### Born-Oppenheimer approximation
Approximation for diatomic molecules. Nuclei are orders of magnitude more massive, so their motion is tiny in comparison to the electrons. As such, they are considered stationary and their kinetic terms are removed from the Hamiltonian.
$$\begin{align}
H&=\sum_{i=1}^{N_{e}}- \frac{\hbar^{2}}{2m}\nabla ^{2}_{\mathbf{r}_{i}}-\sum_{i} \frac{Z_{A}e^{2}}{4\pi \varepsilon_{0}\lvert \mathbf{r}_{i}-\mathbf{R}_{A} \rvert } - \sum _{i} \frac{Z_{B}e^{2}}{4\pi \varepsilon_{0}\lvert \mathbf{r}_{i}-\mathbf{R}_{B} \rvert } \\
&+\sum_{i>j} \frac{e^{2}}{4\pi \varepsilon_{0}\lvert \mathbf{r}_{i}-\mathbf{r}_{j} \rvert }+ \frac{Z_{A}Z_{B}e^{2}}{4\pi \varepsilon_{0}R}
\end{align}$$
#### Hydrogen-hydrogen ion molecule
**Hamiltonian**
$$H=\frac{\hbar^{2}}{2m}\nabla_{r}^{2}- \frac{e^{2}}{4\pi \varepsilon_{0}}\left( \frac{1}{r}+ \frac{1}{\mathfrak{r}} \right)\quad\text{where }\mathfrak{r}=\sqrt{ r^{2}+R^{2}-2rR\cos \theta }$$
Use ground state orbital $\psi_{100}(r)$ for electron, then LCAO $\psi=S[\psi_{100}(r)+\psi_{100}(\mathfrak{r})]$ and normalize it. Only cross-state remains. Superposition integral $I$ not solved in class. Normalization constant is $\lvert S \rvert^{2}=1/2(1+I)$. Energy eigenstate is $\braket{ \psi | H | \psi }$. Direct $C$ and swap $D$ terms come up (avg in same orbital; avg across across orbitals). Energy is
$$E_{\ket{\psi} }=\langle H \rangle_{\psi} =\left[ 1+ 2 \frac{C+D}{1+I} \right]E_{1}$$
$E_{1}$ is ground state ($n=1$).
#### General homogeneous diatomic
**Energy**
$$E=E_{0}+\Delta E=E_{0}+ \frac{C+D}{1\pm S}$$
**Bonding (gerade; even), antibonding (ungerade; odd) wavefunctions**
From LCAO $\Phi\equiv c_{1}\phi_{a}+c_{2}\phi_{b}$:
$$\Phi_{g}=c(\phi_{a}+\phi_{b}),\quad \Phi_{u}=c(\phi_{a}-\phi_{b})$$
### Non-crossing rule
Electronic states, represented by their potentials $E(R)$, that have the same symmetries never cross when varying internuclear distance $R$. In other words, given two distinct electronic states $E_{1}(R)$ and $E_{2}(R)$, there does *not* exist an $R_{C}$ for which $E_{1}(R_{C})=E_{2}(R_{C})$.
### Nuclear motion in molecules
**Vibrational eigenvalues as harmonic oscillator**
$$E_{v}=\hbar \sqrt{ \frac{k}{\mu} }\left( v+ \frac{1}{2} \right)=\omega\left( v+ \frac{1}{2} \right)$$
$2\omega$ is the distance between bands/spectral lines because $\Delta v=\pm 1$ selection rule. Rather large, $\sim 50\textendash 200\text{ eV}$.
**With anharmonic correction** ($\chi$ some constant)
$$E_{v}=\omega\left( v+ \frac{1}{2} \right)-\omega \chi\left( v+ \frac{1}{2} \right)^{2}$$
**Rotational eigenvalues as rigid rotor**
$$E_{r}=\frac{\hbar^{2}}{2\mu R_{0}^{2}}J(J+1)=BJ(J+1)$$
$2B$ is distance between bands/spectral lines because $\Delta J=\pm1$ selection rule implying $\Delta J=\pm 1\quad\to \quad \hbar \omega=2B(J+1)$. Very small, $\sim 10^{-4}\text{ eV}$.
**With centrifugal distorsion** ($\Delta$ some constant)
$$E_{r}=BJ(J+1)-\Delta J^{2}(J+1)^{2}$$
### Transitions
**Matrix element from dipole moment $\mathbf{D}$**
$$M_{fi}=\braket{ \Psi_{fi} | \mathbf{D}| \Psi_{if} }\quad\text{where}\quad\mathbf{D}=-e\sum_{i}\mathbf{r}_{i}+e\sum_{j}z_{j}\mathbf{r}_{j} $$
**Frank-Condon principle**
Electronic state transitions can be considered instant with respect to the time scale of molecular vibrations. The internuclear separation throughout the transition can be considered constant.
### X-ray diffraction for crystal structure
Shoot X-rays, bounce off of ions on plane, path distance dependent on internal structure, diffraction makes Bragg peaks. Bragg diffraction expects specular reflection and constructive interference. Bragg condition is $n\lambda=2d\sin \theta$. $d$ is distance between planes, $\lambda$ is wavelength, $\lambda$ is reflection angle, $n$ is order.

Instead, von Laue uses general wavevectors incident $\mathbf{k}$ and reflected $\mathbf{k}'$ off an ion in some arbitrary location at distance $\mathbf{R}$. von Laue condition is $\mathbf{R}\cdot(\mathbf{k}-\mathbf{k}')=2\pi m$. $\mathbf{k}-\mathbf{k}'$ must be reciprocal lattice vector $\mathbf{K}$. Condition is equivalent to $\mathbf{k}\cdot \hat{\mathbf{K}}=\frac{1}{2}K$.

**Geometrical structure factor (lattice with basis)**
$$S_{\mathbf{K}}=\sum_{j=1}^{n} e^{i\mathbf{K}\cdot \mathbf{d}_{j}}$$
Describes how much interference between atoms in basis diminishes diffraction intensity. If $S_{\mathbf{K}}=0$, no diffraction at all.

**Atomic form factor (lattice with basis)**
$$S_{\mathbf{K}}=\sum_{j=1}^{n} f_{j}(\mathbf{K})e^{i\mathbf{K}\cdot \mathbf{d}_{j}}$$
$f_{j}$ is form factor. Matters if basis atoms aren't all the same. Describes effect of the different shapes of atoms.
### Reciprocal lattice
**Direct to reciprocal vectors (3D)**
$$\mathbf{b}_{1}=2\pi \frac{\mathbf{a}_{2}\times \mathbf{a}_{3}}{\mathbf{a}_{1}\cdot(\mathbf{a}_{2}\times \mathbf{a}_{3})},\quad \mathbf{b}_{2}=2\pi \frac{\mathbf{a}_{3}\times \mathbf{a}_{1}}{\mathbf{a}_{1}\cdot(\mathbf{a}_{2}\times \mathbf{a}_{3})},\quad \mathbf{b}_{3}=2\pi \frac{\mathbf{a}_{1}\times \mathbf{a}_{2}}{\mathbf{a}_{1}\cdot(\mathbf{a}_{2}\times \mathbf{a}_{3})}$$
### Sommerfeld free electron model
1. The $N$ electrons are confined in a cubic volume $V=L^{3}$.
2. The electrons are independent. There is no interaction between electrons.
3. The electrons are free. There is no interaction between electrons and ions.

Then solve a Fermi gas is Born-von Karman periodic boundary conditions. Fermi speed is $\sim 0.01c$. Fermi temperature is $T_{F}\sim 10^{4}\text{ K}$ is most metals. Wigner-Seitz radius for space partition is
$$r_{S}=\left( \frac{3}{4\pi n} \right)^{3},\qquad k_{F}=\frac{(9\pi/4)^{1/3}}{r_{S}}=\frac{1.92}{r_{S}}$$
### Ideal crystal
**Hamiltonian**
$$\begin{align}
H&=\underbrace{ \sum_{i} \frac{p_{i}^{2}}{2m_{i}}+ \sum_{j} \frac{P_{j}^{2}}{2M_{j}} }_{ \text{Kinetic terms} }+ \underbrace{ \frac{1}{2}\sum_{j,j'} \frac{Z_{j}Z_{j'}e^{2}}{\lvert \mathbf{R}_{j}-\mathbf{R}_{j'} \rvert } }_{ \text{Ion-ion interaction} }+ \underbrace{ \frac{1}{2}\sum_{i,i'} \frac{e^{2}}{\lvert \mathbf{r}_{i}-\mathbf{r}_{i'} \rvert } }_{ \text{Electron-electron interaction} }-\underbrace{ \sum_{i,j} \frac{Z_{j}e^{2}}{\lvert \mathbf{r}_{i}-\mathbf{R}_{j} \rvert } }_{ \text{Ion-electron interaction} } \\
&\equiv H_\text{ions}(R_{i})+H_{e}(r_{i},R_{j})+H_\text{e-ion}(r_{i},\delta R_{j})
\end{align}
$$
1. Only outer shell electrons matter.
2. Born-Oppenheimer approximation. Nuclei are stationary.
#### Vibrations
In practice, nuclei aren't actually stationary. Vibrations can only be explained with nuclear motion. We assume that the mean equilibrium position $\langle \mathbf{R} \rangle$ of an ion is stationary. In the harmonic approximation, the displacement from $\langle \mathbf{R} \rangle$ is small w.r.t space between ions (ion oscillations are small), then the potential is Taylor expanded and only up to second order is retained. Energy then is $U=U_\text{equilbrium}+U_\text{harmonic}$. Former is electrostatic, latter is harmonic oscillations. Basically you get ions connected to each other by springs of elastic constant $\gamma$. In 1D monoatomic lattice, solving $M\ddot{u}=-\frac{ \partial U }{ \partial u }$ (wave equation) with plane waves yield the **dispersion relation**
$$\omega(k)=\sqrt{ \frac{2\gamma(1-\cos(ka))}{M} }=2\sqrt{ \frac{\gamma}{M} }\left\lvert  \sin\left( \frac{ka}{2} \right)  \right\rvert $$
for the acoustic branch. In 1D diatomic lattice, you get two solutions
$$\omega ^{2}=\gamma\left( \frac{1}{M_{1}}+ \frac{1}{M_{2}} \right)\pm \gamma\sqrt{  \left( \frac{1}{M_{1}}+ \frac{1}{M_{2}} \right)^{2}- \frac{4}{M_{1}M_{2}}\sin ^{2} \frac{kb}{2}  }$$
Lower branch is acoustic, upper branch is optical (couples with electromagnetic radiation).

Energy needs to be quantized. Change harmonic oscillators to quantum version. Now vibrations have a quantum of energy: the **phonon**.
#### Electronic structure
**Periodic potential in lattice $\mathbf{R}$**
$$U(\mathbf{r})=U(\mathbf{r}+\mathbf{R})$$
**Bloch theorem**
Single-electron eigenstates in periodic potential in 3D Bravais lattice are plane waves multiplied by function with same periodicity as the lattice: $\psi_{n\mathbf{k}}(\mathbf{r})=e^{i\mathbf{k}\cdot \mathbf{r}}u_{n\mathbf{k}}(\mathbf{r})$. Equivalent condition: $\psi(\mathbf{r}+\mathbf{R})=e^{i\mathbf{k}\cdot \mathbf{R}}\psi(\mathbf{r})$. Solving the Schrödinger equation with $\psi_{n\mathbf{k}}$ (only $u_{n\mathbf{k}}$ is really needed) in a finite volume leads to infinite solutions indexed by $n$ and $\mathbf{k}$. The eigenvalues are the **energy bands** $\varepsilon_{n}(\mathbf{k})$. $\mathbf{k}$ is so closely packed it's basically continuous, $\varepsilon_{n}(\mathbf{k})$ are continuous functions. They are dispersion relations since $\varepsilon=\hbar \omega(k)$
**Behavior from bands**
- Some bands are filled. Others are empty. Probably an insulator or semiconductor.
- Some bands are partially filled. Probably a conductor.

**Weak potential**
Useful for conductors and metals. Basically a modified Sommerfeld model with Bloch waves. Solve this
$$\left( \frac{\hbar^{2}k^{2}}{2m}-\varepsilon \right)c_{\mathbf{k}}+\sum_{\mathbf{K}}U_{\mathbf{K}}c_{\mathbf{k}-\mathbf{K}}=0$$
Most $c_{\mathbf{k}}$ are set to zero because the further you get from the current electron, the less they matter. More $c_{\mathbf{k}}$ are better of course. When $U(\mathbf{r})=0$ all $U_{\mathbf{K}}=0$ and you get parabolas like in Sommerfeld model. When $U(\mathbf{r})\neq 0$, you use perturbation theory to correct the energy band $\varepsilon_{0}(\mathbf{k})$. First order $\braket{ \mathbf{k} | U |\mathbf{k} }=U_{0}\equiv 0$ because arbitrary constant in potential. Second order is nonzero. Non-degenerate correction only works outside of the edges of the Brillouin zone. At the edges states are degenerate (periodicity). In that case, must use degenerate perturbation theory as
$$\varepsilon_{0}(\mathbf{k})-E)(\varepsilon_{0}(\mathbf{k}+\mathbf{K})-E)-\lvert U_{\mathbf{K}} \rvert ^{2}=0\quad\Rightarrow \quad E_{\pm}=\varepsilon_{0}(\mathbf{k})\pm \lvert U_{\mathbf{K}} \rvert $$
$2\lvert U_{\mathbf{K}} \rvert$ is the **gap** between the corrected bands. This breaks a band into multiple ones. Big gaps make conduction hard because states inside gaps are unavailable.

**Tight-binding**
Useful for insulators and semiconductors. Start from free atoms, then join them together and see what happens to the atomic orbitals when they superimpose. Assumes superposition is small. Solve this
$$\begin{align}
\hat{H}_\text{solid}&=- \frac{\hbar^{2}\nabla^{2}}{2m}+\sum_{\mathbf{R}}U_\text{atom}(\mathbf{r}-\mathbf{R}) \\
&=- \frac{\hbar^{2}\nabla^{2}}{2m}+U_\text{atom}(\mathbf{r})+\sum_{\mathbf{R}\neq 0}U_\text{atom}(\mathbf{r}-\mathbf{R}) \\
&=\hat{H}_\text{atom}+\mathcal{U}(\mathbf{r})
\end{align}$$
Eigenvalues now have a pure atom contribution and a $\mathcal{U}$ correction. Bands become
$$E(\mathbf{k})=E_{n}-\beta-\sum_{\mathbf{R}\neq 0}t(\mathbf{R})e^{i\mathbf{k}\cdot \mathbf{R}}$$
$\beta$ is the $\mathcal{U}$ contribution. $t$ is the **hopping term** (chance of electron hopping to from one ion to another). Only $t$ determines electron across the solid, so it's the only term that contributes to band width ($t_{0}=0$ makes a constant, zero-width energy band). Each band in this model is associated with a molecular orbital kind ($\sigma$-band, $\pi$-band...). Near minima of $k$, tight-binding is mathematically equivalent to a free electron model with electron mass $m^{*}=\hbar^{2}/2ta^{2}$.
### Useful formulas
**Wavenumber to energy**
Most energies in spectroscopy are given as inverse lengths (wavenumbers), often $\text{cm}^{-1}$. These are ordinary wavenumbers $\tilde{\nu}$, not angular wavenumbers $k=\tilde{\nu}/2\pi$. The actual energy depends on the frequency $\nu$ (or angular frequency $\omega=\nu/2\pi$) by the Planck formula $E=h\nu=\hbar \omega$. To go from wavenumber to frequency, you need the dispersion relation $\nu(\tilde{\nu})$ or $\omega(k)$. In the vacuum this is just $\nu=c \tilde{\nu}$ or $\omega=ck$, so $E=hc \tilde{\nu}=\hbar ck$.