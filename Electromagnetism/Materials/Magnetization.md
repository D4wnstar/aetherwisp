**Magnetization** is the phenomenon where a [[paramagnet]] or [[diamagnet]] that is subject to a [[magnetic field]] will develop an [[magnetic dipole moment]] for as long as the field is active.

A measure of magnetization can be given as
$$\mathbf{M}\equiv\text{magnetic dipole moment per unit volume}\qquad\left[ \frac{\text{A}}{\text{m}^{2}} \right]$$
### Magnetic field of a magnetized object
The [[magnetic vector potential]] of a [[Magnetic dipole]] of [[magnetic dipole moment|moment]] $\mathbf{m}$ is
$$\mathbf{A}(\mathbf{r})=\frac{\mu_{0}}{4\pi} \frac{\mathbf{m}\times \hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}}$$
In the magnetized object, each volume element $d\tau'$ carries a moment $\mathbf{m}=\mathbf{M}d\tau'$ so
$$\mathbf{A}(\mathbf{r})=\frac{\mu_{0}}{4\pi}\int \frac{\mathbf{M}(\mathbf{r}')\times \hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}}\ d\tau'$$
We could find the [[curl]] of this and get the field itself, but we can use
$$\nabla'\left( \frac{1}{\mathfrak{r}} \right)=\frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}}$$
to cast this integral in a more illuminating form. We get
$$\mathbf{A}(\mathbf{r})=\frac{\mu_{0}}{4\pi}\int\left[ \mathbf{M}(\mathbf{r}')\times\nabla'\left( \frac{1}{\mathfrak{r}} \right) \right]\ d\tau'$$
[[Integrazione per parti|Integrating by parts]] we get
$$\mathbf{A}(\mathbf{r})=\frac{\mu_{0}}{4\pi}\left\{ \int \frac{1}{\mathfrak{r}}[\nabla'\times \mathbf{M}(\mathbf{r}')]\ d\tau' -\int \nabla'\times\frac{[\mathbf{M}(\mathbf{r}')]}{\mathfrak{r}}\ d\tau' \right\}$$
The second integral can be turned into a [[Integrale su una superficie|surface integral]], so
$$\mathbf{A}(\mathbf{r})= \frac{\mu_{0}}{4\pi}\int \frac{1}{\mathfrak{r}}[\nabla'\times \mathbf{M}(\mathbf{r}')]\ d\tau' -\frac{\mu_{0}}{4\pi}\oint \frac{1}{\mathfrak{r}}[\mathbf{M}(\mathbf{r}')\times d\mathbf{a}']$$
The first term is essentially the potential of a volume [[Electric current|current]] density $\mathbf{J}$:
$$\boxed{\mathbf{J}_{b}=\nabla\times\mathbf{M}}$$
and the second one looks like the potential of a surface current density $\mathbf{K}$:
$$\boxed{\mathbf{K}_{b}=\mathbf{M}\times \hat{\mathbf{n}}}$$
so if we plug these in
$$\boxed{\mathbf{A}(\mathbf{r})=\frac{\mu_{0}}{4\pi}\int_{\mathcal{V}} \frac{\mathbf{J}_{b}}{\mathfrak{r}}\ d\tau'+ \frac{\mu_{0}}{4\pi}\int_{\mathcal{S}} \frac{\mathbf{K}_{b}}{\mathfrak{r}}\ da'}$$
The currents $\mathbf{J}_{b}$ and $\mathbf{K}_{b}$ are called the **bound currents** and are completely analogous to the bound charges caused by [[dielectric polarization]].

> [!example] Uniformly magnetized sphere
> Consider a sphere of radius $R$ with a uniform magnetization $\mathbf{M}$. For simplicity, choose the $z$ axis to be aligned with $\mathbf{M}$. Thus, we have
>
>$$\mathbf{J}_{b}=\nabla\times\mathbf{M}=0,\qquad \mathbf{K}_{b}=\mathbf{M}\times \hat{\mathbf{n}}=M\sin \theta\ \hat{\boldsymbol{\phi}}$$
>Now, the magnetic field produces by a uniform surface charge $\sigma$ corresponds with the current surface density
>$$\mathbf{K}=\sigma \mathbf{v}=\sigma \omega R\sin \theta \hat{\boldsymbol{\phi}}$$
>but that means that the field of a uniformly magnetized sphere is equal to that of spinning charged sphere with $\mathbf{M}=\sigma R\boldsymbol{\omega}$. We already know what the field of a spinning sphere is, so we get
>$$\mathbf{B}=\frac{2}{3}\mu_{0}\mathbf{M}$$
>inside the sphere, whereas outside it is equal to that of a perfect magnetic dipole with
>$$\mathbf{m}=\frac{4}{3}\pi R^{3}\mathbf{M}$$
### In linear media
Most substances exhibit a linear proportionality between the magnetic field applied onto them and the magnetization they show. This relation is usually expressed in terms of the [[auxiliary field]] $\mathbf{H}$ instead of $\mathbf{B}$:
$$\mathbf{M}=\chi_{m}\mathbf{H}$$
where $\chi_{m}$ is the [[magnetic susceptibility]]. Reversing the relation to get $\mathbf{B}$ from $\mathbf{H}$ we get:
$$\mathbf{B}=\mu_{0}(\mathbf{H}+\mathbf{M})=\mu_{0}(1+\chi_{m})\mathbf{H}=\mu \mathbf{H}$$
with $\mu$ the [[permeability]] of the substance.

The volume bound current density in a homogeneous linear material is proportional to the free current:
$$\mathbf{J}_{b}=\nabla\times\mathbf{M}=\nabla \times(\chi_{m}\mathbf{H})=\chi_{m}\mathbf{J}_{f}$$
In particular, unless the free current flows *inside* the material, then there will be no bound current.