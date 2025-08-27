---
wiki-publish: true
---
The **Hartree-Fock method** is a [[variational method]] that uses a [[Slater determinant]] of single-[[Particle|particle]] [[Funzione d'onda|wavefunctions]] as a trial function. It is used to solve many [[fermion]] systems, such as the [[many-electron atom]].
### Description
The method starts by claiming that the state of the system is described by a Slater determinant
$$\Psi(q_{1},q_{2},\ldots,q_{N})=\frac{1}{\sqrt{ N! }}\begin{vmatrix}
u_{\alpha}(q_{1}) & u_{\beta}(q_{1}) & \ldots & u_{\nu}(q_{1}) \\
u_{\alpha}(q_{2}) & u_{\beta}(q_{2}) & \ldots & u_{\nu}(q_{2}) \\
\vdots \\
u_{\alpha}(q_{N}) & u_{\beta}(q_{N}) & \ldots & u_{\nu}(q_{N})
\end{vmatrix}$$
where $u(q)$ are the single-particle wavefunctions, which are assumed to be [[Orthonormality|orthonormal]] to each other, $\braket{ u_{\lambda} | u_{\mu} }=\delta_{\lambda \mu}$. As per the variational method, the [[energy]] is this state is the minimum of the [[functional]]
$$E[\Psi]=\braket{ \Psi | \hat{H}| \Psi } $$
A given [[Hamiltonian]] $\hat{H}$ can be split in an independent term $\hat{H}_{1}$ and an interaction term $\hat{H}_{2}$ in the form $\hat{H}=\hat{H}_{1}+\hat{H}_{2}$. $\hat{H}_{1}$ is given by a sum of single-particle Hamiltonians $\hat{h}_{i}$, whereas $\hat{H}_{2}$ is a sum of interaction terms dependent on the distance between particles. It consists of doing the typical variational method workflow using the Slater determinant as a trial function.

The energy in $\hat{H}_{1}$ is
$$\braket{ \Psi |\hat{H}_{1}|\Psi  }=\sum_{\lambda}\braket{ u_{\lambda}(q_{i}) | \hat{h}_{i} | u_{\lambda}(q_{i}) }  =\sum_{\lambda}\mathcal{I}_{\lambda}$$
Meanwhile, the energy in $\hat{H}_{2}$ is
$$\begin{align}
\braket{ \Psi | \hat{H}_{2} | \Psi } &=\frac{1}{2}\sum_{\lambda}\sum_{\mu}\left[ \left\langle  u_{\lambda}(q_{i})u_{\mu}(q_{j})| \frac{1}{r_{ij}} | u_{\lambda}(q_{i})u_{\mu}(q_{j})  \right\rangle \right. \quad&(\text{direct term }\mathcal{F}_{\lambda \mu})\\
 &\left.- \left\langle  u_{\lambda}(q_{i})u_{\mu}(q_{j})| \frac{1}{r_{ij}} | u_{\mu}(q_{i})u_{\lambda}(q_{j})  \right\rangle  \right]&(\text{exchange term } \mathcal{K}_{\lambda \mu})
\end{align}$$
The total energy to minimize then is
$$\boxed{E[\Psi]=\sum_{\lambda}\mathcal{I}_{\lambda}+ \frac{1}{2}\sum_{\lambda}\sum_{\mu}[\mathcal{F}_{\lambda \mu}-\mathcal{K}_{\lambda \mu}]}$$
If we impose stationariety on this functional we can obtain a set of single-particle [[Equazione agli autovalori|eigenvalue equations]]
$$\boxed{\left[ \hat{h}_{i}+\sum_{\mu}V_{\text{direct}}^{\mu}(q_{i})-\sum_{\mu}V_{\text{exchange}}^{\mu}(q_{i}) \right]u_{\lambda}(\mathbf{r}_{i})=E_{\lambda}u_{\lambda}(q_{i})}$$
where
$$\begin{align}
V_\text{direct}^{\mu}(\mathbf{r}_{i})&=\int u_{\mu}^{*}(\mathbf{r}_{j}) \frac{1}{r_{ij}} u_{\mu}(\mathbf{r}_{j})dq_{j} \\
V_\text{exchange}^{\mu}(q_{i})u_{\lambda }(q_{i})&=\left[  \int u_{\mu}^{*}(q_{j}) \frac{1}{r_{ij}}u_{\lambda}(q_{j})dq_{j}\right]u_{\mu}(q_{i})
\end{align}$$
These are known as the **Hartree-Fock equations**. They can be solved computationally through an iterative algorithm.