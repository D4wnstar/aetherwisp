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
An equilibrium point is a constant solution to a differential equation. They are zeros of the derivative vector field $f$ in $\dot{\mathbf{x}}=f(\mathbf{x})$. They are also stationary points of the potential. An equilibrium point is stable if there exists a neighborhood around it where if motion starts in that neighborhood, it remains in that neighborhood for all time. Alternatively, it satisfies Ljapunov's theorem.

**Ljapunov's theorem**
Let $\mathbf{c}$ be an equilibrium point for an ODE $\dot{\mathbf{x}}(t)=f(\mathbf{x}(t))$. If there exists a dynamical variable $W:\mathbb{R}^{N}\to \mathbb{R}$ in a neighborhood $U_{c}$ of $\mathbf{c}$ (called a **Lyapunov function**) such that
1. $W$ has a strict minimum in $\mathbf{c}$, i.e. $W(\mathbf{x})>W(\mathbf{c})$ for all $\mathbf{x}\in U_{c}\setminus \{ \mathbf{c} \}$;
2. its Lie derivative is always non-positive, i.e. $\mathcal{L}_{f}W\leq 0$;
then $\mathbf{c}$ is a stable equilibrium point in the future.

A corollary states that isolated potential minima are also stable equilibrium points if the system is conservative.

**Generalized coordinates**
Generalized coordinates $\mathbf{q}$ describe the abstract position of the system. A specific value of the generalized coordinates is called a configuration and they are defined in configuration space $Q$. Their total time derivatives are called generalized velocities $\dot{\mathbf{q}}$ and exist in the tangent space $T_{P}Q$ of $Q$ for a given configuration $P$. The tuple $(\mathbf{q},\dot{\mathbf{q}})$ exists in the tangent bundle $TQ$. The conjugate momenta exists for $P$ exist in the cotangent space $T_{P}^{*}Q$. The tuple $(\mathbf{q},\mathbf{p})$ is called **canonical coordinates** and exists in the cotangent bundle $T^{*}Q$ and is called the **phase space**.

There is a minimum number of generalized coordinates necessary to describe a system. This is known as the **degrees of freedom** and is the dimension of $Q$. Coordinates necessary to define $Q$ are called **free coordinates**. The rest are called **cyclical coordinates**.

**Coordinate transformation**
An invertible linear map, specifically a diffeomorphism, between a real vector space and itself. In general, $\varphi:\mathbb{R}^{N}\mapsto \mathbb{R}^{N}$.

**Constraint**
A constraint is a limitation on the system. With Newton's law: $m\mathbf{a}=\mathbf{F}+\Phi$.
- **Ideal** if $\Phi$ is always orthogonal to configuration space for any configuration: $\Phi\cdot \delta \mathbf{r}=0$.
- **Holonomic** if it can be written as $f(q_{1},\ldots,q_{n},t)=0$.
- **Scleronomous** if it changes in time, else **rheonomous**.

**Kinetic energy**
$$T=T_{2}+T_{1}+T_{0}=\frac{1}{2}\sum_{j,k=1}^{n}a_{jk}(q,t)\dot{q}_{j}\dot{q}_{k}+\sum_{l=1}^{n} b_{l}(q,t)\dot{q}_{l}+\frac{1}{2}c(q,t)$$
If $\mathbf{v}$ is not explicitly dependent on $t$, then $T_{1}=T_{0}=0$ and $T=T_{2}$. $a_{jk}$ are elements of the kinetic matrix, which is symmetric, positive definite and invertible.

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
**Lagrange equation (general)**
$$\frac{d}{dt} \frac{ \partial T }{ \partial \dot{q}_{j} }(q(t),\dot{q}(t),t)- \frac{ \partial T }{ \partial q_{j} } (q(t),\dot{q}(t),t)=Q_{j} $$

**Lagrange equation (conservative system)**
$$\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{i} }(q(t),\dot{q}(t),t)-\frac{ \partial L }{ \partial q_{i} } (q(t),\dot{q}(t),t)=0 $$

**Lagrangian**
$$L=T-V$$

**Effective Lagrangian**
1. See if there's any cyclical coordinates $q_{l}$ (any that does not appear in the Lagrangian).
2. Find the conjugate momenta $\tilde{P}_{l}$ to those. They are all constants of motion.
3. Invert them to get the (also constant) velocity $\dot{q}_{l}$.
4. Substitute the velocities in the Lagrangian while also subtracting $\sum_{l=m+1}^{n} \tilde{P}_{l}\dot{q}_{l}$.
5. You now have the effective Lagrangian.

**Generalized forces**
$$\delta W=\sum_{i=1}^{n} Q_{i}\delta q_{i},\quad Q_{j}=\sum_{i=1}^{N} \mathbf{F}_{i}\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } $$
If conservative forces:
$$Q_{j}=- \frac{ \partial V }{ \partial q_{j} }$$

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
### Hamiltonian mechanics
**Hamilton equations (conservative system)**
$$\dot{q}_{i}=\frac{ \partial H }{ \partial p_{i} },\quad \dot{p}_{i}=-\frac{ \partial H }{ \partial q_{i} }  $$

**Hamilton equations (compact)**
$$\dot{\mathbf{x}}=\mathrm{E}\nabla_{\mathbf{x}}H(\mathbf{x},t)=\{ \mathbf{x},H \}$$

**Hamiltonian**
Generator of time shifts
$$H(p,q,t)\equiv\left.{(\mathbf{p}\cdot \dot{\mathbf{q}}-L(q,\dot{q},t))}\right|_{\dot{q}_{i}=u_{i}(p,q,t)}=T+V,\qquad\frac{ \partial H }{ \partial t } =-\frac{ \partial L }{ \partial t } $$

**Poisson brackets**
$$\{ f,g \}(q,p,t)=\sum_{i=1}^{n} \left( \frac{ \partial f }{ \partial q_{i} } \frac{ \partial g }{ \partial p_{i} } - \frac{ \partial f }{ \partial p_{i} } \frac{ \partial g }{ \partial q_{i} }  \right)$$
**Poisson brackets (compact)**
$$\{ f,g \}(\mathbf{x},t)=\sum_{i,j=1}^{2n} \frac{ \partial f }{ \partial x_{i} } E_{ij}\frac{ \partial g }{ \partial x_{j} } =\nabla_{\mathbf{x}}f\cdot \mathrm{E}\nabla_{\mathbf{x}}g$$

**Poisson brackets (fundamental)**
$$\{ q_{i},q_{j} \}=0,\qquad \{ p_{i},p_{j} \}=0,\qquad \{ q_{i},p_{j} \}=\delta_{ij}$$
$$\{ x_{i},x_{j} \}=E_{ij},\qquad\{ \mathbf{x},G \}=\mathrm{E}\nabla_{\mathbf{x}}G,\qquad \dot{\mathbf{x}}=\{ \mathbf{x},H \}$$
$$\{ L_{1},L_{2} \}=L_{3},\qquad \{ L_{2},L_{3} \}=L_{1},\qquad \{ L_{3},L_{1} \}=L_{2},\qquad \{ L^{2},L_{i} \}=0$$

**Poisson brackets (constants of motion)**
$$f\text{ is a constant of motion}\quad\Leftrightarrow\quad \{ f,H \}+\frac{ \partial f }{ \partial t } =0$$
If $f$ does not depend on $t$ then
$$f\text{ is a constant of motion}\quad\Leftrightarrow\quad \{ f,H \} =0$$

**Canonical transformations**
A canonical transformation is a coordinate transformation that transforms a set of coordinates that satisfy the Hamilton equations into another set that also satisfies them.

Mathematically, the transformation $q_{i}=u_{i}(\tilde{q},\tilde{p},t)$, $p_{i}=v_{i}(\tilde{q},\tilde{p},t)$ is canonical if for all Hamiltonians $H(q,p,t)$, there exists a function $K(\tilde{q},\tilde{p},t)$ called the **conjugate Hamiltonian** such that, if the equations of motion in coordinates $(q,p)$ obey the Hamilton equations
$$\dot{p}_{i}=-\frac{ \partial H }{ \partial q_{i} },\quad  \dot{q}_{i}=\frac{ \partial H }{ \partial p_{i} }$$
then the equations in $(\tilde{q},\tilde{p})$ also obey the Hamilton equations, with $K$ as the Hamiltonian:
$$\dot{\tilde{p}}_{i}=-\frac{ \partial K }{ \partial \tilde{q}_{i} },\quad\dot{\tilde{q}}_{i}=\frac{ \partial K }{ \partial \tilde{p}_{i} }$$
The solutions are related by the functions $u$ and $v$ as $q_{i}(t)=u_{i}(\tilde{q}(t),\tilde{p}(t),t)$ and $p_{i}(t)=v_{i}(\tilde{q}(t),\tilde{p}(t),t)$.

**Canonicity criteria**
1. A transformation can be proven to be canonical by seeing if satisfies the first canonicity criterion.
2. The constant $c$ can be found by taking the determinant of the Jacobian of the transformation, as per $c^{n}=1/\lvert \det J \rvert$.
3. If $c=1$, the Jacobian and the transformation are symplectic.
4. A nonunivalent canonical transformation can always be turned into a univalent one by composing it with a different, appropriate canonical transformation.

**First canonicity criterion**
A transformation $\mathbf{x}=\mathbf{w}(\tilde{\mathbf{x}},t)$ is **canonical** if and only if there exists some $c\neq 0$ for which its Jacobian $J$ satisfies $cJ\mathrm{E}J^{T}=\mathrm{E}$. If $c=1$, the transformation is **univalent canonical** and its Jacobian is symplectic.

**Second canonicity criterion**
A transformation $\mathbf{x}=w(\tilde{\mathbf{x}},t)$ is univalent canonical if and only if it preserves the Poisson brackets.

**Poisson bracket preservation**
$$\{ f,g \}(w(\tilde{\mathbf{x}},t),t)=\{ \tilde{f},\tilde{g} \}(\tilde{\mathbf{x}},t)$$
where $\tilde{f}(\tilde{\mathbf{x}},t)\equiv f(w(\tilde{\mathbf{x}},t),t)$ and $\tilde{g}(\tilde{\mathbf{x}},t)\equiv g(w(\tilde{\mathbf{x}},t),t)$. Basically, the order of operations doesn't matter ("brackets first transform after" is the same as "transform first brackets after").