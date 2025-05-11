---
wiki-publish: true
---
The **Hartree-Fock method** is a [[variational method]] that uses a [[Slater determinant]] of single-[[Particella|particle]] [[Funzione d'onda|wave functions]] as a trial function. It is used to solve many [[fermion]] systems, such as the [[many-electron atom]].

For a given [[Hamiltonian]] $\hat{H}$, it can be split in an independent term $\hat{H}_{1}$ and an interaction term $\hat{H}_{2}$ in the form $\hat{H}=\hat{H}_{1}+\hat{H}_{2}$. $\hat{H}_{1}$ is given by a sum of single-particle Hamiltonians $\hat{h}_{i}$, whereas $\hat{H}_{2}$ is a sum of interaction terms dependent on the distance between particles. It consists of doing the typical variational method workflow using the Slater determinant as a trial function. The [[energy]] [[Expected value|expected values]] are
$$\braket{ \phi |\hat{H}_{1}|\phi  }=\sum_{\lambda}\braket{ u_{\lambda}(q_{i}) | \hat{h}_{i} | u_{\lambda}(q_{i}) }  =\mathcal{I}_{\lambda}$$
and
$$\begin{align}
\braket{ \phi | \hat{H}_{2} | \phi } &=\frac{1}{2}\sum_{\lambda}\sum_{\mu}\left[ \left\langle  u_{\lambda}(q_{i})u_{\mu}(q_{j})| \frac{1}{r_{ij}} | u_{\lambda}(q_{i})u_{\mu}(q_{j})  \right\rangle \right. \quad&(\text{direct term }\mathcal{F}_{\lambda \mu})\\
 &\left.- \left\langle  u_{\lambda}(q_{i})u_{\mu}(q_{j})| \frac{1}{r_{ij}} | u_{\mu}(q_{i})u_{\lambda}(q_{j})  \right\rangle  \right]&(\text{exchange term } \mathcal{K}_{\lambda \mu})
\end{align}$$
The direct/exchange term division is similar to what happens in the [[two electron atom]]. The total energy is
$$E[\phi]=\sum_{\lambda}\mathcal{I}_{\lambda}+ \frac{1}{2}\sum_{\lambda}\sum_{\mu}[\mathcal{F}_{\lambda \mu}-\mathcal{K}_{\lambda \mu}]$$
