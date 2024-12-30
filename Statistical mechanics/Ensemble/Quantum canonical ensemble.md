The **quantum canonical ensemble** is the quantum extension of the [[canonical ensemble]]. It is defined through the [[Matrice di densità|density matrix]]
$$\hat{\rho}=e^{-\beta \hat{H}}$$
where $\hat{H}$ is the [[Hamiltonian]] of the [[Physical system|system]] and $\beta=1/k_{B}T$, with $k_{B}$ the [[Boltzmann constant]] and $T$ the [[temperature]]. The elements of the matrix in the [[Stato stazionario|energy eigenstate]] [[base|basis]] are $\rho_{n}=e^{-\beta E_{n}}$, where $E_{n}$ are the energy [[Equazione agli autovalori|eigenvalues]].
### Partition function
The [[partition function]] is
$$Q_{N}=\text{Tr}(\hat{\rho})=\sum_{n}e^{-\beta E_{n}}$$
The sum notation holds only if we represent $\hat{\rho}$ in the energy eigenstate [[base|basis]], which is generally a bad choice as it's almost never possible to [[diagonalizzazione|diagonalize]] $\hat{H}$. It is possible in an [[ideal gas]], however.
### Internal energy
The internal energy
$$U=\langle \hat{H} \rangle =-\frac{ \partial  }{ \partial \beta } \ln Z,\qquad\text{var}(U)=\frac{ \partial ^{2} }{ \partial \beta ^{2} }\ln Z=-\frac{ \partial U  }{ \partial \beta } $$
### Helmholtz free energy
The [[Helmholtz free energy]] is
$$A=-k_{B}T\ln Z$$
### Entropy
Since we know the state density, we can determine [[entropy]] from the [[Entropy (information theory)|information-theoretical one]] as
$$S=-k_{B}\sum_{n} p(n) \ln p(n)=\frac{k_{B}\beta}{Z}\sum_{n}E_{n}e^{-\beta E_{n}}+k_{B}\ln Z$$
since $p(n)=\rho_{n}/Z=e^{-\beta E_{n}}/Z$. It can equivalently be expressed as
$$S=k_{B}\frac{ \partial  }{ \partial T }(T\ln Z) $$
### Examples
> [!example] Non-interacting two state system
> Consider a single particle with two possible states, one with energy $E_{0}=0$ and another with energy $E_{1}=E$. The partition function for this single-particle system is
> $$Z_{1}=\sum_{n}e^{-\beta E_{n}}=1+e^{-\beta E}=2e^{-\beta E/2}\cosh\left( \frac{\beta E}{2} \right)$$
> We want to find the partition function for a system of $N$ of these particles. If the particles are not coupled (that is, they do not interact), the total partition function is just the product of each particle's partition function:
> $$Z=\prod_{i=1}^{N} Z_{i}=2^{N}e^{-N\beta E/2}\cosh^{N}\left( \frac{\beta E}{2} \right)$$
> The average [[energy]] is
> $$\langle E \rangle =-\frac{ \partial  }{ \partial \beta } \ln Z=\frac{NE}{2}\left( 1-\tanh\left( \frac{\beta E}{2} \right) \right)=\frac{NE}{e^{\beta E}+1}$$
> The last step just comes from applying the exponential definition of the $\tanh$ and simplifying things. This result is identical to the one found with the [[microcanonical ensemble]]. Notably, this was way easier, as we didn't have to use combinatorics at all.
