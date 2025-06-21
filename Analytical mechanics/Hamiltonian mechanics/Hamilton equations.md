---
wiki-publish: true
aliases:
  - Hamiltonian system
---
The **Hamilton equations** are a set of equations that derive the motion of a [[physical system]] from its [[Hamiltonian]] $H$:
$$\dot{q}_{i}=\frac{ \partial H }{ \partial p_{i} },\quad \dot{p}_{i}=-\frac{ \partial H }{ \partial q_{i} }  $$
$q_{i}$ are the [[generalized coordinates]] and $p_{i}$ are their [[conjugate momenta]]. Just like the [[Lagrange equation]], in a system of $n$ [[degrees of freedom]], there are $2n$ Hamilton equations. Solving all of them determines the trajectory of the system. The $2n$ equations can be written in compact form as
$$\dot{\mathbf{x}}=\mathrm{E}\nabla_{\mathbf{x}}H(\mathbf{x},t)=\{ \mathbf{x},H \}$$
where $\mathbf{x}=(\mathbf{q},\mathbf{p})$ are [[canonical coordinates]] and $\mathrm{E}$ is the $2n$-dimensional [[Symplectic matrix|standard symplectic matrix]]. $\nabla_{\mathbf{x}}$ represents the [[gradient]] as computed in canonical coordinates, which is the to say the [[phase space]] gradient. The curly braces are the [[Poisson brackets]].

A system whose dynamics are governed by the Hamilton equations is called a **Hamiltonian system**.
### Derivation from the Lagrange equation
The [[Lagrange equation]] is a second order differential equation of the form $\ddot{\mathbf{q}}=f(q,\dot{q},t)$, which can be also written in as a linear system of first order equations:
$$\begin{cases}
\dot{\mathbf{q}}=\boldsymbol{\eta} \\
\dot{\boldsymbol{\eta}}=f(q,\eta,t)
\end{cases}$$
Typically, we have $n$ Lagrange equations, or $2n$ first order equivalents. In terms of the [[Lagrangian]], each equation reads
$$\frac{d}{dt} \underbrace{ \frac{ \partial L }{ \partial \dot{q}_{i} } }_{ p_{i} } - \frac{ \partial L }{ \partial q_{i} } =0$$
where $i=1,\ldots,n$ and $p_{i}$ are the [[conjugate momenta]]. If the [[determinant]] of the [[Jacobian]] of this quantity is nonzero, so
$$\det\left( \frac{ \partial  }{ \partial \dot{q}_{j} } \frac{ \partial L }{ \partial \dot{q}_{i} }  \right)\neq0$$
we can invert it to extract $\dot{q}_{k}$ as
$$\dot{q}_{k}=u_{k}(p,q,t)$$
for some function $u_{k}$. This comes at the cost of turning $p\equiv(p_{1},\ldots,p_{n})$ into a variable. To motivate this, let's look at an example.

> [!example] Mechanical systems
> In a mechanical system, the quantity $p_{i}$ can be expressed in terms of the [[Kinetic energy|kinetic matrix]] as
> $$p_{i}=\frac{ \partial L }{ \partial \dot{q}_{i} } =\sum_{j=1}^{n} a_{ij}\dot{q}_{j}+b_{i}$$
> which can be inverted as
> $$\dot{\mathbf{q}}=\mathrm{a}^{-1}(\mathbf{p}-\mathbf{b}(q,t))$$
> In this case, the functions $u_{k}$ are packaged as the inverse of the kinetic matrix. In fact, *all* mechanical systems follow this shape.

With this said, we can make the following proposition.

> [!info] Hamilton equations
> Let $L(q,\dot{q},t)$ be a Lagrangian whose [[Hessian]] $\partial ^{2}L$ is [[Invertible matrix|invertible]], so $\det(\partial ^{2}L)\neq 0$. Then, the system
> $$\begin{cases}
> \dot{q}_{i}=u_{i}(p,q,t) \\
> \dot{p}_{i}=\frac{ \partial L }{ \partial q_{i} } (q,u(p,q,t),t)
> \end{cases}$$
> is equivalent to the **Hamilton equations**
> $$\begin{cases}
> \dot{q}_{i}=\frac{ \partial H }{ \partial p_{i} }(p,q,t) \\
> \dot{p}_{i}=-\frac{ \partial H }{ \partial q_{i} } (p,q,t)
> \end{cases}$$ 
> where
> $$H(p,q,t)\equiv\left.{(\mathbf{p}\cdot \dot{\mathbf{q}}-L(q,\dot{q},t))}\right|_{\dot{q}_{i}=u_{i}(p,q,t)}$$
> is the **Hamiltonian**. The following is also true:
> $$\frac{ \partial H }{ \partial t } =-\frac{ \partial L }{ \partial t } $$

> [!quote]- Proof
> Start from the definition of $H(p,q,t)$ and take the [[Differential|total derivative]]:
> $$dH=\sum_{l=1}^{n} \left( \frac{ \partial H }{ \partial p_{l} } dp_{l}+\frac{ \partial H }{ \partial q_{l} } dq_{l} \right)+\frac{ \partial H }{ \partial t } dt\tag{1}$$
> Now also take the differential with respect to the definition $H=\mathbf{p}\cdot \dot{\mathbf{q}}-L$ evaluated in $\dot{\mathbf{q}}=\mathbf{u}(p,q,t)$:
> $$\begin{align}
> dH&=\sum_{l=1}^{n} (p_{l}du_{l}+u_{l}dp_{l})-\sum_{l=1}^{n} \underbrace{ \frac{ \partial L }{ \partial \dot{q}_{l} }(q,u,t) }_{ p_{l} }du_{l}-\sum_{l=1}^{n} \frac{ \partial L }{ \partial q_{l} } dq_{l}-\frac{ \partial L }{ \partial t } dt  \\
> &=\cancel{ \sum_{l=1}^{n} p_{l}du_{l} }+\sum_{l=1}^{n}u_{l}dp_{l}-\cancel{ \sum_{l=1}^{n} p_{l}du_{l} }-\sum_{l=1}^{n} \frac{ \partial L }{ \partial q_{l} } dq_{l}-\frac{ \partial L }{ \partial t } dt \tag{2}
> \end{align}$$
> By comparing terms with the same differentials in both $(1)$ and $(2)$ we get
> $$u_{i}=\dot{q}_{i}=\frac{ \partial H }{ \partial p_{i} },\quad \frac{ \partial L }{ \partial q_{i} }=\dot{p}_{i} =-\frac{ \partial H }{ \partial q_{i} } ,\quad \frac{ \partial L }{ \partial t }=-\frac{ \partial H }{ \partial t }   $$
> which proves our point.

We may also write the Hamilton equations as a first order differential equation. See the equations as as vectors:
$$
\begin{pmatrix}
\dot{q}_1 \\
\vdots \\
\dot{q}_n \\
\dot{p}_1 \\
\vdots \\
\dot{p}_n
\end{pmatrix}
=
\begin{pmatrix}
\frac{\partial H}{\partial p_1} \\
\vdots \\
\frac{\partial H}{\partial p_n} \\
-\frac{\partial H}{\partial q_1} \\
\vdots \\
-\frac{\partial H}{\partial q_n}
\end{pmatrix}
$$
This can be expressed compactly as:
$$
\dot{\mathbf{x}} =
\underbrace{
\begin{pmatrix}
0 & -\mathrm{I}_{n} \\
\mathrm{I}_{n} & 0
\end{pmatrix}
}_{\mathrm{E}} 
\underbrace{
\begin{pmatrix}
\frac{\partial H}{\partial p} \\
\frac{\partial H}{\partial q}
\end{pmatrix}
}_{\nabla_{\mathbf{x}} H}
$$
and so
$$\boxed{\dot{\mathbf{x}}=\mathrm{E}\nabla_{x}H(\mathbf{x},t)}$$
### Derivation from the least-action principle
Above we found the Hamilton equations from the [[Lagrange equation]], which itself was derived from [[Newton's laws|Newton's second law]]. However, the Lagrange equation can also be found from the [[least action principle]]: the motion is the one that minimizes the [[action]]. The Hamilton equations can too be derived from the least action principle, and it involves minimizing the action [[functional]]:
$$S[\mathbf{p},\mathbf{q}]=\int_{t_{1}}^{t_{2}}\left( \sum_{i=1}^{n} p_{i}(t)\dot{q}_{i}(t)-H(p(t),q(t),t) \right)dt$$
 This is because the Lagrangian can be expressed in terms of the Hamiltonian ($L=\mathbf{p}\cdot \dot{\mathbf{q}}-H$), so a simple substitution gives an equivalent definition for $H$ instead of $L$.
### In differential geometry
Recall how the set of possible positions of a system is its [[configuration space]] $Q$. When we add the possible velocities, as we do in the Lagrangian case, we get the so-called *[[tangent bundle]]* $TQ$ of the configuration space. Here in the Hamiltonian case, we add the momentum instead. It can be found that momenta are *[[cotangent vector|cotangent vectors]]* to a given point in the configuration space (like how velocities are *tangent vectors*), and thus the set of all momenta for a given configuration $P$ forms a *[[cotangent space]]* $T^{*}_{P}Q$ (instead of a *[[tangent space]]* $T_{P}Q$) and the union of all of these spaces makes a *[[cotangent bundle]]* $T^{*}Q$ (instead of a *tangent bundle* $TQ$). This cotangent bundle is known as the **[[phase space]]**.
### Changing coordinates
As usual, we may want to change system of coordinates to make our life easier, such as going from [[Cartesian coordinates]] to [[spherical coordinates]] using some [[coordinate transformation]]. However, we need to be a little careful when dealing with the Hamilton equations. Say our original coordinates satisfy the Hamilton equations. Then, we transform to a different set of coordinates. The new ones are *not* guaranteed to satisfy them. We say that the new ones are not guaranteed to **preserve the form** of the Hamilton equations.

Since changing coordinates is nevertheless very useful, we want some way of identifying which transformations *do* preserve the form. These transformations are called **[[canonical transformation|canonical transformations]]**.