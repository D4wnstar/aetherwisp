---
wiki-publish: true
---
An **equilibrium point**, in mathematics, is a constant solution to a differential equation. Given a generic [[Ordinary differential equation|ODE]] $\dot{\mathbf{x}}(t)=f(\mathbf{x}(t))$, an equilibrium point is a solution $\mathbf{x}(t)=\mathbf{c}$. They are called equilibrium *points* because their "trajectories" in [[phase space]] are actually just a single point, unlike the usual [[curve]]. Unless perturbed, the system never moves out of the equilibrium point.
### Properties
- Equilibrium points constitute the set of all zeros of the [[vector field]] $f$: if $\mathbf{c}$ is an equilibrium point, then $f(\mathbf{c})=0$ for all $t$; the converse also applies. 
- An equilibrium point $\mathbf{c}$ is **stable** if for every neighborhood $U$ of $\mathbf{c}$, there exists another neighborhood $V$ of $\mathbf{c}$ such that any motion $\mathbf{x}(t;\mathbf{x}_{0})$ that starts in $V$ ($\mathbf{x}_{0}\in V$) remains in $U$ for all $t$. An equilibrium point that doesn't meet this condition is **unstable**.
- A less binding property is being stable **in the future** and **in the past**. These have the same definition, but motion only remains in $U$ for all $t>0$ (future) or $t<0$ (past).
### Search
In practice, given an ODE, finding its equilibrium points is just a matter of finding the zeros of $f(\mathbf{x}(t))$. More complicated is determining if a given equilibrium point is stable or not. This can be done through [[Ljapunov's theorem]].
### Linearization near equilibrium points
It is possible to make statements about the behavior of differential equations near equilibrium points. Consider a first order autonomous system $\dot{\mathbf{x}}=f(\mathbf{x})$, where $f:\mathbb{R}^{N}\to \mathbb{R}^{N}$. As usual, $f(\mathbf{c})=0$. We want to analyze the behavior of the system near an equilibrium point $\mathbf{c}$, that is, for $\mathbf{x}$ in a neighborhood $\lVert \mathbf{x}-\mathbf{c} \rVert\ll 1$.

To do so, we start with a [[Taylor series]] of each $i$ component of $f$ centered in $\mathbf{c}$, truncating to first order:
$$\begin{align}
f_{i}(\mathbf{x})&=\underbrace{ f_{i}(\mathbf{c}) }_{ 0 }+\sum_{j=1}^{N} \frac{ \partial f_{i} }{ \partial x_{j} } (\mathbf{c})(x_{j}-\mathbf{c})+\mathcal{O}(\lVert \mathbf{x}-\mathbf{c} \rVert^{2} ) \\
&\simeq\sum_{j=1}^{N} \frac{ \partial f_{i} }{ \partial x_{j} } (\mathbf{c})(x_{j}-\mathbf{c})
\end{align}$$
In order to approximate the equation to a practical state, we claim that the ODE can locally approximated as a *linear* ODE $\dot{\mathbf{x}}=\mathrm{A}\mathbf{x}$, where $\mathrm{A}$ is an $N\times N$ matrix. Specifically, our matrix is going to be made of all of the first derivatives that are left in the equation above and we will evaluate it in $\mathbf{x}-\mathbf{c}$:
$$\dot{\mathbf{x}}=f(\mathbf{x})\simeq \mathrm{A}(\mathbf{x}-\mathbf{c})\quad\text{where}\quad A_{ij}=\frac{ \partial f_{i} }{ \partial x_{j} } $$
If we set $\boldsymbol{\xi}(t)=\mathbf{x}(t)-\mathbf{c}$, its derivative is $\dot{\boldsymbol{\xi}}=\dot{\mathbf{x}}=f(\mathbf{x})\simeq \mathrm{A}(\mathbf{x}-\mathbf{c})=\mathrm{A}\boldsymbol{\xi}$. As such, within a small enough neighborhood of an equilibrium point, any mechanical system can be **linearized** to the form
$$\boxed{\dot{\boldsymbol{\xi}}=\mathrm{A}\boldsymbol{\xi}}$$
Now, it would be great if there were a universal solution to this approximation. That way, we'd have a good-enough universal solution to all mechanical systems near equilibrium. Turns out, there actually is one. To find it, we make the following ansatz:
$$\text{The partial solution of }\boldsymbol{\xi}(t)\text{ is }\rho(t)\mathbf{u}\text{ where }\mathbf{u}\in \mathbb{R}^{N}$$
(???)
$$\dot{\rho}\mathbf{u}=\rho(\mathrm{A}\mathbf{u})\quad\Rightarrow \quad \mathbf{u}\text{ is a solution if }\exists \alpha |\mathrm{A}\mathbf{u}=\alpha \mathbf{u}$$
Basically, we want to [[Diagonalization|diagonalize]] $\mathrm{A}$ and find the [[Equazione agli autovalori|eigenvalues]]. In this case, we get
$$\dot{\rho}\mathbf{u}=\rho(\mathrm{A}\mathbf{u})=\rho \alpha \mathbf{u}\quad\to \quad \dot{\rho}=\alpha \rho \quad\to \quad \rho (t)=Ce^{\alpha t}$$
$\rho(t)\mathbf{u}$ is a solution when $\mathbf{u}$ is an eigenvector of $\mathrm{A}$ and when $\rho(t)=Ce^{\alpha t}$, where $\alpha$ is the eigenvalue of $\mathrm{A}$ for $\mathbf{u}$.
### Examples
> [!example] Free particle
> The free particle ODE is $\ddot{\mathbf{x}}(t)=0$, with $f=0$. As such, all points $(x,0)$ (i.e. any starting condition with zero velocity) is an equilibrium point.

> [!example] Second order mechanical system
> A generic second order system of ODE $\ddot{x}=f(x(t),\dot{x}(t))$ can be decomposed into two first order equations $\dot{x}=f(x)$ and $\ddot{x}=\dot{v}=0$. The equilibrium points are the zeros of $f$. Since
> $$f=\begin{pmatrix}
> v \\
> f(x,v)
> \end{pmatrix}$$
> the zeros are given by
> $$\begin{cases}
> v =0 \\
> f(x,v)=0
> \end{cases}$$
> Thus, $\mathbf{c}=\begin{pmatrix}c \\ 0\end{pmatrix}$ with $c$ such that $f(c,0)=0$.

> [!example] Harmonic oscillator
> The ODE of the 1D [[harmonic oscillator]] is $f(x,v)=-\omega ^{2}x$. It has exactly one equilibrium point, $x=0$ (for which $\dot{x}=v=0$).

> [!example] Simple pendulum
> The ODE of a [[simple pendulum]] is $f(x,v)=-\sin x$. It has exactly two equilibrium points, $x=0$ and $x=\pi$. The former is stable, the latter is unstable.
