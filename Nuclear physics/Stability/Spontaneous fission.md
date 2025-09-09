---
wiki-publish: true
---
**Spontaneous fission** (**SF**) is a mode of [[Nuclear decay|decay]] in which a heavy [[Atomic nucleus|nucleus]] undergoes [[nuclear fission]] spontaneously, without [[energy]] input from external [[Particle|particles]]. This causes the nucleus to split in to daughter nuclei of variable size. Unlike other modes of decay, the decay products of spontaneous fission are quite [[random]] and are best described by a [[probability distribution]]. It's a rather rare mode of decay, only observed in superheavy [[Nuclide|radionuclides]] like uranium and plutonium. Spontaneous fission is much less common than [[induced fission]], as few nuclei are unstable enough to even permit it and even in those that do, its [[branching ratio]] is generally tiny compared to other decay modes.

The nuclear reaction reads
$$\ce{X}\to\ce{X'}+\ce{X''}+\nu n$$
where $\ce{X}$ is the original nuclide, $\ce{X'}$ and $\ce{X''}$ are the fission fragments and $\nu n$ are the $\nu$ additional [[neutron|neutrons]] that are emitted as part of the fission. The fragments are almost always extremely unstable and end up themselves decaying in a cascade of reactions.

Like [[alpha decay]], spontaneous fission is governed by the opposition of the nuclear attraction due to the [[Strong interaction|strong force]] and the repulsion due to [[electromagnetism]]. In fact, while it is not a [[cluster decay]], it works in a similar manner.

An example of radionuclide that undergoes spontaneous fission is $^{238}\text{U}$, which has a [[binding energy]] of approximately $\sim7.6\text{ MeV/nucleon}$. Normally it alpha decays, but it may also split. When it does, it splits into two smaller nuclei sampled from two distributions, both of which have higher binding energy.
### Mechanism
Consider some superheavy nucleus ($A\gtrsim 230$). It's binding energy per nucleon is very low compared to much smaller nuclei, generally in the range of $7.5-7.6\text{ MeV/nucleon}$. As such, breaking into smaller nuclei, which may have binding energy in the range of $8.0-8.5\text{ MeV/nucleon}$ is potentially very energy efficient. In practice, however, the strong attraction creates a deep well of [[potential energy]] in which then nucleus sits comfortably in and electrostatic repulsion creates a major potential barrier that prevents the nuclei from escaping or entering.

![[Grafico Fissione nucleare|80%|center]]

Let $R_{0}$ be the radius of the nucleus. If it were to split in two, the fragments would have radii $R_{1}$ and $R_{2}$. At the moment of fission, they would be "touching", so the total "size" of the result would be $R=R_{1}+R_{2}$. This end state would need to have enough energy to overcome the energy barrier for fission to happen. The potential energy at this distance is
$$U(R)=\frac{1}{4\pi\epsilon_{0}} \frac{Z_{1}Z_{2}e^{2}}{R}$$
For fission to be energetically favored, the final state must have a more negative binding energy than the initial one: $\Delta E=E_{f}-E_{i}<0$. Actually, this is just the [[Q value]], so we'll use $Q=-\Delta E$ instead. For conservation to hold, other fission products, be it [[Gamma decay|gamma rays]], individual [[proton|protons]] or [[electron|electrons]] being ejected or other must transfer away this energy through their [[kinetic energy]]: $E_{i}=E_{f}+E_\text{other}=E_{f}+Q$.

> [!example]- Uranium-238
> If $\ce{^{238}_{92}U}$ were to split in two $\ce{^{119}_{46}Pd}$ nuclei[^1], we'd have about $R\simeq 12\text{ fm}$ so
> $$U(12\text{ fm})\simeq250\text{ MeV}$$
> The binding energy of $\ce{^{238}U}$ is $E_{i}=-238\times 7.6\text{ MeV/nucleon}=-1809\text{ MeV}$. Meanwhile, two $\ce{^{119}Pd}$ have $E_{f}=-2\times 119\times8.5\text{ MeV/nucleon}=-2023\text{ MeV}$. Thus, the energy difference is
> $$\Delta E=E_{f}-E_{i}=-214\text{ MeV}$$
> Fission products must overall hold $214\text{ MeV}$ of kinetic energy.
> 
> In practice, this fission is very unrealistic, as it does not contain other products besides the two palladium nuclei and it is extremely unlikely for a nucleus to split precisely in half. Still, it makes for an easy example.

You might wonder how a nucleus whose $Q$ is lower than the potential barrier can cross the barrier. If you know alpha decay, you already know the answer: [[quantum tunneling]]. Despite the available energy being insufficient to fully cross the barrier, since the barrier is not that wide for nuclear scales, there's always a probability that the fragments can tunnel through and escape anyway. The higher $Q$ is, the higher the tunneling chance gets. This is why so few nuclides get to the fission point: $Q$ just isn't remotely high enough in some cases. Even when it is, it's often just *barely* enough to be noticeable: the uranium-238 from before has a fission half-life somewhere in the $\sim 10^{16}$ years.
### Deformation and energy
Fission is a more involved process than something like alpha decay. It involves a heavy deformation of the nucleus until it cracks in two pieces. The process is somewhat reminiscent of cellular [[mitosis]]: from its original shape (sometimes a sphere, sometimes more squished, depends on the nuclide), the nucleus gets deformed by the repulsive electrostatic forces into an [[ellipsoid]]. Eventually, the deformation is so heavy it splits into two pieces.

![[Diagram Nuclear fission deformation|100%]]

We can approximate this process by considering the deformed nucleus as being an ellipsoid of volume $V=\frac{4}{3}\pi ab^{2}$, where $a$ and $b$ are the axes of the ellipsoid. These can be expressed in terms of the volume $R$ of a sphere according to
$$a=R(1+\epsilon),\quad b=\frac{R}{\sqrt{ 1+\epsilon }}$$
where $\epsilon\equiv\beta\sqrt{5/4\pi}$ is the eccentricity and $\beta$ is the **deformation parameter**. If we take the volume the constant all throughout (we're deforming, not adding or removing), the surface area of an ellipsoid can be expressed as a [[power series]] as
$$S=4\pi R^{2}\left( 1+ \frac{2}{5}\varepsilon ^{2}+\ldots \right)$$
Electrostatic repulsion instead weakens by a factor
$$1- \frac{1}{5}\varepsilon ^{2}-\ldots$$
The reduction in binding energy can therefore be expressed by putting what we've found above in the [[semi-empirical mass formula]]:
$$\begin{align}
Q&=B(\epsilon)-B(\epsilon=0) \\
&\simeq-a_{s}A^{2/3}\left( 1+ \frac{2}{5}\epsilon^{2}+\ldots \right)-a_{C} \frac{Z^{2}}{A^{1/3}}\left( 1- \frac{1}{5}\epsilon^{2}+\ldots \right)+a_{s}A^{2/3}+a_{C} \frac{Z^{2}}{A^{1/3}} \\
&\simeq\left(- \frac{2}{5}a_{s}A^{2/3}+ \frac{1}{5}a_{C} \frac{Z^{2}}{A^{1/3}}\right)\epsilon^{2}
\end{align}$$
(the surface and Coulomb terms are the only ones that don't cancel out; also $Z(Z-1)\simeq Z^{2}$). Thus, the $Q$ value of spontaneous fission is, to first order,
$$\boxed{Q\simeq\left( - \frac{2a_{s}}{5}A^{2/3}+ \frac{a_{C}}{5} \frac{Z^{2}}{A^{1/3}} \right)\varepsilon^{2}}$$
Fission becomes spontaneous when $Q>0$, which means
$$\frac{1}{5}a_{C} \frac{Z^{2}}{A^{1/3}}>\frac{2}{5}a_{s}A^{2/3}$$
or equivalently
$$\boxed{\frac{Z^{2}}{A}>47}$$
This is only true for superheavy atoms.