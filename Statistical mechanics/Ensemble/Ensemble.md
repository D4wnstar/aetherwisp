An **ensemble** or **statistical ensemble** is a collection of identical copies of a mechanical [[Physical system|system]] characterized by a **density function** $\rho(p,q,t)$ defined in the [[phase space]] of the system.
### Detailed description
Consider a gas of $N$ [[particella|particles]], each with position $\mathbf{q}$ and momentum $\mathbf{p}$. In three dimensions, each particles has six variables, so for a system of $N$ particles, we are working with a $6N$-dimensional [[Phase space|phase space]] $\Gamma$. This is, of course, impossible to solve analytically.

The system as a whole, when subject to known macroscopic conditions, is set in a measurable *macroscopic state* (as we know from thermodynamics), but internally it contains numerous *microscopic states* (as we know from atomic or particle physics). The collection of internal microscopic states is said to be an **ensemble**, which can be thought of as "variants" of the internal state that are equivalent to each other and lead to the same macroscopic state. In other words, an ensemble is the collection of microscopic states that lead to the same macroscopic state and are therefore entirely interchangeable with each other.

Each ensemble is described by a **density function** $\rho(\mathbf{p},\mathbf{q},t)$, with $\mathbf{q}=(q_{1},\ldots,q_{3N})$ and $\mathbf{p}=(p_{1},\ldots,p_{3N})$. Integration of this function over a region of the phase space (i.e. over $d^{3N}q\,d^{3N}p$) returns the number of representative points (i.e. microscopic states) found that region at a time $t$.
### Properties
The total number of microscopic states in an ensemble is conserved (as is the number of representative points).

The [[probability]] per unit phase space of finding the system in $dp\,dq$ at time $t$ is
$$\text{Prob}=\frac{\rho(p,q,t)}{\int \rho(p,q,t)\,dp\,dq}$$
The *ensemble average* of a physical quantity $O(p,q)$ is defined as the [[thermodynamic limit]]
$$\langle O \rangle =\frac{\int\rho(p,q,t)O(q,p)\,dp\,dq}{\int \rho(p,q,t)\,dp\,dq}$$
