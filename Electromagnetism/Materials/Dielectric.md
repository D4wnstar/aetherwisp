---
wiki-publish: true
aliases:
  - insulator
  - linear dielectric
---
A **dielectric** or **insulator** is a material in which all [[Electric charge|electric charges]] are bound to a specific [[Atom|atom]] or [[molecule]] and cannot move far from it. There are no free charges.
### Behavior under an electric field
#### Atoms
The simplest possible dielectric is a single atom, with a positively charged [[Atomic nucleus|atomic nucleus]] and a negatively charged [[Elettrone|electron]] cloud surrounding it. When subject to an [[electric field]], the nucleus and electron cloud move in opposite direction, as one is attracted by the field and the other is repelled. With a strong enough field, the electrons can be ripped from the nucleus, thus [[ionizzazione|ionizing]] the atom, but for milder fields, a state of equilibrium is reached.

The force keeping the nucleus and cloud together balances the one applied by the external field. In this state, the geometric center of the electron cloud, which acts as a sort of charge equivalent of the [[Center of mass]], does not coincide with the (approximately point-like) nucleus. As such, the positive and negative charges of the atom are not superimposed and this turns the atom into an [[electric dipole]], with a (tiny) [[electric dipole moment]] that is typically proportional to the strength of the external field. Such an atom (or molecule) is said to be **polarized** and the dipole moment is modeled as
$$\mathbf{p}=\alpha \mathbf{E}$$
where $\mathbf{E}$ is the field and $\alpha$ is an atom-specific constant called the [[atomic polarizability]].
#### Molecules
In the case of molecules, the situation is more complicated, as the geometry of a molecule determines whether there are directions in which it is more easily polarized. In the case of a linear molecule, such as $\text{CO}_{2}$, the polarizability is highest on the molecule's axis. This complicates the induced moment's formula due to having to consider both the components parallel and perpendicular to the axis:
$$\mathbf{p}=\alpha_{\perp}\mathbf{E}_{\perp}+\alpha_{\parallel}\mathbf{E}_{\parallel}$$
This may make the moment not even in the same direction of the field. For completely asymmetrical molecules, the polarizability splits in nine different components, one for every combination of axes. The object containing these components is called the **polarizability tensor** and is applied to the electric field:
$$\begin{pmatrix}
p_{x} \\
p_{y} \\
p_{z}
\end{pmatrix}=\begin{pmatrix}
\alpha_{xx} & \alpha_{xy} & \alpha_{xz} \\
\alpha_{yx} & \alpha_{yy} & \alpha_{yz} \\
\alpha_{zx} & \alpha_{zy} & \alpha_{zz}
\end{pmatrix}\begin{pmatrix}
E_{x} \\
E_{y} \\
E_{z}
\end{pmatrix}$$

Some molecules are permanently polarized due to their geometry. These are called **polar molecules**. If a uniform field is applied, the force on the positive end of the molecule is $\mathbf{F}_{+}=q\mathbf{E}$ and cancels out the force of the negative end $\mathbf{F}_{-}=-q\mathbf{E}$ exactly. However, a moment of force is applied:
$$\mathbf{N}=(\mathbf{r}_{+}\times \mathbf{F}_{+})+(\mathbf{r}_{-}\times \mathbf{F}_{-})=\left( \frac{\mathbf{d}}{2}\times q\mathbf{E} \right)+\left( - \frac{\mathbf{d}}{2}\times (-q\mathbf{E}) \right)=q\mathbf{d}\times \mathbf{E}$$
where $\mathbf{d}$ is the distance from the center of the molecule. Clearly then, a dipole $\mathbf{p}$ in a uniform field experiences a moment of force
$$\mathbf{N}=\mathbf{p}\times \mathbf{E}$$
Notably, $\mathbf{N}$ is in such a direction as to make $\mathbf{p}$ line up *parallel* to $\mathbf{E}$, as for $\mathbf{N}$ to be zero, and hence stop the rotation, $\mathbf{p}$ must be parallel to $\mathbf{E}$. This means that the dipole will rotate until it points in the direction of the field.

If the field is nonuniform, $\mathbf{F}_{+}$ does not balance $\mathbf{F}_{-}$ and there will be a net force on the molecule (on top of the moment of force). This is uncommon, as since molecules are tiny, the variation of the field needs to be very important such that we can't ignore the variation even in the space of a molecule. That said, the formula is
$$\mathbf{F}=\Delta \mathbf{F}_{\pm}=q(\mathbf{E}_{+}-\mathbf{E}_{-})=q\Delta \mathbf{E}$$
If the dipole is tiny, we can approximate this for each axis as
$$\Delta E_{i}\equiv(\nabla E_{i})\cdot \mathbf{d}$$
where $i=x,y,z$. In vector terms
$$\Delta \mathbf{E}=(\mathbf{d}\cdot \nabla)\mathbf{E}$$
and therefore
$$\mathbf{F}=(\mathbf{p}\cdot \nabla)\mathbf{E}$$
and the moment of force therefore sums to the previous one to get
$$\mathbf{N}=\mathbf{p}\times \mathbf{E}+\mathbf{r}\times \mathbf{F}$$
#### Linear dielectrics
At a macroscopic level, we can estimate the behavior of materials by their behavior at a microscopic level. From the study of [[dielectric polarization]], we know that it comes from the alignment of atoms and molecules around the electric field. We also know that the intensity of their dipole moment is dependent on the strength of the field, so long it's not large enough to break the molecules. Thus, we can (qualitatively) assume that the polarization of a dielectric is dependent on the electric field that is applied onto it. In fact, many material not only exhibit this dependence, but specifically a linear dependence:
$$\mathbf{P}=\varepsilon_{0}\chi_{e}\mathbf{E}$$
where $\varepsilon_{0}$ is the [[Vacuum permittivity|vacuum permittivity]] and $\chi_{e}$ is the [[electric susceptibility]], whose value depends on the microscopic structure of the material and external factors like temperature. $\mathbf{E}$ is the total field, including the one caused by polarization itself. Materials that obey this relation are known as **linear dielectrics**.

The dependence on the *total* field, as opposed to the external field, can cause problems: say you apply a field to a dielectric. It gets polarized and starts producing a field of its own, which adds on top of the external one, which in turn causes a variation in the polarization, which changes the material's field, which changes the total field, which changes the polarization, which— you get the point. Logically, it goes on to infinity, though it eventually comes to rest. Breaking out of the infinite loop can be done, for instance, by examining the [[electric displacement]] instead:
$$\mathbf{D}=\varepsilon_{0}\mathbf{E}+\mathbf{P}=\varepsilon_{0}\mathbf{E}+\varepsilon_{0}\chi_{e}\mathbf{E}=\varepsilon_{0}(1+\chi_{e})\mathbf{E}$$
We can define the [[permittivity]] of a material as
$$\varepsilon=\varepsilon_{0}(1+\chi_{e})$$
and thus the displacement is
$$\boxed{\mathbf{D}=\varepsilon \mathbf{E}}$$

Despite the displacement being entirely dependent on $\mathbf{E}$, the [[Curl]] of $\mathbf{D}$ is still not guaranteed to be zero. This is because for it to be zero, the line integral across the boundary between materials needs to be zero, but it isn't zero as the electric susceptibility changes when switching material. In fact, this discontinuity in $\chi_{e}$ not only causes the curl to be nonzero, it makes it blow up to infinity in those points. Mathematically, the cause is that the curl of $\mathbf{P}$ in linear dielectrics is
$$\nabla\times\mathbf{P}=\varepsilon_{0}\nabla\times\mathbf{(\chi_{e}\mathbf{E})}=-\varepsilon_{0}\mathbf{E}\times(\nabla \chi_{e})$$
and is dependent on the [[Gradient]] of $\chi_{e}$. The only way this can be zero is if $\chi_{e}$ is spatially constant. In other words, all space[^1] needs to have the same susceptibility, in which case $\nabla \chi_{e}=0$ and the curl of $\mathbf{P}$ (and therefore $\mathbf{D}$) is zero everywhere. A material in which the susceptibility is constant is said to be **homogeneous**. In this scenario, the displacement is very much analogous to the electric field and similar laws apply to it:
$$\nabla\cdot\mathbf{D}=\rho_{f},\qquad \nabla\times\mathbf{D}=0$$
and the displacement can be calculated as if the dielectric was not there in the first place:
$$\mathbf{D}=\varepsilon_{0}\mathbf{E}_\text{vac}$$
where $\mathbf{E}_\text{vac}$ is the field that would be produced by the same free charge distribution if the dielectric was not there. It is related to the actual field by a constant:
$$\mathbf{E}=\frac{1}{\varepsilon}\mathbf{D}=\frac{1}{\varepsilon_{r}}\mathbf{E}_\text{vac}$$
##### Boundary values
Under the assumption that the linear dielectric is both homogeneous and isotropic, the bound charge density $\rho_{b}$ is proportional to the free charge density $\rho_{f}$:
$$\boxed{\rho_{b}=-\nabla\cdot\mathbf{P}=-\nabla \cdot\left( \varepsilon_{0} \frac{\chi_{e}}{\varepsilon}\mathbf{D} \right)=-\left( \frac{\chi_{e}}{1+\chi_{e}} \right)\rho_{f}}$$
In particular, unless free charge is embedded in the material, the bound charge density must be zero. Thus, all the charge must reside on the surface. This way, the potential obeys [[Laplace's equation]] and it can be used to find it.

The conditions can also be rewritten to explicitly only reference the free charge too. Starting from the displacement boundary conditions we have
$$D_\text{above}^{\perp}-D_\text{below}^{\perp}=\varepsilon _\text{above}E_\text{above}^{\perp}-\varepsilon _\text{below}E_\text{below}^{\perp}=\sigma_{f}$$
and in terms of potential
$$\varepsilon _\text{above}\frac{ \partial V_\text{above} }{ \partial n } -\varepsilon _\text{below}\frac{ \partial V_\text{below} }{ \partial n } =-\sigma_{f}$$
### Energy
#### In capacitors
From the fact that a [[Capacitor]] filled with dielectric has a higher [[capacitance]], and from the formula
$$W=\frac{1}{2}CV^{2}$$
we can recognize that it must take more work to charge a dielectric-filled capacitor than a vacuum one. The reason here is because part of the field is cancelled out by the bound charges that occur in a material, thus it takes more free charge to achieve the same potential.
#### In linear dielectrics
For a linear dielectric, the displacement is $\mathbf{D}=\varepsilon \mathbf{E}$. We can modify the formula for the electrostatic energy stored in a system to take this into account:
$$W=\frac{\varepsilon_{0}}{2}\int \varepsilon_{r}E^{2}\ d\tau=\frac{1}{2}\int \mathbf{D}\cdot \mathbf{E}\ d\tau$$
To prove this is true, suppose some (not necessarily linear) dielectric is fixed and we move a free charge closer. Since the distribution $\rho_{f}$ is increased by an amount of $\Delta \rho_{f}$ each time the charge moves a little bit closer, the polarization will change and with it, the bound charge distribution. We're only interested about the incremental work done on the free charge itself:
$$\Delta W=\int(\Delta \rho_{f})V\ d\tau$$
Since $\nabla\cdot\mathbf{D}=\rho_{f}$, $\Delta \rho_{f}=\nabla \cdot(\Delta \mathbf{D})$, where $\Delta \mathbf{D}$ is the change in displacement due to moving the free charge closer. So
$$\Delta W=\int[\nabla \cdot(\Delta \mathbf{D})]V\ d\tau$$
Now
$$\nabla \cdot[(\Delta \mathbf{D})V]=[\nabla \cdot(\Delta \mathbf{D})]V+\Delta \mathbf{D}\cdot(\nabla V)$$
and using [[Integrazione per parti|integration by parts]] we get
$$\Delta W=\int \nabla \cdot[(\Delta \mathbf{D})V]\ d\tau+\int(\Delta \mathbf{D})\cdot \mathbf{E}\ d\tau$$
The [[Divergence theorem|divergence theorem]] turns the first integral into a surface integral, which vanishes if we integrate over  all space. Thus, only the second term remains
$$\Delta W=\int(\Delta \mathbf{D})\cdot \mathbf{E}\ d\tau$$
This is universal and applies to all dielectrics. Now suppose it is linear. We can substitute the displacement like
$$(\Delta \mathbf{D})\cdot \mathbf{E}=\varepsilon(\Delta \mathbf{E})\cdot \mathbf{E}=\frac{1}{2}\Delta(\varepsilon E^{2})=\frac{1}{2}\Delta(\mathbf{D}\cdot \mathbf{E})$$
(for infinitesimal increments). Thus
$$\Delta W=\Delta\left( \frac{1}{2}\int \mathbf{D}\cdot \mathbf{E}\ d\tau \right)$$
The total work done to build up the charge all the way from zero to the end result, then, is
$$\boxed{W=\frac{1}{2}\int \mathbf{D}\cdot \mathbf{E}\ d\tau}$$
This formula ends up differing from the original one, but not because either are wrong, they just represent different energies. The general one dependent on the square of the field represents the energy required to assemble all charges in the system, both free *and* bound, by moving each one independently from infinity (or whatever point of reference). This *does not*, however, include the energy spent when rotating and stretching the molecules and atoms of the dielectric to actually get the charges into their expected geometry, as you are moving the charges one by one. The second formula, dependent on the displacement, instead represents the energy required to move *only* the free charge, but *does* include the elastic "spring" energy contained in the atoms and molecules due to, well, their displacement. The difference here is that the first energy is about moving charges as if they were independent, while the second involves moving only the free ones and figuring out how bound charges respond. The latter is always higher (as it also includes the elastic energy) and generally the one you want, as free charges are usually artificially controlled, but bound ones are not.
### Electromagnetic wave dispersion
[[Dispersion]] is the [[frequency]] dependence of a [[wave|wave]]'s [[phase velocity]]. It is a known phenomenon in optics, where light scattering from a piece of glass disperses into a rainbow. This section attempts to explain *why* an [[electromagnetic wave]] disperses in a dielectric.

A correct model of dispersion requires a quantum mechanical model of [[electron|electronic]] structure, but a qualitative model can be developed even with classical physics alone.
Our end goal is to explain why the [[permittivity]] $\varepsilon$ of a dielectric is dependent on the [[Frequency|angular frequency]] $\omega$ of an electromagnetic wave. We will do so through a simplified model of electrons in matter.

Each electron in a dielectric is, generally speaking, bound to a specific [[molecule]]. We'll say that there is a binding [[force]] $F_{\text{binding}}$ keeping the electron attached to the molecule against the displacement of imposed by the wave (which we assume to be propagating on the $x$ axis and [[Polarization|polarized]] on the $y$ axis as usual) and we'll say that this force is elastic and described by [[Harmonic oscillator|Hooke's law]]:
$$F_\text{binding}=-kx=-m\omega_{0}^{2}y$$
where $k=m\omega_{0}^{2}$ is the spring constant, $m$ is the [[mass]] of the electron and $\omega_{0}=\sqrt{ k/m }$ is the *natural oscillation frequency*. We claim this is a valid approximation since any [[potential]] (and thus force) can be approximated by the [[harmonic oscillator]] for small enough displacements around an [[equilibrium point]], which the electron's stable orbit around the molecule is.

This electron is likely also subject to a damping force $F_\text{damping}$, which we'll assume to be a generic [[dissipative force]]
$$F_\text{damping}=-m\gamma \frac{dy}{dt}$$
for some damping coefficient $\gamma>0$. As for *why* this is here, that's beyond the scope of this model. There are reasons, such as [[Radiation reaction|radiation damping]], but they aren't relevant here.

Finally, when the wave passes by, it will enact a driving force $F_\text{driving}$ on the electron as per the [[electric field]] $E$:
$$F_\text{driving}=qE=qE_{0}\cos (\omega t)$$
where $q$ is the [[elementary charge]] and $E_{0}$ is the [[amplitude]] of the electric part of the wave at the coordinates of the electron. Of course, the full force would be a [[Lorentz force]] including the [[magnetic field]], but magnetic forces are tiny compared to electric ones in the vacuum, so we can ignore without loss of much generality.

Combine all of these with [[Newton's laws|Newton's second law]] and you get
$$F_\text{tot}=m \frac{d^{2}y}{dt^{2}}=F_\text{binding}+F_\text{damping}+F_\text{driving}$$
so
$$m \frac{d^{2}y}{dt^{2}}+m\gamma \frac{dy}{dt}+m\omega_{0}^{2}y=qE_{0}\cos (\omega t)$$
This is an inhomogeneous second-order linear [[ordinary differential equation]] in $x$, representing a damped harmonic oscillator driven at frequency $\omega$. This becomes easier to handle if we regard it as the real part of a complex differential equation in $\tilde{x}$:
$$\frac{d^{2}\tilde{y}}{dt^{2}}+\gamma \frac{d\tilde{y}}{dt}+\omega_{0}^{2}\tilde{y}=\frac{q}{m}E_{0}e^{-i\omega t}$$
where we used [[Euler's formula]] to see the cosine as the real part of a complex exponential. In a steady state, the system oscillates at the driving frequency
$$\tilde{x}(t)=\tilde{x}_{0}e^{-i\omega t}$$
Plugging this into the ODE and solving for $\tilde{x}_{0}$ gives
$$\tilde{x}_{0}=\frac{q}{m}\frac{1}{\omega_{0}^{2}-\omega ^{2}-i\gamma \omega}E_{0}$$
An oscillating charge act as an [[electric dipole]] of [[electric dipole moment]]
$$\tilde{p}(t)=q\tilde{x}(t)=\frac{q^{2}}{m}\frac{1}{\omega_{0}^{2}-\omega ^{2}-i\gamma \omega}E_{0}e^{-i\omega t}$$
Note the presence of an imaginary term $i\gamma \omega$ at the denominator. This causes a [[phase]] shift in $p$ compared to $E$, leaving it $\arctan(\gamma m/(\omega_{0}^{2}-\omega ^{2}))$ behind. This angle is tiny when $\omega\ll \omega_{0}$ and grows asymptotically to $\pi$ when $\omega\gg \omega_{0}$.

The exact values for $\omega$, $\omega_{0}$ and $\gamma$ depend on the position of electron in the molecule and its orbit in the system. Suppose there are $f_{j}$ electrons with natural frequency $\omega_{j}$ and damping coefficient $\gamma_{j}$. If there are $N$ molecules per unit volume, the [[dielectric polarization]] $\mathbf{P}$ is the real part of
$$\tilde{\mathbf{P}}=\frac{Nq^{2}}{m}\left( \sum_{j} \frac{f_{j}}{\omega_{j}^{2}-\omega ^{2}-i\gamma_{j}\omega}  \right)\tilde{\mathbf{E}}$$
Now, $\mathbf{P}$ (the real part) is not currently linearly proportional to $\mathbf{E}$ since there is a phase difference between (all due to that pesky $i\gamma_{j}\omega$ at the denominator), so technically this is not a linear medium. However, the complex $\tilde{\mathbf{P}}$ is linearly proportional to the complex $\tilde{\mathbf{E}}$, so in an odd way, we can see this as a linear medium with *complex* [[electric susceptibility]] $\tilde{\chi}_{e}$ such that
$$\tilde{\mathbf{P}}=\varepsilon_{0}\tilde{\chi}_{e}\tilde{\mathbf{E}}$$
Similarly, we can define a *complex* permittivity $\tilde{\varepsilon}$ and a *complex* relative permittivity
$$\tilde{\varepsilon}_{r}=\frac{\tilde{\varepsilon}}{\varepsilon_{0}}=1+ \frac{Nq^{2}}{m\varepsilon_{0}}\sum_{j} \frac{f_{j}}{\omega_{j}^{2}-\omega ^{2}-i\gamma_{j}\omega}\tag{1}$$
Now, in most cases the imaginary term is negligible, stamped out by $\omega ^{2}_{j}-\omega ^{2}$. However, when $\omega$ gets closer to $\omega_{j}$, that difference approaches zero and the imaginary term is the only thing that is left. This has some major consequences, though before we examine them, let's discuss what we ended up with.

In a dispersive medium, the wave equation now reads
$$\nabla ^{2}\tilde{\mathbf{E}}=\tilde{\varepsilon}\mu_{0}\frac{ \partial ^{2}\tilde{\mathbf{E}} }{ \partial t^{2} } $$
of [[plane wave]] solution
$$\tilde{\mathbf{E}}(x,t)=\tilde{\mathbf{E}}_{0}e^{i(\tilde{k}x-\omega t)}$$
and complex [[wavenumber]] $\tilde{k}=\sqrt{ \tilde{\varepsilon}\mu_{0} }\ \omega$. We can split this in real and imaginary parts $\tilde{k}=k+i\kappa$ to write
$$\tilde{\mathbf{E}}(x,t)=\tilde{\mathbf{E}}_{0}e^{-\kappa x}e^{i(kx-\omega t)}$$
which is an attenuated wave. This is a logical consequence of us adding a damping force. The [[irradiance]] of the wave is proportional to the square of the electric field, $I\propto E^{2}$, so it is attenuated like $I\propto e^{-2\kappa x}$. Because of this, we call $\alpha\equiv2\kappa$ the **absorption coefficient**. It's reciprocal, $1/\alpha$, is called the **penetration depth** of the wave. It is a characteristic length for the suppression of the wave, similar to skin depth, but for irradiance. The [[phase velocity]] is $v_{p}=\omega/k$ and the [[refractive index]] is $n=ck/\omega$. This is all quite similar to what happens to a wave incident on a perfect [[conductor]], although the interpretation of the coefficients is different since the dampening here is due to some arbitrary force instead of rearrangement of free charge.

For most materials, there's not much else we can say without diving deeper into the nature of electronic structure. However, for gases the second term in $(1)$ is small; not enough to delete it completely, but enough to justify approximating the square root in $\tilde{k}=\sqrt{ \tilde{\varepsilon}\mu_{0} }\ \omega=\sqrt{ \varepsilon_{0}\tilde{\varepsilon}_{r}\mu_{0} }\ \omega$ with the first couple of terms in its [[Binomial theorem|binomial expansion]]:
$$\sqrt{ 1+x }\simeq1+ \frac{x}{2}$$
This means, since $\mu_{0}=1/\varepsilon_{0}c^{2}$,
$$\tilde{k}=\sqrt{ \frac{\tilde{\varepsilon}}{\varepsilon_{0}c^{2}} }\ \omega=\frac{\omega}{c}\sqrt{ \tilde{\varepsilon}_{r} }\simeq \frac{\omega}{c}\left[ 1+ \frac{Nq^{2}}{2m\varepsilon_{0}}\sum_{j} \frac{f_{j}}{\omega_{j}^{2}-\omega ^{2}-i\gamma_{j}\omega} \right]$$
and so
$$n=\frac{ck}{\omega}\simeq 1+ \frac{Nq^{2}}{2m\varepsilon_{0}}\sum_{j} \frac{f_{j}(\omega ^{2}_{j}-\omega ^{2})}{(\omega_{j}^{2}-\omega ^{2})^{2}+\gamma ^{2}_{j}\omega ^{2}}$$
and
$$\alpha=2\kappa \simeq \frac{Nq^{2}\omega ^{2}}{m\varepsilon_{0}c}\sum_{j} \frac{f_{j}\gamma_{j}}{(\omega_{j}^{2}-\omega ^{2})^{2}+\gamma ^{2}_{j}\omega ^{2}}$$
These quantities, $n$ and $\alpha$, generally behave pretty nicely, with $n$ increasing monotonically with frequency. However, as we've hinted at before, $\omega_{j}^{2}-\omega ^{2}$ cancels out when $\omega_{j}\simeq \omega$, leaving only the damping term. When oscillations frequencies of different sources match, we get a **[[resonance]]**, which in general causes some weird behavior to crop up. This is the case here also, as when these two frequencies match, the refractive index crashes down immediately to the point it goes below 1. Simultaneously, the absorption coefficients spikes up, as you can see in the figure.

:::image
![[AnomalousDispersion.png]]
Note that the plot shows $n-1$, not $n$. From *Introduction to Electrodynamics 4th ed., Griffiths*
:::

This resonant behavior is called **[[anomalous dispersion]]**. When light is shining on a material at precisely resonant frequency, it will almost entirely be absorbed, as seen by the high $\alpha$ value. This is a consequence of how a driven oscillator works, where the "efficiency" is maximized when the driving frequency is equal to the damping frequency. In this case, the maximum amount of energy is dissipated, as seen by the peak of $\alpha$ in $\omega_{j}=\omega$. Also, the fact that $n$ falls below one in this range implies that the phase speed of the wave $v_{p}=c/n$ is *greater than lightspeed*. At first glance, this is unacceptable. The speed of light is one of the few untouchable tenets of physics alongside the conservation of [[energy]]. However, it's not actually a problem. The reason is the the "speed" of a wave isn't really a speed. Or rather, it is, but the definition is largely invented. There's nothing actually physical moving at the phase speed, since the very concept of speed for something like a wave doesn't even make that much sense. *What* is moving anyway? Waves are delocalized, spread out over a large region of space and without a clear center or "core". All concepts of "speed" on a wave are fundamentally just a suggestion, because they don't relate to any real physical object. As such, it's not really a problem for the phase speed to the exceed lightspeed. The root cause is that the actual physical object, the *energy* transported by the wave, does *not* move at phase speed[^2].

Outside of resonances, behavior is pretty typical. We can ignore the damping term to get
$$n=1+ \frac{Nq^{2}}{2m\varepsilon_{0}}\sum_{j} \frac{f_{j}}{\omega_{j}^{2}-\omega ^{2}}$$

Resonance frequencies are therefore "landmines" in the field of the electromagnetic spectrum. These appear pretty randomly throughout the spectrum, as the logic behind them is not at all easy to understand. For most transparent materials, the resonant frequency nearest to the visible spectrum is in the ultraviolet.

[^1]: Actually, only the space where the field is nonzero needs to be like this. We don't really care about whether the susceptibility is constant or not if there is no field at all. If the field is created within the dielectric and becomes negligible before coming out of the surface, we might as well call all space homogeneous.

[^2]: You might assume that [[group velocity]] must be the "correct one", then. You'd also be wrong, though, as group velocity can *also* exceed the speed of light near a resonance.
