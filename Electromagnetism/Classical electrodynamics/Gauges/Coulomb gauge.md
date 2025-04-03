The **Coulomb gauge** is an electrodynamic [[gauge]] for [[Maxwell's equations]] in which we set the [[divergence]] of the [[magnetic vector potential]] to zero:
$$\nabla\cdot \mathbf{A}=0$$
In this gauge, the [[electric potential]] becomes the well known [[Gauss' law]]:
$$\nabla ^{2}V=- \frac{\rho}{\varepsilon_{0}}$$
The upside of this gauge is that $V$ is relatively easy to calculate, since it is given by [[Poisson's equation]] and that is a very well known and very well studied equation. The downside is that $\mathbf{A}$ is a nightmare to calculate. The general solution to Maxwell's equation to this gauge is
$$V=(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}}\int_{\mathcal{V}} \frac{\rho(\mathbf{r}',t)}{\mathfrak{r}}d\tau'$$
for $V$ and
$$\nabla ^{2}\mathbf{A}-\mu_{0}\varepsilon_{0}\frac{ \partial ^{2}\mathbf{A} }{ \partial t^{2} } =-\mu_{0}\mathbf{J}+\mu_{0}\varepsilon_{0}\nabla\left( \frac{ \partial V }{ \partial t }  \right)$$
for $\mathbf{A}$, which is a second order differential equation that has no general solution.