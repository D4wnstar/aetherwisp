**Dielectric polarization** is the phenomenon where a [[dielectric]] that is subject to an [[electric field]] will develop an [[electric dipole moment]] for as long as the field is active. If the [[molecule|molecules]] that make up the dielectric are either symmetric or asymmetric but randomly ordered (such as in a liquid), the direction of the moment will be that of the field. In other situations, like in a [[crystal]], the orientation will differ.

A measure of polarization can be given as
$$\mathbf{P}\equiv \text{electric dipole moment per unit volume}\qquad\left[ \frac{\text{C}}{\text{m}^{2}} \right]$$
### Electric field of a polarized object
Suppose we have a polarized object with a known $\mathbf{P}$. Since the charges within the object are now misaligned, the object as a whole behaves as one big [[electric dipole]] and therefore produces an electric field. The field of a single dipole is known, so we can reach the total field by examining that of each single dipole that makes up the dielectric. Starting from the [[electric potential]], we have
$$V(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{\mathbf{p}\cdot \hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}}$$
where $\boldsymbol{\mathfrak{r}}$ is the unit vector going from the dipole to the point where we are evaluating the potential. Our dipole moment is $\mathbf{p}=\mathbf{P}\ d\tau'$ so
$$V(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{\mathcal{V}} \frac{\mathbf{P}(\mathbf{r}')\cdot \hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}} d\tau'$$
Now, since[^1]
$$\nabla'\left( \frac{1}{\mathfrak{r}} \right)=\frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}}$$
we have
$$V(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{\mathcal{V}}\mathbf{P}(\mathbf{r}')\cdot \nabla'\left( \frac{1}{\mathfrak{r}} \right)\ d\tau'$$
Using [[Integrazione per parti|integration by parts]] we have
$$V=\frac{1}{4\pi\varepsilon_{0}}\left[ \int_{\mathcal{V}}\nabla'\cdot \left( \frac{\mathbf{P}}{\mathfrak{r}} \right)\ d\tau'-\int_{\mathcal{V}} \frac{1}{\mathfrak{r}}(\nabla'\cdot \mathbf{P})\ d\tau' \right]$$
The first integral obeys the [[Teorema della divergenza|divergence theorem]], so
$$V=\frac{1}{4\pi\varepsilon_{0}}\oint_{\mathcal{S}} \frac{1}{\mathfrak{r}}\mathbf{P}\cdot d\mathbf{a}'- \frac{1}{4\pi\varepsilon_{0}}\int_{\mathcal{V}} \frac{1}{\mathfrak{r}}(\nabla'\cdot \mathbf{P})\ d\tau'$$
The first terms has the form of the potential of a surface charge
$$\boxed{\sigma_{b}=\mathbf{P}\cdot \hat{\mathbf{n}}}$$
and the second one that of the potential of a volume charge
$$\boxed{\rho_{b}=-\nabla'\cdot \mathbf{P}}$$
and so we get
$$\boxed{V=\frac{1}{4\pi\varepsilon_{0}}\oint_{\mathcal{S}} \frac{\sigma_{b}}{\mathfrak{r}}\ da'+\frac{1}{4\pi\varepsilon_{0}}\int_{\mathcal{V}} \frac{\rho_{b}}{\mathfrak{r}}\ d\tau'}$$
Clearly, then, the potential of a polarized material is the result of both a surface charge and a volume charge. Since these charges are in a dielectric and therefore not free to move, they are called **bound charges**. If we can find the bound charges, we can get the potential and then the field.

> [!example] Uniformly polarized sphere
> For a uniformly polarized sphere of radius $R$, the volume charge density is zero as the gradient of a constant polarization is zero. The surface charge is $\sigma_{b}=\mathbf{P}\cdot \hat{\mathbf{n}}=P\cos \theta$, where $\theta$ is the usual coordinate in [[spherical coordinates]]. We might as well put the $z$ axis on the axis of polarization to make $\theta$ have its usual meaning. Thus, we're looking for the field of a sphere with surface charge density $P\cos \theta$. This can be found by solving [[Laplace's equation]] through [[separation of variables]]. We get
> $$V(\mathbf{r})=\begin{cases}
\frac{P}{3\varepsilon_{0}}r\cos \theta \qquad &r\leq R \\
\frac{P}{3\varepsilon_{0}} \frac{R^{3}}{r^{2}}\cos \theta \qquad &r\geq R
\end{cases}$$
>Since $r\cos \theta=z$, the field inside the sphere is uniform and is
>$$\mathbf{E}_\text{in}=-\frac{P}{3\varepsilon_{0}}\hat{\mathbf{z}}=- \frac{1}{3\varepsilon_{0}}\mathbf{P}$$
>The field outside is that of a perfect dipole
>$$\mathbf{E}_\text{out}=\frac{1}{4\pi\varepsilon_{0}} \frac{\mathbf{p}\cdot \hat{\mathbf{r}}}{r^{2}}$$
>whose dipole moment is equal to the total dipole moment of the sphere
>$$\mathbf{p}=\frac{4}{3}\pi R^{3}\mathbf{P}$$
### Bound charges
Bound charges are a net total charged caused by the presence of polarization. The many dipoles that constitute the material align themselves with the field and, *if the field is uniform*, the positive end of one cancels out the negative end of the one in front of it. This chain of canceling goes until the two edges of the chain, at which point we are left with a positive charge on end and a negative charge on the other, with net neutral in between. The charge is the same as the one of each little dipole, but the distance in between the two edges is much larger.

The amount of bound charge is given by the total of each chain. Since the charge in neutral in the middle of the chain, the only charges here are on the surface. Consider a cylinder of cross-section $A$, length $d$ and polarization $P$. The polarization is assumed to be running through the cylinder. Thus, the dipole moment is $p=PAd$, but it's also $p=qd$, so we have $q=PA$. Clearly, the total charge is dependent on the area and the polarization, just as we expected. This area depends on whether the polarization is perpendicular with the surface or not. In the cylinder's case, $\mathbf{P}$ and $\hat{\mathbf{n}}$ are perpendicular, but what if they aren't? Say the surface is oblique by an angle $\theta$ with respect to $\mathbf{P}$. Then, the surface density is
$$\sigma_{b}=\frac{q}{A_{end}}=\frac{q}{A}\cos \theta=P\cos \theta=\mathbf{P}\cdot \hat{\mathbf{n}}$$
which is what we found before.

> [!result] **Bound surface charge origin**
> The bound surface charge comes from the alignment of the single dipoles and their internal cancellation except at the very edges, on the surface of the object.

*If the field is not uniform*, then the cancellation in between each dipole pair in the chain doesn't quite occur, as the dipole moment of each little dipole changes depending on how strong the field is. This creates pockets of nonzero charge internally. But charge must be conserved, and so if we "push" charges to the surface with density $\sigma=\mathbf{P}\cdot \hat{\mathbf{n}}$, the internal ones must be as a whole equal and opposite to those. Thus, the total internal charge must be
$$\int_{\mathcal{V}}\rho_{b}\ d\tau=-\oint_{\mathcal{S}}\mathbf{P}\cdot d\mathbf{a}=-\int_{\mathcal{V}}(\nabla \cdot \mathbf{P})\ d\tau$$
using the divergence theorem. This is independent on geometry as we put no bounds on what the volume $\mathcal{V}$ could be, so we can equate the two integrands to get
$$\rho_{b}=-\nabla \cdot \mathbf{P}$$
which again proves the previous result.

> [!result] Bound volume charge origin
> The bound volume charge comes from the incomplete internal cancellation of dipoles within chains due to the nonuniformity of the external electric field. 
### In linear media
![[Dielectric#Linear dielectrics]]

[^1]: The apostrophe denotes that differentiation is done with respect to the source coordinates.