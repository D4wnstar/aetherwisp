An **ensemble** or **statistical ensemble** is a collection of identical copies of a mechanical [[Physical system|system]] characterized by a **density function** $\rho(\mathbf{q},\mathbf{p},t)$ defined in the [[phase space]] of the system.

The most common ensembles are the [[microcanonical ensemble]], the [[canonical ensemble]]and the [[grand canonical ensemble]]. They differ in the following points:
- The **microcanonical** is [[Physical system|isolated]] from the environment.
- The **canonical** is not isolated and is subject to [[energy]] fluctuations. It is linked to a [[heat reservoir]] so that those fluctuations are temporary.
- The **grand canonical** is not isolated and is subject to both energy fluctuations and number of particles fluctuations. It is connected to both a heat reservoir and particle reservoir.

Notably, all ensembles are equivalent to each other and lead to the same physics. The choice of which to use is fundamentally just a matter of which of the above conditions are met by the studied system.
### Detailed description
Consider a gas of $N$ [[particella|particles]], each with position $\mathbf{q}$ and momentum $\mathbf{p}$. In three dimensions, each particles has six variables, so for a system of $N$ particles, we are working with a $6N$-dimensional [[Phase space|phase space]] $\Gamma$. This is, of course, impossible to solve analytically.

The system as a whole, when subject to known macroscopic conditions, is set in a measurable **[[Stato|macrostate]]** (as we know from thermodynamics), but internally it contains numerous **[[Stato|microstates]]** (as we know from atomic or particle physics). The set of all possible combinations of internal microstates is said to be an **ensemble**, which can be thought of as "variants" of the internal state that are equivalent to each other and lead to the same macroscopic state. In other words, an ensemble is the collection of all the microstates that lead to the same macrostate and are therefore entirely equivalent to each other.

Each ensemble is described by a **density function** $\rho(\mathbf{q},\mathbf{p},t)$, with $\mathbf{q}=(q_{1},\ldots,q_{3N})$ and $\mathbf{p}=(p_{1},\ldots,p_{3N})$. Integration of this function over a region of the phase space (i.e. over $d^{3N}q\,d^{3N}p$) returns the number of representative points (i.e. microscopic states) found that region at a time $t$.
### Properties
The total number of microstates in an ensemble is conserved (as is the number of representative points).

The [[probability]] per unit phase space of finding the system in $dp\,dq$ at time $t$ is
$$\text{Prob}=\frac{\rho(\mathbf{q},\mathbf{p},t)}{\int \rho(\mathbf{q},\mathbf{p},t)\,dp\,dq}$$
