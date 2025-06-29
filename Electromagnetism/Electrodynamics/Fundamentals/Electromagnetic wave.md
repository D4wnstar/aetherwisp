---
wiki-publish: true
---
An **electromagnetic wave** is a [[wave]] produced by the periodic variation and mutual [[Electromagnetic induction|induction]] of an [[Electric field|electric]] and a [[magnetic field]]. It is a [[transverse wave]], which means that the fields are always [[Orthogonality|orthogonal]] to the direction of propagation.

Electromagnetic waves are a consequence of [[Maxwell's equations]]. In the vacuum, with no [[Electric charge|charges]] whatsoever, the equations can be decoupled to read
$$\nabla ^{2}\mathbf{E}=\varepsilon_{0}\mu_{0}\frac{ \partial ^{2}\mathbf{E} }{ \partial t^{2} } ,\qquad \nabla ^{2}\mathbf{B}=\varepsilon_{0}\varepsilon_{0}\frac{ \partial ^{2}\mathbf{B} }{ \partial t^{2} } $$
Both of these are examples of the [[wave equation]] and thus $\mathbf{E}$ and $\mathbf{B}$ accept wave solutions.
### Sine plane waves
Let's start by analyzing the behavior of electromagnetic [[Plane wave|sine waves]]. These are, as always, of paramount importance since all waves can be decomposed into a [[Fourier series]] of sine waves. In complex notation, these read
$$\tilde{\mathbf{E}}=\tilde{\mathbf{E}}_{0}e^{i(kx-\omega t)},\qquad \tilde{\mathbf{B}}=\tilde{\mathbf{B}}_{0}e^{i(kx-\omega t)}$$
assuming the propagate on the $x$ axis. The real fields can be recovered by taking the [[real and imaginary parts|real part]] of the complex field. Now, this equation is entirely determined from the wave equation. However, as it is, it cannot be correct. This is because Maxwell's equation impose specific constraints on the possible functions that $\mathbf{E}$ and $\mathbf{B}$ can be. Here we bypassed all of that by arbitrarily picking a known solution to the wave equation. While it is true that all vacuum solutions of Maxwell's equation must obey the wave equation, solutions to the wave equation may instead not obey Maxwell's equations. As such, we must reintroduce these obligations back into the fields manually.

Maxwell's equation determine the fields, so the conditions must be applied to $\tilde{\mathbf{E}}_{0}$ and $\tilde{\mathbf{B}}_{0}$. These conditions are the values of the [[divergence]] and [[curl]]. The divergence of these fields in a vacuum is zero, so it must be that
$$\tilde{E}_{0,x}=\tilde{B}_{0,x}=0$$
Intuitively, this is because the divergence in a way represents propagation. As such, if it must be zero, then the field cannot possibly extend in the direction of propagation. But if the oscillation of field cannot be in the direction of propagation, then *all electromagnetic waves must be transverse*! That's it for divergence. The curls on the other hand tell us that the fields induce each other, so clearly there has to be some connection between electric waves and magnetic waves. The curl of $\mathbf{E}$ gives one connection (by looking at the components of the [[vector product]] directly):
$$-k\tilde{E}_{0,y}=\omega \tilde{B}_{0,z},\qquad-k\tilde{E}_{0,z}=\omega \tilde{B}_{0,y}$$
or with the vector product
$$\tilde{\mathbf{B}}_{0}=\frac{k}{\omega}(\hat{\mathbf{x}}\times \tilde{\mathbf{E}}_{0})$$
The curl of $\mathbf{B}$ provides nothing new: it just recreates this formula starting from the other side. This should be enough to convince you that the electric and magnetic parts of the wave not only are symmetric, but also *strongly bound* to each other, for they must be both in [[phase]] and mutually [[Orthogonality|perpendicular]] (due to the vector product). Their real [[Amplitude|amplitudes]] must be related by
$$B_{0}=\frac{k}{\omega}E_{0}=\frac{1}{c}E_{0}\tag{1}$$
where $c=\omega/k$ is the [[phase velocity]] of the wave, coinciding with the [[speed of light]].

For example, suppose you have a wave moving on the $x$ axis. Suppose also that the electric field moves on the $y$ axis. Then, the magnetic one must occupy the last remaining axis, $z$. Their equations in general are of the sort
$$\tilde{\mathbf{E}}(x,t)=\tilde{E}_{0}e^{i(kx-\omega t)}\hat{\mathbf{y}},\qquad \tilde{\mathbf{B}}(x,t)=\tilde{B}_{0}e^{i(kx-\omega t)}\hat{\mathbf{z}}$$
Apply the previous conditions to get
$$\tilde{\mathbf{E}}(x,t)=\tilde{E}_{0}e^{i(kx-\omega t)}\hat{\mathbf{y}},\qquad \tilde{\mathbf{B}}(x,t)=\frac{1}{c}\tilde{E}_{0}e^{i(kx-\omega t)}\hat{\mathbf{z}}$$
Take the real part and finally you have a electromagnetic sine wave on the $x$ axis:
$$\mathbf{E}(x,t)=E_{0}\cos(kx-\omega t+\varphi)\hat{\mathbf{y}},\qquad \mathbf{B}(x,t)=\frac{1}{c}E_{0}\cos(kx-\omega t+\varphi)\hat{\mathbf{z}}$$
This is an electromagnetic wave propagating over $\hat{\mathbf{x}}$ that is [[Polarization|polarized]] in the $\hat{\mathbf{y}}$ direction (by convention, it is the direction of $\mathbf{E}$ that specifies the polarization). Of course, electromagnetic waves can propagate in any direction, so we can generalize to a truly general purpose electromagnetic sine wave by introducing the [[Wavenumber|wavevector]] $\mathbf{k}$ and the polarization vector $\hat{\mathbf{n}}$:
$$\boxed{\begin{align}
\tilde{\mathbf{E}}(\mathbf{r},t)&=\tilde{E}_{0}e^{i(\mathbf{k}\cdot \mathbf{r}-\omega t)}\hat{\mathbf{n}} \\
\tilde{\mathbf{B}}(\mathbf{r},t)&=\frac{1}{c}\tilde{E}_{0}e^{i(\mathbf{k}\cdot \mathbf{r}-\omega t)}(\hat{\mathbf{k}}\times \hat{\mathbf{n}})=\frac{1}{c}\hat{\mathbf{k}}\times \tilde{\mathbf{E}}
\end{align}}$$
whose real part is
$$\boxed{\begin{align}
\mathbf{E}(\mathbf{r},t)&=E_{0}\cos(\mathbf{k}\cdot \mathbf{r}-\omega t+\varphi)\hat{\mathbf{n}} \\
\mathbf{B}(\mathbf{r},t)&=\frac{1}{c}E_{0}\cos(\mathbf{k}\cdot \mathbf{r}-\omega t+\varphi)(\hat{\mathbf{k}}\times \hat{\mathbf{n}})=\frac{1}{c}\hat{\mathbf{k}}\times \mathbf{E}
\end{align}}$$
### Transported quantities
Electromagnetic waves are essentially traveling electromagnetic fields. As such, they carry all quantities that the fields themselves do, chiefly [[energy]] and [[Linear momentum|momentum]].

The energy density of an electromagnetic field is
$$u=\frac{1}{2}\left( \varepsilon_{0}E^{2}+ \frac{1}{\mu_{0}}B^{2} \right)$$
In case of a sine wave, we can use $(1)$ to state
$$B^{2}=\frac{E^{2}}{c^{2}}=\mu_{0}\varepsilon_{0}E^{2}$$
and so
$$\boxed{u=\varepsilon_{0}E^{2}=\varepsilon_{0}E_{0}^{2}\cos ^{2}(\mathbf{k}\cdot \mathbf{r}-\omega t+\varphi)}$$
Evidently, only the electric field matters in the energy transfer, as the magnetic field's contribution is identical to that of the electric field[^1]. We can say more about this by looking at the [[Poynting vector]], which represent the energy [[flux]] density (energy per unit area per unit time). Plugging in the previous equation for $B$ gives
$$\mathbf{S}=c\varepsilon_{0}E_{0}^{2}\cos ^{2}(\mathbf{k}\cdot \mathbf{r}-\omega t+\varphi)\hat{\mathbf{n}}=cu\ \hat{\mathbf{n}}$$
Perhaps unsurprisingly, the energy moves in the exact direction of the wave. Finally, the momentum density carried by the field is
$$\mathbf{g}=\frac{u}{c}\hat{\mathbf{n}}$$

Generally speaking though, electromagnetic wave [[Frequency|frequencies]] are *fast*. So fast in fact that any measurement done at a macroscopic level will surely encompass a large number of cycles of oscillation. As such, a reading of any of these quantities is going to be smeared across so many cycles it essentially just becomes the time average of the quantity. As such, it's in our interest to take a look at the mathematical predictions of these averages. Since the only variable part in these quantities is the square cosine, we just need its  average over a full cycle of [[period]] $T$:
$$\langle \cos ^{2}(\ldots) \rangle = \frac{1}{T}\int_{0}^{T}\cos ^{2}\left( \mathbf{k}\cdot \mathbf{r}- \frac{2\pi}{T} t+\varphi \right)dt=\frac{1}{2}$$
Thus, the average energy density, Poynting vector and momentum density are
$$\boxed{\langle u \rangle =\frac{\varepsilon_{0}}{2}E_{0}^{2},\quad \langle \mathbf{S} \rangle =\frac{\varepsilon_{0}c}{2}E_{0}^{2}\ \hat{\mathbf{n}},\quad \langle \mathbf{g} \rangle =\frac{\varepsilon_{0}}{2c}E_{0}^{2}\ \hat{\mathbf{n}}}$$
In the context of electromagnetic waves, the **[[irradiance]]** of the wave is the time average of the Poynting vector:
$$I\equiv\langle S \rangle =\frac{\varepsilon_{0}c}{2}E_{0}^{2}$$
Since momentum is conserved, whenever light collides with sometimes, a part of its momentum must be transferred to it. If light lands perpendicularly (normal incidence) and the receiver is a so-called "perfect absorber" (meaning, it absorbs 100% of the momentum that hits it), we can give a mathematical expression of this transfer. In a time $\Delta t$, the transfer is determined by the momentum density as $\Delta \mathbf{p}=\langle \mathbf{g} \rangle Ac\Delta t$. But remember that by [[Newton's laws|Newton's second law]], a variation in momentum is a [[force]], so when spread over the area $A$ that's being lit up, we get a [[pressure]]:
$$\boxed{P=\frac{1}{A} \frac{\Delta \lvert \mathbf{p} \rvert }{\Delta t}=\frac{\varepsilon_{0}}{2}E_{0}^{2}=\frac{I}{c}}$$
This pressure is known as **[[radiation pressure]]** and, in general, it is *extremely* weak. Weak enough that it's fair if you assumed that electromagnetic radiation was simply incapable of applying a force to something. But it *is* there, all because momentum conservation must be preserved. By the way, if the receiver was a "perfect reflector" (meaning, it reflects 100% of the momentum), the pressure would be doubled since the effective $\Delta \lvert \mathbf{p} \rvert$ would itself be doubled (since we'd be sending $\mathbf{p}\mapsto-\mathbf{p}$ instead of $\mathbf{p}\mapsto0$).

[^1]: The magnetic's field contribution being entirely determined by the electric field is a recurring theme in electrodynamics and it is no coincidence. However, the explanation must wait until relativistic electrodynamics to make any semblance of sense.
