---
wiki-publish: true
---
An **ideal crystal** is a solid-state material with a periodic, perfectly geometric, rigid lattice. It is the simplest mathematical description of a [[crystal]], much like how an [[ideal gas]] is the simplest description of a [[gas]]. The [[Hamiltonian]] is
$$H=\underbrace{ \sum_{i} \frac{p_{i}^{2}}{2m_{i}}+ \sum_{j} \frac{p_{j}^{2}}{2m_{j}} }_{ \text{Kinetic terms} }+ \underbrace{ \frac{1}{2}\sum_{j,j'} \frac{Z_{j}Z_{j'}e^{2}}{\lvert R_{j}-R_{j'} \rvert } }_{ \text{Ion-ion interaction} }+ \underbrace{ \frac{1}{2}\sum_{i,i'} \frac{e^{2}}{\lvert r_{i}-r_{i'} \rvert } }_{ \text{Electron-electron interaction} }-\underbrace{ \sum_{i,j} \frac{Z_{j}e^{2}}{\lvert r_{j}-R_{j} \rvert } }_{ \text{Ion-electron interaction} }$$
This is an $N$-body Hamiltonian that's certainly not analytically solvable. It can be solved in an approximate manner by combining two assumptions:
1. **Core and valence electrons**. We split electrons in two categories: core electrons (inner electron shells) and valence electrons (outermost electron shell). Only the valence electrons are significant when it comes to interactions.
2. **Born-Oppenheimer approximation**. The [[Born-Oppenheimer approximation]] is noticing that the [[Nucleo atomico|nuclei]] move at much lower speeds than the electrons, which allows us to state that ions are subject to a [[mean]] [[potential]] and that the electrons see the ions as basically stationary.

Furthermore, we'll use approximate forms for potentials.
### Harmonic potentials
We'll start from the ionic part of the Hamiltonian. We don't actually know what the potential looks like. We know it in principle, as we understand [[Interazione elettromagnetica|electromagnetic interaction]], but finding the *total* potential of this many ions is far beyond the limits of analytical solutions. So, to make our life easier, we'll choose a reasonable shape for them, specifically a *harmonic interaction potential*.
1. We assume that the equilibrium position of each ion correspond to a point $\mathbf{R}$ in the [[Bravais lattice]].
2. We assume that displacements from this position are small compared to the distance between ions.

In other words, we have a perfect periodic shape in which we slot in our ions and assume that any change from this configuration is small. The generic position of the ion will then be given by $\mathbf{r}(\mathbf{R})=\mathbf{R}+\mathbf{u}(\mathbf{R})$, where $\mathbf{u}(\mathbf{R})$ is the displacement from the lattice point. The generic interaction potential between ions $U$ is then $U\equiv U(\mathbf{r})=U(\mathbf{R}+\mathbf{u})$. Here's the mathematical approximation: we take this potential and expand it in a [[Taylor series]] around the lattice point:
$$U(\mathbf{R}+\mathbf{u})=U(\mathbf{R})+(\mathbf{u}\cdot \nabla )U(\mathbf{R})+ \frac{1}{2}(\mathbf{u}\cdot \nabla)^{2}U(\mathbf{R})+ \frac{1}{3!}(\mathbf{u}\cdot \nabla)^{3}U(\mathbf{R})+\ldots$$
If we express $U$ in terms of the individual potential energy $\phi$ we get 
$$\begin{align}
U&=\frac{N}{2}\phi(\mathbf{R})\\
&+ \frac{1}{2}\sum_{\mathbf{R}\mathbf{R}'}(\mathbf{u}(\mathbf{R})-\mathbf{u}(\mathbf{R}'))\cdot \nabla \phi(\mathbf{R}-\mathbf{R}') \\
&+ \frac{1}{4}\sum_{\mathbf{R}\mathbf{R}'}[\mathbf{u}(\mathbf{R})-\mathbf{u}(\mathbf{R})'\cdot \nabla]^{2}\phi(\mathbf{R}-\mathbf{R}') \\
&+O^{3}
\end{align}$$
If we stop at the second order, our potential can now be written as a sum of two parts
$$U=U_\text{equilbrium}+U_\text{harmonic}$$
where the equilibrium term is the first line and the harmonic term is the third one (??? See mid lesson 05/05/2025).
#### The spring model
Since we're using harmonic potentials for the interaction between ions, how do we interpret this? Well, usually harmonic potentials are springs. They have some elastic constant and the strength of the pullback increases quadratically with distance. This justifies a somewhat toyish but otherwise not unreasonable model of claiming that ions are bound to each other by (invisible) *springs*. In other words, a chain of [[Harmonic oscillator|harmonic oscillators]].

Let's start from a 1D crystal, so an (effectively) infinite chain of oscillator ions all bound to their two closest neighbors. The oscillations are longitudinal, that is, on the axis of the springs[^1]. The solution for $u_{n}(t)$ is this context is
$$u_{n}(t)=ue^{i(kan-\omega t)}$$
When substituted in the differential equation we get
$$\begin{align}
-M\omega ^{2}\cancel{ e^{i(kan-\omega t)} }&=-\gamma[2-e^{ika}-e^{ika}][\cancel{ e^{i(kan)-\omega t} }] \\
M\omega ^{2}&=\gamma[2-e^{-ika}-e^{ika}]
\end{align}$$
Extracting $\omega$ gives[^2]
$$\omega(k)=\sqrt{ \frac{2\gamma(1-\cos(ka))}{M} }=2\sqrt{ \frac{\gamma}{M} }\left\lvert  \sin\left( \frac{ka}{2} \right)  \right\rvert $$
This is the **dispersion relation** of the 1D, spring modeled, ideal crystal, which tells us the [[Frequency|angular frequency]] of the [[wave]] that carries a perturbation through the chain of oscillators. With it, it's fair to analyze the speed of the wave itself. Since it's a wave, we need both the phase speed and the group speed.

In the $k\ll \pi/a$ case, the [[wavelength]] of the vibration is much larger than the lattice distance $a$, so [[Atom|atoms]] next to each other essentially move with the same phase. Moreover,
$$\sin \frac{ka}{2}\simeq \frac{ka}{2}\quad\to \quad \omega(k)=2\sqrt{ \frac{\gamma}{M} } \frac{ka}{2}=vk\quad\text{with }v=\sqrt{ \frac{\gamma}{M} }a$$
In this case, $v=\omega/k=\frac{ \partial \omega }{ \partial k }$. The phase and group speeds coincide and neither depends on $k$. This happens when the wave is [[stationary wave|stationary]], so $v$ corresponds to sound speed in the crystal.

[^1]: In 1D it can't be any other way, but it does matter if you interpret this as an approximately 1D object in 3D.

[^2]: Since $e^{ix}+e^{-ix}=2\cos x$ and  $(1-\cos ^{2}x)/2=\sin ^{2}x$.
