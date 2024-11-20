The **quantum microcanonical ensemble** is the quantum extension of the [[microcanonical ensemble]]. Its [[Matrice di densità|density matrix]] is
$$\hat{\rho}=\sum_{E<E_{n}<E+\Delta}\ket{\phi_{n}} \bra{\phi_{n}} $$
where $E$ is the [[energy]] of the system, $\Delta\ll E$ is a small energy amount to account for small fluctuations, $\ket{\phi_{n}}$ are the [[Equazione agli autovalori|eigenstates]] of the [[Physical system|system]] and $E_{n}$ are the energy eigenvalues. Compared to the general case (see [[Quantum statistical mechanics]]), the $\lvert b_{n} \rvert^{2}$ coefficients are all [[Normalizzazione|normalized]]. The counting function $\Gamma(E)$ is
$$\Gamma(E)=\sum_{n}\rho_{nn}=\text{Tr}(\hat{\rho})$$
where $\text{Tr}$ is the [[Traccia|trace]]. Notably, it does not suffer from the [[Gibbs paradox]], unlike its classical sibling.
### Properties
The [[entropy]] is the same as the classical case
$$S=k_{B}\log \Gamma(E)$$
where $k_{B}$ is the [[Boltzmann constant]].