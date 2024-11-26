**Entropy** $S$ is a measurement of uniformity and disorder of a system. In Clausius' words, it is the "amount of transformation of a system". In differential form it is defined as
$$dS=\frac{\delta Q_{\text{rev}}}{T}=k_{B}\ dS_\text{it}$$
where $Q_\text{rev}$ is the [[heat]] exchanged by a reversible [[thermodynamic transformation]] and $T$ is [[temperature]]. $S_\text{it}$ is the [[entropy (information theory)|information theory entropy]], which becomes thermodynamic entropy when weighed by the [[Boltzmann constant|Boltzmann constant]] $k_{B}$. Notably, $dS$ is an [[exact differential]], unlike $\delta Q$, which usually isn't.

Entropy is defined up to an additive constant and the difference between two [[stato|states]] $A$ and $B$ connected by a reversible transformation is
$$\Delta S=S(B)-S(A)\equiv \int_{A}^{B} \frac{\delta Q}{T}$$
By [[Clausius' theorem]], $\Delta S$ is independent of path, so long it is reversible.
### Irreversible transformations
To understand the effects of an irreversible transformation, let's define two paths, $P$ and $R$, between the same end states. $P$ is not reversible, $R$ is. The combined process $P-R$ forms an irreversible cycle. Invoking Clausius' theorem again, we know that $\int_{P-R}\delta Q/T\leq 0$, which in turn means
$$\int_{P} \frac{\delta Q}{T}\leq \int_{R} \frac{\delta Q}{T}=\Delta S$$
since the right-hand integral is the entropy variation defined above. In other words, for an irreversible path $P$ between $A$ and $B$, we have
$$\Delta S=S(B)-S(A)\geq \int_{A}^{B} \frac{\delta Q}{T}$$
If we are working in an [[Physical system|isolated system]], $\delta Q=0$ and so we get
$$\Delta S\geq 0$$
which means that the entropy of an isolated system can only increase or, at most, remain constant if all transformations are reversible. Since the [[Universo|Universe]] is considered and isolated system, that means that the global entropy of the Universe can only increase.
### From heat capacity
Entropy can be measure starting from [[heat capacity]] $C(T)$, as
$$\frac{C(T)}{T}=\frac{ \partial S }{ \partial T } $$
This is a convenient way to measure entropy differences experimentally, as we can see by inverting the formula:
$$\Delta S=\int_{T_{1}}^{T_{2}} \frac{C(T)}{T}dT$$
With an experimental [[Parameter estimation|fit]] of $C(T)$, we can perform consistency tests on the theory. Also, if we take the second derivative of $S$ in terms of $E$ we get
$$\frac{ \partial ^{2}S }{ \partial E^{2} } =- \frac{1}{T^{2}C}$$
The second derivative of entropy is negative if heat capacity is positive, which it almost always is[^1]. If $C>0$, the system is said to be **thermodynamically stable**. The reason is that the [[Laws of thermodynamics|second law of thermodynamics]] requires us to maximize entropy during heat exchange. For that to be true, the post-exchange entropy needs to be at a [[Punto critico|stationary point]] $\frac{ \partial S }{ \partial E }=0$[^2] and the second derivative needs to be negative, $\frac{ \partial ^{2}S }{ \partial E^{2} }<0$, which it is if the heat capacity of both participating systems is positive.
### Etymology
The word "entropy" was coined by Clausius starting from the Greek work $\tau \rho o\pi \eta$ (tropi) which means "transformation". The "en" comes from "energy". It was added as a prefix to make the word as similar as possible to energy due to them being intrinsically linked.

[^1]: The big exceptions are [[Buco nero|black holes]].
[^2]: For proof, see [[Entropy (information theory)#Second law of thermodynamics]].