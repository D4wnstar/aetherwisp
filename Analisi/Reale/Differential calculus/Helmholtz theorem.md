The **Helmholtz theorem** provides the necessary conditions for existence and uniqueness of a vector function $\mathbf{F}$ for a given [[Divergence]] $\nabla\cdot\mathbf{F}=D$ and [[Curl]] $\nabla\times\mathbf{F}=\mathbf{C}$.

> [!info] Helmholtz theorem
> If both the divergence $D$ and curl $\mathbf{C}$ of a vector field $\mathbf{F}$ are specified, if both go to zero faster than $1/r^{2}$ at $r \rightarrow \infty$ and if $\mathbf{F}(\mathbf{r})$ goes to zero as $r \rightarrow \infty$, then $\mathbf{F}$ is uniquely given by
> $$\mathbf{F}=-\nabla U+\nabla\times\mathbf{W}$$
> where
> $$U(\mathbf{r})=\frac{1}{4\pi}\int \frac{D(\mathbf{r}')}{|\mathbf{r}-\mathbf{r}'|}d\tau'$$
> and
> $$\mathbf{W}(\mathbf{r})=\frac{1}{4\pi}\int \frac{\mathbf{C}(\mathbf{r}')}{|\mathbf{r}-\mathbf{r}'|}d\tau'$$

### Proof
Consider a vector field $\mathbf{F}(\mathbf{r})$ whose divergence and curl are
$$\nabla\cdot\mathbf{F}=D, \quad \nabla\times\mathbf{F}=\mathbf{C}\tag{1}$$
The curl must be divergenceless as the divergence of a curl is always zero:
$$\nabla\cdot\mathbf{C}=0$$

Let's assume that the function $\mathbf{F}$ is of the form
$$\mathbf{F}=-\nabla U+\nabla\times\mathbf{W}$$
where
$$U(\mathbf{r})\equiv\frac{1}{4\pi}\int _\text{all space} \frac{D(\mathbf{r}')}{\mathfrak{r}}d\tau'$$
and
$$\mathbf{W}(\mathbf{r})\equiv\frac{1}{4\pi}\int _\text{all space} \frac{\mathbf{C}(\mathbf{r}')}{\mathfrak{r}}d\tau'$$
where $\mathfrak{r} = \lvert \mathbf{r}-\mathbf{r}' \rvert$. For this (and therefore the theorem) to be true, both the divergence and curl of $\mathbf{F}$ must be $(1)$.

Let's check the divergence:
$$\nabla\cdot\mathbf{F}=-\nabla^{2}U=-\frac{1}{4\pi}\int D\nabla^{2}\left( \frac{1}{\mathfrak{r}} \right)d\tau'=\int D(\mathbf{r}')\delta^{3}(\mathbf{r}-\mathbf{r}')d\tau'=D(\mathbf{r})$$
where we used $\nabla^{2}\left( 1/\mathfrak{r} \right)=-4\pi \delta^{3}(\mathfrak{r})$. This is the correct result.

Let's check the curl:
$$\nabla\times\mathbf{F}=\nabla\times\mathbf{(\nabla\times\mathbf{W})}=-\nabla^{2}\mathbf{W}+\nabla(\nabla\cdot\mathbf{W})$$
where we used that the curl of [[Gradient]] is zero. Now the first term is
$$-\nabla^{2}\mathbf{W}=-\frac{1}{4\pi}\int \mathbf{C}\nabla^{2}\left( \frac{1}{\mathfrak{r}} \right)d\tau'=\int \mathbf{C}(\mathbf{r}')\delta^{3}(\mathbf{r}-\mathbf{r}')d\tau'=\mathbf{C}(\mathbf{r})$$
This is what we expect. For the whole equation to be true, then we must have $\nabla(\nabla\cdot\mathbf{W})=0$:
$$4\pi \nabla \cdot\mathbf{W}=\int \mathbf{C}\cdot \nabla\left( \frac{1}{\mathfrak{r}} \right)d\tau'=-\int \mathbf{C}\cdot \nabla'\left( \frac{1}{\mathfrak{r}} \right)d\tau'=\ldots$$
this is because derivatives of $\mathfrak{r}$ change only by a sign between primed and unprimed coordinates. We continue by using [[Integrazione per parti|integration by parts]] as
$$\ldots=\int \frac{1}{\mathfrak{r}}\nabla'\cdot \mathbf{C} \, d\tau'-\oint \frac{1}{\mathfrak{r}}\mathbf{C}\cdot d\mathbf{a} $$
The divergence of $\mathbf{C}$ is zero by definition, so all we need is for the second integral to also vanish. This happens if $\mathbf{ C}$ goes to zero sufficiently rapidly.

The condition of $\mathbf{C}$ comes naturally when we look at the conditions it needs to fulfill for its integral to even exist. At large $r'$, where $\mathfrak{r}\simeq r'$, the integrals in $D$ and $\mathbf{C}$ have the form
$$\int ^{\infty} \frac{X(r')}{r'}r'^{2}dr'=\int ^{\infty}r'X(r')dr'$$
where $X$ is either $D$ or $\mathbf{C}$. For these to exist, $X(r')$ must go to zero at large $r'$. If $X\propto 1/r$, then the integrand is a constant and diverges. If $X\propto 1/r^{2}$, the integral becomes a logarithm and still diverges. This means that $X$ must go to zero at least faster than $1/r^{2}$. This automatically makes the previous integral go to zero too, so the condition of $\nabla\times\mathbf{F}=\mathbf{C}$ is also satisfied. Since $(1)$ is proven, then the theorem is true.
### Corollary
The Helmholtz theorem has a useful corollary:

> [!info] Corollary
> Any differentiable vector function $\mathbf{F}(\mathbf{r})$ that goes to zero faster than $1/r$ as $r \to \infty$ can be expressed as the gradient of a scalar plus the curl of a vector as
> $$\mathbf{F}(\mathbf{r})=\nabla\left( - \frac{1}{4\pi}\int \frac{\nabla'\cdot \mathbf{F}(\mathbf{r})}{\mathfrak{r}}\ d\tau'  \right)+\nabla\times\left( \frac{1}{4\pi} \int\frac{\nabla'\times \mathbf{F}(\mathbf{r}')}{\mathfrak{r}}\ d\tau' \right)$$

 This applies, for instance, to the [[electric field]]:
$$\mathbf{E}(\mathbf{r})=-\nabla\left( \frac{1}{4\pi \varepsilon_{0}}\int \frac{\rho(\mathbf{r}')}{\mathfrak{r}}d\tau' \right)=-\nabla V$$
and also the [[magnetic field]]:
$$\mathbf{B}(\mathbf{r})=\nabla\times\left( \frac{\mu_{0}}{4\pi} \int \frac{\mathbf{J}(\mathbf{r}')}{\mathfrak{r}}d\tau' \right)=\nabla\times\mathbf{A}$$
