---
wiki-publish: true
---
The **canonical ensemble** is an [[ensemble]] that is not [[Physical system|isolated]] from the environment, but is in [[thermal equilibrium]] with a larger [[Physical system|system]] that acts as a [[heat reservoir]] (i.e., the environment). The [[energy]] is subject to fluctuation, but the number of [[Particle|particles]] is constant. Its density function is
$$\rho(\mathbf{q},\mathbf{p})=e^{-\beta H(\mathbf{q},\mathbf{p})}$$
where $\beta=1/k_{B}T$, $H$ is the [[Hamiltonian]], $k_{B}$ is the [[Boltzmann constant]] and $T$ is the [[temperature]]. The [[Normalization|normalization]] factor is the [[partition function]][^1]
$$Q_{N}(V,T)=\int \frac{e^{-\beta H(\mathbf{q},\mathbf{p})}}{h^{3N}N!} \ d^{3N}q\,d^{3N}p$$
Here, $h$ is a constant to make the function dimensionless. It is usually assumed to be the [[Planck constant|Planck constant]] when working with quantum objects like [[Atom|atoms]] and [[molecule|molecules]], but it should be emphasized that there is no a priori reason why it should be precisely that. Its value depends on the what is being considered as components of the system.

It differs from the [[microcanonical ensemble]], which has constant energy with no fluctuations, and the [[grand canonical ensemble]], which has fluctuations in both energy and particle number. For most solid and liquid systems, the canonical ensemble is the most convenient description, as it takes the interaction with the environment into account. Compared to the microcanonical, energy is derived from the equilibrium temperature instead of the other way around. In fact, in the canonical ensemble, temperature serves much of the same role as energy does in the microcanonical, being the quantity that's conserved.
### Derivation from the microcanonical ensemble
Let's consider the system (1) and the reservoir (2) separately, each with a large and constant number of particles $N_{1}\gg 1$ and $N_{2}\gg 1$. Combined, they make up an [[Physical system|isolated system]] which can be described by a [[microcanonical ensemble]][^2] of energy $E_{1} + E_{2}$ that obeys
$$E_\text{total}<E_{1}+E_{2}<E_\text{total}+2\Delta$$
where $E_\text{total}$ is the energy of the system + reservoir and $\Delta$ is a small amount of energy (to account for uncertainty). For clarity: $E_\text{total}$ is constant, but $E_{1}$ and $E_{2}$ are *not*. We ignore the interaction between the two system beyond the transfer of energy, so that the total Hamiltonian is separable:
$$H=H_{1}+H_{2}$$
The reservoir's energy and number of particle is taken to be much larger than that of the system, so $E_{2}\gg E_{1}$ and $N_{2}\gg N_{1}$.

Now, we really only care about the state of system 1, regardless of what reservoir 2 is doing. The [[probability]] of system 1 being in a volume element $d\mathbf{q}_{1}d\mathbf{p}_{1}$ centered on $(\mathbf{q}_{1},\mathbf{p}_{1})$ in its own [[phase space]] is proportional to
$$\propto\Gamma_{2}(E_{2})d\mathbf{q}_{1}d\mathbf{p}_{1}=\Gamma_{2}(E_\text{total}-E_{1})d\mathbf{q}_{1}d\mathbf{p}_{1}$$
since $E_{2}$ is the only state the reservoir is likely to be in at equilibrium. The density function of system 1 is going to be determined by its most likely state
$$\rho_{1}(\mathbf{q}_{1},\mathbf{p}_{1})=\Gamma_{2}(E_\text{total}-E_{1})$$
We want to find the number of [[Stato|microstates]] at energy $E_{1}$, and to do so we can start from the [[Entropy (information theory)|Boltzmann entropy]] formula $S(E_\text{total}-E_{1})=k_{B}\log \Gamma(E_\text{total}-E_{1})$. Remember that $E_{2}\gg E_{1}$, so we can approximate $S(E_\text{total}-E_{1})$ using a [[Taylor series|Taylor series]] in $E_\text{total}-E_{1}=E_{2}$ centered in $E_\text{total}$ and truncate at the first order without much error:
$$\begin{align}
k_{B}\log \Gamma_{2}(E_\text{total}-E_{1})&=S_{1}(E_\text{total}-E_{1}) \\
&=S_{1}(E_\text{total})-E_{1}\left.\frac{ \partial S_{1} }{ \partial E_{2} } \right|_{E_{2}=E_\text{total}} +\ldots\\
&\simeq S_{1}(E_{\text{total}})- E_{1} \frac{1}{T}
\end{align}$$
where we used the [[Maxwell relations|Maxwell relation]] $\frac{ \partial S_{2} }{ \partial E_{2} }=\frac{1}{T_{2}}$, the fact that $T_{1}=T_{2}=T$ always because that's how reservoirs work. If we pull $\Gamma_{2}$ out we get
$$\Gamma_{2}(E_\text{total}-E_{1})=e^{S_{2}(E_\text{total})/k_{B}}e^{-E_{1}/k_{B}T}=\rho_{1}(\mathbf{q}_{1},\mathbf{p_{1}})$$
The first exponential is a constant, so we can drop it by redefining the normalization constant. By writing $E_{1}=H_{1}(\mathbf{q}_{1},\mathbf{p}_{1})$, using the inverse temperature $\beta=1/k_{B}T$ and dropping the index 1, we can write the density function:
$$\boxed{\rho(\mathbf{q},\mathbf{p})=e^{-\beta H(\mathbf{q},\mathbf{p})}}$$
Note that it is not yet normalized. The normalization factor is the partition function below.

This is the density function of the canonical ensemble and is an incredibly important result in and out of physics because it essentially encodes a universal method to find a [[stato|state]] of equilibrium from an extremely complex system. In statistical physics, of course, it represents a huge number of particles needing to thermalize. But it may also represent cities in the [[traveling salesman problem]] or many other systems completely detached from physics. The function $H$ here is the [[Hamiltonian]], but it is more generally a [[cost function]] the minimum of which is the most stable equilibrium state.
### Partition function
The [[partition function]] of the canonical ensemble is
$$\boxed{Q_{N}(V,T)=\int \frac{e^{-\beta H(\mathbf{q},\mathbf{p})}}{h^{3N}N!} \ d^{3N}q\,d^{3N}p }$$
The $N!$ comes from correct Boltzmann counting[^1], meanwhile $h^{3N}$ keeps the function dimensionless by canceling the dimensions of $d^{3N}q\,d^{3N}p$. Integration happens over the entire phase space. The following important result also holds:
$$\boxed{Q_{N}(V,T)=e^{-\beta A(V,T)}}$$
where $A=U-TS$ is the [[Helmholtz free energy]] (needs to be proven; see below). Since $A$ is an [[equation of state]], it encodes all information about the system. If one can calculate the partition function, the free energy can be extracted from it, and from the free energy we get everything about the system.

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
$$\boxed{U=-\frac{ \partial  }{ \partial \beta } \ln Q_{N}}$$
#### Energy fluctuations
The difference between the canonical ensemble and the [[microcanonical ensemble]] is that in the former, energy is allowed to fluctuate, whereas in the latter it is fixed and has no communication with the outside environment.

Let's find how the energy fluctuates by computing its [[variance]] (up to a constant). Start by differentiating the internal energy:
$$\frac{ \partial U }{ \partial \beta }=\frac{ \partial  }{ \partial \beta }  \frac{\int He^{-\beta H}d\mathbf{q}\,d\mathbf{p}}{\int e^{-\beta H}d\mathbf{q}\,d\mathbf{p}}=- \frac{\int H^{2}e^{-\beta H}d\mathbf{q}\,d\mathbf{p}}{\int e^{-\beta H}d\mathbf{q}\,d\mathbf{p}}+\left( \frac{\int He^{-\beta H}d\mathbf{q}\,d\mathbf{p}}{\int e^{-\beta H}d\mathbf{q}\,d\mathbf{p}} \right)^{2}=-\langle H^{2} \rangle +\langle H \rangle^{2} $$
So the variance is just another derivative, with an additional minus in front:
$$\boxed{\text{var}(H)=-\frac{ \partial U }{ \partial \beta } =\frac{ \partial  }{ \partial \beta ^{2} } \ln Q_{N}}$$
We can rewrite this to be
$$\text{var}(H)=-\frac{ \partial U }{ \partial \beta }=-\frac{ \partial U }{ \partial T } \frac{ \partial T }{ \partial \beta } =- \frac{1}{k_{B}} \frac{-1}{\beta ^{2}}\frac{ \partial U }{ \partial T } =k_{B}T^{2} \frac{ \partial U }{ \partial T } $$
Using the definition of [[heat capacity]] we can see that fluctuations are connected to it:
$$\boxed{\text{var}(H)=k_{B}T^{2}C_{V}}$$
The right hand side goes like $N$ for large particle numbers, as $k_{B}$ is constant and $T$ is [[Intensive property|intensive]], so only $C_{V}\sim N$ contributes. As such, the variance goes like $N$ asymptotically. If we compare it to the square [[mean]] of the energy $\langle H \rangle^{2}$, which goes like $N^{2}$, we can see that it gets nullified:
$$\boxed{\frac{\langle H^{2} \rangle -\langle H \rangle ^{2}}{\langle H \rangle ^{2}}\sim \frac{N}{N^{2}}\sim \frac{1}{N}\to 0}$$
So, in the [[thermodynamic limit]], energy fluctuations tend to vanish or, better, they increase but become insignificant with respect to the total energy. This makes the internal energy basically constant up to a tiny margin of uncertainty. But that's just what the definition of the microcanonical ensemble is, and so in the thermodynamic limit, the two are equivalent. For canonical ensembles with a realistic number of particles $(\sim 10^{23})$, we might as well write $\text{var}(H)=0$ and therefore $\langle H \rangle=H$.

Another thing that can we can see from variance equation is that the energy fluctuations are seemingly directly correlated with the heat capacity of a system. Though it might seem a bit odd at first, think of it like this: the heat capacity is the ability of a system to absorb and dissipate energy without large change in temperature. If an energy fluctuation occurs, a system with large heat capacity will scarcely respond it, whereas one with small heat capacity will feel it much more. As such, it's pretty natural to see that the system's fluctuations are dependent on how "good" it is at absorbing and dissipating energy. The bigger the heat capacity, the bigger the fluctuations are allowed to be without having a tangible effect. This is a specific case of a more universal result known as the [[fluctuation-dissipation theorem]].
##### Alternative argument for equivalence
Another possible argument for equivalence starts from the partition function, using the $\omega(E)$ function defined in the [[#Minimization of free energy]] section below.
$$Q_{N}(V,T)=\int e^{-\beta H(\mathbf{q},\mathbf{p})}dq\,dp=\int_{0}^{\infty} \omega(E)e^{-\beta E} \ dE=\int _{0}^{\infty}e^{-\beta E+\log \omega(E)} \ dE  =$$
$$=\int_{0}^{\infty} e^{\beta(TS(E)-E)}dE=\ldots$$
We can use [[Laplace's method]] here. Since $T\left( \frac{ \partial S }{ \partial E } \right)_{E}=1$.
$$\left( \frac{ \partial ^{2}S }{ \partial E^{2} }  \right)_{E=E}=\left( \frac{ \partial  }{ \partial E } \frac{1}{T} \right)_{E=E}=- \frac{1}{T^{2}}\left.\frac{ \partial T }{ \partial E }\right|_{E=E}=- \frac{1}{T^{2}C_{V}} $$
with $C_{V}>0$. But the fact that the specific heat must be positive (it would break conservation of energy if it weren't), implies that there is a maximum of entropy in $E$. Expanding in [[Serie|series]]
$$TS(E)-E=[TS(E)-E]+ \frac{1}{2}(E-E)T\left( \frac{ \partial ^{2}S }{ \partial E^{2} }  \right)_{E=E}+\ldots=$$
$$=TS(U)-U- \frac{1}{2TC_{V}}(E-U)^{2}$$
So back to the integral we get
$$\ldots=e^{\beta[TS(U)-U]}\int_{0}^{E}e^{-(E-U)^{2}/2k_{B}T^{2}C_{V}}=\ldots$$
The distribution energy for the states is a [[Gaussian distribution]] centered on $E=U$, with uncertainty dependent on the number of particles, $\Delta E\propto \sqrt{ N }$. The relative error goes to zero at high particle counts:
$$\frac{\Delta E}{U}\sim \frac{1}{N}\to 0 \text{ for } N\to 0$$
So for large particle counts, the energy distribution tends to become a [[Delta di Dirac|Dirac-delta]]-esque spike centered on $E$, which means that all of the energy becomes associated with just one possible state, specifically the most likely one. So the integral can be readily approximated as
$$\ldots=\int_{-U}^{\infty}e^{-x^{2}/2k_{B}T^{2}C_{V}}dx \simeq \int_{-\infty}^{\infty} e^{-x^{2}/2k_{B}T^{2}C_{V}} dx =\sqrt{ 2\pi k_{B}T^{2}C_{V} }$$

A third argument for equivalence is purely qualitative. Consider a body in thermal equilibrium. Necessarily, the temperature of any piece of it has to be equal to the average temperature, as if it weren't, it wouldn't be in equilibrium. More generally, a body at equilibrium with the Universe must have the same temperature of the Universe. (TODO: Finish this discussion)
### Minimization of free energy
In thermodynamics, a system will spontaneously converge to the state of lowest free energy. This can be derived from the canonical partition function using the Helmholtz free energy. The partition function can be rewritten
$$Q_{N}(V,T)=\int_{0}^{\infty} e^{-\beta E}dE\int \frac{\delta(H(\mathbf{q},\mathbf{p})-E)}{h^{3N}N!}d^{3N}q\ d^{3N}p$$
We use a [[Delta di Dirac|Dirac delta]] to select only the states with energy $E$ and split the integral into two. Since the Dirac delta only permits integrals where $E=H(\mathbf{q},\mathbf{p})$, the left integral evaluates to $e^{-\beta H}$, which returns the original form. The integral with the delta is a density of states (DOS) function with respect to $E$:
$$\omega(E)=\int \frac{\delta(H(\mathbf{q},\mathbf{p})-E)}{h^{3N}N!}d^{3N}q\ d^{3N}p$$
Since it counts states, we can get its [[Entropy (information theory)|Boltzmann entropy]]:
$$S=k_{B}\ln \omega(E)$$
which we can invert to express the states as a function of entropy:
$$\omega(E)=e^{S(E)/k_{B}}=e^{\beta TS(E)}$$
With this, the partition function becomes
$$Q_{N}(V,T)=\int_{0}^{\infty} e^{-\beta E}\omega (E)dE=\int_{0}^{\infty}e^{-\beta[E-TS(E)]}\ dE=\int_{0}^{\infty}e^{-\beta A(E)}\ dE$$
by using the definition of Helmholtz free energy. Mathematically, the most impactful contribution to the integral is given by the highest exponent, which occurs when $\beta A(E)$ is lowest. Since $\beta$ is constant, we're left with a minimization problem for $A(E)$.

This kind of integral is well suited for approximation with [[Laplace's method]]. Under the assumption that this minimum exists, we call the energy value at which it occurs $\bar{E}$. Thus, $A(\bar{E})$ is a [[Punto critico|stationary point]]:
$$\frac{ \partial A }{ \partial E } (\bar{E})=0$$
Unpacking the definition $A=E-TS$, we get
$$\left( 1-T\frac{ \partial S }{ \partial E }  \right)(\bar{E})=0$$
which gives us the well-known entropy-temperature relation
$$\frac{ \partial S }{ \partial E } (\bar{E})=\frac{1}{T}$$
The neat part of this specific relation is that it shows that the equilibrium temperature $T$ is determined exclusively by the energy state $\bar{E}$ at which free energy is minimized. We can also examine the second derivative:
$$\frac{ \partial ^{2}A }{ \partial E^{2} } (\bar{E})=-T \frac{ \partial ^{2}S }{ \partial E^{2} }=-T\frac{ \partial  }{ \partial E } \frac{1}{T}= -T \left( -\frac{1}{T^{2}} \right)\frac{ \partial T }{ \partial E }  =\frac{1}{TC_{V}}$$
since the [[heat capacity]] is $C_{V}=\frac{ \partial E }{ \partial T }$. Since [[absolute temperature]] and heat capacity are both strictly positive, this is also a strictly positive quantity, which guarantees that $A(\bar{E})$ is a minimum. We can expand $A$ in a [[Taylor series|Taylor series]] about $\bar{E}$ up to the second order:
$$\begin{align}
A(E)&\simeq A(\bar{E})+\frac{ \partial A }{ \partial E } (\bar{E})(E-\bar{E})+ \frac{1}{2}\frac{ \partial ^{2}A }{ \partial E^{2} } (\bar{E})(E-\bar{E})^{2} \\
&=A(\bar{E})+ \frac{1}{2TC_{V}}(E-\bar{E})^{2}
\end{align}$$
We can substitute this in the partition function to get
$$Q_{N}(V,T)\simeq e^{-\beta A(\bar{E})}\int_{0}^{\infty}e^{-(\beta/2TC_{V})(E-\bar{E})^{2}}dE$$
Since the integrand is very sharply peaked around $\bar{E}$, we can extend the lower integration bound from $0$ to $-\infty$ without much error. We are now left with a [[Gaussian integral]], we can be solved as
$$Q_{N}\simeq \sqrt{ 2\pi k_{B}T^{2}C_{V} }e^{-\beta A(\bar{E})}$$
and the natural logarithm, for convenience, is
$$\ln Q_{N}=- \frac{A(\bar{E})}{k_{B}T}+ \frac{1}{2}\ln(2\pi k_{B}T^{2}C_{V})$$
In the [[thermodynamic limit]], the first term is of order $N$ (since $\bar{E}\sim N$ inside of $A$), whereas the second is of order $\ln N$ (since $C_{V}\sim N$). Thus, when $N$ is large, the second term becomes vanishingly small in comparison to the first and can be neglected without error. In this case, we finally find:
$$\ln Q_{N}=-\beta A(\bar{E})\quad\Rightarrow \quad Q_{N}=e^{-\beta A(\bar{E})}$$
The only term left is the minimum energy state.

> [!success] Result
> All of the relevant information about the system can be deduced just from the state of lowest free energy. Though it is technically an approximation, just like the [[Laws of thermodynamics|second law of thermodynamics]] it is so exceedingly unlikely for the system to stabilize in any other state that we might as well consider it to a be a perfect, non-approximate result.

[^1]: If the objects the system is made up of are [[Identical particles|distinguishable]], the $N!$ must be omitted.
[^2]: Remember that the fluctuations we consider for a canonical ensemble are between the system itself and an *external* reservoir. If we consider them as one singular block, the fluctuations become internal and can be ignored, which leaves us with a microcanonical.