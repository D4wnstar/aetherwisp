---
wiki-publish: true
---
**Hamilton's principle** is a formulation of the [[least action principle]] that states that the dynamics of a [[physical system]] are fully determined by the minimization of a [[functional]], known as the [[action]], of the [[Lagrangian]]. The functions for which the functional is minimized uniquely determine the motion of the system.
### Equivalence with the differential solution of motion
Hamilton's principle is a fundamental result from which the entirety of mechanics can be derived. This can be seen by the following statement:

> [!info] Hamilton's principle equivalence
> The motion $q(t)$ in a period of time $t_{1}\leq t\leq t_{2}$ makes the action functional $S[q]$ stationary for the variations $\delta q_{1},\ldots,\delta q_{n}$ null at the boundaries $t_{1},t_{2}$ if and only if the functions $q_{i}(t)$ satisfy the [[Lagrange equation]].

Consider two Lagrangians $L(q,\dot{q},t)$ and $\tilde{L}(\tilde{q},\dot{\tilde{q}},t)$ linked by
$$L(\tilde{q},\dot{\tilde{q}},t)=L(q(\tilde{q},t),\dot{q}(\tilde{q},\dot{\tilde{q}},t),t)$$
The motion $\tilde{q}(t)$ satisfies the Lagrange equation for $\tilde{L}$ if and only if the motion $q(t)\equiv q(\tilde{q}(t),t)$ satisfies the Lagrange equation for $L$.

> [!info] Proof
> Since both are valid motions, they must both minimize action, and so
> $$\int_{t_{1}}^{t_{2}}\tilde{L}(\tilde{q}(t),\dot{\tilde{q}}(t),t)dt=\int_{t_{1}}^{t_{2}}L(q(t),\dot{q}(t),t)dt$$
> The left hand side is stationary in $\tilde{q}(t)$ if and only if $\tilde{q}(t)$ solves the Lagrange equation for $\tilde{L}$. Similarly, the right hand side is stationary in $q(t)$ if and only if $q(t)$ solves the Lagrange equation for $L$. But because the actions are equal, these statements are equivalent and must be simultaneously true.
