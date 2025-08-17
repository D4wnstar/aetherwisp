---
wiki-publish: true
---
An **electromagnetic wave** is a [[wave]] produced by the periodic variation and mutual [[Electromagnetic induction|induction]] of an [[Electric field|electric]] and a [[magnetic field]]. It is a [[transverse wave]], which means that the fields are always [[Orthogonality|orthogonal]] to the direction of propagation.

Electromagnetic waves are described through [[Maxwell's equations]]. In the vacuum, with no [[Electric charge|charges]] whatsoever, the equations can be decoupled to read
$$\nabla ^{2}\mathbf{E}=\varepsilon_{0}\mu_{0}\frac{ \partial ^{2}\mathbf{E} }{ \partial t^{2} } ,\qquad \nabla ^{2}\mathbf{B}=\varepsilon_{0}\mu_{0}\frac{ \partial ^{2}\mathbf{B} }{ \partial t^{2} } $$
Both of these are examples of the [[wave equation]] and thus $\mathbf{E}$ and $\mathbf{B}$ accept wave solutions. Their [[phase velocity]] must be
$$c=\frac{1}{\sqrt{ \varepsilon_{0}\mu_{0} }}$$
which is the [[speed of light]].
### In the vacuum
Let's start by analyzing the behavior of electromagnetic [[Plane wave|sine waves]]. These are, as always, of paramount importance since all waves can be decomposed into a [[Fourier series]] of sine waves. Thus, understanding sine waves in theory means that you understand all other waves. In complex notation, they read
$$\tilde{\mathbf{E}}=\tilde{\mathbf{E}}_{0}e^{i(kx-\omega t)},\qquad \tilde{\mathbf{B}}=\tilde{\mathbf{B}}_{0}e^{i(kx-\omega t)}$$
assuming propagation on the $x$ axis. The real fields can be found by taking the [[real and imaginary parts|real part]] of the complex field. Now, this equation is entirely determined from the wave equation. However, as it is, it cannot be correct. This is because Maxwell's equation impose specific constraints on the possible functions that $\mathbf{E}$ and $\mathbf{B}$ can be. Here we bypassed all of that by arbitrarily picking a known solution to the wave equation. While it is true that all vacuum solutions of Maxwell's equation obey the wave equation, the converse is not necessarily true: not all solutions to the wave equation obey Maxwell's equations. In light of this, we should analyze Maxwell's equation to figure out what these additional constraints are.

Maxwell's equation determine the fields, so the conditions must be applied to $\tilde{\mathbf{E}}_{0}$ and $\tilde{\mathbf{B}}_{0}$. These conditions are the values of the [[divergence]] and [[curl]]. The divergence of these fields in a vacuum is zero, so it must be that
$$\tilde{E}_{0,x}=\tilde{B}_{0,x}=0$$
Intuitively, this is because the divergence in a way represents propagation. As such, if it must be zero, then the field cannot possibly extend in the direction of propagation. But if the oscillation cannot be in the direction of propagation, then *all electromagnetic waves must be transverse*!

That's it for divergence. The curls on the other hand tell us that the fields induce each other, so clearly there has to be some connection between electric waves and magnetic waves. The curl of $\mathbf{E}$ ([[Faraday's law]]) gives one connection (by looking at the components of the [[vector product]] directly):
$$\nabla\times \tilde{\mathbf{E}}=-\frac{ \partial \tilde{E}_{z} }{ \partial x } \hat{\mathbf{y}}+\frac{ \partial \tilde{E}_{y} }{ \partial x } \hat{\mathbf{z}}=-\tilde{E}_{0,z}ike^{i(kx-\omega t)}\hat{\mathbf{y}}+\tilde{E}_{0,y}ike^{i(kx-\omega t)}\hat{\mathbf{z}}=ik(-\tilde{E}_{z}\hat{\mathbf{y}}+\tilde{E}_{y}\hat{\mathbf{z}})$$
and also
$$\nabla\times \tilde{\mathbf{E}}=-\frac{ \partial \tilde{\mathbf{B}} }{ \partial t }=\tilde{\mathbf{B}}_{0}i\omega e^{i(kx-\omega t)}=i\omega \tilde{\mathbf{B}}=i\omega(\tilde{B}_{y}\hat{\mathbf{y}}+\tilde{B}_{z}\hat{\mathbf{z}})$$
(since the $x$ component is guaranteed zero). So, comparing the two:
$$-k\tilde{E}_{0,z}=\omega \tilde{B}_{0,y},\qquad k\tilde{E}_{0,y}=\omega \tilde{B}_{0,z}$$
which is equivalent to the vector product
$$\tilde{\mathbf{B}}_{0}=\frac{k}{\omega}(\hat{\mathbf{x}}\times \tilde{\mathbf{E}}_{0})$$
The curl of $\mathbf{B}$ provides the same result. This should be enough to convince you that the electric and magnetic parts of the wave not only are symmetric, but also *strongly* coupled, for they must be both in [[phase]] and [[Orthogonality|perpendicular]] (due to the vector product). Their real [[Amplitude|amplitudes]] must be related by
$$B_{0}=\frac{k}{\omega}E_{0}=\frac{1}{c}E_{0}\tag{1}$$
where $c=\omega/k$ is the [[phase velocity]] of the wave, coinciding with the [[speed of light]].

For example, suppose you have a wave moving on the $x$ axis. Suppose also that the electric field moves on the $y$ axis. Then, the magnetic one must occupy the last remaining axis, $z$. Their equations in general are of the sort
$$\tilde{\mathbf{E}}(x,t)=\tilde{E}_{0}e^{i(kx-\omega t)}\hat{\mathbf{y}},\qquad \tilde{\mathbf{B}}(x,t)=\tilde{B}_{0}e^{i(kx-\omega t)}\hat{\mathbf{z}}$$
Apply the previous conditions to get
$$\tilde{\mathbf{E}}(x,t)=\tilde{E}_{0}e^{i(kx-\omega t)}\hat{\mathbf{y}},\qquad \tilde{\mathbf{B}}(x,t)=\frac{1}{c}\tilde{E}_{0}e^{i(kx-\omega t)}\hat{\mathbf{z}}$$
Take the real part and finally you have a electromagnetic sine wave on the $x$ axis:
$$\mathbf{E}(x,t)=E_{0}\cos(kx-\omega t+\varphi)\hat{\mathbf{y}},\qquad \mathbf{B}(x,t)=\frac{1}{c}E_{0}\cos(kx-\omega t+\varphi)\hat{\mathbf{z}}$$
This is an electromagnetic wave propagating over $\hat{\mathbf{x}}$ that is [[Polarization|polarized]] on $\hat{\mathbf{y}}$ (by convention, it is the direction of $\mathbf{E}$ that specifies the polarization). The magnetic field needs to be orthogonal to both propagation and $\mathbf{E}$, so it ends up on $\hat{\mathbf{z}}$.

Of course, electromagnetic waves can propagate in any direction, so we can generalize further by introducing the [[Wavenumber|wavevector]] $\mathbf{k}$ and the polarization vector $\hat{\mathbf{n}}$:
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
Electromagnetic waves are really just traveling electromagnetic fields. As such, they carry all quantities that the fields themselves do, chiefly [[energy]] and [[Linear momentum|momentum]].

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

Generally speaking though, electromagnetic wave [[Frequency|frequencies]] are *fast*. So fast in fact that any measurement done at a macroscopic level will surely encompass a large number of cycles of oscillation. As such, a reading of any of these quantities is going to be smeared across so many cycles it essentially just becomes the time average of the quantity. As such, it's in our interest to take a look at the mathematical predictions of these averages. Since the only time-variable part in these quantities is the square cosine, we just need its  average over a full cycle of [[period]] $T$:
$$\langle \cos ^{2}(\ldots) \rangle = \frac{1}{T}\int_{0}^{T}\cos ^{2}\left( \mathbf{k}\cdot \mathbf{r}- \frac{2\pi}{T} t+\varphi \right)dt=\frac{1}{2}$$
Thus, the average energy density, Poynting vector and momentum density are
$$\boxed{\langle u \rangle =\frac{\varepsilon_{0}}{2}E_{0}^{2},\quad \langle \mathbf{S} \rangle =\frac{\varepsilon_{0}c}{2}E_{0}^{2}\ \hat{\mathbf{n}},\quad \langle \mathbf{g} \rangle =\frac{\varepsilon_{0}}{2c}E_{0}^{2}\ \hat{\mathbf{n}}}$$
Notably, energy density and momentum density (and by extension energy and momentum themselves) are related by
$$\langle u \rangle =\langle g \rangle c\quad\Rightarrow \quad E=\int_{\mathcal{V}}\langle u \rangle d\tau=c\int_{\mathcal{V}}\langle g \rangle d\tau=pc$$
The energy of a wave is given by the momentum it carries times the speed of light. "Neat," you might say, but keep this in mind when you look at quantum physics, as it might just reappear somewhere else (and if you've already studied quantum physics, you might recognize a sneaky first appearance of the [[Planck formula]] and the [[Formula di de Broglie|de Broglie formula]]).

In the context of electromagnetic waves, the **[[irradiance]]** of the wave is the magnitude of the time average of the Poynting vector:
$$I\equiv \lvert \langle S \rangle \rvert  =\frac{\varepsilon_{0}c}{2}E_{0}^{2}$$
Since momentum is conserved, whenever light collides with, sometimes a part of its momentum will be transferred to it. If light lands perpendicularly (normal incidence) and the receiver is a so-called "perfect absorber" (meaning, it absorbs 100% of the momentum that hits it), we can give a mathematical expression of this transfer. In a time $\Delta t$, the transfer is determined by the momentum density as $\Delta \mathbf{p}=\langle \mathbf{g} \rangle Ac\Delta t$. But remember that by [[Newton's laws|Newton's second law]], a variation in momentum is a [[force]], so when spread over the area $A$ that's being lit up, we get a [[pressure]]:
$$\boxed{P=\frac{1}{A} \frac{\Delta \lvert \mathbf{p} \rvert }{\Delta t}=\frac{\varepsilon_{0}}{2}E_{0}^{2}=\frac{I}{c}}$$
This pressure is known as **[[radiation pressure]]** and, in general, it is *extremely* weak. Weak enough that it's fair if you assumed that electromagnetic radiation was simply incapable of applying a force to something. But it *is* there, all because momentum conservation must be preserved. By the way, if the receiver was a "perfect reflector" (meaning, it reflects 100% of the momentum), the pressure would be doubled since the effective $\Delta \lvert \mathbf{p} \rvert$ would itself be doubled (since we'd be sending $\mathbf{p}\mapsto-\mathbf{p}$ instead of $\mathbf{p}\mapsto0$).
### In dielectrics
To develop a theory of electromagnetic waves in matter, we turn to the Maxwell equations in matter. We start off in an analogous way as the vacuum case by setting the free charge and free current to zero; this corresponds to claiming with are working with [[Dielectric|dielectrics]], where free charges are scarce. [[Conductor|Conductors]] require more refined analysis, which we'll defer to later. Still, even in this no-free-charge setting we quickly hit an impasse. The behavior of waves in matter is, unsurprisingly, dependent on the nature of the material itself, namely how the [[electric displacement]] and [[auxiliary field]] behave. We can however restrict ourselves to the usual and generally quite useful case of linear, homogeneous and isotropic materials, in which the shapes of $\mathbf{D}$ and $\mathbf{H}$ are well-known. In such a setting, we get
$$\nabla ^{2}\mathbf{E}=\varepsilon\mu\frac{ \partial ^{2}\mathbf{E} }{ \partial t^{2} } ,\qquad \nabla ^{2}\mathbf{B}=\varepsilon\mu\frac{ \partial ^{2}\mathbf{B} }{ \partial t^{2} } $$
This form is near-identical to the vacuum one, with the difference of using general [[permittivity]] and [[permeability]] instead of their vacuum versions. This leads to a different shape for the phase velocity:
$$v=\frac{1}{\sqrt{ \varepsilon \mu }}=\frac{1}{\sqrt{ \varepsilon_{0}\varepsilon_{r}\mu_{0}\mu_{r} }}=\underbrace{ \frac{1}{\sqrt{ \varepsilon_{0} \mu_{0} }} }_{ c } \underbrace{ \frac{1}{\sqrt{ \varepsilon_{r}\mu_{r} }} }_{ 1/n }=\frac{c}{n}$$
The quantity $n=\sqrt{ \varepsilon_{r}\mu_{r} }\geq1$ is called the **[[refractive index]]** of the material and, among other things, determines a slowdown of the wave when in matter. Most materials are not really magnetic, so in many cases $\mu_{r}\simeq1$ and $n\simeq \sqrt{ \varepsilon_{r} }$.

The transported quantities of these waves are largely the same and can be found by substituting $\varepsilon_{0}\to \varepsilon$, $\mu_{0}\to \mu$ and $c\to c/n$, so
$$u=\frac{1}{2}\left( \epsilon E^{2}+ \frac{1}{\mu}B^{2} \right),\quad \mathbf{S}=\frac{1}{\mu}(\mathbf{E}\times \mathbf{B})$$
In case of a sine wave, we have the same condition as $(1)$, so
$$u=\varepsilon E_{0}^{2},\quad \mathbf{S}=\varepsilon cE_{0}^{2}\hat{\mathbf{n}}$$
and then averaged
$$\boxed{\langle u \rangle =\frac{\varepsilon}{2}E_{0}^{2},\quad \langle \mathbf{S} \rangle =\frac{\varepsilon c}{2n}E_{0}^{2}\ \hat{\mathbf{n}}}$$
You might notice the suspicious lack of momentum density here. That's because the momentum of a wave in matter is, as of today, still a matter of debate, so no formula here.
#### Interface reflection and transmission
As all waves, electromagnetic waves too exhibit interesting behavior when they reach the "end of the line", that is, when they collide with an interface between two different materials. Say we've got a wave traveling over the $x$ direction and there's an interface on the $yz$ plane at $x=0$ so that $x<0$ is one material with refractive index $n_{1}$ and $x>0$ is another with refractive index $n_{2}$. Say also for simplicity that the wave is linearly polarized on the $y$ axis and it has an angular frequency of $\omega$ and a wavenumber $k_{1}$. The wave equations are
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
##### Normal incidence
When incidence is normal, the two perpendicular boundary conditions don't matter since there is no perpendicular component. The parallel electric field condition implies
$$\tilde{E}_{0,I}+\tilde{E}_{0,R}=\tilde{E}_{0,T}$$
and the parallel magnetic field implies
$$\frac{1}{\mu_{1}}\left( \frac{n_{1}}{c}\tilde{E}_{0,I}- \frac{n_{1}}{c}\tilde{E}_{0,R} \right)=\frac{1}{\mu_{2}} \frac{n_{2}}{c}\tilde{E}_{0,T}$$
If we define
$$\beta\equiv \frac{\mu_{1}n_{2}}{\mu_{2}n_{1}}$$
this simplifies to
$$\tilde{E}_{0,I}-\tilde{E}_{0,R}=\beta \tilde{E}_{0,T}$$
We can solve these to express reflected and transmitted amplitude in terms of the incident one:
$$\boxed{\tilde{E}_{0,R}=\left( \frac{1-\beta}{1+\beta} \right)\tilde{E}_{0,I},\qquad \tilde{E}_{0,T}=\left( \frac{2}{1+\beta} \right)\tilde{E}_{0,T}}$$
These are the amplitudes we were looking for. These are true in general for electromagnetic sine waves at normal incidence. We can however squeeze more physical significance out of these. This is because in most materials, the relative permeability is *essentially* one, and so $\mu \simeq \mu_{0}$. Thus, $\beta$ simplifies down to $\beta \simeq n_{2}/n_{1}$ and our amplitudes become
$$\tilde{E}_{0,R}\simeq\left( \frac{n_{1}-n_{2}}{n_{1}+n_{2}} \right)\tilde{E}_{0,I},\qquad \tilde{E}_{0,T}\simeq\left( \frac{2n_{1}}{n_{1}+n_{2}} \right)\tilde{E}_{0,I}$$
Don't let the approximate equals sign fool you: these are perfectly valid equations in most materials. These of course fail when $\mu_{r}\gg1$, as is the case in many metals and generally all strong magnetic amplifiers, but most other materials have quite negligible relative permeabilities, so these are safe to use. If $n_{1}<n_{2}$, the reflected wave is flipped upside down compared to the incident wave (a minus sign on complex amplitude corresponds to a $\pi$ [[phase]] shift). If $n_{1}>n_{2}$, then the phase is the same. The real parts are
$$E_{0,R}\simeq \left\lvert  \frac{n_{1}-n_{2}}{n_{1}+n_{2}}  \right\rvert E_{0,I},\qquad E_{0,T}\simeq \left(  \frac{2n_{1}}{n_{1}+n_{2}}   \right) E_{0,I}$$
The amplitudes themselves are theoretically important, but in practice one generally cares about the irradiance of the wave. The amplitude uniquely determines the irradiance according to
$$\boxed{I_{I}=\frac{\varepsilon c}{2n_{1}}E_{0,I}^{2},\qquad I_{R}=\frac{\varepsilon c}{2n_{1}}E_{0,R}^{2},\qquad I_{T}=\frac{\varepsilon c}{2n_{2}}E_{0,T}^{2}}$$
More so than the irradiances themselves though, it's interesting to see how they change after reflection or transmission. We do this by finding the ratios between incident and reflected/transmitted irradiance:
$$\boxed{R\equiv \frac{I_{R}}{I_{I}}=\left( \frac{E_{0,R}}{E_{0,I}} \right)^{2}=\left( \frac{n_{1}-n_{2}}{n_{1}+n_{2}} \right)^{2},\qquad T\equiv \frac{I_{T}}{I_{I}}=\frac{\varepsilon_{2}n_{1}}{\varepsilon_{1}n_{2}}\left( \frac{E_{0,T}}{E_{0,I}} \right)^{2}=\frac{4n_{1}n_{2}}{(n_{1}+n_{2})^{2}}}$$
These are known as the **reflection** and **transmission coefficients** (or **reflectance** and **transmittance**) and represent the fraction of the irradiance that is transferred to the reflected and transmitted waves on interface interaction. The ratios of the electric fields are instead called the **Fresnel coefficients**, and the reflectance and transmittance are their squares. Note that, since energy must be conserved, these coefficients abide by
$$R+T=1$$
as can be shown by doing the math directly.

Now, to be a little pedantic, calling $I_{R}$ and $I_{T}$ "irradiances" is *technically* wrong here because both reflected and transmitted waves are *outgoing*, not *ingoing*. Irradiance is specifically the energy flux *incident* on a surface. Flux that is exiting a surface is called **[[radiant exitance]]**[^2]. For correctness, $I_{R}$ is **reflected exitance** and $I_{T}$ is **transmitted exitance**. If you are confused at the nomenclature, don't worry, radiometry (the study of electromagnetic radiation) is confusing. I have written a [[Radiometric nomenclature survival guide]] to help.
##### Oblique incidence
Now that we have developed a theory in normal incidence, let's twist the surface a bit so that it is no longer perpendicular to the radiation. We call $\theta_{I}$ the angle of incidence, the angle between the wavevector and the surface normal. Normal incidence is when $\theta_{I}=0$. The reflected and transmitted waves then emanate at their own angles of reflection $\theta_{R}$ and transmission $\theta_{T}$ (also called angle of refraction).

Suppose we have a generic incident sine wave
$$\tilde{\mathbf{E}}_{I}(\mathbf{r},t)=\tilde{\mathbf{E}}_{0,I}e^{i(\mathbf{k}_{I}\cdot \mathbf{r}-\omega t)},\qquad \tilde{\mathbf{B}}_{I}(\mathbf{r},t)=\frac{n_{1}}{c}(\hat{\mathbf{k}}_{I}\times \tilde{\mathbf{E}}_{I})$$
which induces a reflected wave
$$\tilde{\mathbf{E}}_{R}(\mathbf{r},t)=\tilde{\mathbf{E}}_{0,R}e^{i(\mathbf{k}_{R}\cdot \mathbf{r}-\omega t)},\qquad \tilde{\mathbf{B}}_{R}(\mathbf{r},t)=\frac{n_{1}}{c}(\hat{\mathbf{k}}_{R}\times \tilde{\mathbf{E}}_{R})$$
and a transmitted wave
$$\tilde{\mathbf{E}}_{T}(\mathbf{r},t)=\tilde{\mathbf{E}}_{0,T}e^{i(\mathbf{k}_{T}\cdot \mathbf{r}-\omega t)},\qquad \tilde{\mathbf{B}}_{T}(\mathbf{r},t)=\frac{n_{2}}{c}(\hat{\mathbf{k}}_{T}\times \tilde{\mathbf{E}}_{T})$$
all at the same frequency $\omega$.

![[Diagram Oblique incidence EM wave]]

The wavevectors are all connected by
$$\frac{k_{I}}{n_{1}}=\frac{k_{R}}{n_{1}}=\frac{k_{T}}{n_{2}}=\omega \quad\Rightarrow \quad k_{I}=k_{R}=\frac{n_{1}}{n_{2}}k_{T}\tag{1}$$
These waves must obey the boundary conditions, so $\tilde{\mathbf{E}}_{I}+\tilde{\mathbf{E}}_{R}$ and $\tilde{\mathbf{B}}_{I}+\tilde{\mathbf{B}}_{R}$ must be joined with $\tilde{\mathbf{E}}_{T}$ and $\tilde{\mathbf{B}}_{T}$ in a way that satisfies the conditions. Altogether we get
$$Ae^{i(\mathbf{k}_{I}\cdot \mathbf{r}-\omega t)}+Be^{i(\mathbf{k}_{R}\cdot \mathbf{r}-\omega t)}=Ce^{i(\mathbf{k}_{T}\cdot \mathbf{r}-\omega t)}$$
where $A,B$ and $C$ are some values that we'll determine later. Right now we care about the exponentials. For this equality to be true, we need
$$A+B=C,\quad \mathbf{k}_{I}\cdot \mathbf{r}-\omega t=\mathbf{k}_{R}\cdot \mathbf{r}-\omega t =\mathbf{k}_{T}\cdot \mathbf{r}-\omega t$$

> [!quote]- Proof
> Say you have the equation $Ae^{iax}+Be^{ibx}=Ce^{ icx }$ where $A,B,C,a,b,c$ are all nonzero. For $x=0$, we have $A+B=C$. For any $x$, take the derivative
> $$iaAe^{ iax }+ibBe^{ ibx }=icCe^{ icx }$$
> Divide by $i$ to get
> $$aAe^{ iax }+bBe^{ ibx }=cCe^{icx}$$
> Notice how the right hand side is the same as the starting equation, just multiplied by $c$. So, we can say
> $$aAe^{ iax }+bBe^{ ibx }=c(Ae^{ iax }+Be^{ ibx })\quad\Rightarrow \quad (a-c)Ae^{ iax }+(b-c)Be^{ ibx }=0$$
> Since $A,B\neq 0$ and $e^{iax},e^{ ibx }$ are nonzero for all $x$, the only way this is true is if $a=b=c$.

The time-frequency part is trivially equal already and drops out, so the only part that the exponentials need to match is
$$\mathbf{k}_{I}\cdot \mathbf{r}=\mathbf{k}_{R}\cdot \mathbf{r}=\mathbf{k}_{T}\cdot \mathbf{r}\quad\text{on the surface}\tag{2}$$
Writing the components out gives us
$$yk_{I,y}+zk_{I,z}=yk_{R,y}+zk_{R,z}=yk_{T,y}+zk_{T,z}$$
where the $x$ components are zero because we are on the surface $x=0$. This is true only if the components are individually equal, so when $y=0$ we get
$$zk_{I,z}=zk_{R,z}=zk_{T,z}$$
and when $z=0$ we get
$$yk_{I,y}=yk_{R,y}=yk_{T,y}\tag{3}$$
We haven't had any specific request on the [[frame of reference]] up until now, so let's exploit this freedom to reorient the axes just so that $\mathbf{k}_{I}$ is on the $xy$ plane. This implies $k_{I,z}=0$ and so $k_{I,z}=k_{R,z}=k_{T,z}=0$, which is to say that $\mathbf{k}_{R}$ and $\mathbf{k}_{T}$ must be *coplanar* with $\mathbf{k}_{I}$, that is, lie in the same plane.

> [!info] First law of geometrical optics
> The incident, reflected and transmitted wave are coplanar. The plane they share is called the **plane of incidence**.

(Of course this is true in any frame of reference, the choice from before was just for convenience.) Since we are now on a plane, we can express the components of $\mathbf{k}$ using angles on this plane, which is precisely what $(3)$ is saying:
$$k_{I}\sin \theta_{I}=k_{R}\sin \theta_{R}=k_{T}\sin \theta_{T}$$
However, we know that $k_{I}=k_{R}$ due to $(1)$ so the sines must themselves be equal and with them, their angle:

> [!info] Second law of geometrical optics
> The angle of incidence is equal to the angle of reflection, $\theta_{I}=\theta_{R}$.

This is also known as the **[[law of reflection]]**. Since $k_{I}=k_{R}=\frac{n_{1}}{n_{2}}k_{T}$ we can also state one final law:

> [!info] Third law of geometrical optics
> The angle of incidence is tied to the angle of refraction by the ratio of refractive indexes:
> $$\frac{\sin\theta_{T}}{\sin \theta_{I}}=\frac{n_{1}}{n_{2}}$$

This is also known as **[[Snell's law]]**. These are the three laws of classical geometric optics. These have been known for a very long time, even before the rise of modern electrodynamics, and it is interesting to note how they arise spontaneously only though the wave form of Maxwell's equations. In fact, none of this derivation even really *cares* about electric or magnetic fields. The only prerequisite here is the wave equation and the quite generic boundary conditions we used, which can represent a whole host of waves, like sea waves or sound waves or what have you. In fact, these laws are essentially universal across all kinds of waves, provided you can express them as sinusoidal plane waves.

According to $(2)$, the exponential factors cancel out and we are left with the leading coefficients. These obey the boundary conditions specific to electrodynamics
$$\begin{align}
\varepsilon_{1}E_{1}^{\perp}-\varepsilon_{2}E_{2}^{\perp} & =\sigma_{f} & \mathbf{E}_{1}^{\parallel}-\mathbf{E}_{2}^{\parallel} & =\mathbf{0} \\
B_{1}^{\perp}-B_{2}^{\perp} & =0 & \frac{1}{\mu_{1}}\mathbf{B}_{1}^{\parallel}- \frac{1}{\mu_{2}}\mathbf{B}_{2}^{\parallel}&=\mathbf{0}
\end{align}$$
which using our values and our frame of reference become
$$\begin{align}
\varepsilon_{1}(\tilde{\mathbf{E}}_{0,I}+\tilde{\mathbf{E}}_{0,R})_{x}& =\varepsilon_{2}(\tilde{\mathbf{E}}_{0,T})_{x} & (\tilde{\mathbf{E}}_{0,I}+\tilde{\mathbf{E}}_{0,R})_{y,z} & =(\tilde{\mathbf{E}}_{0,T})_{y,z} \\
(\tilde{\mathbf{B}}_{0,I}+\tilde{\mathbf{B}}_{0,R})_{x} & =(\tilde{\mathbf{B}}_{0,T})_{x} & \frac{1}{\mu_{1}}(\tilde{\mathbf{B}}_{0,I}+\tilde{\mathbf{B}}_{0,R})_{y,z}&=\frac{1}{\mu_{2}}(\tilde{\mathbf{B}}_{0,T})_{y,z}
\end{align}$$
Suppose that the incident wave is polarized parallel to the plane of incidence. Then, the reflected and transmitted waves must themselves be polarized in the same plane[^3]. In this case, we get
$$\begin{align}
\varepsilon_{1}(-\tilde{E}_{0,I}\sin \theta_{I}+\tilde{E}_{0,R}\sin \theta_{R}) & =\varepsilon_{2}(-\tilde{E}_{0,T}\sin \theta_{T}) & \tilde{E}_{0,I}\cos \theta_{I}+\tilde{E}_{0,R}\cos \theta_{R} & =\tilde{E}_{0,T}\cos \theta_{T} \\
0 & =0 & \frac{n_{1}}{\mu_{1}}(\tilde{E}_{0,I}+\tilde{E}_{0,R})&=\frac{n_{2}}{\mu_{2}}\tilde{E}_{0,T}
\end{align}$$
Using the law of reflection and Snell's law, top left and bottom right both become
$$\tilde{E}_{0,I}-\tilde{E}_{0,R}=\beta \tilde{E}_{0,T}$$
where $\beta=\mu_{1}n_{2}/\mu_{2}n_{1}$. Meanwhile, top right becomes
$$\tilde{E}_{0,I}+\tilde{E}_{0,R}=\alpha \tilde{E}_{0,T}$$
where $\alpha=\cos \theta_{T}/\cos \theta_{I}$. Solving these to express the amplitudes in terms of $\tilde{E}_{0,I}$ yields
$$\boxed{\tilde{E}_{0,R}=\left( \frac{\alpha-\beta}{\alpha+\beta} \right)\tilde{E}_{0,I},\qquad \tilde{E}_{0,T}=\left( \frac{2}{\alpha+\beta} \right)\tilde{E}_{0,I}}$$
These are known as **[[Fresnel's equations]]** for polarization in the plane of incidence. There are two more, for polarization perpendicular to the plane of incidence. From the sign of the coefficients, we can see that the transmitted wave must always be in [[phase]] with the incident one (since $2/(\alpha+\beta)>0$), but the reflected may or may not be depending on the sign of $\alpha-\beta$. If $\alpha>\beta$, then it is in phase, otherwise it is out of phase by precisely half a cycle (it's "upside down") since changing the sign of the amplitude in a sine wave is like shift by half a cycle ($\pi$ or 180°). Of course, if set $\theta_{I}=0$, then $\alpha=1$ and we get the equations we found in the normal incidence case.

Note how since $\cos \theta_{I}$ is at the denominator in $\alpha$, if $\theta_{I}$ approaches $\pi/2$ (or 90°), the $\cos \theta_{I}$ approaches zero and $\alpha$ diverges. In that case, the coefficient on the transmitted wave collapses to zero and only the reflected wave remains: this is called **total reflection** and you can pretty easily experience it yourself by taking any partially reflective object and rotating it while under a light. Eventually, you'll see nothing but reflected light.

Curiously, there is another angle worth discussing. When $\alpha=\beta$, we get
$$\sin ^{2}\theta_{B}=\frac{1-\beta ^{2}}{\left( n_{1}/n_{2}\right)^{2}-\beta ^{2}}$$
In most materials, $\mu_{1}\simeq \mu_{2}$, so $\beta \simeq n_{2}/n_{1}$ and this simplifies down to
$$\tan \theta_{B}\simeq \frac{n_{2}}{n_{1}}\quad\Rightarrow \quad \theta_{B}\simeq\arctan\left( \frac{n_{2}}{n_{1}} \right)$$
This angle is known as **[[Brewster's angle]]** and it is special because here, the reflected wave is fully extinguished. This is the other half of the medal: at 90°, the transmitted wave vanishes, and at Brewster's angle, the reflected wave vanishes.

:::image
![[Plot Amplitudes in EM wave incidence.png|500]]
A plot of the real amplitudes ratios of incident, reflected an transmitted waves with respect to the incidence angle. Negative values imply an out-of-phase wave; the amplitude itself is the absolute value.
From *Introduction to Electrodynamics 4th ed., Griffiths*.
:::

Actually, there is yet *another* interesting angle to talk about, although it is not universal. When a wave moves from an "optically dense" material (say, water) to an "optically thin" one (say, air), that is $n_{1}>n_{2}$, the transmitted wavevector tends to move away form the normal and towards the being flush with the interface. This isn't asymptotic: the wavevector becomes exactly parallel with the surface ($\theta_{T}=\pi/2$ or 90°) at the **critical angle**
$$\theta_{C}\equiv \arcsin\left( \frac{n_{2}}{n_{1}} \right)$$
by using Snell's law. Incidence at any angle greater than the critical one ($\theta_{I}>\theta_{C}$) and *there is no transmission*, just like normally when reaching 90°. Since air is quite optically thin, this typically happens when a ray of light attempts to leave a material (almost certainly optically denser) and move into the air. As such, in some conditions, it's possible that a ray of light might remain "trapped" inside the material if it only ever bounces at angles greater than the critical one. This is the idea behind **total internal reflection**, a technique used to transfer light beams from one place to another without energy loss by making sure all internal incidence is at an angle greater than critical (if you have fiber optics somewhere in your house, this is how they work).

This said, while the wave is fully reflected, the fields are actually *not* zero in material 2. They form a so-called **[[evanescent wave]]**, a wave that attenuates extremely rapidly and transports no energy into material 2. It can be constructed by setting $k_{T}=\omega n_{2}/c$ and $\mathbf{k}_{T}=k_{T}(\sin \theta_{T}\ \hat{\mathbf{y}}+\cos \theta_{T}\ \hat{\mathbf{z}})$. This causes Snell's law
$$\sin \theta_{T}=\frac{n_{1}}{n_{2}}\sin \theta_{I}$$
to report an *imaginary* transmission angle when $\theta_{I}>\theta_{C}$. Of course, it no longer makes sense as an angle (at least a real one).

:::image
![[DenseToThinEMWaveReflection.svg]]
By Josell7 - Own work, CC BY-SA 3.0, from [Wikipedia](https://commons.wikimedia.org/w/index.php?curid=21670922).
:::

Finally, we close this off with the irradiance of the incident wave is
$$\boxed{I_{I}=\langle \mathbf{S} \rangle\cdot \hat{\mathbf{x}}=\frac{\varepsilon_{1}c}{2n_{1}}E_{0,I}^{2}\cos \theta_{I}}$$
and the reflected and transmitted exitances
$$\boxed{I_{R}=\frac{\varepsilon_{1}c}{2n_{1}}E_{0,I}^{2}\cos \theta_{R},\qquad I_{R}=\frac{\varepsilon_{2}c}{2n_{2}}E_{0,I}^{2}\cos \theta_{T}}$$
The reflectance and transmittance hence end up as
$$\boxed{R=\frac{I_{R}}{I_{I}}=\left( \frac{\alpha-\beta}{\alpha+\beta} \right)^{2},\qquad T=\frac{I_{T}}{I_{I}}=\alpha \beta\left( \frac{2}{\alpha+\beta} \right)^{2}}$$
### In conductors
Now that we're done with dielectrics, we move on to [[conductor|conductors]]. Maxwell's wave equations for conductors are
$$\nabla ^{2}\mathbf{E}=\varepsilon \mu \frac{ \partial ^{2}\mathbf{E} }{ \partial t^{2} }+\mu \sigma \frac{ \partial \mathbf{E} }{ \partial t },\qquad\nabla ^{2}\mathbf{B}=\varepsilon \mu \frac{ \partial ^{2}\mathbf{B} }{ \partial t^{2} }+\mu \sigma \frac{ \partial \mathbf{B} }{ \partial t }$$
They differ by having an additional first derivative in time on top of the second derivative. These are no longer the standard wave equation we've gotten used to and are in fact a generalization of it. Nevertheless, they still admit plane wave solutions, so that's what we'll follow through with:
$$\tilde{\mathbf{E}}(z,t)=\tilde{\mathbf{E}}_{0}e^{i(\tilde{k}z-\omega t)},\qquad \tilde{\mathbf{B}}(z,t)=\tilde{\mathbf{B}}_{0}e^{i(\tilde{k}z-\omega t)}$$
You'll notice an unfamiliar tilde over the $k$: this is because in order for a plane wave to satisfy one of these equations, it must have a *complex* wavenumber. Before moving on, we should probably investigate this odd quantity further.

Substituting the plane wave, our wave equations become (we'll use the electric field, but the magnetic field is identical):
$$\nabla ^{2}\mathbf{E}=\nabla ^{2}[\mathbf{E}_{0}e^{i(\tilde{k}z-\omega t)}]=-\tilde{k}^{2}\mathbf{E}$$
Be careful with $\tilde{k}^{2}$! It's a complex value, not a real one, so the square is a little more complicated. When plugging this Laplacian in, the wave equation enforces
$$\tilde{k}^{2}=\mu \varepsilon \omega ^{2}+i\mu \sigma \omega$$
We'll split the real and imaginary parts:
$$\tilde{k}=k+i\kappa$$
so that the square is
$$\tilde{k}^{2}=(k+i\kappa)(k-i\kappa)=k^{2}+2ik\kappa-\kappa ^{2}$$
We now have two results for $\tilde{k}^{2}$ that we can compare to get:
$$k^{2}+2ik\kappa-\kappa ^{2}=\mu \varepsilon \omega ^{2}+i\mu \sigma \omega$$
This can equivalently be shown as
$$\begin{cases}
k^{2}-\kappa ^{2}=\mu \varepsilon \omega ^{2} \\
2k\kappa=\mu \sigma \omega
\end{cases}\quad\to \quad\begin{cases}
(k+\kappa)(k-\kappa)=\mu \varepsilon \omega ^{2} \\
\kappa=\frac{\mu \sigma \omega}{2k}
\end{cases}$$
The real and imaginary wavenumbers end up being
$$
\boxed{k=\omega \sqrt{ \frac{\varepsilon \mu}{2} }\sqrt{ \sqrt{ 1+\left( \frac{\sigma}{\omega \varepsilon} \right)^{2} }+1 },\qquad \kappa=\omega \sqrt{ \frac{\varepsilon \mu}{2} }\sqrt{ \sqrt{ 1+\left( \frac{\sigma}{\omega \varepsilon} \right)^{2} }-1 }}\tag{4}
$$
(The only difference between the two is the plus or minus at the end). These are significant results for a couple of reasons, especially the imaginary part. In fact, if we go back to the oscillating fields
$$\mathbf{E}(x,t)=\mathbf{E}_{0}e^{i[(k+i\kappa)x-\omega t]}=\mathbf{E}_{0}e^{i(kx-\omega t)}e^{-\kappa x}\tag{5}$$
(the same goes for $\mathbf{B}$). We have the usual plane wave with a *real* wavenumber $k$, but now it's weighed by $e^{-\kappa x}$. Specifically, this term says that as $x$ grows larger (i.e. the wave propagates), it is *suppressed*, with a larger $\kappa$ incurring a more significant suppression; this phenomenon is known as the **skin effect**:

> [!info] Skin effect
> An electromagnetic wave incident on a conductor gets suppressed in the direction in propagates in. The distance it takes for the [[Wave equation|amplitude]] to be reduced by a factor of $1/e$ is called the **skin depth** $d\equiv 1/\kappa$.

$1/e$ is qualitatively around one third, so the wave's amplitude cuts down by a third every skin depth. This leads to a very fast suppression of the wave, doubly so since skin depths are typically very small, generally millimeters or fractions of millimeters. Lower frequencies have higher skin depths and viceversa[^4].

Moreover, we see that the wavevector is dependent on $\omega$ multiplied by a factor made up of $\varepsilon$, $\mu$ and $\sigma$. These three parameters determine the materials behavior against incoming electromagnetic waves. You could consider them constants, but you'd be slightly wrong. These are actually measured to be mildly *frequency-dependent*: $\varepsilon\equiv \varepsilon(\omega)$, $\mu\equiv \mu(\omega)$ and $\sigma\equiv \sigma(\omega)$. As such, $\tilde{k}$ is *nonlinearly* dependent on $\omega$. This leads to a phenomenon known as **[[dispersion]]**, which occurs when the [[phase velocity]] of the wave in the material is dependent on the frequency, $v_{p}\equiv v_{p}(\omega)$. The relation $k\equiv k(\omega)$ is called the **dispersion relation**. In our case, since $v_{p}=c/n$, this is like saying that dispersion occurs when the refractive index depends on frequency, $n\equiv n(\omega)$.

Equation $(5)$ is universally correct for the conductor wave equations. Maxwell's equations impose further constraints on which waves are permitted; this is the same argument as in the beginning of [[#In the vacuum]]. Assuming the wave propagates on $x$, due to $\nabla\cdot \mathbf{E}=0$ and $\nabla\cdot \mathbf{B}=0$, there can be no $x$ component to the fields. Similarly, using the curls we get that the fields are perpendicular to each other at all times. For instance, setting the electric field as polarized over $\hat{\mathbf{y}}$ and using its curl we find
$$\tilde{\mathbf{E}}(x,t)=\tilde{E}_{0}e^{i(kx-\omega t)}e^{-\kappa x}\hat{\mathbf{y}},\qquad \tilde{\mathbf{B}}(x,t)=\frac{\tilde{k}}{\omega}\tilde{E}_{0}e^{i(kx-\omega t)}e^{-\kappa x}\hat{\mathbf{z}}\tag{6}$$
We can further analyze the complex wavenumber $\tilde{k}$ by expressing it in polar form:
$$\tilde{k}=\lvert \tilde{k} \rvert e^{i\phi}=Ke^{i\phi}$$
The modulus is
$$K=\sqrt{ k^{2}+\kappa ^{2} }=\omega \sqrt{ \varepsilon \mu \sqrt{ 1+\left( \frac{\sigma}{\varepsilon \omega} \right)^{2} } }$$
and the angle is
$$\phi=\arctan\left( \frac{\kappa}{k} \right)$$
Using $(6)$, we see that the complex amplitudes $\tilde{E}_{0}=E_{0}e^{i\delta_{E}}$ and $\tilde{B}_{0}=B_{0}e^{i\delta_{B}}$ are related by
$$\tilde{B}_{0}=\frac{\tilde{k}\tilde{E}_{0}}{\omega}\quad\to \quad B_{0}e^{i\delta_{B}}=\frac{Ke^{i\phi}}{\omega}E_{0}e^{i\delta_{E}}=\frac{KE_{0}}{\omega}e^{i(\delta_{E}+\phi)}$$
Evidently, the phase is shifted by an angle $\phi$ determined by the wavevector and the fields are no longer in phase by precisely this angle: $\delta_{B}-\delta_{E}=\phi$. Specifically, the magnetic field is lagging behind the electric one.

:::hidden
The real amplitudes $E_{0}$ and $B_{0}$ are instead related by
$$\frac{B_{0}}{E_{0}}=\frac{K}{\omega}=\sqrt{ \varepsilon \mu \sqrt{ 1+\left( \frac{\sigma}{\varepsilon \omega} \right)^{2} } }$$
This can also be written as
$$B_{0}=\frac{E_{0}}{\omega}K=\frac{nE_{0}}{c}$$
Inverting the equation, we get
$$n=\frac{c}{\omega}K=\sqrt{ n_{re}^{2}+n_{im}^{2} }$$
where $n_{re}$ and $n_{im}$ are the real and imaginary parts of a **complex refractive index** $\tilde{n}$ defined as $\tilde{n}=n_{re}+in_{im}$. The parts are $n_{re}=ck/\omega$ and $n_{im}=c\kappa/\omega$.
:::

The real parts of waves incident on a conductor are
$$\boxed{\mathbf{E}(x,t)=E_{0}e^{-\kappa x}\cos(kx-\omega t+\delta_{E})\hat{\mathbf{y}},\qquad \mathbf{B}(x,t)=B_{0}e^{-\kappa x}\cos(kx-\omega t+\delta_{E}+\phi)\hat{\mathbf{z}}}$$
The irradiance can be found to be
$$I\propto \langle E^{2} \rangle _{T}=\frac{E_{0}^{2}}{2}e^{-2\kappa t}$$
where $\langle E^{2} \rangle_{T}$ is the time average over a period $T$, and
$$I(x)=\frac{k}{2\mu \omega}e^{-2\kappa x}=\frac{k}{2\mu \omega}e^{-x/\alpha}$$
$\alpha=1/2\kappa$ is the called the **penetration depth** of the wave. It is the characteristic length of suppression of irradiance when moving through a conductor; it's basically the skin depth of irradiance. Just like skin depth, it is usually less than or a few millimeters. For UV waves on a typical conductor, it's around $0.6\text{ mm}$ and for infrared waves, it's about $6\text{ mm}$.
#### Interface reflection and transmission
Like all surfaces, an electromagnetic wave can be reflected by a conducting surface too. Unlike dielectrics however, conductors show some remarkable behavior due to their near-immediate reallocation of charge. The boundary conditions of a conductor are the general ones
$$\begin{align}
\varepsilon_{1}E_{1}^{\perp}-\varepsilon_{2}E_{2}^{\perp} & =\sigma_{f} & \mathbf{E}_{1}^{\parallel}-\mathbf{E}_{2}^{\parallel} & =\mathbf{0} \\
B_{1}^{\perp}-B_{2}^{\perp} & =0 & \frac{1}{\mu_{1}}\mathbf{B}_{1}^{\parallel}- \frac{1}{\mu_{2}}\mathbf{B}_{2}^{\parallel}&=\mathbf{K}_{f}\times \hat{\mathbf{n}}
\end{align}$$
since we cannot arbitrarily choose for $\sigma_{f}$ and $\mathbf{K}_{f}$ to be zero (don't confuse $\sigma_{f}$, free surface charge, with $\sigma$, conductivity, and $\hat{\mathbf{n}}$, the surface normal, with the polarization vector!).

We'll work with ohmic conductors. These work with Ohm's law $\mathbf{J}_{f}=\sigma \mathbf{E}$ and therefore implies $\mathbf{K}_{f}=0$ since if if were nonzero, we'd need an infinite electric current at the boundary. In fact, consider a slice of infinitesimal thickness $l$ of the material right on the surface. The surface current is approximately $\mathbf{K}_{f}=\mathbf{J}_{f}l=\sigma l\mathbf{E}$. For this to be exact we need $l\to 0$, which implies $\mathbf{K}_{f}\to 0$ unless $\mathbf{E}\to \infty$, which is of course unphysical, so $\mathbf{K}_{f}=0$.
##### Normal incidence
We start by investigating normal incidence, $\theta_{I}=0$. As usual, we pick a wave traveling forwards on $\hat{\mathbf{x}}$ with the conductor's surface on the $yz$ plane. We polarize the wave on $\hat{\mathbf{y}}$. The coupled fields are
$$\tilde{\mathbf{E}}_{I}(x,t)=\tilde{E}_{0,I}e^{i(k_{1}x-\omega t)}\hat{\mathbf{y}},\qquad \tilde{\mathbf{B}}_{I}(x,t)=\frac{n_{1}}{c} \tilde{E}_{0,I}e^{i(k_{1}x-\omega t)}\hat{\mathbf{z}}$$
The reflected wave will be
$$\tilde{\mathbf{E}}_{R}(x,t)=\tilde{E}_{0,R}e^{i(-k_{1}x-\omega t)}\hat{\mathbf{y}},\qquad \tilde{\mathbf{B}}_{R}(x,t)=-\frac{n_{1}}{c} \tilde{E}_{0,R}e^{i(-k_{1}x-\omega t)}\hat{\mathbf{z}}$$
and the transmitted one
$$\tilde{\mathbf{E}}_{T}(x,t)=\tilde{E}_{0,T}e^{i(\tilde{k}_{2}x-\omega t)}\hat{\mathbf{y}},\qquad \tilde{\mathbf{B}}_{T}(x,t)=\frac{\tilde{k}_{2}}{\omega} \tilde{E}_{0,T}e^{i(\tilde{k}_{2}x-\omega t)}\hat{\mathbf{z}}$$
The complex wavevector $\tilde{k}_{2}$ denotes the attenuation of the wave. At $x=0$, the waves must abide by the boundary conditions. $E^{\perp}=0$ on both sides since we are at normal incidence, which implies $\rho_{f}=0$ by the top left condition. Top right becomes
$$\tilde{E}_{0,I}+\tilde{E}_{0,R}=\tilde{E}_{0,T}$$
$B^{\perp}=0$ is also true on both sides for the same reason, so bottom left becomes trivial. Bottom right becomes
$$\frac{n_{1}}{\mu_{1}c}(\tilde{E}_{0,I}-\tilde{E}_{0,R})- \frac{\tilde{k}_{2}}{\mu_{2}\omega}\tilde{E}_{0,T}=0$$
or, if we define
$$\tilde{\beta}\equiv \frac{\mu_{1}c}{\mu_{2}n_{2}\omega}\tilde{k}_{2}$$
we get
$$\tilde{E}_{0,I}-\tilde{E}_{0,R}=\tilde{\beta}\tilde{E}_{0,T}$$
Solving these yields
$$\boxed{\tilde{E}_{0,R}=\left( \frac{1-\tilde{\beta}}{1+\tilde{\beta}} \right)\tilde{E}_{0,I},\qquad \tilde{E}_{0,T}=\left( \frac{2}{1+\tilde{\beta}} \right)\tilde{E}_{0,I}}$$
The coefficients maintain the same shape as the dielectric case, but the $\beta$ parameter is now *complex* to take the attenuation into account. In case of a perfect conductor, $\sigma=\infty$, so $k_{2}=\kappa_{2}=\infty$ using $(4)$, so $\tilde{\beta}=\infty$ (in the complex sense). In this case we get
$$\tilde{E}_{0,R}=-\tilde{E}_{0,I},\qquad \tilde{E}_{0,T}=0$$
The wave is totally reflected with an accompanying 180° phase flip. In other words, the conductor is a perfect mirror. If you've ever wondered why metal is so shiny, this is why!

:::hidden
As with previous reflection/transmission analysis, we invoke the Fresnel coefficients $r_{\perp}$ and $r_{\parallel}$. In this scenario, we have
$$[r_{\parallel}]_{\theta_{I}=0}=[r_{\perp}]_{\theta_{I}=0}=\frac{n_{2}-n_{1}}{n_{2}+n_{1}}$$
where $2$ and $1$ denote the indexes of the outer and inner materials respectively. The reflection coefficient is
$$R=\lvert \tilde{r} \rvert ^{2}=\left( \frac{\tilde{n}-1}{\tilde{n}+1} \right)^{*}\left( \frac{\tilde{n}-1}{\tilde{n}+1} \right)=\frac{(n_{re}-1)^{2}+n_{im}^{2}}{(n_{re}+1)^{2}+n_{im}^{2}}$$
Remember that $n_{re}$ and $n_{im}$ are related to $k$ and $\kappa$ as found above. For a perfect conductor, where $\sigma\to \infty$, the imaginary component becomes massive, $n_{im}\gg n_{re}$. This means that $\kappa\gg k$, and that's exactly what we want: the higher $\kappa$ is, them more the transmitted wave is suppressed, leaving only the reflection. For a terrible conductor (i.e. a perfect [[dielectric]]), where $\sigma\to0$, the opposite happens. $n_{im}=0$ and $n_{re}=c/v$. There is no suppression at all: it's just a normal, undamped plane wave.

An important detail to notice is that, since $k$ and $\kappa$ are both dependent on $\omega$ and so are $n_{re}$ and $n_{im}$. In other words, the reflection/transmission angle (and coefficients) in conductors is dependent on the wavelength or frequency of the wave. This is one case of a broader phenomenon known as **[[dispersion]]**.
:::

[^1]: The magnetic's field contribution being entirely determined by the electric field is a recurring theme in electrodynamics and it is no coincidence. However, the explanation must wait until relativistic electrodynamics to make any semblance of sense (but if you're eager, see [[Magnetism as a relativistic phenomenon]]).

[^2]: It's just a matter of perspective. The units of measurements are still the same ($\text{W/m}^{2}$). Many authors don't even bother and call all of these "intensity" anyway, but that's unnecessarily confusing.

[^3]: This can be proven by setting the new polarizations as $\hat{\mathbf{n}}_{R}=\cos \theta_{R}\hat{\mathbf{y}}+\sin \theta_{R}\hat{\mathbf{z}}$ and $\hat{\mathbf{n}}_{T}=\cos \theta_{T}\hat{\mathbf{y}}+\sin \theta_{T}\hat{\mathbf{z}}$ and applying boundary conditions to see that $\theta_{T}=\theta_{R}=0$.

[^4]: This should not be confused with an [[evanescent wave]], which is instead suppressed *perpendicularly* to the direction it propagates.