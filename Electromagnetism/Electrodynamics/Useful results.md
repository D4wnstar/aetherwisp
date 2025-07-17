---
wiki-publish: true
---
### Preparatory topics
**Poynting's theorem**
$$P=\frac{ \partial U }{ \partial t } =-\frac{ \partial  }{ \partial t } \int_{\mathcal{V}}u(\mathbf{r})\ d\tau-\oint_{\mathcal{S}}\mathbf{S}\cdot d\mathbf{a},\qquad-\frac{ \partial u(\mathbf{r}) }{ \partial t }=\mathbf{E}\cdot \mathbf{J} -\nabla\cdot\mathbf{S}$$

**Poynting vector**
$$\mathbf{S}\equiv \frac{1}{\mu_{0}}\mathbf{E}\times \mathbf{B}$$

**Electromagnetic energy density**
$$u=\frac{1}{2}\left( \varepsilon_{0}E^{2}+ \frac{1}{\mu_{0}}B^{2} \right)$$

**Momentum density and angular momentum density**
$$\mathbf{g}=\varepsilon_{0}\mu_{0}\mathbf{S}=\varepsilon_{0}(\mathbf{E}\times \mathbf{B})=\frac{1}{c^{2}}\mathbf{S},\qquad\boldsymbol{\ell}=\mathbf{r}\times \mathbf{g}=\varepsilon_{0}[\mathbf{r}\times(\mathbf{E}\times \mathbf{B})]$$

**Maxwell stress tensor**
$$T_{ij}=\varepsilon_{0}\left( E_{i}E_{j}- \frac{1}{2}\delta_{ij}E^{2} \right)+ \frac{1}{\mu_{0}}\left( B_{i}B_{j}- \frac{1}{2}\delta_{ij}B^{2} \right)$$

**Lorentz force and force density (tensor form)**
$$\mathbf{F}=\oint_{\mathcal{S}}\mathrm{T}\cdot d\mathbf{a}-\varepsilon_{0}\mu_{0}\frac{d}{dt} \int_{\mathcal{V}}\mathbf{S}\ d\tau,\qquad\mathbf{f}=\nabla\cdot \mathrm{T}-\varepsilon_{0} \mu_{0} \frac{ \partial \mathbf{S} }{ \partial t } $$

**d'Alembertian**
$$\square ^{2}\equiv \nabla ^{2}- \frac{1}{v^{2}}\frac{ \partial ^{2} }{ \partial t^{2} } $$
### Electromagnetic waves
**General relations**
$$k=\frac{2\pi}{\lambda},\quad \omega=\frac{2\pi}{T},\quad\omega=\frac{c}{n(\omega)}k,\quad v_{p}=\frac{\omega}{k(n)}=\frac{c}{n},\quad v_{g}=\frac{ \partial \omega }{ \partial k },\quad I=\lvert \psi \rvert ^{2}=\frac{P}{4\pi d^{2}}$$
where $\psi$ is a wave. The other form of $I$ is for a spherical wave with $P$ emitted power at distance $d$.

**Monochromatic plane wave (real and complex)**
$$u(\mathbf{r},t)=A\sin(\mathbf{k}\cdot \mathbf{r}-\omega t+\varphi)$$
$$\tilde{u}(\mathbf{r},t)=Ae^{i[\mathbf{k}\cdot \mathbf{r}-\omega t+\varphi]}\quad \text{where}\quad u(\mathbf{r},t)=\mathrm{Re}(\tilde{u}(\mathbf{r},t))$$
The phasor is $Ae^{i\varphi}$.

**Electromagnetic sine wave (complex)**
$$\begin{align}
\tilde{\mathbf{E}}(\mathbf{r},t)&=\tilde{E}_{0}e^{i(\mathbf{k}\cdot \mathbf{r}-\omega t)}\hat{\mathbf{n}} \\
\tilde{\mathbf{B}}(\mathbf{r},t)&=\frac{1}{c}\tilde{E}_{0}e^{i(\mathbf{k}\cdot \mathbf{r}-\omega t)}(\hat{\mathbf{k}}\times \hat{\mathbf{n}})=\frac{1}{c}\hat{\mathbf{k}}\times \tilde{\mathbf{E}}
\end{align}$$

**Electromagnetic sine wave (real)**
$$\begin{align}
\mathbf{E}(\mathbf{r},t)&=E_{0}\cos(\mathbf{k}\cdot \mathbf{r}-\omega t+\varphi)\hat{\mathbf{n}} \\
\mathbf{B}(\mathbf{r},t)&=\frac{1}{c}E_{0}\cos(\mathbf{k}\cdot \mathbf{r}-\omega t+\varphi)(\hat{\mathbf{k}}\times \hat{\mathbf{n}})=\frac{1}{c}\hat{\mathbf{k}}\times \mathbf{E}
\end{align}$$
Also
$$B_{0}=\frac{k}{\omega}E_{0}=\frac{1}{c}E_{0}$$

**Averaged quantities (vacuum)**
$$\langle u \rangle =\frac{\varepsilon_{0}}{2}E_{0}^{2},\quad \langle \mathbf{S} \rangle=\frac{\varepsilon_{0}c}{2}E_{0}^{2}\ \hat{\mathbf{n}},\quad I\equiv \lvert \langle \mathbf{S} \rangle  \rvert ,\quad \langle \mathbf{g} \rangle =\frac{\varepsilon_{0}}{2c}E_{0}^{2}\ \hat{\mathbf{n}}$$
Multiply by $2$ for non-averages.

**Averaged quantities (matter)**
$$\langle u \rangle =\frac{\varepsilon}{2}E_{0}^{2},\quad \langle \mathbf{S} \rangle=\frac{\varepsilon c}{2n}E_{0}^{2}\ \hat{\mathbf{n}}$$
Multiply by $2$ for non-averages. $\langle \mathbf{g} \rangle$ is still debated.

**Radiation pressure**
$$P=\frac{1}{A} \frac{\Delta \lvert \mathbf{p} \rvert }{\Delta t}=\frac{\varepsilon_{0}}{2}E_{0}^{2}=\frac{I}{c}$$

**Irradiances (normal incidence)**
(Tip: Fields superimpose due to Maxwell's equations' linearity. Irradiance is quadratic so it doesn't.)
$$I_{I}=\frac{\varepsilon c}{2n_{1}}E_{0,I}^{2},\qquad I_{R}=\frac{\varepsilon c}{2n_{1}}E_{0,R}^{2},\qquad I_{T}=\frac{\varepsilon c}{2n_{2}}E_{0,T}^{2}$$

**Reflection and transmission coefficients (normal incidence + nonmagnetic material)**
$$R\equiv \frac{I_{R}}{I_{I}}=\left( \frac{E_{0,R}}{E_{0,I}} \right)^{2}=\left( \frac{n_{1}-n_{2}}{n_{1}+n_{2}} \right)^{2},\qquad T\equiv \frac{I_{T}}{I_{I}}=\frac{\varepsilon_{2}n_{1}}{\varepsilon_{1}n_{2}}\left( \frac{E_{0,T}}{E_{0,I}} \right)^{2}=\frac{4n_{1}n_{2}}{(n_{1}+n_{2})^{2}}$$

**Irradiances (oblique incidence)**
$$I_{I}=\langle \mathbf{S} \rangle\cdot \hat{\mathbf{x}}=\frac{\varepsilon_{1}c}{2n_{1}}E_{0,I}^{2}\cos \theta_{I},\qquad I_{R}=\frac{\varepsilon_{1}c}{2n_{1}}E_{0,I}^{2}\cos \theta_{R},\qquad I_{R}=\frac{\varepsilon_{2}c}{2n_{2}}E_{0,I}^{2}\cos \theta_{T}$$
Normal incidence when $\theta_{I}=\theta_{R}=0$.

**Reflection and transmission coefficients (oblique incidence)**
$$R=\frac{I_{R}}{I_{I}}=\left( \frac{\alpha-\beta}{\alpha+\beta} \right)^{2},\qquad T=\frac{I_{T}}{I_{I}}=\frac{4\alpha \beta}{(\alpha+\beta)^{2}}$$
where
$$\alpha=\frac{\cos \theta_{T}}{\cos \theta_{I}},\qquad\beta=\frac{\mu_{1}n_{2}}{\mu_{2}n_{1}}$$
Normal incidence when $\alpha=1$.

**Laws of geometrical optics**
1. Incident, reflected and transmitted waves are coplanar.
2. Reflection angle is identical to incident angle, $\theta_{I}=\theta_{R}$.
3. Transmitted angle is given by Snell's law
$$\frac{\sin\theta_{T}}{\sin \theta_{I}}=\frac{n_{1}}{n_{2}}$$

**Brewster's angle**
Angle at which there is no reflection, $R=0$.
$$\theta_{B}\simeq\arctan\left( \frac{n_{2}}{n_{1}} \right)$$

**Critical angle**
Angle after which there is no transmission, $T=0$ (total internal reflection). Only when going from optically dense to thin, $n_\text{inner}>n_\text{outer}$. When $n_\text{inner}<n_\text{outer}$, critical angle is $\pi/2$, so orthogonal incidence, i.e. total reflection occurs when the wave is parallel to the surface.
$$\theta_{C}\equiv \arcsin\left( \frac{n_\text{outer}}{n_\text{inner}} \right)$$

**Etendue (acceptance)**
Etendue (or acceptance) is a measure of how spread out light is in area and angle. The angle of maximum etendue is
$$\theta_{e}=\arcsin\left(\sqrt{ n_{1}^{2}-n_{2}^{2} } \right)$$
### Potentials
**Electrodynamic electric and magnetic fields**
$$\mathbf{E}=-\nabla V-\frac{ \partial \mathbf{A} }{ \partial t },\qquad \mathbf{B}=\nabla\times \mathbf{A} $$

**Maxwell's equation (potential form, unspecified gauge)**
$$\square ^{2}V+\frac{ \partial L }{ \partial t } =- \frac{\rho}{\varepsilon_{0}},\qquad\square ^{2}\mathbf{A}-\nabla L=-\mu_{0}\mathbf{J}$$
where $L\equiv \nabla\cdot \mathbf{A}+\mu_{0}\varepsilon_{0}\ \partial V/\partial t$.

**Maxwell's equation (potential form, Lorenz gauge)**
$$\square ^{2}V=- \frac{\rho}{\varepsilon_{0}},\qquad\square ^{2}\mathbf{A}=-\mu_{0}\mathbf{J}$$

**Coulomb and Lorenz gauges**
$$\nabla\cdot \mathbf{A}=0,\qquad\nabla\cdot \mathbf{A}=-\mu_{0}\varepsilon_{0}\frac{ \partial V }{ \partial t} $$

**Jefimenko's equations**
$$\mathbf{E}(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}}\int_{\mathcal{V}}\frac{\rho(\mathbf{r}',t)}{\mathfrak{r}^{2}}\hat{\boldsymbol{\mathfrak{r}}}+ \frac{\dot{\rho}(\mathbf{r}',t)}{c\mathfrak{r}}\hat{\boldsymbol{\mathfrak{r}}}- \frac{\dot{\mathbf{J}}(\mathbf{r}',t)}{c^{2}\mathfrak{r}}d\tau'$$
$$\mathbf{B}(\mathbf{r},t)=\frac{\mu_{0}}{4\pi}\int_{\mathcal{V}}\frac{\mathbf{J}(\mathbf{r}',t_{r})}{\mathfrak{r}^{2}}+ \frac{\dot{\mathbf{J}}(\mathbf{r}',t_{r})}{c\mathfrak{r}}d\tau'$$

**Liénard-Wiechert potentials**
Retarded potentials of a point charge
$$V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}} \frac{qc}{(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})},\qquad\mathbf{A}(\mathbf{r},t)=\frac{\mu_{0}}{4\pi} \frac{qc\mathbf{v}}{(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})}=\frac{\mathbf{v}}{c^{2}}V(\mathbf{r},t)$$

**Fields of a point charge**
Derived from the Liénard-Wiechert potentials
$$\mathbf{E}(\mathbf{r},t)=\frac{q}{4\pi \varepsilon_{0}} \frac{\mathfrak{r}}{(\boldsymbol{\mathfrak{r}}\cdot \mathbf{u})^{3}}
[(c^{2}-v^{2})\mathbf{u}+\boldsymbol{\mathfrak{r}}\times(\mathbf{u}\times \mathbf{a})],\qquad\mathbf{B}(\mathbf{r},t)=\frac{1}{c}\hat{\boldsymbol{\mathfrak{r}}}\times \mathbf{E}(\mathbf{r},t)$$
where $\mathbf{u}\equiv c \hat{\boldsymbol{\mathfrak{r}}}-\mathbf{v}$.

**Fields of a point charge (constant velocity)**
$$\mathbf{E}(\mathbf{r},t)=\frac{q}{4\pi \varepsilon_{0}} \frac{1- v^{2}/c^{2}}{(1-(v^{2}/c^{2})\sin ^{2}\theta)^{3/2}} \frac{\hat{\mathbf{R}}}{R^{2}},\qquad\mathbf{B}(\mathbf{r},t)=\frac{1}{c^{2}}(\mathbf{v}\times \mathbf{E})$$
where $\mathbf{R}\equiv \mathbf{r}-\mathbf{v}t$ is the vector from the present location of the charge to $\mathbf{r}$ and $\theta$ is the angle between $\mathbf{R}$ and $\mathbf{v}$.
### Radiation
**Oscillating electric dipole (far field)**
$$V(r,\theta,t)=- \frac{p_{0}\cos\theta}{4\pi \varepsilon r}\frac{\omega}{c} \sin\left[ \omega\left( t- \frac{r}{c} \right) \right],\qquad\mathbf{A}(r,\theta,t)=- \frac{\mu_{0}p_{0}\omega}{4\pi r}\sin\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\mathbf{z}}$$
$$\mathbf{E}=- \frac{\mu_{0}p_{0}\omega ^{2}}{4\pi r}\sin \theta\cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\boldsymbol{\theta}},\qquad\mathbf{B}=- \frac{\mu_{0}p_{0}\omega ^{2}}{4\pi cr}\sin\theta\cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\boldsymbol{\phi}}$$
$$\mathbf{S}(\mathbf{r},t) =\frac{\mu_{0}}{c}\left[ \frac{p_{0}\omega ^{2}}{4\pi r} \sin\theta\cos\left[ \omega\left( t- \frac{r}{c} \right) \right] \right]^{2}\hat{\mathbf{r}},\qquad I=\frac{\mu_{0}p_{0}^{2}\omega^{4}}{32\pi ^{2}c} \frac{\sin^{2}\theta}{r^{2}},\qquad\langle P \rangle =\frac{\mu_{0}p_{0}^{2}\omega^{4}}{12\pi c}$$
(Tip: Fields superimpose due to Maxwell's equations' linearity. Irradiance is quadratic so it doesn't.)

**Oscillating magnetic dipole (far field)**
$$V=0,\qquad\mathbf{A}(r,\theta,t)=- \frac{\mu_{0}m_{0}\omega}{4\pi cr}\sin \theta \sin\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\boldsymbol{\phi}}$$
$$\mathbf{E}(r,t)=\frac{\mu_{0}m_{0}\omega ^{2}}{4\pi cr}\sin \theta \cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\boldsymbol{\phi}}$$
$$\mathbf{B}(r,t)=- \frac{\mu_{0}m_{0}\omega ^{2}}{4\pi c^{2}r}\sin \theta \cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\boldsymbol{\theta}}=- \frac{1}{c}\hat{\mathbf{r}}\times \mathbf{E}$$
$$\mathbf{S}(\mathbf{r},t)=\frac{\mu_{0}}{c}\left[ \frac{m_{0}\omega ^{2}}{4\pi cr} \sin\theta\cos\left[ \omega\left( t- \frac{r}{c} \right) \right] \right]^{2}\hat{\mathbf{r}},\quad I=\frac{\mu_{0}m_{0}^{2}\omega^{4}}{32\pi ^{2}c^{3}} \frac{\sin^{2}\theta}{r^{2}},\quad\langle P \rangle =\frac{\mu_{0}m_{0}^{2}\omega^{4}}{12\pi c^{3}}$$

**Small arbitrary source (far field)**
$$V(\mathbf{r},t)\simeq \frac{1}{4\pi \varepsilon_{0}}\left[ \frac{Q}{r}+ \frac{\hat{\mathbf{r}}\cdot \mathbf{p}(t_{0})}{r^{2}}+ \frac{\hat{\mathbf{r}}\cdot \dot{\mathbf{p}}(t_{0})}{rc} \right],\qquad\mathbf{A}(\mathbf{r},t)\simeq \frac{\mu_{0}}{4\pi r}\dot{\mathbf{p}}(t_{0})$$
Coordinate-free
$$\mathbf{E}(\mathbf{r},t)\simeq \frac{\mu_{0}}{4\pi r}[(\hat{\mathbf{r}}\cdot \ddot{\mathbf{r}})\hat{\mathbf{r}}-\ddot{\mathbf{p}}]=\frac{\mu_{0}}{4\pi r}\hat{\mathbf{r}}\times(\hat{\mathbf{r}}\times \ddot{\mathbf{p}}),\qquad\mathbf{B}(\mathbf{r},t)\simeq - \frac{\mu_{0}}{4\pi cr}\hat{\mathbf{r}}\times \ddot{\mathbf{p}}=- \frac{1}{c}\hat{\mathbf{r}}\times \mathbf{E}$$
Spherical coordinates
$$\mathbf{E}(r,\theta,t)\simeq \frac{\mu_{0}\ddot{p}(t_{0})}{4\pi r}\sin \theta\ \hat{\boldsymbol{\theta}},\qquad \mathbf{B}(r,\theta,t)\simeq \frac{\mu_{0}\ddot{p}(t_{0})}{4\pi cr} \sin \theta\ \hat{\boldsymbol{\phi}}$$
where $t_{0}$ is the time of radiation emission.
$$\mathbf{S}(\mathbf{r},t)\simeq \frac{\mu_{0}}{16\pi ^{2}cr^{2}}[\ddot{p}(t_{0})]^{2}\sin ^{2}\theta\ \hat{\mathbf{r}},\qquad P_\text{rad}(t_{0})\simeq \frac{\mu_{0}}{6\pi c}[\ddot{p}(t_{0})]^{2}$$

**Radiation resistance**
$$R_\text{rad}=\frac{\langle P_\text{rad} \rangle}{\langle I \rangle ^{2}}$$
where $I$ is the current that powers the source.

**Larmor formula and Liénard generalization**
$$P=\frac{\mu_{0}q^{2}a^{2}}{6\pi c},\qquad P_\text{charge}=\frac{\mu_{0}q^{2}\gamma^{6}}{6\pi c}\left( a^{2}- \left\lvert  \frac{\mathbf{v}\times \mathbf{a}}{c}  \right\rvert ^{2} \right)$$

**Radiation reaction (periodic motion)**
$$\mathbf{F}_\text{rad}=\frac{\mu_{0}q^{2}}{6\pi c}\dot{\mathbf{a}}$$
### Relativity
**Postulates**
1. The laws of physics are the same in all inertial frames of reference.
2. Light moves in the vacuum at a constant speed in all inertial frames of reference, and it is the maximum speed at which energy can propagate.

**Einstein velocity addition rule**
$$v_{AC}=\frac{v_{AB}+v_{BC}}{1+v_{AB}v_{BC}/c^{2}},\qquad u'=\frac{u-v}{1-uv/c^{2}}$$
where A, B and C are three objects (including frames of reference) moving in relation to each other. All of these are absolute values. Alternatively, the second form uses actual signs depending on the direction of motion. They are equivalent.

**Lorentz transformation**
$$\left\{\begin{align}
&x'=\gamma(x-\beta ct) \\
&y'=y \\
&z'=z \\
&t'=\gamma\left( t- \frac{\beta}{c}x \right)
\end{align}\right.,\qquad\gamma\equiv \frac{1}{\sqrt{ 1-\beta ^{2} }},\qquad \beta\equiv\frac{v}{c}$$
$$\bar{x}=\Lambda x,\qquad\Lambda=\begin{pmatrix}\gamma & -\beta \gamma & 0 & 0 \\ -\beta \gamma & \gamma & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1\end{pmatrix},\qquad x=\begin{pmatrix}
x^{0} \\ x^{1} \\ x^{2} \\ x^{3}
\end{pmatrix}$$

**Time dilation and distance contraction**
$$\Delta t_\text{moving}=\gamma\Delta t_\text{rest},\qquad\Delta x_\text{moving} = \frac{\Delta x_\text{rest}}{\gamma}$$

**Proper time, proper velocity**
$$d\tau=\sqrt{ 1- \frac{v^{2}}{c^{2}} }dt=\frac{dt}{\gamma},\qquad\eta^{\mu}=\frac{dx^{\mu}}{d\tau}=(\eta^{0},\boldsymbol{\eta}),\qquad\boldsymbol{\eta}=\gamma \mathbf{v}$$

**Four-momentum, relativistic energy, rest energy, relativistic kinetic energy**
$$p^{\mu}=m\eta^{\mu}=\left(\frac{E}{c},\;\mathbf{p}\right)=(\gamma mc,\gamma m\mathbf{v}),\qquad E=\sqrt{ p^{2}c^{2}+m^{2}c^{4} }=\gamma mc^{2}$$
$$E^{2}=E_{0}^{2}+K^{2},\qquad E_{0}=mc^{2},\qquad K=(\gamma-1)mc^{2}=E-E_{0}$$
$$\gamma=\frac{E}{mc^{2}},\qquad\beta=\frac{pc}{E}$$

**Minkowski force**
$$K^{\mu}\equiv \frac{dp^{\mu}}{d\tau},\qquad\mathbf{K}=\gamma\mathbf{F}$$

**Transformation rules of E and B**
$$\begin{align}
&E'_{x}=E_{x},&E'_{y}&=\gamma(E_{y}-vB_{z}),&E'_{z}&=\gamma(E_{z}+vB_{y}) \\
&B'_{x}=B_{x},&B'_{y}&=\gamma\left( B_{y}+ \frac{v}{c^{2}}E_{z} \right),&B'_{z}&=\gamma\left( B_{z}- \frac{v}{c^{2}}E_{y} \right)
\end{align}$$
If either field is zero in the original frame, their corresponding field in the new frame is
$$\mathbf{E}'=\mathbf{v}\times \mathbf{B}',\quad \mathbf{B}'=- \frac{1}{c^{2}}(\mathbf{v}\times \mathbf{E}')$$

**Field and dual tensors**
$$F^{\mu \nu}\equiv \begin{pmatrix}
0 & E_{x}/c & E_{y}/c & E_{z}/c \\
-E_{x}/c & 0 & B_{z} & -B_{y} \\
-E_{y}/c & -B_{z} & 0 & B_{x} \\
-E_{z}/c & B_{y} & -B_{x} & 0
\end{pmatrix},\qquad G^{\mu \nu}\equiv \begin{pmatrix}
0 & B_{x} & B_{y} & B_{z} \\
-B_{x} & 0 & -E_{z}/c & -E_{y}/c \\
-B_{y} & E_{z}/c & 0 & -E_{x}/c \\
-B_{z} & -E_{y}/c & E_{x}/c & 0
\end{pmatrix}$$
