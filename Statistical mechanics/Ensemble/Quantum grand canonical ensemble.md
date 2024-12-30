The **quantum grand canonical ensemble** is the quantum extension of the [[grand canonical ensemble]]. Its [[Matrice di densità|density matrix]] is
$$\hat{\rho}=z^{N}Q_{N}(V,T)$$
where $Q_{N}$ is the quantum [[Partition function|canonical partition function]].
### Partition function
Its [[partition function]] is
$$\mathcal{Z}(z,V,T)=\sum_{N=0}^{\infty}z^{N}Q_{N}(V,T)=\text{Tr}(e^{-\beta(\hat{H}-\mu \hat{N})})$$
where $z$ is the [[fugacity]], $V$ is the volume, $\beta=1/k_{B}T$ with $k_{B}$ is the [[Boltzmann constant]] and $T$ is the [[temperature]], $\hat{H}$ is the [[Hamiltonian]] of the [[Physical system|system]], $\mu$ is the [[chemical potential]] and $\hat{N}$ is the [[particella|particle]] number [[Operatore|operator]].
### Bosons and fermions
The partition function takes on different forms for [[Boson|bosons]] and [[Fermion|fermions]]. We get
$$\mathcal{Z}(z,V,T)=\left\{\begin{align}
\text{(Bosons)}\quad &\prod_{\mathbf{p}} \frac{1}{1-ze^{-\beta \varepsilon_{p}}} \\
\text{(Fermions)}\quad &\prod_{\mathbf{p}} (1+ze^{-\beta \varepsilon_{p}})
\end{align}\right.$$
