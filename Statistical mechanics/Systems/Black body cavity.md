---
aliases:
  - Planck radiation law
---
A **black body cavity** is a hollow [[corpo nero|black body]] with a pinhole dug into the surface. The cavity emits [[radiazione elettromagnetica|electromagnetic radiation]] from within. If the cavity is large enough, the system approximately looses the dependency on boundary conditions. It was the [[physical system]] that spurred the start of quantum mechanics, as classical results differ massively from reality due to the **ultraviolet catastrophe**.
### Quantum description
Since electromagnetic radiation is described by the exchange of [[Photon|photons]], the whole cavity can be described as an [[canonical ensemble]] of them. Since photons are absorbed and emitted, the total number of photons is not conserved. The [[chemical potential]] is zero[^1].

Let's say we have $N$ photons, each with [[wave vector]] $\mathbf{k}$ and polarization $\hat{\varepsilon}$. Each state is $n_{\mathbf{k},\hat{\varepsilon}}=0,1,2,\ldots$. The total [[energy]] is
$$E(\{ n_{\mathbf{k},\hat{\varepsilon}} \})=\sum_{\mathbf{k},\hat{\varepsilon}}\hbar \omega n_{\mathbf{k},\hat{\varepsilon}}\tag{1}$$
where the frequency is $\omega=c\lvert \mathbf{k} \rvert$ using the [[velocità della luce|speed of light]] $c$. The [[partition function]] is
$$Q=\sum_{\{ n_{\mathbf{k},\hat{\varepsilon}} \}}=\exp\left( -\beta \sum_{\mathbf{k},\hat{\varepsilon}}\hbar \omega n_{\mathbf{k},\hat{\varepsilon}} \right)=\prod_{\mathbf{k},\hat{\varepsilon}}\sum_{n=0}^{\infty} (e^{-\beta \hbar \omega})^{n}=\prod_{\mathbf{k},\hat{\varepsilon}} \frac{1}{1-e^{-\beta \hbar \omega}}$$
since we have a [[Serie geometrica|geometric series]]. The logarithm is then
$$\log Q=-\sum_{\mathbf{k},\hat{\varepsilon}}\log(1-e^{-\beta \hbar \omega})=-2\sum_{\mathbf{k}}\log(1-e^{-\beta \hbar \omega})$$
since there are only two possible $\hat{\varepsilon}$ states. The average [[occupation number]] is
$$\langle n_{\mathbf{k}} \rangle =- \frac{1}{\beta}\frac{ \partial  }{ \partial (\hbar \omega) } \log Q=\frac{2}{\beta} \frac{\beta e^{\hbar \omega \beta}}{1-e^{-\beta \hbar \omega}}=\frac{2}{e ^{\beta \hbar \omega}-1}$$
which is the [[Bose-Einstein distribution]], as we should expect from since photons are [[Boson|bosons]]. The [[internal energy]] is
$$U=-\frac{ \partial  }{ \partial \beta } \log Q=\sum_{\mathbf{k}}\hbar \omega \langle n_{\mathbf{k}} \rangle $$
Note that this result is essentially equation $(1)$ but using the [[ensemble average]] instead[^2]. This is expected, as we know that in a canonical ensemble, $\langle E \rangle=U$. The [[pressure]] is
$$P=-\frac{ \partial A }{ \partial V } =\frac{1}{\beta}\frac{ \partial  }{ \partial V } \log Q=\frac{1}{\beta}\frac{ \partial  }{ \partial V } \left( -2\sum_{\mathbf{k}}\log(1-e^{-\beta \hbar c_{2}\pi \lvert \hat{\mathbf{n}} \rvert /V^{1/3}}) \right)=\frac{1}{3V}\sum_{\mathbf{k}}\hbar \omega \langle n_{\mathbf{k}} \rangle $$
From which we can get the [[equation of state]] of a photon gas
$$\boxed{PV=\frac{1}{3}U}$$
We can calculate $U$ more explicitly in the [[Thermodynamic limit]]:
$$U=\sum_{\mathbf{k},\hat{\varepsilon}}\hbar \omega \langle n_{\mathbf{k}} \rangle =\frac{V}{(2\pi)^{3}}2\int_{0}^{\infty}4\pi k^{2} \frac{\hbar ck}{e^{\beta \hbar ck}-1}dk=\frac{2V}{(2\pi)^{3}}4\pi \int_{0}^{\infty} \frac{1}{c} \frac{\omega ^{2}}{c^{2}} \hbar \frac{\omega}{e^{\beta \hbar \omega}-1}d\omega$$
The energy density by volume is
$$\boxed{\frac{U}{V}=\int_{0}^{\infty}u(\omega,T)\ d\omega \quad\text{where}\quad u(\omega,T)=\frac{\hbar}{\pi ^{2}c^{3}} \frac{\omega ^{3}}{e^{\beta \hbar \omega}-1}}$$
This is called the **Planck radiation law**. Ideally, we want to solve the integral above. To that end, let's first solve
$$\begin{align}
\int_{0}^{\infty} \frac{\omega ^{3}}{e^{\beta \omega}-1}d\omega&=\int_{0}^{\infty} \frac{\omega ^{3}e^{-\beta \omega}}{1-e^{-\beta \omega}}d\omega \\
&=\int_{0}^{\infty}\omega ^{3}e^{-\beta \omega}\sum_{n=0}^{\infty}(e^{-\beta \omega})^{n}d\omega \\
(\text{Gamma})\quad&=\sum_{n=1}^{\infty} \int_{0}^{\infty}\omega ^{3}e^{-\beta \omega n}d\omega \\
&=\sum_{n=1}^{\infty} \left( -\frac{ \partial ^{3} }{ \partial (\beta \omega) ^{3}  }  \right)\int_{0}^{\infty}e^{-\beta \omega n}d\omega \\
(n\beta \omega=\xi)\quad&=\sum_{n=1}^{\infty} \left( -\frac{ \partial ^{3} }{ \partial (\beta n) } ^{3} \right)\int_{0}^{\infty} \frac{1}{\beta}e^{-\xi}d\xi \\
&=- \frac{1}{\beta^{4}}\sum_{n=1}^{\infty} \frac{ \partial ^{3} }{ \partial n^{3} } \frac{1}{n} \\
&=\frac{6}{\beta^{4}}\sum_{n=1}^{\infty} \frac{1}{n^{4}}=\frac{\pi^{4}}{90}
\end{align}$$
This integral could have also been solved by noticing that it becomes a [[Gamma function]] in step (Gamma). Using this, we can get the energy density
$$\frac{U}{V}=\frac{\hbar}{\pi ^{2}c^{3}} \frac{1}{(\beta \hbar)^{4}} \frac{6\pi^{4}}{90}=\frac{\pi ^{2}}{15} \frac{(k_{B}T)^{4}}{(\hbar c)^{3}}$$
We can even use this to get the [[heat capacity]]:
$$C_{V}=\frac{1}{V}\frac{ \partial U }{ \partial T } =\frac{4\pi ^{2}}{15} \frac{k_{B}^{4}T^{3}}{(\hbar c)^{3}}$$
and also the [[irradianza|irradiance]] by [[temperature]]:
$$I(T)=\int_{0}^{\infty}I(\omega,T)d\omega$$
The irradiance by frequency is
$$I(\omega,T)=c\int \frac{1}{4\pi}u(\omega,T)\cos \theta \ d\Omega=\frac{c}{4}u(\omega,T) $$
over the [[solid angle]] $\Omega$ because
$$\int \frac{\cos\theta}{4\pi}d\Omega=\int_{0}^{2\pi}d\phi\int_{0}^{\pi/2} \frac{\sin\theta}{4\pi}\cos \theta\ d\theta=\frac{1}{4}$$
As such, we get
$$\boxed{I(T)=\frac{\pi ^{2}k_{B}^{4}}{60\hbar ^{3}c^{2}}T^{4}=\sigma T^{4}}$$
This is known as the [[legge di Stefan-Boltzmann|Stefan law]] for [[irradiazione|irradiation]], where $\sigma$ is the [[Costante di Stefan-Boltzmann|Stefan-Boltzmann constant]].

[1]: This might seem weird as photons are being added and removed all the time. The real reason is that photons have no [[mass]] and only carry [[kinetic energy]], so when they are absorbed, they give away their energy and vanish. As such, the energy increases, but the particles do not (since the photon vanished). Photons really just move energy around and once they deliver their energy, the disappear.
[^2]: However, do be careful of the factor 2 from the sum over polarization states.