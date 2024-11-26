---
aliases:
  - absolute zero
---
The **absolute temperature** or **thermodynamic temperature** $\theta$ is the quantity such that the ratio of absolute temperatures $\theta_{1}$ and $\theta_{2}$ of two [[heat reservoir|heat reservoirs]] connected by a [[Carnot engine]] is
$$\frac{\theta_{1}}{\theta_{2}}\equiv 1- \frac{Q_{1}}{Q_{2}}=1-\eta$$
where $\eta$ is the [[thermal efficiency]] of the Carnot engine. It is measured in kelvins $\text{K}$.

Since the Carnot engine is independent of the substance it is working on, so is the absolute temperature. Since $Q_{1}>0$ (the [[Laws of thermodynamics|second law of thermodynamics]] forbids otherwise), the absolute temperature has a lower bound
$$\theta>0$$
The asymptotic bound $\theta=0$ is called the **absolute zero**.
### From entropy
The above definition is equivalent to the following
$$\boxed{\frac{1}{T}=\frac{\partial S}{\partial E}}$$
where $S$ is [[entropy]] and $E$ is the [[internal energy]] of the system. This is derived from [[Clausius' theorem]] and its definition of entropy in a constant-volume system (so no [[work]] $W$), where $dQ=dE$ and so
$$\frac{dQ}{T}=dS\quad\Rightarrow \quad T=\frac{dS}{dE}$$
Entropy could be dependent on other variables other than $E$, so we use the partial derivative instead.
### Ideal gas
The absolute temperature coincides with the [[Ideal gas]] temperature $T=PV/Nk_{B}$, as can be shown by using an ideal gas as the working substance for the Carnot engine. Thus, $\theta=T$.