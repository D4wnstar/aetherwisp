---
aliases:
  - Ampere-Maxwell law
---
**Ampere's law** relates the circulation of a [[magnetic field]] $\mathbf{B}$ around a closed loop to the [[electric current]] passing through the loop. In differential form it reads
$$\nabla\times\mathbf{B}=\mu_{0}\mathbf{J}$$
where $\mu_{0}$ is the [[Vacuum permeability]] and $\mathbf{J}$ is the volume current density. It can be converted to integral form by application of the [[Curl theorem|curl theorem]]:
$$\oint_{\gamma} \mathbf{B}\cdot d\mathbf{r}=\mu_{0}I_\text{enc}$$
where $I_\text{enc}$ is the enclosed current passing through the surface. This law can be thought of as the magnetic counterpart of [[Gauss' law]] and just like it, it makes solving some problems trivial, provided symmetry allows.

It can also be expressed in terms of the [[magnetic vector potential]] $\mathbf{A}$ as
$$\nabla ^{2}\mathbf{A}=-\mu_{0}\mathbf{J}$$
which are three [[Poisson's equation]], one for each coordinate.
### Symmetries
There are four symmetries that work well for Ampere's law:
- a *loop around* an infinite straight wire
- a *loop across* an infinite flat surface charge density
- an infinite *solenoid*
- a *toroid*
#### Loop around a wire
Consider a wire carrying a steady current $I$. We want to find the magnetic field at a distance $s$ from it. We know the field goes around the wire, so the magnitude of $\mathbf{B}$ is constant on a loop around that wire. So, Ampere's law gives
$$\oint \mathbf{B}\cdot d\mathbf{r}=B\oint dl=B 2\pi s=\mu_{0}I_{enc}=\mu_{0}I$$
or
$$B=\frac{\mu_{0}I}{2\pi s}$$
#### Loop across a surface
Consider a uniform surface current density $\mathbf{K}=K \hat{\mathbf{x}}$ flowing over the $xy$ plane. The magnetic field cannot have an $x$ component since the [[Vector product|cross product]] between the current and the position vector in the [[Biot-Savart law]] must be on the $yz$ plane. But it also cannot have a $z$ component as the $z$ component of the field cannot possibly depend on the direction of the current in the $xy$ plane. Another way of looking at this is to imagine a wire in the direction of the current density. This creates a loop of magnetic field around it. If you add another wire right next to it, it'll create a second loop, but the left side of the second loop cancels out the right side of the first loop because of the superposition principle. The only parts that don't cancel out are the horizontal ones at the top and bottom. This way, the leftmost and rightmost parts remains circular, but the center is now stretched out a little. If you keep adding wires, the central flat field gets stretched out even more, until it either goes to infinity or you just pretend the surface current you just made is large enough you can only consider the central portion. Thus, the field of a flat current density is parallel to the surface and perpendicular to the current and the only direction that can be is the $y$ axis.

Thus, we draw an Amperian square loop across the surface with a side of $l$, with the current passing through the loop (i.e. on the $yz$ plane). Applying Ampere's law
$$\oint \mathbf{B}\cdot \mathbf{r}=2Bl=\mu_{0}I_\text{enc}=\mu_{0}Kl$$
(one $Bl$ comes from the bottom edge, the other from the top edge. The edges that cross the surface cancel each other out). Thus
$$B=\frac{\mu_{0}K}{2}$$
or more precisely
$$\mathbf{B}=\begin{cases}
+\frac{\mu_{0}K}{2}\hat{\mathbf{y}} & z>0 \\
-\frac{\mu_{0}K}{2}\hat{\mathbf{y}} & z<0
\end{cases}$$
#### Solenoid
Consider a long, closely wound solenoid of radius $R$ carrying a steady current $I$. The magnetic field cannot have a radial component as that would imply that reversing the current could make the radial component flip sign, but that makes no sense as reversing the current is equivalent to putting the solenoid upside down, which would certainly not affect the magnetic field (radially). It also cannot have a circumferential component, as if it did, the field would be constant over a loop around the solenoid and applying Ampere's law
$$\oint B\cdot d\mathbf{r}=B2\pi s=\mu_{0}I_\text{enc}=0$$
since the loop is outside the solenoid and there is no current there. This implies that the field is zero everywhere, which is manifestly false. So the field of an infinite, closely wound solenoid can only have a component on the axis of the solenoid. Goes in the reverse of the winding direction inside and alongside it outside. Knowing this, let's try applying Ampere's law to a loop outside of the solenoid, with sides at distances $a$ and $b$ from the axis:
$$\oint \mathbf{B}\cdot \mathbf{r}=(B(a)-B(b))L=\mu_{0}L=0$$
so
$$B(a)=B(b)$$
Clearly then, the field outside of the solenoid does not depend on the distance from the axis. But it also goes to zero at large distances, so the only value it can have is zero everywhere.

Let's try again with a loop going around some of the turns. Half of the loop is inside, the other half outside, so Ampere's law gives
$$\oint \mathbf{B}\cdot \mathbf{r}=BL=\mu_{0}I_\text{enc}=\mu_{0}nIL$$
so
$$B=\mu_{0}nI$$
where the field here is the one inside of the solenoid.
### For magnetized matter
Consider any magnetized object upon which is set a free current $\mathbf{J}_{f}$. The total current then is the sum of the free one and the bound one $\mathbf{J}_{b}$:
$$\mathbf{J}=\mathbf{J}_{b}+\mathbf{J}_{f}$$
From Ampere's law we get
$$\frac{1}{\mu_{0}}(\nabla\times\mathbf{B})=\mathbf{J}=\mathbf{J}_{b}+\mathbf{J}_{f}=\mathbf{J}_{f}+(\nabla\times\mathbf{M})$$
if we collect the [[Curl|curls]] we get
$$\nabla \times\left( \frac{1}{\mu_{0}}\mathbf{B}-\mathbf{M} \right)=\nabla\times\mathbf{H}=\mathbf{J}_{f}$$
where $\mathbf{H}$ is the [[auxiliary field]]. Thus Ampere's law in magnetized matter is
$$\nabla\times\mathbf{H}=\mathbf{J}_{f}$$
and in integral form
$$\oint \mathbf{H}\cdot d\mathbf{r}=I_{f,\text{enc}}$$
where $I_{f,enc}$ is the free current enclosed in the Amperian loop.
### In electrodynamics
There is an internal issue with how Ampere's law is formulated. In differential form, it is the curl of the magnetic field and from calculus we know that the [[Divergence]] of curl is always zero. And yet, if we apply the divergence to Ampere's law we get
$$\nabla\cdot(\nabla\times\mathbf{B})=\mu_{0}(\nabla\cdot\mathbf{J})$$
which is, in general, not zero. It *is* zero in magnetostatics, when using steady currents, but beyond magnetostatics (when dealing with electrodynamics), it cannot be correct. Truth is, Ampere's law is actually missing a piece, as Maxwell discovered.

For a thought experiment, imagine we are charging a [[Capacitor]]. The integral from of Ampere's law is
$$\oint \mathbf{B}\cdot d\mathbf{r}=\mu_{0}I_\text{enc}$$
Say I want to use this law on a loop right after a capacitor, beyond the second plate.

![[Circuit Ampere's law inconsistency|60%|center]]

What's the enclosed current? Well, it's whatever current is passing through the surface of the loop. But what is the surface of the loop? It's any surface bounded by it. The obvious choice here is just the flat space within the loop (blue in the image), but it just as well be the amorphous green one, similar to a balloon. The issue here is that, while in the blue surface the current passing through is obvious, in the green one there is *no* current passing through. This makes no sense: Ampere's law must hold for every possible surface bounded by the loop, it can't be picky. There's clearly something wrong here.

The problem arises in electrodynamics: this never occurred in magnetostatics because steady current don't cause a buildup of [[electric charge]] anywhere, whereas non-steady currents do. Since in order to charge a capacitor you need a non-steady current (to stockpile charge on the capacitor plates), this occurs only now. In fact, in all of electrodynamics, the concept of "current enclosed by the loop" is ill-defined, as it predicates on the notion that the current is constant in time.

To find the missing link, apply the current continuity equation and Gauss' law to the problematic side of Ampere's law
$$\nabla\cdot\mathbf{J}=- \frac{ \partial \rho }{ \partial t } =-\frac{ \partial  }{ \partial t } (\varepsilon_{0}\nabla\cdot\mathbf{E})=-\nabla \cdot\left( \varepsilon_{0}\frac{ \partial \mathbf{E} }{ \partial t }  \right)$$
where we brought the time derivative inside the [[Divergence]] because the $\mathbf{E}$ function is "well-behaved", i.e. continuous and [[Differential|differentiable]]. So, if we add the term in brackets to Ampere's law, it would exactly cancel out the divergence of the right hand side and fix the law. Thus, we get the **Ampere-Maxwell law**:
$$\boxed{\nabla\times\mathbf{B}=\mu_{0}\mathbf{J}+\mu_{0}\varepsilon_{0}\frac{ \partial \mathbf{E} }{ \partial t }}$$
The new terms vanishes in magnetostatics, where $\mathbf{E}$ is constant in time, but it cannot be ignored in electrodynamics, where it has the fundamental consequence:

> **Changing electric fields induce magnetic fields.**

The additional term $\varepsilon_{0}\frac{ \partial \mathbf{E} }{ \partial t }\equiv \mathbf{J}_{d}$ is called the **displacement current** (as opposed to the **conduction current** $\mathbf{J}$), though it has nothing to do with the actual current beyond adding to its value. To see why this fixes the law physically, beyond mathematically, let's go back to the capacitor problem. If the capacitor plates are close to each other, the field between them is
$$E=\frac{\sigma}{\varepsilon_{0}}=\frac{1}{\varepsilon_{0}} \frac{Q}{A}$$
where $Q$ is the charge on the plate and $A$ is its area. We thus have
$$\frac{ \partial E }{ \partial t } =\frac{1}{\varepsilon_{0}A}\frac{dQ}{dt} =\frac{1}{\varepsilon_{0}A}I$$
Substituting this in the fixed Ampere's law gives us
$$\oint \mathbf{B}\cdot d\mathbf{r}=\mu_{0}I_\text{enc}+\mu_{0}\varepsilon_{0}\int\left( \frac{ \partial \mathbf{E} }{ \partial t }  \right)\cdot d\mathbf{a}$$
If we choose the flat surface, then $E=0$ and $I_\text{enc}=I$, but if we choose the pathological balloon-like surface instead, then $I_\text{enc}=0$ and $\int \frac{ \partial \mathbf{E} }{ \partial t }\cdot d\mathbf{a}=I/\varepsilon_{0}$, which again gives us the correct result.