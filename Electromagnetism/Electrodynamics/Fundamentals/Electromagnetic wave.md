---
wiki-publish: true
---
An **electromagnetic wave** is a [[wave]] produced by the periodic variation and mutual [[Electromagnetic induction|induction]] of an [[Electric field|electric]] and a [[magnetic field]]. It is a [[transverse wave]], which means that the fields are always [[Orthogonality|orthogonal]] to the direction of propagation.

Electromagnetic waves are a consequence of [[Maxwell's equations]]. In the vacuum, with no [[Electric charge|charges]] whatsoever, the equations can be decoupled to read
$$\nabla ^{2}\mathbf{E}=\varepsilon_{0}\mu_{0}\frac{ \partial ^{2}\mathbf{E} }{ \partial t^{2} } ,\qquad \nabla ^{2}\mathbf{B}=\varepsilon_{0}\mu_{0}\frac{ \partial ^{2}\mathbf{B} }{ \partial t^{2} } $$
Both of these are examples of the [[wave equation]] and thus $\mathbf{E}$ and $\mathbf{B}$ accept wave solutions. Being solutions to the wave equations, their [[phase velocity]] must be
$$c=\frac{1}{\sqrt{ \varepsilon_{0}\mu_{0} }}$$
which is the [[speed of light]].
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
### In matter
To develop a theory of electromagnetic waves in matter, we turn to the Maxwell equations in matter. We set the free charge and free current to zero, but quickly hit an impasse. The behavior of waves in matter is, unsurprisingly, dependent on the nature of the material itself, namely how the [[electric displacement]] and [[auxiliary field]] behave. We can however restrict ourselves to the usual and generally quite useful case of linear, homogeneous and isotropic materials, in which the shapes of $\mathbf{D}$ and $\mathbf{H}$ are well-known. In such a setting, we get
$$\nabla ^{2}\mathbf{E}=\varepsilon\mu\frac{ \partial ^{2}\mathbf{E} }{ \partial t^{2} } ,\qquad \nabla ^{2}\mathbf{B}=\varepsilon\mu\frac{ \partial ^{2}\mathbf{B} }{ \partial t^{2} } $$
This form is near-identical to the vacuum one, with the difference of using general [[permittivity]] and [[permeability]] instead of their vacuum versions. This leads to a different shape for the phase velocity:
$$v=\frac{1}{\sqrt{ \varepsilon \mu }}=\frac{1}{\sqrt{ \varepsilon_{0}\varepsilon_{r}\mu_{0}\mu_{r} }}=\underbrace{ \frac{1}{\sqrt{ \varepsilon_{0} \mu_{0} }} }_{ c } \underbrace{ \frac{1}{\sqrt{ \varepsilon_{r}\mu_{r} }} }_{ 1/n }=\frac{c}{n}$$
The quantity $n\geq1$ is called the **[[refractive index]]** of the material and, among other things, determines a slowdown of the wave when in matter.

The transported quantities of these waves are largely the same and can be found by substituting $\varepsilon_{0}\to \varepsilon$, $\mu_{0}\to \mu$ and $c\to c/n$, so
$$u=\frac{1}{2}\left( \epsilon E^{2}+ \frac{1}{\mu}B^{2} \right),\quad \mathbf{S}=\frac{1}{\mu}(\mathbf{E}\times \mathbf{B})$$
In case of a sine wave, we have the same condition as $(1)$, so
$$u=\varepsilon E_{0}^{2},\quad \mathbf{S}=\varepsilon cE_{0}^{2}\hat{\mathbf{n}}$$
and then averaged
$$\boxed{\langle u \rangle =\frac{\varepsilon}{2}E_{0}^{2},\quad \langle \mathbf{S} \rangle =\frac{\varepsilon c}{2n}E_{0}^{2}\ \hat{\mathbf{n}}}$$
You might notice the suspicious lack of momentum density here. That's because the momentum of a wave in matter is, as of today, still a matter of debate, so no formula here.
### Interface reflection and transmission
As all waves, electromagnetic waves too exhibit interesting behavior when they reach the "end of the line", that is, when they collide with an interface between two different materials. Say we've got a wave traveling over the $x$ direction and there's an interface on the $yz$ plane at $x=0$ so that $x<0$ is one material with refractive index $n_{1}$ and $x>0$ is another with refractive index $n_{2}$. Say also for ease of use that the wave is linearly polarized on the $y$ axis and it has an angular frequency of $\omega$ and a wavenumber $k_{1}$. The wave equations are
$$\tilde{\mathbf{E}}_{I}(x,t)=\tilde{E}_{0,I}e^{i(k_{1}x-\omega t)}\hat{\mathbf{y}},\quad \tilde{\mathbf{B}}_{I}(x,t)=\frac{n_{1}}{c}\tilde{E}_{0,I}e^{i(k_{1}x-\omega t)}\hat{\mathbf{z}}$$
We know from the general theory of waves (see [[Wave equation#Boundary conditions]]) that an incident wave to a surface gives rise to a reflected and a transmitted wave, whose nature depends on the boundary conditions. These waves are
$$\tilde{\mathbf{E}}_{R}(x,t)=\tilde{E}_{0,R}e^{i(-k_{1}x-\omega t)}\hat{\mathbf{y}},\quad \tilde{\mathbf{B}}_{R}(x,t)=-\frac{n_{1}}{c}\tilde{E}_{0,R}e^{i(-k_{1}x-\omega t)}\hat{\mathbf{z}}$$
for the reflected one and
$$\tilde{\mathbf{E}}_{T}(x,t)=\tilde{E}_{0,T}e^{i(k_{2}x-\omega t)}\hat{\mathbf{y}},\quad \tilde{\mathbf{B}}_{T}(x,t)=\frac{n_{2}}{c}\tilde{E}_{0,T}e^{i(k_{2}x-\omega t)}\hat{\mathbf{z}}$$
The boundary conditions are given by Maxwell's equations
$$\begin{align}
\varepsilon_{1}E_{1}^{\perp}-\varepsilon_{2}E_{2}^{\perp} & =\sigma_{f} & \mathbf{E}_{1}^{\parallel}-\mathbf{E}_{2}^{\parallel} & =\mathbf{0} \\
B_{1}^{\perp}-B_{2}^{\perp} & =0 & \frac{1}{\mu_{1}}\mathbf{B}_{1}^{\parallel}- \frac{1}{\mu_{2}}\mathbf{B}_{2}^{\parallel}&=\mathbf{0}
\end{align}$$
Now, what these tell us depends on how the wave strikes the surface. If, as we chose above, have a wave that hits the surface at an exact 90° angle, we say that the wave is at **normal incidence**. This is the easiest case and in general not too unrealistic either in some artificial conditions, so that's the one we start with.

When incidence is normal, the two perpendicular boundary conditions don't matter since there is no perpendicular component. The parallel electric field condition implies
$$\tilde{E}_{0,I}+\tilde{E}_{0,R}=\tilde{E}_{0,T}$$
and the parallel magnetic field implies
$$\frac{1}{\mu_{1}}\left( \frac{n_{1}}{c}\tilde{E}_{0,I}- \frac{n_{1}}{c}\tilde{E}_{0,R} \right)=\frac{1}{\mu_{2}} \frac{n_{2}}{c}\tilde{E}_{0,T}$$
If we define
$$\beta\equiv \frac{\mu_{1}n_{2}}{\mu_{2}n_{1}}$$
this simplifies to
$$\tilde{E}_{0,I}-\tilde{E}_{0,R}=\beta \tilde{E}_{0,T}$$
We can solve these to express reflected and transmitted amplitude in terms of the incident one:
$$\tilde{E}_{0,R}=\left( \frac{1-\beta}{1+\beta} \right)\tilde{E}_{0,I},\qquad \tilde{E}_{0,T}=\left( \frac{2}{1+\beta} \right)\tilde{E}_{0,T}$$
These are the amplitudes we were looking for. These are true in general for electromagnetic sine waves at normal incidence. We can however squeeze more physical significance out of these. This is because in most materials, the relative permeability is *essentially* one, and so $\mu \simeq \mu_{0}$. Thus, $\beta$ simplifies down to $\beta \simeq n_{2}/n_{1}$ and our amplitudes become
$$\tilde{E}_{0,R}\simeq\left( \frac{n_{1}-n_{2}}{n_{1}+n_{2}} \right)\tilde{E}_{0,I},\qquad \tilde{E}_{0,T}\simeq\left( \frac{2n_{1}}{n_{1}+n_{2}} \right)\tilde{E}_{0,I}$$
Don't let the approximate equals sign fool you: these are perfectly valid equations in most materials. These of course fail when $\mu_{r}\gg1$, as is the case in many metals and generally all strong magnetic amplifiers, but most other materials have quite negligible relative permeabilities, so these are safe to use. The real parts are
$$E_{0,R}\simeq \left\lvert  \frac{n_{1}-n_{2}}{n_{1}+n_{2}}  \right\rvert E_{0,I},\qquad E_{0,T}\simeq \left\lvert  \frac{2n_{1}}{n_{1}+n_{2}}  \right\rvert E_{0,I}$$
The amplitudes themselves are theoretically important, but in practice one generally cares about the irradiance of the wave. Since the amplitude uniquely determines the irradiance according to
$$I=\frac{\varepsilon c}{2n}E_{0}^{2}$$
More so than the irradiances themselves though, it's interesting to see how they change after reflection or transmission. We do this by finding the ratios between incident and reflected/transmitted irradiance:
$$\boxed{R\equiv \frac{I_{R}}{I_{I}}=\left( \frac{E_{0,R}}{E_{0,I}} \right)^{2}=\left( \frac{n_{1}-n_{2}}{n_{1}+n_{2}} \right)^{2},\qquad T\equiv \frac{I_{T}}{I_{I}}=\frac{\varepsilon_{2}n_{1}}{\varepsilon_{1}n_{2}}\left( \frac{E_{0,T}}{E_{0,I}} \right)^{2}=\frac{4n_{1}n_{2}}{(n_{1}+n_{2})^{2}}}$$
These are known as the **reflection** and **transmission coefficients** respectively and represent the fraction of the irradiance that is transferred to the reflect and transmitted waves on interface interaction. Note that, since energy must be conserved, these coefficients abide by
$$R+T=1$$
as can be shown by doing the math directly.

[^1]: The magnetic's field contribution being entirely determined by the electric field is a recurring theme in electrodynamics and it is no coincidence. However, the explanation must wait until relativistic electrodynamics to make any semblance of sense.
