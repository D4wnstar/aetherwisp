The **Maxwell relations** are a set of equations in thermodynamics regarding a system's energy when subject to a reversible [[thermodynamic transformation]]. These shouldn't be confused with [[Maxwell's equations]], which are the description of electromagnetism. They are useful to determine state variables like [[pressure]] and [[entropy]] from the system's energy. There are many forms for Maxwell relations, depending on which system energy is chosen.

Maxwell relations can be rendered graphically in a square diagram (I have no idea how it works):

![[Diagram Maxwell Relations|50%|center]]
### Derivations
The difference between exact differentials ($d$) and inexact differentials ($\delta$) here is somewhat important. This assumes reversible transformations and therefore exact differentials.

For all of these, we use $dW=PdV$ and $dS=dQ/T$.
#### Enthalpy
From $H$ we get
$$dH=dU+d(PV)=dQ-\cancel{ dW }+\cancel{ PdV }+VdP=TdS+VdP$$
We get
$$T=\left( \frac{ \partial H }{ \partial S }  \right)_{P}\qquad V=\left( \frac{ \partial H }{ \partial P }  \right)_{S}$$
#### Helmholtz free energy
From $A$ we get
$$dA=dU-d(TS)=\cancel{ dQ }-dW-\cancel{ TdS }-SdT$$
so
$$dA=-PdV-SdT$$
Since $A=A(V,T)$, we get
$$P=-\left( \frac{ \partial A }{ \partial V }  \right)_{T}\qquad S=-\left( \frac{ \partial A }{ \partial T }  \right)_{V}$$
#### Gibbs free energy
From $G$ we get
$$dG=dA+d(PV)=-SdT-\cancel{ PdV }+\cancel{ PdV }+VdP$$
and so
$$dG=VdP-SdT$$
We get
$$S=-\left( \frac{ \partial G }{ \partial T }  \right)_{P}\qquad V=\left( \frac{ \partial G }{ \partial P }  \right)_{T}$$
