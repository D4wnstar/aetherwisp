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
Soon enough however, we hit a wall. To vibrate, the ions must affect each other somehow. Of course, they do so [[Interazione elettromagnetica|electromagnetically]] (electrostatically even), but we don't know what the [[electric potential]] looks like. In order to get a solution that's can be handled by hand, we take a second, more stringent assumption:
2. The displacements from the mean equilibrium position are small compared to the distance between ions.

It might be more illuminate to read it this way: ion oscillations are small. And the answer to small oscillations is always the same: the [[harmonic oscillator]]. Thus, the electric potential varies *harmonically* in time: this is called the **harmonic approximation**. You might argue whether this assumption is even valid: fair. But recall that the mass of an ion is essentially that of the [[Nucleo atomico|nucleus]] (a "blob" of [[proton|protons]] and [[neutron|neutrons]]) and that is enormous compared to that of the few electrons surrounding it, entire orders of magnitude higher. So large in fact, the [[Born-Oppenheimer approximation]] in [[Molecule|molecules]] just does away with nuclear motion outright and *still* gets good results. Thus, it's perfectly legitimate to assume that the ions move very little around their resting spot.

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
This is the equation of motion of a [[point mass]] $M$ attached with two massless springs of elastic constant $\gamma=\phi''(a)$. It is a [[wave equation]], so we'll choose the solution for $u(na,t)\equiv u_{n}(t)$ to be a [[plane wave]]
$$u_{n}(t)=ue^{i(kna-\omega t)}\tag{2}$$
for some constant $u$. 

The complete solution also requires knowing the initial position and velocity/[[Linear momentum|momentum]] of each ion in the chain, but we don't need those to gather more information from this system. When substituting $(2)$ into $(1)$ we get
$$\begin{align}
-M\omega ^{2}\cancel{ e^{i(kan-\omega t)} }&=-\gamma[2-e^{ika}-e^{ika}]\cancel{ e^{i(kan)-\omega t} } \\
M\omega ^{2}&=\gamma[2-e^{-ika}-e^{ika}]
\end{align}$$
Extracting $\omega$, using $e^{ix}+e^{-ix}=2\cos x$ and  $(1-\cos ^{2}x)/2=\sin ^{2}x$ gives
$$\omega(k)=\sqrt{ \frac{2\gamma(1-\cos(ka))}{M} }=2\sqrt{ \frac{\gamma}{M} }\left\lvert  \sin\left( \frac{ka}{2} \right)  \right\rvert $$
This is the **[[dispersion|dispersion relation]]** of the 1D, spring-modeled, ideal crystal, which tells us the [[Frequency|angular frequency]] of the [[wave]] that carries a perturbation through the chain of ions. The wave, as usual, moves with two different velocities: the [[phase velocity]] $c=\omega/k$ and the [[group velocity]] $v_{g}=\partial \omega/\partial k$.

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

The lower branch behaves like before, with vanishing frequency at the edges and a dispersion relation of the form $\omega=ck$. This is called the **acoustic branch** of dispersion. The upper branch however has much higher frequencies and never vanishes. This is called the **optical branch** of dispersion because the higher frequencies can actually interact and couple with commonly encountered [[electromagnetic radiation]], thus defining the crystal's optical behavior.
#### Energy spectrum
The above discussion is adequate for the general solution to the wave equation, but in practice, we need some boundary conditions to fully solve it. If there are $N$ total ions in the crystal, then we can use periodic boundary conditions[^3] to state that the crystal is actually a looping ring, so $u(0)=u(Na)$.

The periodic condition enforces
$$e^{ikNa}=1\quad\Rightarrow \quad \boxed{k=\frac{2\pi}{a} \frac{n}{N}}$$
Evidently, there's only a discrete set of acceptable [[Wavenumber|wavenumbers]] for the oscillation of a 1D crystal. These wavenumbers, or rather their associated [[Frequency|frequencies]], are known as the **[[normal mode|normal modes]]** of oscillation of the system. We take these to lie between $-\pi/a$ and $\pi/a$, which is essentially saying that the must be contained in the first [[Brillouin zone]] of the [[reciprocal lattice]].

Everything that we've discovered up to now is actually fairly classical. There's nothing obligatorily quantum anywhere in here. The "quantization" of normal modes is not actually a quantum effect at all: it's just that the ions are discrete and so their modes of oscillation are also naturally discrete.

But now that we're working with specific modes of vibration, we need to deal with the kind of energy that they carry. In a macroscopic system, energy quantization doesn't matter. Energy scales are way too large for that to be significant. But we're not in a macroscopic setting, we're dealing with individual ions. So the energy *has* to be quantized and the quantization must matter because the energy scales are just that small. But the fix is simple: just change the harmonic oscillators to [[Oscillatore armonico quantistico|quantum harmonic oscillators]]. This quantizes the energy of the $k$-th mode of oscillation to
$$E_{l}(k)=\hbar \omega(k)\left( l+ \frac{1}{2} \right)$$
where $l$ is the "principal [[Numero quantico|quantum number]]" of the vibration. Clearly then, not only are the modes of oscillation discrete (not quantum), each individual mode has its possible energies quantized (definitely quantum). Taking inspiration from electromagnetic radiation, where the [[photon]] is the quantum of energy, we call **[[phonon]]** the quantum of energy of [[acoustic radiation]].

A phonon behaves in many ways like a [[particle]]. In fact, it is the particle aspect of the sound wave, just like how the photon is the particle aspect of the light wave. However, phonons aren't "real" particles: they're a special class of phenomenon called a [[quasiparticle]]. Basically, they are external phenomena that display particle-like behavior. The big difference is that quasiparticles don't have "physicality", they can't exist on their own. A photon is its own thing and is capable of traversing the vacuum on its own, such as when it's shot out from a [[stella|star]] into outer space. A phonon isn't "its own thing", it is just that the vibration of the chain of oscillator produces behavior that is consistent with a particle formulation, so we describe it as a particle. It's a purely mathematical invention. This is why phonons are part of a class of quasiparticles generally called **collective excitations**. They aren't *actual freestanding particles*, they are a collective vibration of several other objects that just happens to *behave like a particle*[^4].

Phonons are useful because they are technically [[Boson|bosons]], so if we put a lot of them together (i.e. cause some vibrations in the crystal), we get a [[Bose gas]] that obeys the [[Bose-Einstein distribution]]. We can then use the whole machinery of statistical mechanics to describe the crystal with a quantum [[ensemble]] and derive macroscopically relevant thermodynamic properties about it by knowing the microscopic behavior. See [[Harmonic oscillator#Oscillator chains]] for more.

[^1]: They start to matter in high-energy conditions when the crystal starts to break down, such as a [[phase transition]] (think melting).

[^2]: In 1D space it can't be any other way, but it does matter for a 1D object in 3D space.

[^3]: In this context, they're known as **[[Born-von Karman boundary conditions]]** and more generally they require that the [[Funzione d'onda|wavefunction]] be periodic over the Bravais lattice.

[^4]: For more discussion on this, it's fascinating to notice a historical parallel here. Back in the late 1800s, physicists were hunting for the "luminiferous ether", this assumed substance that permeated the vacuum (thus not making it *really vacuum*) that allowed for electromagnetic radiation to occur. At the time, the idea of a wave was inconceivable without a medium. The wave is a distortion of the medium! And yet try as they might, they would be proved wrong by Millikan & Morley's experiment. Physicists needed to accept that some wave just exist without a medium. Well, this is it. This is the difference. We're now accustomed to photons being their own thing, so light traveling wherever it wants is perfectly normal. It's its own object that at most passes *through* other media. Meanwhile, the phonon discussion is just going through history in reverse. Now it's weird to think of a particle that *can't* exist on its own, even though historically that was always the "obviously correct" one. It's just an odd little consequence of the wave-particle duality. In fact, any wave of any kind could have this kind of treatment applied to it, regardless of whether it's medium-locked or not. The key takeaway here is that quasiparticles are "fake" and are really just a useful mathematical trick.
