**Maxwell's equations** are four equations that determine the [[divergence]] and [[curl]] of the [[Electric field|electric]] and [[magnetic field]]. In the vacuum they are
$$\boxed{\begin{align}
\nabla\cdot\mathbf{E} & =\frac{\rho}{\varepsilon_{0}} &
\nabla\times\mathbf{E} & = -\frac{ \partial \mathbf{B} }{ \partial t } \\
\nabla\cdot\mathbf{B} & =\mathbf{0} &
\nabla\times\mathbf{B} &= \mu_{0}\mathbf{J}+\mu_{0}\varepsilon_{0}\frac{ \partial \mathbf{E} }{ \partial t } 
\end{align}}$$
and together with the boundary conditions $\mathbf{E}\to 0$ and $\mathbf{B}\to  0$ approaching infinity, they uniquely determine the two fields. $\rho$ is a volume [[electric charge]] density and $\mathbf{J}$ is a volume [[electric current]] density. $\varepsilon_{0}$ and $\mu_{0}$ are the [[Costante dielettrica del vuoto|permittivity]] and [[permeability of free space]] respectively.

These laws, alongside the [[Lorentz force]], explain the entirety of electromagnetic phenomena. Maxwell's equations tell you how *charges* produces *fields*, whereas the Lorentz force tells you how *fields* affect *charges*. With both, the circle is complete. This is true in both electro/magnetostatics and electrodynamics.
### In the vacuum
The laws above are correct in the vacuum. However, in the special case of a "true" vacuum, that is, there is truly nothing in that region of space, not even charges, they become
$$\begin{align}
\nabla\cdot\mathbf{E} & =0 &
\nabla\times\mathbf{E} & = -\frac{ \partial \mathbf{B} }{ \partial t } \\
\nabla\cdot\mathbf{B} & =\mathbf{0} &
\nabla\times\mathbf{B} &=\mu_{0}\varepsilon_{0}\frac{ \partial \mathbf{E} }{ \partial t } 
\end{align}$$
This is particularly interesting since it shows that, in a way, the electric and magnetic fields are one and the same. In fact, [[Faraday's law]] shows that the space derivative of an electric field is the time derivative of a magnetic field, and [[Ampere's law]] (the corrected form) shows that the space derivative of a magnetic field is the time derivative of an electric field. The only differences are the signs and the constants $\mu_{0}\varepsilon_{0}$ (which only appear in SI units).
### In matter
It is possible to rewrite Maxwell's equation in a more convenient manner when dealing with [[Dielectric polarization|polarized]] and [[Magnetization|magnetized]] matter. We already know that polarization produces a bound charge density $\rho_{b}$ and magnetization a bound current density $\mathbf{J}_{b}$. The only thing we're missing is to consider what happens when polarization and magnetization change in time. A changing magnetization, at most, changes $\mathbf{J}_{b}$, so it doesn't add any new pieces, but a changing polarization moves the $\rho_{b}$, which is to say it *produces a current*. This is emphatically *not* part of $\mathbf{J}_{b}$: it is a completely new piece of the puzzle. See, when polarization occurs, a certain amount of charges are moved such that they are plastered over a surface[^1] on one end ($\sigma_{b}$) and some on the other ($-\sigma_{b}$). When the polarization $\mathbf{P}$ changes, these charges increase or decrease depending on the intensity of polarization, giving a net current
$$dI=\frac{ \partial \sigma_{b} }{ \partial t } da_{\perp}=\frac{ \partial P }{ \partial t } da_{\perp}$$
The current density induced by a changing polarization is
$$\mathbf{J}_{p}=\frac{ \partial \mathbf{P} }{ \partial t } $$
and is called the **polarization current**. It obeys continuity:
$$\nabla\cdot\mathbf{J}_{p}=\nabla \cdot \frac{\partial\mathbf{P}}{\partial t}=\frac{ \partial  }{ \partial t } (\nabla\cdot\mathbf{P})=- \frac{ \partial \rho_{b} }{ \partial t } $$
This allows us to break down charge density and current density into their constituent parts. Where charge density is expressed with two terms:
$$\rho=\rho_{f}+\rho_{b}=\rho_{f}-\nabla\cdot\mathbf{P}$$
current density is expressed in *three* terms:
$$\mathbf{J}=\mathbf{J}_{f}+\mathbf{J}_{b}+\mathbf{J}_{p}=\mathbf{J}_{f}+\nabla\times\mathbf{M}+\frac{ \partial \mathbf{P} }{ \partial t } $$
[[Gauss' law]] is now written as
$$\nabla\cdot\mathbf{E}=\frac{1}{\varepsilon_{0}}(\rho_{f}-\nabla\cdot\mathbf{P})$$
or, using [[electric displacement]],
$$\nabla\cdot\mathbf{D}=\rho_{f}$$
where $\mathbf{D}=\varepsilon_{0}\mathbf{E}+\mathbf{P}$. Meanwhile, the corrected [[Ampere's law]] becomes
$$\nabla\times\mathbf{B}=\mu_{0}\left( \mathbf{J}_{f}+\nabla\times\mathbf{M}+\frac{ \partial \mathbf{P} }{ \partial t }  \right)+\mu_{0}\varepsilon_{0}\frac{ \partial \mathbf{E} }{ \partial t } $$
or, using the [[auxiliary field]],
$$\nabla\times\mathbf{H}=\mathbf{J}_{f}+\frac{ \partial \mathbf{D} }{ \partial t } $$
where $\mathbf{H}=(1/\mu_{0})\mathbf{B}-\mathbf{M}$. [[Faraday's law]] and $\nabla\cdot\mathbf{B}=0$ are not affected by these changes, as they do not depend on $\rho$ or $\mathbf{J}$. Thus, Maxwell's equations for materials are
$$\boxed{\begin{align}
\nabla\cdot\mathbf{D}&=\rho_{f} & \nabla\times\mathbf{E}&=-\frac{ \partial \mathbf{B} }{ \partial t }  \\
\nabla\cdot\mathbf{B} & =0 & \nabla\times\mathbf{\mathbf{H}} & =\mathbf{J}_{f}+\frac{ \partial \mathbf{D} }{ \partial t } 
\end{align}}$$
or in integral form
$$\begin{align}
\oint_{\mathcal{S}}\mathbf{D}\cdot d\mathbf{a} & =Q_{f,enc} & \oint_{\gamma}\mathbf{E}\cdot d\mathbf{r} & =- \frac{d}{dt} \int_{\mathcal{S}}\mathbf{B}\cdot d\mathbf{a} \\
\oint_{\mathcal{S}}\mathbf{B}\cdot d\mathbf{a} & =0 & \oint_{\gamma}\mathbf{H}\cdot d\mathbf{r} & =I_{f,enc}+\frac{d}{dt} \int_{\mathcal{S}}\mathbf{D}\cdot d\mathbf{a}
\end{align}$$
where the two left ones are integrated over any closed [[Superficie|surface]] $\mathbf{S}$ and the two right ones are for any closed surface bounded by a closed [[curva|line]] $\gamma$.
### Boundary conditions
In general, all the fields used in Maxwell's equations will be discontinuous over a surface charge or current. We can find the boundary conditions by applying the integral equations in matter.

Take a thin Gaussian pillbox straddling a surface charge density $\sigma_{f}$. From the displacement equation we get
$$\mathbf{D}_{1}\cdot \mathbf{a}-\mathbf{D}_{2}\cdot \mathbf{a}=\sigma_{f}a$$
where the positive direction for $\mathbf{a}$ is from 2 towards 1. The edge of the pillbox contributes nothing as it goes to zero as the thickness of the pillbox does. Volume charge densities also do not contribute. Thus, we are left with
$$D_{1}^{\perp}-D_{2}^{\perp}=\sigma_{f}$$
The same logic can be applied to the magnetic field equation to find
$$B_{1}^{\perp}-B_{2}^{\perp}=0$$

For the other two equations, we instead use an Amperian loop crossing a surface current density $\mathbf{K}_{f}$. From the electric field equation we get
$$\mathbf{E}_{1}\cdot \mathbf{l}-\mathbf{E}_{2}\cdot \mathbf{l}=-\frac{d}{dt} \int_{\mathcal{S}}\mathbf{B}\cdot d\mathbf{a}$$
The flux vanishes as we make the loop smaller and smaller, as do the contributions at the edges of $\oint \mathbf{E}\cdot \mathbf{r}$. We then get
$$\mathbf{E}_{1}^{\parallel}-\mathbf{E}_{2}^{\parallel}=\mathbf{0}$$
The same logic applied to the auxiliary field implies
$$\mathbf{H}_{1}\cdot \mathbf{l}-\mathbf{H}_{2}\cdot \mathbf{l}=I_{f,enc}$$
where $I_{f,enc}$ is the free current passing through the Amperian loop. No volume current density contributes for an arbitrarily small loop, but a surface current does. If $\hat{\mathbf{n}}$ is normal vector of the surface density, point upwards so that $\hat{\mathbf{n}}\times \mathbf{l}$ is normal to the Amperian loop, then
$$I_{f,enc}=\mathbf{K}_{f}\cdot(\hat{\mathbf{n}}\times \mathbf{l})=(\mathbf{K}_{f}\times \hat{\mathbf{n}})\cdot \mathbf{l}$$
and hence
$$\mathbf{H}_{1}^{\parallel}-\mathbf{H}_{2}^{\parallel}=\mathbf{K}_{f}\times \hat{\mathbf{n}}$$
Summarized, these are
$$\boxed{\begin{align}
D_{1}^{\perp}-D_{2}^{\perp} & =\sigma_{f} & \mathbf{E}_{1}^{\parallel} -\mathbf{E}_{2}^{\parallel} & =\mathbf{0} \\
B_{1}^{\parallel}-B_{2}^{\parallel} & =0 & \mathbf{H}_{1}^{\parallel}-\mathbf{H}_{2}^{\parallel} & =\mathbf{K}_{f}\times \hat{\mathbf{n}}
\end{align}}$$
In the case of linear media, these can be expressed in terms of $\mathbf{E}$ and $\mathbf{B}$ alone:
$$\boxed{\begin{align}
\varepsilon_{1}E_{1}^{\perp}-\varepsilon_{2}E_{2}^{\perp} & =\sigma_{f} & \mathbf{E}_{1}^{\parallel}-\mathbf{E}_{2}^{\parallel} & =\mathbf{0} \\
B_{1}^{\perp}-B_{2}^{\perp} & =0 & \frac{1}{\mu_{1}}\mathbf{B}_{1}^{\parallel}- \frac{1}{\mu_{2}}\mathbf{B}_{2}^{\parallel}&=\mathbf{0}
\end{align}}$$

[^1]: For correctness' sake, the charges themselves only *align* with the polarization, but don't move much. If they did all actually move to the surface, we'd be working with [[conductor|conductors]] and not with polarized [[dielectric|dielectrics]]. Still, this alignment motion is sufficient to produce a small current.