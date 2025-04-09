---
aliases:
  - Hooke's law
---
A **harmonic oscillator** is a system with an [[equilibrium point]] that, after undergoing a perturbation, experiences a restoring force $\mathbf{F}$ proportional to the displacement distance $\mathbf{x}$ according to **Hooke's law**:
$$\mathbf{F}=-k\mathbf{x}$$
with $k$ being a positive constant called the **spring constant**.
### Simple harmonic motion
If the force $F$ is the only one acting on the system, it is called a **simple harmonic oscillator**, and the moving object describes a **simple harmonic motion**. In this case, we can use [[Newton's laws|Newton's second law of motion]] to analyze the system:
$$F=ma=m\ddot{x}=-kx$$
which gives us a second-order linear differential equation
$$\ddot{x}=- \frac{k}{m}x=-\omega^{2}x$$
where $\omega=\sqrt{k/m}$ is the angular frequency. The general solution is of the form
$$x(t)=A\cos(\omega t)+B\sin(\omega t)=C\cos(\omega t+\varphi)$$
with the constants determined by the boundary conditions, as usual. This motion is periodic and the period is $T=2\pi/\omega$.

The velocity and acceleration oscillate with the same frequency, but have a different phase from the position. In particular, the velocity is minimal when the displacement is maximal, and vice versa.

The oscillator has [[Potential|potential]] energy in position $x$ equal to
$$V=\frac{1}{2}kx^{2}\tag{1}$$
and the force is conservative.
### Approximations
The harmonic oscillator is extremely important because _any_ potential $V(x)$ associated with an oscillatory motion can be approximated as a parabola of the form $(1)$ as long as the oscillation is small. To demonstrate this, we expand $V(x)$ in a [[Serie di Taylor|Taylor series]] centered at a local minimum $x_{0}$:
$$V(x)=V(x_{0})+V'(x_{0})(x-x_{0})+ \frac{1}{2}V''(x_{0})(x-x_{0})^{2}+O(x^{3})$$
Since the constant $V(x_{0})$ vanishes by deriving to obtain the force, we can subtract it without loss of generality. Furthermore, since $x_{0}$ is a [[critical point]], $V'(x_{0})=0$. Thus, we are left with the exact form
$$V(x)=\frac{1}{2}V''(x_{0})(x-x_{0})^{2}+O(x^{3})$$
which we can approximate by truncating all terms of third order and higher, which are small if the oscillations are also small:
$$V(x)\simeq \frac{1}{2}V''(x_{0})(x-x_{0})^{2}$$
which has the same form as $(1)$. $V''(x_{0})>0$ because $x_{0}$ is a minimum by construction. This means that, for small oscillations, every oscillatory motion can be treated as if it were a harmonic oscillator.
### Oscillator chains
A system made of a chain of harmonic oscillators can be solved analytically by using the fact that all quadratic forms can [[Diagonalization|diagonalized]]. These are commonly employed in atomic and solid state physics, especially in the study of crystals or as approximate models to more complicated states.
#### Phonons
The simplest case is that of a 1D crystal. Consider a series of $N$ particles (likely [[Atomo|atoms]]) on a one dimensional line, each equally spaced by a distance $a$. We define the position vector $\mathbf{n}=n\mathbf{a}$, where $n=0,1,2\ldots,N$ is the label of each atom. Each point is subject to oscillations. If we call $\xi_{\mathbf{n}}$ the distance from the [[equilibrium point]] for the particle in $\mathbf{n}$, we can write the total [[kinetic energy]] as
$$K=\frac{m}{2}\sum_{\mathbf{n}}\dot{\xi}_{\mathbf{n}}^{2}$$
using dot notation to represent the time derivative. The [[potential energy]] is
$$U=\frac{\gamma}{2}\sum_{\mathbf{n}}(\xi_{\mathbf{n}}-\xi_{\mathbf{n}-\mathbf{a}})^{2}$$
with $\gamma \in \mathbb{R}$ the elastic constant.  This is essentially an elastic potential, which encodes the idea that atoms are coupled and that moving one "pulls"  nearby atoms with it, like an elastic net. The potential gets lower if the distance $a$ is increased because atomic interaction is [[Interazione elettromagnetica|electromagnetic]] and falls off with distance. It's a simplistic model of course, but it works as a first approximation. This "springiness" of the atomic lattice is what allows waves to propagate through a solid.

The distance $\xi$ has the periodic boundary condition $\xi_{\mathbf{n}}=\xi_{\mathbf{n}+N\mathbf{a}}$, which means that the ends of the material are connected like a ring. If we describe the oscillation across all particles as a traveling [[Plane wave]] of condition $e^{i\mathbf{k}\cdot \mathbf{x}}= e^{-i\mathbf{k}\cdot (\mathbf{x}+\mathbf{L})}$ where $L=Na$ is the length of the ring, we can write our [[wave vector]] as
$$k=\frac{2\pi \mu}{L},\qquad\mathbf{k}=\frac{2\pi \mu}{Na^{2}}\mathbf{a}$$
where $\mu \in \mathbb{N}$ determines the number of possible oscillation states. This is the major difference between the crystal lattice and a continuum: there are only a discrete amount of possible oscillation states, determined by the number of atoms (i.e. nodes) in the lattice. This is similar to what happens in the [[Oscillatore armonico quantistico|quantum harmonic oscillator]]. Specifically, for a lattice of $N$ atoms, we have[^1]
$$\mu=- \frac{N}{2},\ldots, \frac{N}{2}-1$$
There are exactly $N$ modes of oscillation. Mathematically, this is because the equation we are solving is effectively an [[Equazione agli autovalori|eigenvalue equation]], in the same way as the quantum [[Buca infinita quantistica|infinite square well]], which also gives discrete solutions. These values of $\mu$ are such that the following condition on $\mathbf{k}$ always holds: $-\pi\leq \mathbf{k}\cdot \mathbf{a}\leq \pi$. This interval is the **first [[Brillouin zone]]**. Since this zone is about the wave vector (which is spatial frequency), it lies in [[reciprocal space]], i.e. the [[Teorema di Fourier|Fourier transform]] of position space.

Since the shift $\xi$ is position, we can Fourier transform it to get the reciprocal pair
$$\xi_{\mathbf{n}}=\frac{1}{\sqrt{ N }}\sum_{\mathbf{k}}A_{\mathbf{k}}e^{i\mathbf{k}\cdot \mathbf{n}},\qquad A_{\mathbf{k}}=\frac{1}{\sqrt{ N }}\sum_{\mathbf{n}}\xi_{\mathbf{n}}e^{-i\mathbf{k}\cdot \mathbf{n}}$$
where the sum happens only over the $N$ values of $\mathbf{k}$ within $[-\pi,\pi]$, i.e. in the first Brillouin zone. Since $\xi_{n}\in \mathbb{R}$ it must be $A_{\mathbf{k}}=A_{-\mathbf{k}}^{*}$. In fact, this is a [[Serie di Fourier|Fourier series]]. We also have [[Orthonormality|orthonormality]] between modes.
$$\frac{1}{N}\sum_{\mathbf{k}}e^{i\mathbf{k}\cdot(\mathbf{n}-\mathbf{n}')}=\delta_{\mathbf{n}\mathbf{n'}},\qquad\frac{1}{N}\sum_{\mathbf{n}}e^{i(\mathbf{k}-\mathbf{k}')\cdot\mathbf{n}}=\delta_{\mathbf{k}\mathbf{k'}}$$
using the [[Kronecker delta|Kronecker delta]].

Our goal is to go from position space, where oscillation modes are coupled, to momentum space, where they are independent and form the set of [[normal mode|normal modes]] of oscillations.

By substituting the Fourier series of $\xi$ into the definitions of $K$ and $U$ from before, and seeing
$$\xi_n - \xi_{n-1} \propto \sum_k A_k (1 - e^{-ik}) e^{ikn}$$
we get
$$K=\frac{m}{2}\sum_{\mathbf{n}}\dot{A}_{\mathbf{k}}\dot{A}_{-\mathbf{k}},\qquad U=\frac{m}{2}\sum_{\mathbf{k}}\Omega^{2}(\mathbf{k})A_{\mathbf{k}}A_{-\mathbf{k}}$$
where the cross-terms vanish due to being [[Orthogonality|orthogonal]] and $\Omega$ is given by
$$m\Omega ^{2}(\mathbf{k})=m\Omega ^{2}(-\mathbf{k})\quad\to \quad \Omega(\mathbf{k})=4\gamma \sin ^{2} \frac{\mathbf{k}\cdot \mathbf{a}}{2}$$
The [[Lagrangian]] is
$$L=K-U=\frac{m}{2}\sum_{\mathbf{k}}(\dot{A}_{\mathbf{k}}\dot{A}_{-\mathbf{k}}-\Omega ^{2}(\mathbf{K})A_{\mathbf{k}}A_{-\mathbf{k}})$$
Here we have essentially diagonalized the matrix. But we can make the switch to a [[Hamiltonian]] by defining the [[canonical momentum]]
$$P_{\mathbf{k}}=\frac{ \partial L }{ \partial \dot{A}_{\mathbf{k}} } =m \dot{A}_{-\mathbf{k}}$$
which can also be expressed as the antitransform of "normal" momentum $p_{\mathbf{n}}=m \dot{\xi}_{\mathbf{n}}$
$$P_{\mathbf{k}}=\frac{1}{\sqrt{ N }}\sum_{\mathbf{n}} p_{\mathbf{n}}e^{i\mathbf{k}\cdot \mathbf{n}}$$
With this
$$H=K+U=\frac{1}{2}\sum_{\mathbf{k}}\left( \frac{1}{m}P_{\mathbf{k}}P_{-\mathbf{k}}+m\Omega ^{2}(\mathbf{k})A_{\mathbf{k}}A_{-\mathbf{k}} \right)$$
##### Quantization
This is a classical Hamiltonian. Since we are working with a discrete lattice, not a continuum, we can quantize the quantities by using the [[Commutatore|commutation]] relation
$$[\hat{\xi}_{\mathbf{n}},\hat{p}_{\mathbf{n}}]=i\hbar \delta_{\mathbf{n}\mathbf{n}'}$$
This relation implies
$$[\hat{A}_{\mathbf{k}},\hat{P}_{\mathbf{k}}]=i\hbar \delta_{\mathbf{k}\mathbf{k}'}$$
And a quantum Hamiltonian
$$\hat{H}=\frac{1}{2}\sum_{\mathbf{k}}\left( \frac{1}{m}\hat{P}_{\mathbf{k}}\hat{P}_{-\mathbf{k}}+m\Omega ^{2}(\mathbf{k})\hat{A}_{\mathbf{k}}\hat{A}_{-\mathbf{k}} \right)$$
Like in the quantum harmonic oscillator, we can introduce a pair of [[Operatori di creazione e distruzione|raising and lowering operators]] $\hat{b}$ and $\hat{b}^{+}$ defined as
$$\hat{A}_{\mathbf{k}}=\sqrt{ \frac{\hbar}{2m\Omega(\mathbf{k})} }(\hat{b}_{\mathbf{k}}+\hat{b}^{+}_{-\mathbf{k}}),\qquad \hat{P}_{\mathbf{k}}=\sqrt{ \frac{m\hbar\Omega(\mathbf{k})}{2} }(\hat{b}^{+}_{\mathbf{k}}-\hat{b}_{-\mathbf{k}})$$
In terms of these, the Hamiltonian is
$$\hat{H}=\frac{\hbar}{2}\sum_{\mathbf{k}}\Omega(\mathbf{k})(\hat{b}^{+}_{\mathbf{k}}\hat{b}_{\mathbf{k}}+\hat{b}_{\mathbf{k}}\hat{b}^{+}_{\mathbf{k}})$$
This equation shows that although the starting Hamiltonian had coupled oscillation modes in position space, if we express them in momentum space they become independent of each other and non-interacting, diagonalizing the matrix. These waves of momentum $\mathbf{k}$, when quantized, are called **[[phonon|phonons]]**. They are the quantum of oscillation of a set of joint harmonic oscillators. Specifically, these are called acoustic phonons because they represent mechanical oscillations. There are other kinds, such as optical phonons. Mind you, phonons are emphatically *not* physical objects. They are convenient quantum-like abstractions that we use to reuse all the tooling we have built up in several branches of physics, but they are not "real", so to speak. They are a kind of object known as a [[quasiparticle]], an abstract object that essentially behaves like a quantum particle and can be described like one, with its own state, [[Numero quantico|quantum numbers]], etc..

$\Omega(\mathbf{k})$ can be interpreted as the potential energy associated with the wave vector $\mathbf{k}$, just like how $U(\xi)$ is the potential energy associated with position $\xi$. $\Omega(\mathbf{k})$ is the energy of each phonon.

![[Plot Phonon potential|center]]

The derivative of the potential gives us the velocity of the phonon, usually denoted as $c$ and called the **speed of sound** (again, for acoustic phonons). Note that it's not the [[velocità della luce|speed of light]], despite using the same letter. As is expected out of a harmonic oscillator, it is almost linear for small oscillations (i.e. small $\Omega$). Unlike the speed of light, which is governed directly by the laws of physics, the value of the speed of sound depends on the properties of the material.

An atom can oscillate in 3 dimensions. Accordingly, a crystal of $N$ atoms has $3N$ modes of oscillations. These modes are bound by the condition
$$\int_{0}^{\omega_{\text{max}}}f(\omega)d\omega=3N$$
where $\omega _\text{max}$ is known as the **Debye frequency** and $f(\omega)$ is the frequency [[Probability distribution|distribution]][^2]. The nature of this upper limit is due to the discrete structure of atomic matter. Remember that the waves that we are not actually continuous, they are essentially the interpolating curve between atoms as the shift and vibrate. As such, this wave can only be as frequent as the atoms are dense. Any more frequent than that and there won't be any atoms to actually oscillate. The Debye frequency is the limit.

![[Phonon max frequency.png]]
*From Kerson Huang's Statistical Mechanics*

The frequency distribution can be determined by the possible quantum states of $\mathbf{k}$ in a volume $L^{3}=V$ (similarly to the [[Thomas-Fermi approximation]]; after all, $f(\omega)$ is a just the density of frequency states):
$$f(\omega)d\omega=3\frac{1}{\left( \frac{2\pi}{L} \right)^{3}} 4\pi k^{2}dk=\frac{3V\omega ^{2}}{2\pi^{2}c^{3}}d\omega$$
The $3$ at the start is because we have three oscillation modes per atom. The maximum frequency can be found to be
$$\omega_{\text{max}}=c\left( \frac{6\pi ^{2}N}{V} \right)^{1/3}=c\left( \frac{6\pi ^{2}}{v} \right)^{1/3}$$
with $v=V/N$ the "specific volume" of each atom. The speed of sound thus is
$$c=\frac{\lambda_{\text{max}}}{2\pi} \frac{2\pi}{T}=\frac{\lambda _\text{max}\omega}{2\pi}$$
where we called $\lambda _\text{max}$ the maximum wavelength defined as $\lambda _\text{max}=2\pi c/\omega _\text{max}$. This is an alternative way of thinking of the frequency limit: if this wavelength is shorter than the average distance between atoms, the very idea of a mechanical wave stops making any sense, so there is a limit. Another interesting fact is that, just like the speed of light determines limits in [[electromagnetic wave|electromagnetic waves]], the speed of sound can be used to determine limits in the mechanical waves. In fact, using the expression for $\omega _\text{max}$ we can see that $\lambda _\text{max}\sim v^{1/3}\sim\text{space between atoms}$.
##### Canonical ensemble
We have now described mechanical oscillations as the action of phonons "moving" through the medium. We can use statistical mechanics to describe the medium as a whole as an [[ensemble]] of phonons. Since the particle number of phonons is not conserved and they are [[mass|massless]], we'll use a [[quantum grand canonical ensemble]] with $z=1$, which functionally reduces to a solvable [[quantum canonical ensemble]]. If $n_{i}$ is the [[occupation number]] of the state with frequency $\omega_{i}$, the total energy is
$$E(\{ n_{i} \})=\sum_{i=1}^{3N} n_{i}\varepsilon_{i}=\sum_{i=1}^{3N} n_{i}\hbar \omega_{i}$$
###### Partition function
The [[partition function]] is
$$Q=\sum_{N=0}^{\infty}Q_{N}=\sum_{\{ n_{i} \}}e^{-\beta E(\{ n_{i} \})}=\prod_{i=1}^{3N} \frac{1}{1-e^{-\beta \hbar \omega_{i}}}$$
using $e^{\sum_{n}n}=\prod_{n}e^{n}$ and the [[Serie geometrica|geometric series]]. Its logarithm is
$$\log Q=-\sum_{i=1}^{3N} \log(1-e^{-\beta \hbar \omega_{i}})$$
###### Average occupation
The average occupation number is
$$\langle n_{i} \rangle =- \frac{1}{\beta }\frac{ \partial  }{ \partial (\hbar \omega) }\log Q=\frac{1}{e^{\beta \hbar \omega}-1}$$
This is the [[Bose-Einstein distribution]]. Evidently, phonons behave like [[boson|bosons]][^3] and a phonon ensemble is a [[Bose gas]].
###### Internal energy
The [[internal energy]] is
$$U=-\frac{ \partial  }{ \partial \beta } \log Q=\sum_{i=1}^{3N} \hbar \omega_{i}\langle n_{i} \rangle =\sum_{i=1}^{3N} \frac{\hbar \omega_{i}}{e^{\beta \hbar \omega_{i}}-1}$$
In the [[Thomas-Fermi approximation]] it becomes
$$U=\frac{3V}{2\pi ^{2}c^{3}}\int_{0}^{\omega _\text{max}}\omega ^{2} \frac{1}{e^{\beta \hbar \omega}-1}d\omega$$
Note that unlike in the vacuum, the energy is capped by the maximum frequency, which is itself capped by the density. This makes sense: denser materials stockpile more energy because there's just more *stuff* in them. The energy density by particle is
$$\frac{U}{N}=\frac{g(k_{B}T)^{4}}{(\hbar \omega _\text{max})^{3}}\int_{0}^{\beta \hbar \omega _\text{max}} \frac{t^{3}}{e^{t}-1}dt$$
Notice how this equation is almost identical to the [[Planck radiation law]] for a [[black body cavity]]. This shouldn't be surprising: both are Bose gases in a finite volume, so it makes sense that their energy density would be described by similar equations. The major difference is that [[photon|photons]] in the cavity could have any frequency, but phonons in a medium have frequencies only up to a maximum.

Unfortunately, we don't really have an analytical solution for this. However, we can nevertheless get a parametric result.
###### Equation of state
We can define the **Debye function** $D(x)$ as
$$D(x)\equiv\frac{3}{x^{3}}\int_{0}^{x} \frac{t^{3}}{e^{t}-1}dt$$
and the **Debye temperature** $T_{D}\equiv \hbar \omega _\text{max}/k_{B}$. With these, we can express the density as
$$\boxed{\frac{U}{N}=3k_{B}TD\left( \frac{T}{T_{D}} \right)}$$
This is the [[equation of state]] for a system of phonons in a medium.

Let's call $\lambda=T/T_{D}$. In the limits of high and low temperatures, the Debye function has asymptotic behavior given by the [[Serie|series]] expansions
$$D(\lambda)=\left\{\begin{align}
&1- \frac{3}{8}\lambda+\ldots& \lambda\ll 1,\ T\to \infty \\
&\frac{\pi^{4}}{5\lambda^{3}}+\ldots& \lambda\gg 1,\ T\to 0
\end{align}\right.$$
The equation of state can be approximated as
$$\frac{U}{N}=\left\{\begin{align}
&3k_{B}T\left( 1- \frac{3}{8}\lambda+\ldots \right)& \lambda\ll 1,\ T\to \infty \\
&3k_{B}T\left( \frac{\pi^{4}}{5\lambda^{3}}+\ldots \right)& \lambda\gg 1,\ T\to 0
\end{align}\right.$$
A basic approximation at high temperatures is therefore
$$U=3Nk_{B}T$$
###### Heat capacity
We can recover [[heat capacity]] as
$$\frac{C_{V}}{Nk_{B}}=\frac{1}{Nk_{B}}\frac{ \partial U }{ \partial T } =3D(\lambda)+3T \frac{ \partial D(\lambda) }{ \partial T }=3\left[ 4D(\lambda)- \frac{3\lambda}{e^{\lambda}-1} \right] $$
At high temperatures, we get the classical [[Dulong-Petit law]]:
$$C_{V}=\frac{ \partial U }{ \partial T } =3Nk_{B}$$
which shows that all crystalline solids more ore less have the same heat capacity at high enough temperatures. What "high enough" means depends on the Debye temperature, which depends on the material. For example, lead has $T_{D}=95\text{ K}$, gold has $T_{D}=215\text{ K}$, copper has $T_{D}=309\text{ K}$ and aluminum has $T_{D}=396\text{ K}$. Most of these are near or below room temperature, which is why it appears to us that all solids have the same 

When plotted numerically, the heat capacity goes something like this:

![[Plot Phonon crystal heat capacity|center]]

When the ratio of temperature and Debye temperature approaches one, heat capacity plateaus at $\sim 3$. This model actually works really well for a large class of solids. However, it only works for solids: if the temperature is so high that the material melts, this model stops working.

[^1]: We are assuming $N$ is even. If $N$ were odd, we'd have $\frac{N}{2}-1$ in each term instead.
[^2]: Actually, there's another, earlier, distribution due to Einstein (who was the first to investigate this model) which claims that all oscillation modes are equally likely. This makes for an easier solution, but the end result is not very accurate at low temperature. The Debye distribution is instead very accurate at these temperatures.
[^3]: In hindsight, they could've never been [[Fermion|fermions]]. Why would mechanical oscillations be constrained by the [[Pauli exclusion principle]]?