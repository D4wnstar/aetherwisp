---
wiki-publish: true
aliases:
  - skin depth
  - skin effect
---
A **conductor** is a material that contains a large (ideally infinite) number of free [[electric charge|electric charges]], typically [[Elettrone|electrons]] or [[ione|ions]].
### Properties
Conductors have special characteristic properties:
1. The [[electric field]] $\mathbf{E}$ is zero inside the conductor.
2. The volume charge density $\rho$ is zero inside the conductor.
3. Any net charge resides on the surface[^1].
4. A conductor is an equipotential volume, meaning the [[electric potential]] is the same for any two points inside or on the surface of the conductor.
5. The electric field is perpendicular to the surface at any point on the surface.
#### Explanation
When an external electric field $\mathbf{E}_{0}$ is applied to the conductor, the positive and negative charges that comprise it move towards or away from the field. This means there is a surplus of positive charges on one side of the material and a surplus of negative ones on the other. These excesses then produce what's called an **induced charge**, making the two sides of the material positively and negatively charged overall. These charges cause an electric field $\mathbf{E}_{1}$ to occur whose direction is exactly opposite that of $\mathbf{E}_{0}$. The magnitude of both is also identical, as $\mathbf{E}_{1}$ depends on the displacement of the charges, which itself depends on $\mathbf{E}_{0}$. This means that $\mathbf{E}_{0}$ and $\mathbf{E}_{1}$ cancel each other out within the material, leading to a net neutral zone inside (property 1). Outside, however, the field is nonzero. This adaptive nature of conductors applies for any field almost instantly, leading to a "response" field $\mathbf{E}_{1}$ that follows $\mathbf{E}_{0}$ perfectly.

Using [[Gauss' law]], we have $\nabla\cdot\mathbf{E}=\rho/\varepsilon_{0}$, so if $\mathbf{E}$ is zero inside, so is $\rho$ (property 2). Since charges cannot be created or destroyed and cannot stay on the inside, they must "migrate" to the surface, leading to a surface charge distribution (property 3). In fact, this can be seen as a consequence of the [[least action principle]], as the energy of the system needs to be at its lowest for the system to come to rest. As it happens the electrostatic energy of a solid is always lowest when all charge is distributed at the boundary surface, when keeping charge and shape constant.

The electric field is given by $\mathbf{E}=-\nabla V$, so if $\mathbf{E}=0$ then $V$ must be a constant (property 4).

Any component $\mathbf{E}$ not perpendicular to the surface would cause a shift in the underlying charges for the same reasons an outside field does, meaning that charges reassess constantly in such a way that any tangential component $\mathbf{E}$ is removed (property 5).
### Cavity and internal charges
Say you have a solid conductor with a hollow cavity dug out in it. Say, then, you place a charge within the cavity. The electric field within the cavity will not be zero, but outside of the cavity it will be entirely nullified, similarly to an external field. This implies that the internal charge is completely isolated from the outside world and viceversa.

That said, the charge still has an effect on the interior surface of the cavity, as it forces the charges of the solid to be aligned in such a way that they nullify the internal field. This has a repercussions on the outer surface too, which will be charged in the opposite manner as the inner one for balance and thus communicate the presence of an internal charge to an outside observer. The charge on the inner surface is equal and opposite to the cavity charge, as a consequence of Gauss' law. The charge on the outer surface must be equal and opposite to the inner surface charge, which means equal to the cavity charge. So for a charge $q$ it goes
$$+q_\text{cavity} \to -q_\text{inner surface} \to +q_\text{outer surface}$$
### Surface force and pressure
We can find the force applied to a charge on the surface by taking the average of the internal and external fields. In a conductor, the internal field is always zero, so the result is very simple:
$$\mathbf{E}_\text{avg}=\frac{\mathbf{E}_\text{above}}{2}$$
so the force per unit area is
$$\mathbf{f}=\frac{\sigma}{2}\mathbf{E}_\text{above}=\frac{\sigma^{2}}{2\varepsilon_{0}}\hat{\mathbf{n}}$$
where we used the fact that the discontinuity of the field over a surface is always $(\sigma/\varepsilon_{0})\hat{\mathbf{n}}$. This amounts to an outwards [[electrostatic pressure]] on the surface, tending to draw the conductor into the field, regardless of the sign of $\sigma$. Just outside the surface, the pressure is
$$P=\frac{\varepsilon_{0}}{2}E^{2}$$
### Maxwell's equations
(Derivation goes here)

In conductors, the [[Electric current|continuity equation]] and [[Ohm's law]] can be used to rewrite [[Maxwell's equations]] in a form specific to conductors. They read
$$\begin{align}
\nabla\cdot\mathbf{E} & =0 &
\nabla\times\mathbf{E} & = -\frac{ \partial \mathbf{B} }{ \partial t } \\
\nabla\cdot\mathbf{B} & =0 &
\nabla\times\mathbf{B} &=\mu\sigma \mathbf{E} +\mu \sigma \frac{ \partial \mathbf{E} }{ \partial t } 
\end{align}$$
#### As electromagnetic waves
Like the general case, we can rewrite these equations to find a [[Wave equation]] for [[electromagnetic wave|electromagnetic waves]]. To do so, we use the usual vector calculus methods:
$$\begin{align}
\nabla \times(\nabla\times\mathbf{E})&=-\nabla\times \frac{ \partial \mathbf{B} }{ \partial t } =-\frac{ \partial  }{ \partial t } (\nabla\times \mathbf{B})=-\frac{ \partial  }{ \partial t } \left( \varepsilon \mu \frac{ \partial \mathbf{E} }{ \partial t } +\mu \sigma \mathbf{E} \right) \\
&=-\varepsilon \mu \frac{ \partial ^{2}\mathbf{E} }{ \partial t^{2} } -\mu \sigma \frac{ \partial \mathbf{E} }{ \partial t }
\end{align} $$
from which
$$\nabla ^{2}\mathbf{E}=\varepsilon \mu \frac{ \partial ^{2}\mathbf{E} }{ \partial t^{2} }+\mu \sigma \frac{ \partial \mathbf{E} }{ \partial t }  \tag{1}$$
Meanwhile, $\nabla\times(\nabla\times \mathbf{B})$ leads to
$$\nabla ^{2}\mathbf{B}=\varepsilon \mu \frac{ \partial ^{2}\mathbf{B} }{ \partial t^{2} } +\mu \sigma \frac{ \partial \mathbf{B} }{ \partial t } \tag{2}$$
Unlike the vacuum case, there's a new term dependent on the *first* derivative of time. If the typical electromagnetic wave equation was analogous to the [[harmonic oscillator]], this is analogous to a *dampened* harmonic oscillator: the conductor counteracts the wave and suppresses it.

Solving these equations is (unsurprisingly) more difficult than the vacuum counterpart. That said, the equation still admits a [[Plane wave]] solutions. The usual method of finding the physics here is to introduce *complex* electric and magnetic fields:
$$\mathbf{E}(z,t)=\mathbf{E}_{0}e^{i(\tilde{k}z-\omega t)},\qquad \mathbf{B}(z,t)=\mathbf{B}_{0}e^{i(\tilde{k}z-\omega t)}$$
where $\mathbf{E}_{0}$, $\mathbf{B}_{0}$ and $\tilde{k}$ are complex constants, $\tilde{k}$ is the (complex) [[Wavenumber]] and $\omega$ is the [[Frequency|angular frequency]]. These are the plane waves that solve the equation. Our task is now to find what these actually mean.

With these definitions, our wave equations become (here using the electric field):
$$\nabla ^{2}\mathbf{E}=\nabla ^{2}[\mathbf{E}_{0}e^{i(\tilde{k}z-\omega t)}]=-\tilde{k}^{2}\mathbf{E}$$
Be careful with $\tilde{k}^{2}$! It's a complex value, not a real one, so the square is a little more complicated. The above equation solves to $\tilde{k}^{2}=\mu \varepsilon \omega ^{2}+i\mu \sigma \omega$. Remember that $\tilde{k}$ is complex, so we can split the real and imaginary parts:
$$\tilde{k}=k+i\kappa$$
and the square then is
$$\tilde{k}^{2}=(k+i\kappa)(k-i\kappa)=k^{2}+2ik\kappa-\kappa ^{2}$$
We now equate the two results for $\tilde{k}^{2}$ to get:
$$k^{2}+2ik\kappa-\kappa ^{2}=\mu \varepsilon \omega ^{2}+i\mu \sigma \omega$$
This can be equivalently shown as
$$\begin{cases}
k^{2}-\kappa ^{2}=\mu \varepsilon \omega ^{2} \\
2k\kappa=\mu \sigma \omega
\end{cases}\quad\to \quad\begin{cases}
(k+\kappa)(k-\kappa)=\mu \varepsilon \omega ^{2} \\
\kappa=\frac{\mu \sigma \omega}{2k}
\end{cases}\quad\to\ldots$$
The real and imaginary wavenumbers end up being
$$
\boxed{k=\omega \sqrt{ \frac{\varepsilon \mu}{2} }\sqrt{ \sqrt{ 1+\left( \frac{\sigma}{\omega \varepsilon} \right)^{2} }+1 },\qquad \kappa=\omega \sqrt{ \frac{\varepsilon \mu}{2} }\sqrt{ \sqrt{ 1+\left( \frac{\sigma}{\omega \varepsilon} \right)^{2} }-1 }}
$$
These are significant results, especially the imaginary part. In fact, if we go back to the oscillating fields
$$\mathbf{E}(z,t)=\mathbf{E}_{0}e^{i[(k+i\kappa)]z-\omega t}=\mathbf{E}_{0}e^{i(kz-\omega t)}e^{-\kappa z}\tag{3}$$
(the same goes for $\mathbf{B}$). We have the usual plane wave with a *real* wavenumber $k$, but now it's weighed by $e^{-\kappa z}$. Specifically, this term says that as $z$ grows larger (i.e. the wave propagates), the more suppressed it becomes, with a larger $\kappa$ incurring a more significant suppression; this phenomenon is known as the **skin effect**. Thus, the conclusion must be the following:

> [!success] Electromagnetic waves in conductors
> An electromagnetic wave incident on a conductor gets suppressed in the direction in propagates in. The distance it takes for the [[Wave equation|amplitude]] to be reduced by a factor of $1/e$ is called the **skin depth** $d\equiv 1/\kappa$.

$1/e$ is qualitatively around one third, so the wave's amplitude cuts down by a third every skin depth. This leads to a very fast suppression of the wave, doubly so since skin depths are typically very small, generally millimeters or fractions of millimeters. Lower frequencies have higher skin depths and viceversa.

This should not be confused with an [[evanescent wave]], which is instead suppressed *perpendicularly* to the direction it propagates.

The solution $(3)$ is universally correct for equation $(1)$ (equation $(2)$ is solved by the magnetic counterpart where $\mathbf{E}\to \mathbf{B}$). Maxwell's equations impose further constraints on which waves are permitted: assuming the wave propagates on $z$, due to $\nabla\cdot \mathbf{E}=0$ and $\nabla\cdot \mathbf{B}=0$, there can be no $z$ component to the fields. Similarly, using the curls we get that the fields are perpendicular to each other at all times. For instance, setting the electric field as polarized over $\hat{\mathbf{x}}$ and using its curl we find
$$\tilde{\mathbf{E}}(z,t)=\tilde{E}_{0}e^{i(kz-\omega t)}e^{-\kappa z}\hat{\mathbf{x}},\qquad \tilde{\mathbf{B}}(z,t)=\frac{\tilde{k}}{\omega}\tilde{E}_{0}e^{i(kz-\omega t)}e^{-\kappa z}\hat{\mathbf{y}}\tag{4}$$

We can further analyze the wavenumber $\tilde{k}$ by expressing it in polar form:
$$\tilde{k}=\lvert \tilde{k} \rvert e^{i\phi}=Ke^{i\phi}$$
The modulus is
$$K=\sqrt{ k^{2}+\kappa ^{2} }=\omega \sqrt{ \varepsilon \mu \sqrt{ 1+\left( \frac{\sigma}{\varepsilon \omega} \right)^{2} } }$$
and the angle is
$$\phi=\arctan\left( \frac{\kappa}{k} \right)$$
Using $(4)$, we see that the complex amplitudes $\tilde{E}_{0}=E_{0}e^{i\delta_{E}}$ and $\tilde{B}_{0}=B_{0}e^{i\delta_{B}}$ are related by
$$\tilde{B}_{0}=\frac{\tilde{k}\tilde{E}_{0}}{\omega}\quad\to \quad B_{0}e^{i\delta_{B}}=\frac{Ke^{i\phi}}{\omega}E_{0}e^{i\delta_{E}}=\frac{KE_{0}}{\omega}e^{i(\delta_{E}+\phi)}$$
Evidently, the phase shifted by $\phi$ and the fields are no longer in phase: $\delta_{B}-\delta_{E}=\phi$. Specifically, the magnetic field is lagging behind the electric one by an angle $\phi$.

The real amplitudes $E_{0}$ and $B_{0}$ are instead related by
$$\frac{B_{0}}{E_{0}}=\frac{K}{\omega}=\sqrt{ \varepsilon \mu \sqrt{ 1+\left( \frac{\sigma}{\varepsilon \omega} \right)^{2} } }$$
This can also be written as
$$B_{0}=\frac{E_{0}}{\omega}K=\frac{E_{0}}{v}=\frac{nE_{0}}{c}$$
where $v$ is the speed of propagation, $n$ is the [[refractive index]] and $c$ is the [[speed of light]]. Inverting the equation, we get
$$n=\frac{c}{\omega}K=\sqrt{ n_{R}^{2}+n_{I}^{2} }$$
where $n_{R}$ and $n_{I}$ are the real and imaginary parts of a complex refractive index $\tilde{n}$ defined as $\tilde{n}=n_{R}+in_{I}$. Each part is $n_{R}=ck/\omega$ and $n_{I}=c\kappa/\omega$.
#### Irradiance
The [[irradiance]] of an electromagnetic wave on a conductor can be found to be
$$I\propto \langle E^{2} \rangle _{T}=\frac{E_{0}^{2}}{2}e^{-2\kappa t}$$
where $\langle E^{2} \rangle_{T}$ is the time average over a [[Period]] $T$. So
$$I(z)=I_{0}e^{-2\kappa z}=I_{0}e^{-z/\alpha}$$
$\alpha=1/2\kappa$ is the called the **penetration depth** of the wave. It is the characteristic length of suppression of irradiance when moving through a conductor; it's basically the skin depth of irradiance. Just like skin depth, it is usually less than or a few millimeters. For UV waves, it's around $0.6\text{ mm}$ and for infrared waves it's about $6\text{ mm}$.
#### Reflection off a conductor
Like all surfaces, an electromagnetic wave can be reflected by a conducting surface too. We start by investigating normal incidence, where the incidence angle $\theta_{i}$ is zero. As with all reflection/transmission analysis, we invoke the [[Fresnel coefficients]] $r_{\perp}$ and $r_{\parallel}$. In this scenario, we have
$$[r_{\parallel}]_{\theta_{i}=0}=[r_{\perp}]_{\theta_{i}=0}=\frac{n_{t}-n_{i}}{n_{t}+n_{i}}$$
where $i$ and $t$ denote "incident" and "transmitted", that is, the indexes of the outer and inner materials respectively. The reflectivity is
$$R=\lvert \tilde{r} \rvert ^{2}=\left( \frac{\tilde{n}-1}{\tilde{n}+1} \right)^{*}\left( \frac{\tilde{n}-1}{\tilde{n}+1} \right)=\frac{(n_{R}-1)^{2}+n_{I}^{2}}{(n_{R}+1)^{2}+n_{I}^{2}}$$
Remember that $n_{R}$ and $n_{I}$ are related to $k$ and $\kappa$ as found above. For a perfect conductor, where $\sigma\to \infty$, the imaginary component becomes massive, $n_{I}\gg n_{R}$. This means that $\kappa\gg k$, and that's exactly what we want: the higher $\kappa$ is, them more the wave transmitted inside the conductor gets suppressed, leaving only the reflection. For a terrible conductor (i.e. a perfect [[dielectric]]), where $\sigma\to0$, the opposite happens. $n_{I}=0$ and $n_{R}=c/v$. There is no suppression at all: it's just a normal, undampened plane wave.

A key detail to notice is that, since $k$ and $\kappa$ are both dependent on $\omega$, so are $n_{R}$ and $n_{I}$. In other words, the reflection/transmission angle (and the reflectivity/transmittivity in general) is dependent on the [[Wavelength]]/[[Frequency]] of the wave. This is one case of a broader phenomenon known as [[dispersion]].



[^1]: It's important to stress that this property only applies to a 3D volume. A 2D conductor such as a disk does not have all its charges on the perimeter circle and a 1D line conductor does not have its charges only at its ends.