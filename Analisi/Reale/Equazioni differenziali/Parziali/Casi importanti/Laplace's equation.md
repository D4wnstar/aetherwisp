**Laplace's equation** is the [[partial differential equation]]
$$\nabla^{2}\psi=0$$
where $\nabla^{2}$ is the [[Laplaciano|Laplacian]]. A solution to this equation is said to be a **harmonic function**. It is a particular case of the [[Poisson's equation|Poisson's equation]], where $f=0$.

It is useful to solve the Laplace equation in coordinate systems other than Cartesian, for example, in [[Spherical coordinates]]. In many coordinates, it is possible to solve the equation using the method of [[separation of variables]].
### One-dimensional case
In one dimension, using [[Cartesian coordinates]], the equation simplifies to a [[Ordinary differential equation|ordinary differential equation]]:
$$\frac{ d^{2} \psi }{ d x^{2} } =0$$
and the general solution is simply
$$\psi(x)=mx+b$$
which is just a straight line. The constants are determined by the boundary conditions. From this, we can derive a couple of useful results that carry over to the two- and three-dimensional cases:
1. Given a certain $a$, $\psi(x)$ is the average of $\psi(x+a)$ and $\psi(x-a)$:$$\psi(x)=\frac{1}{2}[\psi(x+a)+\psi(x-a)]$$and the harmonics that solve the equation fit the endpoints exactly. In a way, Laplace's equation is a rule on how to average a function.
2. There are no *local* [[Punto critico|critical points]] within the harmonic. The only critical points are at the edges of the function. This is a direct consequence of point 1., as if there were maxima and minima within the function, then there would be cases in which the solution would not be an average (as both sides would be bigger or smaller).
### Two-dimensional case
In two dimensions, using Cartesian coordinates, the equation is
$$\frac{ \partial ^{2} \psi }{ \partial x^{2} }+\frac{ \partial ^{2} \psi }{ \partial y^{2} } =0$$
Since it is a partial differential equation, it has no closed-form general solution. Nevertheless, the properties from the one-dimensional case still apply:
1. The value of $\psi(x,y)$ is the average of all surrounding points, given by a closed integral over a circle of radius $R$ around the point:$$\psi(x,y)=\frac{1}{2\pi R}\underset{ \text{circle} }{ \oint }\psi\ dl$$
2. The maxima and minima are all at the boundary. The surface of the function is perfectly smooth, with no hills or valleys.
#### Solution by separation of variables
Separation of variables instructs us to look for solutions of the form
$$\psi(x,y)=\phi(x)\theta(y)$$
so that our equation becomes
$$\theta \frac{ \partial ^{2} \phi }{ \partial x^{2} }+\phi \frac{ \partial ^{2}\theta }{ \partial y^{2} } =0 $$
Dividing through by $\psi$ we get
$$\frac{1}{\phi}\frac{ \partial ^{2}\phi }{ \partial x^{2} } + \frac{1}{\theta}\frac{ \partial ^{2}\theta }{ \partial y^{2} } =0$$
In other terms,
$$\frac{1}{\phi}\frac{ \partial ^{2}\phi }{ \partial x^{2} } =- \frac{1}{\theta}\frac{ \partial ^{2}\theta }{ \partial y^{2} } $$
These two terms are dependent only on $x$ and $y$ respectively, but they are also equal. This means that if one changes (say, $x$ varies and thus $\phi$), than so does the other. The issue is that $\theta$ is not dependent on $x$, but by equality it must change to mimic the other term. In substance, the $\theta$ would be changed by $x$ despite being independent of it. This makes no sense and the only scenario in which this does not happen is if both terms are actually independent of *all* variables, that is, they are constant.

This permits us to write
$$\frac{1}{\phi}\frac{ \partial ^{2}\phi }{ \partial x^{2} } =C_{1},\qquad \frac{1}{\theta}\frac{ \partial ^{2} \theta }{ \partial y^{2} } =C_{2}$$
and thus $C_{1}=-C_{2}$. Renaming them to $k^{2}$, we get
$$\frac{ \partial ^{2}\phi }{ \partial x^{2} } =k^{2}\phi,\qquad \frac{ \partial ^{2}\theta }{ \partial y^{2} } =-k^{2}\theta$$
Since these are just [[Harmonic oscillator|harmonic oscillators]], we have the solution
$$\psi(x,y)=(Ae^{kx}+Be^{-kx})(C\sin ky+D\cos ky)$$
Determining the constants $A$, $B$, $C$ and $D$ requires knowing the boundary conditions, which depends on the problem. The important part is that the solution is not expressible in closed form, as solving this equation gives us an infinite number of possibilities. Each solution individually is likely not the description of the system at hand, but they possess the important property of linearity, that is, the sum of several solutions is still a solution. Thus, it is possible to [[combinazione lineare|linearly combine]] several solutions (an infinite number, actually), to describe the state of the system. As an example, it may take the form
$$\psi(x,y)=\sum_{n=1}^{\infty} c_{n}e^{-n\pi x/a}\sin\left( \frac{n\pi x}{a} \right)$$
where $n$ is a nonzero integer and $a$ is a constant. This is a [[Serie di Fourier|Fourier series]], specifically a sine series. From Fourier analysis, we know that any [[Funzione generalmente continua|almost always continuous]] function can be expressed as a Fourier series, so that's the only limitation on $\psi(x,y)$. The coefficients can as usual be derived with a [[Prodotto scalare|dot product]] like
$$c_{n}=(\psi_{n},\ \psi)=\left( e^{-n\pi x/a}\sin\left( \frac{n\pi x}{a} \right),\ \psi \right)$$
As is always the case for separable solutions, the set formed by $\{\psi_{n}\}_{n\in \mathbb{N}}$ is a [[Sistema ortonormale completo|complete orthonormal set]] and thus $\psi_{n}\psi_{m}=\delta_{nm}$ with the [[Delta di Kronecker|Kronecker delta]] and $\psi=\sum_{n}^{\infty}c_{n}\psi_{n}$ is always true.

We can also find a solution in [[Spherical coordinates]] by starting in three-dimensions and then assuming *azimuthal symmetry*, which states that $\psi$ is independent from the azimuthal angle. This removes one variable, leaving a two-dimensional solution. The most general solution found that is compatible with minimum physical requirements is
$$\psi(r,\theta)=\sum_{l=0}^{\infty} \left( A_{l}r^{l}+ \frac{B_{l}}{r^{l+1}} \right)P_{l}(\cos \theta)$$
where $P_{l}(\cos \theta)$ are the [[Polinomi di Legendre|Legendre polynomials]].
### Three-dimensional case
In three dimensions, we get the full equation:
$$\frac{ \partial ^{2} \psi }{ \partial x^{2} } + \frac{ \partial ^{2} \psi }{ \partial y^{2} } + \frac{ \partial ^{2} \psi }{ \partial z^{2} } =0$$
In this case, the properties are as follow:
1. The value of $\psi(x,y,z)$ is again the average of all surrounding points, this time determined by a loop integral on a sphere centered on that point:$$\psi(x,y,z)=\frac{1}{4\pi R^{2}}\underset{ \text{sphere} }{ \oint } \psi\ da$$
2. The maxima and minima are still at the boundary. There is no easy way to visualize this, but the general property of minimizing the [[measure]] of the space spanning the boundary still applies.

The separable variable solution for the three-dimensional case is similar to the two-dimensional case, but becomes more complicated as it ends up requiring a double Fourier series over two sets of solutions. An example is
$$\psi(x,y,z)=\sum_{n=1}^{\infty} \sum_{m=1}^{\infty} c_{nm}e^{-\pi \sqrt{ (n/a)^{2}+(m/b)^{2} }\ x}\sin\left( \frac{n\pi y}{a} \right)\sin\left( \frac{m\pi z}{b} \right)$$
where $n$ and $m$ are the integer indexes and $a$ and $b$ are constants.

For a solution in spherical coordinates, see [[Equazione di Schrödinger#Soluzione tridimensionale|Schrödinger's equation]].
### Uniqueness theorems
Determining what the boundary conditions are in the one-dimensional case is easy: just provide the values at the edges, or a derivative at an edge and a value at the same edge, or... several other combinations. But we can't provide the derivative at both edges, as that would be either redundant (if they are equal) or nonsense (if they are different).

For the two- and three-dimensional case, such easy logic doesn't hold. The proof that a set of boundary condition provides a unique solution is usually given in the form of a *uniqueness theorem*. There are several for the Laplace equation.
#### First uniqueness theorem
> [!info] First uniqueness theorem
> The solution to Laplace's equation in some volume $V$ is uniquely determined if $\psi$ is specified on the boundary surface $S$.

This theorem actually also applies to Poisson's equation.
##### Proof
Consider a volume $V$ and let's assume the we know the value of $\psi$ on its surface. It does not need to be solid: there may "holes" within, provided we know $\psi$ on all of those surfaces too. It's also possible for the outer surface to be at infinity provided, again, we know the limit of $\psi$ at infinity. Suppose there are two solutions to the equation:
$$\nabla ^{2}\psi_{1}=0, \qquad \nabla ^{2}\psi_{2}=0$$
both of which have the same value on the surface(s). If we look at their difference, it is
$$\psi_{3}=\psi_{1}-\psi_{2}$$
which must also obey Laplace's equation:
$$\nabla ^{2}\psi_{3}=\nabla ^{2}\psi_{1}-\nabla ^{2}\psi_{2}=0$$
This takes the value *zero* on all boundaries, since $\psi_{1}$ and $\psi_{2}$ have the same value there. But we know there are no maxima and minima outside of the boundary, thus all other points must be themselves zero, so $\psi_{3}=0$, which means $\psi_{1}=\psi_{2}$.

$$F(r)=- \frac{q^{2}r_{0}r}{4\pi \varepsilon_{0}(r^{2}-r_{0}^{2})^{2}}$$

The same can be proven for Poisson's equation, as the function $f$ cancels out either way. We can express this as a sort of corollary:

> [!info] Corollary, first uniqueness theorem
> The solution to Poisson's equation in a volume $V$ is uniquely determined if the function $f$ and the value of $\psi$ on all boundaries are specified.

##### Electrostatic interpretation
This theorem (especially the corollary) is of particular use in electrostatics, where the [[electric potential]] obeys Poisson's equation. The corollary can therefore be stated as:

> [!info] Corollary, electric potential
> The electric potential in a volume $\mathcal{V}$ is uniquely determined if the volume charge density $\rho$ and the value of the potential $V$ on all boundaries are specified.

This is useful because the potential is often known, since it comes from artificial batteries that are built provide a specific potential.
#### Second uniqueness theorem
The second uniqueness theorem is given directly in electromagnetic flavor.

> [!info] Second uniqueness theorem
> In a volume $\mathcal{V}$ surrounded by [[Conductor|conductors]] (or possibly extending to infinity) and containing a specified charge density $\rho$, the [[electric field]] is uniquely determined if the total charge on each conductor is given.

##### Proof
Suppose there are two fields satisfying the conditions. Both obey [[Gauss' law]]:
$$\nabla\cdot\mathbf{E}_{1}=\frac{\rho}{\varepsilon_{0}},\qquad \nabla\cdot\mathbf{E}_{2}=\frac{\rho}{\varepsilon_{0}}$$
also in integral form for a Gaussian form each containing a conductor:
$$\underset{ i\text{-th conductor} }{ \oint }\mathbf{E}_{1}\cdot d\mathbf{a}=\frac{Q_{i}}{\varepsilon_{0}},\qquad \underset{ i\text{-th conductor} }{ \oint }\mathbf{E}_{2}\cdot d\mathbf{a}=\frac{Q_{i}}{\varepsilon_{0}}$$
and for the outermost surface:
$$\underset{ \text{outer surface} }{ \oint }\mathbf{E}_{1}\cdot d\mathbf{a}=\frac{Q_\text{tot}}{\varepsilon_{0}},\qquad\underset{ \text{outer surface} }{ \oint }\mathbf{E}_{2}\cdot d\mathbf{a}=\frac{Q_\text{tot}}{\varepsilon_{0}}$$
Let's examine the difference
$$\mathbf{E}_{3}=\mathbf{E}_{1}-\mathbf{E}_{2}$$
which obeys
$$\nabla\cdot\mathbf{E}_{3}=0$$
in the region between the conductors and
$$\oint \mathbf{E}_{3}\cdot d\mathbf{a}=0$$
over each boundary surface. Since conductors are equipotential volumes, we know that the potential $V_{3}$ associated with $\mathbf{E}_{3}$ has to be a constant for all conductor surfaces (it doesn't need to be the *same* constant for all of them). The trick is to use the product rule
$$\nabla \cdot(V_{3}\mathbf{E}_{3})=V_{3}(\nabla\cdot\mathbf{E}_{3})+\mathbf{E}_{3}\cdot(\nabla V_{3})=-(E_{3})^{2}$$
Integrating over $\mathcal{V}$ and applying the [[Teorema della divergenza|divergence theorem]] to the left side we get
$$\int_{\mathcal{V}}\nabla\cdot (V_{3}\mathbf{E_{3}})\ d\tau=\oint_{\mathcal{S}}V_{3}\mathbf{E}_{3}\cdot d\mathbf{a}=-\int_{\mathcal{V}}E_{3}^{2}\ d\tau$$
The surface $\mathcal{S}$ covers all boundaries of the region in question, i.e. the conductors and outer boundary. Since $V_{3}$ is constant over each surface, it comes out of the integrals and what remains is zero. Thus we're left with
$$\int_{\mathcal{V}}E_{3}^{2}\ d\tau=0$$
$E_{3}^{2}$ is of course always positive, so the only way for it to vanish is if it's always zero. Therefore $\mathbf{E}_{1}=\mathbf{E}_{2}$.