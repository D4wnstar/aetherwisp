---
wiki-publish: true
---
The **Larmor formula** gives the [[electromagnetic radiation|radiated]] [[radiant power|power]] emitted by an accelerating [[Electric charge|point charge]] $q$:
$$P=\frac{\mu_{0}q^{2}a^{2}}{6\pi c}$$
where $a$ is the acceleration of the charge. This is an approximation that is exact when the speed of the particle is zero and generally works quite well in all [[Lorentz transformation|nonrelativistic]] scenarios. When the speed starts to approach the [[speed of light]], we can use the **Liénard generalization**:
$$P_\text{charge}=\frac{\mu_{0}q^{2}\gamma^{6}}{6\pi c}\left( a^{2}- \left\lvert  \frac{\mathbf{v}\times \mathbf{a}}{c}  \right\rvert ^{2} \right)$$
where $\mathbf{v}$ is the velocity of the charge and $\gamma=1/\sqrt{ 1-v^{2}/c^{2} }$ is the usual relativistic coefficient.
### Derivation
We start from the [[Electric field|electric]] and [[magnetic field]] of an accelerating point charge $q$, as given by the [[Liénard-Wiechert potentials]]:
$$\mathbf{E}(\mathbf{r},t)=\frac{q}{4\pi \varepsilon_{0}} \frac{\mathfrak{r}}{(\boldsymbol{\mathfrak{r}}\cdot \mathbf{u})^{3}}
[(c^{2}-v^{2})\mathbf{u}+\boldsymbol{\mathfrak{r}}\times(\mathbf{u}\times \mathbf{a})]$$
$$\mathbf{B}(\mathbf{r},t)=\frac{1}{c}\hat{\boldsymbol{\mathfrak{r}}}\times \mathbf{E}(\mathbf{r},t)$$
where $\mathbf{u}=c \hat{\boldsymbol{\mathfrak{r}}}-\mathbf{v}$. Recall that the first term is known as the velocity field and the second as the acceleration field due to their dynamical origin. The transfer of [[energy]] is given by the [[Poynting vector]]:
$$\mathbf{S}=\frac{1}{\mu_{0}}(\mathbf{E}\times \mathbf{B})= \frac{1}{\mu_{0}c}[\mathbf{E}\times(\hat{\boldsymbol{\mathfrak{r}}}\times \mathbf{E})]=\frac{1}{\mu_{0}c}[E^{2}\hat{\boldsymbol{\mathfrak{r}}}-(\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{E})\mathbf{E}]$$
using the triple product rule. This is energy that's moved, but it does not necessarily represent radiated energy. It might be energy that's carried with the charge as it moves inside its fields. We only care about the part that leaves the point charge and is launched elsewhere, that is, radiation. To calculate this, we imagine a large [[sphere]] of radius $\mathfrak{r}$ centered on our point charge at the [[retarded time]] $t_{r}$, then imagine waiting for the [[Electromagnetic wave|electromagnetic waves]] to reach the sphere an interval of time given by
$$t-t_{r}=\frac{\mathfrak{r}}{c}$$
Once the waves arrive, we integrate the Poynting vector over the sphere. A sphere has area that goes like $\sim \mathfrak{r}^{2}$, so any term in $\mathbf{S}$ that goes like $\sim \mathfrak{r}^{-2}$ will lead to a finite result and any term of higher order, $\sim r^{-3}$, $\sim r^{-4}$, etc., will vanish and contribute nothing when $\mathfrak{r}\to \infty$. As such, it is only the acceleration field component that remains:
$$\mathbf{E}_\text{rad}=\frac{1}{4\pi \varepsilon_{0}} \frac{\mathfrak{r}}{(\boldsymbol{\mathfrak{r}}\cdot \mathbf{u})^{3}}\boldsymbol{\mathfrak{r}}\times(\mathbf{u}\times \mathbf{a})$$
This term goes like $\sim \mathfrak{r}^{-1}$, which becomes $\sim \mathfrak{r}^{-2}$ when square in the Poynting vector. The velocity field's energy instead remains attached to the charge itself.

Now, $\mathbf{E}_\text{rad}$ is [[Orthogonality|perpendicular]] to $\hat{\boldsymbol{\mathfrak{r}}}$ due to the [[vector product]] with it, so the second term in the Poynting vector vanishes (because the [[scalar product]] $\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{E}$ is zero). We are then left with
$$\mathbf{S}_\text{rad}=\frac{1}{\mu_{0}c}E_\text{rad}^{2}\hat{\boldsymbol{\mathfrak{r}}}$$
We only need the square of the magnitude of $\mathbf{E}_\text{rad}$.

We'll start by analyzing the case where the charge is instantaneously at rest (at time $t_{r}$), then $\mathbf{v}(t_{r})=0$ and so $\mathbf{u}(t_{r})=c \hat{\boldsymbol{\mathfrak{r}}}$. This means, extracting the magnitudes out all the $\boldsymbol{\mathfrak{r}}=\mathfrak{r}\hat{\boldsymbol{\mathfrak{r}}}$, that
$$\mathbf{E}_\text{rad}=\frac{1}{4\pi \varepsilon_{0}} \frac{\mathfrak{r}}{\mathfrak{r}^{3}c^{3}(\hat{\boldsymbol{\mathfrak{r}}}\cdot \hat{\boldsymbol{\mathfrak{r}}})}\mathfrak{r}\hat{\boldsymbol{\mathfrak{r}}}\times(c \hat{\boldsymbol{\mathfrak{r}}}\times \mathbf{a})=\frac{1}{4\pi \varepsilon_{0}} \frac{1}{\mathfrak{r}c^{2}}\hat{\boldsymbol{\mathfrak{r}}}\times(\hat{\boldsymbol{\mathfrak{r}}}\times \mathbf{a})=\frac{\mu_{0}q}{4\pi \mathfrak{r}}[(\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{a})\hat{\boldsymbol{\mathfrak{r}}}-\mathbf{a}]$$
where we again expanded the triple product and also used $c^{2}=1/\mu_{0}\varepsilon_{0}$. The Poynting vector then is
$$\mathbf{S}_\text{rad}=\frac{1}{\mu_{0}c} \left( \frac{\mu_{0}q}{4\pi \mathfrak{r}} \right)^{2}[a^{2}-(\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{a})^{2}]\hat{\boldsymbol{\mathfrak{r}}}=\frac{\mu_{0}q^{2}a^{2}}{16\pi ^{2}c\mathfrak{r}^{2}}\sin ^{2}\theta\ \hat{\boldsymbol{\mathfrak{r}}}$$
where $\theta$ is the angle between $\hat{\boldsymbol{\mathfrak{r}}}$ and $\mathbf{a}$. Similarly to the case of a radiation from a small stationary source, the radiation is emitted in a [[torus]] shape modulated by $\sin ^{2}\theta$. There is no radiation in the (instantaneous) direction of acceleration[^1] of the point charge and it is maximized perpendicular to this direction. Finally, the total radiant power is
$$P=\oint_{\mathcal{S}}\mathbf{S}\cdot d\mathbf{a}=\frac{\mu_{0}q^{2}a^{2}}{16\pi ^{2}c}\int_{0}^{2\pi}\int_{0}^{\pi} \frac{\sin ^{2}\theta}{\mathfrak{r}^{2}} \mathfrak{r}^{2}\sin \theta \ d\theta d\phi $$
which yields
$$\boxed{P=\frac{\mu_{0}q^{2}a^{2}}{6\pi c}}$$
This is known as the **Larmor formula**. It provides the power emitted by an accelerating particle that is instantaneously at rest, which means $\mathbf{v}=0$ at the time of emitting radiation. This is of course an approximation, but it is quite a good one, since it holds pretty well for all [[Lorentz transformation|nonrelativistic]] speeds, $v\ll c$. The exact solution for the $\mathbf{v}\neq 0$ can nevertheless be found, even if it's more complicated.

The complication is twofold: on one hand, we of course can't simplify $\mathbf{u}$ like we did before, but on the other, there's a subtle problem on the rate of emission and rate of absorption of the energy (if you know what the [[Doppler effect]] is, you can probably see where I'm going with this). When a charge accelerates, it emits radiation. If the particle is moving, it emits energy at some rate $P_\text{charge}$, but the sphere receives it as some other rate $P_\text{sphere}$. Since the charge is moving, the waves emitted at some moment will tend to overlap waves emitted at an earlier moment, since the charge "catches up" with them due its own motion. As you might imagine, this *increases* the rate of energy received by the sphere, even though that emitted by the charge is still the same. This is, as mentioned above, a consequence of the [[Doppler effect]] (higher [[frequency]] means higher energy). The exact factor is
$$P_\text{charge}=\left( 1- \frac{\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{v}}{c} \right)P_\text{sphere}$$
You can double check this by taking the retarded-time derivative of the energy $U$, which is the radiated power:
$$P_\text{charge}=\frac{ \partial U }{ \partial t_{r} }=\frac{ \partial U }{ \partial t } \frac{ \partial t }{ \partial t_{r} }=\left( \frac{\boldsymbol{\mathfrak{r}}\cdot \mathbf{u}}{\mathfrak{r}c} \right) \frac{ \partial U }{ \partial t } =\left( 1- \frac{\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{v}}{c} \right)P_\text{sphere}$$
Now, the velocity with respect to the sphere depends on a couple angles, $\theta$ and $\phi$, since we are in [[spherical coordinates]]. As such, we'll figure out what the power per unit *[[solid angle]]* $d\Omega=\sin \theta d\theta d\phi$ is, then integrate over all solid angles. The unit power *radiated* is
$$\begin{align}
dP_\text{charge}&=\left( \frac{\boldsymbol{\mathfrak{r}}\cdot \mathbf{u}}{\mathfrak{r}c} \right) dP_\text{sphere}=\left( \frac{\boldsymbol{\mathfrak{r}}\cdot \mathbf{u}}{\mathfrak{r}c} \right)\mathbf{S}_\text{rad}\cdot d\mathbf{a}=\left( \frac{\boldsymbol{\mathfrak{r}}\cdot \mathbf{u}}{\mathfrak{r}c} \right)S_\text{rad}\mathfrak{r}^{2}\sin \theta d\theta d\phi \\
&=\left( \frac{\boldsymbol{\mathfrak{r}}\cdot \mathbf{u}}{\mathfrak{r}c} \right)S_\text{rad}\mathfrak{r}^{2}d\Omega
\end{align}$$
so
$$\frac{dP_\text{charge}}{d\Omega}=\left( \frac{\boldsymbol{\mathfrak{r}}\cdot \mathbf{u}}{\mathfrak{r}c} \right)S_\text{rad}\mathfrak{r}^{2}=\left( \frac{\boldsymbol{\mathfrak{r}}\cdot \mathbf{u}}{\mathfrak{r}c} \right) \frac{1}{\mu_{0}c}E_\text{rad}^{2}\mathfrak{r}^{2}=\frac{q^{2}}{16\pi ^{2}\varepsilon_{0}} \frac{\lvert \hat{\boldsymbol{\mathfrak{r}}}\times(\mathbf{u}\times \mathbf{a}) \rvert ^{2}}{(\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{u})^{5}}$$
If you're wondering if the integration over all solid angles looks painful, don't worry: it is. The answer is
$$\boxed{P_\text{charge}=\frac{\mu_{0}q^{2}\gamma^{6}}{6\pi c}\left( a^{2}- \left\lvert  \frac{\mathbf{v}\times \mathbf{a}}{c}  \right\rvert ^{2} \right)}$$
where
$$\gamma=\frac{1}{\sqrt{ 1- v^{2}/c^{2} }}$$
This is known as **Liènard's generalization** to the Larmor formula and it is the absolutely general result. Notice the presence of a *sixth* (!) power on $\gamma$. When $v/c$ is small (i.e. any nonrelativistic situation), it remains quite small, $\gamma \simeq 1$, and when $\mathbf{v}=0$, we can see $\gamma=0$ and the old Larmor formula. However, when $v$ starts to approach the [[speed of light]], the $\gamma^{6}$ term increases *immensely*, radiating massive amounts of energy when the charges moves at near light speed.

[^1]: This is important. The radiation doesn't care about where the charge is *going*, it cares about where it's accelerating. Say a charge is going straight through space, then it starts being pushed sideways by, say, the magnetic field of a [[Stella di neutroni|neutron star]]. The acceleration will not be on the line of motion, so the axis of the radiation torus will not follow the trajectory.
