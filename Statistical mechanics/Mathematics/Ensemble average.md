The **ensemble average** of a [[dynamical variable]] $O(\mathbf{q},\mathbf{p})$ over an [[ensemble]] is the weighted average over all possible [[stato|macrostates]] of the [[Physical system|system]] in the [[Thermodynamic limit]]:
$$\langle O \rangle =\frac{\int\rho(\mathbf{q},\mathbf{p},t)O(\mathbf{q},\mathbf{p})\,dp\,dq}{\int \rho(\mathbf{q},\mathbf{p},t)\,dp\,dq}$$
where $\rho$ is the density function of the ensemble. In the quantum case, for a [[Operatore autoaggiunto|Hermitian operator]] $\hat{O}(\hat{q},\hat{p})$ and a [[base|basis]] of [[Equazione agli autovalori|eigenstates]] $\{ \ket{n} \}_{n\in \mathbb{N}}$, it is
$$\langle \hat{O} \rangle =\sum_{n}p(n)\braket{ n | \hat{O}(\hat{q},\hat{p}) | n } $$
where $p(n)$ is the [[probability]] of being in the macrostate $\ket{n}$[^1]. Note that this is just the weighted sum of state averages $\braket{ n | \hat{O} | n }$ where the likeliness of each state is the weight.
### Time independence
Note how $\langle O \rangle$ is in general time dependent, as it depends on $\rho(\mathbf{q},\mathbf{p},t)$. When $\langle O \rangle$ does not depend on time, the system is in [[thermal equilibrium]]. Knowing when $\langle O \rangle$ isn't time dependent can be useful. For instance, if $\rho$ is itself time independent ($\rho(\mathbf{q},\mathbf{p})$ instead of $\rho(\mathbf{q},\mathbf{p},t)$), then it follows that $\langle O \rangle$ is itself independent. But then the question is when does $\rho$ not depend on time? One such case is when
$$\rho(\mathbf{q},\mathbf{p})=\rho'(H(\mathbf{q},\mathbf{p}))$$
where $H$ is the [[Hamiltoniana|Hamiltonian]] of the system. In this case the prime means [[Differenziabilità|differentiation]]. In fact, if this is true then
$$\frac{ \partial \rho }{ \partial t } =-\sum_{i=1}^{3N} \left( \frac{ \partial \rho' }{ \partial H } \frac{ \partial H }{ \partial q_{i} } \frac{ \partial H }{ \partial p_{i} } -\frac{ \partial \rho' }{ \partial H } \frac{ \partial H }{ \partial p_{i} } \frac{ \partial H }{ \partial q_{i} }  \right)=0$$

[^1]: Note that this probability has nothing to do with [[Indeterminatezza quantistica|quantum indeterminacy]].