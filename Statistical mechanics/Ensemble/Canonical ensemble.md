The **canonical ensemble** is an [[ensemble]] that is not [[Physical system|isolated]] from the environment, but is in [[thermal equilibrium]] with a larger [[Physical system|system]] that acts as a [[heat reservoir]] (i.e., the environment). The [[energy]] is subject to fluctuation, but the number of [[Particella|particles]] is constant. Its density function is
$$\rho(\mathbf{q},\mathbf{p})=e^{-\beta H(\mathbf{q},\mathbf{p})}$$
where $\beta=1/k_{B}T$, $H$ is the [[Hamiltonian]], $k_{B}$ is the [[Boltzmann constant]] and $T$ is the [[temperature]]. The [[Normalizzazione|normalization]] factor is the [[partition function]]
$$Q_{N}(V,T)=\int \frac{e^{-\beta H(\mathbf{q},\mathbf{p})}}{h^{3N}N!} \ d^{3N}q\,d^{3N}p$$

It differs from the [[microcanonical ensemble]], which has constant energy with no fluctuations, and the [[grand canonical ensemble]], which has fluctuations in both energy and particle number. For most solid and liquid systems, the canonical ensemble is the most convenient description, as it takes the interaction with the environment into account. Compared to the microcanonical, energy is derived from the equilibrium temperature instead of the other way around.
### Density function derivation
Let's consider the system (1) and the reservoir (2) separately, each with a large and constant number of particles $N_{1}\gg 1$ and $N_{2}\gg 1$. Combined, they make up an [[Physical system|isolated system]] which can be described by a [[microcanonical ensemble]][^1] of energy $E_{1} + E_{2}$ that obeys
$$E_\text{total}<E_{1}+E_{2}<E_\text{total}+2\Delta$$
where $E_\text{total}$ is the energy of the system + reservoir and $\Delta$ is a small amount of energy (to account for uncertainty). For clarity: $E_\text{total}$ is approximately constant, but $E_{1}$ and $E_{2}$ are *not*. We ignore the interaction between the two system beyond the transfer of energy so that the total Hamiltonian is just a sum
$$H=H_{1}+H_{2}$$
The reservoir's energy and number of particle is taken to be much larger than that of the system, so $E_{2}\gg E_{1}$ and $N_{2}\gg N_{1}$.

Now, we really only care about the state of system 1, regardless of what reservoir 2 is doing. The [[probability]] of system 1 being in a volume element $d\mathbf{q}_{1}d\mathbf{p}_{1}$ centered on $(\mathbf{q}_{1},\mathbf{p}_{1})$ in its own [[phase space]] is proportional to
$$\propto\Gamma_{2}(E_{2})d\mathbf{q}_{1}d\mathbf{p}_{1}=\Gamma_{2}(E_\text{total}-E_{1})d\mathbf{q}_{1}d\mathbf{p}_{1}$$
since $E_{2}$ is the only state the reservoir is likely to be in at equilibrium. The density function of system 1 is going to be determined by its most likely state
$$\rho_{1}(\mathbf{q}_{1},\mathbf{p}_{1})=\Gamma_{2}(E_\text{total}-E_{1})=\Gamma_{2}(E_\text{total}-H_{1}(\mathbf{q}_{1},\mathbf{p}_{1}))$$
We want to find the number of [[Stato|microstates]] for which $E_{1}$ is true, and to do so we can start from the [[Entropy (information theory)|Boltzmann entropy]] formula $S(E_\text{total}-E_{1})=k_{B}\log \Gamma(E_\text{total}-E_{1})$. Remember that $E_{2}\gg E_{1}$, so we can approximate $S(E_\text{total}-E_{1})$ using a [[serie di Taylor|Taylor series]] in $E_\text{total}-E_{1}=E_{2}$ centered in $E_\text{total}$ and truncate at the first order without much error:
$$\begin{align}
k_{B}\log \Gamma_{2}(E_\text{total}-E_{1})&=S_{2}(E_\text{total}-E_{1}) \\
&=S_{2}(E_\text{total})-E_{1}\left.\frac{ \partial S_{2} }{ \partial E_{2} } \right|_{E_{2}=E_\text{total}} +\ldots\\
&\simeq S_{2}(E_{2})- E_{1} \frac{1}{T}
\end{align}$$
where we used the [[Maxwell relations|Maxwell relation]] $\frac{ \partial S_{2} }{ \partial E_{2} }=\frac{1}{T_{2}}$, the fact that $T_{1}=T_{2}=T$ always because that's how reservoirs work and that $E_\text{total}\simeq E_{2}$ since $E_{1}$ is comparatively small. If we pull $\Gamma_{2}$ out we get
$$\Gamma_{2}(E_\text{total}-E_{1})=e^{S_{2}(E_\text{total})/k_{B}}e^{-E_{1}/k_{B}T}=\rho_{1}(\mathbf{q}_{1},\mathbf{p_{1}})$$
The first exponential is a constant, so we can drop it by redefining the normalization constant. By writing $E_{1}=H_{1}(\mathbf{q}_{1},\mathbf{p}_{1})$, using the inverse temperature $\beta=1/k_{B}T$ and dropping the index 1, we can write the density function:
$$\boxed{\rho(\mathbf{q},\mathbf{p})=e^{-\beta H(\mathbf{q},\mathbf{p})}}$$
This is the density function of the canonical ensemble and is an incredibly important result in and out of physics because it essentially encodes a universal method to find a [[stato|state]] of equilibrium from an extremely complex system. In statistical physics, of course, it represents a huge number of particles needing to thermalize. But it may also represent cities in the [[traveling salesman problem]] or many other systems completely detached from physics. The function $H$ here is the [[Hamiltonian]], but it is more generally a [[cost function]] the minimum of which is the most stable equilibrium state.
### Partition function
The [[partition function]] of the canonical ensemble is
$$\boxed{Q_{N}(V,T)=\int \frac{e^{-\beta H(\mathbf{q},\mathbf{p})}}{h^{3N}N!} \ d^{3N}q\,d^{3N}p }$$
The $N!$ comes from correct Boltzmann counting[^2], meanwhile $h^{3N}$ keeps the function dimensionless by canceling the dimensions of $d^{3N}q\,d^{3N}p$. Integration happens over the entire phase space. The following important result also holds:
$$\boxed{Q_{N}(V,T)=e^{-\beta A(V,T)}}$$
where $A=U-TS$ is the [[Helmholtz free energy]] (needs to be proven; see below). Since $A$ is an [[equation of state]], it encodes all information about the system. If one can calculate the partition function, the free energy can be extracted from it, and from the free energy we get everything about the system.

> [!success] The partition function
> The partition function contains all information about the system. Finding it is equivalent to solving the system completely.

> [!example] $A$ is the Helmholtz free energy
> To prove that $A$ in $Q_{N}=e^{-\beta A}$ is the Helmholtz free energy, let's write it explicitly
> $$\int \frac{e^{-\beta H}}{h^{3N}N!} \ d^{3N}q\,d^{3N}p=e^{-\beta A}\quad\to \quad\int \frac{e^{\beta (A-H)}}{h^{3N}N!} \ d^{3N}q\,d^{3N}p=1\tag{1}$$
> If we differentiate by $\beta$ on both sides we get
> $$\int \frac{e^{\beta (A-H)}}{h^{3N}N!}  \left[ A(V,T)+\beta \frac{ \partial A(V,T) }{ \partial \beta } -H(\mathbf{q},\mathbf{p}) \right]\ d^{3N}q\,d^{3N}p=0$$
> The first two terms in the brackets are independent of $q$ and $p$ so we can pull them out of the integral
> $$\left[ A+\beta \frac{ \partial A }{ \partial \beta }  \right]\int \frac{e^{\beta(A-H)}}{h^{3N}N!}dq^{3N}\,dp^{3N}-\int \frac{He^{\beta(A-H)}}{h^{3N}N!} \ dq^{3N}\,dp^{3N}=0$$
> But the first integral is equal to $1$ because of equation $(1)$, whereas the second integral is equal to the internal energy (see below, just using a modified density function because of $A$). As such, we get
> $$A+\beta \frac{ \partial A }{ \partial \beta } -U=0$$
> But since $\beta=1/k_{B}T$ we can write
> $$\beta \frac{ \partial A }{ \partial \beta } =\frac{1}{k_{B}T}\frac{ \partial A }{ \partial T } \frac{ \partial T }{ \partial \beta } =\frac{1}{k_{B}T}\frac{ \partial A }{ \partial T } \frac{1}{k_{B}T} \frac{-1}{\beta ^{2}} T=-T \frac{ \partial A }{ \partial T } $$
> and so
> $$A-T\frac{ \partial A }{ \partial T } -U=0$$
> If $A$ really is the Helmholtz free energy, then the Maxwell relation $\frac{ \partial A }{ \partial T }=-S$ must apply to it:
> $$A+TS-U=0$$
> but this just gives us
> $$A=U-TS$$
> which is exactly the free energy, proving our point.
### Energy
The [[internal energy]] of the system is the [[ensemble average]] of the Hamiltonian
$$U=\langle H \rangle = \frac{\int He^{-\beta H}d\mathbf{q}\,d\mathbf{p}}{\int e^{-\beta H}d\mathbf{q}\,d\mathbf{p}}$$
as $H$ is variable due to fluctuations. We also have
$$U=-\frac{ \partial  }{ \partial \beta } \ln Q_{N}$$
#### Canonical-microcanonical ensemble
The difference between the canonical ensemble and the [[microcanonical ensemble]] is that in the former, energy is allowed to fluctuate, whereas in the latter it is fixed and has no communication with the outside environment.

Let's find how the energy fluctuates by computing its [[variance]] (up to a constant):
$$\text{var}(H)=\langle (U-H)^{2} \rangle =\frac{\int e^{-\beta H}(U-H)^{2} dq\,dp}{Q_{N}}$$
(???)
$$\frac{ \partial U }{ \partial \beta } +\langle (U-H)^{2} \rangle =0$$
$$\langle H^{2} \rangle -\langle H \rangle ^{2}=-\frac{ \partial U }{ \partial \beta }=-\frac{ \partial U }{ \partial T } \frac{ \partial T }{ \partial \beta } =-C_{V} \frac{1}{k_{B}} \frac{-1}{\beta}=k_{B}C_{V}T^{2} $$
This connects the energy of a system with its constant-volume [[heat capacity]]. But the right hand side goes like $N$ for large particle numbers, as $k_{B}$ is constant and $T$ is [[Intensive property|intensive]], so only $C_{V}\sim N$ contributes. As such, the variance goes like $N$ asymptotically. If we compare it to the square [[mean]] of the energy $\langle H \rangle^{2}$, which goes like $N^{2}$, we can see that
$$\boxed{\frac{\langle H^{2} \rangle -\langle H \rangle ^{2}}{\langle H \rangle ^{2}}\sim \frac{N}{N^{2}}\sim \frac{1}{N}}$$
So in the [[thermodynamic limit]], for large $N$, the fluctuations tend to zero, which means that the energy of the system is essentially defined up to a tiny margin of error. But that's just the definition of the microcanonical ensemble, which confirms that for macroscopic systems, they are equivalent. In fact, for canonical ensembles with a realistic number of particles $(\sim 10^{23})$, we might as well write $\text{var}(H)=0$ and $\langle H \rangle=H$.

Another point that can be derived from variance equation is that the energy fluctuations are seemingly directly correlated with the heat capacity of a system. Though it might seem a bit odd at first, think of it like this: the heat capacity is the ability of a system to absorb and dissipate energy without large change in temperature. If an energy fluctuation occurs, a system with large heat capacity will scarcely respond it, whereas one with small heat capacity will feel it much more. As such, it's pretty natural to see that the system's fluctuations are dependent on how "good" it is at absorbing and dissipating energy. The bigger the heat capacity, the bigger the fluctuations are allowed to be without "breaking" the system. This is a specific case of a more universal result known as the [[fluctuation-dissipation theorem]].
##### Alternative argument
Another possible argument for equivalence starts from the partition function
$$Q_{N}(V,T)=\int e^{-\beta H(\mathbf{q},\mathbf{p})}dq\,dp=\int_{0}^{\infty} \omega(E)e^{-\beta E} \ dE=\int _{0}^{\infty}e^{-\beta E+\log \omega(E)} \ dE  =$$
$$=\int_{0}^{\infty} e^{\beta(TS(E)-E)}dE=\ldots$$
We can use [[Laplace's method]] here. Since $T\left( \frac{ \partial S }{ \partial E } \right)_{E}=1$.
$$\left( \frac{ \partial ^{2}S }{ \partial E^{2} }  \right)_{E=E}=\left( \frac{ \partial  }{ \partial E } \frac{1}{T} \right)_{E=E}=- \frac{1}{T^{2}}\left.\frac{ \partial T }{ \partial E }\right|_{E=E}=- \frac{1}{T^{2}C_{V}} $$
with $C_{V}>0$. But the fact that the specific heat must be positive (it would break conservation of energy if it weren't), implies that there is a maximum of entropy in $E$. Expanding in [[serie|series]]
$$TS(E)-E=[TS(E)-E]+ \frac{1}{2}(E-E)T\left( \frac{ \partial ^{2}S }{ \partial E^{2} }  \right)_{E=E}+\ldots=$$
$$=TS(U)-U- \frac{1}{2TC_{V}}(E-U)^{2}$$
So back to the integral we get
$$\ldots=e^{\beta[TS(U)-U]}\int_{0}^{E}e^{-(E-U)^{2}/2k_{B}T^{2}C_{V}}=\ldots$$
The distribution energy for the states is a [[Gaussian distribution]] centered on $E=U$, with uncertainty dependent on the number of particles, $\Delta E\propto \sqrt{ N }$. The relative error goes to zero at high particle counts:
$$\frac{\Delta E}{U}\sim \frac{1}{N}\to 0 \text{ for } N\to 0$$
So for large particle counts, the energy distribution tends to become a [[Delta di Dirac|Dirac-delta]]-esque spike centered on $E$, which means that all of the energy becomes associated with just one possible state, specifically the most likely one. So the integral can be readily approximated as
$$\ldots=\int_{-U}^{\infty}e^{-x^{2}/2k_{B}T^{2}C_{V}}dx \simeq \int_{-\infty}^{\infty} e^{-x^{2}/2k_{B}T^{2}C_{V}} dx =\sqrt{ 2\pi k_{B}T^{2}C_{V} }$$

A third argument for equivalence is purely qualitative. Consider a body in thermal equilibrium. Necessarily, the temperature of any piece of it has to be equal to the average temperature, as if it weren't, it wouldn't be in equilibrium. More generally, a body at equilibrium with the Universe must have the same temperature of the Universe. (TODO: Finish this discussion)

[^1]: Remember that the fluctuations we consider for a canonical ensemble are between the system itself and an *external* reservoir. If we consider them as one singular block, the fluctuations become internal and can be ignored, which leaves us with a microcanonical.
[^2]: If the objects the system is made up of are distinguishable, the $N!$ must be omitted.