The **ensemble average** of a [[dynamical variable]] $O(\mathbf{q},\mathbf{p})$ over an [[ensemble]] is the weighted average over all possible [[stato|microstates]] of the [[Physical system|system]] in the [[thermodynamic limit]]:
$$\langle O \rangle =\frac{\int\rho(\mathbf{q},\mathbf{p},t)O(\mathbf{q},\mathbf{p})\,dp\,dq}{\int \rho(\mathbf{q},\mathbf{p},t)\,dp\,dq}=\frac{1}{Z}\int O\rho\ dpdq$$
where $\rho$ is the density function of the ensemble and $Z$ is the [[partition function]]. For discrete states, this becomes
$$\langle O \rangle =\frac{\sum \rho(t)O }{\sum \rho(t)}=\frac{1}{Z}\sum O\rho$$
where the sums go over some label to index the states.

In the quantum case, the average in a system state $\ket{\psi}$ for an [[Osservabile|observable]] $\hat{O}$, expressed in a [[base|basis]] of [[Equazione agli autovalori|eigenstates]] $\{ \ket{n} \}_{n\in \mathbb{N}}$, is
$$\langle \hat{O} \rangle=\frac{\text{Tr}(\hat{O}\hat{\rho})}{\text{Tr}(\hat{\rho})} =\sum_{n}p(n)\braket{ n | \hat{O}| n }$$
where $\hat{\rho}$ is the [[Matrice di densità|density matrix]] of the system and $p(n)$ is the [[probability]] of being in the microstate $\ket{n}$[^1] . Note that this is just the weighted sum of state averages $\braket{ n | \hat{O} | n }$ where the likeliness of each state is the weight. The probabilities can be computed from the coefficients of the [[Serie di Fourier|Fourier series]] expansion of $\ket{\psi}$ in the $\ket{n}$ basis:
$$\ket{\psi} =\sum_{n}c_{n}\ket{n} \quad\to \quad p(n)=\lvert c_{n} \rvert ^{2}$$
### Time independence
Note how $\langle O \rangle$ is in general time dependent, as it depends on $\rho(\mathbf{q},\mathbf{p},t)$. When $\langle O \rangle$ does not depend on time, the system is in [[thermal equilibrium]]. Knowing when $\langle O \rangle$ isn't time dependent can be useful. For instance, if $\rho$ is itself time independent ($\rho(\mathbf{q},\mathbf{p})$ instead of $\rho(\mathbf{q},\mathbf{p},t)$), then it follows that $\langle O \rangle$ is itself independent. But then the question is, when does $\rho$ not depend on time? One such case is when
$$\rho(\mathbf{q},\mathbf{p})=\rho'(H(\mathbf{q},\mathbf{p}))$$
where $H$ is the [[Hamiltoniana|Hamiltonian]] of the system. In this case the prime means [[Differential|differentiation]]. In fact, if this is true then
$$\frac{ d \rho }{ d t } =-\sum_{i=1}^{3N} \left( \frac{ \partial \rho' }{ \partial H } \frac{ \partial H }{ \partial q_{i} } \frac{ \partial H }{ \partial p_{i} } -\frac{ \partial \rho' }{ \partial H } \frac{ \partial H }{ \partial p_{i} } \frac{ \partial H }{ \partial q_{i} }  \right)=0$$
This verifies [[Liouville's theorem]].

[^1]: Note that this probability has nothing to do with [[Indeterminatezza quantistica|quantum indeterminacy]].