The [[Lagrange equation]] is a second order differential equation of the form $\ddot{\mathbf{q}}=f(q,\dot{q},t)$, which can be also written in as a linear system of first order equations:
$$\begin{cases}
\dot{\mathbf{q}}=\boldsymbol{\eta} \\
\dot{\boldsymbol{\eta}}=f(q,\eta,t)
\end{cases}$$
Typically, we have $n$ Lagrange equations, or $2n$ first order equivalents. In terms of the [[Lagrangian]], each equation reads
$$\frac{d}{dt} \underbrace{ \frac{ \partial L }{ \partial \dot{q}_{i} } }_{ p_{i} } - \frac{ \partial L }{ \partial q_{i} } =0$$
where $i=1,\ldots,n$ and
$$p_{i}=\frac{ \partial L }{ \partial \dot{q}_{i} } (q_{1},\ldots,q_{n},\dot{q}_{1},\ldots,\dot{q}_{n},t)$$
If the [[determinant]] of the [[Jacobian]] of this quantity is nonzero, so
$$\det\left( \frac{ \partial  }{ \partial \dot{q}_{j} } \frac{ \partial L }{ \partial \dot{q}_{i} }  \right)\neq0$$
we can invert it to extract $\dot{q}_{k}$ as
$$\dot{q}_{k}=u_{k}(p,q,t)$$
for some function $u_{k}$. This comes at the cost of turning $p=p_{1},\ldots,p_{n}$ into a variable. To motivate this, let's look at an example.

> [!example] Mechanical systems
> In a mechanical system, the quantity $p_{i}$ can be expressed in terms of the [[Kinetic energy|kinetic matrix]] as
> $$p_{i}=\frac{ \partial L }{ \partial \dot{q}_{i} } =\sum_{j=1}^{n} a_{ij}\dot{q}_{j}+b_{i}$$
> which can be inverted as
> $$\dot{\mathbf{q}}=\mathrm{a}^{-1}(\mathbf{p}-\mathbf{b}(q,t))$$
> In this case, the functions $u_{k}$ are packaged as the inverse of the kinetic matrix. In fact, *all* mechanical systems allow this.

With this said, we can make the following proposition.

> [!info] Proposition
> Let $L(q,\dot{q},t)$ be a Lagrangian whose [[Hessian]] is [[Invertible matrix|invertible]], so $\det(\partial ^{2}L)\neq 0$. Then, the system
> $$\begin{cases}
> \dot{q}_{i}=u_{i}(p,q,t) \\
> \dot{p}_{i}=\frac{ \partial L }{ \partial q_{i} } (q,u(p,q,t),t)
> \end{cases}$$
> is equivalent to the **Hamilton equations**
> $$\begin{cases}
> \dot{q}_{i}=\frac{ \partial H }{ \partial q_{i} }(p,q,t) \\
> \dot{p}_{i}=-\frac{ \partial H }{ \partial q_{i} } (p,q,t)
> \end{cases}$$ 
> where
> $$H(p,q,t)\equiv\left.{(\mathbf{p}\cdot \dot{\mathbf{q}}-L(q,\dot{q},t))}\right|_{\dot{q}_{i}=u_{i}(p,q,t)}$$
> is the **Hamiltonian**. The following is also true:
> $$\frac{ \partial H }{ \partial t } =-\frac{ \partial L }{ \partial t } $$

We can prove it as follows. Start from the definition of $H(p,q,t)$ and take the [[Differential|total derivative]]:
$$dH=\sum_{l=1}^{n} \left( \frac{ \partial H }{ \partial p_{l} } dp_{l}+\frac{ \partial H }{ \partial q_{l} } dq_{l} \right)+\frac{ \partial H }{ \partial t } dt\tag{1}$$
Now also take the differential with respect to the definition evaluated in $\dot{\mathbf{q}}=\mathbf{u}(p,q,t)$:
$$\begin{align}
dH&=\sum_{l=1}^{n} (p_{l}du_{l}+u_{l}dp_{l})-\sum_{l=1}^{n} \underbrace{ \frac{ \partial L }{ \partial \dot{q}_{l} }(q,u,t) }_{ p_{l} }du_{l}-\sum_{l=1}^{n} \frac{ \partial L }{ \partial q_{l} } dq_{l}-\frac{ \partial L }{ \partial t } dt  \\
&=\cancel{ \sum_{l=1}^{n} p_{l}du_{l} }+\sum_{l=1}^{n}u_{l}dp_{l}-\cancel{ \sum_{l=1}^{n} p_{l}du_{l} }-\sum_{l=1}^{n} \frac{ \partial L }{ \partial q_{l} } dq_{l}-\frac{ \partial L }{ \partial t } dt \tag{2}
\end{align}$$
By comparing terms with the same differentials in both $(1)$ and $(2)$ we get
$$u_{i}=\frac{ \partial H }{ \partial p_{i} },\quad \frac{ \partial L }{ \partial q_{i} } =-\frac{ \partial H }{ \partial q_{i} } ,\quad \frac{ \partial L }{ \partial t }=-\frac{ \partial H }{ \partial t }   $$
which proves our point.

We may also write the Hamilton equations as a differential equation
$$\dot{\mathbf{x}}=E\nabla_{x}H(\mathbf{x},t)$$
There is also a very important point to note:

> [!info] Mechanical Hamiltonian is energy
> In a mechanical system, the Hamiltonian is the total energy of the system:
> $$H=T+V$$

Finally, as a note on differential geometry, recall how the set of possible positions of a system is the [[configuration space]] $Q$. When we add the possible velocities, as we do in the Lagrangian case, we get the so-called *[[tangent bundle]]* $TQ$ of the configuration space. Here in the Hamiltonian case, we add the momentum instead. It can be found that momenta are *[[cotangent vector|cotangent vectors]]* to a given point in the configuration space (like how velocities are *tangent vectors*), and thus the set of all momenta for a given configuration $P$ forms a *[[cotangent space]]* $T^{*}_{P}Q$ (instead of a *[[tangent space]]* $T_{P}Q$) and the union of all of these spaces makes a *[[cotangent bundle]]* $T^{*}Q$ (instead of a *tangent bundle* $TQ$). This cotangent bundle is known as the **[[phase space]]**.

To illustrate the behavior of a Hamiltonian, we'll use the most basic examples:

> [!example] Point mass
> The kinetic and potential energies are
> $$T=\frac{m}{2}(\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2}),\quad V\equiv V(x,y,z)$$
> for some potential energy $V$. The Lagrangian is $L=T-V$. We want to show that the Hamiltonian is instead $H=T+V$. To do that, we'll express the kinetic energy in terms of the [[Linear momentum|momentum]] instead of velocity:
> $$p_{x}=\frac{ \partial L }{ \partial \dot{x} } =m \dot{x},\quad p_{y}=\frac{ \partial L }{ \partial \dot{y} } =m \dot{y},\quad p_{z}=\frac{ \partial L }{ \partial \dot{z} } =m \dot{z}$$
> Hence
> $$H=\frac{m}{2}\left( \frac{p_{x}^{2}}{m^{2}}+ \frac{p_{y}^{2}}{m^{2}}+ \frac{p_{z}^{2}}{m^{2}}\right)+V(x,y,z)=\frac{\mathbf{p}^{2}}{2m}+V(\mathbf{x})$$
> The grand majority of Hamiltonians in physics have this form: $\mathbf{p}^{2}/2m$ plus a potential. This is because [[Cartesian coordinates]] are ubiquitous, as is considering point masses as objects, but it is a matter of "habit". This is not, *in general*, the shape of a Hamiltonian, as that depends on other factors such as the choice of coordinates. It just happens to be an overwhelmingly common specific case.

> [!example] Harmonic oscillator
> Using the same process of expressing kinetic energy in terms of momentum, the Hamiltonian of a (one-dimensional) [[harmonic oscillator]] is
> $$H=\frac{p^{2}}{2m}+ \frac{1}{2}m\omega ^{2}q^{2}$$

> [!example] Electromagnetic force
> The Lagrangian of a point mass under a [[Lorentz force]] is
> $$L=\frac{m}{2}\dot{\mathbf{q}}^{2}+e \dot{\mathbf{q}}\cdot \mathbf{A}-e\phi$$
> where we used the [[electric potential]] $\phi$ and the [[magnetic vector potential]] $\mathbf{A}$. $e$ is the [[electric charge]] (since $q$ is already taken by position). We'll use the [[Lagrange equation]] to find the Hamiltonian through its definition. Firstly,
> $$p_{i}=\frac{ \partial L }{ \partial \dot{q}_{i} } =m \dot{q}_{i}+eA_{i},\quad \dot{q}_{i}=\frac{p_{i}}{m}- \frac{e}{m}A_{i}$$
> and using the Hamiltonian definition
>$$\begin{align}
> H(p,q)&=\mathbf{p}\cdot \dot{\mathbf{q}}-L|_{\dot{\mathbf{q}}=\frac{p_{i}}{m}- \frac{e}{m}A_{i}} \\
> &=\frac{\mathbf{p}^{2}}{m}- \frac{e}{m}\mathbf{A}\cdot \mathbf{p}- \frac{m}{2} \frac{(\mathbf{p}-e\mathbf{A})^{2}}{m^{2}}- \frac{e}{m}(\mathbf{p}-e\mathbf{A})\cdot \mathbf{A}+e\phi \\
> &=\frac{(\mathbf{p}-e\mathbf{A})^{2}}{m}- \frac{(\mathbf{p}-e\mathbf{A})^{2}}{2m}+e\phi \\
> &=\frac{(\mathbf{p}-e\mathbf{A})^{2}}{2m}+e\phi
> \end{align}$$

### Derivation from the least-action principle
Above we derived the Hamilton equation from the [[Lagrange equation]], which itself was derived from [[Newton's laws|Newton's second law]]. However, the Lagrange equation can also be found from the [[least action principle]]: real motion is the one that minimizes the [[action]]. It's fair to ask if we can do the same thing with the Hamiltonian, and the answer to that is yes, and it involves minimizing the action [[functional]]:
$$S[\mathbf{p},\mathbf{q}]=\int_{t_{1}}^{t_{2}}\left( \sum_{i=1}^{n} p_{i}(t)\dot{q}_{i}(t)-H(p(t),q(t),t) \right)dt$$
This is because the term in parenthesis is actually just the Lagrangian, expressed in terms of the Hamiltonian. As such, everything else works the same as the Lagrangian case.
### In different coordinates
Say the motion is described by the function $(q_{1}(t),\ldots,q_{n}(t),p_{1}(t),\ldots,q_{n}(t))\in T^{*}Q$, whose components obey the Hamilton equations. As usual, we may want to change system of coordinates, such as going from [[Cartesian coordinates]] to [[spherical coordinates]] using some [[coordinate transformation]]. However, strictly speaking, just because our function satisfies the Hamilton equations in one system doesn't mean that it will satisfy them in the other. A coordinate transformation is *not* guaranteed to preserve the Hamiltonian structure. Since changing coordinates is useful, we'd want some subset of transformations that *do* retain the Hamiltonian structure. Such a transformation is said to be a **[[canonical transformation]]**, which is a coordinate transformation that also returns a function that satisfies the Hamilton equations.