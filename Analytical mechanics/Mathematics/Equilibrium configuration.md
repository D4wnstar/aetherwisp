---
wiki-publish: true
---
An **equilibrium configuration** is a [[Generalized coordinates|configuration]] that leaves a [[Physical system|system]] at rest. By definition, $\mathbf{q}^{*}$ is an equilibrium configuration for the [[Lagrange equation]] if $\mathbf{c}\equiv(\mathbf{q}^{*},0)$ is an [[equilibrium point]] for the system.

The Lagrange equation is $\ddot{\mathbf{q}}=f(\mathbf{q},\dot{\mathbf{q}})=Q^{-1}(\mathbf{Q}+\ldots)$. The second term is expressed as an [[invertible matrix]] $Q$ multiplied by some function $\mathbf{Q}+\ldots$, where the dots are some quantity dependent on $\dot{\mathbf{q}}$.

Say we describe the system with a system of [[Ordinary differential equation|ODEs]]:
$$\ddot{q}_{k}=f_{k}(q,\dot{q})\quad\leftrightarrow \quad \begin{cases}
\dot{q}_{k}=\eta_{k} \\
\dot{\eta}_{k}=f_{k}(q,\eta)
\end{cases}$$
The condition of equilibrium can be stated as $f(\mathbf{c})=f(\mathbf{q}^{*},0)=0$. But since we wrote $f$ in terms of $Q$ we can also say
$$Q^{-1}\left.{\mathbf{Q}}\right|_{(\mathbf{q}^{*},0)}=0\quad\Rightarrow \quad \mathbf{Q}(\mathbf{q}^{*},0)=0$$
Hence we can just look to zero out $\mathbf{Q}$ instead of $f$. If $Q_{n}=-\frac{ \partial V }{ \partial q_{n} }$ then $\mathbf{q}^{*}$ is an equilibrium configuration if and only if $\frac{ \partial V }{ \partial q_{h} }(\mathbf{q}^{*},0)=0$ for all $h=1,\ldots,n$.
### Properties
$\mathbf{q}^{*}$ is said to be **stable** if $\mathbf{c}\equiv(\mathbf{q}^{*},0)$ is a stable equilibrium point for $f$.