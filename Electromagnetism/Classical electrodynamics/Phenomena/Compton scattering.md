---
wiki-publish: true
aliases:
  - Compton edge
  - Compton wavelength
---
**Compton scattering** is a [[particle scattering]] phenomenon between a [[photon]] and an [[electron]] that involves the absorption and re-emission of a photon by the atomic electron, deflecting it and changing its [[frequency]]. It is a higher energy form of [[Thomson scattering]].
### Mechanism
The process can be written schematically as
$$\gamma e^{-} \rightarrow \gamma e^{-}$$
and graphically it looks like the following figure:

![[Schema Diffusione Compton|center]]

For photon energies much greater than the [[binding energy]] of the electron, the electron can be considered free and interact with the photon elastically, where the electron absorbs part of the photon's energy and varies its frequency. It is found that
$$\Delta \lambda=\lambda-\lambda_{0}=\frac{h}{m_{e}c}(1-\cos\theta)=\lambda_{C}(1-\cos\theta)$$
where $\lambda_{0}$ is the original, pre-scattering wavelength, $\lambda$ is the new one post-scattering and $\lambda_{C}$ is the **Compton wavelength** of the electron. The greater the scattering angle $\theta$, the greater the energy transferred.

> [!info] Result
> The frequency change in the photon is greater the closer the frequency of the photon is to the Compton wavelength $\lambda_{C}$ of the electron. This happens when the energy of the photon is $E_{\gamma}=h\nu\simeq hc/\lambda_{C}=m_{e}c^{2}=0.51$ MeV. For much larger values, the frequency change is substantially zero.

Two interesting cases are distinguished:
- $\theta=0$: we have $\Delta \lambda=0$, i.e. the electron has not ceded energy.
- $\theta=\pi$: there is the maximum transfer of energy.

It follows that the energy transferred to the electron in the collision is:
$$E_{e}=E_{\gamma} \frac{\frac{E_{\gamma}}{m_{e}c^{2}}(1-\cos\theta)}{1+\frac{E_{\gamma}}{m_{e}c^{2}}(1-\cos\theta)}$$
which varies between 0 and a maximum value when $\theta=\pi$, which is
$$E_{e,max}=E_{\gamma} \frac{\frac{2E_{\gamma}}{m_{e}c^{2}}}{1+\frac{2E_{\gamma}}{m_{e}c^{2}}}<E_{\gamma}$$
called the **Compton edge**. The fact that the energy absorbed must be less than the energy of the photon differentiates Compton scattering from the [[photoelectric effect]]. In fact, it cannot possibly be greater, as it would violate the conservation of [[invariant mass]].

Unfortunately, the scattering angle cannot be predicted; as far as we know, it is entirely random. Consequently, the energy of the scattered electron will also be random, within a known interval $0<E_{e}<E_{e,max}<E_{\gamma}$. From an experimental point of view, this means that Compton scattering can at best give a lower limit to the energy of the incident photon, but not an exact value. The best that can be done is to measure the result of a monochromatic photon beam and obtain a good statistic that gives us the Compton edge and from there have more accurate estimates.

![[Schema Fronte Compton|90%|center]]
### Inverse mechanism
It is sometimes possible that the energy exchange takes place in reverse, i.e. that a high-energy electron transfers energy to an impinging photon with less energy. This phenomenon is called **inverse Compton scattering**. It is rare in compact matter since electrons are confined to atoms, but under more extreme conditions, such as the [[accretion disk]] of a [[black hole]], it is possible for a relativistic free electron to impinge on a photon with less energy, thus causing inverse Compton scattering.
### Derivation
The system begins with a photon carrying energy $E_{0}$ and a still electron with no [[kinetic energy]]. Since the photon is massless, it only has kinetic energy. [[Relativistic energy]] $E^{2}-p^{2}c^{2}=m^{2}c^{4}$ must be conserved, as is [[Linear momentum|momentum]]. The latter is:
$$p_{e}\sin \phi=p_{\gamma}\sin \theta y\quad\to \quad \sin \phi= \frac{E_{\gamma}}{p_{e}c}\sin \theta$$
and the former is:
$$\frac{E_{0}}{c}=p_{\gamma}\cos \theta+p_{e}\cos \phi=\frac{E_{\gamma}}{c}\cos \theta+p_{e}\sqrt{ 1- \left( \frac{E_{\gamma}}{p_{\gamma }c}\sin \theta \right)^{2} }$$
$$p_{e}^{2}c^{2}=(E_{0}-E_{\gamma}\cos \theta )^{2}+E_{\gamma}^{2}\sin ^{2}\theta=E_{0}-2E_{0}E_{\gamma}\cos \theta+E_{\gamma}^{2}$$
$$E_{0}+mc^{2}=E_{\gamma}+E_{e}=E_{\gamma}+\sqrt{ m^{2}c^{4}+E_{0}^{2}-2E_{0}E_{\gamma}\cos \theta+E_{\gamma}^{2} }$$
Extracting the energy of the photon we find
$$E_{\gamma}=\frac{1}{\frac{1-\cos\theta}{mc^{2}}+ \frac{1}{E_{0}}}$$
and by applying [[Formula di Planck|Planck's formula]] $E_{\gamma}=h\nu=hc/\lambda$ (since the [[wavelength]] is $\lambda=c/\nu$) we get
$$\frac{hc}{\lambda}=\frac{1}{\frac{1-\cos\theta}{mc^{2}}+ \frac{1}{E_{0}}}$$
where we also found the initial, pre-scattering wavelength $\lambda_{0}=E_{0}/hc$ with the same formula. With some rearrangement we can extract the wavelength
$$\lambda=hc\left( \frac{1-\cos\theta}{mc^{2}}+ \frac{\lambda_{0}}{hc} \right)$$
If we extract $h/mc$ and call it $\lambda_{C}$ we can further simplify to:
$$\boxed{\lambda=\lambda_{0}+ \lambda_{C}(1-\cos \theta)}$$
This is the wavelength of the photon *after* the scattering, and $\lambda_{C}$ is known as the **Compton frequency** of the electron, which is the change in frequency that occurs during a scattering event at an angle $\theta$.