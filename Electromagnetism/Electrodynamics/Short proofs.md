---
wiki-publish: false
---
**Poynting's theorem**
1. Start from work done by Lorentz force: $dW=q(\mathbf{E}+\mathbf{v}\times \mathbf{B})\cdot d\mathbf{s}=q\mathbf{E}\cdot d\mathbf{s}$.
2. Change to charge distribution $dq=\rho d\tau$ and sub into work (recall $\rho \mathbf{v}=\mathbf{J}$).
3. Move $dt$ to get power.
4. Express $\mathbf{E}\cdot \mathbf{J}$ by inverting Ampere-Maxwell's law for $\mathbf{J}$.
5. Vector calculus magic on $\mathbf{E}\cdot (\nabla\times \mathbf{B})$ and use Poynting vector.
6. Plug into integral, use divergence theorem. Result:

$$P=\frac{ \partial U }{ \partial t } =-\frac{ \partial  }{ \partial t } \int_{\mathcal{V}}u(\mathbf{r})\ d\tau-\oint_{\mathcal{S}}\mathbf{S}\cdot d\mathbf{a}$$

**Conservation of momentum**
1. Newton's third law kinda broken (diagram of two charges, magnetic forces don't balance).
2. Solution: give the fields momentum.
3. Newton's second law says $\mathbf{F}=d\mathbf{p}_\text{mech}/dt$.
4. Tensor form of Lorentz law says $d\mathbf{p}_\text{mech}/dt=-\varepsilon_{0}\mu_{0}\int_{\mathcal{V}}\mathbf{S}d\tau+\oint_{\mathcal{S}}T\cdot d\mathbf{a}$.
5. Looks a lot like Poynting's theorem: $\mathbf{S}$ integral is momentum stored in the fields, tensor integral is momentum exiting and entering.
6. Divide $\mathbf{S}$ integral by density to get $\mathbf{g}=\varepsilon_{0}\mu_{0}\mathbf{S}=\varepsilon_{0}(\mathbf{E}\times \mathbf{B})$.
7. Angular momentum is usual: $\boldsymbol{\ell}=\mathbf{r}\times \mathbf{g}=\varepsilon_{0}[\mathbf{r}\times(\mathbf{E}\times \mathbf{B})]$.

**Vacuum Maxwell equations**
1. Vacuum: no charges, $\rho=J=0$. Start from
   $$\begin{align} \nabla\cdot\mathbf{E} & =0 & \nabla\times\mathbf{E} & = -\frac{ \partial \mathbf{B} }{ \partial t } \\ \nabla\cdot\mathbf{B} & =0 & \nabla\times\mathbf{B} &=\mu_{0}\varepsilon_{0}\frac{ \partial \mathbf{E} }{ \partial t } \end{align}$$
2. Use $\nabla\times(\nabla\times \mathbf{A})=\nabla(\nabla\cdot \mathbf{A})-\nabla ^{2}\mathbf{A}$, extract Laplacian, divergence is zero, apply curl laws.

**Dielectric Maxwell equations**
1. Dielectric: no free charges, $\rho_{f}=J_{f}=0$. Start from
   $$\begin{align} \nabla\cdot\mathbf{D}&=0 & \nabla\times\mathbf{E}&=-\frac{ \partial \mathbf{B} }{ \partial t }  \\ \nabla\cdot\mathbf{B} & =0 & \nabla\times\mathbf{\mathbf{H}} & =\frac{ \partial \mathbf{D} }{ \partial t } \end{align}$$
2. Use $\nabla\times(\nabla\times \mathbf{A})=\nabla(\nabla\cdot \mathbf{A})-\nabla ^{2}\mathbf{A}$ like vacuum, do the curls. Same as vacuum, but $\mu \varepsilon$ instead of $\mu_{0}\varepsilon_{0}$.

**Conductor Maxwell equations**
1. Use Ohm's law $\mathbf{J}_{f}=\sigma \mathbf{E}$.
2. Maxwell equations become
   $$\begin{align} \nabla\cdot\mathbf{E} & =\frac{\rho_{f}}{\varepsilon} & \nabla\times\mathbf{E} & = -\frac{ \partial \mathbf{B} }{ \partial t } \\ \nabla\cdot\mathbf{B} & =0 & \nabla\times\mathbf{B} &=\mu\sigma \mathbf{E} +\mu \sigma \frac{ \partial \mathbf{E} }{ \partial t } \end{align}$$
3. Continuity equation is $\nabla\cdot \mathbf{J}_{f}=-\partial \rho_{f}/\partial t$. Use Gauss' law on charge, Ohm's law on current, get exponentially decreasing charge $\rho_{f}(t)=\rho_{f}(0)e^{-(\sigma/\varepsilon)t}$.
4. Basically zero, so $\rho_{f}=0$ and
   $$\begin{align} \nabla\cdot\mathbf{E} & =0 & \nabla\times\mathbf{E} & = -\frac{ \partial \mathbf{B} }{ \partial t } \\ \nabla\cdot\mathbf{B} & =0 & \nabla\times\mathbf{B} &=\mu\sigma \mathbf{E} +\mu \sigma \frac{ \partial \mathbf{E} }{ \partial t } \end{align}$$
5. Use $\nabla\times(\nabla\times \mathbf{A})=\nabla(\nabla\cdot \mathbf{A})-\nabla ^{2}\mathbf{A}$ like vacuum, do the curls. They have an additional term that causes dampening in skin-depth lengths.

**Potential Maxwell equations**
1. Faraday's law means electric potential no longer hold. However, express $\mathbf{B}$ as $\nabla\times \mathbf{A}$ and flip Faraday's law to find electrodynamic electric field.
2. $\nabla\cdot \mathbf{B}=0$ is still valid. Check $\nabla\cdot \mathbf{E}$ and $\nabla\times \mathbf{B}$. Put potential form of $\mathbf{E}$ and $\mathbf{B}$ in both and run the math using $\nabla\times(\nabla\times \mathbf{A})=\nabla(\nabla\cdot \mathbf{A})-\nabla ^{2}\mathbf{A}$.
3. Result is ugly. Gauge freedom can be used to nuke one term in $\nabla\times \mathbf{B}$ by setting $\nabla\cdot \mathbf{A}$. Write the rest with d'Alembertian $\square ^{2}\equiv \nabla ^{2}-(1/c^{2})\partial^{2}/\partial t^{2}$.

**Gauge freedom**
1. You can add a constant to scalar potential and a gradient of a scalar field to vector potential, like $\mathbf{A}'=\mathbf{A}+\boldsymbol{\alpha}$ and $V'=V+\beta$, where $\boldsymbol{\alpha}=\nabla \lambda$.
2. These are true only if the fields are the same, so $-\nabla V-\frac{ \partial \mathbf{A} }{ \partial t }=-\nabla V'-\frac{ \partial \mathbf{A}' }{ \partial t }$.
3. Substitute $\mathbf{A}'$, $V'$ and $\alpha$ and get $\nabla (\beta+\frac{ \partial \lambda  }{ \partial t })=0$. Gradient is zero so stuff in parenthesis is not space dependent.
4. Call parenthesis $k(t)$, so $\beta=-\frac{ \partial \lambda }{ \partial t }+k(t)$. But $\lambda$ is anything, so just change it so that it includes (the integral of) $k(t)$. So $\beta=-\frac{ \partial \lambda }{ \partial t }$.
5. Now both $\mathbf{A}'$ and $V'$ are determined by a single $\lambda$. Since $\lambda$ can be anything, you have (gauge) freedom to set one value of the potentials.

**Vacuum waves**
1. Solution to Maxwell vacuum wave equations is $\tilde{\mathbf{E}}=\tilde{\mathbf{E}}_{0}e^{i(kx-\omega t)}$ (same for $\mathbf{B}$). Must be such that they obey Maxwell's equations.
2. Divergence is zero on both fields, so they can't propagate: fields are perpendicular to axis of motion $x$, so $\tilde{E}_{0,x}=\tilde{B}_{0,x}=0$. EM waves are transverse.
3. Both curls give the same result. From $\nabla\times \mathbf{E}$, recall that $\mathbf{E}\equiv \mathbf{E}(x,t)$ (only depends on the axis of motion) and $E_{0,x}=0$, so curl reduces to $-\frac{ \partial \tilde{E}_{z} }{ \partial x }\hat{\mathbf{y}}+\frac{ \partial \tilde{E}_{y} }{ \partial x }\hat{\mathbf{z}}$. Do the math. Faraday's law also gives $-\frac{ \partial \tilde{\mathbf{B}} }{ \partial t }$. Do this math too, compare the two, get $\tilde{\mathbf{B}}_{0}=\frac{k}{\omega}(\hat{\mathbf{x}}\times \mathbf{E})$. Electric and magnetic fields are perpendicular.
4. Since $k/\omega=1/c$, also have $B_{0}=E_{0}/c$. Plug this in wave solutions, take real part (remember phase in cosine), extend to arbitrary wavevector and polarization.

**Transported quantities (vacuum)**
1. Energy density is $u=1/2(\varepsilon_{0}E^{2}+(1/\mu_{0})B^{2})$. But $B_{0}=E_{0}/c$, so $u=\varepsilon_{0} E^{2}$.
2. Poynting vector is $\mathbf{S}=(1/\mu_{0})(\mathbf{E}\times \mathbf{B})$, so $\mathbf{S}=c\varepsilon_{0}E^{2}\hat{\mathbf{n}}=cu\, \hat{\mathbf{n}}$.
3. Momentum density is $\mathbf{g}=\varepsilon_{0}(\mathbf{E}\times \mathbf{B})$, so $\mathbf{g}=(u/c)\hat{\mathbf{n}}$.
4. Averages are half of these because $\sin ^{2}$ over full period is $1/2$.
5. Radiation pressure (on perfect absorber) is due to momentum transfer $\Delta \mathbf{p}=\langle \mathbf{g} \rangle Ac\Delta t$ over an area $A$: $P=(1/A)(\Delta p/\Delta t)=\varepsilon_{0}E_{0}^{2}/2=I/c$.

**Dielectric waves**
1. Same as vacuum, but with $\mu \varepsilon$ instead of $\mu_{0}\varepsilon_{0}$. Speed becomes $v=c/n$ since $n=\sqrt{ \varepsilon_{r}\mu_{r} }\simeq \sqrt{ \varepsilon_{r} }$. Transported quantities change accordingly. Most important is irradiance $I=(\varepsilon c/2n)E_{0}^{2}$.

**Dielectric reflection and transmission**
1. Assume surface is at $x=0$, propagation on $x$ and polarization on $y$.
2. Reflection flips $k_{1}$ to $-k_{1}$. Transmission changes $k_{1}$ to $k_{2}$. You get
   $$\begin{align}\tilde{\mathbf{E}}_{I}(x,t)=\tilde{E}_{0,I}e^{i(k_{1}x-\omega t)}\hat{\mathbf{y}},&\quad \tilde{\mathbf{B}}_{I}(x,t)=\frac{n_{1}}{c}\tilde{E}_{0,I}e^{i(k_{1}x-\omega t)}\hat{\mathbf{z}} \\ \tilde{\mathbf{E}}_{R}(x,t)=\tilde{E}_{0,R}e^{i(-k_{1}x-\omega t)}\hat{\mathbf{y}},&\quad \tilde{\mathbf{B}}_{R}(x,t)=-\frac{n_{1}}{c}\tilde{E}_{0,R}e^{i(-k_{1}x-\omega t)}\hat{\mathbf{z}} \\ \tilde{\mathbf{E}}_{T}(x,t)=\tilde{E}_{0,T}e^{i(k_{2}x-\omega t)}\hat{\mathbf{y}},&\quad \tilde{\mathbf{B}}_{T}(x,t)=\frac{n_{2}}{c}\tilde{E}_{0,T}e^{i(k_{2}x-\omega t)}\hat{\mathbf{z}}\end{align}$$
3. Boundary conditions are
   $$\begin{align} \varepsilon_{1}E_{1}^{\perp}-\varepsilon_{2}E_{2}^{\perp} & =\sigma_{f} & \mathbf{E}_{1}^{\parallel}-\mathbf{E}_{2}^{\parallel} & =\mathbf{0} \\ B_{1}^{\perp}-B_{2}^{\perp} & =0 & \frac{1}{\mu_{1}}\mathbf{B}_{1}^{\parallel}- \frac{1}{\mu_{2}}\mathbf{B}_{2}^{\parallel}&=\mathbf{0} \end{align}$$

**- Normal incidence**
1. $\theta_{I}=0°$: no perpendicular fields. Parallel electric field is $\tilde{E}_{0,I}+\tilde{E}_{0,R}=\tilde{E}_{0,T}$. Parallel magnetic field is
   $$\frac{1}{\mu_{1}}\left( \frac{n_{1}}{c}\tilde{E}_{0,I}- \frac{n_{1}}{c}\tilde{E}_{0,R} \right)=\frac{1}{\mu_{2}} \frac{n_{2}}{c}\tilde{E}_{0,T}$$
2. Call $\beta=\mu_{1}n_{2}/\mu_{2}n_{1}$. Then you get $\tilde{E}_{0,I}-\tilde{E}_{0,R}=\beta \tilde{E}_{0,T}$. Solve for $\tilde{E}_{0,R}$ and $\tilde{E}_{0,T}$:
   $$\tilde{E}_{0,R}=\left( \frac{1-\beta}{1+\beta} \right)\tilde{E}_{0,I},\qquad \tilde{E}_{0,T}=\left( \frac{2}{1+\beta} \right)\tilde{E}_{0,T}$$
3. If materials are nonmagnetic ($\mu_{1}\simeq \mu_{2}\simeq \mu_{0}$), $\beta=n_{2}/n_{1}$, so
   $$\tilde{E}_{0,R}=\left( \frac{n_{1}-n_{2}}{n_{1}+n_{2}} \right)\tilde{E}_{0,I},\qquad \tilde{E}_{0,T}=\left( \frac{2n_{1}}{n_{1}+n_{2}} \right)\tilde{E}_{0,T}$$
4. Reflectance and transmittance are ratios of incoming and reflected/transmitted irradiance. $R+T=1$ by just doing the math.

**- Oblique incidence (laws of optics)**
1. $\theta_{I}\neq 0°$: all boundary conditions apply. Waves are
   $$\begin{align} \tilde{\mathbf{E}}_{I}(\mathbf{r},t)=\tilde{\mathbf{E}}_{0,I}e^{i(\mathbf{k}_{I}\cdot \mathbf{r}-\omega t)},\qquad \tilde{\mathbf{B}}_{I}(\mathbf{r},t)=\frac{n_{1}}{c}(\hat{\mathbf{k}}_{I}\times \tilde{\mathbf{E}}_{I}) \\ \tilde{\mathbf{E}}_{R}(\mathbf{r},t)=\tilde{\mathbf{E}}_{0,R}e^{i(\mathbf{k}_{R}\cdot \mathbf{r}-\omega t)},\qquad \tilde{\mathbf{B}}_{R}(\mathbf{r},t)=\frac{n_{1}}{c}(\hat{\mathbf{k}}_{R}\times \tilde{\mathbf{E}}_{R}) \\ \tilde{\mathbf{E}}_{T}(\mathbf{r},t)=\tilde{\mathbf{E}}_{0,T}e^{i(\mathbf{k}_{T}\cdot \mathbf{r}-\omega t)},\qquad \tilde{\mathbf{B}}_{T}(\mathbf{r},t)=\frac{n_{2}}{c}(\hat{\mathbf{k}}_{T}\times \tilde{\mathbf{E}}_{T}) \end{align}$$
2. Wavevectors must obey
   $$\frac{k_{I}}{n_{1}}=\frac{k_{R}}{n_{1}}=\frac{k_{T}}{n_{2}}=\omega \quad\Rightarrow \quad k_{I}=k_{R}=\frac{n_{1}}{n_{2}}k_{T}$$
3. For the boundary conditions to hold, we need this on the surface:
   $$\tilde{E}_{0,I}e^{i(\mathbf{k}_{I}\cdot \mathbf{r}-\omega t)}+\tilde{E}_{0,R}e^{i(\mathbf{k}_{R}\cdot \mathbf{r}-\omega t)}=\tilde{E}_{0,T}e^{i(\mathbf{k}_{T}\cdot \mathbf{r}-\omega t)}$$
4. This implies $\mathbf{k}_{I}\cdot \mathbf{r}=\mathbf{k}_{R}\cdot \mathbf{r}=\mathbf{k}_{T}\cdot \mathbf{r}$. Write the components explicitly: $yk_{I,y}+zk_{I,z}=yk_{R,y}+zk_{R,z}=yk_{T,y}+zk_{T,z}$. True only when the components are individually equal (set $y=0$ and $z=0$ to show that).
5. Reorient axes so that $k_{I,z}=0=k_{R,z}=k_{T,z}$. But then $\mathbf{k}_{I},\mathbf{k}_{R},\mathbf{k}_{T}$ must all be coplanar.
6. Using angles on this plane, $k_{I}\sin \theta_{I}=k_{R}\sin \theta_{R}=k_{T}\sin \theta_{T}$. But since $k_{I}=k_{R}$, then $\theta_{I}=\theta_{R}$. Also, since $k_{I}=\frac{n_{1}}{n_{2}}k_{T}$ we get $\sin \theta_{T}/\sin \theta_{I}=n_{1}/n_{2}$.
7. Boundary conditions become
   $$\begin{align} \varepsilon_{1}(\tilde{\mathbf{E}}_{0,I}+\tilde{\mathbf{E}}_{0,R})_{x}& =\varepsilon_{2}(\tilde{\mathbf{E}}_{0,T})_{x} & (\tilde{\mathbf{E}}_{0,I}+\tilde{\mathbf{E}}_{0,R})_{y,z} & =(\tilde{\mathbf{E}}_{0,T})_{y,z} \\ (\tilde{\mathbf{B}}_{0,I}+\tilde{\mathbf{B}}_{0,R})_{x} & =(\tilde{\mathbf{B}}_{0,T})_{x} & \frac{1}{\mu_{1}}(\tilde{\mathbf{B}}_{0,I}+\tilde{\mathbf{B}}_{0,R})_{y,z}&=\frac{1}{\mu_{2}}(\tilde{\mathbf{B}}_{0,T})_{y,z} \end{align}$$
8. If the incident wave is polarized in the plane of incidence, so are the reflected and transmitted waves:
   $$\begin{align} \varepsilon_{1}(-\tilde{E}_{0,I}\sin \theta_{I}+\tilde{E}_{0,R}\sin \theta_{R}) & =\varepsilon_{2}(-\tilde{E}_{0,T}\sin \theta_{T}) & \tilde{E}_{0,I}\cos \theta_{I}+\tilde{E}_{0,R}\cos \theta_{R} & =\tilde{E}_{0,T}\cos \theta_{T} \\ 0 & =0 & \frac{n_{1}}{\mu_{1}}(\tilde{E}_{0,I}+\tilde{E}_{0,R})&=\frac{n_{2}}{\mu_{2}}\tilde{E}_{0,T} \end{align}$$
9. Use law of reflection and Snell on top left, bottom right, get $\tilde{E}_{0,I}-\tilde{E}_{0,R}=\beta \tilde{E}_{0,T}$, whereas at top right becomes $\tilde{E}_{0,I}+\tilde{E}_{0,R}=\alpha \tilde{E}_{0,T}$. Here $\alpha=\cos \theta_{T}/\cos \theta_{I}$ and $\beta=\mu_{1}n_{2}/\mu_{2}n_{1}$. Solve for $\tilde{E}_{0,R}$ and $\tilde{E}_{0,T}$ to get Fresnel's equations
   $$\tilde{E}_{0,R}=\left( \frac{\alpha-\beta}{\alpha+\beta} \right)\tilde{E}_{0,I},\qquad \tilde{E}_{0,T}=\left( \frac{2}{\alpha+\beta} \right)\tilde{E}_{0,I}$$

**- Brewster's angle**
1. When $\alpha=\beta$ in the Fresnel equations, the reflected field disappears. The transmitted amplitude is the same as the incident one. This is true when
   $$\sin ^{2}\theta_{B}=\frac{1-\beta ^{2}}{\left( n_{1}/n_{2}\right)^{2}-\beta ^{2}}\quad\Rightarrow \quad \theta_{B}\simeq \arctan\left( \frac{n_{2}}{n_{1}} \right)\quad\text{if }\mu_{1}\simeq \mu _{2}$$

**Conductor waves**
1. Maxwell's equation have an extra first-order term. This causes dampening. The wave functions are still valid but with a complex wavenumber $\tilde{k}=k+i\kappa$:
   $$\mathbf{E}(x,t)=\mathbf{E}_{0}e^{i[\tilde{k}x-\omega t]}=\mathbf{E}_{0}e^{i(kx-\omega t)}e^{-\kappa x}$$
2. The additional term is exponential dampening. The amplitude is reduced by $1/e$ in a skin depth $d=1/\kappa$.

**Dispersion in dielectrics**
1. $\varepsilon$ is frequency dependent. Assume electrons are bound to molecules by approximately an oscillating force $F_\text{binding}=-kx=-m\omega_{0}^{2}y$ where $\omega_{0}$ is the natural oscillation frequency. Some energy is dissipated by a nonconservative force $F_\text{damping}=\frac{-m\gamma dy}{dt}$ and some is added by an external force $F_\text{driving}=qE=qE_{0}\cos(\omega t)$.
2. Combine forces and Newton's second law to get
   $$m \frac{d^{2}y}{dt^{2}}+m\gamma \frac{dy}{dt}+m\omega_{0}^{2}y=qE_{0}\cos (\omega t)$$
3. Regard it as the real part of
   $$\frac{d^{2}\tilde{y}}{dt^{2}}+\gamma \frac{d\tilde{y}}{dt}+\omega_{0}^{2}\tilde{y}=\frac{q}{m}E_{0}e^{-i\omega t}$$
4. The steady state is $\tilde{x}(t)=\tilde{x}_{0}e^{-i\omega t}$. Put this in the ODE to get
   $$\tilde{x}_{0}=\frac{q}{m}\frac{1}{\omega_{0}^{2}-\omega ^{2}-i\gamma \omega}E_{0}$$
5. This is an oscillating dipole
   $$\tilde{p}(t)=q\tilde{x}(t)=\frac{q^{2}}{m}\frac{1}{\omega_{0}^{2}-\omega ^{2}-i\gamma \omega}E_{0}e^{-i\omega t}$$

**Retarded potentials**
1. Static potentials are
   $$V(\mathbf{r})=\frac{1}{4\pi \varepsilon_{0}}\int_{\mathcal{V}} \frac{\rho(\mathbf{r}')}{\mathfrak{r}} \ d\tau',\qquad \mathbf{A}(\mathbf{r})=\frac{\mu_{0}}{4\pi}\int_{\mathcal{V}} \frac{\mathbf{J}(\mathbf{r}')}{\mathfrak{r}} \ d\tau'  $$
2. Since light has a finite speed, use the retarded time $t_{r}\equiv t- \mathfrak{r}/c$. Add this as a dependency of $\rho(\mathbf{r}',t_{r})$ and $\mathbf{J}(\mathbf{r}',t_{r})$, while $V(\mathbf{r},t)$ and $\mathbf{A}(\mathbf{r},t)$ remain dependent on current time.
3. Prove this is true by showing these obey Maxwell's law in potential. Remember that $t_{r}$ depends on space too, so also $\rho$ and $\mathbf{J}$. Start with the gradient of $V$. $\nabla \rho=-\dot{\rho}/c\, \hat{\boldsymbol{\mathfrak{r}}}$ since $\nabla \mathfrak{r}=\hat{\boldsymbol{\mathfrak{r}}}$. Also $\nabla(1/\mathfrak{r})=-\hat{\boldsymbol{\mathfrak{r}}}/\mathfrak{r}^{2}$.
4. Take the divergence to find the Laplacian with $\nabla\cdot(a\mathbf{F})=a(\nabla\cdot \mathbf{F})+\mathbf{F}\cdot (\nabla a)$ and $\nabla(\hat{\boldsymbol{\mathfrak{r}}}/\mathfrak{r}^{2})=4\pi \delta^{3}(\boldsymbol{\mathfrak{r}})$.
5. Introduce the d'Alembertian and you have the potential equation.
6. Same process for $\mathbf{A}$.
7. Advanced potentials (for $t_{a}\equiv t+\mathfrak{r}/c$) are technically valid but discarded.

**Jefimenko's equations**
1. Add the retarded potentials is $\mathbf{E}=-\nabla V-\frac{ \partial \mathbf{A} }{ \partial t }$ and $\mathbf{B}=\nabla\times \mathbf{A}$ and run the math. Much of it is similar to the retarded potential derivation. The curl of $\mathbf{J}$ is easier to calculate component-by-component.

**Liénard-Wiechert potentials**
1. Start from retarded electric potential. Realize that the solution can't quite be the same as the static one, as the retarded potential distorts $\rho(\mathbf{r}',t_{r})$ across time, since signals from different parts of the distribution will arrive at different times.
2. Train example. It looks longer if you are standing in front of it and it's coming towards you. This is because by the time the light from the back reaches you, the train has moved forward and you see the front closer to you, so it's stretched out.