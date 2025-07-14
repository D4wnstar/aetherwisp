---
wiki-publish: true
---
**Maxwell's equations** are four equations that determine the [[divergence]] and [[curl]] of the [[Electric field|electric]] and [[magnetic field]]. In the vacuum they are
$$\boxed{\begin{align}
\nabla\cdot\mathbf{E} & =\frac{\rho}{\varepsilon_{0}} &
\nabla\times\mathbf{E} & = -\frac{ \partial \mathbf{B} }{ \partial t } \\
\nabla\cdot\mathbf{B} & =0 &
\nabla\times\mathbf{B} &= \mu_{0}\mathbf{J}+\mu_{0}\varepsilon_{0}\frac{ \partial \mathbf{E} }{ \partial t } 
\end{align}}$$
and together with the boundary conditions $\mathbf{E}\to 0$ and $\mathbf{B}\to  0$ approaching infinity, they uniquely determine the two fields. $\rho$ is a volume [[electric charge]] density and $\mathbf{J}$ is a volume [[electric current]] density. $\varepsilon_{0}$ and $\mu_{0}$ are the [[vacuum permittivity]] and [[vacuum permeability]] respectively.

The divergence of $\mathbf{E}$ is [[Gauss' law]], while that of $\mathbf{B}$ is unnamed. The curls are respectively [[Faraday's law]] and the [[Ampere's law|Ampere-Maxwell law]]. These laws, alongside the [[Lorentz force]], explain the entirety of electromagnetic phenomena. Maxwell's equations tell you how *charges* produce *fields*, whereas the Lorentz force tells you how *fields* affect *charges*. With both, the circle is complete and all electromagnetic phenomena can, at least in principle, be explained. This is true in both electro/magnetostatics and electrodynamics.
### In the vacuum
The laws above are correct in the vacuum. However, in the special case of a "true" vacuum, that is, there is truly nothing in that region of space, not even charges, they become
$$\begin{align}
\nabla\cdot\mathbf{E} & =0 &
\nabla\times\mathbf{E} & = -\frac{ \partial \mathbf{B} }{ \partial t } \\
\nabla\cdot\mathbf{B} & =0 &
\nabla\times\mathbf{B} &=\mu_{0}\varepsilon_{0}\frac{ \partial \mathbf{E} }{ \partial t } 
\end{align}$$
This is particularly interesting since it shows that, in a way, the electric and magnetic fields are one and the same. In fact, Faraday's law shows that the space derivative (curl, in this case) of an electric field is the time derivative of a magnetic field, and Ampere's law (the corrected form) shows that the space derivative of a magnetic field is the time derivative of an electric field. The only differences are the signs and the constants $\mu_{0}\varepsilon_{0}$ (which only appear in SI units).
#### Waves
This symmetry can be explored further by looking for the [[Laplacian]] of $\mathbf{E}$ and $\mathbf{B}$. Recall that $\nabla\times(\nabla\times \mathbf{A})=\nabla(\nabla\cdot \mathbf{A})-\nabla ^{2}\mathbf{A}$. Using the Maxwell equations, specifically by taking the curl of the curl on both $\mathbf{E}$ and $\mathbf{B}$ and dropping the null divergence, we can find that the fields satisfy
$$\boxed{\nabla ^{2}\mathbf{E}=\varepsilon_{0}\mu_{0}\frac{ \partial ^{2}\mathbf{E} }{ \partial t^{2} } ,\qquad \nabla ^{2}\mathbf{B}=\varepsilon_{0}\mu_{0}\frac{ \partial ^{2}\mathbf{B} }{ \partial t^{2} }}$$
These are very clearly symmetrical. In fact, they are *identical* in everything except the name of the vector. The greatest importance of these is that they are exactly [[Wave equation|wave equations]]; they must admit oscillatory solutions, that is, solutions dependent on sines and cosines (or complex exponentials, if you prefer). But oscillatory solutions in space represent *waves*, and so what these equations are telling us is that when electromagnetic fields vary in time, they always make waves: we call these **[[electromagnetic wave|electromagnetic waves]]** and they form the bulk of electrodynamic theory, optics and really any form of signal transfer you are used to from everyday life, like Wi-Fi, Bluetooth, radio, wireless charging and everything else.

One might question the velocity of these waves: as it happens, by comparing the above equations with wave equation, their speed in entirely determined by the permittivity and permeability by
$$c=\frac{1}{\sqrt{ \varepsilon_{0}\mu_{0} }}=299\ 792\ 458\text{ m/s}$$
This is the [[speed of light]], derived entirely from fundamental physical constants. This does certainly lead to a very legitimate question: *why?* What does light have to do with electricity and magnets? Well, at this point the connection is hard to deny: if $c$ is the speed of a wave, and that wave is derived exclusively from the laws of electromagnetism, then surely *light must be an electromagnetic wave*.
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
where the two left ones are integrated over any closed [[Surface|surface]] $\mathbf{S}$ and the two right ones are for any closed surface bounded by a closed [[Curve|line]] $\gamma$.
#### Waves in dielectrics
In the same way as the vacuum laws, we can find Laplacians for matter laws too. It is much easier in [[Dielectric|dielectrics]], where we can just set $\rho_{f}=0$ and $\mathbf{J}_{f}=0$ and redo the curl of the curl. However, these end up depending on the kind of material you are measuring the fields in. In linear, homogeneous and isotropic materials however, they look almost identical to the vacuum ones:
$$\boxed{\nabla ^{2}\mathbf{E}=\varepsilon\mu\frac{ \partial ^{2}\mathbf{E} }{ \partial t^{2} } ,\qquad \nabla ^{2}\mathbf{B}=\varepsilon\mu\frac{ \partial ^{2}\mathbf{B} }{ \partial t^{2} }}$$
The only difference is that we are using general [[permittivity]] and [[permability]] instead of the vacuum one. One interesting difference is that speed also changes accordingly:
$$v=\frac{1}{\sqrt{ \varepsilon \mu }}=\frac{1}{\sqrt{ \varepsilon_{0}\varepsilon_{r}\mu_{0}\mu_{r} }}=\underbrace{ \frac{1}{\sqrt{ \varepsilon_{0} \mu_{0} }} }_{ c } \underbrace{ \frac{1}{\sqrt{ \varepsilon_{r}\mu_{r} }} }_{ 1/n }=\frac{c}{n}$$
Clearly then, since both $\varepsilon_{r}\geq1$ and $\mu_{r}\geq1$, our quantity $n$, which we call the **[[refractive index]]**, must itself be $n\geq1$. As such, the speed of light is *always diminished* when in matter, by some quantity characteristic of the material itself. It must be, then, that the speed of light is the vacuum is the upper limit: even before the dawn of special relativity, the speed of light could not be surpassed with just electrodynamics[^2].
#### Waves in conductors
Outside of dielectrics, things get tricky. Free charges are near-infinite, so certainly cannot afford to state that they are approximately zero. We must therefore tackle Maxwell's equations head-on. We'll start by invoking [[Ohm's law]], which means reducing ourselves to linear, homogeneous and isotropic media:
$$\mathbf{J}_{f}=\sigma \mathbf{E}$$
With these the equations become
$$\begin{align}
\nabla\cdot\mathbf{E} & =\frac{\rho_{f}}{\varepsilon} &
\nabla\times\mathbf{E} & = -\frac{ \partial \mathbf{B} }{ \partial t } \\
\nabla\cdot\mathbf{B} & =0 &
\nabla\times\mathbf{B} &=\mu\sigma \mathbf{E} +\mu \sigma \frac{ \partial \mathbf{E} }{ \partial t } 
\end{align}$$
The [[Electric current|continuity equation]] for free current, $\nabla\cdot \mathbf{J}_{f}=-\partial \rho_{f}/\partial t$, combined with Ohm's law and then Gauss' law gives
$$\frac{ \partial \rho_{f} }{ \partial t } =-\nabla\cdot \mathbf{J}_{f}=-\nabla\cdot(\sigma \mathbf{E})=- \frac{\sigma}{\varepsilon}\rho_{f}$$
This is a rather simple first-order [[partial differential equation]] that solves to
$$\rho_{f}(t)=\rho_{f}(0)e^{-(\sigma/\varepsilon)t}$$
This explains the redistribution of charge over the surface of a conductor. $\varepsilon/\sigma\equiv \tau$ is the characteristic time of the conductor, which is a constant similar to the [[electrical conductivity]]. In perfect conductors ($\sigma\to \infty$) it is more or less zero, meaning the charge redistribution is instant[^3]. This isn't that important though: what is important is that free charges disappears *fast*, and when they do, we are back to $\rho_{f}=0$.
$$\begin{align}
\nabla\cdot\mathbf{E} & =0 &
\nabla\times\mathbf{E} & = -\frac{ \partial \mathbf{B} }{ \partial t } \\
\nabla\cdot\mathbf{B} & =0 &
\nabla\times\mathbf{B} &=\mu\sigma \mathbf{E} +\mu \sigma \frac{ \partial \mathbf{E} }{ \partial t } 
\end{align}$$
The difference here is that we have the additional nonzero "Ohm's law" term in the curl of $\mathbf{B}$. When working with dielectrics, $\sigma \simeq 0$, so it checks out with what we had before. Taking the curl of the curl now leads to
$$\boxed{\nabla ^{2}\mathbf{E}=\varepsilon \mu \frac{ \partial ^{2}\mathbf{E} }{ \partial t^{2} }+\mu \sigma \frac{ \partial \mathbf{E} }{ \partial t },\qquad\nabla ^{2}\mathbf{B}=\varepsilon \mu \frac{ \partial ^{2}\mathbf{B} }{ \partial t^{2} }+\mu \sigma \frac{ \partial \mathbf{B} }{ \partial t }}$$
The presence of a new, first-order term causes quite a number of differences compared to the dielectric case, chiefly the presence of very fast dampening in the [[amplitude]] of the wave. If the typical electromagnetic wave equation was analogous to the [[harmonic oscillator]], this is analogous to a *damped* harmonic oscillator: the conductor counteracts the wave and suppresses it.
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
These boundary conditions are particularly important, as they lay the foundation for the study of electromagnetic wave reflection and transmission.
### Potential form
Maxwell's equations can also be rewritten so that they are instead dependent on the [[electric potential]] $V$ and the [[magnetic vector potential]] $\mathbf{A}$. The benefit of this formulation is that it reduces a six-variable problem (three electric and three magnetic components) to a four-variable problem (one electric potential and three vector potential components). The issue here is that $V$ cannot exist in electrodynamics as we're used to from electrostatics, because Faraday's law calls for a nonzero electric curl and therefore $\mathbf{E}$ stops being [[Vector field|irrotational]]. What we can do is move things around until we get something that's still irrotational even when considering time. We do this by expressing the magnetic field in terms of the vector potential:
$$\nabla\times \mathbf{E}=-\frac{ \partial  }{ \partial t } (\nabla\times \mathbf{A})\quad\to \quad \nabla\times\left( \mathbf{E}+\frac{ \partial \mathbf{A} }{ \partial t } \right)=0$$
Now *this* is irrotational and we can thus will a potential into existence:
$$\mathbf{E}+\frac{ \partial \mathbf{A} }{ \partial t } =-\nabla V$$
or, isolating the field
$$\boxed{\mathbf{E}=-\nabla V-\frac{ \partial \mathbf{A} }{ \partial t } }\tag{1}$$
This is the time-dependent electric field in terms of potentials. Mix it with the fact that the magnetic field still has no divergence and is still $\mathbf{B}=\nabla\times \mathbf{A}$ and we have all our cards on the table to shed fields in favor of potentials. Next step: actually do that.

The equation $\nabla\cdot \mathbf{B}=0$ is trivially satisfied: we haven't changed anything on the magnetic field. Similarly, $\nabla\times \mathbf{E}=-\frac{ \partial \mathbf{A} }{ \partial t }$ is still true because that's how we got to $(1)$ in the first place. We need to check what becomes of $\nabla\cdot \mathbf{E}$ and $\nabla\times \mathbf{B}$, i.e. Gauss' law and Ampere-Maxwell's law. When we substitute $(1)$ in Gauss' law we get
$$\nabla ^{2}V+\frac{ \partial  }{ \partial t } (\nabla\cdot \mathbf{A})=- \frac{\rho}{\varepsilon_{0}}$$
Simple enough; take away time dependence and it goes back to the usual [[Poisson's equation]] for electric potential. Ampere-Maxwell's law is a little clunkier:
$$\nabla\times (\nabla\times \mathbf{A})=\mu_{0}\mathbf{J}-\mu_{0}\varepsilon_{0}\nabla\left( \frac{ \partial V }{ \partial t }  \right)-\mu_{0}\varepsilon_{0}\frac{ \partial ^{2}\mathbf{A} }{ \partial t^{2} } $$
Using the vector identity $\nabla\times(\nabla\times \mathbf{A})=\nabla(\nabla\cdot \mathbf{A})-\nabla ^{2}\mathbf{A}$ and with some rearrangements we get
$$\left( \nabla ^{2}\mathbf{A}-\mu_{0}\varepsilon_{0}\frac{ \partial ^{2}\mathbf{A} }{ \partial t^{2} }  \right)-\nabla\left( \nabla\cdot \mathbf{A}+\mu_{0}\varepsilon_{0}\frac{ \partial V }{ \partial t }  \right)=-\mu_{0}\mathbf{J}\tag{2}$$
On paper, this is the potential form of Maxwell's equation. It is also horribly confusing compared to the field form, so it begs the question of why you'd ever do this to yourself. The answer to that, beyond the proposition of reducing variables from six to four, is that potentials come packaged with a certain degree of freedom. Recall that a [[potential]] is defined up to a constant (the gradient of a constant always vanishes) and that a [[vector potential]] is defined up to the gradient of a [[scalar field]] (since the curl of a gradient always vanishes). This is the *soul* of these two equation, and it is important enough to warrant a name of its own: **[[gauge freedom]]**.

As a side note, if we define $L\equiv \nabla\cdot \mathbf{A}+\mu_{0}\varepsilon_{0}\ \partial V/\partial t$ and invoke the [[d'Alembertian]] operator, we can write Maxwell's equations in potential form as
$$\boxed{\square ^{2}V+\frac{ \partial L }{ \partial t } =- \frac{\rho}{\varepsilon_{0}},\qquad\square ^{2}\mathbf{A}-\nabla L=-\mu_{0}\mathbf{J}}$$
#### Gauge freedom
You may be wondering why gauge freedom matters. Instead of explaining it with words, let's just do the math directly. Call $\nabla \lambda=\boldsymbol{\alpha}$ the gradient of a scalar field we add onto $\mathbf{A}$. Call $\beta$ the constant we add onto $V$. Our new potentials are then $\mathbf{A}'=\mathbf{A}+\boldsymbol{\alpha}$ and $V'=V+\beta$. The two are not independent of each other: for $(1)$ to give the old field with the new potentials we must have
$$-\nabla V-\frac{ \partial \mathbf{A} }{ \partial t } =-\nabla V'-\frac{ \partial \mathbf{A}' }{ \partial t } $$
which gives
$$\nabla \beta+\frac{ \partial \boldsymbol{\alpha} }{ \partial t } =\nabla\left( \beta+\frac{ \partial \lambda }{ \partial t }  \right)=0$$
Call the term in parenthesis $k(t)$; its gradient is zero so it must be not vary with position (though it might vary in time). Our $\beta$ then is
$$\beta=-\frac{ \partial \lambda }{ \partial t } +k(t)$$
However, since $\beta$ is a constant, we may as well redefine $\lambda$ so that it also contains $\int_{0}^{t}k(t')dt'$. The gradient of $\lambda$ won't change (which, remember, is $\boldsymbol{\alpha}$) and it makes our life easier. Our $\beta$ then is
$$\beta=-\frac{ \partial \lambda }{ \partial t } \quad(\text{new }\lambda)$$
But wait, now both $\boldsymbol{\alpha}$ and $\beta$ are uniquely determined by this one scalar field $\lambda$:
$$\mathbf{A}'=\mathbf{A}+\nabla \lambda,\quad V'=V-\frac{ \partial \lambda  }{ \partial t } $$
Evidently, given *any* scalar function $\lambda(\mathbf{r},t)$ and adding it onto the potentials as above, Maxwell's equation *do not change*. Choosing a $\lambda$, or moving from one to another, is called a **gauge transformation** and the function itself is called a **gauge**. Our duty, then, is to figure how to exploit this freedom to make the potential equations as nice as possible.

Actually, we've already seen a gauge, even though not explicitly: in magnetostatics it's generally convenient to set $\nabla\cdot \mathbf{A}=0$ by just invent a $\lambda$ for which for which this is true. This is known as the [[Coulomb gauge]] and it is typical in static scenarios as it makes sets the electric potential into Poisson's equation. In electrodynamics, however, what gauge to pick is not always clear and historically many choices have been explored and studied. Ultimately, the best choice depends on the system at hand. That said, we do have a "default choice", which we call the [[Lorenz gauge]], which states
$$\nabla\cdot \mathbf{A}=-\mu_{0}\varepsilon_{0}\frac{ \partial V }{ \partial t } $$
and is designed to make the middle term of $(2)$ vanish. This yields
$$\nabla ^{2}V-\mu_{0}\varepsilon_{0}\frac{ \partial ^{2}V }{ \partial t^{2} } =- \frac{\rho}{\varepsilon_{0}},\qquad\nabla ^{2}\mathbf{A}-\mu_{0}\varepsilon_{0}\frac{ \partial ^{2}\mathbf{A} }{ \partial t^{2} } =-\mu_{0}\mathbf{J}$$
or, using the d'Alembertian:
$$\boxed{\square ^{2}V=- \frac{\rho}{\varepsilon_{0}},\quad\square ^{2}\mathbf{A}=-\mu_{0}\mathbf{J}}\tag{3}$$
The Lorenz gauge turns the potentials themselves into waves, although their wave equations are *inhomogeneous*.
### Relativistic form
Maxwell's equations can be written in a complete, unified form using what we know about the theory of relativity. To start, consider some arbitrarily shaped electric charge $\rho$ For the sake of generality, we focus only on an infinitesimal volume $V$ containing total charge $Q$, so that the density is $Q/V$ and is moving at some velocity $\mathbf{v}$. For the sake of simplicity we assume that $\rho$ only contains charges of the same sign (if it contained both, the argument is the same but we'd have to have both a positive and negative term). The current density is $\mathbf{J}=\rho \mathbf{v}$.

The volume of $\rho$ depends on the observer due to [[distance contraction]]. We'll call $\rho_{0}$ the **proper charge density**, which is the density in the rest frame of the charge:
$$\rho_{0}=\frac{Q}{V_{0}}$$
where $V_{0}$ is the volume in the rest system (charge in [[Relativistic invariant|relativistically invariant]] so it never changes). But we can go further: only one dimension is contracted (the one the charge is moving on, i.e. the direction of $\mathbf{v}$), so we can readily write the transformation rule:
$$V=\frac{V_{0}}{\gamma}=\sqrt{ 1-v^{2}/c^{2} }\ V_{0}$$
and thus
$$\rho=\gamma \rho_{0}=\frac{\rho_{0}}{\sqrt{ 1-u^{2}/c^{2} }},\quad \mathbf{J}=\gamma \rho_{0}\mathbf{v}=\rho_{0} \frac{\mathbf{v}}{\sqrt{ 1-v^{2}/c^{2} }}$$
But $\gamma \mathbf{v}$ is just the spatial part of the [[proper velocity]]! So we can extend $\mathbf{J}=\rho \mathbf{v}$ to a [[four-vector]] by saying
$$J^{\mu}=\rho_{0}\eta^{\mu}=(c\rho,J_{x},J_{y},J_{z})$$
This is known as the **[[four-current]]**. The **relativistic Maxwell's equations** then are
$$\boxed{\frac{ \partial F^{\mu \nu} }{ \partial x^{\nu} } =\mu_{0}J^{\mu},\qquad \frac{ \partial G^{\mu \nu} }{ \partial x^{\nu} } =0}$$
in both [[field tensor]] and [[Field tensor|dual tensor]] formalisms (summation over $\nu$ implied). Each of these equations have *four* components. This is because the values of $\mu=0,1,2,3$ each lead to one component. Combined, these two provide the same information as the classical Maxwell's equations.

> [!quote]- Deriving the old equations
> To prove that these are actually correct, we will derive the classical Maxwell's equations from just these two. Start from $\mu=0$:
> $$\begin{align}
> \frac{ \partial F^{0\nu} }{ \partial x^{\nu} } &=\frac{ \partial F^{00} }{ \partial x^{0} } +\frac{ \partial F^{01} }{ \partial x^{1} } +\frac{ \partial F^{02} }{ \partial x^{2} } +\frac{ \partial F^{03} }{ \partial x^{3} } \\
> &=\frac{1}{c}\frac{ \partial E_{x} }{ \partial t } +\frac{ \partial E_{y} }{ \partial y } -\frac{ \partial E_{z} }{ \partial z }  \\
> &=\frac{1}{c}\left( \nabla\cdot \mathbf{E} \right) \\
> &=\mu_{0}J^{0} \\
> &=\mu_{0}c\rho
> \end{align}$$
> By using $c^{2}=1/\varepsilon_{0}\mu_{0}$ we find
> $$\nabla\cdot \mathbf{E}=\frac{\rho}{\varepsilon_{0}}$$
> This is [[Gauss' law]]. Now take $\mu=1$ for example. In that case, we get
> $$\begin{align}
> \frac{ \partial F^{1\nu} }{ \partial x^{\nu} } &=\frac{ \partial F^{10} }{ \partial x^{0} } +\frac{ \partial F^{11} }{ \partial x^{1} } +\frac{ \partial F^{12} }{ \partial x^{2} } +\frac{ \partial F^{13} }{ \partial x^{3} } \\
> &=- \frac{1}{c^{2}}\frac{ \partial E_{x} }{ \partial t } +\frac{ \partial B_{z} }{ \partial y } -\frac{ \partial B_{y} }{ \partial z }  \\
> &=\left( - \frac{1}{c^{2}}\frac{ \partial \mathbf{E} }{ \partial t } +\nabla\times \mathbf{B} \right)_{x} \\
> &=\mu_{0}J^{1} \\
> &=\mu_{0}J_{x}
> \end{align}$$
> Similar results come up for $\mu=2$ and $\mu=3$, just for $J_{y}$ and $J_{z}$, which we can combine in vector notation to read
> $$\nabla\times \mathbf{B}=\mu_{0}\mathbf{J}+\mu_{0}\varepsilon_{0}\frac{ \partial \mathbf{E} }{ \partial t }$$
> This is the [[Ampere's law|Ampere-Maxwell law]].
> 
> We've exhausted the field tensor. Now let's use the dual tensor. Similarly, $\mu=0$ on $G^{\mu \nu}$ gives
> $$\begin{align}
> \frac{ \partial G^{0\nu} }{ \partial x^{\nu} } &=\frac{ \partial G^{00} }{ \partial x^{0} } +\frac{ \partial G^{01} }{ \partial x^{1} } +\frac{ \partial G^{02} }{ \partial x^{2} } +\frac{ \partial G^{03} }{ \partial x^{3} } \\
> &=\frac{ \partial B_{x} }{ \partial x } +\frac{ \partial B_{y} }{ \partial y } +\frac{ \partial B_{z} }{ \partial z }   \\
> &=\nabla\cdot \mathbf{B}=0
> \end{align}$$
> This is the unnamed Maxwell equation. Finally, for $\mu=1$:
> $$\begin{align}
> \frac{ \partial G^{1\nu} }{ \partial x^{\nu} } &=\frac{ \partial G^{10} }{ \partial x^{0} } +\frac{ \partial G^{11} }{ \partial x^{1} } +\frac{ \partial G^{12} }{ \partial x^{2} } +\frac{ \partial G^{13} }{ \partial x^{3} } \\
> &=- \frac{1}{c}\frac{ \partial B_{x} }{ \partial t } - \frac{1}{c}\frac{ \partial E_{z} }{ \partial y } + \frac{1}{c}\frac{ \partial E_{y} }{ \partial z }  \\
> &=- \frac{1}{c}\left( \frac{ \partial \mathbf{B} }{ \partial t } +\nabla\times \mathbf{E} \right)_{x} \\
> &=0
> \end{align}$$
> Combine it with the results for $\mu=2$ and $\mu=3$ to get
> $$\nabla\times \mathbf{E}=-\frac{ \partial \mathbf{B} }{ \partial t }$$
> which is [[Faraday's law]].

But why stop here? We already know that Maxwell's equations can be express in potential form, so let's look for the *relativistic* potential form. When combined, the electric and magnetic vector potentials make up a [[four-vector]]:
$$A^{\mu}=\left( \frac{V}{c},A_{x},A_{y},A_{z} \right)$$
We call it (very creatively) the **[[four-vector potential]]**. In its terms, the field tensor can be rewritten as
$$\boxed{F^{\mu \nu}=\frac{ \partial A^{\nu} }{ \partial x_{\mu} } -\frac{ \partial A^{\mu} }{ \partial x_{\nu} }}$$
where we are taking derivatives using covariant four-vectors (important! You'd get a wrong sign if used contravariant ones).

> [!quote]- Finding the fields
> This definition of the field tensor leads to the same field-from-potentials equations
> $$\mathbf{E}=-\nabla V- \frac{ \partial \mathbf{A} }{ \partial t } ,\qquad \mathbf{B}=\nabla\times \mathbf{A}$$
> For $\mu=0$ and $\nu=1$ we get
> $$F^{01}=\frac{ \partial A^{1} }{ \partial x_{0} }- \frac{ \partial A^{0} }{ \partial x_{1} } =-\frac{ \partial A_{x} }{ \partial (ct) } - \frac{1}{c}\frac{ \partial V }{ \partial x } =- \frac{1}{c}\left( \frac{ \partial \mathbf{A} }{ \partial t } +\nabla V \right)_{x}=\frac{E_{x}}{c} $$
> and match $E_{x}$ with the parenthesis. Do the same for $\nu=2,3$ and you get the electric field. Similarly, for $\mu=1$ and $\nu=2$ we get
> $$F^{12}=\frac{ \partial A^{2} }{ \partial x_{1} } -\frac{ \partial A^{1} }{ \partial x_{2} }=\frac{ \partial A_{y} }{ \partial x } -\frac{ \partial A_{x} }{ \partial y } =(\nabla\times \mathbf{A})_{z}=B_{z} $$
> Do the same for $F^{23}$ and $F^{31}$ and you get the magnetic field.

If you put this field tensor in its Maxwell equation, you get
$$\frac{ \partial  }{ \partial x_{\mu} } \left( \frac{ \partial A^{\nu} }{ \partial x^{\nu} }  \right)-\frac{ \partial  }{ \partial x_{\nu} } \left( \frac{ \partial A^{\mu} }{ \partial x^{\nu} }  \right)=\mu_{0}J^{\mu}$$
which is not really solvable. But notice how if you add the gradient of a scalar function $\lambda$ to $A^{\mu}$, nothing changes in $F^{\mu \nu}$. This is gauge invariance, so we can invoke the [[Lorenz gauge]] again to state, in relativistic form:
$$\nabla\cdot \mathbf{A}=- \frac{1}{c^{2}}\frac{ \partial V }{ \partial t } \quad\Rightarrow \quad \frac{ \partial A^{\mu} }{ \partial x^{\mu} } =0$$
and with this definition, the previous equation simplifies to
$$\boxed{\square ^{2}A^{\mu}=-\mu_{0}J^{\mu}}$$
using the relativistic [[d'Alembertian]]. This equation contains the entirety of the electromagnetic field, all of it packaged in a single inhomogeneous wave equation in spacetime as the combined form of $(3)$.

[^1]: For correctness' sake, the charges themselves only *align* with the polarization, but don't move much. If they did all actually move to the surface, we'd be working with [[conductor|conductors]] and not with polarized [[dielectric|dielectrics]]. Still, this alignment motion is sufficient to produce a small current.

[^2]: Of course, [[Galilean relativity]] would still debate that the speed of light cannot be a universal speed limit since it can always be summed with the speed of the [[frame of reference]] (at least in an inertial frame), thus always being able to achieve a faster speed by just changing perspective. Of course we now know this is wrong, but this problem is about *mechanics*; *electromagnetism*, on the other hand, was always right.

[^3]: In practice, it actually isn't, not just because that would be physically impossible but because Ohm's law is a rather high-level approximation and starts to break down around the mean time between [[electron]] collisions, which is $\tau_{C} \simeq 10^{-14}$. Coincidentally, this is also the order of magnitude of time it takes for charges to redistribute. The *actual* theory of conduction is a lot more complicated; see for instance [[Ideal crystal#Electronic structure]] for a quantum-mechanical approach for crystalline solids.
