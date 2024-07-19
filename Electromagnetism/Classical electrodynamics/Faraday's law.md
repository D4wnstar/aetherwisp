**Faraday's law** gives a mathematical quantification of [[electromagnetic induction]]. It states
$$\nabla\times\mathbf{E}=- \frac{ \partial \mathbf{B} }{ \partial t } $$
so the [[curl]] of an [[electric field]] is dependent on the rate of change of a [[magnetic field]]. In the magnetostatic case, where $\frac{ \partial \mathbf{B} }{ \partial t }=0$, this reduces to the well known fact that electrostatic fields have no curl. In integral form (using [[Teorema del rotore|Stokes' theorem]]) it reads
$$\oint \mathbf{E}\cdot d\mathbf{r}=-\int \frac{ \partial \mathbf{B} }{ \partial t }\cdot d\mathbf{a} $$
### Discovery
The law was derived by Faraday after noticing that keeping a loop still inside of a moving magnetic field caused an [[electric current]] to flow. On paper, this seems natural, as moving the *loop* while keeping the *field* static would do the same thing. The issue is deeper, though. When moving the loop, the magnetic force sets up the [[Electromotive force|emf]] that produces the current, but if the loop is still, there can be no magnetic force as by the [[Lorentz force]], magnetic forces occur only for moving [[Electric charge|charges]]. Thus, *something* must be producing the current and it could not be the magnetic field.

What Faraday hypothesized was that it's the *changing* of the magnetic field that causes the current, indirectly, by  *inducing* an electric field. For if the emf is equal to the rate of change of the magnetic flux through the loop (a fact experimentally verified by Faraday), we can use the [[Electromotive force|flux rule]] to state
$$\mathcal{E}=\oint \mathbf{E}\cdot d\mathbf{r}=- \frac{d\Phi}{dt}$$
But the magnetic flux is, of course, related to the magnetic field
$$\Phi=\int \mathbf{B}\cdot d\mathbf{a}$$
which means
$$\oint \mathbf{E}\cdot d\mathbf{r}=-\int \frac{ \partial \mathbf{B} }{ \partial t } \cdot d\mathbf{a}$$
which is Faraday's law in integral form. By application of Stokes' theorem we get
$$\nabla\times\mathbf{E}=-\frac{ \partial \mathbf{B} }{ \partial t } $$
