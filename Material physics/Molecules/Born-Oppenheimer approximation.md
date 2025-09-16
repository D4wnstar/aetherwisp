---
wiki-publish: true
aliases:
  - adiabatic approximation
---
The **Born-Oppenheimer approximation**, also called the **adiabatic approximation**, is a computational method to solve the quantum [[Funzione d'onda|wavefunction]] of a diatomic [[molecule]] and thus determine their [[molecular orbital|molecular orbitals]]. It is based on the following simplification: the motion of the [[Atomic nucleus|nuclei]] is considerably slower than that of the [[Electron|electrons]] and can thus be considered stationary, removing the nuclear kinetic terms from the [[Hamiltonian]]. The positions of the nuclei are then constant parameters and not variables, which also decouples them from the motion of the electrons. The **electronic wavefunctions** are then treated separately from the nuclear ones.

The Hamiltonian becomes
$$\begin{align}
H&=\sum_{i=1}^{N_{e}}- \frac{\hbar^{2}}{2m}\nabla ^{2}_{\mathbf{r}_{i}}-\sum_{i} \frac{Z_{A}e^{2}}{4\pi \varepsilon_{0}\lvert \mathbf{r}_{i}-\mathbf{R}_{A} \rvert } - \sum _{i} \frac{Z_{B}e^{2}}{4\pi \varepsilon_{0}\lvert \mathbf{r}_{i}-\mathbf{R}_{B} \rvert } \\
&+\sum_{i>j} \frac{e^{2}}{4\pi \varepsilon_{0}\lvert \mathbf{r}_{i}-\mathbf{r}_{j} \rvert }+ \frac{Z_{A}Z_{B}e^{2}}{4\pi \varepsilon_{0}R}
\end{align}$$
In order, the terms are:
1. The [[kinetic energy]] of the electrons.
2. The electric [[potential energy]] of the electrons due to nucleus $A$.
3. The electric potential energy of the electrons due to nucleus $B$.
4. The electric potential energy of the electrons due to other electrons.
5. The electric potential energy of one nucleus due to the other.
where:
- $\mathbf{r}_{i}$ is the position of the $i$-th electron.
- $\mathbf{R}_{A}$ and $\mathbf{R}_{B}$ are the positions of nuclei $A$ and $B$.
- $R=\lvert \mathbf{R}_{A}-\mathbf{R}_{B} \rvert$ is the distance between nuclei.
- $N_{e}$ is the number of electrons.

Parametrically, the solutions depend on $R$ as
$$H_{e}\Phi_{q\{  \mathbf{R} \}}(\mathbf{r}_{1},\ldots,\mathbf{r}_{N_{e}})=E_{q}\Phi_{q\{ \mathbf{R} \}}(\mathbf{r}_{1},\ldots,\mathbf{r}_{N_{e}})$$
After fixing an electronic state, the values $E_{q}(\mathbf{R})$ depend on the positions of the nuclei and so the Hamiltonian that describes the motion of the nuclei is
$$H_{N}=- \frac{\hbar^{2}}{2M_{A}}\nabla ^{2}_{R_{A}}- \frac{\hbar^{2}}{2M_{B}}\nabla ^{2}_{R_{B}}+ E_{q}(\mathbf{R})$$
In the [[center of mass]] [[frame of reference]] this is
$$\left[ - \frac{\hbar^{2}}{2\mu}\nabla ^{2}_{\mathbf{R}}+E_{q}(\mathbf{R}) \right]F(\mathbf{R})=E_\text{tot}F(\mathbf{R})$$
using the reduced mass $\mu=M_{A}M_{B}/(M_{A}+M_{B})$.
### The hydrogen-hydrogen ion molecule
One way to solve the system is to use the [[variational method]], letting the distance between nuclei $R$ be the variable parameter. We'll use the [[hydrogen atom]] as an introductory example since we can solve the system exactly. Our goal is to test the simplest possible molecule, $\text{H}\textendash\text{H}^{+}$, so a molecule composed of one hydrogen atom and a hydrogen [[ion]] (literally just a [[proton]]). Our two nuclei are simple protons and we only have a single electron. For the molecule to be possible, its ground state energy must be negative: this way it will a bound state that the system can stabilize into.

The Hamiltonian is
$$H=\frac{\hbar^{2}}{2m}\nabla_{r}^{2}- \frac{e^{2}}{4\pi \varepsilon_{0}}\left( \frac{1}{r}+ \frac{1}{\mathfrak{r}} \right)$$
where $\mathfrak{r}=\sqrt{ r^{2}+R^{2}-2rR\cos \theta }$ and we ignored the interaction between nuclei since it's constant and we only need a variational analysis. The ground state wavefunction of an electron in the hydrogen atom is
$$\psi_{100}(r)=\frac{1}{\sqrt{ \pi a^{3} }}e^{-r/a}$$
This will be our trial function. For brevity we'll write $\psi_{100}\equiv \psi_{0}$. We'll use what's called a **[[Linear Combination of Atomic Orbitals]]** (or **LCAO** for short):
$$\psi=S[\psi_{100}(r)+\psi_{100}(\mathfrak{r})]$$
 where $S$ is a [[normalization]] constant. We are taking a [[linear combination]] of [[atomic orbital|atomic orbitals]]. It is not the most accurate or general solution, but the benefit is that it is quick and easy to set up: it's just a sum. For this wave function to be a realizable state, it must be [[Normalization|normalized]], so
$$1=\int \lvert \psi \rvert ^{2}d\tau=\lvert S\rvert ^{2}\left[ \underbrace{ \int \psi_{0}(r)^{2}d\tau }_{ 1 }+ \underbrace{ \int \psi_{0}(\mathfrak{r})^{2}d\tau }_{ 1 }+2\int \psi_{0}(r)\psi_{0}(\mathfrak{r})d\tau \right]$$
The first two integrals are trivial because physically realizable states are always normalized. The last one can be solved by substituting the definition of $\psi$ above (and changing to [[spherical coordinates]]):
$$I=\frac{1}{\pi a^{3}}\int e^{-r/a}e^{-\sqrt{ r^{2}+R^{2}-2rR\cos \theta }/a}R^{2}\sin \theta drd\theta d\phi$$
It can be solved by setting $\sqrt{ r^{2}+R^{2}-2rR\cos \theta }=y$[^1]. It results in
$$I=e^{-R/a}\left[ 1+ \left( \frac{R}{a} \right)+ \frac{1}{3}\left( \frac{R}{a} \right)^{2} \right]$$
and is known as the **superposition integral**. The normalization constant ends up being
$$\lvert S\rvert ^{2}=\frac{1}{2(1+I)}$$
With a known wavefunction, we can now evaluate the energy in that state:
$$E_{\ket{\psi} }=\braket{ \psi | H | \psi } =E_{1}-2\lvert S\rvert ^{2}\left( \frac{e^{2}}{4\pi \varepsilon_{0}} \right)\left[ \underbrace{ \left\langle  \psi_{0}(r)\left| \frac{1}{\mathfrak{r}}\right| \psi_{0}(r)  \right\rangle }_{ \text{Direct} }+ \underbrace{ \left\langle  \psi_{0}(r)\left| \frac{1}{\mathfrak{r}}\right| \psi_{0}(\mathfrak{r}) \right\rangle }_{ \text{Swap} }  \right]$$
The position-dependent terms in brackets are known as the **direct** and **swap** terms and denote them as $C$ and $D$ respectively. The direct term comes from the electromagnetic interaction between an electron on a nucleus with the *other* nucleus. The swap term relies on the superposition of wave functions of $r$ and $\mathfrak{r}$, hence "swap". The factor of $2$ comes from the fact that the interaction is symmetric and indexes can be switched, leading to the same term twice. All in all, the state energy is
$$E_{\ket{\psi} }=\langle H \rangle_{\psi} =\left[ 1+ 2 \frac{C+D}{1+I} \right]E_{1}$$
Using, say, computational methods, we can graph this function to achieve something of this sort:

![[Plot Hydrogen-hydrogen ion ground state|90%]]

We can see that the energy actually is negative and has a minimum where the molecule can stabilize into. The molecule is possible![^2]
### Generalizing
We are now ready to generalize the previous discussion to, ideally, any diatomic molecule. We are looking for solutions of the kind
$$\Phi\equiv c_{1}\phi_{a}+c_{2}\phi_{b}$$
and we need some way to determine $c_{1}$ and $c_{2}$. The [[Equazione di Schrödinger|Schrödinger equation]] reads
$$\left( \underbrace{ - \frac{\hbar^{2}}{2m}\nabla ^{2}- \frac{e^{2}}{4\pi \varepsilon_{0}r_{a}} }_{ H_{a} }- \frac{e^{2}}{4\pi \varepsilon_{0}r_{b}} \right)c_{1}\phi_{a}+\left( \underbrace{ - \frac{\hbar^{2}}{2m}\nabla ^{2}- \frac{e^{2}}{4\pi \varepsilon_{0}r_{b}} }_{ H_{b} }- \frac{e^{2}}{4\pi \varepsilon_{0}r_{a}} \right)c_{2}\phi_{b}=E\Phi$$
and so, defining $\Delta E\equiv E-E_{0}$, we get
$$\left( -\Delta E+ \frac{e^{2}}{4\pi \varepsilon_{0}r_{b}} \right)c_{1}\phi_{a}+\left( -\Delta E - \frac{e^{2}}{4\pi \varepsilon_{0}r_{a}} \right)c_{2}\phi_{b}=0$$
To find conditions on $c_{1}$ and $c_{2}$ we can take the [[scalar product]] of this expression with $\phi_{a}$ or $\phi_{b}$. For instance, with $\phi_{a}$:
$$c_{1}\left( -\Delta E \int \phi^{*}_{a}\phi_{a}+\underbrace{ \int \frac{e^{2}}{4\pi \varepsilon_{0}r_{b}}\phi_{a}^{*}\phi_{a} }_{ C } \right)-c_{2}\left( -\Delta E\underbrace{ \int \phi_{a}^{*}\phi_{b} }_{ S }- \underbrace{ \int \frac{e^{2}}{4\pi \varepsilon_{0}r_{a}}\phi_{a}^{*}\phi_{b} }_{ D }\right)=0$$
which yields
$$c_{1}(C-\Delta E)+c_{2}(D-S\Delta E)=0$$
The symbols have the same meaning as above. Taking the scalar product by $\phi^{*}_{b}$ gives a second condition which, packaged with the first, leads to the system
$$\begin{cases}
c_{1}(C-\Delta E)+c_{2}(D-S\Delta E)=0 \\
c_{1}(D-S\Delta E)+c_{2}(C-\Delta E)=0
\end{cases}$$
Being a linear system, it has a finite set of solutions only when its [[determinant]] is nonzero. As such, we also claim that
$$(C-\Delta E)^{2}-(D-S\Delta E)^{2}=0$$
which means
$$\Delta E=\frac{C+D}{1\pm S}$$
and so
$$E=E_{0}+\Delta E=E_{0}+ \frac{C+D}{1\pm S}$$
The two valid solutions are for $+$ and $-$ cases. The minus case implies $c_{1}=c_{2}\equiv c$, whereas the plus case implies $c_{1}=-c_{2}\equiv-c$, so the two possible solutions are
$$\Phi_{g}=c(\phi_{a}+\phi_{b}),\quad \Phi_{u}=c(\phi_{a}-\phi_{b})$$
$\Phi_{g}$ is called a **bonding orbital**, whereas $\Phi_{u}$ is called an **antibonding integral**. Bonding orbitals are [[Permutation operator|symmetric states]] (*gerade*, hence the subscript), whereas antibonding ones [[Permutation operator|antisymmetric]] (*ungerade*).

![[Plot Hydrogen-hydrogen ion bonding-antibonding orbitals|100%]]

In the bonding orbital, the wavefunctions of the individual atoms show constructive [[interference]] in between them and, as a consequence, there is a nonzero charge density between the nuclei. In other words, electrons reside in between the nuclei, forming a chemical bond. There is an energy minimum at a certain distance between the nuclei in which the system falls into. This is the distance between the nuclei of the atoms that make up the molecule.

In the antibonding orbital, interference is destructive and the charge density between the nuclei is suppressed. There is no energy minimum to let the atoms bond, so it does not happen and the molecule is not constructed. Thus, as the name suggests, only bonding orbitals lead to the creation of a molecule.

![[Plot Hydrogen-hydrogen ion bonding-antibonding orbital energy]]

Now, it's important to note that when atoms join to make a molecule, each of their (outer shell atomic) orbitals combine to make two (molecular) orbital: the bonding and antibonding orbitals come in pairs. However, as we've seen, the energy of the bonding integral is far lower and so all of the bonding orbitals will be occupied *first*. This binds the atoms together. Then, the antibonding orbitals will be filled *last*. If for some reason a molecule only has an antibonding state filled, then it will dissociate immediately.

Populating the bonding orbital decreases the bond energy (thus leading to a stronger bond), whereas populating the antibonding one increases it. A full shell is "neutral" towards bonding, as there are always just as many electrons in the bonding orbital as there are in the antibonding one.
### The hydrogen-hydrogen molecule
Now that we have a more general set of tools, we should test our theory on the second easiest molecule, hydrogen-hydrogen molecule $\text{H}\textendash\text{H}$. Like $\text{H}\textendash\text{H}^{+}$, this only contains two protons for nuclei, but now includes *two* electrons instead of just one. It's kind of like the molecular equivalent of the [[two-electron atom]] and just like, we'll build the orbitals starting from more basic ones by using suitable approximations.

Let's call the electrons $1$ and $2$. Since there are two electrons, we must obey the [[Pauli exclusion principle]] and the total electronic wavefunction must be antisymmetric. The *spin* wavefunctions are either the singlet state ($S=0$) $\chi_{0,0}(1,2)$ or the triplet states ($S=1$) $\chi_{1,1}(1,2)$, $\chi_{1,0}(1,2)$ and $\chi_{1,-1}(1,2)$. So, the spatial wavefunctions must be either symmetric (for singlet, makes a parastate), or antisymmetric (for triplet, makes an orthostate). We know that bonding integrals $\Phi_{g}$ are symmetric and viceversa for antibonding ones $\Phi_{u}$, so we really only have for possible combinations:
$$\begin{align}
\Phi_{A}(1,2)&=\Phi_{g}(1)\Phi_{g}(2)\chi_{0,0}(1,2) \\
\Phi_{B}(1,2)&=\Phi_{u}(1)\Phi_{u}(2)\chi_{0,0}(1,2) \\
\Phi_{C}(1,2)&=\frac{1}{\sqrt{ 2 }}[\Phi_{g}(1)\Phi_{u}(2)+\Phi_{g}(2)\Phi_{u}(1)]\chi_{0,0}(1,2) \\
\Phi_{D}(1,2)&=\frac{1}{\sqrt{ 2 }}[\Phi_{g}(1)\Phi_{u}(2)-\Phi_{g}(2)\Phi_{u}(1)]\chi_{1,M_{S}}(1,2),\quad M_{S}=0,\pm 1
\end{align}$$
Let's discuss $\Phi_{A}$ specifically. It describes two electrons in their respective ground states $1s$ with opposite spins, each occupying a *bonding* orbital $\Phi_{g}$. This is the lowest energy state for each electron and the difference in spin means no extra repulsion due to Pauli exclusion, so we intuit that it must be the ground state of the whole molecule. Similarly for $\Phi_{B}$, which is the same state but with spins reversed on both sides. Either way, they lead to the same end state since electrons are [[Identical particles|indistinguishable]]. These are $1\Sigma_{g}^{+}$ states. Meanwhile, $\Phi_{C}$ corresponds to a $1\Sigma_{u}^{+}$ term and $\Phi_{D}$ to a $3\Sigma_{u}^{+}$ state.

While we don't know the exact shape of the ground state $\Phi_{A}$, we can make an ansatz using an LCAO:
$$\begin{align}
\Phi_{A}&=\frac{1}{2}[\psi_{1s}(r_{A 1})\psi_{1s}(r_{B 2})+\psi_{1s}(r_{A 2})\psi_{1s}(r_{B 1})  \\
&\qquad+ \psi_{1s}(r_{A 1})\psi_{1s}(r_{A 2})+\psi_{1s}(r_{B 1})\psi_{1s}(r_{B 2})]\chi_{0,0}(1,2)
\end{align}$$
Each line can be split into its own terms
$$\Phi_{A}^{\text{cov}}=\frac{1}{2}[\psi_{1s}(r_{A 1})\psi_{1s}(r_{B 2})+\psi_{1s}(r_{A 2})\psi_{1s}(r_{B 1}) ]\chi_{0,0}(1,2)$$
$$\Phi_{A}^{\text{ion}}=\frac{1}{2}[\psi_{1s}(r_{A 1})\psi_{1s}(r_{A 2})+\psi_{1s}(r_{B 1})\psi_{1s}(r_{B 2})]\chi_{0,0}(1,2)$$
The two terms that make up the orbital $\Phi_{A}=\Phi_{A}^{\text{cov}}+\Phi_{A}^{\text{ion}}$ are known as the **covalent term** $\Phi_{A}^{\text{cov}}$ and the **ionic term** $\Phi_{A}^{\text{ion}}$.

The covalent term represents the case in which each electron is associated with both nuclei, being "in the middle" if you prefer. The electronic distribution is shared between the nuclei. If you push the atoms really far from each other (the "separated atom limit"), this term does not vanish, but rather becomes two isolated neutral hydrogen atoms in the ground state. The kind of bonding associated with this term is called a **covalent bond** (and $\Phi_{A}^{\text{cov}}$ is said to be the **covalent part** of $\Phi_{A}$).

The ionic term represents the situation where both electrons are attached to one nucleus, with the bond being "slanted to one side" if you prefer. The electronic distribution is strongly unequal, being mostly around only one nucleus. In the separated atom limit, this leads to one negative and one positive hydrogen [[ion]][^3]. The kind of bonding associated with this term is called an **ionic bond** (and $\Phi_{A}^{\text{ion}}$ is said to be the **ionic part** of $\Phi_{A}$).

Overall, this wavefunction $\Phi_{A}$ is mostly a learning tool. The resemblance to the actual wavefunction of the ground state of $\text{H}\textendash\text{H}$ is pretty poor and there are much better methods available for approximating it, such as using the [[Rayleigh-Ritz principle]].
### Heteronuclear molecules
Next up is the case of molecules built up of different nuclei, like $\text{C}\textendash\text{H}$ or $\text{H}\textendash\text{F}$. Here we also mix orbitals with the same $M_{z}$ momentum number, but due to different nuclear charges, the electron distribution will necessarily be slanted towards one nucleus, similar to how the ionic part of $\Phi_{A}$ behaved above. Which nucleus depends on the kind of orbital: bonding orbitals will be pushed to the nucleus with higher [[electronegativity]], whereas antibonding ones will go to the less electronegative one.

A very important difference compared to the homonuclear molecule is that there is no midpoint symmetry here (like $A_{y}$ if the bond axis is $z$). This because the nuclei are now different and so do not mirror. As such, the gerade/ungerade classification no longer applies.

[^1]: See, for instance, *Introduction to Quantum Mechanics, David. J. Griffiths*.

[^2]: Also remember that this energy is an *overestimate* because it comes from the variational method, so the actual molecule is even more strongly bound.

[^3]: However, the terms in $\Phi_{A}^{\text{ion}}$ are a poor representation of the bound state of $\text{H}^{-}$.
