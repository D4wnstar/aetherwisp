---
wiki-publish: true
aliases:
  - canonical partition function
  - grand canonical partition function
---
The **partition function** of an [[ensemble]] is the [[Normalization|normalization]] factor of the [[probability density function]] $\rho$ for the [[stato|states]]. It includes the statistical properties of a system in [[thermal equilibrium]] and most thermodynamic variables, like [[temperature]] and [[entropy]], can be derived from it directly or from its derivatives. As such, it is a [[Generating function (physics)|generating function]]. It is the sum of the density function over all possible states:
$$Z=\int\rho(\mathbf{q},\mathbf{p})\ d^{3N}q\ d^{3N}p,\qquad Z=\sum_{n}\hat{\rho}(\hat{q},\hat{p})=\text{Tr}(\hat{\rho})$$
The first case is the classical one, where integration happens over all [[phase space]]. The second is the quantum case, which instead uses the [[Matrice di densità|density matrix]] and its [[Traccia|trace]].

It is usually denoted using $Z$, which comes from German "Zustandsumme", or $Q_{N}$. The most common partition functions are the **canonical partition function** of the [[canonical ensemble]] $Q_{N}$ and the **grand canonical partition function** of the [[grand canonical ensemble]] $\mathcal{Z}$. Their expressions change depending on whether we are consider the classical or quantum ensemble and whether [[Particella|particles]] are [[Identical particles|distinguishable]] or not.
### Properties
The probability of a state in an ensemble is given by the density function normalized by the partition function
$$p(n)=\frac{\rho(n)}{Z}$$
For independent and classical [[Physical system|systems]], canonical partition functions multiply. That is, the partition function of two systems that do not interact is
$$Z=Z_{1}Z_{2}$$
This is because the [[energy]] of the combined system is just the sum of the energy of each system:
$$\begin{align}
Z&=\sum_{n}\sum_{m}e^{-\beta(E_{n}^{(1)}+E_{m}^{(2)})}=\sum_{n}\sum_{m}e^{-\beta E_{n}^{(1)}}e^{-\beta E_{m}^{(n)}} =\sum_{n}e^{-\beta E_{n}^{(1)}}\sum_{m}e^{-\beta E_{m}^{(2)}}=Z_{1}Z_{2}
\end{align}$$
More generally, for $N$ independent components equipped with the same partition function $Z_{1}$, we have
$$Z=Z_{1}^{N}$$

In quantum systems however, this is no longer true due to the [[Funzione d'onda|wavefunction]] constraints of [[Fermion|fermions]] and [[Boson|bosons]] and, more specifically, their [[Identical particles|indistinguishability]]. For bosons, every combination of states is permitted, but we don't want to overcount states that only differ by a [[permutation]]. To express this mathematically, nested sums now begin at the previous index:
$$Z=\sum_{n}\sum_{m\geq n}e^{-\beta(E_{n}^{(1)}+E_{m}^{(2)})}\quad\text{(Bosons)}$$
The sums are no longer independent, so we cannot solve them separately like in the classical case. The solution now depends on the shape of $E_{n}$. For fermions, particles also cannot simultaneously occupy the same state due to the [[Pauli exclusion principle]], so the greater-or-equals becomes a simple greater:
$$Z=\sum_{n}\sum_{m>n}e^{-\beta(E_{n}^{(1)}+E_{m}^{(2)})}\quad\text{(Fermions)}$$
Because of these constraints, solving quantum partition functions can be much more involved than classical ones. In practice, it shows that quantum systems are effectively never independent from each other, even if there are no formal interactions between components. For an abstract exercise on quantum state counting, see [[Occupation number#Average occupation]].

To compute these sums, it is typically useful to consider the [[Serie geometrica|geometric series]] and some simple generalizations:
$$\sum_{n=1}^{\infty} x^{n}=\frac{1}{1-x},\qquad \sum_{n\geq m}^{\infty} x^{n}=\frac{x^{m}}{1-x},\qquad \sum_{x>m}^{\infty} \frac{x^{m+1}}{1-x}$$
### Derived quantities
In general, the [[ensemble average]] of a quantity $O$ can be derived as
$$\langle O \rangle=\frac{1}{Z}\sum O\rho(O) $$
where summation (or integration, if continuous) happens over all states. If there exists an $x$ for which
$$O\rho(O)=\frac{ \partial  }{ \partial x } \rho(O)$$
is true, then the ensemble average can be rewritten as
$$\langle O \rangle =\frac{ \partial  }{ \partial x } \ln Z$$
This can be seen, for instance, in the [[internal energy]] of a system (where $x=-\beta$):
$$U=-\frac{ \partial  }{ \partial \beta } \ln Z$$
where $\beta=1/k_{B}T$ with $k_{B}$ the [[Boltzmann constant]] and $T$ the [[temperature]].

The canonical partition function is related to the [[Helmholtz free energy]] by
$$Q_{N}=e^{-\beta A}\quad\Rightarrow \quad A=- \frac{1}{\beta} \ln Q_{N}$$
Using [[Maxwell relations]], this leads to an expression for [[entropy]]:
$$S=k_{B}\frac{ \partial  }{ \partial T }(T\ln Q_{N}) $$
