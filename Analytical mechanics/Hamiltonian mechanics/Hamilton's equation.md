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
> is equivalent to **Hamilton's equations**
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