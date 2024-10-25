The **canonical ensemble** is an [[ensemble]] that is not [[Physical system|isolated]] from the environment, but is in [[thermal equilibrium]] with a larger [[Physical system|system]]. The [[energy]] is subject to fluctuation, but the number of [[Particella|particles]] is constant.

Let's divide the considered system in two subsystems, each with a large number of particles $N_{1}\gg 1$ and $N_{2}\gg 1$. Singularly, each subsystem is described by a [[microcanonical ensemble]] of energies $E_{1}$ and $E_{2}$ that obey
$$E<E_{1}+E_{2}<E+2\Delta$$
where $E$ is the energy of the collective system and $\Delta$ is a small amount of energy (to account for uncertainty). There are two states $\bar{E}_{1}$ and $\bar{E}_{2}$ which account for almost all of the [[entropy]] of each subsystem. Let's assume $\bar{E}_{2}\gg \bar{E}_{1}$. We want to find the amount of [[Phase space|representative points]] in the [[Phase space|phase spaces]] of each subsystem for these energies.
$$k_{B}\log \Gamma_{2}(E-E_{1})=S_{2}(E-E_{2})=S_{2}(E)-E_{1}\left.\frac{ \partial S_{2}(E_{2}) }{ \partial E_{2} } \right|_{E}\simeq S_{2}(E_{2})- \frac{E_{1}(T)}{T} \frac{1}{T}=\frac{ \partial S }{ \partial E} $$

The [[probability]] of subsystem 1 being in a volume element $dq_{1}dq_{1}$ centered on $(q_{1},p_{1})$ is
$$dq_{1}dp_{1}\Gamma_{2}(\bar{E}_{2})$$


$$\log \Gamma_{2}(E-E_{1})=\frac{S_{2}(E)}{k_{B}}- \frac{E_{1}}{k_{B}T}$$
from which
$$\Gamma_{2}(E-E_{1})=e^{S_{2}(E)/k_{B}}e^{-E_{1}/k_{B}T}$$
Notably, the first exponential is entirely independent on subsystem 1. Since $E_{1}=H_{1}(\mathbf{q},\mathbf{p})$ we can get the density function
$$\rho(\mathbf{q}_{1},\mathbf{p}_{1})=e^{-H(\mathbf{q},\mathbf{p})/k_{B}T}$$
defined up to a [[Normalizzazione|normalization]] constant. Using the inverse temperature $\beta=1/k_{B}T$ and noticing that this holds for any subsystem, we can write the [[Fattore di Boltzmann|Boltzmann factor]]:
$$\boxed{\rho(\mathbf{q},\mathbf{p})=e^{-\beta H(\mathbf{q},\mathbf{p})}}$$
This is the density function of the canonical ensemble and is an incredibly important result in and out ot physics because it essentially encodes a universal method to find a [[stato|state]] of equilibrium from an extremely complex system. In statistical physics, of course, it represents a huge number of particles needing to thermalize. But it may also represent cities in the [[traveling salesman problem]] or many other systems completely detached from physics. The function $H$ here is the [[Hamiltonian]], but it is more generally a [[cost function]] the minimum of which is the most stable equilibrium state.

The [[partition function]] of the system is
$$\boxed{Q_{N}(V,T)=\int \frac{e^{-\beta H(\mathbf{q},\mathbf{p})}}{h^{3N}N!} \ d^{3N}q\,d^{3N}p }$$
and the following important result also holds:
$$\boxed{Q_{N}(V,T)=e^{-\beta A(V,T)}}$$
where $A=U-TS$ is the [[Helmholtz free energy]] (needs to be proven; see below). Since $A$ is an [[equation of state]], it encodes all information about the system. If one can calculate the partition function, $A$ can be derived from it and with it, everything about the system. This single equation above single-handedly turns the entirety of classical statistical physics in a hunt for the partition function, for it contains everything that can be known about the system.
### Energy
The [[internal energy]] of the system is the [[expected value]] of the Hamiltonian
$$U=\langle H \rangle $$
as $H$ is variable due to fluctuations.
### Canonical-microcanonical equivalence
The difference between the canonical ensemble and the [[microcanonical ensemble]] is that in the former, energy is allowed to fluctuate, whereas in the latter it is fixed and has no communication with the outside environment.

Let's consider the internal energy of the canonical:
$$U=\langle H \rangle = \frac{\int He^{-\beta H}dq\,dp}{\int e^{-\beta H}dq\,dp}$$
Of course this means
$$U-\frac{\int He^{-\beta H}dq\,dp}{\int e^{-\beta H}dq\,dp}=0$$
But the denominator is the partition function
$$U- \frac{1}{Q_{N}} \int He^{-\beta H}dq\,dp=0$$
And so
$$U-e^{\beta A}\int e^{- \beta H}H\,dq\,dp=0$$
$$U-\int e^{\beta(A-H)}H\,dq\,dp=0$$
$$\int e^{\beta(A-H)}dq\,dp=1=e^{\beta A}\int e^{-\beta H}\,dq\,dp=\frac{Q_{N}}{Q_{?}}$$
$$\frac{ \partial  }{ \partial \beta } \int[U-H(\mathbf{q},\mathbf{p})]e^{\beta[A-H(\mathbf{q},\mathbf{p})]}dq\,dp=0$$
$$\frac{ \partial U }{ \partial \beta }+\int(U-H)\frac{ \partial  }{ \partial \beta } e^{\beta(A-H)}\,dq\,dp=0 $$
$$\frac{ \partial U }{ \partial \beta }+\int(U-H)e^{\beta(A-H)}\left( A-H-\underbrace{ \beta \frac{ \partial A }{ \partial \beta } }_{ T \frac{ \partial A }{ \partial T }  }  \right)dq\,qp=0 $$
$$\beta \frac{ \partial A }{ \partial \beta } =\frac{1}{k_{B}T}\frac{ \partial A }{ \partial T } \frac{ \partial T }{ \partial \beta } =\frac{1}{k_{B}T}\frac{ \partial A }{ \partial T } \frac{1}{k_{B}T} \frac{-1}{\beta ^{2}} T=-T \frac{ \partial A }{ \partial T } $$
Now to find the [[variance]]:
$$\langle (U-H)^{2} \rangle =\int e^{-\beta H}(U-H)^{2} \frac{1}{Q_{N}}dq\,dp$$
$$\frac{ \partial U }{ \partial \beta } +\langle (U-H)^{2} \rangle =0$$
$$\langle H^{2} \rangle -\langle H \rangle ^{2}=-\frac{ \partial U }{ \partial \beta }=-\frac{ \partial U }{ \partial T } \frac{ \partial T }{ \partial \beta } =-C_{V} \frac{1}{k_{B}} \frac{-1}{\beta}=k_{B}C_{V}T^{2} $$
This connects the energy of a system with its constant-volume [[heat capacity]]. So now we can find the [[mean squared error]]:
$$\boxed{\frac{\langle H^{2} \rangle -\langle H \rangle ^{2}}{\langle H \rangle ^{2}}\sim \frac{N}{N^{2}}\sim \frac{1}{N}}$$
So for a large number of particles, the MSE of the energy tends to zero, which means that there is a state of defined energy $E$ that fully describes the system. But that's exactly what the microcanonical ensemble does, which means that they describe the same thing and are equivalent.

Another possible argument for equivalence starts from the partition function
$$Q_{N}(V,T)=\int e^{-\beta H(\mathbf{q},\mathbf{p})}dq\,dp=\int_{0}^{\infty} \omega(E)e^{-\beta E} \ dE=\int _{0}^{\infty}e^{-\beta E+\log \omega(E)} \ dE  =$$
$$=\int_{0}^{\infty} e^{\beta(TS(E)-E)}dE=\ldots$$
We can use the [[saddle point method]] here. Since $T\left( \frac{ \partial S }{ \partial E } \right)_{\bar{E}}=1$.
$$\left( \frac{ \partial ^{2}S }{ \partial E^{2} }  \right)_{E=\bar{E}}=\left( \frac{ \partial  }{ \partial E } \frac{1}{T} \right)_{E=\bar{E}}=- \frac{1}{T^{2}}\left.\frac{ \partial T }{ \partial E }\right|_{E=\bar{E}}=- \frac{1}{T^{2}C_{V}} $$
with $C_{V}>0$. But the fact that the specific heat must be positive (it would break conservation of energy if it weren't), implies that there is a maximum of entropy in $\bar{E}$. Expanding in [[serie|series]]
$$TS(E)-E=[TS(\bar{E})-\bar{E}]+ \frac{1}{2}(E-\bar{E})T\left( \frac{ \partial ^{2}S }{ \partial E^{2} }  \right)_{E=\bar{E}}+\ldots=$$
$$=TS(U)-U- \frac{1}{2TC_{V}}(E-U)^{2}$$
So back to the integral we get
$$\ldots=e^{\beta[TS(U)-U]}\int_{0}^{E}e^{-(E-U)^{2}/2k_{B}T^{2}C_{V}}=\ldots$$
The distribution energy for the states is a [[Gaussian distribution]] centered on $\bar{E}=U$, with uncertainty dependent on the number of particles, $\Delta E\propto \sqrt{ N }$. The relative error goes to zero at high particle counts:
$$\frac{\Delta E}{U}\sim \frac{1}{N}\to 0 \text{ for } N\to 0$$
So for large particle counts, the energy distribution tends to become a [[Delta di Dirac|Dirac-delta]]-esque spike centered on $\bar{E}$, which means that all of the energy becomes associated with just one possible state, specifically the most likely one. So the integral can be readily approximated as
$$\ldots=\int_{-U}^{\infty}e^{-x^{2}/2k_{B}T^{2}C_{V}}dx \simeq \int_{-\infty}^{\infty} e^{-x^{2}/2k_{B}T^{2}C_{V}} dx =\sqrt{ 2\pi k_{B}T^{2}C_{V} }$$

A third argument for equivalence is purely qualitative. Consider a body in thermal equilibrium. Necessarily, the temperature of any piece of it has to be equal to the average temperature, as if it weren't, it wouldn't be in equilibrium. More generally, a body at equilibrium with the Universe must have the same temperature of the Universe. (TODO: Finish this discussion)