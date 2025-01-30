The **Fermi-Dirac distribution** is a [[probability distribution]] that describes the behavior of a [[Physical system|system]] of $N$ non-interacting [[Fermion|fermions]] in [[thermal equilibrium]]. Its [[probability density function]] is
$$\langle n_{i} \rangle =\frac{1}{e^{\beta(\varepsilon_{i}-\mu)}+1}=\frac{1}{z^{-1}e^{\beta \varepsilon_{i}}+1}$$
$\langle n_{i} \rangle$ is the average number of fermions in the $i$-th single-[[Particella|particle]] [[stato|state]] of energy $\varepsilon_{i}$, $\mu$ is the system's [[chemical potential]], $\beta=1/k_{B}T$ is the inverse temperature, with $k_{B}$ the [[Boltzmann constant]] and $T$ the [[temperature]], and $z$ is the [[fugacity]]. The [[Normalizzazione|normalization]] constant is
$$\sum_{i}n_{i}=N$$
Since we are working with fermions, the [[Pauli exclusion principle|Pauli exclusion principle]] must hold, which is to say that $\langle n_{i} \rangle< 1$. In fact, at low temperatures, this causes the distribution to approach the [[Heaviside step function]] according to the limit
$$\lim_{ T \to 0 } \langle n_{i} \rangle=\Theta(\mu-\varepsilon_{i})$$

![[Fermi-Dirac distribution at low temperatures.png]]
*From David Tong's lecture notes on statistical physics. $E_{F}$ is the [[Fermi energy]].*