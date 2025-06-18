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
It is possible to make statements about the behavior of differential equations near equilibrium points. Consider a first order autonomous system $\dot{\mathbf{x}}=f(\mathbf{x})$, where $f:\mathbb{R}^{N}\to \mathbb{R}^{N}$, and an equilibrium point $\mathbf{c}$. As usual, $f(\mathbf{c})=0$. We want to analyze the behavior of the system near $\mathbf{c}$, that is, for $\mathbf{x}$ in a neighborhood $\lVert \mathbf{x}-\mathbf{c} \rVert\ll 1$.

To do so, we start with a [[Taylor series]] of each $i$ component of $f$ centered in $\mathbf{c}$, truncating to first order:
$$\begin{align}
f_{i}(\mathbf{x})&=\underbrace{ f_{i}(\mathbf{c}) }_{ 0 }+\sum_{j=1}^{N} \frac{ \partial f_{i} }{ \partial x_{j} } (\mathbf{c})(x_{j}-c_{j})+O(\lVert \mathbf{x}-\mathbf{c} \rVert^{2} ) \\
&\simeq\sum_{j=1}^{N} \frac{ \partial f_{i} }{ \partial x_{j} } (\mathbf{c})(x_{j}-c_{j})
\end{align}$$
This assumes that the derivatives of $f$ in the equilibrium point $\mathbf{c}$ are nonzero. If they are, then this approximation would claim that $f_{i}(\mathbf{x})=0$ everywhere, which is manifestly false and in the entire approximation fails. In such a case, we wouldn't be able to stop at the first term and we'd require the quadratic terms too (the second derivatives) which, in other words, means that we'd be stuck with nonlinear analysis. When working with linearization, we need to assume (or ideally, prove) that the derivatives are nonzero in $\mathbf{c}$.

In order to approximate the equation to a practical state, we claim that the ODE can be locally[^1] approximated as a *linear* ODE $\dot{\mathbf{x}}=\mathrm{A}\mathbf{x}$, where $\mathrm{A}$ is an $N\times N$ [[matrix]]. Specifically, our matrix is going to be made of all of the first derivatives that are left in the equation above and we will evaluate it in $\mathbf{x}-\mathbf{c}$:
$$\dot{\mathbf{x}}=f(\mathbf{x})\simeq \mathrm{A}(\mathbf{x}-\mathbf{c})\quad\text{where}\quad A_{ij}=\frac{ \partial f_{i} }{ \partial x_{j} }(\mathbf{c}) $$
But this matrix is precisely the [[Jacobian]] $\mathrm{J}$ of the function $f$ when evaluated in $\mathbf{c}$, and so $\mathrm{A}\equiv \mathrm{J}(\mathbf{c})$. If we set $\boldsymbol{\xi}(t)=\mathbf{x}(t)-\mathbf{c}$, its derivative is $\dot{\boldsymbol{\xi}}=\dot{\mathbf{x}}=f(\mathbf{x})\simeq \mathrm{J}(\mathbf{c})(\mathbf{x}-\mathbf{c})=\mathrm{J}(\mathbf{c})\boldsymbol{\xi}$. As such, within a small enough neighborhood of an equilibrium point, any mechanical system with nonzero derivatives in $\mathbf{c}$ can be **linearized** to the form
$$\boxed{\dot{\boldsymbol{\xi}}=\mathrm{J}(\mathbf{c})\boldsymbol{\xi}}$$
In the simplest scenario of a one-dimensional system $\dot{x}=f(x)$, with $\xi(t)=x(t)-c$ , the Jacobian simplifies down to the only derivative of $f$, $\frac{df}{dx}(x)\equiv f'(x)$. In such a case, then
$$\boxed{\dot{\xi}=f'(c)\xi}$$
This is a one-dimensional, linear ODE in $\xi$. It's solution is easy: it's an exponential. Moreover, $f'(c)$ provides useful information on the behavior around the point. If the sign is negative, and thus the slope of $f(c)$ is downwards, then the point is stable. Else, it isn't. Either way, the *magnitude* of $f'(c)$ tells us *how* stable the point is, and its reciprocal $1/\lvert f'(c) \rvert$ is the **characteristic time scale** of the system, which gives a ballpark number of how long the system takes to vary significantly in the neighborhood of $c$.

Now, it would be great if there were a universal solution to this approximation. That way, we'd have a good-enough universal solution to all mechanical systems near equilibrium. Turns out, there actually is one. To find it, we make the following ansatz:
$$\text{The partial solution of }\boldsymbol{\xi}(t)\text{ is }\rho(t)\mathbf{u}\text{ where }\mathbf{u}\in \mathbb{R}^{N}$$
Basically, we claim that $\boldsymbol{\xi}(t)$ is a constant vector $\mathbf{u}$ scaled by a [[scalar field]] $\rho(t)$. Plugging this into the linearized equation, knowing that $\dot{\boldsymbol{\xi}}(t)=\dot{\rho}(t)\mathbf{u}$, we get
$$\dot{\rho}(t)\mathbf{u}=\rho(t)\mathrm{A}\mathbf{u}$$
For this to hold, $\mathbf{u}$ must be an [[Equazione agli autovalori|eigenvector]] of $\mathrm{A}$, of some eigenvalue $\alpha$, so that
$$\mathrm{A}\mathbf{u}=\alpha \mathbf{u}\quad\Rightarrow \quad \dot{\rho}(t)\mathbf{u}=\alpha\rho(t)\mathbf{u}$$
We can now match the coefficients of $\mathbf{u}$:
$$\dot{\rho}(t)=\alpha \rho(t) \quad\Rightarrow \quad \rho (t)=Ce^{\alpha t}$$
Thus, the partial solution of $\boldsymbol{\xi}(t)$ must in general be
$$\boldsymbol{\xi}(t)=Ce^{\alpha t}\mathbf{u}$$
for some constants $C$ and an eigenvalue $\alpha$ satisfying $\mathrm{A}\mathbf{u}=\alpha \mathbf{u}$. There is one of these for each eigenvector $\mathbf{u}$. The general solution will then be the [[linear combination]] of all of these:
$$\boxed{\boldsymbol{\xi}(t)=\sum_{k=1}^{N} C_{k}e^{\alpha_{k}t}\mathbf{u}_{k}}$$
This approach works as long as $\mathrm{A}\equiv \mathrm{J}(\mathbf{c})$ is [[Diagonalization|diagonalizable]] or at the very least admits a [[basis]] of eigenvectors $\mathbf{u}_{1},\ldots,\mathbf{u}_{N}$. The behavior of $\boldsymbol{\xi}(t)$ near $\mathbf{c}$ can then be discerned by the real parts of $\alpha_{k}$ (which may very well be complex):
- if all $\alpha_{k}$ have negative real parts, $\mathbf{c}$ is stable;
- if all $\alpha_{k}$ have positive real parts, $\mathbf{c}$ is unstable;
- if any $\alpha_{k}$ has zero real part but nonzero imaginary part, then that signals oscillatory behavior around the equilibrium.

The idea here is that the [[spectrum]] of the Jacobian of $f$ determines how the system behaves around equilibrium points.
### Examples
> [!example] Free particle
> The free particle ODE is $\ddot{\mathbf{x}}(t)=0$, with $f=0$. As such, all points $(x,0)$ (i.e. any starting condition with zero velocity) is an equilibrium point.

> [!example] Second order mechanical system
> A generic second order ODE $\ddot{x}=f(x(t),\dot{x}(t))$ can be decomposed into two first order equations $\dot{x}=f(x)$ and $\ddot{x}=\dot{v}=0$. The equilibrium points are the zeros of $f$. Since
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

[^1]: By "locally" we're talking about the neighborhood of $\mathbf{c}$.
