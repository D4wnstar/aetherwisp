---
wiki-publish: true
aliases:
  - conjugate Hamiltonian
---
A **canonical transformation** is a [[coordinate transformation]] that transforms a set of [[canonical coordinates]] that satisfy the [[Hamilton equations|Hamilton equations]] into another set that also satisfies them. It is said that canonical transformations **preserve the form** of the Hamilton equations.

Mathematically, the transformation $q_{i}=u_{i}(\tilde{q},\tilde{p},t)$, $p_{i}=v_{i}(\tilde{q},\tilde{p},t)$ is canonical if for all [[Hamiltonian|Hamiltonians]] $H(q,p,t)$, there exists a function $K(\tilde{q},\tilde{p},t)$ called the **conjugate Hamiltonian** such that, if the equations of motion in coordinates $(q,p)$ obey the Hamilton equations
$$\dot{p}_{i}=-\frac{ \partial H }{ \partial q_{i} },\quad  \dot{q}_{i}=\frac{ \partial H }{ \partial p_{i} }$$
then the equations in $(\tilde{q},\tilde{p})$ also obey the Hamilton equations, with $K$ as the Hamiltonian:
$$\dot{\tilde{p}}_{i}=-\frac{ \partial K }{ \partial \tilde{q}_{i} },\quad\dot{\tilde{q}}_{i}=\frac{ \partial K }{ \partial \tilde{p}_{i} }$$
The solutions are related by the functions $u$ and $v$ as $q_{i}(t)=u_{i}(\tilde{q}(t),\tilde{p}(t),t)$ and $p_{i}(t)=v_{i}(\tilde{q}(t),\tilde{p}(t),t)$.
### Canonicity criteria
Determining if a transformation is canonical can be arduous: you have to prove that it is canonical for *all* possible Hamiltonians, and there's infinite of them. Sometimes this brute force way is a valid approach, such as in some of the examples below, but there is a better method to ensuring canonicity. For a transformation to be canonical, it must satisfy the so-called **canonicity criteria**.

Assume we're working for some [[dynamical system]] $\dot{\mathbf{x}}=f(\mathbf{x},t)$. Consider a generic coordinate transformation $x_{i}=w_{i}(\tilde{\mathbf{x}},t)$. The inverse is $\tilde{x}_{i}=\tilde{w}_{i}(\mathbf{x},t)$. Motion in [[phase space]] is described by either $x_{i}(t)$ or $\tilde{x}_{i}(t)$, linked by the aforementioned equations as $x_{i}(t)=w(\tilde{\mathbf{x}}(t),t)$ and $\tilde{x}_{i}(t)=\tilde{w}(\mathbf{x}(t),t)$. The [[Differential|total time derivative]] is
$$\dot{\tilde{x}}_{i}=\sum_{j=1}^{n} \underbrace{ \frac{ \partial \tilde{w}_{i} }{ \partial x_{j} } }_{ \tilde{J}_{ij} } (\mathbf{x}(t),t)\dot{x}_{j}(t)+\frac{ \partial \tilde{w} }{ \partial t } (\mathbf{x}(t),t)$$
where $\tilde{J}$ is the [[Jacobian]] of $\tilde{w}$. Since $\dot{x}_{j}=f_{j}(\mathbf{x},t)$, then
$$\dot{\tilde{x}}_{i}=\sum_{j=1}^{2n} \tilde{J}_{ij}(w(\tilde{\mathbf{x}}(t),t),t)f_{j}(w(\tilde{\mathbf{x}}(t),t),t)+\frac{ \partial \tilde{w} }{ \partial t } (w(\tilde{\mathbf{x}}(t),t),t)$$
There's a lot of function composition going on here. To avoid making the notation even more cluttered, we'll suppress the function argument in future steps. Still, you should remember that we're working with functions, not constants. The previous step becomes
$$\dot{\tilde{x}}_{i}=\sum_{j=1}^{2n} \tilde{J}_{ij}f_{j}+\frac{ \partial \tilde{w} }{ \partial t } $$
Let's say that our coordinates solve the Hamilton equations $\dot{\mathbf{x}}=\mathrm{E}\nabla_{\mathbf{x}}H=f(\mathbf{x},t)$, with individual components $\dot{x}_{i}=\sum_{l}\mathrm{E}_{il}\frac{ \partial H }{ \partial x_{l} }=f_{i}(\mathbf{x},t)$. Then,
$$\dot{\tilde{x}}_{i}=\sum_{j=1}^{2n} \tilde{J}_{ij}\sum_{l}\mathrm{E}_{il}\frac{ \partial H }{ \partial x_{l} } +\frac{ \partial \tilde{w}_{i} }{ \partial t } $$
Or in vector form,
$$\dot{\tilde{\mathbf{x}}}=\tilde{J}\mathrm{E}\nabla_{\mathbf{x}}H+\frac{ \partial \tilde{\mathbf{w}} }{ \partial t }$$
If the transformation is canonical, then this must also be equal to $\dot{\tilde{\mathbf{x}}}=\mathrm{E}\nabla_{\tilde{\mathbf{x}}}K$. This provides an initial criterion for canonicity[^1].

> [!info] Canonicity lemma
> A transformation is canonical if, for all $H(\mathbf{x},t)$, there exists a conjugate Hamiltonian $K(\tilde{\mathbf{x}},t)$ such that
> $$\tilde{J}\mathrm{E}\nabla_{\mathbf{x}}H+\frac{ \partial \tilde{\mathbf{w}} }{ \partial t } =\mathrm{E}\nabla_{\tilde{\mathbf{x}}}K$$
> In particular, we call $K_{0}$ the conjugate Hamiltonian when $H=0$, that is
> $$\frac{ \partial \tilde{\mathbf{w}} }{ \partial t }=\mathrm{E}\nabla_{\tilde{\mathbf{x}}}K_{0} $$

The issue now is that we don't really know what $K$ *is*. We'll start from $\mathrm{E}\nabla_{\mathbf{x}}K$ and see what we can do.
$$\mathrm{E}\nabla_{\tilde{\mathbf{x}}}K=\tilde{J}\mathrm{E}\nabla_{\mathbf{x}}H+\frac{ \partial \tilde{\mathbf{w}} }{ \partial t } =\tilde{J}\mathrm{E}\tilde{J}^{T}(\tilde{J}^{T})^{-1}\nabla_{\mathbf{x}}H+\mathrm{E}\nabla_{\tilde{\mathbf{x}}}K_{0}=\ldots$$
In the first step, we used the first part of the canonicity lemma. In the second, we used the second part of the lemma and we arbitrarily added $\tilde{J}^{T}(\tilde{J}^{T})^{-1}$ since a [[matrix]] multiplied by its [[Invertible matrix|inverse]] is the [[identity matrix]] and doesn't change anything. It's a weird step, but it allows us to use the following equality. First, notice that, since $\tilde{J}^{-1}=J$, $(\tilde{J}^{T})^{-1}=(\tilde{J}^{-1})^{T}=J^{T}$. Then
$$\begin{align}
((\tilde{J}^{T})^{-1} \nabla_{\mathbf{x}}H)_{i}&=\sum_{j}J_{ij}^{T}\frac{ \partial H }{ \partial x_{j} } \\
(\text{symmetric: }J^{T}_{ij}=J_{ji})&=\sum_{j}J_{ji}\frac{ \partial H }{ \partial x_{j} } \\
\left( \text{def: }J_{ij}=\frac{ \partial w_{j} }{ \partial \tilde{x}_{i} }  \right)&=\sum_{j}\frac{ \partial w_{j} }{ \partial \tilde{x}_{i} } \frac{ \partial H }{ \partial x_{j} } \\
(\text{def: }H(w(\tilde{x},t),t)\equiv\tilde{H}(\tilde{x},t))&=\frac{ \partial \tilde{H} }{ \partial \tilde{x}_{i} } 
\end{align}$$
The last step uses the [[chain rule]]. In vector form:
$$(\tilde{J}^{T})^{-1}\nabla_{\mathbf{x}}H=\nabla_{\tilde{\mathbf{x}}}\tilde{H}$$
The meaning of this is that we can use the Jacobian of the transformation to transform from the [[gradient]] in $\mathbf{x}$ of $H$ to the one in $\tilde{\mathbf{x}}$ of $\tilde{H}$ (basically, we use the derivatives of the transformation to transform the *gradient's* coordinates). Plugging this into our previous equation yields
$$\begin{align}
\ldots&=\tilde{J}\mathrm{E}\tilde{J}^{T}\nabla_{\tilde{\mathbf{x}}}\tilde{H}+\mathrm{E}\nabla_{\tilde{\mathbf{x}}}K_{0} \\
\end{align}$$
We can see that we have a gradient of $K$ and of $K_{0}$. We can move the one with $K_{0}$ on the other side to get
$$\tilde{J}\mathrm{E}\tilde{J}^{T}\nabla_{\tilde{\mathbf{x}}}\tilde{H}=\mathrm{E}\nabla_{\tilde{\mathbf{x}}}(K-K_{0})$$
By applying $\mathrm{E}^{-1}=-\mathrm{E}$ on the left on both sides of the equation we get
$$-\mathrm{E}\tilde{J}\mathrm{E}\tilde{J}^{T}\nabla_{\tilde{\mathbf{x}}}\tilde{H}=\nabla_{\tilde{\mathbf{x}}}(K-K_{0})$$
The [[vector field]] $-\mathrm{E}\tilde{J}\mathrm{E}\tilde{J}^{T}\nabla_{\tilde{\mathbf{x}}}\tilde{H}$ is [[Vector field|irrotational]] for all $\tilde{H}$. This is because it is equal to a gradient, and the [[curl]] of a gradient is always zero. This means that there exists some [[potential]] whose gradient is the field itself. This won't be proven here, but knowing this, we can write
$$-\mathrm{E}\tilde{J}\mathrm{E}\tilde{J}^{T}=c\mathrm{I}_{2n}\tag{1}$$
where $\mathrm{I}_{2n}$ is the $2n$-dimensional [[identity matrix]] and $c$ is some real constant. With one last substitution we see
$$c\nabla_{\tilde{\mathbf{x}}}\tilde{H}=\nabla_{\tilde{\mathbf{x}}}(K-K_{0})$$
and so, matching the gradient arguments and rearranging:
$$\boxed{K=c \tilde{H}+K_{0}}\tag{2}$$
This is the *general* shape of the conjugate Hamiltonian. In the special case where $c=1$, the transformation is said to be **univalent**. This equation allows us to state another canonicity criterion.

> [!info] First canonicity criterion
> A transformation $\mathbf{x}=\mathbf{w}(\tilde{\mathbf{x}},t)$ is **canonical** if and only if there exists some $c\neq 0$ for which its Jacobian $J$ satisfies $cJ\mathrm{E}J^{T}=\mathrm{E}$. If $c=1$, the transformation is **univalent canonical** and its Jacobian is [[Symplectic matrix|symplectic]].

> [!quote]- Proof
> $(\Rightarrow)$ If the transformation is canonical, the $c\neq 0$ must exist such that $cJ\mathrm{E}\tilde{J}=\mathrm{E}$. Starting from $(1)$ we can apply $\mathrm{E}$ to the right on both sides
> $$-\tilde{J}\mathrm{E}\tilde{J}\mathrm{E}\mathrm{E}=c\mathrm{I}_{2n}\mathrm{E}\quad\Rightarrow \quad \tilde{J}\mathrm{E}\tilde{J}^{T}=c\mathrm{E}$$
> We now apply $J$ to the left and $J^{T}$ to the right on both sides
> $$J\tilde{J}\mathrm{E}\tilde{J}^{T}J^{T}=cJ\mathrm{E}J^{T}\quad\Rightarrow \quad \mathrm{E}=cJ\mathrm{E}\tilde{J}$$
> since $J=\tilde{J}^{-1}$ and so $J\tilde{J}=\tilde{J}^{T}J^{T}=\mathrm{I}_{2n}$.
> 
> $(\Leftarrow)$ If $c\neq 0$ exists, then the transformation must be canonical, that is, for all $H$ there exists some $K$ such that $E\nabla_{\tilde{\mathbf{x}}}K=\tilde{J}\mathrm{E}\nabla_{\mathbf{x}}H+\frac{ \partial \tilde{ \mathbf{w}} }{ \partial t }$ (part 1 of canonicity lemma). We already know that $\nabla_{\mathbf{x}}H=\tilde{J}^{T}\nabla_{\tilde{\mathbf{x}}}\tilde{H}$ so
> $$\tilde{J}\mathrm{E}\nabla_{\mathbf{x}}H=\tilde{J}\mathrm{E}\tilde{J}^{T}\nabla_{\tilde{\mathbf{x}}}\tilde{H}=c\mathrm{E}\nabla_{\tilde{\mathbf{x}}}\tilde{H}$$
> With two more lemmas that won't be covered here, one can prove that if $K_{0}$ exists such that $\mathrm{E}\nabla_{\tilde{\mathbf{x}}}K_{0}=\frac{ \partial \tilde{\mathbf{w}} }{ \partial t }$ (part 2 of canonicity lemma), then there exists a $K$ such that the canonicity lemma is valid and thus the transformation is canonical.

We should stop for a moment to think about this result. What does $cJ\mathrm{E}J^{T}=\mathrm{E}$ *mean*? Well, if you set $c=1$, you get $J\mathrm{E}J^{T}=\mathrm{E}$. This is the definition of a [[symplectic matrix]], a set of [[matrix|matrices]] which form a [[group]] with useful properties that is *very* important in Hamiltonian mechanics[^2]. Unfortunately, the $c$ makes things harder. In general, we need to analyze things further. Spoilers: while $J$ may not be symplectic when $c\neq 1$, everything else regarding Hamilton's equations stays the same (up to some scaling).

If we take the [[determinant]] of $cJ\mathrm{E}J^{T}=\mathrm{E}$, remember that $\det(\mathrm{A}\mathrm{B})=\det \mathrm{A}\det \mathrm{B}$ and that $\det \mathrm{E}=1$, we get $c^{2n}(\det J)^{2}=1$ and so
$$\boxed{c^{n}=\frac{1}{\lvert \det J \rvert }}\tag{3}$$
Now take a *canonical* transformation $w'(\tilde{\mathbf{x}},t)$ of Jacobian $J'$. We have $cJ'\mathrm{E}J'^{T}=\mathrm{E}$ for some $c$. We compose it with the *canonical* transformation[^3] $\mathbf{x}=\sqrt{ \lvert c \rvert }\ \mathbf{x}'$. Our original transformation $w'(\tilde{\mathbf{x}},t)$ now becomes $w(\tilde{\mathbf{x}},t)=\sqrt{ \lvert c \rvert }\ w'(\tilde{\mathbf{x}},t)$. Its Jacobian is
$$J_{ij}=\frac{ \partial w_{i} }{ \partial x_{j} } =\sqrt{ \lvert c \rvert  }\ \frac{ \partial w'_{i} }{ \partial x_{j} } =\sqrt{ \lvert c \rvert  }\ J'_{ij}$$
So
$$J\mathrm{E}J^{T}=\lvert c \rvert J'\mathrm{E}J'^{T}=\text{sign}(c)cJ'\mathrm{E}J'^{T}=\text{sign}(c)\mathrm{E}\quad\to \quad\begin{cases}
c>0\quad J\mathrm{E}J^{T}=\mathrm{E} \\
c<0\quad J\mathrm{E}J^{T}=-\mathrm{E}
\end{cases}$$
So, if $c>0$, the first canonicity criterion seems to hold. If $c<0$, we can compose the coordinates with
$$\mathbf{x}''=\begin{pmatrix}0 & \mathrm{I} \\ \mathrm{I} & 0\end{pmatrix}\mathbf{x}=\mathcal{I}\mathbf{x}$$
which leads to
$$J''\mathrm{E}J''^{T}=\mathcal{I}J\mathrm{E}J^{T}\mathcal{I}=-\mathcal{I}\mathrm{E}\mathcal{I}=\mathrm{E}$$
and so we go back to our canonicity criterion, up to a composition. In fact, this is fully general. We can *always* do this. What we just found is that we can always compose a generic canonical transformation with a specific canonical transformation such that the composition has $c=1$. In other words, all canonical transformations can be reduced to univalent ones, provided we figure out the correct compositions.

Univalent transformations are such an important group of functions that a lot of study has gone into them. Most importantly, they are a part of a more general set of transformations called **[[symplectic transformation|symplectic transformations]]**, which are all the transformations whose Jacobian is symplectic. Since by the first canonicity criterion all univalent canonical transformations have a symplectic Jacobian, they are automatically all symplectic transformations.

> [!success] Symplectic transformations
> A canonical transformation can always be reduced to a symplectic one by composing it with a different, appropriate canonical transformation. 

As a bonus property, note $(3)$. Since $c=1$ for all univalent transformations, then $\lvert \det J \rvert=1$ for them too. This is sometimes important, since $\lvert \det J \rvert$ appears when doing coordinate changes inside of integrals. For a relevant example, see for instance [[Liouville's theorem#Proof (analytical mechanics)]].
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
### Infinitesimal transformations
An interesting case is that of **infinitesimal transformations**, which are
$$\begin{cases}
\tilde{q}_{i}=q_{i}+\delta q_{i} \\
\tilde{p}_{i}=p_{i}+\delta p_{i}
\end{cases}$$
where $\delta q_{i}$ and $\delta p_{i}$ are intended as "small" compared to the rest of the coordinates. Alternatively, in compact form, $\tilde{x}_{j}=x_{j}+\delta x_{j}(x,t)$. We want to see if these are canonical. For that to be true, $\delta x_{j}$ needs to satisfy the fundamental Poisson brackets
$$\mathrm{E}_{ij}=\{ \tilde{w}_{i},\tilde{w}_{j} \}=\{ x_{i}+\delta x_{i},x_{j}+\delta x_{j} \}=\underbrace{ \{ x_{i},x_{j} \} }_{ \mathrm{E}_{ij} }+\{ x_{i},\delta x_{j} \}+\{ \delta x_{i},x_{j} \}+\{ \delta x_{i},\delta x_{j} \}$$
(TODO: Finish this, end of lesson 14/05/2025)

$$\begin{cases}
\delta p_{k}=-\varepsilon \frac{ \partial G }{ \partial q_{k} }  \\
\delta q_{k}=\varepsilon \frac{ \partial G }{ \partial p_{k} } 
\end{cases}$$
The function $G(x,t)$ is known as the **generator** of the infinitesimal canonical transformation. We can use the Poisson brackets on the generator to determine the infinitesimal transformation:
$$\boxed{\delta x_{i}=\varepsilon \{ x_{i},G \}=\varepsilon \mathrm{E}\nabla_{x}G}$$
This is also true for functions of dynamical variables, not just simple dynamical variables:
$$\delta f=f(x+\delta x)-f(x)=\varepsilon \{ f,G \}$$
#### Infinitesimal Hamiltonian transformations
The above results universally work for all dynamical variable. Arguably the most important dynamical variable is the Hamiltonian itself, $H(x,t)$. Let's consider a canonical transformation that is *independent* of $t$ generated by some generator $G(x)$. As per the above, the variation of $H$ is
$$\delta H=\epsilon \{ H,G \}$$
Clearly then, if $\{ H,G \}=0$, the Hamiltonian does not change and $G$ is a [[constant of motion]]. This is essentially the proof of the Hamiltonian version of [[Nöther's theorem]].

We can analyze what happens to the variation of $H$ during a time-independent coordinate change:
$$\delta H=H(x+\delta x)-H(x)=H(\tilde{x})-\tilde{H}(\tilde{x})=H(\tilde{x})-K(\tilde{x})$$
where $x+\delta x=\tilde{x}$ and in the last step we used the time independence. If the transformation is instead dependent on $t$, we have
$$\delta H=H(\tilde{x})-K(\tilde{x})=H(\tilde{x})-\tilde{H}(\tilde{x})-K_{0}(\tilde{x})=\underbrace{ H(x+\delta x)-H(x) }_{ \varepsilon \{ H,G \} }-K_{0}(\tilde{x})\tag{4}$$
Recalling that
$$\mathrm{E}\nabla_{\tilde{x}}K_{0}=\frac{ \partial \tilde{ w} }{ \partial t }(w(\tilde{x},t),t)=\frac{ \partial  }{ \partial t } (x+\delta x(x,t))=\frac{ \partial \delta x }{ \partial t } =\frac{ \partial  }{ \partial t } \varepsilon \mathrm{E}\nabla_{x}G(x,t)=\mathrm{E}\nabla_{x}\left( \varepsilon \frac{ \partial G }{ \partial t }  \right)$$
The last term in the brackets is a function of $x$ and $t$. We will define
$$\Lambda(\tilde{x},t)\equiv \varepsilon \frac{ \partial G }{ \partial t } (\tilde{x}-\delta x,t)$$
The (components of the) [[gradient]] of this function are
$$\frac{ \partial }{ \partial \tilde{x}_{j} } \Lambda=\sum_{i}\varepsilon \frac{ \partial ^{2}G }{ \partial x_{i}\partial t }(\tilde{x}-\delta x,t) \frac{ \partial \tilde{x}_{i}+\delta x_{i} }{ \partial \tilde{x}_{j} } =\frac{ \partial  }{ \partial x_{j} } \left( \varepsilon \frac{ \partial G }{ \partial t }  \right)(\tilde{x}-\delta x,t)$$
But this is just the last term of the previous equation:
$$\nabla_{x}\left( \varepsilon \frac{ \partial G }{ \partial t } \right)=\nabla_{\tilde{x}}\Lambda$$
so
$$\mathrm{E}\nabla_{\tilde{x}}K_{0}=\mathrm{E}\nabla_{\tilde{x}}\Lambda$$
and thus
$$K_{0}(\tilde{x})=\Lambda(\tilde{x})=\varepsilon \frac{ \partial G }{ \partial t } $$
Substituting this back in $(4)$ yields
$$\delta H=\varepsilon \left( \{ H,G \}- \frac{ \partial G }{ \partial t }  \right)$$
#### Finite transformation from a differential equation
Consider a usual, finite transformation $\tilde{x}=\tilde{w}(x,t)$. If expand it in a [[Taylor series|Taylor series]] as
$$\tilde{x}(\varepsilon)=\tilde{w}(x,t,\varepsilon)\simeq x+ \underbrace{ \varepsilon \frac{d\tilde{w}}{d\varepsilon}(x,t,0) }_{ \delta x }+\ldots$$
If $\varepsilon \ll1$, the transformation becomes infinitesimal, $\delta x$, that is, there exists some generator $G$ for which $\delta x=\varepsilon \{ x,G \}=\varepsilon \mathrm{E}\nabla_{x}G$. Dividing through by $\varepsilon$ gives us
$$\frac{\tilde{x}-x}{\varepsilon}=\mathrm{E}\nabla_{x}G\quad\to \quad \frac{d\tilde{x}}{d\varepsilon}(0)=\mathrm{E}\nabla_{x}G(\tilde{x}(0),t)\quad\to \quad \frac{d\tilde{x}}{d\varepsilon}(\varepsilon)=\mathrm{E}\nabla_{x}G(\tilde{x}(\varepsilon),t)$$
Thus, we found a differential equation to determine $\tilde{x}$ through the generator $G$. This can be solved by integration. But notice that this differential equation is actually a Hamilton equation, where $G$ is the Hamiltonian and $\varepsilon$ is time. We found this equation when using the Hamiltonian flux, and in fact, here it's $\tilde{x}(\varepsilon)$ that takes on the role of the flux. Specifically, it is the flux generated by the Hamiltonian $G$. In conclusion:

> [!success] Result
> The Hamiltonian is the generator of time shifts.
#### Infinitesimal rotations
[[rotation|Rotations]] are a particularly important and ubiquitous kind of transformation. Infinitesimal rotations specifically appear quite a few times in analytical mechanics. It's fair to ask if the infinitesimal rotations are also canonical transformations. To prove if they are, let's start with some rotation
$$R(\alpha)=\mathrm{I}+\Omega(\alpha)$$
where $R(\alpha)\in SO(3)$ is a rotation on the $\hat{\omega}$ axis of angle $\alpha$, $\mathrm{I}$ is the [[identity matrix]] and $\Omega(\alpha)$ is the infinitesimal rotation defined by its components as
$$\Omega(\alpha)_{ij}=-\alpha \sum_{k}\epsilon_{ijk}\hat{\omega}_{k}$$
where $\epsilon_{ijk}$ is the [[Tensore di Levi-Civita|Levi-Civita tensor]]. The angular speed is $\boldsymbol{\omega}=\alpha\hat{\omega}$. We want to see how this rotation affects coordinates and momentum.
$$\tilde{p}_{j}=\sum_{k}R_{jk}p_{k},\quad \tilde{q}_{i}=\sum_{m}R_{im}q_{m}$$
We'll look at the fundamental Poisson brackets:
$$\{ \tilde{p}_{j},\tilde{p}_{l} \}=\sum_{k,s}R_{jk}R_{ls}\underbrace{ \{ p_{k},p_{s} \} }_{ 0 }=0$$
$$\{ \tilde{q}_{j},\tilde{q}_{l} \}=0$$
$$\{ \tilde{q}_{i},\tilde{p}_{j} \}=\sum_{k,m}R_{im}R_{jk}\underbrace{ \{ q_{m},p_{k} \} }_{ \delta_{mk} }=\sum_{k}R_{ik}R_{jk}=\sum_{k}R_{ik}R_{kj}^{T}=(\underbrace{ RR^{T} }_{ \mathrm{I} })_{ij}=\delta_{ij}$$


$$\delta \mathbf{p}=\{ \mathbf{p},\alpha\hat{\omega}\cdot \mathbf{M} \}$$
On the $i$-th axis we get
$$\begin{align}
\{ p_{i},\alpha \hat{\omega}\cdot \mathbf{M} \}&=\left\{  p_{i},\alpha \sum_{j}\hat{\omega}_{j}M_{j}  \right\}=\alpha \sum_{j}\hat{\omega}_{j}\{ p_{i},M_{j} \}=\alpha \sum_{j}\hat{\omega}_{j}\sum_{k}\epsilon_{ijk}p_{k} \\
&=\sum_{k}\left( -\alpha \sum_{j}\epsilon_{ikj}\hat{\omega}_{j} \right)p_{j}=\sum_{k}\Omega(\alpha)_{ij}p_{k}
\end{align}$$
Let's consider a function $f(\mathbf{p},\mathbf{q})$ that is invariant under rotation, that is, $f(R\mathbf{p},R\mathbf{q})=f(\mathbf{p},\mathbf{q})$. In this case, we can write
$$f(\mathbf{p},\mathbf{q})=g(\lvert \mathbf{p} \rvert ^{2},\lvert \mathbf{q} \rvert ^{2},\mathbf{p}\cdot \mathbf{q})$$
This is because $\lvert \mathbf{p} \rvert^{2}$, $\lvert \mathbf{q} \rvert^{2}$ and $\mathbf{p}\cdot \mathbf{q}$ are all invariant under rotation, therefore for $f$ to be invariant, it must exclusively depend on these. In fact,
$$\{ M_{k},\lvert \mathbf{p} \rvert ^{2} \}=\sum_{i}\{ M_{i},p_{i}^{2} \}=\sum_{i}2p_{i}\{ M_{i},p_{i} \}=\sum_{i,j}2\epsilon_{kij}p_{j}p_{i}=0$$
since $\epsilon_{kij}$ is antisymmetric and $p_{j}p_{i}$ is symmetric. Similarly for $\lvert \mathbf{q} \rvert^{2}$. Then
$$\begin{align}
\{ M_{k},\mathbf{p}\cdot \mathbf{q} \}&=\sum_{i}\{ M_{k},p_{i}q_{i} \}=\sum_{i}(p_{i}\{ M_{k},q_{i} \}+\{ M_{k},p_{i} \}q_{i}) \\
&=\sum_{i,j}(\epsilon_{kij}q_{j}p_{i}+\epsilon_{kij}p_{i}q_{j})=\sum_{i,j}\epsilon_{kij}(q_{j}p_{i}+p_{i}q_{j})=0
\end{align}$$
because again, $e_{kij}$ is antisymmetric and the term in brackets is symmetric. As further confirmation, we can prove that $f$ is invariant by calculating the Poisson brackets directly:
$$\begin{align}
\{ M_{k},f \}&=\sum_{i}\left( \frac{ \partial M_{k} }{ \partial q_{i} } \frac{ \partial f }{ \partial p_{i} } -\frac{ \partial M_{k} }{ \partial p_{i} } \frac{ \partial f }{ \partial q_{i} }  \right) \\
&=\sum_{i}\left( \frac{ \partial M_{k} }{ \partial q_{i} } \sum_{j=1}^{3}\frac{ \partial g }{ \partial \alpha_{j} } \frac{ \partial \alpha_{j} }{ \partial p_{i} } -\frac{ \partial M_{k} }{ \partial p_{i} } \sum_{j=1}^{3} \frac{ \partial g }{ \partial \alpha_{j} } \frac{ \partial \alpha_{j} }{ \partial q_{i} }  \right) \\
&=\sum_{j=1}^{3} \frac{ \partial g }{ \partial \alpha_{j} } \underbrace{ \sum_{i}\left( \frac{ \partial M_{k} }{ \partial q_{i} } \frac{ \partial \alpha_{j} }{ \partial p_{i} } -\frac{ \partial M_{k} }{ \partial p_{i} } \frac{ \partial \alpha_{j} }{ \partial q_{i} }  \right) }_{ \{ M_{k},\alpha_{j} \}=0 } \\
&=0
\end{align}$$
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

[^2]: So important in fact that the entire field of symplectic geometry spawned as a consequence of the development of Hamiltonian mechanics.

[^3]: It's canonical because any transformation like $\mathbf{p}=\alpha \tilde{\mathbf{p}}$, $\mathbf{q}=\beta \tilde{\mathbf{q}}$ is canonical, and this one is $\mathbf{p}=\sqrt{ \lvert c \rvert }\ \mathbf{p}'$ and $\mathbf{q}=\sqrt{ \lvert c \rvert }\ \mathbf{q}'$. See the examples.
