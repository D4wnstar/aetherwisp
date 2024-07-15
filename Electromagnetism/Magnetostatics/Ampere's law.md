**Ampere's law** relates the circulation of a [[magnetic field]] $\mathbf{B}$ around a closed loop to the [[electric current]] passing through the loop. In differential form it reads
$$\nabla\times\mathbf{B}=\mu_{0}\mathbf{J}$$
where $\mu_{0}$ is the [[permeability of free space]] and $\mathbf{J}$ is the volume current density. It can be converted to integral form by application of the [[Teorema del rotore|curl theorem]]:
$$\oint_{\gamma} \mathbf{B}\cdot d\mathbf{r}=\mu_{0}I_\text{enc}$$
where $I_\text{enc}$ is the enclosed current passing through the surface. This law can be thought of as the magnetic counterpart of [[Gauss' law]] and just like it, it makes solving some problems trivial, provided symmetry allows.
### Symmetries
There are three symmetries that work well for Ampere's law:
- a *loop around* an infinite straight wire
- a *loop across* an infinite flat surface charge density
- an infinite *solenoid*
- a toroid
#### Loop around a wire
Consider a wire carrying a steady current $I$. We want to find the current at a distance $s$ from it. We know the magnetic field goes around the wire, so the magnitude of $\mathbf{B}$ is constant on a loop around that wire. So, Ampere's law gives
$$\oint \mathbf{B}\cdot d\mathbf{r}=B\oint dl=B 2\pi s=\mu_{0}I_{enc}=\mu_{0}I$$
or
$$B=\frac{\mu_{0}I}{2\pi s}$$
#### Loop across a surface
Consider a uniform surface current density $\mathbf{K}=K \hat{\mathbf{x}}$ flowing over the $xy$ plane. The magnetic field cannot have an $x$ component since the [[Prodotto vettoriale|cross product]] between the current and the position vector in the [[Biot-Savart law]] must be on the $yz$ plane. But it also cannot have a $z$ component as the $z$ component of the field cannot possibly depend on the direction of the current in the $xy$ plane. Another way of looking at this is to image a wire in the direction of the current density. This creates a loop of magnetic field around it. If you add another wire right next to it, it'll create a second loop, but the left side of the second loop cancels out the right side of the first loop because of the superposition principle. The only parts that don't cancel out are the horizontal ones at the top and bottom. This way, the leftmost and rightmost parts remains circular, but the center is now stretched out a little. If you keep adding wires, the central flat field gets stretched out even more, until it either goes to infinity or you just pretend the surface current you just made is large enough you can only consider the central portion. Thus, the field of a flat current density is parallel to the surface and perpendicular to the current and the only direction that can be is the $y$ axis.

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