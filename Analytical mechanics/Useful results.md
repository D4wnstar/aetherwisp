---
wiki-publish: true
---
### General ODEs
**Dynamical variable**
$$G:\mathbb{R}^{N}\to \mathbb{R},\quad \frac{d}{dt}G(\mathbf{x}(t))=\sum_{i=1}^{N} \frac{ \partial G }{ \partial x_{i} } (\mathbf{x}(t))\dot{\mathbf{x}}_{i}(t)$$

**Constant of motion**
Quantity $I$ that does not change over time over a trajectory of motion. $\frac{d}{dt}I(\mathbf{x}(t))=0$. Each constant of motion removes one degree of freedom. Energy is always constant in conservative systems. Angular momentum is another useful one. To check if $I$ is a constant, either take the Lie derivative, use a system-specific argument or solve motion $\mathbf{x}(t)$, substitute it in $I(\mathbf{x}(t))$ and see if $I(\mathbf{x}(t))$ is constant with respect to $t$.

**Lie derivative on dynamical variable $G$ and vector field $f(\mathbf{x})$**
$$\begin{align}
&\mathcal{L}_{f}G:\mathbb{R}^{N}\to \mathbb{R} \\
&\mathbf{x}\mapsto \sum_{i=1}^{N} \frac{ \partial G }{ \partial x_{i} } (\mathbf{x})f_{i}(\mathbf{x})=\nabla G\cdot f=dG[f]
\end{align}$$
If Lie derivative is zero, then $G$ is a constant of motion (and viceversa).

**Equilibrium point**
An equilibrium point is a constant solution to a differential equation. They are zeros of the derivative vector field $f$ in $\dot{\mathbf{x}}=f(x)$. An equilibrium point is stable if there exists a neighborhood around it where if motion starts in that neighborhood, it remains in that neighborhood for all time. Alternatively, it satisfies Ljapunov's theorem.

**Ljapunov's theorem**
Let $\mathbf{c}$ be an equilibrium point for an ODE $\dot{\mathbf{x}}(t)=f(\mathbf{x}(t))$. If there exists a dynamical variable $W:\mathbb{R}^{N}\to \mathbb{R}$ in a neighborhood $U_{c}$ of $\mathbf{c}$ (called a **Lyapunov function**) such that
1. $W$ has a strict minimum in $\mathbf{c}$, i.e. $W(\mathbf{x})>W(\mathbf{c})$ for all $\mathbf{x}\in U_{c}\setminus \{ \mathbf{c} \}$;
2. its Lie derivative is always non-positive, i.e. $\mathcal{L}_{f}W\leq 0$;
then $\mathbf{c}$ is a stable equilibrium point in the future.

A corollary states that isolated potential minima are also equilibrium points if the system is conservative.

**Generalized coordinates**
Generalized coordinates $\mathbf{q}$ describe the abstract position of the system. A specific value of the generalized coordinates is called a configuration and they are defined in configuration space $Q$. Their total time derivatives are called generalized velocities $\dot{\mathbf{q}}$ and exist in the tangent space $T_{P}Q$ of $Q$ for a given configuration $P$. The tuple $(\mathbf{q},\dot{\mathbf{q}})$ exists in the tangent bundle $TQ$.

There is a minimum number of generalized coordinates necessary to describe a system. This is known as the **degrees of freedom** and is the dimension of $Q$. Coordinates necessary to define $Q$ are called **free coordinates**. The rest are called **cyclical coordinates**.

**Coordinate transformation**
An invertible linear map, specifically a diffeomorphism, between a real vector space and itself. In general, $\varphi:\mathbb{R}^{N}\mapsto \mathbb{R}^{N}$.

**Nöther's theorem conservations**
- Invariance under spatial shifts is conservation of linear momentum.
- Invariance under rotations is conservation of angular momentum.
- Invariance under temporal shifts is conservation of energy.

**Rotations**
Antisymmetric matrices in $SO(N)$ with unit determinant. They make a vector space (actually: Lie algebra) and can be seen as a sum of basis rotations $\mathrm{E}_{i}$ called generators. In general, $R(\omega)=e^{\omega \mathrm{E}}$ for a rotation on the axis of the generator $\mathrm{E}$. A generic rotation is
$$R=\prod_{i=1}^{N}e^{\omega_{i}\mathrm{E}_{i}}$$
An infinitesimal rotation is a rotation for an infinitesimal angle. In terms of generators it is a simple sum
$$\Omega=\sum_{i=1}^{3} \omega_{i}\mathrm{E}_{i}=\Omega_{ij}=-\sum_{k=1}^{3} \epsilon_{ijk}\omega_{k}$$
### Lagrangian mechanics
**Conjugate momenta**
$$P_{l}(q,\dot{q},t)\equiv \frac{ \partial L }{ \partial \dot{q}_{l} } (q,\dot{q},t)$$

**Equilibrium configuration**
An equilibrium configuration is a configuration that leaves the system at rest. $\mathbf{q}^{*}$ is an equilibrium configuration if $\mathbf{c}=(\mathbf{q}^{*},0)$ is an equilibrium point for a Lagrangian system $(\mathbf{q},\dot{\mathbf{q}})$.

**Total energy in a Lagrangian system**
$$E(q,\dot{q},t)=\sum_{i=1}^{n} \dot{q}_{i}\frac{ \partial L }{ \partial \dot{q}_{i} }(q,\dot{q},t)-L(q,\dot{q},t) $$

**Nöther's theorem**
Consider the transformations
$$q_{n}\mapsto\varphi_{n}(q,\alpha),\qquad\dot{q}_{n}\mapsto \psi(q,\dot{q},\alpha)=\sum_{k=1}^{n} \frac{ \partial \varphi_{n}(q,\alpha) }{ \partial q_{k} } \dot{q}_{k}$$
$\varphi_{n}(q,\alpha)$ must be continuous and differentiable in a neighborhood of $\alpha=0$. Also, $\varphi_{n}(q,0)=q_{n}$. $\psi(q,\dot{q},\alpha)$ must be continuous. If a Lagrangian $L$ with conjugate momenta $P_{k}$ is invariant under the transformation $(q,\dot{q},t)\mapsto(\varphi(q,\alpha),\psi(q,\dot{q},\alpha),t)$, then
$$\mathcal{P}(q,\dot{q},t)=\sum_{m=1}^{n} \frac{ \partial \varphi_{m} }{ \partial \alpha } (q,0)P_{m}(q,\dot{q},t)$$
is a constant of motion.