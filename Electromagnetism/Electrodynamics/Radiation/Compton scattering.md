---
wiki-publish: true
aliases:
  - Compton edge
  - Compton wavelength
---
**Compton scattering** is a [[particle scattering]] phenomenon between a [[photon]] and an [[electron]] that involves the absorption and re-emission of a photon by the electron, deflecting it and changing its [[frequency]]. It essentially redirects [[electromagnetic radiation]]. It is a higher energy form of [[Thomson scattering]].
### Mechanism
In the language of [[particle]] physics, Compton scattering reads
$$\gamma+ e^{-} \rightarrow \gamma +e^{-}$$
It is an elastic scattering process. Graphically it looks like this:

![[Diagram Compton scattering|center]]

Before the scattering, the photon carries [[relativistic energy]] $E_{0}$ and the electron only has its rest energy. The process can be explained starting from [[four-momentum]] conservation, which is valid in elastic scatterings. Elaboration through relativistic energy yields a final photon energy of
$$E_{\gamma}=\dfrac{1}{\dfrac{1-\cos\theta}{m_{e}c^{2}}+ \dfrac{1}{E_{0}}}$$
Applying [[Planck formula|Planck's formula]] $E_{\gamma}=h\nu=hc/\lambda$ yields
$$\frac{hc}{\lambda}=\dfrac{1}{\dfrac{1-\cos\theta}{m_{e}c^{2}}+ \dfrac{1}{E_{0}}}$$
($\lambda$ is the final [[wavelength]]). Rearranging to extract $\lambda$ and recognizing that $E_{0}=hc/\lambda_{0}$ where $\lambda_{0}$ is the starting wavelength yields
$$\lambda=hc\left( \frac{1-\cos\theta}{m_{e}c^{2}}+ \frac{\lambda_{0}}{hc} \right)=\lambda_{0}+ \frac{h}{m_{e}c}(1-\cos \theta)$$
We define
$$\lambda_{C}=\frac{h}{m_{e}c}$$
which is known as the **[[Compton wavelength]]** (in this case of the electron). Then, the final wavelength depends on the starting one according to
$$\boxed{\lambda=\lambda_{0}+ \lambda_{C}(1-\cos \theta)}$$
The second term is an angular rescaling of the Compton wavelength based on the angle of scattering, meaning that there is a minimum and maximum variation that Compton scattering can do. Specifically:
- If $\theta=0$, the electron continues straight and there is no change ($\cos \theta=1$).
- If $\theta=\pi$, the electron bounces back right where it came from and the change is maximized ($\cos \theta=-1$), being equal to $2\lambda_{C}$.

The Compton wavelength is an interesting quantity energetically speaking. The wavelength variation $\lambda-\lambda_{0}$ is most important when $\lambda_{0}\simeq \lambda_{C}$. The energy of a photon of wavelength $\lambda_{C}$ is
$$E_{C}=h\nu=\frac{hc}{\lambda_{C}}=\frac{hc}{h}m_{e}c=m_{e}c^{2}$$
which is precisely the [[Relativistic energy|rest energy]] of the electron. Evidently, the energy transfer is most efficient when the photon matches the energy of the electron (a [[resonance]] phenomenon).

By using energy conservation, it also follows that the energy transferred to the electron is:
$$E_{e}=E_{\gamma} \dfrac{\dfrac{E_{\gamma}}{m_{e}c^{2}}(1-\cos\theta)}{1+\dfrac{E_{\gamma}}{m_{e}c^{2}}(1-\cos\theta)}$$
which, like the wavelength, varies between 0 and a maximum value when $\theta=\pi$, which is
$$E_{e,\text{max}}=E_{\gamma} \dfrac{\dfrac{2E_{\gamma}}{m_{e}c^{2}}}{1+\dfrac{2E_{\gamma}}{m_{e}c^{2}}}<E_{\gamma}$$
This is known as the **Compton edge** and, interestingly, it's guaranteed to be less than the photon's energy. But it must be so, because this is an elastic scattering event: photons have no [[mass]], so if they were to transfer all their energy they'd just disappear and we'd be talking about the [[photoelectric effect]] instead. We know that the photoelectric effect can't happen in the vacuum, so there's no way Compton scattering can lead to complete energy transfer.

Finally, we know that the [[cross section]] of Compton scattering decreases with energy, meaning lower-energy photons are favored.

:::image
![[Diagram Compton scattering cross section]]
Cross section of Compton scattering. It is highest at low energies and eventually drops down to zero.
:::

Compton scattering cross section is also known to go like $\sim Z$, meaning that if the electron is bound to a [[Atomic nucleus|nucleus]], the larger the more likely Compton scattering is, linearly so to be specific.
### In detectors
Unlike the photoelectric effect, Compton scattering is of limited utility for [[Detector|detectors]]. Since photons aren't detectable by themselves due to being [[Electric charge|electrically neutral]], we need to want to use some other particle (an electron, say) as a proxy for its energy. In principle, since we know the relation between $E_{e}$ and $E_{\gamma}$, we could measure the former and the calculate the latter. But there's two big problems:
1. Unlike the photoelectric effect, which is entirely deterministic, Compton scattering is entirely [[random]]. The scattering angle is unpredictable and since the energy relation is dependent on it, we can't reliably use it. For a single electron, the energy can be anywhere between 0 and $E_{e,\text{max}}$, so we don't get any real information out of it besides a tenous lower bound, since $E_{\gamma}>E_{e,\text{max}}$.
2. Even if we try to measure a large number of photons to get a [[probability distribution]], the photons would have to all be the same energy in order to create electrons with the same energy distributions, which isn't terribly realistic. Still, this is a viable strategy if nothing better is available, as sampling the entire distribution gives us a better estimate of $E_{e,\text{max}}$ and therefore a better lower bound for $E_{\gamma}$.
### Inverse mechanism
It is sometimes possible that the energy exchange takes place in reverse, i.e. that a high-energy electron transfers energy to an impinging photon with less energy. This phenomenon is called **inverse Compton scattering**. It is rare in compact matter since electrons are confined to atoms, but under more extreme conditions, such as the [[accretion disk]] of a [[black hole]], it is possible for a relativistic free electron to impinge on a photon with less energy, thus causing inverse Compton scattering.