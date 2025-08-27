A [[point mass]] of [[mass]] $m$ typically has an easily defined [[kinetic energy]] of $T=\frac{1}{2}mv^{2}$. In relativity, however, things get more complicated. This article is a derivation of the *relativistic* kinetic energy of a point mass. Spoilers: the end result will be
$$T=\underbrace{ \frac{mc^{2}}{\sqrt{ 1- v^{2}/c^{2} }} }_{ \text{Total energy} }-\underbrace{ mc^{2} }_{ \text{Rest energy} }$$
As the test bench for this derivation, we'll use the annihilation of an [[electron]] $e^{-}$ and its antiparticle the positron $e^{+}$[^1]. This allows us to illustrate conservation of [[energy]]. We'll start with a [[frame of reference]] in which the total [[Linear momentum|momentum]] of the particles is zero: $\mathbf{p}_{T}=0$. The electron-positron pair is "at rest". This implies that $\mathbf{p}_{e^{-}}=-\mathbf{p}_{e^{+}}$. The annihilation of an electron-positron pair creates [[photon|photons]], typically two, and since the momentum is also conserved, the total momentum of the photons must itself be zero, so $\mathbf{p}_{1}=-\mathbf{p}_{2}$. Thanks to de Broglie, we know that the momentum of a massless [[Particle|particle]] is related to its oscillation [[frequency]] $\nu$ by his [[Formula di de Broglie|formula]] $p=2\pi \hbar \nu/c$. So,
$$\lvert \mathbf{p}_{1} \rvert =\frac{E_{1}^{0}}{c}=\frac{2\pi \hbar \nu_{1}}{c},\qquad \lvert \mathbf{p}_{2} \rvert =\frac{E_{2}^{0}}{c}=\frac{2\pi \hbar \nu_{2}}{c}$$
But since the momenta need to be equal and opposite, the frequencies must themselves be equal: $\nu_{1}=\nu_{2}=\nu_{0}$. This gives a total final energy of $E_{1}^{0}+E_{2}^{0}=2\pi \hbar (2\nu_{0})=2E_{0}$. Energy is, of course, conserved, so this must have been the energy at the start too, before the annihilation. To go back to the energies of the electron and positron, we need to be careful about frames of reference.

In particle physics, it's usual to employ two standardized frames: the lab frame and the center of mass frame. The lab frame is the frame attached to the laboratory in which the particles move. It's a "static" frame, at least compared to the people taking the measurements. The center of mass frame is the one we used before, where $\mathbf{p}_{T}=0$ and the system of particle as a whole is at rest. This is essentially just designed to simplify the math. However, the values we actually care about are usually in the lab frame, since that's the one we perceive. We need to find a conversion between center of mass and lab frames.

Firstly, when observing from the lab, we are subject to the relativistic [[Doppler effect]]. The photon frequency we see is modified by the speed $v$ relative to us according to
$$\nu^{\pm}=\nu_{0} \frac{1\pm v/c}{\sqrt{ 1-v^{2}/c^{2} }}$$
Thus, the energy of a photon in the lab frame must be
$$E^{\pm}=2\pi \hbar \nu^{\pm}=2\pi \hbar \nu_{0} \frac{1\pm v/c}{\sqrt{ 1-v^{2}/c^{2} }}=E_{0} \frac{1\pm v/c}{\sqrt{ 1-v^{2}/c^{2} }}$$
By conservation of energy, this is the total lab frame electron-positron energy too
$$E_{e^{+}e^{-}}=\frac{E_{0}(1+v/c)}{\sqrt{ 1-v^{2}/c^{2} }}+ \frac{E_{0}(1-v/c)}{\sqrt{ 1-v^{2}/c^{2} }}=\frac{2E_{0}}{\sqrt{ 1-v^{2}/c^{2} }}=\frac{E^{0}_{e^{+}e^{-}}}{\sqrt{ 1-v^{2}/c^{2} }}\equiv E_{e^{+}e_{-}}(v)$$
 We can see how the energy is a function of velocity. To further analyze this function, we'll make a [[Taylor series|Taylor series]] in $(v/c)^{2}$ centered in zero:
$$E_{e^{+}e^{-}}(v)=E^{0}_{e^{+}e^{+}}+ \frac{1}{2}E^{0}_{e^{+}e^{-}}\left( \frac{v}{c} \right)^{2}+O\left( \left( \frac{v}{c} \right)^{4} \right)$$
The first term is independent of speed. It's some constant amount of energy that is intrinsic to the particles. This is the **rest energy**. The second term is quadratically dependent on velocity. Since $E^{0}_{e^{+}e^{-}}/c^{2}$ has the units of mass, we can interpret this as just the classical kinetic energy $\frac{1}{2}mv^{2}$, with the mass being determined by this now very famous formula for the rest energy due to Einstein:
$$\boxed{E^{0}_{e^{+}e^{-}}=m_{e^{+}e^{-}}c^{2}}$$
Knowing this, we can go back and rewrite the total energy of the electrons:
$$\boxed{E_{e^{+}e^{-}}=\frac{m_{e^{+}e^{-}}c^{2}}{\sqrt{ 1-v^{2}/c^{2} }}=\gamma m_{e^{+}e^{-}}c^{2}}$$
The kinetic energy must then be the the total energy minus the rest energy:
$$T=E_{e^{+}e^{-}}(v)-m_{e^{+}e^{-}}c^{2}=\gamma m_{e^{+}e^{-}}c^{2}-m_{e^{+}e^{-}}c^{2}=(\gamma-1)m_{e^{+}e^{-}}c^{2}$$
When substituting $\gamma$ we get
$$\boxed{T=\gamma mc^{2}-mc^{2}=\frac{mc^{2}}{\sqrt{ 1- v^{2}/c^{2} }}-mc^{2}}$$
as we claimed at the beginning. If take our series expansion of $E^{0}$ again and we subtract $mc^{2}$ from it, we see
$$T=\frac{1}{2}mv^{2}+O(v^{4})$$
Evidently, the classical kinetic energy is just the first term in the expansion of the relativistic kinetic energy.


[^1]: For more in-depth discussion on particle interactions, see [[Diffusione di particelle]].
