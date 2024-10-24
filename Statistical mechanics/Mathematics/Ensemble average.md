The **ensemble average** of a [[dynamical variable]] $O(\mathbf{q},\mathbf{p})$ over an [[ensemble]] is the weighted average over all possible [[stato|states]] of the [[Physical system|system]] in the [[thermodynamic limit]]:
$$\langle O \rangle =\frac{\int\rho(\mathbf{q},\mathbf{p},t)O(\mathbf{q},\mathbf{p})\,dp\,dq}{\int \rho(\mathbf{q},\mathbf{p},t)\,dp\,dq}$$
where $\rho$ is the density function of the ensemble.

Note how $\langle O \rangle$ is on average time dependent, as it depends on $\rho(\mathbf{q},\mathbf{p},t)$. Knowing when $\langle O \rangle$ isn't time dependent can be useful. For instance, if $\rho$ is itself time independent ($\rho(\mathbf{q},\mathbf{p})$ instead of $\rho(\mathbf{q},\mathbf{p},t)$), then $\langle O \rangle$ is pretty naturally also independent. But then the question is when does $\rho$ not depend on time? One such case is when
$$\rho(\mathbf{q},\mathbf{p})=\rho'(H(\mathbf{q},\mathbf{p}))$$
where $H$ is the [[Hamiltoniana|Hamiltonian]] of the system. In this case the prime means [[Differenziabilità|differentiation]]. In fact, if this is true then
$$\frac{ \partial \rho }{ \partial t } =-\sum_{i=1}^{3N} \left( \frac{ \partial \rho' }{ \partial H } \frac{ \partial H }{ \partial q_{i} } \frac{ \partial H }{ \partial p_{i} } -\frac{ \partial \rho' }{ \partial H } \frac{ \partial H }{ \partial p_{i} } \frac{ \partial H }{ \partial q_{i} }  \right)=0$$
