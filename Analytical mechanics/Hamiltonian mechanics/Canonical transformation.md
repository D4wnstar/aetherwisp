---
wiki-publish: true
aliases:
  - conjugate Hamiltonian
---
A **canonical transformation** is a [[coordinate transformation]] that transforms a set of coordinates that satisfy the [[Hamilton equation|Hamilton equations]] of a [[Physical system|system]] into another set that also satisfies the Hamilton equations.

Mathematically, the transformation $q_{i}=u_{i}(\tilde{q},\tilde{p},t)$, $p_{i}=v_{i}(\tilde{q},\tilde{p},t)$ is canonical if for all [[Hamiltonian|Hamiltonians]] $H(q,p,t)$, there exists a function $K(\tilde{q},\tilde{p},t)$ such that, if the equations of motion in coordinates $(q,p)$ have the form of Hamilton equations ($\dot{p}_{i}=-\frac{ \partial H }{ \partial q_{i} }$ and $\dot{q}_{i}=\frac{ \partial H }{ \partial p_{i} }$), then the equations in $(\tilde{q},\tilde{p})$ also have the form of Hamilton equations, with $K$ as the Hamiltonian ($\dot{\tilde{p}}_{i}=-\frac{ \partial K }{ \partial \tilde{q}_{i} }$ and $\dot{\tilde{q}}_{i}=\frac{ \partial K }{ \partial \tilde{p}_{i} }$). The solutions are related by the functions $u$ and $v$ as $q_{i}(t)=u_{i}(\tilde{q}(t),\tilde{p}(t),t)$ and $p_{i}(t)=v_{i}(\tilde{q}(t),\tilde{p}(t),t)$. The Hamiltonians $H$ and $K$ are said to be **conjugate**.
### Canonicity criteria
Determining if a transformation is canonical can be arduous: you have to prove that it is canonical for *all* possible Hamiltonians, and there's infinite of them. Sometimes it's possible, such as in the examples below, but there is a better method to ensuring canonicity. For a transformation to be canonical, it must satisfy the so-called **canonicity criteria**.

Consider a generic coordinate transformation $x_{i}=w_{i}(\tilde{x},t)$. The inverse is $\tilde{x}=\tilde{w}_{i}(x,t)$. Motion in [[phase space]] is described by the either the functions $x_{i}(t)$ or $\tilde{x}_{i}(t)$, linked by the aforementioned equations as $x_{i}(t)=w(\tilde{x}(t),t)$ and $\tilde{x}_{i}(t)=\tilde{w}(x(t),t)$. The derivative is
$$\dot{\tilde{x}}_{i}=\sum_{j=1}^{n} \underbrace{ \frac{ \partial \tilde{w}_{i} }{ \partial x_{j} } }_{ \tilde{J}_{ij} } (x(t),t)\dot{x}_{j}(t)+\frac{ \partial \tilde{w} }{ \partial t } (x(t),t)$$
where $\tilde{J}$ is the [[Jacobian]] of $\tilde{w}$. If $\dot{x}_{j}=f_{j}(x,t)$, then
$$\dot{\tilde{x}}_{i}=\sum_{j=1}^{2n} \tilde{J}_{ij}(w(\tilde{x}(t),t),t)f_{j}(w(\tilde{x}(t),t),t)+\frac{ \partial \tilde{w} }{ \partial t } (w(\tilde{x}(t),t),t)$$
Let's say that $\dot{\mathbf{x}}=\mathrm{E}\nabla_{x}H$, with individual components $\dot{x}_{i}=\sum_{l}\mathrm{E}_{ij}\frac{ \partial H }{ \partial x_{l} }=f_{i}(x,t)$. Thus
$$\dot{\tilde{x}}_{i}=\sum_{j=1}^{2n} \tilde{J}_{ij}\sum_{l}\mathrm{E}_{il}\frac{ \partial H }{ \partial x_{l} } +\frac{ \partial \tilde{w}_{i} }{ \partial t } $$
In vector form, $\dot{\tilde{\mathbf{x}}}=\tilde{J}\mathrm{E}\nabla_{x}H+\frac{ \partial \tilde{\mathbf{w}} }{ \partial t }$. If the transformation is canonical, then this must also be equal to $\dot{\tilde{\mathbf{x}}}=\mathrm{E}\nabla_{\tilde{x}}K$. This provides a universal criterion for canonicity.

> [!info] Canonicity criterion
> A transformation is canonical if, for all $H(x,t)$, there exists a conjugate Hamiltonian $K(\tilde{x},t)$ such that
> $$\tilde{J}\mathrm{E}\nabla_{x}H+\frac{ \partial \tilde{w} }{ \partial t } =\mathrm{E}\nabla_{\tilde{x}}K$$
> In particular, we call $K_{0}$ the conjugate Hamiltonian when $H=0$, that is
> $$\mathrm{E}\nabla_{\tilde{x}}K_{0}=\frac{ \partial \tilde{w} }{ \partial t } $$

$$\mathrm{E}\nabla_{\tilde{x}}K=\tilde{J}\mathrm{E}\nabla_{x}H+\frac{ \partial \tilde{w} }{ \partial t } =\mathrm{E}^{-1}\mathrm{E}\tilde{J}\mathrm{E}\tilde{J}^{T}(\tilde{J}^{T})^{-1}\nabla_{x}H+\frac{ \partial \tilde{w} }{ \partial t }=\ldots$$
$$(\underbrace{ (\tilde{J}^{T})^{-1} }_{ =(\tilde{J}^{-1})^{T} }\nabla_{x}H)_{i}=\sum_{j}J_{ij}^{T}\frac{ \partial H }{ \partial x_{j} } =\sum_{j}J_{ji}\frac{ \partial H }{ \partial x_{j} } =\sum_{j}\frac{ \partial w_{j} }{ \partial \tilde{x}_{i} } \frac{ \partial H }{ \partial x_{j} } =\sum_{j}\frac{ \partial H }{ \partial x_{j} } \frac{ \partial w_{j} }{ \partial \tilde{x}_{i} } =\frac{ \partial \tilde{H} }{ \partial \tilde{x}_{i} } $$
where $\tilde{H}(\tilde{x},t)\equiv H(w(\tilde{x},t),t)$. Then
$$\ldots=-\mathrm{E}\mathrm{E}\tilde{J}\mathrm{E}\tilde{J}^{T}\nabla_{\tilde{x}}\tilde{H}+\mathrm{E}\nabla_{\tilde{x}}K_{0}$$
By applying $\mathrm{E}^{-1}$ on the left on both sides of the equation we get
$$-\mathrm{E}\tilde{J}\mathrm{E}\tilde{J}^{T}\nabla_{\tilde{x}}\tilde{H}=\nabla_{\tilde{x}}(K-K_{0})$$
This won't be proven here, but $-\mathrm{E}\tilde{J}\mathrm{E}\tilde{J}^{T}\nabla_{\tilde{x}}\tilde{H}$ is [[Vector field|irrotational]] for all $H$. Hence, we can write
$$-\mathrm{E}\tilde{J}\mathrm{E}\tilde{J}^{T}=c\mathrm{I}_{2n}$$
where $\mathrm{I}_{2n}$ is the $2n$-dimensional [[identity matrix]]. With one last substitution we state
$$c\nabla_{\tilde{x}}\tilde{H}=\nabla_{\tilde{x}}(K-K_{0})$$
and so
$$\boxed{K=c \tilde{H}+K_{0}}$$
If $c=1$, the transformation is said to be **univalent**.
### Examples
> [!example]
> Take this coordinate transformation:
> $$q=\frac{\tilde{p}}{m\omega}\sin \tilde{q},\quad p=\tilde{p}\cos \tilde{q}$$
> with Hamiltonian $H=p^{2}/2m$, that yields the equations of motion
> $$\begin{cases}
> \dot{p}=0 \\
> \dot{q}=p/m
> \end{cases}$$
> The derivatives of the transformation are
> $$\dot{q}=\frac{\dot{\tilde{p}}}{m\omega}\sin \tilde{q}+ \frac{\tilde{p}\dot{\tilde{q}}}{m\omega}\cos \tilde{q},\quad \dot{p}=\dot{\tilde{p}}\cos \tilde{q}-\tilde{p}\dot{\tilde{q}}\sin \tilde{q}$$
> If we plug this in the equations of motion we get
> $$\begin{cases}
> \dot{\tilde{p}}=\omega \tilde{p}\cos \tilde{q}\sin \tilde{q} \\
> \dot{\tilde{q}}=\omega \cos ^{2}\tilde{q}
> \end{cases}$$
> This is correct, but we have not proven if this is a canonical transformation or not. To do so, we need to check if these new equations of motions take the form of Hamilton equations for some Hamiltonian $K$:
> $$\begin{cases}
> \dot{\tilde{p}}=\omega \tilde{p}\cos \tilde{q}\sin \tilde{q}=?-\frac{ \partial K }{ \partial \tilde{q} }  \\
> \dot{\tilde{q}}=\omega \cos ^{2}\tilde{q}=?\frac{ \partial K }{ \partial \tilde{p} } 
> \end{cases}\tag{1}$$
> We need some property to verify that such a $K$ can exist. Since we're working with derivatives, we may as well use the [[Teorema di Schwarz]] as a check. The following must be true:
> $$\frac{ \partial  }{ \partial \tilde{p} } \frac{ \partial K }{ \partial \tilde{q} } =\frac{ \partial  }{ \partial \tilde{q} } \frac{ \partial K }{ \partial \tilde{p} } $$
> but doing the math with the values we are hoping for in $(1)$ leads to
> $$-\omega \cos \tilde{q}\sin \tilde{q}=-2\omega \cos \tilde{q}\sin \tilde{q}$$
> This is impossibile, so $K$ cannot exists. As such, this transformation is not canonical.

> [!example]
> Here's another transformation
> $$p_{i}=\alpha \tilde{p}_{i},\quad q_{i}=\beta \tilde{q}_{i}$$
> with derivatives
> $$\dot{p}_{i}=\alpha \dot{\tilde{p}}_{i},\quad \dot{q}_{i}=\beta \dot{\tilde{q}}_{i}$$
> In abstract, the equations of motion $\dot{p}_{i}=-\frac{ \partial H }{ \partial q_{i} }(q,p,t)$ and $\dot{q}_{i}=\frac{ \partial H }{ \partial p_{i} }(q,p,t)$ become
> $$\dot{\tilde{p}}_{i}=- \frac{1}{\alpha}\frac{ \partial H }{ \partial q_{i} } (\alpha \tilde{p},\beta \tilde{q},t),\quad \dot{\tilde{q}}_{i}=\frac{1}{\beta}\frac{ \partial H }{ \partial p_{i} } (\alpha \tilde{p},\beta \tilde{q},t)$$
> We can pretty readily see that these are equivalent to
> $$\dot{\tilde{p}}_{i}=-\frac{ \partial K }{ \partial q_{i} } (\tilde{p},\tilde{q},t),\quad \dot{\tilde{q}}_{i}=\frac{ \partial K }{ \partial p_{i} } (\tilde{p},\tilde{q},t)\qquad \text{for }K=\frac{1}{\alpha \beta}H(\alpha \tilde{p},\beta \tilde{q},t)$$
> Thus, this is a canonical transformation of conjugate Hamiltonian $K$.

> [!example]
> Consider the transformation $p_{i}=\tilde{p}_{i}$ and $q_{i}=\tilde{q}_{i}+\alpha t \tilde{p}_{i}$.
> $$K(\tilde{p},\tilde{q},t)=H(\tilde{p},\tilde{q}+\alpha t \tilde{p})- \frac{\alpha}{2}\tilde{\mathbf{p}}^{2}$$
> $$H(p,q)=\frac{\mathbf{p}^{2}}{2m}\quad\to \quad \dot{p}=0,\quad \dot{q}=\frac{p}{m}$$
> If $\alpha=1/m$, we have
> $$\tilde{K}=\frac{\tilde{\mathbf{p}}^{2}}{2m}- \frac{1/m}{2}\tilde{\mathbf{p}}^{2}=0\quad\to \quad \dot{\tilde{p}}=0,\quad \dot{\tilde{q}}=0$$
> So, in the modified coordinate systems, the equations of motion become trivial: $\tilde{p}$ and $\tilde{q}$ are just constants. Of course, the issue was getting here, i.e. knowing what transformation to do in the first place. (TODO: Fix this, 08/05/2025)

