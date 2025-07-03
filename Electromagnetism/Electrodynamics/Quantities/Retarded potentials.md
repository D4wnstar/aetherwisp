---
wiki-publish: true
---
**Retarded potentials** are general forms of the [[electric potential]] and [[magnetic vector potential]] in terms of the [[retarded time]]
$$V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}}\int \frac{\rho(\mathbf{r}',t_{r})}{\mathfrak{r}} \ d\tau',\qquad \mathbf{A}(\mathbf{r},t)=\frac{\mu_{0}}{4\pi}\int \frac{\mathbf{J}(\mathbf{r}',t_{r})}{\mathfrak{r}} \ d\tau'  $$
These are necessary when the [[electric charge]] and [[electric current]] distributions change in time in order to preserve [[causality]].
### Derivation
In the [[Lorenz gauge]], [[Maxwell's equations]] for potential read
$$\square ^{2}V=- \frac{\rho}{\varepsilon_{0}},\qquad\square ^{2}\mathbf{A}=-\mu_{0}\mathbf{J}\tag{1}$$
These reduce to
$$\nabla^{2}V=- \frac{\rho}{\varepsilon_{0}},\qquad\nabla^{2}\mathbf{A}=-\mu_{0}\mathbf{J}$$
in the static case, where the solutions are
$$V(\mathbf{r})=\frac{1}{4\pi \varepsilon_{0}}\int_{\mathcal{V}} \frac{\rho(\mathbf{r}')}{\mathfrak{r}} \ d\tau',\qquad \mathbf{A}(\mathbf{r})=\frac{\mu_{0}}{4\pi}\int_{\mathcal{V}} \frac{\mathbf{J}(\mathbf{r}')}{\mathfrak{r}} \ d\tau'  $$
In the dynamic case, we must consider the change in time, which is to say the propagation of the fields. This occurs at the [[speed of light]] $c$, which means that the potential that an object feels from an object a distance $\mathfrak{r}$ away is not due to the potentials right *now*, but to the potentials when they were emitted at some time *in the past*. This time is right now minus the time it took for the potential to travel to its destination at light speed, called the **retarded time**:
$$t_{r}\equiv t- \frac{\mathfrak{r}}{c}$$
The potentials then naturally generalize to
$$\boxed{V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}}\int_{\mathcal{V}} \frac{\rho(\mathbf{r}',t_{r})}{\mathfrak{r}} \ d\tau',\qquad \mathbf{A}(\mathbf{r},t)=\frac{\mu_{0}}{4\pi}\int_{\mathcal{V}} \frac{\mathbf{J}(\mathbf{r}',t_{r})}{\mathfrak{r}} \ d\tau'  }$$
To prove that this heuristic logic is valid, we must check that it satisfies the Maxwell's equations $(1)$, which means that we need the [[Laplacian]] of $V$ and $\mathbf{A}$ and their second time derivative. Let's start from the [[gradient]] of $V$. We need to take derivatives in space. Notice how $V$ depends on space not just in $\mathfrak{r}=\lvert \mathbf{r}'-\mathbf{r} \rvert$ at the denominator, but also implicitly in $t_{r}\propto \mathfrak{r}$ at the numerator inside of $\rho$. As such
$$\nabla V=\frac{1}{4\pi \varepsilon_{0}}\int_{\mathcal{V}}\left[ \frac{\nabla \rho}{\mathfrak{r}} + \rho \nabla\left( \frac{1}{\mathfrak{r}} \right) \right]d\tau'$$
Separately, we get
$$\nabla \rho=\dot{\rho}\nabla t_{r}=- \frac{1}{c}\dot{\rho}\nabla \mathfrak{r}=- \frac{1}{c}\dot{\rho}\hat{\boldsymbol{\mathfrak{r}}}$$
since $\nabla \mathfrak{r}=\hat{\boldsymbol{\mathfrak{r}}}$ and using dot notation for time derivatives. Now, we know from electrostatics that $\nabla(1/\mathfrak{r})=-\hat{\boldsymbol{\mathfrak{r}}}/\mathfrak{r}^{2}$, so
$$\nabla V=\frac{1}{4\pi \varepsilon_{0}}\int_{\mathcal{V}}\left[ - \frac{\dot{\rho}}{c} \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}}-\rho \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}} \right]d\tau'$$
Taking the [[divergence]] to obtain the Laplacian
$$\nabla ^{2}V=\frac{1}{4\pi \varepsilon_{0}}\int_{\mathcal{V}}\left[ - \frac{\dot{\rho}}{c}\nabla\cdot\left( \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}} \right)- \frac{1}{c}\frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}}\cdot(\nabla \dot{\rho}) \right]- \left[ \frac{\hat{\boldsymbol{\mathfrak{r}}}}{r}\cdot(\nabla \rho)+\rho \nabla\cdot\left( \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}} \right) \right]d\tau'$$
Notice that
$$\nabla \dot{\rho}=- \frac{1}{c}\ddot{\rho}\nabla \mathfrak{r}=- \frac{1}{c}\ddot{\rho}\hat{\boldsymbol{\mathfrak{r}}},\qquad \nabla\left( \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}} \right)=4\pi \delta^{3}(\boldsymbol{\mathfrak{r}})$$
and we already know the other two gradients, so
$$\nabla ^{2}V=\frac{1}{4\pi \varepsilon_{0}}\int_{\mathcal{V}}\left[ \frac{1}{c^{2}}\frac{\ddot{\rho}}{\mathfrak{r}}-4\pi \rho \delta^{3}(\mathfrak{\mathbf{r}}) \right]d\tau'=\frac{1}{c^{2}}\frac{ \partial^{2} V }{ \partial t^{2} }- \frac{1}{\varepsilon_{0}}\rho(\mathbf{r},t)$$
or
$$\square ^{2}V=- \frac{\rho(\mathbf{r},t)}{\varepsilon_{0}}$$
which confirms that the retarded electric potential does in fact satisfy the potential wave equation. An analogous process also proves that the retarded vector potential satisfies $(1)$.

You can rerun this method again to prove that it also applies just as well to the **advanced time** $t_{a}\equiv t+ \mathfrak{r}/c$ and the associated **advanced potentials** (same equations, just with $t_{a}$ instead of $t_{r}$). This is a curious and rather absurd result; think about it for a moment. The retarded time is necessary to keep the speed of light into account. A signal, even one moving at the speed of light, takes time to arrive to destination. This extra time is $\mathfrak{r}/c$ of course, which we *remove* to go back into the past when the signal was created... but if we *add* it, we go forward into the future when... the signal will be created? Which implies that *technically* the potential we feel *now* may also be due to a signal that has not even been *created* yet. This is obvious witchcraft and it flagrantly violates **causality**, the principle that cause must precede effect, but it's not the math that proves it wrong, we can only *say* that is wrong because the theory has no problem allowing it. This is a property known as **[[time-reversal]] [[symmetry]]**, the fact that a theory does not change if you invert the time coordinate (you set $t$ to $-t$). Time-reversal *asymmetry* is introduce into electrodynamic theory right here, completely artificially, by arbitrarily choosing that advanced potentials are invalid choices. The choice is driven not by mathematical proof, but by overwhelming empirical evidence of it.