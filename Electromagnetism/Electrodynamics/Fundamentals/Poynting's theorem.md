---
wiki-publish: true
---
**Poynting's theorem** is a result expressing conservation of [[energy]] in electrodynamics.

> [!info] Poynting's theorem
> Given a volume $\mathcal{V}$, the stored electromagnetic energy $U$ changes at a [[power|rate]] $P$ given by the [[work]] done on the [[electric charge|charges]] within the volume, minus the rate at which energy leaves the volume. In integral form it reads
> $$P=\frac{ \partial U }{ \partial t } =-\frac{ \partial  }{ \partial t } \int_{\mathcal{V}}u(\mathbf{r})\ d\tau-\oint_{\mathcal{S}}\mathbf{S}\cdot d\mathbf{a}$$
> where $u(\mathbf{r})$ is the electromagnetic energy density of [[electric field]] $\mathbf{E}$ and [[magnetic field]] $\mathbf{B}$
> $$u=\frac{1}{2}\left( \varepsilon_{0}E^{2}+ \frac{1}{\mu_{0}}B^{2} \right)$$
> $\mathcal{S}$ is the bounding [[Surface|surface]] of $\mathcal{V}$ and $\mathbf{S}$ is the [[Poynting vector]].
> 
> In differential form it reads
> $$\mathbf{E}\cdot \mathbf{J}=-\frac{ \partial u(\mathbf{r}) }{ \partial t }-\nabla\cdot\mathbf{S}$$

> [!quote]- Proof
> We begin by looking at the work being done by the Lorentz force on a [[Electric charge|point charge]] $q$ moving at velocity $\mathbf{v}$ over a line element $d\mathbf{s}=\mathbf{v}dt$:
> $$dW=q(\mathbf{E}+\mathbf{v}\times \mathbf{B})\cdot d\mathbf{s}=q\mathbf{E}\cdot \mathbf{v}dt+q\cancel{ (\mathbf{v}\times \mathbf{B})\cdot \mathbf{v}dt }=q\mathbf{E}\cdot d\mathbf{s}$$
> To go from point charges to charge distributions, we can pick a tiny volume $d\tau$ with charge $dq=\rho d\tau$. If this charge element moves at a velocity $\mathbf{v}$, the work over a time $dt$ is
> $$dW=dq\mathbf{E}\cdot \mathbf{v}dt=\rho d\mathcal{V}\ \mathbf{E}\cdot \mathbf{v}dt=\mathbf{E}\cdot \rho \mathbf{v}\ d\mathcal{V}dt=\mathbf{E}\cdot \mathbf{J}\ d\tau dt$$
> since $\rho \mathbf{v}=\mathbf{J}$. $\mathbf{E}\cdot \mathbf{J}$ must the work done per unit time, per unit volume. If we "divide" by $dt$ and integrate over the volume we get the [[power]]
> $$P=\frac{dW}{dt}=\int_{\mathcal{V}}\mathbf{E}\cdot \mathbf{J}\ d\tau\tag{1}$$
> We can elaborate on $\mathbf{E}\cdot \mathbf{J}$ by expressing $\mathbf{J}$ through the [[Ampere's law|Ampere-Maxwell law]]:
> $$\begin{align}
> \mathbf{E}\cdot \mathbf{J}&=\mathbf{E}\cdot \frac{\nabla\times\mathbf{B}}{\mu_{0}}-\varepsilon_{0}\mathbf{E}\cdot\frac{ \partial \mathbf{E} }{ \partial t } \\
> \left( \mathbf{E}\cdot \frac{ \partial \mathbf{E} }{ \partial t } =\frac{1}{2}\frac{ \partial E^{2} }{ \partial t }  \right)&=\frac{1}{\mu_{0}} \mathbf{E}\cdot(\nabla\times\mathbf{B})- \frac{\varepsilon_{0}}{2}\frac{ \partial E^{2} }{ \partial t }  \\
> &=\frac{1}{\mu_{0}} [\mathbf{B}\cdot(\nabla\times\mathbf{E})- \nabla\cdot(\mathbf{E}\times \mathbf{B})]- \frac{\varepsilon_{0}}{2} \frac{ \partial E^{2} }{ \partial t }  \\
> &=\frac{1}{\mu_{0}} \left[ -\mathbf{B}\cdot \frac{ \partial \mathbf{B} }{ \partial t } - \nabla \cdot(\mathbf{E}\times \mathbf{B}) \right]- \frac{\varepsilon_{0}}{2}\frac{ \partial E^{2} }{ \partial t } \\
> \left( \mathbf{B}\cdot \frac{ \partial \mathbf{B} }{ \partial t } =\frac{1}{2}\frac{ \partial B^{2} }{ \partial t }  \right)&=- \frac{1}{2\mu_{0}}\frac{ \partial B^{2} }{ \partial t } - \frac{\varepsilon_{0}}{2}\frac{ \partial E^{2} }{ \partial t } -\nabla\cdot \mathbf{S}
> \end{align}$$
> where we expanded
> $$\nabla \cdot(\mathbf{E}\times \mathbf{B})=\mathbf{B}\cdot(\nabla\times \mathbf{E})-\mathbf{E}\cdot(\nabla\times \mathbf{B})$$
> and rearranged to find $\mathbf{E}\cdot(\nabla\times \mathbf{B})$, used [[Faraday's law]] and defined the [[Poynting vector]]
> $$\mathbf{S}=\frac{1}{\mu_{0}}\mathbf{E}\times \mathbf{B}$$
> 
> If we extract and merge the time derivative from the first two terms, we are left with the electromagnetic energy density by volume $u$:
> $$- \frac{1}{2\mu_{0}}\frac{ \partial B^{2} }{ \partial t } - \frac{\varepsilon_{0}}{2}\frac{ \partial E^{2} }{ \partial t }=- \frac{1}{2}\frac{ \partial  }{ \partial t } \left( \frac{1}{\mu_{0}}B^{2} + \varepsilon_{0}E^{2} \right)=-\frac{ \partial u }{ \partial t }$$
> Which means
> $$\mathbf{E}\cdot \mathbf{J}=-\frac{ \partial u }{ \partial t } -\nabla\cdot \mathbf{S}$$
> which is the differential expression of the theorem. If we plug this back into $(1)$, we get
> $$P=-\frac{ \partial  }{ \partial t } \int_{V}u\ d\tau-\int_{V}\nabla\cdot\mathbf{S}=-\frac{ \partial  }{ \partial t } \int_{V}u\ d\tau-\oint_{S}\mathbf{S}\cdot d\mathbf{a}$$
> where we used the [[Divergence theorem|divergence theorem]]. This completes the proof.

The two integrals can be interpreted individually: the first is the *stored* energy[^1], of which we take the time derivative of, whereas the second is the *transfer* of energy from inside the volume $\mathcal{V}$ to outside, as determined by checking what goes through the boundary $\mathcal{S}$.

It is equivalent in nature to the mechanical [[work-energy theorem]] and binds *stored* energy to *transported* energy as a consequence of energy conservation: if something goes out, it must be removed from what's inside. It is in large part the same statement as the continuity equation for [[electric current]] $\nabla\cdot\mathbf{J}=-\frac{ \partial \rho }{ \partial t }$, except instead of charge we have energy. In fact, if no work is being done on the charges, then $\mathbf{E}\cdot \mathbf{J}=0$ and we get $\nabla\cdot \mathbf{S}=-\frac{ \partial u }{ \partial t }$. This confirms that the Poynting vector is an "energy current": it represents the flow of energy and therefore plays a pivotal role in energy conservation.

[^1]: *Where* the energy is stored is a whole other problem. Electrodynamics alone does not give a really satisfactory answer and you could realistically place it anywhere, be it in fields, matter or charges, but since field theory relies on this, it is best to think of it as being stored in the fields.