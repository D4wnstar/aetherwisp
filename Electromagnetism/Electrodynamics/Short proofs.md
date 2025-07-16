---
wiki-publish: true
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
3. Train is $L$ long, but back light needs to travel $L'$ which is $L$ plus distance traveled by train in the time it takes for light to reach. Time to reach is same, so
   $$\frac{L'}{c}=\frac{L'-L}{v}\quad\to \quad L'=\frac{L}{1-v/c}$$
4. If at an angle $\theta$, if observer is far enough for front and back light beams to be approximately parallel, the distance traveled by light is $L'\cos \theta$, so
   $$\frac{L'\cos \theta}{c}=\frac{L'-L}{v}\quad\to \quad L'=\frac{L}{1-v\cos \theta/c}$$
5. $v\cos \theta=\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{v}$, so volume is shrunk by
   $$\tau'=\frac{\tau}{1-\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{v}/c}$$
6. Throw this in volume integral for potential, get old potential rescaled by $\tau'$.
7. Retarded time is implied by $\lvert \mathbf{r}-\mathbf{w}(t_{r}) \rvert =c(t-t_{r})$. Call left side $\boldsymbol{\mathfrak{r}}$ since it is unique (if it weren't particle would need to travel faster than $c$). This guarantees that an observer feels only one Liénard-Wiechert at any given time.
8. Vector potential is found by $\mathbf{J}=\rho \mathbf{v}$. $\mathbf{v}$ comes out of integral and you get $V$ again.

**Electromagnetic radiation**
1. Use Poynting's theorem, no $u$ since it's constant, flip sign so that power is exiting: $P=\oint_{\mathcal{S}}\mathbf{S}\cdot d\mathbf{a}$. Surface is a really big sphere.
2. Since $c$ is finite, power felt on the sphere is due to signal at $t_{0}=t-r/c$. Then, send sphere radius to infinity: $P_\text{rad}(t_{0})=\lim_{ r \to \infty }P(r,t_{0}+r/c)$.
3. Sphere area goes like $\sim r^{2}$, so any field that goes like less than $\sim r^{-2}$ will vanish when $r\to \infty$. Since $P\propto \mathbf{E}\times \mathbf{B}$, the only fields that matters are the $\sim r^{-1}$ terms in Jefimenko's equations (acceleration field for point charge).

**Electric dipole radiation**
1. Take two charges $q(t)$ and $-q(t)$, oscillate in phase $q(t)=q_{0}\cos \omega t$, dipole moment is $\mathbf{p}(t)=p_{0}\cos \omega t\ \hat{\mathbf{z}}$ with $p_{0}=q_{0}d$. Charges are at $\mathfrak{r}_{\pm}=\sqrt{ r^{2}\mp rd\cos \theta+ \left( d/2 \right)^{2} }$.
2. Start from superposition of Liénard-Wiechert potential with $\mathbf{v}=0$.
3. Apply perfect dipole approximation, $d\ll r$.
4. Approximate $\mathfrak{r}_{\pm}$ by factoring out $r^{2}$ and use binomial expansion to first order.
5. Plug into cosine term of potential, use cosine sum-to-product, apply large wavelength approximation $d\ll \lambda\sim c/\omega$ which implies $\omega d/c\ll 1$ to set $\cos(\ldots)\simeq 1$ and $\sin x\simeq x$.
6. Combine result with binomial expansion of $1/\mathfrak{r}_{\pm}$ to get $V$.
7. Apply far field approximation $r\gg c/\omega$ (equivalent: $r\gg \lambda$) to drop $r^{-2}$ terms and be left with the radiated potential.
8. Magnetic vector potential starts from $\mathbf{I}(t)=\frac{dq}{dt}\hat{\mathbf{z}}=-q_{0}\omega \sin(\omega t)\hat{\mathbf{z}}$. Put this in integral with as $\mathbf{I}(t_{r})$ and integrate in the line between the charges from $-d/2$ to $d/2$. Since integration adds $d$, approximate integral with its value at the center $r$ since $d\ll r$.
9. Fields are just doing $\nabla V$, $\frac{ \partial \mathbf{A} }{ \partial t }$ and $\nabla\times \mathbf{A}$.
10. Waves are spherical monochromatic of frequency $\omega$. Poynting vector and irradiance are the usual, power is $\langle P \rangle=\int_{\mathcal{S}}\langle \mathbf{S} \rangle\cdot d\mathbf{a}$. Power ends up $P\propto \omega^{4}$, ultraviolet catastrophe.

**Magnetic dipole radiation**
1. Take a current $I(t)=I_{0}\cos \omega t$ on loop of radius $b$. Magnetic dipole is $\mathbf{m}(t)=\pi b^{2}I(t)\hat{\mathbf{z}}=m_{0}\cos(\omega t)\hat{\mathbf{z}}$ where $m_{0}=\pi b^{2}I_{0}$.
2. No electric charge, no electric potential, $V=0$.
3. Vector potential is from integrating the current over the loop.
4. Complicated figure for angles, notice $\mathbf{A}$ must be over $y$ since $x$ is cancelled by equal and opposite contributions. Integrate over polar coordinates in $\phi'$ with $\mathfrak{r}=\sqrt{ r^{2}+b^{2}-2rb\cos \psi }=\sqrt{ r^{2}+b^{2}-2rb\sin \theta \cos \phi' }$ since $rb\cos \psi=\mathbf{r}\cdot \mathbf{b}=rb\sin \theta \cos \phi'$.
5. Apply perfect dipole approximation $b\ll r$.
6. Approximate $\mathfrak{r}$ by factoring out $r^{2}$ and use binomial expansion to first order.
7. Plug into cosine term of potential, use cosine sum-to-product, apply large wavelength approximation $d\ll \lambda\sim c/\omega$ which implies $\omega d/c\ll 1$ to set $\cos(\ldots)\simeq 1$ and $\sin x\simeq x$.
8. Combine result with binomial expansion of $1/\mathfrak{r}$, put into integral, first term integrates to zero, second and third involve $\int_{0}^{2\pi}\cos ^{2}\phi'd\phi'=\phi$. What remains is $\mathbf{A}$.
9. Apply far field approximation $r\gg c/\omega$ (equivalent: $r\gg \lambda$) to drop $r^{-2}$ terms and be left with the radiated vector potential.
10. Fields are just doing $\nabla V$, $\frac{ \partial \mathbf{A} }{ \partial t }$ and $\nabla\times \mathbf{A}$.
11. Waves are same as electric dipole. Power is incredibly small compared to electric dipole so generally ignore it.

**Radiation from arbitrary source**
1. Generic charge distribution of finite volume near the origin. Figure with volume element of charge. 
2. Start with retarded electric potential where $\mathfrak{r}=\sqrt{ r^{2}+r'^{2}-2\mathbf{r}\cdot \mathbf{r}' }$. $\mathbf{r}'$ is from origin to volume element $d\tau'$.
3. Apply small source approximation $r'\ll r$ for all integration.
4. Approximate $\mathfrak{r}$ by factoring out $r^{2}$ and use binomial expansion to first order to get $\mathfrak{r}\simeq r\left( 1- \mathbf{r}\cdot\mathbf{r}'/r^{2} \right)$.
5. Charge distribution depend on (sort-of) retarded time $t_{0}=t-r/c$ plus the extra term above: $\rho(\mathbf{r}',t_{0}+\hat{\mathbf{r}}\cdot \mathbf{r}'/c)$.
6. Expand $\rho$ in Taylor series in t about $t_{0}$ to get
   $$\rho\left( \mathbf{r}',t- \frac{\mathfrak{r}}{c} \right)\simeq \rho(\mathbf{r}',t_{0})+\dot{\rho}(\mathbf{r}',t_{0})\left( \frac{\hat{\mathbf{r}}\cdot\mathbf{r}'}{c} \right)+ \frac{1}{2}\ddot{\rho}\left( \frac{\hat{\mathbf{r}}\cdot \mathbf{r}'}{c} \right)^{2}+ \frac{1}{3!}\dddot{\rho}\, \left( \frac{\hat{\mathbf{r}}\cdot \mathbf{r}'}{c} \right)^{3}+\ldots$$
7. Apply the "large wavelength" approximation to keep only the first order term
   $$r'\ll \frac{c}{\lvert \ddot{\rho}/\dot{\rho} \rvert }, \frac{c}{\lvert \dddot{\rho},\dot{\rho }\rvert^{1/2} }, \frac{c}{\lvert \ \ddddot{\rho}\ ,\dot{\rho} \rvert^{1/3} }\ldots$$
8. Combine first order of $\rho$ with binomial expansion of $1/\mathfrak{r}$ to get the integral for $V$.
9. Drop second order in $\mathbf{r}'$, integrals left are the normal point charge potential plus multipole expansion term $\mathbf{p}$ and dynamic term $\dot{\mathbf{p}}$.
10. Vector potential is skipped, but $\int_{\mathcal{V}}\mathbf{J}d\tau'=\dot{\mathbf{p}}$ and plug this in the integral for $\mathbf{A}$.
11. Fields are still just doing $\nabla V$, $\frac{ \partial \mathbf{A} }{ \partial t }$ and $\nabla\times \mathbf{A}$, but also remember to drop $\sim r^{-2}$ terms in the far field limit. The only term that survives in $\mathbf{E}$ is the $\sim \ddot{\mathbf{p}}$ one.
12. Since $\mathbf{B}\propto\mathbf{E}\propto  \ddot{\mathbf{p}}$, the Poynting vector $\mathbf{S}\propto \ddot{p}^{2}$ and so does the radiated power $P_\text{rad}$. If you set $\mathbf{p}(t)=q\mathbf{d}(t)$ as the dipole moment of an individual charge, then $\ddot{\mathbf{p}}(t)=q\mathbf{a}(t)$ and so $P_\text{rad}\propto a^{2}$, which is the Larmor formula.

**Larmor formula**
1. Start from the fields given by the Liénard-Wiechert potentials.
2. Imagine the usual large sphere of radius $r$ around the charge, whose area goes like $\sim r^{2}$. As such, when integrating the Poynting vector, only $\sim r^{-2}$ terms survive, which are the products of $\sim r^{-1}$ terms in $\mathbf{E}$ and $\mathbf{B}$. Anything less vanishes. Thus, keep the acceleration field only
   $$\mathbf{E}_\text{rad}=\frac{1}{4\pi \varepsilon_{0}} \frac{\mathfrak{r}}{(\boldsymbol{\mathfrak{r}}\cdot \mathbf{u})^{3}}\boldsymbol{\mathfrak{r}}\times(\mathbf{u}\times \mathbf{a})$$
3. Poynting vector ends up being $\mathbf{S}_\text{rad}=(1/\mu_{0}c)E_\text{rad}^{2}\hat{\boldsymbol{\mathfrak{r}}}$.
4. Only the case $\mathbf{v}=0$ is easy. In this case, algebra handles the form of $\mathbf{E}_\text{rad}$ then take the square to get $\mathbf{S}$. Integrate over a sphere, $\mathfrak{r}$ dependency disappears so no need to take the limit, and you get the Larmor formula.
5. $\mathbf{v}\neq 0$ is hard and ends up depending on $\gamma^{6}$. Also, its angular distribution is $\mathbf{v}$-dependent and gets stretched in the direction of $\mathbf{v}$, causing bremmstrahlung.

**Radiation reaction (periodic motion)**
1. Conservation of energy demands that energy radiated comes from kinetic energy, which means a radiating particle accelerates less than a neutral one, due to a self-force.
2. Start from Larmor formula. Generally, the energy stored in the fields (which is where the radiated energy comes from) is mixed between acceleration and velocity fields, so you need to care for both.
3. If motion is periodic, then the state of the particle at the start and end of a cycle is the same, so the velocity field is the same before and after and can be neglected if we only consider changes over a fully cycle. Power loss in entirely due to Larmor formula then.
4. Energy lost over a period is integral of self-force scalar velocity, which is also equal to integral of Larmor formula:
   $$U=\int_{t_{1}}^{t_{2}}\mathbf{F}_\text{rad}\cdot \mathbf{v}dt=- \frac{\mu_{0}q^{2}}{6\pi c}\int_{t_{1}}^{t_{2}}a^{2}dt$$
5. Express $\mathbf{a}=d\mathbf{v}/dt$, then integrate by parts to move the derivative and get $\mathbf{v}\cdot d^{2}\mathbf{v}/dt^{2}=\mathbf{v}\cdot \dot{\mathbf{a}}$. Boundary term vanishes because start and end states are the same. 
6. Equate the integrals, move to left side, it's all equal to zero. One possible solution is setting part of the integrand to zero, which leads to the Abraham-Lorentz formula.
7. If you equate it to Newton's second law, you get a first order ODE in $a$, which gives exponential rise. Basically, $a(t)$ blows up exponentially by itself just due to radiation reaction. If you try to set $a_{0}=0$ to prevent this, you get preacceleration and causality is broken. No one really knows why.

**Relativity of simultaneity**
1. Train moves with constant speed. A light bulb is at the center of the wagon. It is turned on.
2. An observer on the train will see the light reach the sides of the wagon at the same time.
3. An observer on the ground will see them desynchronized, because the light always travels at $c$ regardless of the speed of the train (in Galilean relativity, the speed of the train would be added onto $c$, canceling the effect). Thus, the space needed to reach the back is smaller than the front so, at the same speed, the light reaches the back first.

**Relativity of simultaneity (from Lorentz transformation)**
1. Take two events $A=(t_{A},x_{A})=(0,0)$ and $B=(t_{B},x_{B})=(0,b)$. They are simultaneous and separated by distance $b$.
2. Apply a Lorentz transformation over the $x$ axis to get $t_{A}'=0$ and $t_{B}'=-\gamma b v_{x}/c^{2}$. They are no longer simultaneous when $v_{x}\neq 0$.
3. The sign of the speed determines the ordering. If $v_{x}>0$, then $B$ happens before. If $v_{x}<0$, then $B$ happens after.

**Time dilation**
1. Train moves with constant speed $v$. A light bulb is on the ceiling of the wagon, height $h$. It is turned on and the time it takes to reach the floor is measured.
2. An observer on the train will record the time taken by light to go straight down to the floor, $\Delta \tilde{t}=h/c$.
3. An observer on the ground will record the time taken to go down the diagonal to the floor and due to the train motion. The train moves $v\Delta t$ while light reaches the floor. The total distance then is $\sqrt{ h^{2}+(v\Delta t)^{2} }$, so $\Delta t=\sqrt{ h^{2}+(v\Delta t)^{2} }/c$. Solve for $\Delta t$, notice the presence of $\gamma$, get $\Delta \tilde{t}=\Delta t/\gamma$.

**Time dilation (from Lorentz transformation)**
1. An observer in $\mathcal{S}$ reads several moving clocks. $\mathcal{S}'$ is the frame in which these clocks are at rest. They all read different times depending on the distance.
2. Time part of Lorentz transformation is $t'=-\gamma  \frac{v}{c^{2}}x$. Assuming $v>0$, any clock at $x>0$ will be behind and any at $x<0$ will be ahead.
3. Clocks moving relative to the observer are desynchronized and cannot be trusted with consistent measurements.
4. Pick some clock in $\mathcal{S}'$ at $x'=a$ and observe it over $\Delta t=t_\text{end}-t_\text{start}$. The clock moves at speed $v$ because it's in $\mathcal{S}'$ compared to $\mathcal{S}$. Time transformation is
   $$t=\gamma\left( t'+ \frac{v}{c^{2}}a \right)$$
5. Put this in $\Delta t$ using $t'_\text{end}$ and $t'_\text{start}$ respectively to get $\Delta t=\gamma \Delta t'$.

**Length contraction**
1. Train moves with constant speed $v$. A light bulb is on one end of the wagon, length $\Delta \tilde{x}$. On the other side there is a mirror. It is turned on and the time it takes to reach the other side and bounce back is measured.
2. An observer on the train will record the time taken by light to go straight to the other side and bounce back, $\Delta \tilde{t}=2\Delta \tilde{x}/c$.
3. An observer on the ground has to consider the motion of the train. By the time light hits the mirror the train has moved $v\Delta t_{1}$. Between the bounce and when it comes back the train moves $v\Delta t_{2}$. The times then are $\Delta t_{1}=(\Delta x+v\Delta t_{1})/c$. Same for 2. Solve for $\Delta t_{1}$ and $\Delta t_{2}$, sum them, apply time dilation and compare them to get $\Delta \tilde{x}=\gamma \Delta x$.

**Length contraction (from Lorentz transformation)**
1. A metal pipe is at rest in $\mathcal{S}'$. An observer in $\mathcal{S}$ sees it move at speed $v$.
2. The rest length of the pipe (the one in $\mathcal{S}'$) is $\Delta x'=x_{r}'-x_{l}'$.
3. Measuring the length simultaneously in $\mathcal{S}$ returns $\Delta x=x_{r}-x_{l}$.
4. Apply Lorentz transformation to $x'_{r}$ and $x'_{l}$ in $\Delta x'$ to find $\Delta x'=\gamma \Delta x$.

**Lorentz transformation**
1. Some event $E=(x,y,z,t)$ is in $\mathcal{S}$. We want to convert it to another inertial frame $\mathcal{S}'$.
2. Say $\mathcal{S}'$ moves at speed $v$ on the $x$ axis compared to $\mathcal{S}$, and they overlap at $t=0$ so that $\mathcal{S}\equiv \mathcal{S}'$ in that moment.
3. In Galilean relativity, the only change at time $t$ is the $x$ coordinate $x=x'+vt$.
4. In special relativity, these can't work because length contraction affects $x'$ and time dilation changes $t'$. $y$ and $z$ are safe since they are not on the axis of motion.
5. Say at time $t$ we measure a distance $d$ between the origin of $\mathcal{S}'$ and the $x$-component of $E$, so that $x=d+vt$. In Galilean relativity, $d=x'$, but in special relativity, $d=x'/\gamma$, which implies $x'=\gamma(x-vt)$.
6. The same applies in reverse to $x$ from $x'$, giving $x=\gamma(x'+vt')$. Substitute $x'$ from before, solve for $t'$, get $t'=\gamma\left( t- \frac{v}{c^{2}}x \right)$.
7. Put these all in a curly brace and you get the Lorentz transformations.

**Lorentz transformation (as hyperbolic rotation)**
1. Write Lorentz transformation in matrix form. It has the shape of a 4D hyperbolic rotation matrix. Top left elements must be $\cosh \theta=\gamma$ and $-\sinh=-\beta \gamma$. Divide the second by the first, find $\beta=\tanh\theta$, where $\theta$ is the rapidity.

**Einstein velocity addition rule**
1. Some object moves $dx$ in $\mathcal{S}$. Its velocity in that frame is $u=dx/dt$.
2. In another frame $\mathcal{S}'$, moving with velocity $v$ relative to $\mathcal{S}$, the distance it moved is $dx'=\gamma(dx-vdt)$ due to Lorentz transformation.
3. Time take to move in $\mathcal{S}'$ is $dt'=\gamma\left( dt- \frac{v}{c^{2}}dx \right)$.
4. The velocity in $\mathcal{S}'$ is $dx'/dt'$, which gives the formula with some algebra.

**Relativistic energy-momentum relation**
1. Take the norm $p^{\mu}p_{\mu}$ using $p^{\mu}=(\gamma mc,\gamma m\mathbf{v})$ for components, get $-m^{2}c^{2}$.
2. Take the norm using $p^{\mu}=\left( \frac{E}{c},\mathbf{p} \right)$, get $- \frac{E^{2}}{c^{2}}+p^{2}$.
3. Match the two to get $-\frac{E^{2}}{c^{2}}+p^{2}=-m^{2}c^{2}$ and reorder.

**Magnetism as a relativistic phenomenon**
1. Consider a wire with linear charge density $\lambda$ going one direction and $-\lambda$ going the other. They are both moving with speed $v$. The current is $I=2\lambda v$.
2. Assume a point charge $q$ passes by at speed $u$ moving parallel to the wire in the positive direction. This frame, attached to the wire, is $\mathcal{S}$. The frame attached to $q$ is $\mathcal{S}'$.
3. In $\mathcal{S}$, there is not electric field because the charges cancel.
4. In $\mathcal{S}'$, the speeds of the charge densities change according to the Einstein velocity addition rule
   $$v_{\pm}=\frac{v\mp u}{1\mp vu/c^{2}}$$
5. The charge sees the wire as charges as contracted due to length contraction. This increases the densities. However, since the speeds are different, the densities contract in different ways as $\lambda_{\pm}=\gamma_{\pm}\lambda_{0}$ and the charges are no longer neutral. Therefore, there is an electric field of a wire of charge $\lambda _\text{tot}=\lambda_{+}+\lambda_{-}=(\gamma_{+}+\gamma_{-})\lambda_{0}\neq 0$.
6. Find $\gamma_{\pm}$ by algebra, then use it to express $\lambda _\text{tot}$, then use it to find the field $E$ and the force $F'$ in $\mathcal{S}'$.
7. If a force exists in $\mathcal{S}'$, one must exist in $\mathcal{S}$ too, and it is the (anti-)Lorentz transform $F=F'/\gamma$. Since a force exists despite the lack of electric field, the force is a magnetic one.

**Transformations of E and B**
1. Need two things: electric charge must be relavistically invariant, and transformation rules need to be the same regardless of the origin of the fields.
2. Use capacitor flat on the $xz$ plane (field goes over $y$), plates have densities $\pm\sigma_{0}$ and its sides are $l$ and $w$. Field is $E_{y}=\sigma_{0}/\varepsilon_{0}$.
3. Start in a frame $\mathcal{S}_{0}$ in which the capacitor is at rest. Then, change to a frame $\mathcal{S}$ in which the capacitor is moving at speed $v_{0}$.
4. The densities get contracted so $\sigma=\gamma_{0}\sigma_{0}$ and the new field is $E_{y}=\sigma/\varepsilon_{0}$. They also create a surface current $\mathbf{K}_{\pm}=\mp \sigma v_{0}\hat{\mathbf{x}}$ making a magnetic field $B_{z}=-\mu_{0}\sigma v_{0}$.
5. Change to another frame $\mathcal{S}'$ moving velocity $v$ relative to $\mathcal{S}$ and velocity $v'$ relative to $\mathcal{S}_{0}$, which is found by $v'=(v+v_{0})/(1+vv_{0}/c^{2})$. The fields will be $E_{y}'=\sigma'/\varepsilon_{0}$ and $B_{z}'=-\mu_{0}\sigma'v'$, with $\sigma'=\gamma'\sigma_{0}$, but since $\sigma= \gamma_{0}\sigma_{0}$ we have $\sigma'=(\gamma'/\gamma_{0})\sigma$.
6. Find the ratio of the gammas, put it in the fields, invert the field formulas to express a primed field in terms of both unprimed fields, and you get the transformations for $E_{y}$ and $B_{z}$.
7. Do the same thing on the other axis of the capacitor, you get the same thing but for $E_{z}$ and $B_{y}$.
8. On the third axis, the electric field does not change because the movement is perpendicular to the surface charges, causing no contraction. This gives no info on the magnetic field.
9. To find the magnetic field, imagine a solenoid over the $x$ axis. The magnetic field is $B_{x}=\mu_{0}nI$.
10. Change to $\mathcal{S}'$ and let the solenoid move at speed $v$. The coils per unit length compress to become $n'=\gamma n$. The electric current is time-dilated to $I'=I/\gamma$. These two changes cancel out to keep the field identical.
11. The transformations end up being
    $$\begin{align} &E'_{x}=E_{x},&E'_{y}&=\gamma(E_{y}-vB_{z}),&E'_{z}&=\gamma(E_{z}+vB_{y}) \\ &B'_{x}=B_{x},&B'_{y}&=\gamma\left( B_{y}+ \frac{v}{c^{2}}E_{z} \right),&B'_{z}&=\gamma\left( B_{z}- \frac{v}{c^{2}}E_{y} \right) \end{align}$$
