---
wiki-publish: true
aliases:
  - ultraviolet catastrophe
  - Raileigh-Jeans law
  - Planck radiation law
---
A **black body** is an idealized body that absorbs all incident [[radiation]]. It is a good approximation for many bodies that only (or mostly) exhibit thermal radiation, such as [[stella|stars]] and the human body.

A hollow spherical object with the inner surface painted black and a pinhole dug into it is an accurate real world representation of a black body. The cavity emits [[Electromagnetic radiation]] from the pinhole due to thermal excitation. If the cavity is large enough, the system approximately looses the dependency on boundary conditions.

It was the [[physical system]] that spurred the start of quantum mechanics, as the classical result for the emission spectrum differs massively from reality in the higher frequencies, such as ultraviolet: this discrepancy has been called the **ultraviolet catastrophe**.
### Classical description
Let's assume our body is made up of many little [[Electric dipole|electric dipoles]] (imagine [[atom|atoms]] moving around and reorienting). These dipoles are organized in such a manner as to possess a translational symmetry, which allows us to use periodic boundary conditions. Namely, if we take a cubic box of side $L$ as our "periodicity cell" (the single volume element that gets periodically repeated), our [[wavenumber]] will look like
$$k_{i}=\frac{\pi n_{i}}{L}$$
where $i=x,y,z$ and $n\in \mathbb{N}$. This comes from the [[harmonic oscillator]]. Mind you, this is *not* quantization: we have not quantized fields, matter, light or anything else. The number of possible oscillation modes can be calculated in the space of wavenumbers. Let's consider an infinitesimally thick (thickness $dk$) spherical shell in this space, and let's cut out only the octant where all components $k_{x},k_{y}$ and $k_{z}$ are positive.

![[Diagram Black body wavenumber shell]]


Remember that the modes are discrete, as they depend on a natural number $n$, so the density of oscillation modes in this infinitesimal "volume" (which is more of a 3D grid of points due to discreteness) is given by
$$\rho_{k}^{dK}=\frac{N_{k}}{V}=\frac{1}{8}4\pi k^{2}dk\ \underbrace{ \left( \frac{\pi}{L} \right)^{-3} }_{ \text{"volume"} }\ \underbrace{ 2 }_{ \text{polarizations} } \frac{1}{V}=\frac{k^{2}}{\pi ^{2}}dk$$
From here we can obtain the density of modes as a function of the [[frequency]] $\nu$ remembering that
$$k=\frac{2\pi}{\lambda}=\frac{2\pi \nu}{c}\quad\Rightarrow \quad dk=\frac{2\pi}{c}d\nu \quad\Rightarrow \quad d\nu=\frac{4\pi ^{2}\nu ^{2}}{\pi ^{2}c^{2}} \frac{2\pi}{c}d\nu=\frac{8\pi \nu ^{2}}{c^{3}}$$
The energy density will thus be
$$u(\nu) \bar{\varepsilon}=\frac{8\pi \nu ^{2}}{c^{3}}\bar{\varepsilon}\quad\text{where}\quad \bar{\varepsilon}=\frac{\int_{0}^{\infty}\varepsilon e^{-\beta \varepsilon}d\varepsilon}{\int_{0}^{\infty}e^{-\beta \varepsilon}d\varepsilon}=\frac{1}{\beta}$$
The relation
$$\boxed{\rho(\nu)=\frac{8\pi \nu ^{2}}{\beta c^{3}}}$$
is known as the **Rayleigh-Jeans law**. It is the classical description of the emission of a black body, and unfortunately it fails miserably as soon as you try to apply it: being a quadratic law in $\nu$, it just keeps getting higher and higher as the frequencies climb up. In theory, extremely high frequencies like gamma rays would have to carry near infinite energy! This is quite obviously nonsensical, but the solutions are much less evident. In fact, they require claiming something almost just as nonsensical: that energy is quantized.
### Quantum ensemble
To fix the Rayleigh-Jeans law, we must shed classical descriptions and move on to a fully quantized world, where radiation is not just a [[Wave]], but also a [[particle]], namely a [[photon]]. Since electromagnetic radiation is the exchange of photons, the whole cavity can be described as an [[ensemble]] of them. Specifically, it is a [[Bose gas]] of [[mass|massless]] [[boson|bosons]]. Since photons are absorbed and emitted, the total number of photons $N$ is not conserved. As such, we'll use a [[quantum grand canonical ensemble]]. The [[chemical potential]] is therefore zero[^1], so the [[fugacity]] is $z=1$.

As with all photons, their properties are
$$E=\hbar \omega,\qquad \mathbf{p}=\hbar \mathbf{k},\qquad \lvert \mathbf{k} \rvert =\frac{\omega}{c}$$
where $\hbar$ is the [[Planck constant|reduced Planck constant]], $\omega$ is the [[angular frequency]], $\mathbf{k}$ is the [[wave vector]] and $c$ is the [[Speed of light]]. They also all possess a polarization unit vector $\hat{\varepsilon}$ that is [[Orthogonality|orthogonal]] to $\mathbf{k}$.
#### Partition function
Each state can be indexed like $n_{\mathbf{k},\hat{\varepsilon}}=0,1,2,\ldots$ and they represent [[normal mode|normal modes]] of oscillation. The particle number is variable, so we can't rely on it like we can with massive particles. The total [[energy]] on the other had is always conserved, so we can use
$$E(\{ n_{\mathbf{k},\hat{\varepsilon}} \})=\sum_{\mathbf{k},\hat{\varepsilon}}\hbar \omega n_{\mathbf{k},\hat{\varepsilon}}\tag{1}$$
Since $z=1$, the [[Partition function|grand canonical partition function]] reduces itself to just the [[Partition function|canonical partition function]], except with a solvable sum since the constraint $\sum_{i}n_{i}=N$ is lifted:
$$\mathcal{Z}(z=1)=\sum_{N=0}^{\infty} Q_{N}=\sum_{N=0}^{\infty}\sum_{\substack{\{ n_{\mathbf{k},\hat{\varepsilon}} \} \\ \sum_{i}n_{i}=N}}e^{-\beta E(\{ n_{\mathbf{k},\hat{\varepsilon}} \})}=\sum_{\{ n_{\mathbf{k},\hat{\varepsilon}} \}}e^{-\beta E(\{ n_{\mathbf{k},\hat{\varepsilon}} \})}$$
This is solved as
$$\sum_{\{ n_{\mathbf{k},\hat{\varepsilon}} \}}e^{-\beta \sum_{\mathbf{k},\hat{\varepsilon}}\hbar \omega n_{\mathbf{k},\hat{\varepsilon}} }=\prod_{\mathbf{k},\hat{\varepsilon}}\sum_{n=0}^{\infty} (e^{-\beta \hbar \omega})^{n}=\prod_{\mathbf{k},\hat{\varepsilon}} \frac{1}{1-e^{-\beta \hbar \omega}}$$
since $e^{\sum n}=\prod_{n}e^{n}$ and using the [[Serie geometrica|geometric series]]. See [[Ideal gas#In the quantum grand canonical ensemble]] for steps on how to invert sum and product. The logarithm is then
$$\log Q_{N}=-\sum_{\mathbf{k},\hat{\varepsilon}}\log(1-e^{-\beta \hbar \omega})=-2\sum_{\mathbf{k}}\log(1-e^{-\beta \hbar \omega})$$
since there are only two possible $\hat{\varepsilon}$ states[^2].
#### Occupation numbers
Now that we know $Q_{N}$, we can calculate everything else. The average [[occupation number]] for a given $\mathbf{k}$ is
$$\langle n_{\mathbf{k}} \rangle =- \frac{1}{\beta}\frac{ \partial  }{ \partial (\hbar \omega) } \log Q_{N}=\frac{2}{\beta} \frac{\beta e^{-\hbar \omega \beta}}{1-e^{-\beta \hbar \omega}}=\frac{2}{e ^{\beta \hbar \omega}-1}$$
which is a [[Bose-Einstein distribution]] multiplied by the polarization factor, as we should expect.
### Internal energy
The [[internal energy]] is
$$U=-\frac{ \partial  }{ \partial \beta } \log Q_{N}=\sum_{\mathbf{k}}\hbar \omega \langle n_{\mathbf{k}} \rangle $$
Note that this result is essentially equation $(1)$ but using the [[ensemble average]] instead[^3]. This is expected, as we know that in a canonical ensemble, $\langle E \rangle=U$. However, this sum can't be solved as is. 
### Pressure
The [[pressure]] is from the [[Maxwell relations]] on [[Helmholtz free energy]]:
$$P=-\frac{ \partial A }{ \partial V } =\frac{1}{\beta}\frac{ \partial  }{ \partial V } \log Q_{N}=\frac{1}{\beta}\frac{ \partial  }{ \partial V } \left( -2\sum_{\mathbf{k}}\log(1-e^{-\beta \hbar c\ 2\pi \lvert \hat{\mathbf{n}} \rvert /V^{1/3}}) \right)=\frac{1}{3V}\sum_{\mathbf{k}}\hbar \omega \langle n_{\mathbf{k}} \rangle $$
where we used $\omega=c\lvert \mathbf{k} \rvert$ and $\lvert \mathbf{k} \rvert=\frac{2\pi}{L}\lvert \mathbf{n} \rvert=\frac{2\pi}{V^{1/3}}\lvert \mathbf{n} \rvert$ since quantum states of an ideal gas can be counted directly from phase space in a volume $V=L^{3}$ (see start of [[Thomas-Fermi approximation]]). Noticing the internal energy, we can state the [[equation of state]] of a photon gas
$$\boxed{PV=\frac{1}{3}U}$$
It differs from a "normal" (i.e. massive) ideal gas by a factor of $2$. However, this relation can be found to also apply to massive particles *if* they move at speeds close to the speed of light. Clearly, relativity plays a role in the equation of state[^4].
### Internal energy
We can calculate $U$ more explicitly in the [[Thomas-Fermi approximation]]:
$$U=\sum_{\mathbf{k},\hat{\varepsilon}}\hbar \omega \langle n_{\mathbf{k}} \rangle \simeq 2\int_{0}^{\infty}\hbar \omega g(k)\langle n_{k} \rangle dk=\ldots$$
Again, don't miss the $2$ from the polarization. The state density is given by
$$G(k)=\frac{\frac{4}{3}\pi k^{3}}{\left( \frac{2\pi}{L} \right)^{3}}=\frac{k^{3}}{6\pi ^{2}}V,\qquad g(k)=\frac{ \partial G }{ \partial k } =\frac{k^{2}}{2\pi ^{2}}V$$
Substituting yields
$$\ldots= 2\hbar \int_{0}^{\infty} \frac{\omega k^{2}}{2\pi ^{2}}V \frac{1}{e^{\beta \hbar \omega}-1}dk=\frac{\hbar V}{\pi ^{2}} \int_{0}^{\infty} \frac{\omega ^{2}}{c^{2}} \frac{\omega}{e^{\beta \hbar \omega}-1} \frac{d\omega}{c}$$
The energy density by volume is
$$\frac{U}{V}=\int_{0}^{\infty}u(\omega,T)\ d\omega \quad\text{where}\quad \boxed{u(\omega,T)=\frac{\hbar}{\pi ^{2}c^{3}} \frac{\omega ^{3}}{e^{\beta \hbar \omega}-1}}$$
This is called the **Planck radiation law**.

![[Black_body.svg]]

Ideally, we want to solve the integral above. To that end, let's momentarily omit $\hbar$ for brevity and then do
$$\begin{align}
\int_{0}^{\infty} \frac{\omega ^{3}}{e^{\beta \omega}-1}d\omega&=\int_{0}^{\infty} \frac{\omega ^{3}e^{-\beta \omega}}{1-e^{-\beta \omega}}d\omega \\
\text{(geometric series)}&=\int_{0}^{\infty}\omega ^{3}e^{-\beta \omega}\sum_{n=0}^{\infty}(e^{-\beta \omega})^{n}d\omega \\
(\text{Gamma})&=\sum_{n=1}^{\infty} \int_{0}^{\infty}\omega ^{3}e^{-\beta \omega n}d\omega \\
&=\sum_{n=1}^{\infty} \left( -\frac{ \partial ^{3} }{ \partial (\beta n) ^{3}  }  \right)\int_{0}^{\infty}e^{-\beta \omega n}d\omega \\
(n\beta \omega=\xi)&=\sum_{n=1}^{\infty} \left( -\frac{ \partial ^{3} }{ \partial (\beta n)^{3} }  \right)\frac{1}{\beta n}\underbrace{ \int_{0}^{\infty} e^{-\xi}d\xi }_{ 1 } \\
&=- \frac{1}{\beta^{4}}\sum_{n=1}^{\infty} \frac{ \partial ^{3} }{ \partial n^{3} } \frac{1}{n} \\
&=\frac{6}{\beta^{4}}\sum_{n=1}^{\infty} \frac{1}{n^{4}} \\
&=\frac{6}{\beta^{4}}\zeta(4)=\frac{6}{\beta^{4}}\frac{\pi^{4}}{90}
\end{align}$$
where we used the [[Riemann Zeta function]]. This integral could have also been solved by noticing that it becomes a [[Gamma function]] in step (Gamma). Using this, we can get the energy density
$$\boxed{\frac{U}{V}=\frac{\hbar}{\pi ^{2}c^{3}} \frac{1}{(\beta \hbar)^{4}} \frac{6\pi^{4}}{90}=\frac{\pi ^{2}}{15} \frac{(k_{B}T)^{4}}{(\hbar c)^{3}}}$$
### Heat capacity
We can use this to get the [[heat capacity]]:
$$C_{V}=\frac{1}{V}\frac{ \partial U }{ \partial T } =\frac{4\pi ^{2}}{15} \frac{k_{B}^{4}T^{3}}{(\hbar c)^{3}}$$
### Irradiance
The [[irradianza|irradiance]] by [[temperature]] can be expressed in terms of the irradiance by frequency for all frequencies:
$$I(T)=\int_{0}^{\infty}I(\omega,T)d\omega$$
Then the irradiance by frequency is the energy emitted over a [[solid angle]] $\Omega$:
$$I(\omega,T)=c\int \frac{1}{4\pi}u(\omega,T)\cos \theta \ d\Omega$$
where $u$ is the energy density by frequency. The appearance of light speed can be see from dimensional considerations: the units of $u$ are
$$[u]=\frac{\text{Energy}}{\text{Volume}\times\text{Frequency}}$$
and those of the irradiance are
$$[I]=\frac{\text{Energy}}{\text{Area}}=\frac{\text{Energy}}{\text{Volume}\times\text{Frequency}}\times \frac{\text{Length}}{\text{Time}}$$
We can see that the irradiance is an energy density multiplied by a velocity. Since photons move at light speed, the velocity must be the speed of light.

The solid angle we integrate over is not a full sphere, but rather just one hemisphere. This is because the emission is from a pinhole on the surface of the black body. The surface is massive compared to the pinhole, so we can consider it locally flat. Thus, half of space is covered by the black body itself and radiation is not propagated in that direction.

![[Schema Black body pinhole|center]]

$u$ is not dependent on any angle, so it comes out. We are left with
$$\int \frac{\cos\theta}{4\pi}d\Omega=\int_{0}^{2\pi}d\phi\int_{0}^{\pi/2} \frac{\sin\theta}{4\pi}\cos \theta\ d\theta=\frac{1}{4}$$
As such, we get
$$I(T)=\frac{c}{4}\int_{0}^{\infty}u(\omega,T)d\omega$$
We solved this integral before, so our final result is
$$\boxed{I(T)=\frac{\pi ^{2}k_{B}^{4}}{60\hbar ^{3}c^{2}}T^{4}=\sigma T^{4}}$$
This is known as the [[Stefan-Boltzmann law]] for [[irradiazione|irradiation]], where $\sigma$ is the [[Stefan-Boltzmann constant|Stefan-Boltzmann constant]].

[^1]: This might seem weird as photons are being added and removed all the time. The real reason is that photons have no [[mass]] and only carry [[kinetic energy]], so when they are absorbed, they give away their energy and vanish. As such, the energy increases, but the particles do not (since the photon vanished). Photons really just move energy around and once they deliver their energy, the disappear. In fact, all ensembles of massless particles have zero chemical potential.
[^2]: If the photon had more than two polarizations, the factor would be different. However, all experimental tests point to there being only two. This is one way of proving theoretically that a photon can only have two polarizations. (Consider that at the time this derivation was first made, the number of photon polarizations was still a matter of debate.)
[^3]: It's like taking the average of both sides. However, do be careful of the factor 2 from the sum over polarization states.
[^4]: This is due to the energy dispersion relation: massive non-relativistic particles possess kinetic energy $E=p^{2}/2m$, so $\propto p^{2}$, but relativistic particles behave like $E=cp$, so $\propto p$. This drops the $2/3$ to a $1/3$. More generally, if $E\propto p^{s}$, then $PV=(s/3)U$.
