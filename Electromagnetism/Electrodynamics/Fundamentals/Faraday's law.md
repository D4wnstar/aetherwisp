---
wiki-publish: true
---
**Faraday's law** gives a mathematical quantification of [[Electromagnetic induction]]. It states
$$\nabla\times\mathbf{E}=- \frac{ \partial \mathbf{B} }{ \partial t } $$
so the [[Curl]] of an [[electric field]] depends on the rate of change of a [[magnetic field]]. In the magnetostatic case, where $\frac{ \partial \mathbf{B} }{ \partial t }=0$, this reduces to the well known fact that electrostatic fields have no curl. In integral form (using [[Curl theorem|Stokes' theorem]]) it reads
$$\mathcal{E}=\oint \mathbf{E}\cdot d\mathbf{r}=-\int \frac{ \partial \mathbf{B} }{ \partial t }\cdot d\mathbf{a} $$
where $\mathcal{E}$ is the induced [[Electromotive force|emf]].
### Discovery
The law was derived by Faraday after noticing that keeping a loop still while inside of a moving magnetic field caused an [[electric current]] to flow. On paper, this seems natural, as moving the *loop* while keeping the *field* static would do the same thing. The issue is deeper, though. When the loop is the one moving, the magnetic force sets up the emf that produces the current by way of the [[Lorentz force]], but if the loop is still, there can be no magnetic force as the Lorentz force requires moving [[Electric charge|charges]]. Thus, *something* must have been producing the current and it could not have been the magnetic field.

What Faraday hypothesized was that it's the *changing* of the magnetic field that causes the current, indirectly, by  *inducing* an electric field. For if the emf is equal to the rate of change of the magnetic flux through the loop (a fact experimentally verified by Faraday), we can use the [[Electromotive force|flux rule]] to state
$$\mathcal{E}=\oint \mathbf{E}\cdot d\mathbf{r}=- \frac{\partial \Phi}{\partial t}$$
But the magnetic flux is, of course, related to the magnetic field
$$\Phi=\int \mathbf{B}\cdot d\mathbf{a}$$
which means
$$\oint \mathbf{E}\cdot d\mathbf{r}=-\int \frac{ \partial \mathbf{B} }{ \partial t } \cdot d\mathbf{a}$$
which is Faraday's law in integral form. By application of Stokes' theorem we get
$$\nabla\times\mathbf{E}=-\frac{ \partial \mathbf{B} }{ \partial t } $$
