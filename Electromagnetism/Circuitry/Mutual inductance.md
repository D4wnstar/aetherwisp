The **mutual inductance** $M$ of two [[electric current]] loops is the quantity that describes the amount of current that is induced from one loop to the other. It is a purely geometric quantity that relies on the size and shape of the loops.
### Derivation
Say you have two loops of wire, run through by currents $I_{1}$ and $I_{2}$. The current on loop 1 produces a [[magnetic field]] $\mathbf{B}_{1}$ whose field lines pass through loop 2 with a flux of $\Phi_{2}$. We know by way of the [[Biot-Savart law]] that the $\mathbf{B}_{1}$'s intensity is proportional to the intensity of the current $I_{1}$. This is not surprising, but what is surprising is that this means that the flux $\Phi_{2}$ through loop 2 is *also* dependent on $I_{1}$ as
$$\Phi_{2}=\int \mathbf{B}_{1}\cdot d\mathbf{a}_{2}$$
and thus
$$\Phi_{2}=M_{21}I_{1}$$
where $M_{21}$ is a constant of proportionality called the **mutual inductance**.

This constant can be derived by expressing the flux in terms of the [[magnetic vector potential]] and the using [[Teorema del rotore|Stokes' theorem]]:
$$\Phi_{2}=\int \mathbf{B}_{1}\cdot d\mathbf{a}_{2}=\int(\nabla\times\mathbf{A}_{1})\cdot d\mathbf{a}_{2}=\oint \mathbf{A}_{1}\cdot d\mathbf{I}_{2}$$
Now, the vector potential for a line current is
$$\mathbf{A}_{1}=\frac{\mu_{0}I_{1}}{4\pi}\oint \frac{1}{\mathfrak{r}}d\mathbf{I}_{1}$$
and hence
$$\Phi_{2}=\frac{\mu_{0}I_{1}}{4\pi}\oint \oint \frac{d\mathbf{I}_{1}\cdot d\mathbf{I}_{2}}{\mathfrak{r}}$$
from which
$$\boxed{M_{21}=\frac{\mu_{0}}{4\pi}\oint \oint \frac{d\mathbf{I}_{1}\cdot d\mathbf{I}_{2}}{\mathfrak{r}}}$$
This is called the **Neumann formula for mutual inductance**. Though it's unwieldy for actual calculation, it is rich with meaning:
1. The behavior $M_{21}$ is geometrically determined: the only things that matter are the shape, size and distance of the loops (which is what the integrals say).
2. The integral is unchanged if we invert the roles of the loops, that is, we look for $M_{12}$ instead. This means that the mutual inductance is a symmetric quantity and hence $M_{21}=M_{12}=M$.

Furthermore, if the magnetic field changes in loop 1, this prompts a change in flux in loop 2. But we know that a change in magnetic flux induces an [[Electromotive force|emf]] by the [[Electromotive force|flux rule]], so
$$\mathcal{E}_{2}=- \frac{d\Phi_{2}}{dt}=-M \frac{dI_{1}}{dt}$$
This is a remarkable result: it states that we can change the current in loop 2 by acting only on loop 1, even though the two loops are completely detached from each other. In simple terms, you can "telepathically" change currents on a loop just by having *another* loop whose current you can manipulate, as long as the two can communicate magnetically.