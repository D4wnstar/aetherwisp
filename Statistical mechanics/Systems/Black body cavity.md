---
aliases:
  - Planck radiation law
---
A **black body cavity** is a hollow [[corpo nero|black body]] with a pinhole dug into the surface. The cavity emits [[radiazione elettromagnetica|electromagnetic radiation]] from within. If the cavity is large enough, the system approximately looses the dependency on boundary conditions. It was the [[physical system]] that spurred the start of quantum mechanics, as classical results differ massively from reality due to the **ultraviolet catastrophe**.
### Quantum description
Since electromagnetic radiation is the exchange of [[Photon|photons]], the whole cavity can be described as a [[canonical ensemble]]. Specifically, it is a [[Bose gas]] of [[mass|massless]] [[boson|bosons]]. Since photons are absorbed and emitted, the total number of photons is not conserved. The [[chemical potential]] is zero[^1].

As with all photons, their properties are
$$E=\hbar \omega,\qquad \mathbf{p}=\hbar \mathbf{k},\qquad \lvert \mathbf{k} \rvert =\frac{\omega}{c}$$
where $\hbar$ is the [[Costante di Planck|reduced Planck constant]], $\omega$ is the [[angular frequency]], $\mathbf{k}$ is the [[wave vector]] and $c$ is the [[speed of light]]. They also all possess a polarization unit vector $\hat{\varepsilon}$ that is [[Ortogonalità|orthogonal]] to $\mathbf{k}$.
#### Partition function
Each state can be indexed like $n_{\mathbf{k},\hat{\varepsilon}}=0,1,2,\ldots$ and they represent [[normal mode|normal modes]] of oscillation. The particle number is variable, so we can't rely on it like we can with massive particles. The total [[energy]] on the other had is always conserved, so we can use
$$E(\{ n_{\mathbf{k},\hat{\varepsilon}} \})=\sum_{\mathbf{k},\hat{\varepsilon}}\hbar \omega n_{\mathbf{k},\hat{\varepsilon}}\tag{1}$$
We'll use a [[quantum canonical ensemble]]. The [[Partition function|canonical partition function]] is
$$Q_{N}=\sum_{\{ n_{\mathbf{k},\hat{\varepsilon}} \}}\exp\left( -\beta \sum_{\mathbf{k},\hat{\varepsilon}}\hbar \omega n_{\mathbf{k},\hat{\varepsilon}} \right)=\prod_{\mathbf{k},\hat{\varepsilon}}\sum_{n=0}^{\infty} (e^{-\beta \hbar \omega})^{n}=\prod_{\mathbf{k},\hat{\varepsilon}} \frac{1}{1-e^{-\beta \hbar \omega}}$$
since $e^{\sum n}=\prod_{n}e^{n}$ and using the [[Serie geometrica|geometric series]]. See [[Ideal gas#In the quantum grand canonical ensemble]] for steps on how to invert sum and product. The logarithm is then
$$\log Q_{N}=-\sum_{\mathbf{k},\hat{\varepsilon}}\log(1-e^{-\beta \hbar \omega})=-2\sum_{\mathbf{k}}\log(1-e^{-\beta \hbar \omega})$$
since there are only two possible $\hat{\varepsilon}$ states[^2].
#### Occupation numbers
Now that we know $Q_{N}$, we can calculate everything else. The average [[occupation number]] is
$$\langle n_{\mathbf{k}} \rangle =- \frac{1}{\beta}\frac{ \partial  }{ \partial (\hbar \omega) } \log Q_{N}=\frac{2}{\beta} \frac{\beta e^{\hbar \omega \beta}}{1-e^{-\beta \hbar \omega}}=\frac{2}{e ^{\beta \hbar \omega}-1}$$
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
It differs from a "normal" (i.e. massive) ideal gas by a factor of $2$.
### Internal energy
We can calculate $U$ more explicitly in the [[Thomas-Fermi approximation]]:
$$U=\sum_{\mathbf{k},\hat{\varepsilon}}\hbar \omega \langle n_{\mathbf{k}} \rangle \simeq 2\int_{0}^{\infty}\hbar \omega g(k)\langle n_{k} \rangle dk=\ldots$$
Again, don't miss the $2$ from the polarization. The state density is given by
$$G(k)=\frac{\frac{4}{3}\pi k^{3}}{\left( \frac{2\pi}{L} \right)^{3}}=\frac{k^{3}}{6\pi ^{2}}V,\qquad g(k)=\frac{ \partial G }{ \partial k } =\frac{k^{2}}{2\pi ^{2}}V$$
Substituting yields
$$\ldots= 2\hbar \int_{0}^{\infty} \frac{\omega k^{2}}{2\pi ^{2}}V \frac{1}{e^{\beta \hbar ck}-1}dk=\frac{\hbar V}{\pi ^{2}} \int_{0}^{\infty} \frac{\omega ^{2}}{c^{2}} \frac{\omega}{e^{\beta \hbar \omega}-1} \frac{d\omega}{c}$$
The energy density by volume is
$$\boxed{\frac{U}{V}=\int_{0}^{\infty}u(\omega,T)\ d\omega \quad\text{where}\quad u(\omega,T)=\frac{\hbar}{\pi ^{2}c^{3}} \frac{\omega ^{3}}{e^{\beta \hbar \omega}-1}}$$
This is called the [[Planck radiation law]]. Ideally, we want to solve the integral above. To that end, let's momentarily omit $\hbar$ for brevity and then do
$$\begin{align}
\int_{0}^{\infty} \frac{\omega ^{3}}{e^{\beta \omega}-1}d\omega&=\int_{0}^{\infty} \frac{\omega ^{3}e^{-\beta \omega}}{1-e^{-\beta \omega}}d\omega \\
\text{(geometric series)}&=\int_{0}^{\infty}\omega ^{3}e^{-\beta \omega}\sum_{n=0}^{\infty}(e^{-\beta \omega})^{n}d\omega \\
(\text{Gamma})&=\sum_{n=1}^{\infty} \int_{0}^{\infty}\omega ^{3}e^{-\beta \omega n}d\omega \\
&=\sum_{n=1}^{\infty} \left( -\frac{ \partial ^{3} }{ \partial (\beta n) ^{3}  }  \right)\int_{0}^{\infty}e^{-\beta \omega n}d\omega \\
(n\beta \omega=\xi)&=\sum_{n=1}^{\infty} \left( -\frac{ \partial ^{3} }{ \partial (\beta n) } ^{3} \right)\frac{1}{\beta}\underbrace{ \int_{0}^{\infty} e^{-\xi}d\xi }_{ 1 } \\
&=- \frac{1}{\beta^{4}}\sum_{n=1}^{\infty} \frac{ \partial ^{3} }{ \partial n^{3} } \frac{1}{n} \\
&=\frac{6}{\beta^{4}}\sum_{n=1}^{\infty} \frac{1}{n^{4}} \\
&=\frac{6}{\beta^{4}}\zeta(4)=\frac{6}{\beta^{4}}\frac{\pi^{4}}{90}
\end{align}$$
where we used the [[Riemann Zeta function]]. This integral could have also been solved by noticing that it becomes a [[Gamma function]] in step (Gamma). Using this, we can get the energy density
$$\boxed{\frac{U}{V}=\frac{\hbar}{\pi ^{2}c^{3}} \frac{1}{(\beta \hbar)^{4}} \frac{6\pi^{4}}{90}=\frac{\pi ^{2}}{15} \frac{(k_{B}T)^{4}}{(\hbar c)^{3}}}$$
### Heat capacity
We can even use this to get the [[heat capacity]]:
$$C_{V}=\frac{1}{V}\frac{ \partial U }{ \partial T } =\frac{4\pi ^{2}}{15} \frac{k_{B}^{4}T^{3}}{(\hbar c)^{3}}$$
### Irradiance
Also the [[irradianza|irradiance]] by [[temperature]]:
$$I(T)=\int_{0}^{\infty}I(\omega,T)d\omega$$
The irradiance by frequency is
$$I(\omega,T)=c\int \frac{1}{4\pi}u(\omega,T)\cos \theta \ d\Omega=\frac{c}{4}u(\omega,T) $$
over the [[solid angle]] $\Omega$ because
$$\int \frac{\cos\theta}{4\pi}d\Omega=\int_{0}^{2\pi}d\phi\int_{0}^{\pi/2} \frac{\sin\theta}{4\pi}\cos \theta\ d\theta=\frac{1}{4}$$
As such, we get
$$\boxed{I(T)=\frac{\pi ^{2}k_{B}^{4}}{60\hbar ^{3}c^{2}}T^{4}=\sigma T^{4}}$$
This is known as the [[legge di Stefan-Boltzmann|Stefan law]] for [[irradiazione|irradiation]], where $\sigma$ is the [[Costante di Stefan-Boltzmann|Stefan-Boltzmann constant]].

[1]: This might seem weird as photons are being added and removed all the time. The real reason is that photons have no [[mass]] and only carry [[kinetic energy]], so when they are absorbed, they give away their energy and vanish. As such, the energy increases, but the particles do not (since the photon vanished). Photons really just move energy around and once they deliver their energy, the disappear. In fact, all ensembles of massless particles have zero chemical potential.
[^2]: If the photon had more than two polarizations, the factor would be different. However, all experimental tests verify the final result that we get using two of them. This is one way of proving that a photon can only have two polarizations. (Consider that at the time this derivation was first made, the number of photon polarizations was still very much debated.)
[^3]: It's like taking the average of both sides. However, do be careful of the factor 2 from the sum over polarization states.