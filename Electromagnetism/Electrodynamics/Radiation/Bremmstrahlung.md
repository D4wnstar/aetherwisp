---
wiki-publish: true
---
**Bremmstrahlung** or **braking radiation** is the [[electromagnetic radiation]] emitted by a [[Electric charge|point charge]] due to deceleration (or acceleration) in the direction of its velocity. The angular [[radiant power]] distribution is
$$\frac{dP}{d\Omega}=\frac{\mu_{0}q^{2}a^{2}}{16\pi ^{2}c} \frac{\sin ^{2}\theta}{(1-\beta \cos \theta)^{5}}$$
and the total radiant power emitted is
$$P=\frac{\mu_{0}q^{2}a^{2}\gamma^{6}}{6\pi c}$$
where $\gamma=(1-\beta ^{2})^{-1/2}$ is the usual [[Lorentz transformation|relativistic]] coefficient.
### Derivation
Consider a point charge moving in the same direction it is accelerating in, such that $\mathbf{v}$ and $\mathbf{a}$ are collinear at some [[retarded time]] $t_{r}$. We care about the angular distribution of the [[radiant power]] emitted, so use the [[Larmor formula]] in the Liénard generalization, specifically its [[solid angle]]
$$\frac{dP}{d\Omega}=\frac{q^{2}}{16\pi ^{2}\varepsilon_{0}} \frac{\lvert \hat{\boldsymbol{\mathfrak{r}}}\times(\mathbf{u}\times \mathbf{a}) \rvert ^{2}}{(\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{u})^{5}}$$
Since $\mathbf{u}=c \hat{\boldsymbol{\mathfrak{r}}}-\mathbf{v}$ and $\mathbf{v}$ is collinear with $\mathbf{a}$, we get $\mathbf{u}\times \mathbf{a}=c(\hat{\boldsymbol{\mathfrak{r}}}\times \mathbf{a})-\cancel{ \mathbf{v}\times \mathbf{a} }$. Also $\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{u}=c-\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{v}$. Thus
$$\frac{dP}{d\Omega}=\frac{q^{2}}{16\pi ^{2}\varepsilon_{0}} \frac{\lvert \hat{\boldsymbol{\mathfrak{r}}}\times(\hat{\boldsymbol{\mathfrak{r}}}\times \mathbf{a}) \rvert ^{2}}{(c-\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{v})^{5}}$$
The triple product expands to
$$\hat{\boldsymbol{\mathfrak{r}}}\times(\hat{\boldsymbol{\mathfrak{r}}}\times \mathbf{a})=(\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{a})\hat{\boldsymbol{\mathfrak{r}}}-\mathbf{a}\quad\Rightarrow \quad \lvert \hat{\boldsymbol{\mathfrak{r}}}\times(\hat{\boldsymbol{\mathfrak{r}}}\times \mathbf{a}) \rvert^{2}=a^{2}-(\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{a})^{2} $$
If we set the [[frame of reference]] such that $\mathbf{v}$ is on the $x$ axis, then
$$\frac{dP}{d\Omega}=\frac{\mu_{0}q^{2}a^{2}}{16\pi ^{2}c} \frac{\sin ^{2}\theta}{(1-\beta \cos \theta)^{5}}$$
where $\beta\equiv v/c$ is the usual relativistic coefficient. Now, when $\beta \simeq 0$, the whole denominator below the sine goes away and we get the typical [[torus]]-shaped radiation emission. However, when $\beta$ is large, the quintic term at the denominator distorts the torus so that looks something like this:

![[Diagram Bremmstrahlung angular distribution|80%]]

The squished blue shapes are the directions in which radiation is strongest. While there is still no radiation in the $\mathbf{v}$ direction, most of it is being emitted forwards. Notice how, due to the square of $a$, the radiation distribution does not care about whether the charge is accelerating or decelerating. Either way, it gets emitted in the direction of the velocity. This kind of radiation is known as **bremmstrahlung**, or **braking radiation** since it is typically encountered when charges brake due to the presence of external fields.

The total power emitted is
$$P=\int_{\mathcal{S}} \frac{dP}{d\Omega}d\Omega=\frac{\mu_{0}q^{2}a^{2}}{16\pi ^{2}c}\int_{\mathcal{S}} \frac{\sin ^{2}\theta}{(1-\beta \cos \theta)^{5}}\sin \theta d\theta d\phi$$
over a [[sphere]] $\mathcal{S}$ that contains the charge. The $\phi$ integral is trivial since there is no $\phi$ dependency and makes $2\pi$. The $\theta$ is solved with the substitution $x\equiv \cos \theta$:
$$P=\frac{\mu_{0}q^{2}a^{2}}{8\pi c}\int_{-1}^{1} \frac{1-x^{2}}{(1-\beta x)^{5}}dx$$
We then [[integration by parts|integrate by parts]] on numerator and denominator, which results in $\frac{4}{3}(1-\beta ^{2})^{-3}$, and so
$$P=\frac{\mu_{0}q^{2}a^{2}\gamma^{6}}{6\pi c}$$
### In detectors
For an [[electron]], the [[particle]] process of bremmstrahlung due to some [[atomic nucleus]] $^{A}_{Z}X$ is
$$e^{-}+\ _{Z}^{A}X \rightarrow e^{-}+\gamma+\ _{Z}^{A}X$$
It consists of the emission of a [[photon]] with no change on the electron or the nucleus. The effects are largely kinematic and cause the deflection of the electron. This is useful in [[detector]] physics, where bremmstrahlung is the primary cause of energy loss for light particles traversing matter (also see [[Stopping power]]).