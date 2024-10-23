An **ensemble** or **statistical ensemble** is a collection of identical copies of a mechanical [[Physical system|system]] characterized by a **density function** $\rho(p,q,t)$ defined in the [[phase space]] of the system.
### Detailed description
Consider a gas of $N$ [[particella|particles]], each with position $\mathbf{q}$ and momentum $\mathbf{p}$. In three dimensions, each particles has six variables, so for a system of $N$ particles, we are working with a $6N$-dimensional [[Phase space|phase space]] $\Gamma$. This is, of course, impossible to solve analytically.

The system as a whole, when subject to known macroscopic conditions, is set in a measurable *macroscopic state* (as we know from thermodynamics), but internally it contains numerous *microscopic states* (as we know from atomic or particle physics). The collection of internal microscopic states is said to be an **ensemble**, which can be thought of as "variants" of the internal state that are equivalent to each other and lead to the same macroscopic state. In other words, an ensemble is the collection of microscopic states that lead to the same macroscopic state and are therefore entirely interchangeable with each other.

Each ensemble is described by a **density function** $\rho(p,q,t)$, with $q=(q_{1},\ldots,q_{3N})$ and $p=(p_{1},\ldots,p_{3N})$. Integration of this function over a region of the phase space (i.e. over $d^{3N}q\,d^{3N}p$) returns the number of representative points (i.e. microscopic states) found that region at a time $t$.
### Properties
The total number of microscopic states in an ensemble is conserved (as is the number of representative points).

The [[probability]] per unit phase space of finding the system in $dp\,dq$ at time $t$ is
$$\text{Prob}=\frac{\rho(p,q,t)}{\int \rho(p,q,t)\,dp\,dq}$$
The *ensemble average* of a [[variabile dinamica|dynamic variable]] $O(p,q)$ is defined as the [[thermodynamic limit]]
$$\langle O \rangle =\frac{\int\rho(p,q,t)O(q,p)\,dp\,dq}{\int \rho(p,q,t)\,dp\,dq}$$
Note how $\langle O \rangle$ is on average time dependent, as it depends on $\rho(p,q,t)$. Knowing when $\langle O \rangle$ isn't time dependent can be useful. For instance, if $\rho$ is itself time independent ($\rho(p,q)$ instead of $\rho(p,q,t)$), then $\langle O \rangle$ is pretty naturally also independent. But then the question is when does $\rho$ not depend on time? One such case is when
$$\rho(p,q)=\rho'(H(p,q))$$
where $H$ is the [[Hamiltoniana|Hamiltonian]] of the system. In this case the prime means [[Differenziabilità|differentiation]]. In fact, if this is true then
$$\frac{ \partial \rho }{ \partial t } =-\sum_{i=1}^{3N} \left( \frac{ \partial \rho' }{ \partial H } \frac{ \partial H }{ \partial q_{i} } \frac{ \partial H }{ \partial p_{i} } -\frac{ \partial \rho' }{ \partial H } \frac{ \partial H }{ \partial p_{i} } \frac{ \partial H }{ \partial q_{i} }  \right)=0$$
