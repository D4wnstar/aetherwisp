---
wiki-publish: true
---
The **magnetic field** $\mathbf{B}$ is the [[Vector field|vector field]] that describes the action of an [[electric current]] onto other [[Electric charge|electric charges]]. It is measured in either Teslas $\text{T}$ or Gauss $\text{G}$. It is given by the [[Biot-Savart law]].

Magnetic fields obey the [[superposition principle]]. If there are two currents producing fields $\mathbf{B}_{1}$ and $\mathbf{B}_{2}$, their combined field is simply $\mathbf{B}=\mathbf{B}_{1}+\mathbf{B}_{2}$.

Similarly to the [[electric field]], the magnetic field of a [[Physical system|system]] is in general the combination of more than one piece. However, for magnetic fields the division is complicated by the fact that, while electrical forces can push charges around, magnetic forces do no [[work]] and therefore cannot. As such, there are no source and response fields in magnetism and the extra terms are entirely dependent on the nature of the material (and are therefore not relevant in the vacuum). Beyond the magnetic field produce by a free current, a material can hold a permanent [[magnetization]], which produces are permanent current rotating around the material and therefore a magnetic field. Moreover, if the material is a [[dielectric]] whose [[Dielectric polarization|polarization]] changes in time (say, by a variable source electric field), the motion of the charges is a current that creates a (time-variable) magnetic field. In general, the total field is
$$\mathbf{B}_\text{total}=\mathbf{B}_\text{free}+\mathbf{B}_\text{magnetization}+\mathbf{B}_\text{var. polarization}$$
### Curl
The magnetic field's [[Curl]] is manifestly nonzero as it rotates around the current. We can start from the magnetic field of a long straight wire and calculate the [[Integrale su una curva|path integral]] over a closed circular path of radius $s$ centered in the wire:
$$\oint \mathbf{B}\cdot d\mathbf{r}=\oint \frac{\mu_{0}I}{2\pi s}dl=\frac{\mu_{0}I}{2\pi s}\oint dl=\frac{\mu_{0}I}{2\pi s}2\pi s=\mu_{0}I$$
The answer is independent of the radius. In fact, it's independent of the shape of the loop too, the circle was just a convenient choice. Now, say you have several wires arranged in any way. Only the ones passing through the loop make a difference, and the ones that do all end up providing $\mu_{0}I_{i}$, so the total is just the sum of currents that pass through:
$$\oint \mathbf{B}\cdot d\mathbf{r}=\mu_{0}I_\text{enc}$$
This is known as [[Ampere's law]]. If the flow of charge is described by a volume current density
$$I_\text{enc}=\int \mathbf{J}\cdot d\mathbf{a}$$
where the integral is taken over any surface bounded by the loop. Here we can apply the [[Curl theorem|curl theorem]]:
$$\int (\nabla\times\mathbf{B})\cdot d\mathbf{a}=\mu_{0}\int \mathbf{J}\cdot d\mathbf{a}$$
and we can extract the integrands
$$\nabla\times\mathbf{B}=\mu_{0}\mathbf{J}$$
This is a simple, yet restrictive way of finding the curl of $\mathbf{B}$. Unfortunately, this implies a system made up of infinite straight wires, which isn't quite realistic in the majority of cases. For a more rigorous definition, we must start from the Biot-Savart law.
### Divergence
The Biot-Savart law, for a volume current, reads
$$\mathbf{B}(\mathbf{r})=\frac{\mu_{0}}{4\pi}\int \frac{\mathbf{J}(\mathbf{r}')\times \hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}}\ d\tau'$$
Here in particular, it's important to note that $\mathbf{B}$ is a function of the point $\mathbf{r}$ unprimed coordinates, whereas $\mathbf{J}$ is a function of the primed source coordinate, as is the volume element $d\tau'$. $\mathfrak{r}$ is, as usual, the difference between the two. Applying the [[Divergence]] we get
$$\nabla\cdot\mathbf{B}=\frac{\mu_{0}}{4\pi}\int \nabla \cdot\left( \mathbf{J}(\mathbf{r}')\times \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}} \right)\ d\tau'$$
The divergence of [[Vector product|cross product]] can be developed like
$$\nabla \cdot\left( \mathbf{J}(\mathbf{r}')\times \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}} \right)=\frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}}\cdot(\nabla\times\mathbf{J}(\mathbf{r}'))-\mathbf{J}(\mathbf{r}')\cdot\left( \nabla\times \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}} \right)$$
The derivation $\nabla$ is over the unprimed coordinates and since $\mathbf{J}$ doesn't depend on them, it's derivative is zero: $\nabla\times\mathbf{J}=0$. The curl of $\hat{\boldsymbol{\mathfrak{r}}}/\mathfrak{r}^{2}$ is also zero. Thus
$$\boxed{\nabla\cdot\mathbf{B}=0}$$
### Curl, again
We can also get the curl out of the Biot-Savart law. Applying the curl to it we get
$$\nabla\times\mathbf{B}=\frac{\mu_{0}}{4\pi}\int \nabla \times\left( \mathbf{J}\times \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}} \right)\ d\tau'\tag{1}$$
Developing the double cross product we get
$$\nabla \times\left( \mathbf{J}\times \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}} \right)=\mathbf{J}\left( \nabla\cdot \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}} \right)-(\mathbf{J}\cdot \nabla) \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}}$$
where terms involving derivatives of $\mathbf{J}$ where removed because of coordinate differences. The first term is the divergence of $\hat{\boldsymbol{\mathfrak{r}}}/\mathfrak{r}^{2}$, which is known
$$\nabla \cdot\left( \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}} \right)=4\pi \delta^{3}(\boldsymbol{\mathfrak{r}})$$
using the three-dimensional [[Delta di Dirac|Dirac delta]]. To solve the second term, notice that $\hat{\boldsymbol{\mathfrak{r}}}/\mathfrak{r}^{2}$ depends on both coordinates, specifically by a difference, so we can freely switch the coordinates of $\nabla$ to $\nabla'$ at the cost of inverting the sign[^1]:
$$-(\mathbf{J}\cdot \nabla)\left( \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}} \right)=(\mathbf{J}\cdot \nabla')\left( \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}} \right)$$
The $x$ component is
$$(\mathbf{J}\cdot \nabla')\left( \frac{x-x'}{\mathfrak{r}^{3}} \right)=\nabla'\cdot\left[ \frac{x-x'}{\mathfrak{r}^{3}}\mathbf{J} \right]-\left( \frac{x-x'}{\mathfrak{r}^{3}} \right)(\nabla'\cdot \mathbf{J})$$
For *steady* currents, the divergence of $\mathbf{J}$ is zero, so
$$\left[ -(\mathbf{J}\cdot \nabla') \frac{\boldsymbol{\mathfrak{r}}}{\mathfrak{r}^{2}} \right]_{x}=\nabla'\cdot\left[ \frac{x-x'}{\mathfrak{r}^{3}}\mathbf{J} \right]$$
and therefore the contribution to the original integral $(1)$ can be written as
$$\int_{V}\nabla'\cdot \left[ \frac{x-x'}{\mathfrak{r}^{3}}\mathbf{J} \right]d\tau'=\oint_{S} \frac{x-x'}{\mathfrak{r}^{3}}\mathbf{J}\cdot d\mathbf{a}'$$
using [[Integrazione per parti|integration by parts]] (which is why we switched to primed coordinates in the first place). But the surface we are integrating on is the bounding surface of the volume in the Biot-Savart law, which is the volume large enough to contain the whole current. Since the current exists entirely *inside* the volume, there is no current on the surface, for which $\mathbf{J}=0$ for any point on the surface, which means the integral is zero[^2]. Thus what we are left with
$$\nabla\times\mathbf{B}=\frac{\mu_{0}}{4\pi}\int \mathbf{J}(\mathbf{r}')4\pi \delta^{3}(\mathbf{r}-\mathbf{r}')\ d\tau'$$
which integrates to
$$\boxed{\nabla\times\mathbf{B}=\mu_{0}\mathbf{J}(\mathbf{r})}$$
which is [[Ampere's law]].
### Notable cases
> [!example] Straight wire segment
>Consider a long straight wire on the $x$ axis carrying a steady current $I$. We want to find the magnetic field $\mathbf{B}$ at a distance $s$ on the $y$ axis. If the point is above the wire, $d\mathbf{I}\times \hat{\boldsymbol{\mathfrak{r}}}$ points out of the page and has a magnitude
>$$dl'\sin \alpha=dl'\cos \theta$$
>where $\alpha$ is the angle between the current vector $\boldsymbol{\mathfrak{r}}$ and $\theta$ is the ("azimuthal") angle between $\boldsymbol{\mathfrak{r}}$ and the vertical $y$ axis. We have $l'=s\tan \theta$, so
>$$dl'=\frac{s}{\cos ^{2}\theta}d\theta$$
>and $s=\mathfrak{r}\cos \theta$, so
>$$\frac{1}{\mathfrak{r}^{2}}=\frac{\cos^{2}\theta}{s^{2}}$$
>Thus Biot-Savart's law becomes
>$$B=\frac{\mu_{0}I}{4\pi}\int_{\theta_{1}}^{\theta_{2}} \frac{ \cos ^{2}\theta}{s^{2}} \frac{s}{\cos ^{2}\theta}\cos \theta\ d\theta=\frac{\mu_{0}I}{4\pi s}\int_{\theta_{1}}^{\theta_{2}}\cos \theta\ d\theta=\frac{\mu_{0}I}{4\pi s}(\sin \theta_{2}-\sin \theta_{1})$$
>where $\theta_{1}$ and $\theta_{2}$ are the angle between the point of calculation and the start and end of the segment of wire.
>
>Of course, the wire itself has to be a loop, otherwise the current cannot go anywhere, but this formula can represent a piece of a closed circuit. If the wire really is infinite, then $\theta_{1}=-\pi/2$ and $\theta_{2}=\pi/2$ and the field is
>$$B=\frac{\mu_{0}I}{2\pi s}$$
>The direction is, as usual, the one that circles around the wire
>$$\mathbf{B}=\frac{\mu_{0}I}{2\pi s}\hat{\boldsymbol{\phi}}$$

> [!example] Attraction between long wires
> Consider two long wires with currents $I_{1}$ and $I_{2}$ going up the page a distance $d$ apart. The field on wire 2 due to wire 1 is
> $$B=\frac{\mu_{0}I}{4\pi d}$$
> a points into the page. The [[Lorentz force]] between the two is
> $$F=I_{2}\left( \frac{\mu_{0}I_{1}}{2\pi d} \right)\int dl$$
> The total force is, unsurprisingly, infinite. But the force per unit length is
> $$f=\frac{\mu_{0}}{2\pi} \frac{I_{1}I_{2}}{d}$$
> If the currents go in the same direction, the force is attractive, but in opposite directions it is repulsive.

> [!example] Wire loop
> Consider a wire loop of radius $R$ with steady current $I$. The field above the loop at distance $z$ is
> $$B(z)=\frac{\mu_{0}I}{4\pi} \frac{\cos \theta}{\mathfrak{r}^{2}}2\pi R=\frac{\mu_{0}I}{2} \frac{R^{2}}{(R^{2}+z^{2})^{3/2}}$$

> [!example] Solenoid
> Consider a solenoid of with a coil density of $n$ turn per unit length around a cylindrical tube of radius $a$ and carrying current $I$. The magnetic field applied on a point on the axis can be found by extending the wire loop magnetic field above to a ring of thickness $dz$ and current $nIdz$:
> $$B=\frac{\mu_{0}nI}{2}\int \frac{a^{2}}{(a^{2}+z^{2})^{3/2}}dz$$
> but since $z=a\cot \theta$ we have
> $$dz=- \frac{a}{\sin ^{2}\theta}d\theta,\qquad \frac{1}{(a^{2}+z^{2})^{3/2}}=\frac{\sin ^{3}\theta}{a^{3}}$$
> So
> $$B=\frac{\mu_{0}nI}{2}\int \frac{a^{2}\sin ^{3}\theta}{a^{3}\sin ^{2}\theta}(-ad\theta)=- \frac{\mu_{0}nI}{2}\int_{\theta_{1}}^{\theta_{2}} \sin \theta d\theta$$
> which solves to
> $$B=\frac{\mu_{0}nI}{2}(\cos \theta_{2}-\cos \theta_{1})$$
> where $\theta_{1}$ and $\theta_{2}$ are the angles between the point of calculation and the closest and furthest coil respectively.
> 
> If the solenoid is infinite, the angles are $\theta_{2}=0$ and $\theta_{1}=\pi$ so $\cos \theta_{2}-\cos \theta_{1}=1-(-1)=2$ and so
> $$B=\mu_{0}nI$$
### Boundary conditions
The magnetic field suffers a discontinuity when passing through a surface current density $\mathbf{K}$. Say we apply
$$\oint \mathbf{B}\cdot d\mathbf{a}=0$$
to a pillbox straddling the surface current, we get
$$B^{\perp}_\text{above}=B^{\perp}_\text{below}=0$$
because the magnetic field caused by a surface is entirely parallel to the surface. Let us, then, look at the parallel component by running an Amperian loop across the surface, perpendicular to the current:
$$\oint \mathbf{B}\cdot d\mathbf{r}=(B_\text{above}^{\parallel}-B_\text{below}^{\parallel})l=\mu_{0}\mathbf{I}_\text{enc}=\mu_{0}\mathbf{K}l$$
or
$$B_\text{above}^{\parallel}-B_\text{below}^{\parallel}=\mu_{0}K$$
This component is parallel to the surface, by perpendicular to the current. A similar loop running parallel to the current instead gives us that the component parallel to the current is instead continuous. Thus, what we have above is the only discontinuity in the field, which we can put into vector form as
$$\mathbf{B}_\text{above}-\mathbf{B}_\text{below}=\mu_{0}(\mathbf{K}\times \hat{\mathbf{n}})$$
with $\hat{\mathbf{n}}$ being the normal vector to the surface.
#### Transmission angle
The presence of a discontinuity implies that the field incident on a surface changes direction as it passes through the surface (i.e. it is transmitted).

![[Schema Magnetic field transmission|90%]]

When a magnetic field passes through the surface, the component perpendicular to the surface is conserved. We can use this to connect the incidence angle $\alpha_{\text{ext}}$ and the transmission angle $\alpha_{\text{int}}$. We can express the perpendicular components in terms of the sines of these two angles:
$$B_\text{ext}\sin \alpha _\text{ext}=B_\text{int}\sin \alpha _\text{int}$$
Since we're working in materials, we can employ the [[auxiliary field]] $\mathbf{H}$, which instead conserves the parallel component to the surface, which means the cosines:
$$H_\text{ext}\cos \alpha _\text{ext}=H_\text{int}\cos \alpha _\text{int}$$
We can divide the first equation by the second:
$$\frac{B_\text{ext}}{H_\text{ext}}\tan \alpha _\text{ext}=\frac{B_\text{int}}{H_\text{int}}\tan \alpha _\text{int}$$
This is a general relation that applies for most [[Paramagnet|paramagnets]] and [[Diamagnet|diamagnets]][^3]. If we specifically say that we are working with linear and isotropic materials, we can claim that $\mathbf{H}=\mathbf{B}/\mu_{0}\mu_{r}$, using the [[permeability]] of the materials. If we make the substitution we find
$$\boxed{\mu_{r,\text{ext}}\tan \alpha _\text{ext}=\mu_{r,\text{int}}\tan \alpha _\text{int}}$$
In general, the bigger the difference between permeabilities, the larger the difference in angle will be. If the internal permeability is higher than the external one, the field will tend to align flush to the surface. This is a key aspect of a [[magnetic circuit]], where very high permeability ($\mu\gg 1000$) materials are used to the keep the internal field aligned and prevent it from being dispersed into the external environment.

Given the relative permeabilities of the materials and one of the two angles, we can find the other. We can also measure the angles themselves to figure out the permeability of one the materials, if we know the other.

[^1]: In fact, for a general function $f(x-x')$, the partial derivatives go like$$\frac{ \partial  }{ \partial x } f(x-x')=-\frac{ \partial  }{ \partial x' } f(x-x')$$
[^2]: If the current extends to infinity, such as for a straight wire, more care needs to be taken, though it's still common for it to go to zero anyway.

[^3]: This equation assumes that the fields $\mathbf{B}$ and $\mathbf{H}$ do not reverse direction when passing through the surface. In these cases, more care should be taken to keep the signs consistent.
