---
aliases:
  - ideal gas law
---
An **ideal gas** is an approximate model of the behavior of a gas that holds for low density gases. It is sparse and has weak internal interactions that limit [[information]] exchange. The dynamics are determined by the **ideal gas law**:
$$PV=Nk_{B}T=nRT$$
where $P$ is the [[pressure]], $V$ is the volume occupied by the gas, $N$ is the number of [[particella|particles]] composing the gas, $k_{B}$ is the [[Costante di Boltzmann|Boltzmann constant]], $T$ is the [[temperature]], $n$ is the number of [[mole|moles]] and $R$ is the [[Ideal gas constant|ideal gas constant]]. The latter form exists because, besides being of practical convenience, thermodynamics was historically developed at a time where the existence of the [[atomo|atom]] had yet to be proven and with it, the [[Particella|particle]] division of matter. In fact, classical thermodynamics as a whole does not strictly require the existence of particles like atoms.

![[Schema Ideal Gas state|center]]

The low self-interactivity of the ideal gas shows the limits of the model: when a gas is made to interact with another object of temperature $T$, by the [[laws of thermodynamics]] the two objects thermalize. But to thermalize, the gas must interact with itself (else the gas would never reach an equilibrium state), so it cannot be used to even define the concept of temperature.

"In generale, si porta l'oggetto di cui $T$ a contatto con il gas ideale e si misura $T$."
### Properties
The [[heat capacity]] by volume of an ideal gas is
$$C_{V}=\frac{3}{2}Nk_{B}$$
### Entropy
The [[entropy]] of an ideal gas can calculated as a function of volume $V$ and temperature $T$ by explicitly integrating $dS=dQ/T$. Let's consider a [[stato|state]] $A$, which we approach from two different states: one using an constant-volume transformation (path 1), the other using a isothermal one (path 2).

Along path 1, $V$ is constant, so
$$\int \frac{dQ}{T}=C_{V}\int \frac{dT}{T}$$
and thus if we start the transformation at temperature $T_{0}$ we get
$$S(V,T)=S(V,T_{0})+C_{V}\int_{T_{0}}^{T} \frac{dT}{T}=S(V,T_{0})+C_{V}\ln \frac{T}{T_{0}}$$
(TODO: Finish this proof)