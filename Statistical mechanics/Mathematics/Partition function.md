---
aliases:
  - canonical partition function
  - grand canonical partition function
---
The **partition function** of an [[ensemble]] is the [[Normalizzazione|normalization]] factor of the [[probability density function]] $\rho$ for the [[stato|states]]. It includes the statistical properties of a system in [[thermal equilibrium]] and most thermodynamic variables, like [[temperature]] and [[entropy]], can be derived from it directly or from its derivatives. It is the sum of the density function over all possible states:
$$Z=\int\rho(\mathbf{q},\mathbf{p})\ d^{3N}q\ d^{3N}p,\qquad Z=\sum_{n}\hat{\rho}(\hat{q},\hat{p})=\text{Tr}(\hat{\rho})$$
The first case is the classical one, where integration happens over all [[phase space]]. The second is the quantum case, which instead uses the [[Matrice di densità|density matrix]] and its [[Traccia|trace]].

It is usually denoted using $Z$, which comes from German "Zustandsumme", or $Q_{N}$ (in Huang's). The most common partition functions are the **canonical partition function** of the [[canonical ensemble]] $Q_{N}$ and the **grand canonical partition function** of the [[grand canonical ensemble]] $\mathcal{Z}$. Their expressions change depending on whether we are consider the classical or quantum ensemble and whether [[Particella|particles]] are [[Identical particles|distinguishable]] or not.
### Properties
The probability of a state in an ensemble is given by the density function normalized by the partition function
$$p(n)=\frac{\rho}{Z}$$
For independent [[Physical system|systems]], partition functions multiply. That is, the partition function of two systems that do not interact is
$$Z=Z_{1}Z_{2}$$
This is because the [[energy]] of the combined system is just the sum of the energy of each system:
$$\begin{align}
Z&=\sum_{n}\sum_{m}e^{-\beta(E_{n}^{(1)}+E_{m}^{(2)})}=\sum_{n}\sum_{m}e^{-\beta E_{n}^{(1)}}e^{-\beta E_{m}^{(n)}} =\sum_{n}e^{-\beta E_{n}^{(1)}}\sum_{m}e^{-\beta E_{m}^{(2)}}=Z_{1}Z_{2}
\end{align}$$
### Derived quantities
The [[internal energy]] of a system is
$$U=-\frac{ \partial  }{ \partial \beta } \ln Z$$
where $\beta=1/k_{B}T$ with $k_{B}$ the [[Boltzmann constant]] and $T$ the [[temperature]]. The [[Helmholtz free energy]] is
$$Z=e^{-\beta A}\quad\Rightarrow \quad A=- \frac{1}{\beta} \ln Z$$
The [[entropy]] is
$$S=k_{B}\frac{ \partial  }{ \partial T }(T\ln Z) $$
