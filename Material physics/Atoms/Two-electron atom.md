---
wiki-publish: true
---
The **two-electron atom** is a [[physical system]] modeling an [[atom]] with two [[elettrone|electron]] around and arbitrary [[Nucleo atomico|nucleus]]. It is a generalization of the [[Hydrogen atom|hydrogenic atom]]. The key challenge of the system is the [[Identical particles|indistinguishability]] of electrons. The [[Hamiltonian]] of the system is
$$\hat{H}=- \frac{\hbar^{2}}{2m}\nabla ^{2}_{r_{1}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{1}}- \frac{\hbar^{2}}{2m}\nabla ^{2}_{r_{2}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{2}}+ \frac{e^{2}}{4\pi \varepsilon_{0}r_{12}}$$

![[Diagram Two electrom atom|50%]]
### Spin states
The solved [[Equazione agli autovalori|eigenfunction]] (in [[Rappresentazioni dello stato|position representation]]) will be of the form $\Psi\equiv \Psi(q_{1},q_{2})$, where $q_{1}$ and $q_{2}$ are the coordinates of the electrons. Electrons are [[spin]] $1/2$ [[Fermion|fermions]] and so $\Psi$ must be an [[Permutation operator|antisymmetric state]]: $\Psi(q_{1},q_{2})=-\Psi(q_{2},q_{1})$. Since $\hat{H}$ does not directly depend on spin, we can factor out the spin and leave a coordinate-only and spin-only [[Funzione d'onda|wave function]]:
$$\Psi(q_{1},q_{2})=\psi (\mathbf{r}_{1},\mathbf{r}_{2})\chi(1,2)$$
The spin wave functions $\chi(1,2)$ can be constructed from the more general $\chi_{1/2,m_{s}}(1)$ and $\chi_{1/2,m_{s}}(2)$. We denote $\mathbf{S}_{1}$ and $\mathbf{S}_{2}$ the spin operators of the electrons and by $(S_{1})_{z}$ and $(S_{2})_{z}$ their $z$ components. We denote the basic spin functions of the electrons $\alpha(1)$, $\beta(1)$, $\alpha(2)$ and $\beta(2)$. $\mathbf{S}_{1}$ only acts on $\alpha(1)$ and $\beta(1)$, whereas $\mathbf{S}_{2}$ only acts on $\alpha(2)$ and $\beta(2)$. In turn, this means that $\mathbf{S}_{1}$ and $\mathbf{S}_{2}$ [[Commutator|commute]].

The total spin is $\mathbf{S}=\mathbf{S}_{1}+\mathbf{S}_{2}$ and the total $z$ component is $S_{z}=(S_{1})_{z}+(S_{2})_{z}$. The square of the total is
$$\mathbf{S}^{2}=\mathbf{S}_{1}^{2}+\mathbf{S}_{2}^{2}+2\mathbf{S}_{1}\cdot \mathbf{S}_{2}=\frac{3}{2}+2\mathbf{S}_{1}\cdot \mathbf{S}_{2}$$
since $\mathbf{S}_{1}^{2}=\mathbf{S}_{2}^{2}=3/4$. Since the interaction between electrons is purely [[Interazione elettromagnetica|electromagnetic]], it is independent of spin. As such, each electron's spin is simply either up $(\uparrow)$ or down $(\downarrow)$ without reference to the other, which leads to four distinct spin states:
$$\begin{align}
\chi_{1}(1,2)&=\alpha(1)\alpha(2)&\uparrow\uparrow \\
\chi_{2}(1,2)&=\alpha(1)\beta(2)&\uparrow\downarrow \\
\chi_{3}(1,2)&=\beta(1)\alpha(2)&\downarrow\uparrow \\
\chi_{4}(1,2)&=\beta(1)\beta(2)&\downarrow\downarrow
\end{align}$$
Applying the $z$ spin operator to $\chi_{1}$ leads to
$$\begin{align}
S_{z}\chi_{1}(1,2)&=[(S_{1})_{z}+(S_{2})_{z}]\alpha(1)\alpha(2) \\
&=[(S_{1})_{z}\alpha(1)]\alpha(2)+\alpha(1)[(S_{2})_{z}\alpha(2)] \\
&=\frac{1}{2}\alpha(1)\alpha(2)+ \frac{1}{2}\alpha(1)\alpha(2) \\
&=\alpha(1)\alpha(2) \\
&=\chi_{1}(1,2)
\end{align}$$
Clearly, the total spin over $z$ in the $\chi_{1}$ spin state is $1$ (in $\hbar$ units). More generally, we have
$$S_{z}\chi=M_{S}\chi$$
By doing the math for all four $\chi_{i}$ functions, we find that $M_{S}=1,0,0,-1$, in that order. There's evidently some [[Degenerazione|degeneracy]] on $M_{S}=0$. Moreover, while $\chi_{1}$ and $\chi_{4}$ are [[Permutation operator|symmetric]] under label exchange, $\chi_{2}$ and $\chi_{3}$ are not, and are also not [[Permutation operator|antisymmetric]]. As such, the *actual* $M_{S}=0$ state must be a [[Normalization|normalized]] [[linear combination]] of the two that *is* (anti)symmetric under label exchange:
$$\chi_{\pm}=\frac{1}{\sqrt{ 2 }}[\alpha(1)\beta(2)\pm\alpha(2)\beta(1)]$$
The $+$ is symmetric, the $-$ is antisymmetric. These two functions are eigenstates of $\mathbf{S}^{2}$ and $S_{z}$, with eigenvalues $S_{z}=1$ and $M_{S}=0$ for $+$ and $S_{z}=0$ and $M_{S}=0$ for $-$. We now have four spin states, divided in one state for $S_{z}=0$ and three states $S_{z}=1$. The former is called the **singlet state**
$$\chi_{0,0}=\frac{1}{\sqrt{ 2 }}[\alpha(1)\beta(2)-\alpha(2)\beta(1)]$$
and is antisymmetric. The latter three are known as the **triplet states**
$$\begin{align}
\chi_{1,1}&=\alpha(1)\alpha(2) \\
\chi_{1,0}&=\frac{1}{\sqrt{ 2 }}[\alpha(1)\beta(2)+\alpha(2)\beta(1)] \\
\chi_{1,-1}&=\beta(1)\beta(2)
\end{align}$$
and are all symmetric. At this point, since the wave functions that describe a two-electron atom must be antisymmetric (because we're working with fermions), we only have two options:
- **Parastates** are wavefunctions where the spin component is antisymmetric (spin singlet) and the spatial component is symmetric.
- **Orthostates** are wavefunctions where the spin component is symmetric (spin triplet) and the spatial component is antisymmetric.
### Independent particle model
The electrons obviously repel each other electrically. However, as a first, somewhat qualitative approximation, we can solve the system by neglecting the interaction term. This makes for two independent electrons around the same nucleus. Following [[Teoria delle perturbazioni|perturbation theory]], we rewrite the Hamiltonian as
$$H=H_{0}+H'$$
(More Bransden page 258+)

$H_{0}$ is invariant under particle exchange, so we can choose the wave functions to be either even or odd under exchange:
$$\Psi^{0}_{\pm}(\mathbf{r}_{1},\mathbf{r}_{2})=\frac{1}{\sqrt{ 2 }}(\Psi_{n_{1},l_{1},m_{1}}(\mathbf{r}_{1})\Psi_{n_{2},l_{2},m_{2}}(\mathbf{r}_{2})\pm \Psi_{n_{1},l_{1},m_{1}}(\mathbf{r}_{2})\Psi_{n_{2},l_{2},m_{2}}(\mathbf{r}_{1}))$$
In this approximation, symmetric and antisymmetric states have the same energy, which is the eigenvalue of $H_{0}\Psi^{0}_{\pm}(\mathbf{r}_{1},\mathbf{r}_{2})=E^{0}_{n_{1},n_{2}}\Psi^{0}_{\pm}(\mathbf{r}_{1},\mathbf{r}_{2})$ and comes out to be
$$E^{0}_{n_{1},n_{2}}=- \frac{Z^{2}}{2}\left[ \frac{1}{n_{1}^{2}}+ \frac{1}{n_{2}^{2}} \right]$$
A note: if $n_{1},l_{1},m_{1}=n_{2},l_{2},m_{2}$, the antisymmetric combination vanishes. This is correct and what we'd hoped for. After all, this is really just the [[Pauli exclusion principle]] at play: two electrons cannot possibly have the same quantum numbers at the same time. In fact, if two electrons have the same spatial state, their spins must differ (i.e., be opposite), but if the spins are opposite then the total spin is zero ($S_{z}=0$), which always ends up being a singlet state, a parastate.

For parastates and orthostates to not have the same energy we must surrender the approximation and consider the actual interaction between electrons.

> [!example] A measure of mistakes
> Every time we make an approximation, it's fair (and responsible) to check how far from reality the approximation is. Luckily, we can do that here, because we have some experimental measurements. A helium atom ($Z=2$) in the ground state has, according to the formula above, energy $E^{0}=-108.8\text{ eV}$. Experimental results instead give $E_{0}=-79.0\text{ eV}$. That's a ~30% difference: not exactly something you can justifiably ignore. Evidently, electron repulsion is *important*, enough so that we cannot realistically ignore it. The repulsion increases the state energy and our approximation gravely underestimates it.
> 
> For what it's worth, the approximate ground state wavefunction is
> $$\Psi_{0}(r_{1},r_{2})=\Psi_{100}(r_{1})\Psi_{100}(r_{2})=\frac{8}{\pi a^{3}}e^{-2(r_{1}+r_{2})/a}$$
> 
> The error grows larger the smaller $Z$ is and because tolerable for large $Z$. For hydrogen ($Z=1$), the error is around 40%, but for carbon ($Z=6$) it's already down to about 10%. In some cases, this quite useful: provided that the [[valence shell]] of an atom (realistically an [[ion]]) is made up of only two electrons, this can be applied with decent results if the atom is large enough.
### Variational model
Much better results can be obtained by applying the [[variational method]]. Specifically, we allow the nuclear charge $Z$ to be the variable quantity; it is no longer a constant and we are looking for an *effective* nuclear charge $Z_{e}$. To start, we need a trial function. We'll use
$$\phi(r_{1},r_{2})=\frac{Z_{e}^{3}}{\pi a^{3}}e^{-Z_{e}(r_{1}+r_{2})/a}=\Psi_{1s}^{Z_{e}}(r_{1})\Psi_{1s}^{Z_{e}}(r_{2})$$
where
$$\psi_{1s}^{Z_{e}}(r)=\left( \frac{Z_{e}^{3}}{\pi a^{3}} \right)^{1/2}e^{Z_{e}r/a}$$
We need to evaluate
$$E(\phi)=\frac{\braket{ \phi | H|\phi }}{\braket{ \phi | \phi } } =\braket{ \phi | H | \phi } $$
since $\braket{ \phi | \phi }=1$. Ignoring the constants, our $H$ is
$$H=\nabla_{1}^{2}+\nabla_{2}^{2}-\left( \frac{Z_{e}}{r_{1}}+ \frac{Z_{e}}{r_{2}}- \frac{1}{r_{12}} \right)$$
Since $\braket{ \phi | A+B | \phi }=\braket{ \phi | A | \phi }+\braket{ \phi | B | \phi }$, we can calculate these term separately. The "kinetic" terms (the first two) end up being
$$\langle H \rangle _{\phi}=2Z^{2}E_{1}$$
The latter three becomes
$$\langle H \rangle _{\phi}= 2(Z-2) \frac{e^{2}}{4\pi \varepsilon_{0}} \left\langle  \frac{1}{r_{12}}  \right\rangle_{\phi} +\langle V_{ee} \rangle_{\phi} $$
The distance average is
$$\braket{ \phi | \frac{1}{r_{12}} | \phi } =\frac{5}{8}Z_{e}$$
???
Putting it all together we get
$$Z_{e}=Z- \frac{5}{16}$$
As it happens, the effective charge is reduced by a constant.