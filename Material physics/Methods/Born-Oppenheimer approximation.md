The **Born-Oppenheimer approximation**, also called the **adiabatic approximation**, is a computational method to solve the quantum [[Funzione d'onda|wave function]] of a diatomic [[molecule]]. It is based on the following simplification: the motion of the [[Nucleo atomico|nuclei]] is considerably slower than that of the [[Elettrone|electrons]] and can thus be considered stationary, removing the nuclear kinetic terms from the [[Hamiltonian]]. The positions of the nuclei are then constant parameters and not variables.

The Hamiltonian becomes
$$H=\sum_{i=1}^{N_{e}}- \frac{\hbar^{2}}{2m}\nabla ^{2}_{\mathbf{r}_{i}}-\sum_{i} \frac{Z_{A}e^{2}}{4\pi \varepsilon_{0}\lvert \mathbf{r}_{i}-\mathbf{R}_{A} \rvert } - \sum _{i} \frac{Z_{B}e^{2}}{4\pi \varepsilon_{0}\lvert \mathbf{r}_{i}-\mathbf{R}_{B} \rvert }+\sum_{i>j} \frac{e^{2}}{4\pi \varepsilon_{0}\lvert \mathbf{r}_{i}-\mathbf{r}_{j} \rvert }+ \frac{Z_{A}Z_{B}e^{2}}{4\pi \varepsilon_{0}R}$$
In order, the terms are:
1. The [[kinetic energy]] of the electrons;
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
### Variational approach
One way to solve the system is to use the [[variational method]], letting the distance between nuclei $R$ be the variable parameter. The ground state wave function of an electron centered around $r$ is our trial function and is
$$\psi_{100}(r)=\frac{1}{\sqrt{ \pi a^{3} }}e^{-r/a}$$
For brevity we'll write $\psi_{100}\equiv \psi_{0}$. We'll use what's called a **Linear Combination of Atomic Orbitals** (or **LCAO** for short):
$$\psi=S[\psi_{100}(r)+\psi_{100}(\mathfrak{r})]$$
where $\mathfrak{r}=\sqrt{ r^{2}+R^{2}-2rR\cos \theta }$. For this wave function to be a realizable state, it must be [[Normalization|normalized]], so
$$1=\int \lvert \psi \rvert ^{2}d\tau=\lvert S\rvert ^{2}\int \psi_{0}(r)^{2}d\tau \int \psi_{0}(\mathfrak{r})d\tau+2\int \psi_{0}(r)\psi_{0}(\mathfrak{r})d\tau$$
These integrals can be solved by substituting the definition of $\psi$ above. The mixed integral
$$I=\frac{1}{\pi a^{3}}\int e^{-r/a}e^{-\sqrt{ r^{2}+R^{2}-2rR\cos \theta }/a}R^{2}\sin \theta drd\theta d\phi$$
can be solved by setting $\sqrt{ r^{2}+R^{2}-2rR\cos \theta }=y$[^1]. It results in
$$I=e^{-R/a}\left[ 1+ \left( \frac{R}{a} \right)+ \frac{1}{3}\left( \frac{R}{a} \right)^{2} \right]$$
and the normalization constant ends up being
$$\lvert S\rvert ^{2}=\frac{1}{2(1+I)}$$
With a known wave function, we can now evaluate the energy in that state:
$$\braket{ \psi | H | \psi } =E_{1}-2\lvert S\rvert ^{2}\left( \frac{e^{2}}{4\pi \varepsilon_{0}} \right)\left[ \underbrace{ \left\langle  \psi_{0}(r)\left| \frac{1}{\mathfrak{r}}\right| \psi_{0}(r)  \right\rangle }_{ \text{Direct} }+ \underbrace{ \left\langle  \psi_{0}(r)\left| \frac{1}{\mathfrak{r}}\right| \psi_{0}(\mathfrak{r}) \right\rangle }_{ \text{Swap} }  \right]$$
The factor of $2$ in the second terms comes from the fact that the interaction is symmetric and indexes can be switched, leading to the same term twice. There are two terms dependent on position. We call the first the "Direct" term or integral (symbol: $C$), and it comes from the electromagnetic interaction between an electron on a nucleus with the *other* nucleus. We call the second term the "Swap" integral (symbol: $D$) and it relies on the superposition of wave functions of $r$ and $\mathfrak{r}$, hence "Swap". All in all, the state energy is
$$E=\langle H \rangle =\left[ 1+ 2 \frac{C+D}{1+I} \right]E_{1}$$


[^1]: See, for instance, *Introduction to Quantum Mechanics, David. J. Griffiths*.
