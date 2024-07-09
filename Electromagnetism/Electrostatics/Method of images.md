The **method of images** is a method for solving electrostatics problems that exploits the uniqueness of solutions for [[Laplace's equation]], which determines the [[electric potential]]. The method consists of modifying the system in such a way that the solution becomes more tractable and the conditions in the region of interest are identical to the unmodified system. The conditions outside the region will be different, but they can be discarded without an issue. Since the solution to Laplace's equation is unique, it doesn't matter that it was found in a different system: the conditions are the same where it matters, so the solution is correct.

This method can be applied to any charge distribution near a grounded plane substituting the plane with the mirror image of the charge distribution, with inverse charge. The mirror maintains the potential on the plane identically zero, therefore preserving the boundary conditions. In fact, the method works as long as the charge distribution $\rho$ and the zeroed potential $V$ of the conductor remain the same. As an algorithm, it works more or less like this:
1. Find the boundary conditions: where is $V$ null? Where is $\rho$?
2. Remove the conductor.
3. Find a place to add one or more point charges so that $\rho$ and the potential void are unchanged. The new charges must not be anywhere you're trying to calculate $V$, as that would change $\rho$ and therefore the conditions.
4. Solve the potential for the new system.
### Examples
#### Point charge and conductor plane
We want to find the [[electric field]] of a point [[Electric charge|charge]] $q$ and an infinite, grounded [[Conductor]] plane. The charge is a distance $d$ above the plane. Since we want to know the field on the charge, we only care about the solution in $z>0$, above the plane. We know the boundary conditions are
1. $V=0$ at $z=0$ because the plane is grounded.
2. $V=0$ at $x^{2}+y^{2}+z^{2} \gg d^{2}$, because convention.

The issue is that we don't know how the induced charge distributes itself over the conductor, nor how strong it is. Thus, we ditch the plane altogether. We instead keep the charge above at $(0,0,+d)$ and add another charge $-q$ at $(0,0,-d)$, opposite the one we have. The potential is now trivial to derive
$$V(x,y,z)=\frac{1}{4\pi \varepsilon_{0}}\left[ \frac{q}{\sqrt{ x^{2}+y^{2}+(z-d)^{2} }} - \frac{q}{\sqrt{ x^{2}+y^{2}+(z+d)^{2} }} \right]$$
We can easily see that the boundary conditions are preserved, as $V=0$ for $z=0$ and $V=0$ for $x^{2}+y^{2}+z^{2}\gg d^{2}$. The region $z>0$ is also unchanged, as the charge is were it was before and nothing was added or removed there. Since the solution in $z>0$ is unique, the formula for $V$ we just found must also apply to the previous system.

Importantly, the solution in $z\leq {0}$ is *not* correct at all when we put the plane back, but does not matter because that's not what we were looking for in the first place.

Since we know the potential, we can also find the surface charge density
$$\sigma=-\varepsilon_{0} \frac{ \partial V }{ \partial n } $$
using the normal derivative. The normal direction is just $z$ so
$$\sigma=-\varepsilon_{0} \left.\frac{ \partial V }{ \partial z }\right|_{z=0} $$
and since
$$\frac{ \partial V }{ \partial z } =\frac{1}{4\pi \varepsilon_{0}}\left[ \frac{-q(z-d)}{[x^{2}+y^{2}+(z-d)^{2}]^{3/2}}+ \frac{q(z+d)}{[x^{2}+y^{2}+(z+d)^{2}]^{3/2}} \right]$$
we get
$$\sigma(x,y)=\frac{-qd}{2\pi(x^{2}+y^{2}+d^{2})^{3/2}}$$
which gives us a negative charge, as expected. Notably, it's not uniform and it's denser near the charge and tapers off to infinity. We can also compute the total charge
$$Q=\underset{ xy\text{-plane} }{ \int }\sigma\ da$$
We can use [[polar coordinates]] for an easier integral
$$\sigma(r)=\frac{-qd}{2\pi(r^{2}+d^{2})^{3/2}}$$
so
$$Q=\int_{0}^{2\pi}\int_{0}^{\infty} \frac{-qd}{2\pi(r^{2}+d^{2})^{3/2}}r\ drd\phi=\left.\frac{qd}{\sqrt{ r^{2}+d^{2} }}\right|_{0}^{\infty}=-q$$
which checks out, because it could not have been anything else.

Since the potential is the same (in $z>0$) in both the original and modified systems, so are the electric field and the force on $q$. We have
$$\mathbf{E}=-\frac{1}{4\pi\varepsilon_{0}} \frac{q}{(2d)^{2}},\qquad\mathbf{F}=-\frac{1}{4\pi \varepsilon_{0}} \frac{q^{2}}{(2d)^{2}}\hat{\mathbf{z}}$$
Notably, the energy is *not* the same, not even in $z>0$. In fact, the charge-plane energy is exactly half of the two-charge energy. This is because the top and bottom planes contribute equally, but in the two-charge system, there is a field in both the top and bottom half of space, whereas in the charge-plane system, the field is only above.