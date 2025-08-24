---
wiki-publish: true
---
An **ideal crystal** is a solid-state material with a periodic, perfectly geometric [[Bravais lattice]]. It is the simplest mathematical description of a [[crystal]], much like how an [[ideal gas]] is the simplest description of a [[gas]]. The [[Hamiltonian]] is
$$H=\underbrace{ \sum_{i} \frac{p_{i}^{2}}{2m_{i}}+ \sum_{j} \frac{P_{j}^{2}}{2M_{j}} }_{ \text{Kinetic terms} }+ \underbrace{ \frac{1}{2}\sum_{j,j'} \frac{Z_{j}Z_{j'}e^{2}}{\lvert \mathbf{R}_{j}-\mathbf{R}_{j'} \rvert } }_{ \text{Ion-ion interaction} }+ \underbrace{ \frac{1}{2}\sum_{i,i'} \frac{e^{2}}{\lvert \mathbf{r}_{i}-\mathbf{r}_{i'} \rvert } }_{ \text{Electron-electron interaction} }-\underbrace{ \sum_{i,j} \frac{Z_{j}e^{2}}{\lvert \mathbf{r}_{i}-\mathbf{R}_{j} \rvert } }_{ \text{Ion-electron interaction} }$$
This is an $N$-body Hamiltonian that's certainly not analytically solvable. It can be solved in an approximate manner by combining two assumptions:
1. **Core and valence electrons**. We split electrons in two categories: core electrons (inner electron shells) and valence electrons (outermost electron shell). Only the valence electrons are significant when it comes to interactions.
2. **Born-Oppenheimer approximation**. The [[Born-Oppenheimer approximation]] is noticing that the [[Nucleo atomico|nuclei]] move at much lower speeds than the electrons, which allows us to state that ions are subject to a [[mean]] [[potential]] and that the electrons see the ions as basically stationary.

In this sense, the Hamiltonian can be written as
$$H\equiv H_\text{ions}(R_{i})+H_{e}(r_{i},R_{j})+H_\text{e-ion}(r_{i},\delta R_{j})$$
where $H_\text{ions}$ is the lattice energy (the energy of each individual [[ion]] in isolation), $H_{e}$ is the interaction energy between [[electron|electrons]] with "frozen" ions (without motion) and $H_\text{e-ion}$ is the interaction energy between electrons with ion *vibrations*.
## Vibrations
In order to realistically describe a crystal's behavior, we cannot ignore the fact that the ions do move inside the lattice. The great importance of this is that if they didn't, no [[energy]] could be transferred through the material through vibrations, a fact that's obviously a glaring issue as any object in a nonzero [[temperature]] environment will have some collisions from the outside transferring energy to it. Thus, we need some way to detach the actual position of an ion from the lattice of the crystal. In mathematical terms, the positions $\mathbf{R}$ are no longer constant, but a function of time, $\mathbf{R}(t)$.

The vibrations of a crystal are determined by the ions alone, so their study only affects the ionic part of the Hamiltonian $H_\text{ions}$. By observing the real world behavior of a crystal, we can (and should) make an assumption:
1. The [[mean]] equilibrium position $\langle \mathbf{R}(t) \rangle_{t}$ of each ion correspond to a point $\mathbf{R}$ in the [[Bravais lattice]].

This accounts for the fact that a real-world crystal manifestly abides by some sort of lattice structure, whilst still allowing for ionic motion. This assumption casts a very wide net: *any* ionic motion is fine so long that *on average*, it makes the ion stay on the lattice point. The only kind of motion that this assumption openly rejects is ion *[[scattering]]*, where the ions fully break off the lattice and either leave the material entirely, to take a free spot somewhere else in the lattice. These are pretty intuitive scenarios, but is stable conditions, they don't particularly matter.[^1]
### The harmonic approximation
Soon enough however, we hit a wall. To vibrate, the ions must affect each other somehow. Of course, they do so [[Electromagnetism|electromagnetically]] (electrostatically even), but we don't know what the [[electric potential]] looks like. In order to get a solution that's can be handled by hand, we take a second, more stringent assumption:
2. The displacements from the mean equilibrium position are small compared to the distance between ions.

It might be more illuminate to read it this way: ion oscillations are small. And the answer to small oscillations is always the same: the [[harmonic oscillator]]. Thus, the electric potential varies *harmonically* in time: this is called the **harmonic approximation**. You might argue whether this assumption is even valid: fair point. But recall that the mass of an ion is essentially that of the [[Nucleo atomico|nucleus]] (a "blob" of [[proton|protons]] and [[neutron|neutrons]]) and that is enormous compared to that of the few electrons surrounding it, entire orders of magnitude higher. So large in fact, the [[Born-Oppenheimer approximation]] in [[Molecule|molecules]] just does away with nuclear motion outright and *still* gets good results. Thus, it's perfectly legitimate to assume that the ions move very little around their resting spot.

So, we have a periodic shape in which we slot in our ions and assume that any change from this configuration is small. The generic position of each ion will then be given by $\mathbf{r}(\mathbf{R})=\mathbf{R}+\mathbf{u}(\mathbf{R})$, where $\mathbf{u}(\mathbf{R})$ is the (small) displacement from the lattice point. The generic interaction potential between ions $U$ is then $U\equiv U(\mathbf{r})=U(\mathbf{R}+\mathbf{u})$. Here's the mathematical statement of the approximation: we take this potential and expand it in a [[Taylor series]] around the lattice point:
$$U(\mathbf{R}+\mathbf{u})=U(\mathbf{R})+(\mathbf{u}\cdot \nabla )U(\mathbf{R})+ \frac{1}{2}(\mathbf{u}\cdot \nabla)^{2}U(\mathbf{R})+ \frac{1}{3!}(\mathbf{u}\cdot \nabla)^{3}U(\mathbf{R})+\ldots$$
If we express $U$ in terms of the individual potential energy $\phi$ of each ion we get 
$$\begin{align}
U&=\frac{N}{2}\sum_{\mathbf{R}\neq 0}\phi(\mathbf{R})\\
&+ \frac{1}{2}\sum_{\mathbf{R}\mathbf{R}'}(\mathbf{u}(\mathbf{R})-\mathbf{u}(\mathbf{R}'))\cdot \nabla \phi(\mathbf{R}-\mathbf{R}') \\
&+ \frac{1}{4}\sum_{\mathbf{R}\mathbf{R}'}[\mathbf{u}(\mathbf{R})-\mathbf{u}(\mathbf{R}')\cdot \nabla]^{2}\phi(\mathbf{R}-\mathbf{R}') \\
&+O(\mathbf{u}^{3})
\end{align}$$
The first-order term contains
$$\sum_{\mathbf{R}'}\nabla \phi(\mathbf{R}-\mathbf{R}')$$
which is (minus) the total force exerted on the ion at equilibrium in $\mathbf{R}$ by all other atoms $\mathbf{R}'$. But there is no total force at equilibrium, that's the whole point of equilibrium. Thus, this entire term must vanish.

The harmonic approximation consists of truncating at the second order, where we're only left with zeroth- and second-order terms, which we can denote as
$$\boxed{U=U_\text{equilbrium}+U_\text{harmonic}}$$
The former term is the energy of a perfectly immobile lattice. It is purely electrostatic potential. The second term is due to the oscillations of the ions about their resting spots, and can be expanded to read
$$U_\text{harmonic}=\frac{1}{4}\sum_{\mathbf{R}\mathbf{R}'\mu \nu}[u_{\mu}(\mathbf{R})-u_{\mu}(\mathbf{R}')]\phi_{\mu \nu}(\mathbf{R}-\mathbf{R}')[u_{\nu}(\mathbf{R})-u_{\nu}(\mathbf{R}')]$$
where $\mu,\nu=x,y,z$ and
$$\phi_{\mu \nu}=\frac{ \partial ^{2}\phi(\mathbf{r}) }{ \partial r_{\mu}r_{\nu} } $$
For convenience, an alternative format is used
$$\boxed{U_\text{harmonic}=\frac{1}{2}\sum_{\mathbf{R}\mathbf{R}'\mu \nu} u_{\mu}(\mathbf{R})D_{\mu \nu}(\mathbf{R}-\mathbf{R}')u_{\nu}(\mathbf{R}')}$$
where
$$D_{\mu \nu}(\mathbf{R}-\mathbf{R}')=\delta_{\mathbf{R}\mathbf{R}'}\sum_{\mathbf{R}''}\phi_{\mu \nu}(\mathbf{R}-\mathbf{R}'')-\phi_{\mu \nu}(\mathbf{R}-\mathbf{R}')$$
are the elements of the **dynamical matrix**. $\delta_{\mathbf{R}\mathbf{R}'}$ is the three-dimensional [[Delta di Dirac|Dirac delta]].
#### The spring model
Since we're using harmonic potentials for the interaction between ions, how do we interpret this? Well, harmonic potentials are springs. They have some elastic constant and the strength of the pullback increases quadratically with distance. This justifies a somewhat toyish but otherwise not unreasonable model of claiming that ions are bound to each other by (invisible) *springs*. In other words, a chain of [[Harmonic oscillator|harmonic oscillators]].

Say that all of the oscillators have the same elastic constant $\gamma$. Then their single-oscillator Hamiltonian is
$$H_\text{osc}=\frac{1}{2}Mv^{2}+ \frac{1}{2}\gamma x^{2}$$
where $M$ is the [[mass]] of the ion.

Let's start from a 1D crystal, so an (effectively) infinite chain of oscillators all bound to their two closest neighbors. We'll assume each primitive cell has just one ion in it. The oscillations are longitudinal, that is, on the axis of the springs[^2]. The lattice parameter is $a$, so each ion's resting position is $na$, for $n\in \mathbb{Z}$. We assume that the ions only interact with their nearest neighbors (short range approximation), so the potential is
$$U_\text{harmonic}=\frac{1}{2}\phi''(a)\sum_{n}[u(na)-u([n+1]a)]^{2}$$
The [[ordinary differential equation|differential equation]] of motion then is
$$M\ddot{u}(na)=-\frac{ \partial U_\text{harmonic} }{ \partial u(na) }=-\phi''(a)[2u(na)-u([n-1]a)-u([n+1]a)] \tag{1}$$
This is the equation of motion of a [[point mass]] $M$ attached with two massless springs of elastic constant $\gamma=\phi''(a)$. It is a [[wave equation]], so we'll choose the solution for $u(na,t)\equiv u_{n}(t)$ to be a [[Plane wave]]
$$u_{n}(t)=ue^{i(kna-\omega t)}\tag{2}$$
for some constant $u$. 

The complete solution also requires knowing the initial position and velocity/[[Linear momentum|momentum]] of each ion in the chain, but we don't need those to gather more information from this system. When substituting $(2)$ into $(1)$ we get
$$\begin{align}
-M\omega ^{2}\cancel{ e^{i(kan-\omega t)} }&=-\gamma[2-e^{ika}-e^{ika}]\cancel{ e^{i(kan)-\omega t} } \\
M\omega ^{2}&=\gamma[2-e^{-ika}-e^{ika}]
\end{align}$$
Extracting $\omega$, using $e^{ix}+e^{-ix}=2\cos x$ and  $(1-\cos ^{2}x)/2=\sin ^{2}x$ gives
$$\omega(k)=\sqrt{ \frac{2\gamma(1-\cos(ka))}{M} }=2\sqrt{ \frac{\gamma}{M} }\left\lvert  \sin\left( \frac{ka}{2} \right)  \right\rvert $$
This is the **[[dispersion|dispersion relation]]** of the 1D, spring-modeled, ideal crystal, which tells us the [[Frequency|angular frequency]] of the [[Wave]] that carries a perturbation through the chain of ions. The wave, as usual, moves with two different velocities: the [[phase velocity]] $c=\omega/k$ and the [[group velocity]] $v_{g}=\partial \omega/\partial k$.

![[1D monatomic lattice crystal dispersion.png]]

Something interesting happens when the vibration wavelength is very large compared to the lattice spacing $a$. In the $k\ll \pi/a$ case, the [[wavelength]] of the vibration is much larger than the lattice distance $a$, so ions next to each other largely move with the same phase. This is called a **continuous approximation**. Moreover, since $ka\ll \pi$, the dispersion becomes *linear*
$$\sin \frac{ka}{2}\simeq \frac{ka}{2}\quad\to \quad \omega(k)\simeq 2\sqrt{ \frac{\gamma}{M} } \frac{ka}{2}=ck\quad\text{with }c=\sqrt{ \frac{\gamma}{M} }a$$
In this specific case, the phase velocity is equal to [[group velocity]], as
$$v_{g}\equiv\frac{ \partial \omega(k) }{ \partial k } =\frac{ \partial  }{ \partial k } \sqrt{ \frac{\gamma}{M} }ka=\sqrt{ \frac{\gamma}{M} }a=c$$
They're also constant and independent of frequency. $c$ is the **[[speed of sound]]** of the material.

Another interesting case is when $k=\pi/a$. In this case, the [[wavelength]] of the vibration is exactly $\lambda=2a$ and the direction of motion alternates between ions. For instance, all even ions will move to the right and all odd ions to the left.
$$\sin \frac{ka}{2}=\sin \frac{\pi}{2}=1\quad\to \quad \omega=2\sqrt{ \frac{\gamma}{M} }$$
Clearly then, the group velocity is *zero*. There can be no propagation in this regime: the wave is a [[standing wave]].

Something useful to note is that the dispersion relation is periodic. This is important because it's specifically periodic in the range of the first Brillouin zone. This means that, if we know the Bravais lattice of the crystal, we can find the [[reciprocal lattice]], then the Brillouin zone and finally all of the above.
#### Two-point basis
For now we've talked about a lattice whose points correspond with actual ions. Let's expand the concept to a lattice with a basis. In the same 1D model, we'll have twice as many ions, but they're still all connected with the same springs as above. We'll identify with $u_{n}$ the location of one type of ion and with $v_{n}$ the location of the other. We'll use $b$ for the lattice parameter.

We'll now have two equations of motion, one for each ion:
$$\begin{align}
M_{1} \frac{d^{2}u_{n}}{dt^{2}}=-\gamma[2u_{n}-v_{n-1}-v_{n}],\qquad &M_{2} \frac{d^{2}v_{n}}{dt^{2}}=-\gamma[2v_{n}-u_{n}-u_{n+1}] \\
-\omega ^{2}M_{1}u=\gamma v(1+e^{-ikb})-2\gamma u\qquad&-\omega ^{2}M_{2}v=\gamma u(1+e^{ikb})-2\gamma v
\end{align}$$
This yields the system
$$\begin{cases}
(2\gamma-\omega ^{2}M_{1})u-\gamma(1+e^{-ikb})v=0 \\
-\gamma(1+e^{ikb})u-(2\gamma-\omega ^{2}M_{2})v=0
\end{cases}$$
This has nontrivial solution only if its [[determinant]] is zero:
$$\begin{vmatrix}
2\gamma-\omega ^{2}M_{1} & -\gamma(1+e^{-ikb}) \\
-\gamma(1+e^{ikb}) & 2\gamma-\omega ^{2}M_{2}
\end{vmatrix}=0$$
There will only be two possible nontrivial solutions, both dependent on $k$. The dispersion relation therefore splits in two:
$$\omega ^{2}=\gamma\left( \frac{1}{M_{1}}+ \frac{1}{M_{2}} \right)\pm \gamma\sqrt{  \left( \frac{1}{M_{1}}+ \frac{1}{M_{2}} \right)^{2}- \frac{4}{M_{1}M_{2}}\sin ^{2} \frac{kb}{2}  }$$
On further analysis, these solutions have *very* different behaviors. Collectively, they're known as the **branches** of the dispersion relation.

![[1D diatomic lattice crystal dispersion.png]]

The lower branch behaves like before, with vanishing frequency at the edges and a dispersion relation of the form $\omega=ck$. This is called the **acoustic branch** of dispersion. The upper branch however has much higher frequencies and never vanishes. This is called the **optical branch** of dispersion because the higher frequencies can actually interact and couple with commonly encountered [[Electromagnetic radiation]], thus defining the crystal's optical behavior.
#### Energy spectrum
The above discussion is adequate for the general solution to the wave equation, but in practice, we need some boundary conditions to fully solve it. If there are $N$ total ions in the crystal, then we can use periodic boundary conditions[^3] to state that the crystal is actually a looping ring, so $u(0)=u(Na)$.

The periodic condition enforces
$$e^{ikNa}=1\quad\Rightarrow \quad \boxed{k=\frac{2\pi}{a} \frac{n}{N}}$$
Evidently, there's only a discrete set of acceptable [[Wavenumber|wavenumbers]] for the oscillation of a 1D crystal. These wavenumbers, or rather their associated [[Frequency|frequencies]], are known as the **[[normal mode|normal modes]]** of oscillation of the system. We take these to lie between $-\pi/a$ and $\pi/a$, which is essentially saying that the must be contained in the first [[Brillouin zone]] of the [[reciprocal lattice]].

Everything that we've discovered up to now is actually fairly classical. There's nothing obligatorily quantum anywhere in here. But now that we're working with specific modes of vibration, we need to deal with the kind of energy that they carry. In a macroscopic system, energy quantization doesn't matter. Energy scales are way too large for that to be significant. But we're not in a macroscopic setting, we're dealing with individual ions. So the energy *has* to be quantized and the quantization must matter because the energy scales are just that small. But the fix is simple: just change the harmonic oscillators to [[Oscillatore armonico quantistico|quantum harmonic oscillators]]. This quantizes the energy of the $k$-th mode of oscillation to
$$E_{l}(k)=\hbar \omega(k)\left( l+ \frac{1}{2} \right)$$
where $l$ is the "principal [[Numero quantico|quantum number]]" of the vibration. Clearly then, not only are the modes of oscillation discrete (not quantum), each individual mode has its possible energies quantized (definitely quantum). Taking inspiration from electromagnetic radiation, where the [[photon]] is the quantum of energy, we call **[[phonon]]** the quantum of energy of [[acoustic radiation]].

A phonon behaves in many ways like a [[particle]]. In fact, it is the particle aspect of the sound wave, just like how the photon is the particle aspect of the light wave. However, phonons aren't "real" particles: they're a special class of phenomenon called a [[quasiparticle]]. Basically, they are external phenomena that display particle-like behavior. The big difference is that quasiparticles don't have "physicality", they can't exist on their own. A photon is its own thing and is capable of traversing the vacuum on its own, such as when it's shot out from a [[stella|star]] into outer space. A phonon isn't "its own thing", it is just that the vibration of a chain of oscillator produces behavior that is consistent with a particle formulation, so we describe it as a particle. It's a purely mathematical invention. This is why phonons are part of a class of quasiparticles generally called **collective excitations**. They aren't *actual particles*, they are a collective vibration of several other objects that just happens to *behave like a particle*[^4].

Phonons are useful because they are technically [[Boson|bosons]], so if we put a lot of them together (i.e. cause some vibrations in the crystal), we get a [[Bose gas]] that obeys the [[Bose-Einstein distribution]]. We can then use the whole machinery of statistical mechanics to describe the crystal with a quantum [[ensemble]] and derive macroscopically relevant thermodynamic properties about it by knowing the microscopic behavior. See [[Harmonic oscillator#Oscillator chains]] for more.
## Electronic structure
The electronic structure of a crystalline solid is a rather complicated topic, but it serves to explain a considerable portion of the nature of the material itself. Electrons are mobile and somewhat prone to being dislodged from individual ions, so they tend to be the cause of most behavior of the crystal when interacting with other materials or [[Electromagnetic radiation]].

The complication arises from trying to understand how the electrons interact with the lattice of ions they are in. There's two extremes to this interaction: on one side, the atoms are so far away that all electrons exclusively interact with their nucleus (**free atom limit**); on the other, the electrons are so weakly bound to any one nucleus in particular that they end up roaming around freely, disregarding the ions completely (**free electron limit**). The truth is, as usual, somewhere in the middle, and the real question is: how do we get there?

![[Electronic structure limits.png]]

There's two paths we could take, each starting from one edge of the potential limit. We could start with free atoms and then progressively make them close and closer, analyzing what effect this has on the energy levels of the electrons. Alternatively, we could start with free electrons and add an ionic potential, making more and more intense and seeing what that does to the electrons.

Both approaches are valid and have their merits. What they have in common is that crystal are, in principle at least, constructed from a perfectly periodic lattice of atoms, each with the same properties. Thus, the potential profile of each lattice cell is identical to that of every other cell. This makes the foundation of how electrons are handled in solid crystalline matter: a **periodic potential**.

Of course, a real crystal is not perfectly periodic. They aren't perfectly pure, leading to occasional differences in the contents of each cell and therefore the potential in proximity of those cells. Thermal effects always provide a chance that an atom is not where it's supposed to be, leading to a hole in the lattice or a misplaced atom. Ionic vibrations, as seen in the section above, also contribute to breaking perfect periodicity. Finally, electron-electron interactions are incredibly complicated. That said, the study of a periodic potential is paramount, because it sets the foundation of the quantum description of electronic structure. Just like with the fine structure of the [[hydrogen atom]] or nuclear motion after the [[Born-Oppenheimer approximation]], it's much easier to develop a theory for an ideal system, then fix it with subsequent corrective terms for each individual problem. This is what we'll be done here too, starting with the perfect periodicity of an ideal crystal.
### The periodic potential
The basic idea is simple. We have a lattice that repeats every $\mathbf{R}$. So, our potential, which we'll call $U(\mathbf{r})$ and is due to the ions in that lattice, repeats in the same way:
$$U(\mathbf{r})=U(\mathbf{r}+\mathbf{R})\tag{3}$$
Now, we need to choose a $U(\mathbf{r})$. That's a hard task. An even harder task is trying to solve the wavefunction of the whole crystal; we can't just put this in a Hamiltonian containing every single ion and electron in the crystal and expect it to work. It's unthinkable to even start solving such an equation. What we'll do is exploit the fact that, regardless of what the potential looks like, it must satisfy $(3)$. This statement already contains a lot of useful information that we can discover.

Let's start by solving for a periodic potential on a single, lone electron. The Schrödinger equation then is
$$- \frac{\hbar^{2}\nabla^{2}}{2m_{e}}\psi(\mathbf{r})+U(\mathbf{r})\psi(\mathbf{r})=E\psi(\mathbf{r})\tag{4}$$
From here, we can make a first, quite trivial choice of periodic potential: $U(\mathbf{r})=0$. A constant *is technically* periodic, and if we make this choice, we get the right edge of the potential limits: the free electron limit. In other words, we went back to the [[Sommerfeld model]] of electronic structure. Of course, we won't *use* the zero potential, but it does prove that the older Sommerfeld model is just a specific case of the periodic potential model, and by extension that we're proving something more general here.

Some terminology: an independent electron (that is, independent of other electrons, not of ions) that obeys a one-electron Schrödinger equation $(4)$ is said to be a **Bloch electron**. The Sommerfeld free electron is a subtype of the Bloch electron that occurs when the potential is zero. A Bloch electron is interesting because it satisfies **[[Bloch's theorem]]**, which has a whole host of consequences regarding both the electron and the structure of the crystal itself; go read that page before continuing here.

One key way Bloch electrons differ from free ones is how their energy levels are distributed. In the Sommerfeld model (a [[Fermi gas]]; assume $T=0$ for simplicity) the electrons all pile up from the lowest energy state to the highest. Each energy level is determined by $\varepsilon(\mathbf{k})=\hbar^{2}k^{2}/2m\leq\varepsilon_{F}$, where $\varepsilon_{F}$ is the [[Fermi energy]]. Meanwhile, Bloch electrons have their energy levels identified by $\varepsilon_{n}(\mathbf{k})$, which includes the additional band index $n$ on top of the wavevector $\mathbf{k}$ and does not have a simple analytical form. If each level is to only be counted once, $\mathbf{k}$ must be confined to a single value per primitive cell, so that if there are $N$ cells, there are $N$ values of $\mathbf{k}$. As the energy levels fill up from lowest to highest, we recognize two possible cases:
1. Some bands are completely filled. Others are completely empty. The difference in energy between the highest occupied level (top of the highest occupied band) and the lowest occupied level (bottom of lowest unoccupied band) in known as the **band gap**. A significant band gap ($\gg k_{B}T$ where $T$ is room temperature) is indicative of an **[[Dielectric|insulator]]**. A smaller, but still relevant band gap ($\sim k_{B}T$) is indicative of an **[[intrinsic semiconductor]]**.
2. Some bands are partially filled. There's no hard line between filled and empty bands. In this case, the Fermi energy (energy of highest occupied state) is somewhere in the range of one or more bands. While this means that there is no global [[Fermi surface]], each band will have its own independent Fermi surface to divide *its* occupied levels from the unoccupied ones. For practical reasons, different terminology is used: the set of all band-specific Fermi surfaces is considered as the whole crystal's Fermi surface. Meanwhile, the band-specific surfaces are called **branches** of the (total) Fermi surface. So a crystal of this kind has one singular Fermi surface, and each energy band has a branch of that surface. Crystals that possess a Fermi surface are **metals**.
#### Electronic density of states[^5]
In any quantum statistical mechanical scenario dealing with a very large number of components, it's often convenient to assume that such a huge number of possibilities can turn a discrete set of levels into a continuous set of levels by sheer virtue of the fact that the difference between each level will be minuscule. Thus, one can turn sums into integrals weighed by a density of states function. This is the gist of the [[Thomas-Fermi approximation]] and it works quite well with energy band levels too.

It's pretty common in a many-electron scenario to need to calculate a quantity $Q$ of the form
$$Q=2\sum_{n,\mathbf{k}}Q_{n}(\mathbf{k})$$
where the factor 2 takes [[spin]] [[Degenerazione|degeneracy]] into account and the sum is over all distinct levels $\mathbf{k}$ in a single primitive cell of the reciprocal lattice. If the volume is very large then we can define the volume density $q$ of $Q$ as
$$q=\lim_{ V \to \infty } \frac{Q}{V}=2\sum_{n} \frac{Q_{n}(\mathbf{k})}{(2\pi)^{3}}d^{3}k$$
If $Q_{n}(\mathbf{k})$ depends only on $\varepsilon_{n}(\mathbf{k})$, then we can define a density of states (or **density of levels** in this context) function $g(\varepsilon)$ per unit volume such that
$$q=\int g(\varepsilon)Q(\varepsilon)d\varepsilon \quad\text{where }g(\varepsilon)=\sum_{n}g_{n}(\varepsilon)\quad\text{and }g_{n}(\varepsilon)=\int _\text{cell} \frac{\delta(\varepsilon-\varepsilon_{n}(\mathbf{k}))}{4\pi ^{3}}d^{3}k$$
using a [[Delta di Dirac|Dirac delta]]. The density of levels in the band $n$ can also be defined as the function for which
$$g_{n}(\varepsilon)d\varepsilon=\frac{2}{V}\times\text{number of wavevectors allowed in }[\varepsilon,\varepsilon+d\varepsilon]$$
In the continuous limit this becomes
$$g_{n}(\varepsilon)d\varepsilon=\int _\text{cell} \frac{d^{3}k}{4\pi ^{3}}\times \begin{cases}
1 & \text{if }\varepsilon_{n}(\mathbf{k})\in[\varepsilon,\varepsilon+d\varepsilon] \\
0 & \text{otherwise}
\end{cases}$$
Since $d\varepsilon$ is infinitesimal, the density of states can be calculated as an integral on a constant energy surface $S_{n}(\varepsilon)$ of energy $\varepsilon_{n}(\mathbf{k})=\varepsilon$:
$$g_{n}(\varepsilon)d\varepsilon=\int_{S_{n}(\varepsilon)} \frac{\delta k(\mathbf{k})}{4\pi ^{3}}dS$$
$\delta k(\mathbf{k})$ is the distance (in reciprocal space) between the surfaces at $\varepsilon$ and $\varepsilon+d\varepsilon$. The [[gradient]] $\nabla_{\mathbf{k}}\varepsilon_{n}(\mathbf{k})$ is normal to the constant-energy surface, so
$$\varepsilon+d\varepsilon=\varepsilon+\lvert \nabla_{\mathbf{k}}\varepsilon_{n} \rvert \cdot \delta k(\mathbf{k})\quad\Rightarrow \quad \delta k(\mathbf{k})=\frac{d\varepsilon}{\lvert \nabla_{\mathbf{k}}\varepsilon_{n} \rvert }$$
Plugging this into the integral yields
$$g_{n}(\varepsilon)=\int_{S_{n}(\varepsilon)} \frac{1}{4\pi ^{3}} \frac{dS}{\lvert \nabla_{\mathbf{k}}\varepsilon_{n} \rvert }$$
This goes to show that the density of states in an energy band is dependent on the geometry of the constant energy surface $S_{n}(\varepsilon)$. It increases when the gradient is small (the states are tightly packed and with little separation) and decreases when it's large (the levels are far apart).
#### Weak potential
Intuitively, given the large nuclear charges of the atoms that make up matter, you'll probably assume that the periodic potential that applies onto the electrons would be rather intense. But for many metals, you'd be *wrong*. As it turns out, modern theoretical and experimental studies on metals of the I, II, III and IV group of the periodic table indicate that their electrons are hardly affected by this potential which, while nonzero, is *almost* constant. These metals are referred to as **nearly free electron** metals and their study begins from the [[Sommerfeld model]] of free electrons to which we add a weak periodic potential.

Firstly, though, we should talk about *why* the potential is so weak. After all, it's quite counter-intuitive. There are two reasons why:
1. Ion-electron interaction falls off with distance due to being electromagnetic. Only the outermost electrons are conduction electrons and they are forbidden by the [[Pauli exclusion principle]] from going near the ion since they cannot cross the already completed inner shells. Thus, conduction electrons are consistently far from ions.
2. The potential felt by the conduction electron is weaker than imagined. This is because core electron shells screen the ion potential. Moreover, the high mobility of conduction electrons further screens and diminishes the net potential that is felt by them.

These are qualitative reasons of course, but the point remains. The potential in most metals is quite weak and almost constant. We can use this to our advantage to get some results about metallic electronic structure.

We start from the single-electron Schrödinger equation that can be found in [[Bloch's theorem#Fourier series proof]][^6]:
$$\left( \frac{\hbar^{2}k^{2}}{2m}-\varepsilon \right)c_{\mathbf{k}}+\sum_{\mathbf{K}}U_{\mathbf{K}}c_{\mathbf{k}-\mathbf{K}}=0$$
We need to solve these equations. To do so, we need the coefficients $c_{\mathbf{k}},c_{\mathbf{k}-\mathbf{K}},c_{\mathbf{k}-\mathbf{K}'},\ldots$, assuming we know the potential $U$. We will start in the free electron limit. Then, we'll add a potential later. We are legitimized in doing this because, since the potential is so weak, we can treat it as a perturbation using [[Teoria delle perturbazioni|perturbation theory]].

To start, we'll use a 1D crystal like we did for vibrations. We'll express the potential in a [[Fourier series]]
$$U(x)=\sum_{n}U_{n}e^{inKx}$$
We will use the arbitrary constant of the potential to set $U_{0}=0$. Assuming [[parità|parity]] [[symmetry]] for the crystal, we also have $U_{n}=U_{-n}$. We require that only $c_{k},c_{k-K},c_{k+K}$ are nonzero, with all other terms vanishing. Consequently, we also only retain $U_{0}$ (which is zero anyway) and $U_{1}=U_{-1}=U$. This decision cannot be justified at this stage, but varying the number of coefficients that are kept has consequences on the predicted behavior. We'll return to this in a moment when it's easier to explain. Keeping only three coefficients leads to a system of three equations, with means three solutions (energy bands) for each $k$. The equations are
$$\begin{align}
\left( \frac{\hbar^{2}(k-K)^{2}}{2m} -\varepsilon\right)c_{k-K}+Uc_{k}&=0 \\
\left( \frac{\hbar^{2}k^{2}}{2m} -\varepsilon\right)c_{k}+Uc_{k-K}+Uc_{k+K}&=0 \\
\left( \frac{\hbar^{2}(k+K)^{2}}{2m} -\varepsilon\right)c_{k+K}+Uc_{k}&=0
\end{align}$$

We start in the free electron limit, so $U(x)=0$ for all $x$. That's like saying $U_{n}=0$ for all $n$, so in the equations above $U=0$. This leaves us with
$$\begin{align}
\left( \frac{\hbar^{2}(k-K)^{2}}{2m} -\varepsilon\right)c_{k-K}&=0 \\
\left( \frac{\hbar^{2}k^{2}}{2m} -\varepsilon\right)c_{k}&=0 \\
\left( \frac{\hbar^{2}(k+K)^{2}}{2m} -\varepsilon\right)c_{k+K}+&=0
\end{align}$$
These equations are effectively just squares of $k$ multiplied and shifted by a constant and then set to zero. In other words, these are all [[parabola|parabolas]] ([[convex]]/concave up specifically).

![[Weak periodic potential coefficients.png]]

Here we can see what the solution looks like in arbitrary units. Due to periodicity arguments, only the part inside the first Brillouin zone (1BZ) really matters, since we just copy and paste that solution throughout the entire solid. We can see that the each coefficient that we retain adds one more parabola to represent the potential *outside* of the 1BZ. These are not insignificant though, as the outer potentials cross into the 1BZ and therefore affect it too. This is the mathematical statement that each electron is not only affected by its closest ion, but also by nearby ions too, just to a lesser extent. The more coefficients we keep, the more ions we consider in the interaction. As we can see by the right graph in the figure, the further the ions are, the higher the energy is when they cross over to the 1BZ. This means that outer ions only really matter in high-energy scenarios.

This is what happens for free electrons in a periodic lattice. Now let's take another step and turn on the potential. We start from a free electron [[Hamiltonian]] $H_{0}=p^{2}/2m$. These are [[Particella libera (quantistica)|free particles]] so their (continuous, delocalized, not physically valid) eigenstates are [[Plane wave|plane waves]] $\ket{\mathbf{k}}$ with eigenvalues $\varepsilon_{0}(\mathbf{k})=\hbar^{2}\lvert \mathbf{k} \rvert^{2}/2m$. Now consider a weak perturbation to this Hamiltonian — our potential — so that we get $H=H_{0}+U(\mathbf{r})$.

Adding a perturbation to an otherwise stable system always adds a form of quantum dynamics, that is the possibility of a [[state transition]]. The [[matrix element]] of a transition from the state $\ket{\mathbf{k}}$ to $\ket{\mathbf{k}'}$ is
$$\braket{ \mathbf{k}' | U | \mathbf{k} } =\frac{1}{V}\int_{\mathbb{R}^{3}} e^{i(\mathbf{k}-\mathbf{k}')\cdot \mathbf{r}}U(\mathbf{r})d\mathbf{r}\equiv U_{\mathbf{k}'-\mathbf{k}}$$
This is zero unless $\mathbf{k}-\mathbf{k}'$ is a reciprocal lattice vector $\mathbf{K}$. Thus, a plane wave $\ket{\mathbf{k}}$ can be transitioned to another one $\ket{\mathbf{k}'}$ only if they differ by a reciprocal lattice vector.

Let's apply [[Teoria delle perturbazioni non degenere|non-degenerate perturbation theory]] at the first order:
$$\varepsilon(\mathbf{k})=\varepsilon_{0}(\mathbf{k})+\braket{ \mathbf{k} | U | \mathbf{k} } =\varepsilon_{0}(\mathbf{k})+U_{0}$$
The first order correction is a constant, so we'll set $U_{0}=0$ since potentials are always defined up to as constant. With the second order correction we get
$$\varepsilon(\mathbf{k})=\varepsilon_{0}(\mathbf{k})+\sum_{\mathbf{k}'=\mathbf{k}+\mathbf{K}}^{\mathbf{K}\neq0} \frac{\lvert \braket{ \mathbf{k}' | U | \mathbf{k} }  \rvert^{2}}{\varepsilon_{0}(\mathbf{k})-\varepsilon_{0}(\mathbf{k}')}$$
The sum occurs only over $\mathbf{K}\neq 0$, which means over transitions between plane waves with a different wavevector than the unperturbed case (basically, only between states permitted by the perturbation). Of course, we're assuming non-degeneracy here. If for any reason any two states that are summed over have the same energy level ($\varepsilon_{0}(\mathbf{k})=\varepsilon_{0}(\mathbf{k}')$) then the correction diverges. So, when does degeneracy occur?

Of course the condition above, $\varepsilon_{0}(\mathbf{k})=\varepsilon_{0}(\mathbf{k}')$, must apply, but also $\mathbf{k}'=\mathbf{k}+\mathbf{K}$. In the 1D case we know that $K=2\pi n/a$ and $\varepsilon_{0}(k)\sim k^{2}$. If we impose these two conditions we get
$$\begin{align}
\varepsilon_{0}(k)&=\varepsilon_{0}(k+K) \\
k^{2}&=(k+K)^{2} \\
k^{2}&=k^{2}+2kK+K^{2} \\
2kK+K^{2}&=0
\end{align}$$
Dividing by $K\neq0$ we get $2k+K=0$ which means
$$k=- \frac{K}{2}=- \frac{n\pi}{a}\quad\Rightarrow \quad k'=k+K = \frac{n\pi}{a}$$
Degeneracy happens when the wavevectors are precisely at the edges of the 1BZ (*of course*, it's periodic, that's the entire point). If this happens, we can't rely on non-degenerate perturbation theory and we need to upgrade to the [[Teoria delle perturbazioni degenere|degenerate version]]. The [[matrix element|matrix elements]] are
$$\begin{align}
\braket{ \mathbf{k} | H | \mathbf{k} } &=\varepsilon_{0}(\mathbf{k}) \\
\braket{ \mathbf{k}' | H | \mathbf{k}' } &= \varepsilon_{0}(\mathbf{k}')=\varepsilon_{0}(\mathbf{k}+\mathbf{K}) \\
\braket{ \mathbf{k} | H | \mathbf{k}' } &= U_{\mathbf{k}-\mathbf{k}'}=U_{\mathbf{K}}^{*} \\
\braket{ \mathbf{k}' | H | \mathbf{k} } &= U_{\mathbf{k}'-\mathbf{k}}=U_{\mathbf{K}}
\end{align}$$
Since the potential is a real function, $U_{-\mathbf{K}}=U_{\mathbf{K}}^{*}$. The degenerate states $\ket{\mathbf{k}}$ and $\ket{\mathbf{k}+\mathbf{K}}$ form a two-dimensional [[vector space]] where each state is a [[linear combination]] of the two:
$$\ket{\psi} =\alpha \ket{\mathbf{k}} +\beta \ket{\mathbf{k}+\mathbf{K}} $$
Applying degenerate perturbation theory gives the [[eigenvalue equation]]
$$\begin{pmatrix}
\varepsilon_{0}(\mathbf{k}) & U_{\mathbf{K}}^{*} \\
U_{\mathbf{K}} & \varepsilon_{0}(\mathbf{k}+\mathbf{K})
\end{pmatrix}\begin{pmatrix}
\alpha \\
\beta
\end{pmatrix}=E\begin{pmatrix}
\alpha \\
\beta
\end{pmatrix}$$
$E$ is determined by
$$\boxed{(\varepsilon_{0}(\mathbf{k})-E)(\varepsilon_{0}(\mathbf{k}+\mathbf{K})-E)-\lvert U_{\mathbf{K}} \rvert ^{2}=0}$$
As an example, let's see what happens if both $\mathbf{k}$ and $\mathbf{k}'=\mathbf{k}+\mathbf{K}$ are on the edges of the Brillouin zone. Since $\varepsilon_{0}(\mathbf{k})=\varepsilon_{0}(\mathbf{k}+\mathbf{K})$ the above equation becomes
$$(\varepsilon_{0}(\mathbf{k})-E)^{2}=\lvert U_{\mathbf{K}} \rvert ^{2}\quad\Rightarrow \quad E_{\pm}=\varepsilon_{0}(\mathbf{k})\pm \lvert U_{\mathbf{K}} \rvert $$
This creates an energy interval of space between the top of a lower energy band ($E_{-}$) and the bottom of higher one ($E_{+}$) that is exactly the size of $2\lvert U_{\mathbf{K}} \rvert$. This interval is called a **gap**. There are no valid electron states in the gap: an electron must either stay in the lower band or jump to the higher one, requiring a state transition of *at least* $2\lvert U_{\mathbf{K}} \rvert$ in distance.

![[Energy gaps.png]]

Let's see what this entails in 1D. Consider a periodic potential like
$$U(x)=\tilde{U}\cos\left( \frac{2\pi x}{a} \right)\quad\text{where }\tilde{U}>0$$
The edges of the Brillouin zone are at $k=\pm \pi/a$. To cause the above degeneracy, we pick wavevectors at the edges, so $k=\pi/a$ and $k'=-k=-\pi/a$. From the eigenvalue equation we see that the degenerate eigenstates are
$$\ket{\psi_{\pm}} =\frac{\ket{k} \pm \ket{k'} }{\sqrt{ 2 }}$$
Using [[Rappresentazioni dello stato|position representation]] $\psi(x)=\braket{ x | k }$, we get two plane waves like $\ket{k}\to e^{i\pi x/a}$ and $\ket{k'}\to e^{-i\pi x/a}$. The position representation of the degenerate states is
$$\psi_{+}(x)\simeq e^{i\pi x/a}+e^{-i\pi x/a}\propto \cos\left( \frac{\pi x}{a} \right),\quad \psi_{-}(x)\simeq e^{i\pi x/a}-e^{-i\pi x/a}\propto \sin\left( \frac{\pi x}{a} \right)$$
$\lvert \psi_{+} \rvert^{2}$ has maxima at the potential maxima. Similarly, $\lvert \psi_{-} \rvert^{2}$ has maxima at the potential minima. As such, $\psi_{+}$ is higher energy than $\psi_{-}$. The energy gap can be found by solving for the coefficients of the potential $U_{n}$ of the potential $U(x)=\sum_{n}U_{n}e^{inKx}$ and then squaring them.

![[Band gap in 1D.png]]

The result is something like this. The left plot shows three coefficients, $U_{-1},U_{0},U_{1}$ and the right plot shows five, $U_{-2},U_{-1},U_{0},U_{1},U_{2}$. Where the lines here would have been parabola in the zero-potential case, we can see that they now split at the edges of the 1BZ, creating energy gaps. Also, we can see another effect of solving the equations with more or less coefficients: the three-coefficient solution missed the band higher band gap since it had $\lvert U_{\pm2} \rvert^{2}=\lvert 0 \rvert^{2}=0$, whereas the five-coefficient shows it. This is another reason why more coefficients provide better results.

:::image
![[Energy gap schemes.png]]
Another plot showing the new energy bands. There is more than one convention to display the energy bands. The left method, called the **extended zone scheme**, shows the new bands (solid line) over the original band (dashed lines in the gaps) across multiple Brillouin zones. The right method, called the **reduced zone scheme**, uses the fact that wavevectors can always be reduced to the 1BZ by translating them by $\mathbf{K}$. The resulting plot hence only includes the 1BZ with multiple bands stacked on top of each other. The bottom band is in the 1BZ, the band above is in the 2BZ, etc.
:::

Another interesting detail is that, since we're dealing with quantum waves, we can use the [[Planck formula]] for energy, $E=\hbar \omega$. That might sound irrelevant, but the [[group velocity]] of a wave (read: electron) is
$$v_{g}=\frac{d\omega(k)}{dk}=\frac{1}{\hbar} \frac{dE(k)}{dk}$$
But we *do* have the energy $E(k)$, it's the energy band itself. Thus, the group velocity of an electron is determined by the slope of the energy band. Since bands with a gap flatten out at the edges of the 1BZ, waves with wavevectors on the edges have zero group velocity: they are [[standing wave|standing waves]].

Also due to the Planck formula, energy and [[Frequency|angular frequency]] are interchangeable. Since energy bands are functions of $k$ to $E$, they can also be seen as functions of $k$ to $\omega$. But a function $\omega(k)$ of a wave is a [[dispersion|dispersion relation]]. Thus, the energy bands are the dispersion relations of the Bloch electrons.

Ultimately, the takeaways here are these.

> [!success] Weak periodic potential effect
> Applying a periodic potential to a free-electron model causes the parabolic energy curves to distort at the edges of the first Brillouin zone and loop, a phenomenon called **backfolding**. The potential breaks the singular energy band into multiple ones, each divided by a **gap**. Electrons are no longer allowed to reach every energy state: states inside a gap are prohibited. The energy spectrum of electrons is therefore no longer (almost) continuous. It has discontinuities in the gaps. In the weak potential case, the size of the gaps is linearly dependent on the magnitude of the potential.

### Tight-binding
The **tight-binding** model attempts a different kind of description as the weak periodic potential. Whereas the weak potential started with free electrons and added a small but significant potential to the mix, the tight-binding model works from the other side. It starts with free *atoms* and then pushes them closer and closer until the effects of vicinity start to become relevant, namely the superposition of [[atomic orbital|atomic orbitals]]. The actual superposition might be small or large, and it really depends on the energy level of the electrons themselves. The tight-binding model attempts to explain cases in which the superposition of atomic orbitals is small but still significant.

Whereas the weak potential described electrons that were largely free to move, tight-binding describes electrons that are largely unable to move and tightly bound to their ion, hence the name. This makes it well-positioned to explain the behavior of [[Dielectric|insulators]] instead of [[Conductor|conductors]], where electron movement is scarce.

We start from the single-electron Hamiltonian for an isolated atom, under the assumption that the solid is entirely made of one type of atom (an pure elemental solid):
$$\hat{H}_\text{atom}=- \frac{\hbar^{2}\nabla ^{2}}{2m}+U_\text{atom}(\mathbf{r})$$
$U_\text{atom}(\mathbf{r})$ is the potential that each electron feels with respect to the atom that it is bound to. Now, let's combine all of the atoms to make a solid in a manner similar to [[Linear Combination of Atomic Orbitals|LCAO]] for [[Molecule|molecules]]. For example, imagine sodium, which only has one valence electron in $3s$, with energy $E_{3s}$ and eigenstate $\ket{3s}$. If each sodium atom is exactly on a Bravais lattice point $\mathbf{R}$ then we get
$$\begin{align}
\hat{H}_\text{solid}&=- \frac{\hbar^{2}\nabla^{2}}{2m}+\sum_{\mathbf{R}}U_\text{atom}(\mathbf{r}-\mathbf{R}) \\
&=- \frac{\hbar^{2}\nabla^{2}}{2m}+U_\text{atom}(\mathbf{r})+\sum_{\mathbf{R}\neq 0}U_\text{atom}(\mathbf{r}-\mathbf{R})
\end{align}$$
The three terms are the [[kinetic energy]] of the electron, the potential due to the atom the electron is bound to and the potential due to every other atom. We'll group the first two in the single-atom Hamiltonian $\hat{H}_\text{atom}$ and call the third $\mathcal{U}(\mathbf{r})$ to distinguish it:
$$\hat{H}_\text{solid}=\hat{H}_\text{atom}+\mathcal{U}(\mathbf{r})$$
We now have the Hamiltonian of the solid as seen from an electron of an atom, with a corrective term $\mathcal{U}$ added onto it. This same idea an be applied to every electron.

Now imagine that the atoms farther away from each other. Each single-atom eigenfunction $\phi_{n}(r)$ has eigenvalue $E_{n}$. We can write the energy eigenvalues of the solid as
$$\langle H \rangle _{\phi_{n}}=\int \phi_{n}^{*}(\mathbf{r})H_\text{solid}\phi_{n}(\mathbf{r})d\mathbf{r}=E_{n}+\int \phi_{n}^{*}(\mathbf{r})\mathcal{U}(\mathbf{r})\phi_{n}(\mathbf{r})d\mathbf{r}=E_{n}-\beta$$
The $\beta$ term depends highly on how superimposed the various wavefunctions are and is zero if they do not superimpose. The eigenfunctions $\phi_{n}$ go to zero before the potential does. For a solid made of $N$ atoms, we get $N$ degenerate solutions for each of the Hamiltonian eigenvalues. We expect this because there is no atom-atom interaction.

Let's see what happens with we include the interaction. We'll use an ansatz to declare the form of the wavefunction of each electron as
$$\psi_{\mathbf{k}}(\mathbf{r})=\frac{1}{\sqrt{ N }}\sum_{\mathbf{R}}c_{\mathbf{k},\mathbf{R}}\phi_{n}(\mathbf{r}-\mathbf{R})$$
This is a linear combination of atomic wavefunctions $\phi_{n}$ on the Bravais lattice. The coefficients are unknown and the thing we need to determine. For this to make sense in a lattice context, it needs to be a Bloch wave, so the coefficients will have to be exponentials:
$$\psi_{\mathbf{k}}(\mathbf{r})=\frac{1}{\sqrt{ N }}\sum_{\mathbf{R}}e^{i\mathbf{k}\cdot \mathbf{r}}\phi_{n}(\mathbf{r}-\mathbf{R})$$
The values $\mathbf{k}$ are those allowed by the boundary conditions. These wavefunctions satisfy [[Bloch's theorem]]:
$$\begin{align}
\psi_{\mathbf{k}}(\mathbf{r}+\mathbf{R}')&=\frac{1}{\sqrt{ N }}\sum_{\mathbf{R}}e^{i\mathbf{k}\cdot \mathbf{R}}\phi_{n}(\mathbf{r}-\mathbf{R}+\mathbf{R}') \\
&=\frac{1}{\sqrt{ N }}e^{i\mathbf{k}\cdot \mathbf{R}'}\sum_{\mathbf{R}}e^{i\mathbf{k}\cdot(\mathbf{R}-\mathbf{R}')}\phi_{n}(\mathbf{r}-(\mathbf{R}-\mathbf{R}')) \\
(\mathbf{R}\to \mathbf{R}''=\mathbf{R}-\mathbf{R}')&=\frac{1}{\sqrt{ N }}e^{i\mathbf{k}\cdot \mathbf{R}'}\sum_{\mathbf{R}''}e^{i\mathbf{k}\cdot \mathbf{R}''}\phi_{n}(\mathbf{r}-\mathbf{R}'') \\
&=e^{i\mathbf{k}\cdot \mathbf{R}'}\psi_{\mathbf{k}}(\mathbf{r})
\end{align}$$
The energy eigenvalues are calculated similarly to the [[Born-Oppenheimer approximation#The hydrogen-hydrogen molecule|hydrogen molecule]].
$$\begin{align}
E(\mathbf{k})&=\int \psi_{\mathbf{k}}^{*}(\mathbf{r})\hat{H}_\text{solid}\psi_{\mathbf{k}}(\mathbf{r})d\mathbf{r} \\
&=\frac{1}{N}\sum_{\mathbf{R},\mathbf{R}'}e^{i\mathbf{k}\cdot(\mathbf{R}-\mathbf{R}')}\int \phi_{n}^{*}(\mathbf{r}-\mathbf{R}')\hat{H}_\text{solid}\phi_{n}(\mathbf{r}-\mathbf{R})d\mathbf{r} \\
&=\ldots
\end{align}$$
Considering periodic boundary conditions, we can remove the dependency on $\mathbf{R}$ and merge the sums
$$\ldots=\sum_{\mathbf{R}}e^{i\mathbf{k}\cdot \mathbf{R}}\int \phi_{n}^{*}(\mathbf{r})\hat{H}_\text{solid}\phi_{n}(\mathbf{r}-\mathbf{R})d\mathbf{r}$$
The total energy eigenvalue must be the sum of this piece and the one we found before for the individual atoms:
$$E(\mathbf{k})=E_{n}-\beta+\sum_{\mathbf{R}\neq 0}e^{i\mathbf{k}\cdot \mathbf{R}}\int \phi_{n}^{*}(\mathbf{r})\hat{H}_\text{solid}\phi_{n}(\mathbf{r}-\mathbf{R})d\mathbf{r}$$
The integral is the real problem here. Let's see what we can do with it:
$$\int \phi_{n}^{*}(\mathbf{r})\hat{H}_\text{solid}\phi_{n}(\mathbf{r}-\mathbf{R})d\mathbf{r}=E_{n}\int \phi_{n}^{*}(\mathbf{r})\phi_{n}(\mathbf{r}-\mathbf{R})d\mathbf{r}+\int \phi_{n}^{*}(\mathbf{r})\mathcal{U}(\mathbf{r})\phi_{n}(\mathbf{r}-\mathbf{R})d\mathbf{r}$$
The first integral on the right is largely inconsequential: it measures the overlap of wavefunctions evaluated at different sites on the lattice, so it's never going to be significant. The second integral however cannot be ignored: the presence of $\mathcal{U}(\mathbf{r})$ makes $\mathcal{U}(\mathbf{r})\phi_{n}(\mathbf{r}-\mathbf{R})$ nontrivial even in the region it overlaps $\phi_{n}^{*}(\mathbf{r})$ so we can't drop it. Instead, we'll add a minus sign and call it $t=-\int \phi_{n}^{*}(\mathbf{r})\mathcal{U}(\mathbf{r})\phi_{n}(\mathbf{r}-\mathbf{R})d\mathbf{r}$. This term is known as the **hopping term** and measures the [[state transition]] [[probability]] of an electron from its own orbital to an orbital of nearby atom.

The energy band function, or the electron dispersion relation depending on how you want to see it, then is
$$\boxed{E(\mathbf{k})=E_{n}-\beta-\sum_{\mathbf{R}\neq 0}t(\mathbf{R})e^{i\mathbf{k}\cdot \mathbf{R}}}$$
This shows the change of an energy level from an independent atom one $E_{n}$ to a lattice one $E(\mathbf{k})$. $\beta$ measures transition probabilities from an orbital to an orbital of the same atom. $t$ measures the same, but to orbitals of other atoms.

Let's a run a simple calculation in a 1D crystal of lattice parameter $a$ for $s$-orbital valence electrons. Each electron has energy eigenvalue $E_{s}$ in the free atom limit. Normally, we'd need to sum over all other atoms, but $s$ wavefunctions decay fast, so in practice only the nearest neighbor matters, which are at $\pm a$. Moreover, $s$ orbitals are spherically symmetric, so $t(-a)=t(a)=t_{s}$. All in all, we get
$$E_{s}(k)=E_{s}-\beta_{s}-t_{s}(e^{ika}+e^{-ika})=E_{s}-\beta_{s}-2t_{s}\cos (ka)$$
$\beta_{s}$ is the value of $\beta$ calculated in the $s$ orbital. Both $E_{s}$ and $\beta_{s}$ are constant, so maxima and minima are chosen by the cosine. The minimum energy is for $k=0$ and the maximum is at the Brillouin zone edge at $k=\pi/a$. The center of the energy band is shifted by $-\beta_{s}$ compared to $E_{s}$ (typically a small shift). These are the edges of the band. The width of the band is $4t_{s}$, as seen by the fact that the cosine term goes from $-2t_{s}$ to $2t_{s}$. This shows that it's the hopping term that determines how wide a band is in the tight-binding model. Hopping depends on the distance, increasing for small distances, so the closer the atoms are, the wider the bands are; this is logical, as closer atoms make transferring electrons easier and therefore conductivity higher.

:::image
![[Tight-binding s-band 1D.png]]
The $s$-band of a 1D crystal in tight-binding in the first Brillouin zone.
:::

You could then solve this same problem using $p$ orbitals instead. Then $d$, then $f$, and so on. Each orbital will give a brand new, separate bands, and because of that, the bands inherit the names of the orbitals: $s$-band, $p$-band, $d$-band... The bottom of each band, the lowest energy level, corresponds to the energy of the bonding [[molecular orbital|molecular orbitals]] of that type ($\sigma$ for $s$-band, $\pi$ for $p$-band...), whereas the top corresponds to the energy of the antibonding one.

![[Tight-binding s- and p-band 1D.png]]

One thing that is very interesting to look at is that the bands look quite similar to the ones in the weak potential limit. They're not *identical* of course, but we can see that at the bottom of each period of the wave, the band looks more or less parabolic. In fact, for small $k$ around the minimum, the dispersion is, to first order, $E(k)=E_{0}+ta^{2}k^{2}$ for some constant $E_{0}$. A shifted parabola basically, just like for free electrons. This lends itself to describing electrons with $k$ near the minimum as *free electrons* with an *effective mass* $m^{*}$ such that their energy satisfies
$$\frac{\hbar^{2}k^{2}}{2m^{*}}=ta^{2}k^{2}\quad\Rightarrow \quad \boxed{m^{*}=\frac{\hbar^{2}}{2ta^{2}}}$$
So, if for whatever reason you only need to consider electrons near the band minimum, you can actually just dispense with the entire tight-binding model (except for $t$, you need $t$) and treat them as free electrons with a mass given the formula above. This is a *weird result*, because tight-binding is useful for *insulators* of all things. We somehow managed to describe an insulator, a material defined by its *lack of freedom* on electrons, with a *free electron model*. To quote A. Wilson:

> We have the rather curious result that not only is it possible to obtain conduction with bound electrons, but it is also possible to obtain non-conduction with free electrons.

[^1]: They start to matter in high-energy conditions when the crystal starts to break down, such as a [[phase transition]] (think melting).

[^2]: In 1D space it can't be any other way, but it does matter for a 1D object in 3D space.

[^3]: In this context, they're known as **[[Born-von Karman boundary conditions]]** and more generally they require that the [[Funzione d'onda|wavefunction]] be periodic over the Bravais lattice.

[^4]: For more discussion on this, it's fascinating to notice a historical parallel here. Back in the late 1800s, physicists were hunting for the "luminiferous ether", this assumed substance that permeated the vacuum (thus not making it *really vacuum*) that allowed for electromagnetic radiation to occur. At the time, the idea of a wave was inconceivable without a medium. The wave is a distortion of the medium! And yet try as they might, they would be proved wrong by Millikan & Morley's experiment. Physicists needed to accept that some wave just exist without a medium. Well, this is it. This is the difference. We're now accustomed to photons being their own thing, so light traveling wherever it wants is perfectly normal. It's its own object that at most passes *through* other media. Meanwhile, the phonon discussion is just going through history in reverse. Now it's weird to think of a particle that *can't* exist on its own, even though historically that was always the "obviously correct" one. It's just an odd little consequence of the wave-particle duality. In fact, any wave of any kind could have this kind of treatment applied to it, regardless of whether it's medium-locked or not. The key takeaway here is that quasiparticles are "fake" and are really just a useful mathematical trick.

[^5]: This section is not particularly well-developed or well-explained. See *Solid State Physics, Ashcroft & Mermin, Chapter 8, § Density of levels* for a proper treatment.

[^6]: We are using $\mathbf{q}\to \mathbf{k}$ and $\mathbf{K}'\to \mathbf{K}$. It's a purely aesthetic change.
