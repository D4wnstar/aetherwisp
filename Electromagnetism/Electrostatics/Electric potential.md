The **electric potential** is a [[potenziale|potential]] function whose derivative is the [[electric field]]. It is defined in integral form as
$$V(\mathbf{r})=-\int_{\mathcal{O}}^{\mathbf{r}}\mathbf{E}\cdot d\mathbf{r}' \qquad [\text{V}]\equiv\left[\frac{\text{J}}{\text{C}}\right]$$
where $\mathbf{r}'$ is the integration variable, not to be confused with the point $\mathbf{r}$ where the potential is calculated, $\mathbf{E}$ is the electric field and $\mathcal{O}$ is a reference point that is arbitrary but must remain consistent for all calculations of $V$. In differential form it reads
$$\mathbf{E}=-\nabla V$$

The electric potential obeys the superposition principle:
$$V=V_{1}+V_{2}+V_{3}+\ldots$$
This is because the electric field also obeys the principle and the integral is a [[Operatore lineare|linear operator]], so we can integrate term by term.

Notably, the electric potential does *not* measure potential *energy*. There is a connection between potential energy and electric potential, but they are not the same thing despite usually being referred to by the same term.
### Choice of reference point
As with all potentials, it is defined up to a constant and therefore carries no real physical significance. In this specific definition, the constant change is equivalent to a change in the reference point $\mathcal{O}$. $\mathcal{O}$ is conventionally set at infinity, as the electric potential commonly goes like $\sim1/r$ and therefore vanishes at infinity like $V(\mathcal{O})=V(\infty)=0$.

This becomes false in case the charge distribution goes to infinity, such as when using an infinite wire or plane. In these cases, the potential explodes to infinity at infinity. Of course, this is a very theoretical problem as there is no such thing as an infinite charge distribution, but many approximation suffer from this problem. The solution is simply to pick a different $\mathcal{O}$, ideally one where $V(\mathcal{O})=0$.
### Derivation of differential form
The differential form is found by calculating the potential difference between two points is
$$V(\mathbf{b})-V(\mathbf{a})=-\int_{\mathcal{O}}^{\mathbf{b}}\mathbf{E}\cdot d\mathbf{r}'+\int_{\mathcal{O}}^{\mathbf{a}}\mathbf{E}\cdot d\mathbf{r}'=-\int_{\mathbf{a}}^{\mathbf{b}}\mathbf{E}\cdot d\mathbf{r}'$$
Using the [[teorema del gradiente|gradient theorem]] we have
$$V(\mathbf{b})-V(\mathbf{a})=\int_{\mathbf{a}}^{\mathbf{b}}(\nabla V)\cdot d\mathbf{r}'$$
Therefore
$$\int_{\mathbf{a}}^{\mathbf{b}}(\nabla V)\cdot d\mathbf{r}'=-\int_{\mathbf{a}}^{\mathbf{b}}\mathbf{E}\cdot d\mathbf{r}'$$
We put no restrictions of what points $\mathbf{a}$ and $\mathbf{b}$ could be, so this is true for any two points. We can therefore equate the integrands and get
$$\boxed{\mathbf{E}=-\nabla V}$$
### Notable cases
#### Spherical, ball or point charge
Consider a point charge $q$ or equivalently a sphere or ball of radius $R$ with total charge $q$. The electric field is
$$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{q}{r^{2}}\hat{\mathbf{r}}$$
(if not using a point charge, assume this is for points outside the sphere). The potential for a point charge or outside a sphere or ball is
$$V(r)=-\int_{\mathcal{O}}^{\mathbf{r}}\mathbf{E}\cdot d\mathbf{r}'=- \frac{1}{4\pi\varepsilon_{0}}\int_{\infty}^{r} \frac{q}{r'^{2}}dr'=\frac{1}{4\pi\varepsilon_{0}} \frac{q}{r}$$
Now let's see how it works inside the sphere (but not the ball). For $r<R$ we must break the integral in two pieces, using in each region the field that prevails there:
$$V(r)=- \underbrace{\frac{1}{4\pi\varepsilon_{0}}\int_{\infty}^{R} \frac{q}{r'^{2}}dr'}\limits_{\text{inside}}-\underbrace{\int_{R}^{r}(0)dr'}\limits_{\text{outside}}=\frac{1}{4\pi\varepsilon_{0}} \left.\frac{q}{r'}\right|_{\infty}^{R}=\frac{1}{4\pi\varepsilon_{0}} \frac{q}{R}$$
Notice how the potential inside the sphere is constant, despite the field being zero. This of course isn't an issue, as the derivative of a constant is zero, so it checks out. This is a particularly important aspect of electric potential: [[Gauss' law]] does not apply to it. Unlike a field, which can be "isolated" with good enough symmetry, as potential cannot and is always "vulnerable" to what happens outside a symmetrical shape, like a ball or a cylinder.