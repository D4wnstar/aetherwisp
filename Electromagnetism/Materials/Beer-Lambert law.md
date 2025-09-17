---
wiki-publish: true
aliases:
  - absorption coefficient
---
The **Beer-Lambert law** or **Beer-Bouguer-Lambert extinction law** describes the attenuation of a beam of light as it passes through matter. More accurately, it describes the behavior of the [[irradiance]] of an [[electromagnetic wave]] in terms of distance traveled. It is a simple exponential decay of the form
$$I=I_{0}e^{-\mu x}$$
where $I_{0}$ is the intensity of the initial beam, $\mu$ is the **absorption coefficient**, and $x$ is the distance traveled within the material. $\mu$ is a measure of how strongly absorbent a material is with respect to light.
### In particle physics
The Beer-Lambert law has applications in particle physics too. Naturally, it's a good description of the attenuation of [[Photon|photons]] in matter, but it can also be useful for very low [[mass]] [[particle|particles]] in general.

Consider a beam of light particles passing through a layer of matter. Most importantly, it is assumed these particles are removed from the beam on any interaction, which means that the number of interactions is equal to the number of particles removed from the beam. For each infinitesimal thickness $dx$ of the material, the number of particles that interact (and thus vanish) is proportional to the number of incident particles at that depth:
$$dN=-N(x)\mu dx$$
where $\mu$ is called the **absorption coefficient**. Integrating gives
$$N(x)=N(0)e^{-\mu x}$$
which is the Beer-Lambert law for particle number. If you take irradiance to be directly proportional to the number of particles at a given depth, you go back to the macroscopic form of the law. We can express it in a slightly different manner as
$$N(x)=N(0)e^{-x/\lambda}$$
where the only thing we did was define  $\lambda=1/\mu$. It is a unit of distance, specifically the distance at which the particle number is reduced by $1/e$. It is called the **[[mean free path]]**. In this context we can interpret $\mu$ and $\lambda$ is more interesting ways. The absorption coefficient is the likelihood per unit length that a particle will interact. Meanwhile, the mean free path is the [[mean]] distance a particle will travel before interacting.

I explicitly avoided using the term "[[probability]]" when discussing $\mu$ because it's not quite a mathematical probability density. Nevertheless, it does indirectly express the likelihood of an interaction. This might remind you of another quantity that works the same way: [[cross section]]. In fact, the two are related by $\mu=n\sigma$, where $n$ is the volume density of [[Cross section|scattering centers]] in the target and $\sigma$ is the geometric cross section. In this case, the law reads
$$N(x)=N(0)e^{-n\sigma x}$$
