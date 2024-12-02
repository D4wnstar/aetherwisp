The **partition function** of an [[ensemble]] is the [[Normalizzazione|normalization]] factor of the [[probability density function]] for the [[stato|states]]. It's usually denoted using $Z$, which comes from German "Zustandsumme" or $Q_{N}$ (in Huang's).
### Properties
It acts as the normalization constant of a set of probabilities.
$$p(n)=\frac{1}{Z}e^{-E(n)/k_{B}T}\qquad Z=\sum_{n} e^{-E(n)/k_{B}T}$$
This can be extended to statistical ensembles by seeing $p$ as the density function $\rho$ and $E$ as the [[Hamiltonian]] $H$.

For independent [[Physical system|systems]], partition functions multiply. That is, the partition function of two systems that do not interact is
$$Z=Z_{1}Z_{2}$$
This is because the [[energy]] of the combined system is just the sum of the energy of each system:
$$\begin{align}
Z&=\sum_{n}\sum_{m}e^{-\beta(E_{n}^{(1)}+E_{m}^{(2)})}=\sum_{n}\sum_{m}e^{-\beta E_{n}^{(1)}}e^{-\beta E_{m}^{(n)}} =\sum_{n}e^{-\beta E_{n}^{(1)}}\sum_{m}e^{-\beta E_{m}^{(2)}}=Z_{1}Z_{2}
\end{align}$$
