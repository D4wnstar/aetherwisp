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
**Singlet state** (antisymmetric)
$$\chi_{0,0}=\frac{1}{\sqrt{ 2 }}[\alpha(1)\beta(2)-\alpha(2)\beta(1)]$$
**Triplet states** (all symmetric)
$$\begin{align}
\chi_{1,1}&=\alpha(1)\alpha(2) \\
\chi_{1,0}&=\frac{1}{\sqrt{ 2 }}[\alpha(1)\beta(2)+\alpha(2)\beta(1)] \\
\chi_{1,-1}&=\beta(1)\beta(2)
\end{align}$$
- **Parastates** are wavefunctions where the spin component is antisymmetric (spin singlet) and the spatial component is symmetric. In independent electron model: $\Psi _\text{para}(q_{1},q_{2})=A_{+}\psi_{+}^{0}(\mathbf{r}_{1},\mathbf{r}_{2})\chi_{0,0}(1,2)$.
- **Orthostates** are wavefunctions where the spin component is symmetric (spin triplet) and the spatial component is antisymmetric. In independent electron model: $\Psi _\text{ortho}(q_{1},q_{2})=A_{-}\psi_{-}^{0}(\mathbf{r}_{1},\mathbf{r}_{2})\sum_{m_{S}}\chi_{1,m_{S}}(1,2)d_{m_{S}}$.

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
Only when $H_{1}\gg H_{2}$ (small/medium $Z$). Uses term notation ($^{2S+1}L$).
**j-j coupling**
Only when $H_{2}\gg H_{1}$ (high $Z$). Splits energy levels, which now depend on $j=l+s$ as $E_{nlj}$ with degeneracy $2j+1$.
### Hund's rules
**Hund's rules** are a set of rules that explain how [[electron|electrons]] organize around an [[atom]]. They were originally found empirically and then developed theoretically later on.
1. Complete [[electron shell model|electron shells]] have $L=S=0$. The values of $L$ and $S$ are determined exclusively by the incomplete shells.
2. Equivalent electrons (electrons with the same $l$) are arranged as to maximize $S$. States with higher multiplicity have lower [[energy|energies]].
3. Electrons are arranged as to maximize $m_{L}=\sum m_{l}$.
4. In multiplets with subshells that are less than half filled, the term with *lowest* $j$ has the lowest energy. In mutliplets with subshells that are more than half filled, the term with *highest* $j$ has the lowest energy.
### Born-Oppenheimer approximation
Approximation for diatomic molecules. Nuclei are orders of magnitude more massive, so their motion is tiny in comparison to the electrons. As such, they are considered stationary and their kinetic terms are removed from the Hamiltonian.
$$\begin{align}
H&=\sum_{i=1}^{N_{e}}- \frac{\hbar^{2}}{2m}\nabla ^{2}_{\mathbf{r}_{i}}-\sum_{i} \frac{Z_{A}e^{2}}{4\pi \varepsilon_{0}\lvert \mathbf{r}_{i}-\mathbf{R}_{A} \rvert } - \sum _{i} \frac{Z_{B}e^{2}}{4\pi \varepsilon_{0}\lvert \mathbf{r}_{i}-\mathbf{R}_{B} \rvert } \\
&+\sum_{i>j} \frac{e^{2}}{4\pi \varepsilon_{0}\lvert \mathbf{r}_{i}-\mathbf{r}_{j} \rvert }+ \frac{Z_{A}Z_{B}e^{2}}{4\pi \varepsilon_{0}R}
\end{align}$$
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
### Useful formulas
**Wavenumber to energy**
Most energies in spectroscopy are given as inverse lengths (wavenumbers), often $\text{cm}^{-1}$. These are ordinary wavenumbers $\tilde{\nu}$, not angular wavenumbers $k=\tilde{\nu}/2\pi$. The actual energy depends on the frequency $\nu$ (or angular frequency $\omega=\nu/2\pi$) by the Planck formula $E=h\nu=\hbar \omega$. To go from wavenumber to frequency, you need the dispersion relation $\nu(\tilde{\nu})$ or $\omega(k)$. In the vacuum this is just $\nu=c \tilde{\nu}$ or $\omega=ck$, so $E=hc \tilde{\nu}=\hbar ck$.