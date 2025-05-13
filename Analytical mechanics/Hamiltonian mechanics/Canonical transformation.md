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
In vector form, $\dot{\tilde{\mathbf{x}}}=\tilde{J}\mathrm{E}\nabla_{x}H+\frac{ \partial \tilde{\mathbf{w}} }{ \partial t }$. If the transformation is canonical, then this must also be equal to $\dot{\tilde{\mathbf{x}}}=\mathrm{E}\nabla_{\tilde{x}}K$. This provides an initial criterion for canonicity[^1].

> [!info] Canonicity lemma
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
$$-\mathrm{E}\tilde{J}\mathrm{E}\tilde{J}^{T}=c\mathrm{I}_{2n}\tag{1}$$
where $\mathrm{I}_{2n}$ is the $2n$-dimensional [[identity matrix]]. With one last substitution we state
$$c\nabla_{\tilde{x}}\tilde{H}=\nabla_{\tilde{x}}(K-K_{0})$$
and so
$$\boxed{K=c \tilde{H}+K_{0}}\tag{2}$$
If $c=1$, the transformation is said to be **univalent**. This equation allows us to state another canonicity criterion.

> [!info] First canonicity criterion
> A transformation $x_{i}=w_{i}(\tilde{x},t)$ is canonical if and only if there exists some $c\neq 0$ such that $cJ\mathrm{E}J^{T}=\mathrm{E}$.
> 
> **Proof.** $(\Rightarrow)$ If the transformation is canonical, then the $c\neq 0$ must exist such that $\mathrm{E}=cJ\mathrm{E}\tilde{J}$. Using $(1)$ we can apply $\mathrm{E}$ to the right on both sides
> $$-\tilde{J}\mathrm{E}\tilde{J}\mathrm{E}\mathrm{E}=cI_{2n}\mathrm{E}\quad\Rightarrow \quad \tilde{J}\mathrm{E}\tilde{J}^{T}=c\mathrm{E}$$
> We now apply $J$ to the left and $J^{T}$ to the right on both sides
> $$J\tilde{J}\mathrm{E}\tilde{J}^{T}J^{T}=cJ\mathrm{E}J^{T}\quad\Rightarrow \quad \mathrm{E}=cJ\mathrm{E}\tilde{J}$$
> since $J\tilde{J}=\tilde{J}^{T}J^{T}=\mathrm{I}$.
> $(\Leftarrow)$ If $c\neq 0$ exists, then the transformation must be canonical, that is, for all $H$ there exists some $K$ such that $E\nabla_{\tilde{x}}K=\tilde{J}\mathrm{E}\nabla_{x}H+\frac{ \partial \tilde{ w} }{ \partial t }$ (the canoncity lemma). We already know that $\nabla_{x}H=\tilde{J}^{T}\nabla_{\tilde{x}}\tilde{H}$ so
> $$\tilde{J}\mathrm{E}\nabla_{x}H=\tilde{J}\mathrm{E}\tilde{J}^{T}\nabla_{\tilde{x}}\tilde{H}=c\mathrm{E}\nabla_{\tilde{x}}\tilde{H}$$
> With two lemmas, that won't be covered here, one can prove that if $K_{0}$ exists such that $\mathrm{E}\nabla_{\tilde{x}}K_{0}=\frac{ \partial \tilde{w} }{ \partial t }$, then there exists a $K$ such that the canonicity lemma is valid and thus the transformation is canonical.

Remember that $J$ is the Jacobian of the transformation. What the first canonicity criterion says is that if the Jacobian of the transformation is $cJ\mathrm{E}J^{T}=\mathrm{E}$, then it's canonical. But what does $cJ\mathrm{E}J^{T}=\mathrm{E}$ *mean*? Well, if you remove the $c$, you get $J\mathrm{E}J^{T}=\mathrm{E}$. As it happens, this is the definition of a [[Matrice simmetrica|symmetric matrix]], a set of [[matrix|matrices]] which form a [[group]] with useful properties. It would be nice if the criterion could simplify to "if the transformation's Jacobian is symmetric, then it's canonical". Alas, the $c$ makes things harder. Now, if $c=1$, then $J$ is certainly symmetric. But in general, we need to analyze things further.

If we take the [[determinant]] of $cJ\mathrm{E}J^{T}=\mathrm{E}$ we get $c^{2n}\det \mathrm{E}(\det J)^{2}=\det \mathrm{E}$ and so
$$c^{n}=\frac{1}{\lvert \det J \rvert }$$
Now take a *canonical* transformation with Jacobian $J'$. We have $cJ'\mathrm{E}J'^{T}=\mathrm{E}$ for some $c$. We compose it with the *canonical* transformation[^2] $x=\sqrt{ \lvert c \rvert }\ x'$, so $p=\sqrt{ \lvert c \rvert }\ p'$ and $q=\sqrt{ \lvert c \rvert }\ q'$. Our original transformation $w'(\tilde{x},t)$ now is $w(\tilde{x},t)=\sqrt{ \lvert c \rvert }\ w'(\tilde{x},t)$. It's Jacobian is
$$J_{ij}=\frac{ \partial w_{i} }{ \partial x_{j} } =\sqrt{ \lvert k \rvert  }\ \frac{ \partial w'_{i} }{ \partial x_{j} } =\sqrt{ \lvert c \rvert  }\ J'_{ij}$$
So
$$J\mathrm{E}J^{T}=\lvert c \rvert J'\mathrm{E}J'^{T}=\text{sgn}(c)cJ'\mathrm{E}J'^{T}=\text{sgn}(c)\mathrm{E}\quad\to \quad\begin{cases}
c>0\quad J\mathrm{E}J^{T}=\mathrm{E} \\
c<0\quad J\mathrm{E}J^{T}=-\mathrm{E}
\end{cases}$$
So, if $c>0$, the first canonicity criterion seems to hold. If $c<0$, we can compose the coordinates with
$$\mathbf{x}''=\begin{pmatrix}0 & \mathrm{I} \\ \mathrm{I} & 0\end{pmatrix}\mathbf{x}=\mathcal{I}\mathbf{x}$$
which leads to
$$J''\mathrm{E}J''^{T}=\mathcal{I}J\mathrm{E}J^{T}\mathcal{I}=-\mathcal{I}\mathrm{E}\mathcal{I}=\mathrm{E}$$
and so we go back to our canonicity criterion, up to a composition. In fact, this is fully general. We can *always* do this. What we just found is that we can always compose a generic canonical transformation with a specific canonical transformation such that the composition has $c=1$. In other words, all canonical transformations can be reduced down to univalent ones with the correct compositions. But recall our previous point: if $c=1$, the Jacobian is symmetric. Thus, the Jacobian of all univalent transformations is symmetric. These are such an important group of functions that they are found to be part of a specific set: all univalent canonical transformations are **symplectic transformations**, which are transformations whose Jacobian is a **[[symplectic matrix]]**.

> [!success] Symplectic transformations
> All canonical transformations can be reduced to symplectic ones (that is, univalent canonical ones) by composing them with other appropriate canonical transformations. 
### Poisson bracket preservation
A transformation $w$ is said to **preserve the [[Poisson brackets]]** if for all $f(x,t)$ and $g(x,t)$ we have
$$\{ f,g \}(w(\tilde{x},t),t)=\{ F,G \}(\tilde{x},t)$$
where $F(\tilde{x},t)\equiv f(w(\tilde{x},t),t)$ and $G(\tilde{x},t)\equiv g(w(\tilde{x},t),t)$ are the compositions of $f$ and $g$ with the transformation $w$.

The following characterizations are valid:

> [!info] Characterization
> The Poisson brackets are preserved for all $f$ and $g$ if and only if they are also preserved for the elementary functions $\mathrm{E}_{ij}=\{ w_{i},w_{j} \}$.
>
> **Proof.**
> $$\begin{align}
> \{ F,G \}&=\sum_{l,s}\frac{ \partial F }{ \partial \tilde{x}_{l} } \mathrm{E}_{ls}\frac{ \partial G }{ \partial \tilde{x}_{s} } =\sum_{l,s}\left( \sum_{i}\frac{ \partial f }{ \partial x_{i} } \frac{ \partial w_{i} }{ \partial \tilde{x}_{l} }  \right)\mathrm{E}_{ls}\left( \sum_{j}\frac{ \partial f }{ \partial x_{j} } \frac{ \partial w_{j} }{ \partial \tilde{x}_{s} }  \right)  \\
> &=\sum_{i,j}\frac{ \partial f }{ \partial x_{i} } \underbrace{ \left( \sum_{l,s}\frac{ \partial w_{i} }{ \partial \tilde{x}_{l} } \mathrm{E}_{ls}\frac{ \partial w_{j} }{ \partial \tilde{x}_{s} }  \right) }_{ \mathrm{E}_{ij} }\frac{ \partial g }{ \partial x_{j} } =\{ f,g \}
> \end{align}$$

> [!info] Characterization
> $x=w(\tilde{x,}t)$ preserves the Poisson brackets if and only its Jacobian is a symplectic matrix.
> 
> **Proof.**
> $$\{ w_{k},w_{l} \}=\sum_{i,j}\frac{ \partial w_{k} }{ \partial \tilde{x}_{i} } \mathrm{E}_{ij}\frac{ \partial w_{l} }{ \partial \tilde{x}_{j} } =\sum_{i,j}J_{ki}\mathrm{E}_{ij}J_{lj}=(J\mathrm{E}J^{T})_{kl}$$

> [!info] Second canonicity criterion
> A transformation $x=w(\tilde{x},t)$ is univalent canonical if and only if it preserves the Poisson brackets.
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

> [!example] Proving canonicity
> Let's prove that $p=\tilde{p}$, $q=\tilde{q}+\alpha t\tilde{p}$ is a canonical transformation. In compact form it is $x=w(\tilde{x},t)$ where $x_{1}=\tilde{x}_{1}$ and $x_{2}=\tilde{x}_{2}+\alpha t\tilde{x}_{1}$. We'll use the first canonicity criterion, so we need the Jacobian:
> $$J=\begin{pmatrix}1 & 0 \\ \alpha t & 1\end{pmatrix},\quad J^{T}=\begin{pmatrix}1 & \alpha t \\ 0 & 1\end{pmatrix}$$
> By the criterion we calculate
> $$J\mathrm{E}J^{T}=\begin{pmatrix}1 & 0 \\ \alpha t & 1\end{pmatrix}\begin{pmatrix}0 & -1 \\ 1 & 0\end{pmatrix}\begin{pmatrix}1 & \alpha t \\ 0 & 1\end{pmatrix}=\begin{pmatrix}0 & -1 \\ 1 & -\alpha t\end{pmatrix}\begin{pmatrix}1 & \alpha t \\ 0  &  1\end{pmatrix}=\begin{pmatrix}0 & -1 \\ 1 & 0\end{pmatrix}=\mathrm{E}$$
> So the transformation is not only canonical, but also univalent (since $c=1$). Thus, $w$ is a symplectic transformation.
> 
> We can also find this out by using the second canonicity criterion. We just need to prove that the Poisson brackets are preserved. The fundamental Poisson brackets are
> $$\{ \tilde{q}+\alpha t\tilde{p},\tilde{p} \}=\{ \tilde{q},\tilde{p} \}+\alpha t\cancel{ \{ \tilde{p},\tilde{p} \} }=1$$
> $$\{ \tilde{q}+\alpha t\tilde{p},\tilde{q}+\alpha t\tilde{p} \}=\cancel{ \{ \tilde{q},\tilde{q} \} }+\{ \tilde{q},\alpha t\tilde{p} \}+\{ \alpha t\tilde{p},\tilde{q} \}+\{ \alpha t\tilde{p},\alpha t\tilde{q} \}=0$$
> (TODO: Finish this, 13/05/2025 end of lesson)
> 
> According the first criterion, there exists some $K_{0}$ for which $K=cH+K_{0}$. We now that $K=\tilde{H}+K_{0}$. The condition is that $\mathrm{E}\nabla_{\tilde{x}}K_{0}=\frac{ \partial \tilde{w} }{ \partial t }$, which means $\nabla_{\tilde{x}}K_{0}=-\mathrm{E}\frac{ \partial \tilde{w} }{ \partial t }$. We can calculate $\frac{ \partial \tilde{w} }{ \partial t }$, so let's do that first:
> $$\frac{ \partial \tilde{w} }{ \partial t }=\begin{pmatrix}0 \\ -\alpha t\end{pmatrix}$$
> The gradient of $K_{0}$ must therefore be
> $$\nabla_{\tilde{x}}K_{0}=\begin{pmatrix}0 & -1 \\ 1 & 0\end{pmatrix}???$$
> (TODO: Finish this, 13/05/2025 towards the end)
> $$K_{0}=- \frac{\alpha \tilde{x}_{1}^{2}}{2}$$
> The modified Hamiltonian is
> $$K(\tilde{w},t)=H(w(\tilde{x},t),t)- \frac{\alpha \tilde{x}_{1}^{2}}{2}$$


[^1]: "Canonicity lemma" is a name I made up, but I haven't found any standard name for this proposition. Since it's used to prove the actual criteria, I chose to call it a lemma.

[^2]: It's canonical because any transformation like $p=\alpha \tilde{p}$, $q=\beta \tilde{q}$ is canonical. See the examples.
