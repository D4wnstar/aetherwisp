The **electric potential** is a [[potenziale|potential]] function whose derivative is the [[electric field]]. It is defined in integral form as
$$V(\mathbf{r})=-\int_{\mathcal{O}}^{\mathbf{r}}\mathbf{E}\cdot d\mathbf{r}' \qquad [\text{V}]\equiv\left[\frac{\text{J}}{\text{C}}\right]$$
where $\mathbf{r}'$ is the integration variable, not to be confused with the point $\mathbf{r}$ where the potential is calculated, $\mathbf{E}$ is the electric field and $\mathcal{O}$ is a reference point that is arbitrary but must remain consistent for all calculations of $V$. In differential form it reads
$$\mathbf{E}=-\nabla V$$
This is a specific case of the [[Helmholtz theorem]].

The electric potential obeys the superposition principle:
$$V=V_{1}+V_{2}+V_{3}+\ldots$$
This is because the electric field also obeys the principle and the integral is a [[Operatore lineare|linear operator]], so we can integrate term by term.

Notably, the electric potential does *not* measure potential *energy*. There is a connection between potential energy and electric potential, but they are not the same thing despite usually being referred to by the same term.
### Divergence and curl of $\mathbf{E}$
The [[divergence]] of $E$ is readily calculated with respect to $V$:
$$\nabla\cdot \mathbf{E}=\nabla\cdot(-\nabla V)=-\nabla^{2}V$$
using the [[Laplaciano|Laplacian]]. Applying [[Gauss' law]], we get
$$\boxed{\nabla^{2}V=- \frac{\rho}{\varepsilon_{0}}}$$
for a volume [[electric charge|charge]] density $\rho$. This is a specific form of [[Poisson's equation]], where $\psi=V$ and $f=-\rho/\varepsilon_{0}$.

The [[curl]] is also easily calculated:
$$\nabla\times \mathbf{E}=\nabla\times(-\nabla V)=0$$
as the curl of a [[gradient]] is always zero. This confirms that the curl of the electric field is always zero, for any charge distribution. This result is important because it shows that we only need *one* differential equation to determine the electric potential (Poisson's equation), but we need *two* to determine the electric field (divergence and curl).
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
#### Spherical, ball or point charge from $\mathbf{E}$
Consider a point charge $q$ or equivalently a sphere or ball of radius $R$ with total charge $q$. The electric field is
$$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{q}{r^{2}}\hat{\mathbf{r}}$$
(if not using a point charge, assume this is for points outside the sphere). The potential for a point charge or outside a sphere or ball is
$$V(r)=-\int_{\mathcal{O}}^{\mathbf{r}}\mathbf{E}\cdot d\mathbf{r}'=- \frac{1}{4\pi\varepsilon_{0}}\int_{\infty}^{r} \frac{q}{r'^{2}}dr'=\frac{1}{4\pi\varepsilon_{0}} \frac{q}{r}$$
Now let's see how it works inside the sphere (but not the ball). For $r<R$ we must break the integral in two pieces, using in each region the field that prevails there:
$$V(r)=- \underbrace{\frac{1}{4\pi\varepsilon_{0}}\int_{\infty}^{R} \frac{q}{r'^{2}}dr'}\limits_{\text{inside}}-\underbrace{\int_{R}^{r}(0)dr'}\limits_{\text{outside}}=\frac{1}{4\pi\varepsilon_{0}} \left.\frac{q}{r'}\right|_{\infty}^{R}=\frac{1}{4\pi\varepsilon_{0}} \frac{q}{R}$$
Notice how the potential inside the sphere is constant, despite the field being zero. This of course isn't an issue, as the derivative of a constant is zero, so it checks out. This is a particularly important aspect of electric potential: Gauss' law does not apply to it. Unlike a field, which can be "isolated" with good enough symmetry, a potential cannot and is always "vulnerable" to what happens outside a symmetrical shape, like a ball or a cylinder.
#### System of charges or charge density
Knowing the distribution of $n$ discrete charges, we can extend the result on a single point charge by using the superposition principle:
$$V(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\sum\limits_{i=1}^{n} \frac{q_{i}}{\mathfrak{r}_{i}}$$
For a continuous distribution, we can just integrate
$$V(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int \frac{1}{\mathfrak{r}}dq$$
For a volume distribution $\rho$ we have
$$\boxed{V(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int\frac{\rho(\mathbf{r}')}{\mathfrak{r}}d\tau'}$$
This is the general equation that can be used to derive the potential field of an arbitrary charge distribution, assuming the point of reference is at infinity. Compared to the electric field formula for $\rho$, it is only dependent on $1/\mathfrak{r}$ instead of $1/\mathfrak{r}^{2}$ and, most importantly, does not include $\hat{\mathfrak{r}}$. Of course, equivalent equations for [[curva|linear]] and [[superficie|surface]] charge densities exist.
### Discontinuities
The potential is continuous over boundaries. In fact, since it's defined by a path integral, we can shrink the path going through the surface to be arbitrarily small, thereby making the integral also arbitrarily small. Thus
$$V_\text{above}-V_\text{below}=-\int_{\gamma}\mathbf{E}\cdot d\mathbf{r} \underset{ \gamma \to 0 }{ \to } 0 \quad \Rightarrow \quad V_\text{above}=V_\text{below}$$
The gradient, however, inherits the electric field's discontinuity:
$$\nabla V_\text{above}-\nabla V_\text{below}=- \frac{1}{\varepsilon_{0}}\sigma \hat{\mathbf{n}}$$
or
$$\frac{ \partial V_\text{above} }{ \partial n } - \frac{ \partial V_\text{below} }{ \partial n }=- \frac{1}{\varepsilon_{0}}\sigma $$
where
$$\frac{ \partial V }{ \partial n } =\nabla V\cdot \hat{\mathbf{n}}$$
This is called the *normal derivative* and represents the rate of change with respect to the normal of the surface.
### Relation to work
The minimum work required to move a charge from point $\mathbf{a}$ to point $\mathbf{b}$ is
$$W=\int_{\mathbf{a}}^{\mathbf{b}}\mathbf{F}\cdot d\mathbf{r}=-Q\int_{\mathbf{a}}^{\mathbf{b}}\mathbf{E}\cdot d\mathbf{r}=Q[V(\mathbf{b})-V(\mathbf{a})]$$
where the minus sign comes from the fact that the force exerted to move the charge is opposite to the one generated by the electric field. Dividing both sides by $Q$ we have
$$\Delta V=\frac{W}{Q}$$
so the difference in potential between two points is equal to the amount of work per unit charge required to move the charge. A nice example is the amount of work needed to bring in a charge from very far away ($\infty$):
$$W=Q[V(\mathbf{r})-V(\infty)]=QV(\mathbf{r})$$
In this sense, the electric potential is energy per unit charge.
### Energy of a system
Since electric potential is related to energy, we can use it to measure the energy stored in a system. The energy required to move a point charge $q_{2}$ from infinity to a near another point charge $q_{1}$ is
$$W_{2}=\frac{1}{4\pi \varepsilon_{0}}q_{2}\left( \frac{q_{1}}{\mathfrak{r}_{12}} \right)$$
where $\mathfrak{r}_{12}$ is the distance between the charges after being moved. The charges are assumed to be static, so they never budge after being moved to their respective locations. Adding another charge $q_{3}$ will take
$$W_{3}=\frac{1}{4\pi \varepsilon_{0}}q_{3}\left( \frac{q_{1}}{\mathfrak{r}_{13}}+ \frac{q_{2}}{\mathfrak{r}_{23}} \right)$$
and a fourth charge $q_{4}$ will take
$$W_{4}=\frac{1}{4\pi \varepsilon_{0}}q_{4}\left( \frac{q_{1}}{\mathfrak{r}_{14}}+ \frac{q_{2}}{\mathfrak{r}_{24}}+ \frac{q_{3}}{\mathfrak{r}_{34}} \right)$$
and therefore the total work will be
$$W=W_{2}+W_{3}+W_{4}=\frac{1}{4\pi \varepsilon_{0}}\left(\frac{q_{1}q_{2}}{\mathfrak{r}_{12}}+ \frac{q_{1}q_{3}}{\mathfrak{r}_{13}}+ \frac{q_{1}q_{4}}{\mathfrak{r}_{14}}+ \frac{q_{2}q_{3}}{\mathfrak{r}_{23}}+ \frac{q_{2}q_{4}}{\mathfrak{r}_{24}}+ \frac{q_{3}q_{4}}{\mathfrak{r}_{34}} \right)$$
The general rule here is that each charge interacts with all the previous ones:
$$W=\frac{1}{4\pi \varepsilon_{0}}\sum_{i=1}^{N} \sum_{j>i}^{N} \frac{q_{i}q_{j}}{\mathfrak{r}_{ij}}$$
where $j>i$ is to avoid counting each pair twice. Alternatively, we can count each pair twice and divide everything by two:
$$W=\frac{1}{8\pi \varepsilon_{0}}\sum_{i=1}^{N} \sum_{j\neq i}^{N} \frac{q_{i}q_{j}}{\mathfrak{r}_{ij}}$$
(we still need to avoid a charge interacting with itself, so $j\neq i$ is still necessary). This form is pleasant because it is independent on order of assembly of the charges.

If we extract $q_{i}$ from the second sum, we can see that what we are left with is just the potential caused by $q_{j}$ and thus
$$\boxed{W=\frac{1}{8\pi \varepsilon_{0}}\sum_{i=1}^{N} q_{i}V(\mathbf{r}_{i})}$$
For volume charges, we can just substitute the sum with an integral over the space of the distribution[^1]:
$$\boxed{W=\frac{1}{2}\int _\text{distr.} \rho V\ d\tau}$$
with corresponding integrals for surface and line distributions. We can also rewrite this in terms of the electric field only. Using Gauss' law as $\rho=\varepsilon_{0}\nabla\cdot\mathbf{E}$, we have
$$W=\frac{\varepsilon_{0}}{2}\int(\nabla\cdot\mathbf{E})V\ d\tau$$
Using [[Integrazione per parti|integration by parts]] we have
$$W=\frac{\varepsilon_{0}}{2}\left[ -\int \mathbf{E}\cdot(\nabla V)\ d\tau + \oint V\mathbf{E}\cdot d\mathbf{a} \right]=\frac{\varepsilon_{0}}{2}\left( \int_{V}E^{2}\ d\tau+\oint_{S}V\mathbf{E}\cdot d\mathbf{a} \right)$$
This volume $V$ that we are integrating over is technically the charge distribution from before, but since $\rho$ is zero outside of the distribution, any volume larger than it will not contribute to the integral. This permits us to choose as arbitrarily large volume, provided it contains the whole charge. Of course, $\int_{V}E^{2}d\tau$ will *increase* with a bigger $V$, but the surface integral *decreases* with a bigger $V$, so they cancel each other out. In fact, $E\propto 1/r^{2}$ and $V\propto 1/r$ at large enough distances and $a\propto r^{2}$, so the whole integral goes like $\sim 1/r$ in total. Since the volume is arbitrary provided it contains the whole charge, we might as well pick all space. In this case, the surface integral vanishes and the field integral contains all the work:
$$\boxed{W=\frac{\varepsilon_{0}}{2}\int _\text{all space} E^{2}\ d\tau}$$
These two integrals are completely equivalent, provided the domain of integration is chosen appropriately. The value of this integral is that it clearly shows that system energy is quadratic and therefore non-linear, so it cannot simply be summed. If the charge is doubled everywhere, then the energy quadruples instead.

[^1]: Actually, there's another change happening here. For any charge, the sum only considers other charges ($j\neq i$), whereas the integral considers everything including the infinitesimal charge element itself. This is fine because $dq$ alone has no impact, as it is infinitesimal. However, if one were to try and calculate the work for point charges using this integral, they would get infinite energy, as the distribution of energy of a charge is discontinuous. The technical reason for the discrepancy is the considering the charge itself in the summation/integral is equivalent to considering the energy necessary to *create* the charge too, not just to move it. Since we can't create or destroy charges, this amount is irrelevant and mostly just leads to headaches. This is also why the integral is always positive (at least in electric field form), but the summation may be negative.