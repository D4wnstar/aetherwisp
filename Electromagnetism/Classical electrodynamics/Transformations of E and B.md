---
wiki-publish: true
---
Within the context of relativity and through the knowledge that the [[electric field]] $\mathbf{E}$ and the [[magnetic field]] $\mathbf{B}$ are interrelated, it is fair to ask how these two transform due to relativity, specifically under a [[Lorentz transformation]]. To start,  we need to lay the groundwork, which is to say we need to make some assumptions about how this *might* work and then check if it's true (experimentally or theoretically). We need to claim two things:
1. the [[electric charge]] is a [[relativistic invariant]]. It does not change under Lorentz transformation. A charge is a charge everywhere and anywhere.
2. the sources are independent on the fields themselves. It does not matter how a field was created: stationary charge, straight moving charge, random motion in the core of the Sun, spinning particles in a cyclotron; it makes no difference. All fields transform the same.

Say now our Lorentz transformation has us move the [[frame of reference]] $\mathcal{S}$ on the $x$ axis at a *constant* speed $v$ (important! The frame needs to be inertial). We'll call the moved frame $\tilde{\mathcal{S}}$, and in general we'll use the tilde to refer to quantities measured in this frame. In this case, the components change as follow:
$$\begin{align}
\tilde{E}_{x}=E_{x},\quad \tilde{E}_{y}&=\gamma(E_{y}-vB_{z}),\quad \tilde{E}_{z}=\gamma(E_{z}+vB_{y}) \\
\tilde{B}_{x}=B_{x},\quad \tilde{B}_{y}&=\gamma\left( B_{y}+ \frac{v}{c^{2}}E_{z} \right),\quad \tilde{B}_{z}=\gamma\left( B_{z}- \frac{v}{c^{2}}E_{y} \right)
\end{align}\tag{1}$$
Interestingly, even we observe *no* fields at a given point in $\mathcal{S}$ ($\mathbf{E}=0$ and $\mathbf{B}=0$ in $\mathcal{S}$ specifically), we *still* observe something at that same point in $\tilde{\mathcal{S}}$:
$$\tilde{\mathbf{E}}=\mathbf{v}\times \tilde{\mathbf{B}},\quad \tilde{\mathbf{B}}=- \frac{1}{c^{2}}(\mathbf{v}\times \tilde{\mathbf{E}})$$
This is prime relativity: the fields "exist" for one person but not for another.
### The field and dual tensor
It's quite evident from the formulas in $(1)$ that when you move from one frame to another, the fields don't just change on their own: the mix. As such, we can't just describe them as (the spatial parts of) plain old [[Four-vector|four-vectors]] which transform in the usual manner like we can with, say, [[Linear momentum|momentum]]. We need some way of considering them together, as a single joint object to which to apply a transformation to. Well, we already did something similar in the past. When we wanted to represent the action of the electromagnetic field as a single object, we made a *[[tensor]]*, specifically, the [[Maxwell stress tensor]]. Here, we follow that advice: the object we're looking for is an antisymmetric, second order tensor (essentially a fancy name for an [[Symmetric matrix|antisymmetric matrix]]). But we are not working in 3D anymore, we're in [[spacetime]]! So this tensor is going to need to be $4\times4$.

Let's start from a four-vector. Such a vector, call it $a^{\mu}$, changes in relativity using a simple Lorentz transformation $\Lambda$:
$$a^{\mu}=\Lambda_{\nu}^{\mu}a^{\nu}$$
(using [[Einstein notation]]). In case of constant-speed movement over the $x$ axis,
$$\Lambda=\begin{pmatrix}
\gamma & -\gamma \beta & 0 & 0 \\
-\gamma \beta & \gamma & 0 & 0 \\
 0 & 0 & 1 & 0 \\
 0 & 0 & 0 & 1
\end{pmatrix}$$
A tensor, call it $t$, has two indexes and will need two transformations, one for each index:
$$t^{\mu \nu}=\Lambda_{\lambda}^{\mu}\Lambda_{\sigma}^{\nu}t^{\lambda \sigma}$$
Before we claimed we wanted our tensor to be antisymmetric. This just means that $t^{\mu \nu}=-t^{\nu \mu}$, which is the same as saying that the diagonal is just zeros and that the off-diagonals are mirrored across the diagonal, with their sign flipped. In order to justify our claim that the tensor we want needs to be antisymmetric, we can derive what the transformation rule above becomes if $t^{\mu \nu}$ is antisymmetric. (TODO: Work out the stuff). Using a tilde to denote the transformed tensor, these come up to be
$$\begin{align}
\tilde{t}^{01}=t^{01},\quad \tilde{t}^{02}&=\gamma(t^{02}-\beta t^{12}),\quad \tilde{t}^{03}=\gamma(t^{03}+\beta t^{31}) \\
\tilde{t}^{23}=t^{23},\quad \tilde{t}^{31}&=\gamma(t^{31}+\beta t^{03}),\quad \tilde{t}^{12}=\gamma(t^{12}-\beta t^{02})
\end{align}\tag{2}$$
The lettering might be a little different, but this is precisely $(1)$. If we just go ahead and change the symbols back to the physical one by substituting the first line of $(1)$ with the first of $(2)$ (and the second with the second), we can construct the tensor we were looking for:
$$\boxed{F^{\mu \nu}\equiv \begin{pmatrix}
0 & E_{x}/c & E_{y}/c & E_{z}/c \\
-E_{x}/c & 0 & B_{z} & -B_{y} \\
-E_{y}/c & -B_{z} & 0 & B_{x} \\
-E_{z}/c & B_{y} & -B_{x} & 0
\end{pmatrix}}$$
This tensor is known as the **[[field tensor]]**, and it describes the behavior of the electromagnetic field even across relativistic transformations. But if you look closely, it's not the *only* one. In fact, we can write another tensor but replacing the first line of $(1)$ with the *second* of $(2)$ and viceversa. After all, we just need to flip a sign. Doing so leads to
$$\boxed{G^{\mu \nu}\equiv \begin{pmatrix}
0 & B_{x} & B_{y} & B_{z} \\
-B_{x} & 0 & -E_{z}/c & -E_{y}/c \\
-B_{y} & E_{z}/c & 0 & -E_{x}/c \\
-B_{z} & -E_{y}/c & E_{x}/c & 0
\end{pmatrix}}$$
This alternative tensor is known as the **[[dual tensor]]** and it describes much the same thing as field tensor. In fact, you can get $G$ from $F$ but substituting $\mathbf{E}/c\to \mathbf{B}$ and $\mathbf{B}\to-\mathbf{E}/c$.
#### Electrodynamics through tensors
For now, we've derived what in principle are the most universal description of the fields possible[^1], but before we can claim victory, we need to make them *do something*. In other words, we need to rewrite the fundamental equations of electromagnetism in the language of the tensors. Specifically, our targets are [[Maxwell's equations]] and the [[Lorentz force]] law.

To start, consider some arbitrarily shaped electric charge $\rho$ moving at some velocity $\mathbf{u}$. For the sake of generality, we focus only on an infinitesimal volume of charge $V$ containing total charge $Q$, so that the density is $Q/V$, but for the sake of simplicity we assume that $\rho$ only contains charges of the same sign (if it contained both, the argument is the same but we'd have to have both a positive and negative term). The [[electric current|current]] density is $\mathbf{J}=\rho \mathbf{u}$.

As with all things moving in relativity, the distance traveled by $\rho$ is relative. In fact, the very spatial extent of $\rho$ is relative due to [[distance contraction]]. We'll call $\rho_{0}$ the **proper charge density**, which is the density in the rest frame of the charge. There, its volume is $V_{0}$ and so $\rho_{0}=Q/V_{0}$ (charge is invariant!). But we can go further: only one dimension is contracted (the one the charge is moving on, i.e. the direction of $\mathbf{u}$), so we can readily write the transformation rule:
$$V=\sqrt{ 1-u^{2}/c^{2} }\ V_{0}$$
and thus
$$\rho=\frac{\rho_{0}}{\sqrt{ 1-u^{2}/c^{2} }},\quad \mathbf{J}=\rho_{0} \frac{\mathbf{u}}{\sqrt{ 1-u^{2}/c^{2} }}$$
Maybe unsurprisingly, we are then justified in extending $\mathbf{J}=\rho \mathbf{u}$ to a four-vector by invoking the [[proper velocity]]:
$$\boxed{J^{\mu}=\rho_{0}\eta^{\mu}=(c\rho,J_{x},J_{y},J_{z})}\tag{3}$$
This is known as the **current density four-vector**. Now that we have relativistic $J$, we can convert the [[Electric current|continuity equation]] too. Starting from
$$\nabla\cdot \mathbf{J}=-\frac{ \partial \rho }{ \partial t } $$
we can exploit the definition of [[divergence]] to compress it to tensor form:
$$\nabla\cdot \mathbf{J}=\sum_{i=1}^{3} \frac{ \partial J^{i} }{ \partial x^{i} } $$
 But by looking at $(3)$ we can pretty readily see
 $$\frac{ \partial \rho }{ \partial t } =\frac{1}{c}\frac{ \partial J^{0} }{ \partial t } =\frac{ \partial J^{0} }{ \partial x^{0} } $$
 As it happens, the continuity equation is just the sum of all the [[partial derivative|partial derivatives]] of $J^{\mu}$ set to zero:
 $$\boxed{\frac{ \partial J^{\mu} }{ \partial x^{\mu} } =0}\tag{4}$$
 This is the **relativistic continuity equation for electric charge** (with summation implied). In a similar vein, the **relativistic Maxwell's equations** are
$$\boxed{\frac{ \partial F^{\mu \nu} }{ \partial x^{\nu} } =\mu_{0}J^{\mu},\quad \frac{ \partial G^{\mu \nu} }{ \partial x^{\nu} } =0}\tag{5,6}$$
in both tensor formalisms (again, summation implied). The important detail to note here is that these aren't one equation each: they are *four*. This is because while each term is a sum over $\nu$, the values of $\mu$ are untouched. Since there are four values of $\mu=0,1,2,3$, there are four equations each.

In theory, this is it. Equations $(4)$, $(5)$ and $(6)$ uniquely describe all of electrodynamics (with suitable boundary conditions). With just two equations, we explain all electrodynamic phenomena of any kind[^2], in any frame. Essentially the ultimate result: the theory of electrodynamics is *closed*.

On paper, at least. In practice, figuring out what $F^{\mu \nu}$ or $G^{\mu \nu}$ are is everything but easy and oftentimes not even that rewarding: most real-world phenomena are already very well described by existing methods, using electric and magnetic fields as separate (but interdependent) objects, which end up being much simpler to solve than trying to tackle the can of worms that relativity is. However, if you cannot ignore relativistic effects, then $(4)$, $(5)$ and $(6)$ are what you reach for.
##### Deriving known equations
It's fair to expect to a confirmation that what we found even works. To do so, we'll just analyze $(5)$ piece-by-piece. Take $\mu=0$ for example
$$\begin{align}
\frac{ \partial F^{0\nu} }{ \partial x^{\nu} } &=\frac{ \partial F^{00} }{ \partial x^{0} } +\frac{ \partial F^{01} }{ \partial x^{1} } +\frac{ \partial F^{02} }{ \partial x^{2} } +\frac{ \partial F^{03} }{ \partial x^{3} } \\
&=\frac{1}{c}\frac{ \partial E_{x} }{ \partial t } +\frac{ \partial E_{y} }{ \partial y } -\frac{ \partial E_{z} }{ \partial z }  \\
&=\frac{1}{c}\left( \nabla\cdot \mathbf{E} \right) \\
&=\mu_{0}J^{0} \\
&=\mu_{0}c\rho
\end{align}$$
By using $c^{2}=1/\varepsilon_{0}\mu_{0}$ we find a familiar form:
$$\boxed{\nabla\cdot \mathbf{E}=\frac{\rho}{\varepsilon_{0}}}$$
This is [[Gauss' law]]. Now take $\mu=1$ for example. In that case, we get
$$\begin{align}
\frac{ \partial F^{1\nu} }{ \partial x^{\nu} } &=\frac{ \partial F^{10} }{ \partial x^{0} } +\frac{ \partial F^{11} }{ \partial x^{1} } +\frac{ \partial F^{12} }{ \partial x^{2} } +\frac{ \partial F^{13} }{ \partial x^{3} } \\
&=- \frac{1}{c^{2}}\frac{ \partial E_{x} }{ \partial t } +\frac{ \partial B_{z} }{ \partial y } -\frac{ \partial B_{y} }{ \partial z }  \\
&=\left( - \frac{1}{c^{2}}\frac{ \partial \mathbf{E} }{ \partial t } +\nabla\times \mathbf{B} \right)_{x} \\
&=\mu_{0}J^{1} \\
&=\mu_{0}J_{x}
\end{align}$$
Similar results come up for $\mu=2$ and $\mu=3$, which we can combine in vector notation to read
$$\boxed{\nabla\times \mathbf{B}=\mu_{0}\mathbf{J}+\mu_{0}\varepsilon_{0}\frac{ \partial \mathbf{E} }{ \partial t } }$$
This is the [[Ampere's law|Ampere-Maxwell law]]. Similarly, $\mu=0$ on the $G^{\mu \nu}$ equation gives us
$$\begin{align}
\frac{ \partial G^{0\nu} }{ \partial x^{\nu} } &=\frac{ \partial G^{00} }{ \partial x^{0} } +\frac{ \partial G^{01} }{ \partial x^{1} } +\frac{ \partial G^{02} }{ \partial x^{2} } +\frac{ \partial G^{03} }{ \partial x^{3} } \\
&=\frac{ \partial B_{x} }{ \partial x } +\frac{ \partial B_{y} }{ \partial y } +\frac{ \partial B_{z} }{ \partial z }   \\
&=\boxed{\nabla\cdot \mathbf{B}=0}
\end{align}$$
This is the unnamed Maxwell equation. Finally, for $\mu=1$:
$$\begin{align}
\frac{ \partial G^{1\nu} }{ \partial x^{\nu} } &=\frac{ \partial G^{10} }{ \partial x^{0} } +\frac{ \partial G^{11} }{ \partial x^{1} } +\frac{ \partial G^{12} }{ \partial x^{2} } +\frac{ \partial G^{13} }{ \partial x^{3} } \\
&=- \frac{1}{c}\frac{ \partial B_{x} }{ \partial t } - \frac{1}{c}\frac{ \partial E_{z} }{ \partial y } + \frac{1}{c}\frac{ \partial E_{y} }{ \partial z }  \\
&=- \frac{1}{c}\left( \frac{ \partial \mathbf{B} }{ \partial t } +\nabla\times \mathbf{E} \right)_{x} \\
&=0
\end{align}$$
Combine it with the results for $\mu=2$ and $\mu=3$ to get
$$\boxed{\nabla\times \mathbf{E}=-\frac{ \partial \mathbf{B} }{ \partial t } }$$
[[Faraday's law]].

The [[Lorentz force]] can be found from the [[Minkowski force]] caused by the field tensor $F^{\mu \nu}$ at a proper velocity $\eta^{\mu}$ on a charge $q$:
$$K^{\mu}=q\eta_{\nu}F^{\mu \nu}$$
The spatial components of these are given by $\mu=1,2,3$. For $\mu=1$:
$$\begin{align}
K^{1}&=aq\eta_{\nu}F^{1\nu} \\
&=q(-\eta^{0}F^{10}+\eta^{1}F^{11}+\eta^{2}F^{12}+\eta^{3}F^{13}) \\
&=q\left[ \frac{-c}{\sqrt{ 1-u^{2}/c^{2} }}\left( - \frac{E_{x}}{c} \right) + \frac{u_{y}}{\sqrt{ 1-u^{2}/c^{2} }}B_{z}+  \frac{u_{z}}{\sqrt{ 1-u^{2}/c^{2} }}(-B_{y})\right] \\
&=\frac{q}{\sqrt{ 1-u^{2}/c^{2} }}[\mathbf{E}+(\mathbf{u}\times \mathbf{B})]_{x}
\end{align}$$
Thus, with the other two components we get
$$\mathbf{K}=\frac{q}{\sqrt{ 1-u^{2}/c^{2} }}[\mathbf{E}+(\mathbf{u}\times \mathbf{B})]$$
and since the spatial component of a Minkowski force are related to the ordinary force by $\mathbf{K}=\mathbf{F}/\sqrt{ 1-u^{2}/c^{2} }$ we get
$$\boxed{\mathbf{F}=\mathbf{E}+(\mathbf{u}\times \mathbf{B})}$$


[^1]: Quantum physics notwithstanding.

[^2]: Again, quantum physics notwithstanding.
