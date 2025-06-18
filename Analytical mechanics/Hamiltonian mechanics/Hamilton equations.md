---
wiki-publish: true
aliases:
  - Hamiltonian flux
---
The **Hamilton equations** are a set of equations that derive the motion of a [[physical system]] from its [[Hamiltonian]] $H$:
$$\dot{q}_{i}=\frac{ \partial H }{ \partial p_{i} },\quad \dot{p}_{i}=-\frac{ \partial H }{ \partial q_{i} }  $$
$q_{i}$ are the [[generalized coordinates]] and $p_{i}$ are their [[conjugate momenta]]. Just like the [[Lagrange equation]], in a system of $n$ [[degrees of freedom]], there are $2n$ Hamilton equations. Solving all of them determines the trajectory of the system. The $2n$ equations can be written in compact form as
$$\dot{\mathbf{x}}=\mathrm{E}\nabla_{\mathbf{x}}H(\mathbf{x},t)=\{ \mathbf{x},H \}$$
where $\mathbf{x}=(\mathbf{q},\mathbf{p})$ are [[canonical coordinates]] and $\mathrm{E}$ is the $2n$-dimensional [[Symplectic matrix|standard symplectic matrix]]. $\nabla_{\mathbf{x}}$ represents the [[gradient]] as computed in canonical coordinates, which is the to say the [[phase space]] gradient. The curly braces are the [[Poisson brackets]].
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

> [!info] Proposition
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

> [!info] Proof
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

Finally, as a note on differential geometry, recall how the set of possible positions of a system is the [[configuration space]] $Q$. When we add the possible velocities, as we do in the Lagrangian case, we get the so-called *[[tangent bundle]]* $TQ$ of the configuration space. Here in the Hamiltonian case, we add the momentum instead. It can be found that momenta are *[[cotangent vector|cotangent vectors]]* to a given point in the configuration space (like how velocities are *tangent vectors*), and thus the set of all momenta for a given configuration $P$ forms a *[[cotangent space]]* $T^{*}_{P}Q$ (instead of a *[[tangent space]]* $T_{P}Q$) and the union of all of these spaces makes a *[[cotangent bundle]]* $T^{*}Q$ (instead of a *tangent bundle* $TQ$). This cotangent bundle is known as the **[[phase space]]**.
### Derivation from the least-action principle
Above we derived the Hamilton equation from the [[Lagrange equation]], which itself was derived from [[Newton's laws|Newton's second law]]. However, the Lagrange equation can also be found from the [[least action principle]]: real motion is the one that minimizes the [[action]]. It's fair to ask if we can do the same thing with the Hamiltonian, and the answer to that is yes, and it involves minimizing the action [[functional]]:
$$S[\mathbf{p},\mathbf{q}]=\int_{t_{1}}^{t_{2}}\left( \sum_{i=1}^{n} p_{i}(t)\dot{q}_{i}(t)-H(p(t),q(t),t) \right)dt$$
This is because the term in parenthesis is actually just the Lagrangian, expressed in terms of the Hamiltonian. As such, everything else works the same as the Lagrangian case.
### In different coordinates
Say the motion is described by the function $(q_{1}(t),\ldots,q_{n}(t),p_{1}(t),\ldots,q_{n}(t))\in T^{*}Q$, whose components obey the Hamilton equations. As usual, we may want to change system of coordinates, such as going from [[Cartesian coordinates]] to [[spherical coordinates]] using some [[coordinate transformation]]. However, strictly speaking, just because our function satisfies the Hamilton equations in one system doesn't mean that it will satisfy them in the other. A coordinate transformation is *not* guaranteed to preserve the Hamiltonian structure. Since changing coordinates is useful, we'd want some subset of transformations that *do* retain the Hamiltonian structure. Such a transformation is said to be a **[[canonical transformation]]**, which is a coordinate transformation that also returns a function that satisfies the Hamilton equations.
### The Hamiltonian flux
As we've seen, the Hamilton equation can be written as
$$\dot{\mathbf{x}}=\mathrm{E}\nabla_{x}H(\mathbf{x},t)$$
which is a first order differential equation. As with other differential equations, we can look for the [[Ordinary differential equation|flux of a vector field]]. We'll denote it $\Phi^{t}:T^{*}Q\to T^{*}Q$ and its application is $\mathbf{x}_{0}\to \Phi^{t}(\mathbf{x}_{0})\equiv \mathbf{x}(t;\mathbf{x}_{0})$. As usual, this isn't a single map, but rather a family of maps parameterized by $t$. We call this the **Hamiltonian flux**.

Given $n$ [[degrees of freedom]], the Hamiltonian flux is an invertible function with domains $\mathbb{R}^{2n}\to \mathbb{R}^{2n}$. This qualifies it as a [[coordinate transformation]], so we can use $\Phi^{t}$ to change coordinates. We'll define the transformation as simply $\mathbf{x}\equiv \mathbf{w}(\tilde{x},t)=\Phi^{t}(\tilde{x})$. This is actually a [[canonical transformation]]! In fact, the [[Jacobian]] is
$$J_{ij}=\frac{ \partial w_{i} }{ \partial \tilde{x}_{j} } =\frac{ \partial \Phi_{i}^{t} }{ \partial \tilde{x}_{j} } $$
We just need to prove that $J$ is a [[Matrice simmetrica|symmetrical matrix]], so $J^{T}\mathrm{E}J=\mathrm{E}$ for all $t$. For $t=0$,
$$w_{i}(\tilde{x},0)=\Phi_{i}^{0}(\tilde{x})=\tilde{x}_{i}\quad\Rightarrow \quad J_{ij}=\frac{ \partial w_{i} }{ \partial \tilde{x}_{j} } =\frac{ \partial \tilde{x}_{i} }{ \partial \tilde{x}_{j} } =\delta_{ij}$$
But remember that the [[Kronecker delta]] defines the components of the [[identity matrix]] $\mathrm{I}$, so $J$ is the identity matrix for $t=0$ (which is symmetrical, and $\mathrm{I}\mathrm{E}\mathrm{I}=\mathrm{E}$). We now want to extend this to any $t$. We'll do so by proving that $J_{t}^{T}\mathrm{E}J_{t}$ does not actually depend on $t$. To do so, we'll just see if the time derivative is zero:
$$\frac{ \partial  }{ \partial t } J_{t}^{T}\mathrm{E}J_{t}=0\quad(?)$$
If this is true, then $J_{t}^{T}\mathrm{E}J_{t}=J_{0}^{T}\mathrm{E}J_{0}=\mathrm{E}$ and that would prove our point. So, the derivative is
$$\begin{align}
\frac{ \partial  }{ \partial t } (J^{T}\mathrm{E}J)_{ih}&=\frac{ \partial  }{ \partial t } \left( \sum_{j,k}J_{ij}^{T}\mathrm{E}_{jk}J_{kh}^{T} \right)=\frac{ \partial  }{ \partial t } \left( \sum_{j,k}J_{ji}\mathrm{E}_{jk}J_{kh} \right)=\frac{ \partial  }{ \partial t } \left( \sum_{j,k}\frac{ \partial \phi_{j}^{T} }{ \partial \tilde{x}_{i} } \mathrm{E}_{jk}\frac{ \partial \Phi_{k}^{t} }{ \partial \tilde{x}_{h} }  \right) \\
&=\sum_{j,k}\left[ \frac{ \partial  }{ \partial \tilde{x}_{i} } \left( \frac{ \partial \Phi^{t}_{j}(\tilde{x}) }{ \partial t }  \right)\mathrm{E}_{jk}\frac{ \partial \Phi_{k}^{t} }{ \partial \tilde{x}_{h} } +\frac{ \partial \Phi_{j}^{t} }{ \partial \tilde{x}_{i} } \mathrm{E}_{jk}\frac{ \partial  }{ \partial \tilde{x}_{h} } \left( \frac{ \partial \Phi^{t}(\tilde{x}) }{ \partial t }  \right) \right]=\ldots
\end{align}$$
Now, we need the time derivative of $\Phi^{t}$. Recall that $\Phi^{t}\equiv \mathbf{w}$, so
$$\frac{ \partial  }{ \partial t } \mathbf{w}(\tilde{x},t)=\frac{ \partial \Phi^{t} }{ \partial t } (\mathbf{x}_{0})=\frac{ \partial }{ \partial t } \mathbf{x}(t,\mathbf{x}_{0})=\dot{\mathbf{x}}(t)=\mathrm{E}\nabla_{x}H(x(t),t)$$
The last step is allowed because this is not a generic $\dot{\mathbf{x}}$, it's specifically the one that solves motion, so $\dot{\mathbf{x}}(t)$, which means we can use the Hamilton equation. Moving on, then, we'll write the first half of the square brackets above:
$$\ldots=\sum_{j,k,l}\underbrace{ \mathrm{E}_{jl} }_{ -\mathrm{E}_{lj} }\frac{ \partial  }{ \partial \tilde{x}_{j} } \underbrace{ \left( \frac{ \partial H }{ \partial \tilde{x}_{i} } (w(\tilde{x},t)) \right) }_{ (*) }\mathrm{E}_{jk}\underbrace{ \frac{ \partial \Phi_{h}^{t} }{ \partial \tilde{x}_{h} } }_{ J_{kh} } +\ldots$$
where
$$(*)\equiv\sum_{a}\frac{ \partial ^{2}H }{ \partial x_{a}\partial x_{l}}\frac{ \partial \Phi_{a}^{t} }{ \partial \tilde{x}_{i} } =\sum_{a}\frac{ \partial ^{2}H }{ \partial x_{a}\partial x_{l}}J_{ai}=\sum_{a}\frac{ \partial ^{2}H }{ \partial x_{a}\partial x_{l}}J_{ia}^{T} $$
The other half is the same, but with different indexes ($j\to m$ and $a\to b$), so
$$\begin{align}
\ldots&=-\sum_{j,k,l,a}J_{ia}^{T}(\partial^{2}H)_{al}\mathrm{E}_{jl}\mathrm{E}_{jk}J_{kh}+\sum_{j,k,m,b}J_{ij}^{T}\mathrm{E}_{jk}\mathrm{E}_{km}(\partial ^{2}H)_{mb}J_{bh} \\
&=-J^{T}(\partial ^{2}H)\mathrm{E}^{2}J+J^{T}\mathrm{E}^{2}(\partial ^{2}H)J \\
&=-J^{T}(\partial ^{2}H)J+J^{T}(\partial ^{2}H)J \\
&=0
\end{align}$$
That completes our proof. The Jacobian is symmetrical at $t=0$ and it also doesn't depend on $t$, so it's always symmetrical. In other words, the Hamiltonian flux is *always* a symplectic transformation.

This is all a very long-winded way of saying that we can talk about motion though these (rather weird) coordinates determined by the Hamiltonian flux. 

%%Let's stop here for a moment. An equation of the form $x=w(\tilde{x},t)$ can be interpreted as a coordinate transformation, but also as an active transformation in [[phase space]] $T^{*}Q$.%%