The **chemical potential** $\mu$ is an [[energy]] difference that determines the amount of energy that needs to be spent to add a [[Particella|particle]] to a [[Physical system|system]]. Despite being called a [[Potential|potential]], it cannot be defined up to a constant as it is already a difference of two energies.

It is important in the description of the [[grand canonical ensemble]], where the number of particles is variable, but also generally describes the energy of adding a particle to a system like the [[Elettrone|electron]] shell of an [[Atomo|atom]].

It can be expressed in terms of the [[internal energy]], [[entropy]], [[Helmholtz free energy]] and [[Gibbs free energy]] as
$$\mu=\left( \frac{ \partial E }{ \partial N }  \right)_{S,V}=-T\left( \frac{ \partial S }{ \partial N }  \right)_{E,V}=\left( \frac{ \partial A }{ \partial N }  \right)_{V,T}=\left( \frac{ \partial G }{ \partial N }  \right)_{P,T}$$
If $\mu>0$, then if $N$ increases (i.e. particles are added), so do $A$ and $G$.
### Connection to the first law of thermodynamics
In a system of $N$ particles that exchanges particles and is subject to a chemical potential $\mu$, the [[Laws of thermodynamics|first law of thermodynamics]] is extended to
$$dU=TdS-PdV+\mu dN$$
since energy now also depends on the number of particles. This is true for all energy functions, not just the internal energy. The Helmholtz free energy variation is
$$dA=-PdV-SdT+\mu dN$$
and the Gibbs free energy one is
$$dG=dA+d(PV)=-PdV+\mu dV+PdV-VdP-SdT=VdP-SdT+\mu dN$$
The chemical potential is the [[Moltiplicatori di Lagrange|Lagrange multiplier]] that governs the number of particles.