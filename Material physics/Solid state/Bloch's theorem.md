---
wiki-publish: true
---
**Bloch's theorem** is a result regarding the electronic structure of an [[ideal crystal]]. It provides a shape for the [[Funzione d'onda|wavefunction]] of an [[electron]] in a periodic [[potential]].

> [!info] Bloch's theorem
> The [[Equazione agli autovalori|eigenstates]] $\psi$ of the one-electron [[Hamiltonian]] $\hat{H}=-\hbar^{2}\nabla ^{2}/2m + U(\mathbf{r})$, where $U(\mathbf{r})=U(\mathbf{r}+\mathbf{R})$ for all $\mathbf{R}$ in a three-dimensional [[Bravais lattice]], can be chosen to be [[plane wave|plane waves]] multiplied by a function $u_{n\mathbf{k}}(\mathbf{r})$ with equal periodicity to the Bravais lattice:
> $$\psi_{n\mathbf{k}}(\mathbf{r})=e^{i\mathbf{k}\cdot \mathbf{r}}u_{n\mathbf{k}}(\mathbf{r})$$
> where $u_{n\mathbf{k}}(\mathbf{r})=u_{n\mathbf{k}}(\mathbf{r}+\mathbf{R})$ for all $\mathbf{R}$. $\psi_{n\mathbf{k}}(\mathbf{r})$ is called a **Bloch wave** and the [[Numero quantico|quantum number]] $n$ is known as the **band index**.
> 
> Equivalently, since the periodicity implies $\psi_{n\mathbf{k}}(\mathbf{r}+\mathbf{R})=e^{i\mathbf{k}\cdot \mathbf{R}}\psi_{n\mathbf{k}}(\mathbf{r})$, the eigenstates of $\hat{H}$ can be chosen so that for each $\psi$ there is a [[Wavenumber|wavevector]] $\mathbf{k}$ such that
> $$\psi(\mathbf{r}+\mathbf{R})=e^{i\mathbf{k}\cdot \mathbf{R}}\psi(\mathbf{r})$$
## Proofs
This theorem can be proven in a couple ways. The first exploits other results in quantum mechanics and is easier. The second is more difficult, but more elementary.
### Translation operator proof
We start at the Bravais lattice. For each lattice vector $\mathbf{R}$, we define a translation [[operator]]  $\hat{T}_{R}$ whose operation is to shift a function by $\mathbf{R}$:
$$\hat{T}_{R}f(\mathbf{r})=f(\mathbf{r}+\mathbf{R})$$
The Hamiltonian is periodic with period $R$, courtesy of the potential, so
$$\hat{T}_{R}\hat{H}\psi=\hat{H}(\mathbf{r}+\mathbf{R})\psi(\mathbf{r}+\mathbf{R})=\hat{H}(\mathbf{r})\psi(\mathbf{r}+\mathbf{R})=\hat{H}\hat{T}_{R}\psi$$
This is true for any function $\psi$, so
$$\hat{T}_{\mathbf{R}}\hat{H}=\hat{H}\hat{T}_{\mathbf{R}}\tag{1}$$
In other words, $\hat{T}_{\mathbf{R}}$ and $\hat{H}$ [[Commutator|commute]]. Furthermore, subsequent applications of the operator do not depend on the order in which they're done, since for any $\psi(\mathbf{r})$
$$\hat{T}_{\mathbf{R}}\hat{T}_{\mathbf{R}'}\psi(\mathbf{r})=\hat{T}_{\mathbf{R}'}\hat{T}_{\mathbf{R}}\psi(\mathbf{r})=\psi(\mathbf{r}+\mathbf{R}+\mathbf{R}')$$
and so
$$\hat{T}_{\mathbf{R}}\hat{T}_{\mathbf{R}'}=\hat{T}_{\mathbf{R}'}\hat{T}_{\mathbf{R}}=\hat{T}_{\mathbf{R}+\mathbf{R}'}\tag{2}$$
So not only do they commute, any combination of $\hat{T}_{\mathbf{R}}$ and $\hat{H}$ commute. As such, these two operator share simultaneous eigenstates, with eigenvalues $c(\mathbf{R})$ for $\hat{T}_{\mathbf{R}}$ and $E$ for $\hat{H}$. Now, the periodicity of $\hat{T}_{\mathbf{R}}$ makes its eigenvalues also related since
$$\hat{T}_{\mathbf{R}'}\hat{T}_{\mathbf{R}}\psi=c(\mathbf{R})\hat{T}_{\mathbf{R}}\psi=c(\mathbf{R})c(\mathbf{R}')\psi$$
but also
$$\hat{T}_{\mathbf{R}'}\hat{T}_{\mathbf{R}}\psi=\hat{T}_{\mathbf{R}+\mathbf{R}'}\psi=c(\mathbf{R}+\mathbf{R}')\psi$$
we must have
$$c(\mathbf{R})c(\mathbf{R}')=c(\mathbf{R}+\mathbf{R}')\tag{3}$$
Now, back to the Bravais lattice itself, let's call $\mathbf{a}_{1},\mathbf{a}_{2},\mathbf{a}_{3}$ the primitive vectors of the Bravais lattice. Invoking periodicity, we can always write the eigenvalue $c(\mathbf{a}_{i})$ as
$$c(\mathbf{a}_{i})=e^{2\pi ix_{i}}$$
by choosing an adequate $x_{i}$. If $\mathbf{R}$ is a generic lattice vector $\mathbf{R}=n_{1}\mathbf{a}_{1}+n_{2}\mathbf{a}_{2}+n_{3}\mathbf{a}_{3}$, then by applying $(3)$ repeatedly on $c(\mathbf{R})$ we get
$$c(\mathbf{R})=c(n_{1}\mathbf{a}_{1}+n_{2}\mathbf{a}_{2}+n_{3}\mathbf{a}_{3})=c(\mathbf{a}_{1})^{n_{1}}c(\mathbf{a}_{2})^{n_{2}}c(\mathbf{a}_{3})^{n_{3}}$$
but this is equivalent to
$$c(\mathbf{R})=e^{i\mathbf{k}\cdot \mathbf{R}}$$
where $\mathbf{k}=x_{1}\mathbf{b}_{1}+x_{2}\mathbf{b}_{2}+x_{3}\mathbf{b}_{3}$ using the [[reciprocal lattice]] primitive vectors where $\mathbf{b}_{i}\cdot \mathbf{a}_{j}=2\pi \delta_{ij}$. Now that we know the form of the eigenvalues, we can state
$$\hat{T}_{\mathbf{R}}\psi(\mathbf{r})=\psi(\mathbf{r}+\mathbf{R})=c(\mathbf{R})\psi(\mathbf{r})=e^{i\mathbf{k}\cdot \mathbf{R}}\psi(\mathbf{r})$$
which completes our proof.
### Fourier series proof
This proof assumes [[Born-von Karman boundary conditions]] (also see below). Any function $\psi$ that satisfies these boundary conditions can be expressed as a sum of a finite, discrete set of [[plane wave|plane waves]] over the allowed wavevectors $\mathbf{q}$:
$$\psi(\mathbf{r})=\sum_{\mathbf{q}}c_{\mathbf{q}}e^{i\mathbf{q}\cdot \mathbf{r}}\tag{4}$$
where summation occurs over all allowed wavevectors. Since the potential is periodic with equal periodicity to the lattice, its plane wave expansion will only contain plane waves with the periodicity of the lattice and therefore vectors that reciprocal lattice vectors:
$$U(\mathbf{r})=\sum_{\mathbf{K}}U_{\mathbf{K}}e^{i\mathbf{K}\cdot \mathbf{r}}\tag{5}$$
where summation occurs over all reciprocal lattice vectors. Both of these are [[Fourier series]] of components $c_{\mathbf{q}}$ and $U_{\mathbf{K}}$. The $U_{\mathbf{K}}$ coefficients are given by
$$U_{\mathbf{K}}=\frac{1}{v}\int _\text{cell}U(\mathbf{r})e^{-i\mathbf{K}\cdot \mathbf{r}}d\mathbf{r}$$
where $v=V/N$ is the volume of the primitive cell in real space. A [[potential]] is only defined up to a constant and we are free to choose this constant as we wish. We shall select it such that the spatial average $U_{0}$ of the potential over a primitive cell vanishes:
$$U_{0}=\frac{1}{v}\int _\text{cell}U(\mathbf{r})d\mathbf{r}=0$$
Since $U(\mathbf{r})$ is real, the coefficients must satisfy $U_{-\mathbf{K}}=U_{\mathbf{K}}^{*}$ where $^{*}$ is the [[complex conjugate]]. If the crystal also has inversion symmetry[^1], that is, it is invariant under [[parità|parity]] $\mathbf{r}\to-\mathbf{r}$, then the coefficients must also be real: $U_{-\mathbf{K}}=U_{\mathbf{K}}$.

We can now put the Fourier series $(4)$ and $(5)$ in the [[Equazione di Schrödinger|Schrödinger equation]] given by the Hamiltonian of the theorem
$$\hat{H}\psi=- \frac{\hbar^{2}}{2m}\nabla ^{2}\psi+U(\mathbf{r})\psi=\varepsilon\psi$$
The kinetic part gives
$$- \frac{\hbar^{2}}{2m}\nabla ^{2}\psi=\sum_{\mathbf{q}} \frac{\hbar^{2}}{2m}q^{2}c_{\mathbf{q}}e^{i\mathbf{q}\cdot \mathbf{r}}$$
The potential part gives
$$U(\mathbf{r})\psi=\left( \sum_{\mathbf{K}}U_{\mathbf{K}}e^{i\mathbf{K}\cdot \mathbf{r}} \right)\left( \sum_{\mathbf{q}}c_{\mathbf{q}}e^{i\mathbf{q}\cdot \mathbf{r}} \right)=\sum_{\mathbf{K}\mathbf{q}}U_{\mathbf{K}}c_{\mathbf{q}}e^{i(\mathbf{K}+\mathbf{q})\cdot \mathbf{r}}=\ldots$$
We can substitute $\mathbf{K}+\mathbf{q}=\mathbf{q}'$ (and so $\mathbf{q}=\mathbf{q}'-\mathbf{K}$) and change the sum from being over $\mathbf{q}$ to being over $\mathbf{q}'$. $\mathbf{K}$ is a reciprocal lattice vector, so it doesn't care about which wavevectors it sums over so long it's over all of them and they all only differ by the periodicity $\mathbf{K}$.
$$\ldots=\sum_{\mathbf{K}\mathbf{q}'}U_{\mathbf{K}}c_{\mathbf{q}'-\mathbf{K}}e^{i\mathbf{q}'\cdot \mathbf{r}}$$
We rename the indices as $\mathbf{q}'\to \mathbf{q}$ and $\mathbf{K}\to \mathbf{K}'$. This is a purely aesthetic change to make it clear that the sum in the potential part and the sum in the kinetic part are over the same $\mathbf{q}$ and can be merged. With this, the Schrödinger equation becomes
$$\sum _{\mathbf{q}} \frac{\hbar^{2}}{2m}q^{2}c_{\mathbf{q}}e^{i\mathbf{q}\cdot \mathbf{r}}+\sum_{\mathbf{K}'\mathbf{q}}U_{\mathbf{K}'}c_{\mathbf{q}-\mathbf{K}'}e^{i\mathbf{q}'\cdot \mathbf{r}}=\varepsilon \sum_{\mathbf{q}}c_{\mathbf{q}}e^{i\mathbf{q}\cdot \mathbf{r}}$$
Rearranged it looks like
$$\sum_{\mathbf{q}}e^{i\mathbf{q}\cdot \mathbf{r}}\left[ \left( \frac{\hbar^{2}}{2m}q^{2} -\varepsilon\right)c_{\mathbf{q}}+\sum_{\mathbf{K}'}U_{\mathbf{K}'}c_{\mathbf{q}-\mathbf{K}'} \right]=0$$
The plane waves derived from the boundary conditions are all [[Orthogonality|orthogonal]], so in order for the whole sum to be zero, then each individual term must be zero, which is to say that the coefficients (the square brackets) must all be zero:
$$\boxed{\left( \frac{\hbar^{2}}{2m}q^{2} -\varepsilon\right)c_{\mathbf{q}}+\sum_{\mathbf{K}'}U_{\mathbf{K}'}c_{\mathbf{q}-\mathbf{K}'}=0}$$
For the sake of convenience, it's useful to express the wavevector $\mathbf{q}$ in terms of a wavevector $\mathbf{k}$ that is guaranteed to be in the first [[Brillouin zone]], which we do as $\mathbf{q}=\mathbf{k}-\mathbf{K}$ where $\mathbf{K}$ is a reciprocal lattice vector that chosen so that $\mathbf{k}$ is in the first Brillouin zone.
$$\left( \frac{\hbar^{2}}{2m}q^{2}-\varepsilon \right)c_{\mathbf{k}-\mathbf{K}}+\sum_{\mathbf{K}'}U_{\mathbf{K}'}c_{\mathbf{k}-\mathbf{K}-\mathbf{K}'}=0$$
Changing summation variable from $\mathbf{K}'$ to $\mathbf{K}'-\mathbf{K}$ yields
$$\boxed{\left( \frac{\hbar^{2}}{2m}q^{2}-\varepsilon \right)c_{\mathbf{k}-\mathbf{K}}+\sum_{\mathbf{K}'}U_{\mathbf{K}'-\mathbf{K}}c_{\mathbf{k}-\mathbf{K}'}=0}\tag{6}$$
which is true for all $\mathbf{q}$ (and $\mathbf{k}$) that is allowed by the boundary conditions. This equation has the same validity as the original Schrödinger equation that we started with, but it's rewritten in the domain of the wavevectors, simplified by the fact that the potential is nonzero only for $\mathbf{K}$ that are reciprocal lattice vectors. For any $\mathbf{k}$ in the first Brillouin zone, the equation above only couples the coefficients $c_{\mathbf{k}},c_{\mathbf{k}-\mathbf{K}},c_{\mathbf{k}-\mathbf{K}'},\ldots$, whose plane waves only differ from $\mathbf{k}$ by a reciprocal lattice vector. Thus, the original problem is broken down into $N$ independent problems: one for each allowed value of $\mathbf{k}$ in first Brillouin zone. Each of these problems has solutions that are superpositions of plane waves containing only the wavevector $\mathbf{k}$ and wavevectors differing from $\mathbf{k}$ only by a reciprocal lattice vector.

We can use this information to notice that the original expansion $(4)$ of the wavefunction now reads
$$\psi_{\mathbf{k}}(\mathbf{r})=\sum_{\mathbf{K}}c_{\mathbf{k}-\mathbf{K}}e^{i(\mathbf{k}-\mathbf{K})\cdot \mathbf{r}}$$
since $\mathbf{q}=\mathbf{k}-\mathbf{K}$. If we extract $e^{i\mathbf{k}\cdot \mathbf{r}}$ we get
$$\psi_{\mathbf{k}}(\mathbf{r})=e^{i\mathbf{k}\cdot \mathbf{r}}\left( \sum_{\mathbf{K}}c_{\mathbf{k}-\mathbf{K}}e^{-i\mathbf{k}\cdot \mathbf{r}} \right)$$
but since the term in parenthesis is periodic with the lattice, this is precisely the statement of Bloch's theorem, with
$$u(\mathbf{k})=\sum_{\mathbf{K}}c_{\mathbf{k}-\mathbf{K}}e^{-i\mathbf{k}\cdot \mathbf{r}}$$
The band index $n$ appears to index the infinitely many solutions of $(6)$ for any given $\mathbf{k}$.
## Boundary conditions
Generally speaking, the wavevector $\mathbf{k}$ is some complex-valued vector. However, certain specific boundary conditions work in such a way as to make it real, and also restrict its allowed values.

Once such set of conditions is the [[Born-von Karman boundary conditions]] (macroscopic periodic boundary conditions). It is most convenient to work in a periodic space that mimics the shape of the primitive cell. Thus, instead of picking a typical, arbitrary cube of side $L$, we generalize the conditions as follows:
$$\psi(\mathbf{r}+N_{i}\mathbf{a}_{i})=\psi(\mathbf{r})\quad\text{for }i=1,2,3$$
$N_{i}$ are integers of order $N^{1/3}$ and $N=N_{1}N_{2}N_{3}$ is the total number of primitive cells in the periodic region (for a simple cubic lattice and $N_{1}=N_{2}=N_{3}=N$, this goes back to a cube of side $L=Na$).

If we apply Bloch's theorem to this wavefunction we get
$$\psi_{n\mathbf{k}}(\mathbf{r})=\psi_{n\mathbf{k}}(\mathbf{r}+N_{i}\mathbf{a}_{i})=e^{iN_{i}\mathbf{k}\cdot \mathbf{a}_{i}}\psi_{n\mathbf{k}}(\mathbf{r})$$
For this to be true we need $e^{iN_{i}\mathbf{k}\cdot \mathbf{a}_{i}}=1$, which leads to the condition
$$\mathbf{k}\cdot \mathbf{a}_{i}=\frac{2\pi m_{i}}{N_{i}}=2\pi x_{i}\quad\text{where} \quad m_{i}\in \mathbb{Z}\text{ and } x_{i}=\frac{m_{i}}{N_{i}}$$
The wavevector must then be of the form
$$\mathbf{k}=\sum_{i=1}^{3} \frac{m_{i}}{N_{i}}\mathbf{b}_{i}$$
where $\mathbf{b}_{i}$ are the reciprocal lattice primitive vectors. Evidently, $\mathbf{k}$ must only possess discrete values, indexed by $m_{i}$. This said, since we're working with macroscopic matter, $N\sim 10^{23}$, so the actual values of $\mathbf{k}$ are so finely packed that we might as well consider them to be continuous. The exact spacing between $\mathbf{k}$ is equal to the volume of the [[parallelepiped]] of sides $\mathbf{b}_{i}/N_{i}$:
$$\Delta \mathbf{k}=\frac{1}{N}\mathbf{b}_{1}\cdot(\mathbf{b}_{2}\times \mathbf{b}_{3})$$
Since $\mathbf{b}_{1}\cdot(\mathbf{b}_{2}\times \mathbf{b}_{3})=N\Delta \mathbf{k}$ is the volume of a primitive cell in the reciprocal lattice, we conclude that the number of *wavevectors* allowed in a cell of the *reciprocal* lattice is equal to the number of *sites* in the *direct* cell. And since the volume of the reciprocal cell is also $(2\pi)^{3}/v_\text{cell}$ where $v_\text{cell}=V/N$ is the volume of the direct cell, we get
$$\boxed{\Delta \mathbf{k}=\frac{(2\pi)^{3}}{V}}$$
This is the same result that can be obtained in the free electron [[Sommerfeld model]].
## Bloch waves
A Bloch wave is a plane wave that is identified by a wavevector $\mathbf{k}$, which reflects the translation invariance under the chosen Hamiltonian, and the band index $n$, which indicates one possible [[energy]] level of a given $\mathbf{k}$. These are the fundamental result of Bloch's theorem, so they warrant some extended analysis.

Plane waves are definitely not [[Normalization|normalizable]], since they extend periodically to infinity without dampening (they are guaranteed not [[Spazi Lp|L^2]] functions). This means that the electrons are *not localized* anywhere in particular, but rather spread across the entire crystal. This is obviously an unphysical state, but it works very well for global, bulk-level descriptions of a crystalline solid. It does however fail to describe any transport phenomenon (e.g. electrons moving to form an [[electric current]]) and a different model is required for such cases.

In the given Bravais lattice, the wavevector $\mathbf{k}$ can always be assumed to be contained within the first [[Brillouin zone]]. This is because any $\mathbf{k}'$ can be reduced to $\mathbf{k}$ by opportune translation:
$$\psi(\mathbf{r}+\mathbf{R})=e^{i\mathbf{k}'\cdot \mathbf{R}}\psi(\mathbf{R})=e^{i(\mathbf{k}+\mathbf{K})\cdot \mathbf{R}}\psi(\mathbf{R})=e^{i\mathbf{k}\cdot \mathbf{R}}\psi(\mathbf{R})$$
The band index $n$ appears in the Bloch wave because the solution for each $\mathbf{k}$ is not unique. If we substitute $\psi(\mathbf{r})=e^{i\mathbf{k}\cdot \mathbf{r}}u_{\mathbf{k}}(\mathbf{r})$ in the [[equazione di Schrödinger|Schrödinger equation]] we get
$$\hat{H}_{\mathbf{k}}u_{\mathbf{k}}(\mathbf{r})=\left[ \frac{\hbar^{2}}{2m}(-i\nabla+\mathbf{k})^{2}+U(\mathbf{r}) \right]u_{\mathbf{k}}(\mathbf{r})=\varepsilon_{\mathbf{k}}u_{\mathbf{k}}(\mathbf{r})$$
Thanks to the boundary condition $u_{\mathbf{k}}(\mathbf{r})=u_{\mathbf{k}}(\mathbf{r}+\mathbf{R})$, we can consider this to be a Hermitian [[eigenvalue equation]], limited to a single cell of the crystal. Since the eigenvalue problem is set in a finite and defined volume, we expect in general to find an infinite [[set]] of solutions with discrete eigenvalues, which we index with the symbol $n$. Thus, every single $\mathbf{k}$ comes along with an infinite set of eigenvalues $\varepsilon_{n\mathbf{k}}$. The eigenfunctions $\psi_{n\mathbf{k}}$ and eigenvalues $\varepsilon_{n\mathbf{k}}$ also obey by periodicity in the reciprocal lattice:
$$\psi_{n,\mathbf{k}+\mathbf{K}}(\mathbf{r})=\psi_{n\mathbf{k}}(\mathbf{r}),\quad \varepsilon_{n,\mathbf{k}+\mathbf{K}}=\varepsilon_{n\mathbf{k}}\equiv \varepsilon_{n}(\mathbf{k})$$
Solving the Schrödinger equation in the periodic potential leads to an infinite set of functions $\varepsilon_{n}(\mathbf{k})$, indexed by $n$ and all periodic in the reciprocal lattice, which represent the energy levels that are accessible to the electrons. The values of $\mathbf{k}$ are technically discrete, but so closely packed that we might as well consider them continuous. For each $n$, the effectively-continuous interval of energy levels given by $\varepsilon_{n}(\mathbf{k})$ is called an **energy band** and collectively, they form the **band structure** of the crystal.

It can be proven[^2] that the [[mean]] velocity of an electron in a band $n$ with wavevector $\mathbf{k}$ is
$$\boxed{\mathbf{v}_{n}(\mathbf{k})=\frac{1}{\hbar}\nabla_{\mathbf{k}}\varepsilon_{n}(\mathbf{k})}$$
This is the [[phase velocity]] of the electron and, critically, it is *not* zero. This is a striking result, because it implies that the electron, despite in theory being constantly subject to collisions with ions, never has its mean velocity degraded. This allows the electron to move indefinitely throughout the entire crystal. This fact, in striking contrast to the old [[Drude model]] that assumed (reasonably so) that each electron-ion collision would degrade velocity, is of fundamental importance to the conductivity of crystals and metals especially.

For as much discussion as we've had surrounding $\mathbf{k}$, we haven't really talked about *what* it is. It's a wavevector of course, but to what? Well to a Bloch wave, and a Bloch wave is the quantum state of an electron in a periodic potential. So is $\mathbf{k}$ the wavevector of the [[wave]] interpretation of an electron? Yes... to an extent. It starts to get a little problematic when you start to talk about [[Linear momentum|momentum]], namely $\mathbf{p}=\hbar \mathbf{k}$. In the free electron model ($U(\mathbf{r})=0$), this is very much the momentum of the electron. This starts to fall apart when you introduce a periodic potential, because now the Hamiltonian is no longer invariant over translations. This makes the eigenstates of $\hat{H}$ no longer simultaneous eigenstates of $\hat{p}$, so the two cannot be known at the same time. Thus, the Bloch wave $\mathbf{k}$ cannot possibly be proportional to $\mathbf{p}$ without breaking the rules of quantum mechanics.

That said, $\hbar \mathbf{k}$ is still *some* momentum, it's just not the electron's specifically. We call it the **crystal momentum** of the electron and, while the name includes the term "momentum", it really isn't one in the traditional sense. It does, however, hold several similarities that can only be appreciated when dealing externally applied [[electromagnetic radiation]]. Until then, $\mathbf{k}$ can be interpreted as a quantum number that representing translational [[symmetry]] of a periodic potential, much like how $\mathbf{p}$ is in a way a quantum number of the translational symmetry of free space.

:::image
![[Bloch wave.png]]
An example of a periodic potential $V(\mathbf{r})$ and a Bloch wave $\psi(\mathbf{k},\mathbf{r})$ for some function $u(\mathbf{k},\mathbf{r})$.
:::

[^1]: This proof is valid even for crystals that do not exhibit inversion symmetry. It is assumed here for simplicity.

[^2]: See Appendix E of *Solid State Physics, Ashcroft & Mermin*.
