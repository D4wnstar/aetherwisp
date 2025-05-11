---
wiki-publish: true
---
**Ljapunov's theorem** gives a method for determining whether an [[equilibrium point]] of an [[Ordinary differential equation|ODE]] is stable or not.

> [!info] Ljapunov's theorem
> Let $\mathbf{c}$ be an equilibrium point for an ODE $\dot{\mathbf{x}}(t)=f(\mathbf{x}(t))$. If there exists a [[dynamical variable]] $W:\mathbb{R}^{N}\to \mathbb{R}$ in a neighborhood $U_{c}$ of $\mathbf{c}$ (called a **Lyapunov function**) such that
> 1. $W$ as a strict minimum in $\mathbf{c}$, i.e. $W(\mathbf{x})>W(\mathbf{c})$ for all $\mathbf{x}\in U_{c}\setminus \{ \mathbf{c} \}$;
> 2. its [[Lie derivative]] is always non-positive, i.e. $\mathcal{L}_{f}W\leq 0$;
> then $\mathbf{c}$ is a stable equilibrium point in the future.

There is also a corollary that applies to [[conservative system|conservative systems]] which states that isolated minima of the [[potential energy]] are always stable equilibrium points.

> [!info] Corollary
> Consider the conservative mechanical system
> $$\begin{cases}
> \dot{x}=v \\
> \dot{v}=f(x)
> \end{cases}$$
> We know that $f(x)$ can be described by the derivative of a [[potential energy]] $V(x)$ as $f(x)=-V'(x)/m$, where $m$ is the [[mass]]. If the potential energy has an isolated minimum in $x^{*}\in \mathbb{R}$, then $\mathbf{c}=(x^{*},0)\in \mathbb{R}^{2}$ is a stable equilibrium point in the future.
> 
> **Proof.** Let $x^{*}$ be an isolated minimum for $V$. Then, $V'(x^{*})=0$ and so $f(x^{*})=0$. Thus, $\mathbf{c}=(x^{*},0)$ is an equilibrium point. To see that it is also stable, consider the total mechanical [[energy]]
> $$E=\frac{1}{2}mv^{2}+V(x)$$
> as a dynamical variable. This quantity satisfies Ljapunov's theorem since
> 1. $E$ has an isolated minimum in $(x^{*},0)$ because the [[kinetic energy]] is zero if $v=0$ and $V(x^{*})$ is an isolated minimum.
> 2. Mechanical energy is a constant of motion, so $\mathcal{L}_{f}E=0$.
> 
> Since it verifies the theorem, it is a stable in the future.
### Examples
> [!example] Dampened harmonic oscillator
> We can prove that the equilibrium point of a dampened [[harmonic oscillator]] is stable using Ljapunov's theorem. The energy of a harmonic oscillator is
> $$E=\frac{1}{2}mv^{2}+ \frac{1}{2}m\omega^{2}x^{2}$$
> Our potential energy is the usual $V(x)=m\omega ^{2}x^{2}/2$. The ODE is $\ddot{x}=-\omega ^{2}x-2\mu \dot{x}$, where $\mu>0$ is the dampening constant. The vector field is
> $$f=\begin{pmatrix}
> v \\
> -\omega ^{2}x-2\mu v
> \end{pmatrix}$$
> To have $f=\begin{pmatrix}0 \\ 0\end{pmatrix}$ we just need $\mathbf{c}=(x,v)=(0,0)$, which is our equilibrium point. We just need to apply Ljapunov's theorem in a neighborhood of $\mathbf{c}$ using the total energy. We already know that $E$ is a constant of motion, so we just need to check that the Lie derivative is always non-positive:
> $$\mathcal{L}_{f}E=\frac{ \partial E }{ \partial x } f_{1}+\frac{ \partial E }{ \partial v } f_{2}=m\omega ^{2}xv+mv(-\omega ^{2}x-2\mu v)=-2m\mu v^{2}\leq 0$$
> This verifies the theorem, so $\mathbf{c}$ is stable in the future.
