---
wiki-publish: true
---
### Preparatory topics
**Poynting's theorem**
$$P=\frac{ \partial U }{ \partial t } =-\frac{ \partial  }{ \partial t } \int_{\mathcal{V}}u(\mathbf{r})\ d\tau-\oint_{\mathcal{S}}\mathbf{S}\cdot d\mathbf{a};\qquad-\frac{ \partial u(\mathbf{r}) }{ \partial t }=\mathbf{E}\cdot \mathbf{J} -\nabla\cdot\mathbf{S}$$

**Poynting vector**
$$\mathbf{S}\equiv \frac{1}{\mu_{0}}\mathbf{E}\times \mathbf{B}$$

**Electromagnetic energy density**
$$u=\frac{1}{2}\left( \varepsilon_{0}E^{2}+ \frac{1}{\mu_{0}}B^{2} \right)$$

**Momentum density**
$$\mathbf{g}=\varepsilon_{0}\mu_{0}\mathbf{S}=\varepsilon_{0}(\mathbf{E}\times \mathbf{B})=\frac{1}{c^{2}}\mathbf{S}$$

**Angular momentum density**
$$\boldsymbol{\ell}=\mathbf{r}\times \mathbf{g}=\varepsilon_{0}[\mathbf{r}\times(\mathbf{E}\times \mathbf{B})]$$

**Maxwell stress tensor**
$$T_{ij}=\varepsilon_{0}\left( E_{i}E_{j}- \frac{1}{2}\delta_{ij}E^{2} \right)+ \frac{1}{\mu_{0}}\left( B_{i}B_{j}- \frac{1}{2}\delta_{ij}B^{2} \right)$$

**Lorentz force and force density (tensor form)**
$$\mathbf{F}=\oint_{\mathcal{S}}\mathrm{T}\cdot d\mathbf{a}-\varepsilon_{0}\mu_{0}\frac{d}{dt} \int_{\mathcal{V}}\mathbf{S}\ d\tau,\qquad\mathbf{f}=\nabla\cdot \mathrm{T}-\varepsilon_{0} \mu_{0} \frac{ \partial \mathbf{S} }{ \partial t } $$
### Electromagnetic waves
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
Multiply by $2$ for non-averages.

**Radiation pressure**
$$P=\frac{1}{A} \frac{\Delta \lvert \mathbf{p} \rvert }{\Delta t}=\frac{\varepsilon_{0}}{2}E_{0}^{2}=\frac{I}{c}$$

**Irradiances (normal incidence)**
$$I_{I}=\frac{\varepsilon c}{2n_{1}}E_{0,I}^{2},\qquad I_{R}=\frac{\varepsilon c}{2n_{1}}E_{0,R}^{2},\qquad I_{T}=\frac{\varepsilon c}{2n_{2}}E_{0,T}^{2}$$

**Reflection and transmission coefficients (normal incidence + nonmagnetic material)**
$$R\equiv \frac{I_{R}}{I_{I}}=\left( \frac{E_{0,R}}{E_{0,I}} \right)^{2}=\left( \frac{n_{1}-n_{2}}{n_{1}+n_{2}} \right)^{2},\qquad T\equiv \frac{I_{T}}{I_{I}}=\frac{\varepsilon_{2}n_{1}}{\varepsilon_{1}n_{2}}\left( \frac{E_{0,T}}{E_{0,I}} \right)^{2}=\frac{4n_{1}n_{2}}{(n_{1}+n_{2})^{2}}$$

**Irradiances (oblique incidence)**
$$I_{I}=\langle \mathbf{S} \rangle\cdot \hat{\mathbf{x}}=\frac{\varepsilon_{1}c}{2n_{1}}E_{0,I}^{2}\cos \theta_{I},\qquad I_{R}=\frac{\varepsilon_{1}c}{2n_{1}}E_{0,I}^{2}\cos \theta_{R},\qquad I_{R}=\frac{\varepsilon_{2}c}{2n_{2}}E_{0,I}^{2}\cos \theta_{T}$$
Normal incidence when $\theta_{I}=\theta_{R}=0$.

**Reflection and transmission coefficients (oblique incidence)**
$$R=\frac{I_{R}}{I_{I}}=\left( \frac{\alpha-\beta}{\alpha+\beta} \right)^{2},\qquad T=\frac{I_{T}}{I_{I}}=\alpha \beta\left( \frac{2}{\alpha+\beta} \right)^{2}$$
Normal incidence when $\alpha=1$.

- Fields superimpose due to Maxwell equations linearity. Irradiance/intensity does not.