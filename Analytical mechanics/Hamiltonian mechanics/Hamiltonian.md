---
wiki-publish: true
---
The **Hamiltonian** $H$ of a [[conservative system]] is the [[Laplace transform]] of the [[Lagrangian]] $L$:
$$H(p,q,t)\equiv\left.{(\mathbf{p}\cdot \dot{\mathbf{q}}-L(q,\dot{q},t))}\right|_{\dot{q}_{i}=u_{i}(p,q,t)}$$
$\mathbf{q}$ are the [[generalized coordinates]] and $\mathbf{p}$ are the [[conjugate momenta]]. In mechanical systems, it coincides with the total [[energy]]:
$$H=T+V$$
where $T$ is the [[kinetic energy]] and $V$ is the [[potential energy]]. The Hamiltonian changes in the opposite sense as the Lagrangian:
$$\frac{ \partial H }{ \partial t } =-\frac{ \partial L }{ \partial t } $$

The Hamiltonian is used in the [[Hamilton equations]] of the system to find its trajectory.
### Examples
> [!example] Point mass
> The kinetic and potential energies are
> $$T=\frac{m}{2}(\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2}),\quad V\equiv V(x,y,z)$$
> for some potential energy $V$. The Lagrangian is $L=T-V$. We want to show that the Hamiltonian is instead $H=T+V$. To do that, we'll express the kinetic energy in terms of the [[Linear momentum|momentum]] instead of velocity:
> $$p_{x}=\frac{ \partial L }{ \partial \dot{x} } =m \dot{x},\quad p_{y}=\frac{ \partial L }{ \partial \dot{y} } =m \dot{y},\quad p_{z}=\frac{ \partial L }{ \partial \dot{z} } =m \dot{z}$$
> Hence
> $$H=\frac{m}{2}\left( \frac{p_{x}^{2}}{m^{2}}+ \frac{p_{y}^{2}}{m^{2}}+ \frac{p_{z}^{2}}{m^{2}}\right)+V(x,y,z)=\frac{\mathbf{p}^{2}}{2m}+V(\mathbf{x})$$
> The grand majority of Hamiltonians in physics have this form: $\mathbf{p}^{2}/2m$ plus a potential. This is because [[Cartesian coordinates]] are ubiquitous, as is considering point masses as objects, but it is a matter of "habit". This is not, *in general*, the shape of a Hamiltonian, as that depends on other factors such as the choice of coordinates. It just happens to be an overwhelmingly common specific case.

> [!example] Harmonic oscillator
> Using the same process of expressing kinetic energy in terms of momentum, the Hamiltonian of a (one-dimensional) [[harmonic oscillator]] is
> $$H=\frac{p^{2}}{2m}+ \frac{1}{2}m\omega ^{2}q^{2}$$

> [!example] Electromagnetic force
> The Lagrangian of a point mass under a [[Lorentz force]] is
> $$L=\frac{m}{2}\dot{\mathbf{q}}^{2}+e \dot{\mathbf{q}}\cdot \mathbf{A}-e\phi$$
> where we used the [[electric potential]] $\phi$ and the [[magnetic vector potential]] $\mathbf{A}$. $e$ is the [[electric charge]] (since $q$ is already taken by position). We'll use the [[Lagrange equation]] to find the Hamiltonian through its definition. Firstly,
> $$p_{i}=\frac{ \partial L }{ \partial \dot{q}_{i} } =m \dot{q}_{i}+eA_{i},\quad \dot{q}_{i}=\frac{p_{i}}{m}- \frac{e}{m}A_{i}$$
> and using the Hamiltonian definition
>$$\begin{align}
> H(p,q)&=\mathbf{p}\cdot \dot{\mathbf{q}}-L|_{\dot{\mathbf{q}}=\frac{p_{i}}{m}- \frac{e}{m}A_{i}} \\
> &=\frac{\mathbf{p}^{2}}{m}- \frac{e}{m}\mathbf{A}\cdot \mathbf{p}- \frac{m}{2} \frac{(\mathbf{p}-e\mathbf{A})^{2}}{m^{2}}- \frac{e}{m}(\mathbf{p}-e\mathbf{A})\cdot \mathbf{A}+e\phi \\
> &=\frac{(\mathbf{p}-e\mathbf{A})^{2}}{m}- \frac{(\mathbf{p}-e\mathbf{A})^{2}}{2m}+e\phi \\
> &=\frac{(\mathbf{p}-e\mathbf{A})^{2}}{2m}+e\phi
> \end{align}$$
