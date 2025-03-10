The **Joule effect** is the phenomenon whereby an [[electric current]] $I$ traversing a material of nonzero [[electrical resistance]] $R$ dissipates [[heat]], the amount of which is dependent on the intensity of the current. For a material subject to an [[electric potential]] difference $\Delta V$,  the power output in heat is
$$P=I\Delta V=RI^{2}=\frac{\Delta V^{2}}{R}$$
The last two forms are derived with [[Ohm's law]] and work in the context of ohmic materials of electrical resistance $R$. Meanwhile, the first form, $P(t)=I(t)V(t)$, is absolutely universal and applicable in materials of all kinds, regardless of whether Ohm's law applies, if they are homogeneous, have a constant cross-section or what their conduction mechanism is. Moreover, the presence of a [[magnetic field]] makes no difference since magnetic forces do no work.

If our material is a homogeneous wire of length $l$ and constant cross-section $S$, we can write
$$P(t)=I(t)V(t)=J_{f}(t)S\ E_{l}(t)l=J_{f}(t)E_{l}\mathcal{V}=\mathcal{V}\ \mathbf{J}_{f}(t)\cdot \mathbf{E}(t)$$
where $E_{l}(t)=V(t)/l$ is the projection of the total [[electric field]] over the [[Curve|curve]] $l$ and $\mathcal{V}$ is the volume of the material. If we divide by the volume we can find the heat emission per unit element of the material centered in $\mathbf{r}$:
$$p(\mathbf{r},t)=\mathbf{J}_{f}(\mathbf{r},t)\cdot \mathbf{E}(\mathbf{r},t)$$
### Derivation
Consider any piece of a circuit subject to an [[electric potential]] difference $\Delta V$ and traversed by a current $I$. In a time $dt$, the piece is traversed by an [[electric charge]] $dq=Idt$, so the [[work]] done by the [[electric field]] here is $dW=\Delta Vdq=I\Delta Vdt$. Since power is the time derivative of work, we have
$$P=\frac{dW}{dt}=I\Delta V$$
If the piece is an ohmic resistor, we can apply [[Ohm's law|Ohm's first law]]:
$$P=RI^{2}$$
