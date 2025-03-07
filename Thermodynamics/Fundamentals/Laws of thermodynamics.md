---
aliases:
  - first law of thermodynamics
  - second law of thermodynamics
  - third law of thermodynamics
---
The **laws of thermodynamics** are a set of experimentally derived laws that describe the fundamental behavior of thermodynamics. They are very useful for predicting thermal behavior.
### First law
The first law states that the difference between [[heat]] $Q$ absorbed by a system and the [[work]] $W$ done by that system is a variation of the system's [[internal energy]] $U$.

> [!info] First law of thermodynamics
> The internal energy $U$ of a system varies according to
> $$\Delta U=\Delta Q-\Delta W$$

This is a form of conservation of energy and shows that heat is "just another type" of energy.

It can also be expressed in differential form as
$$dU=\delta Q-\delta W$$
$dU$ is an [[Exact differential]], which is useful as it proves that $\int dU$ is independent of the path taken and is uniquely determined by the boundaries[^1]. The boundaries in this case are system [[stato|states]], so $U$ is uniquely determined by the state(s) of the system. This makes $U$ an [[equation of state]], $U(P,V,T)$, where $P$ is [[pressure]], $V$ is volume and $T$ is [[temperature]].

The first law can be used by itself to determine three equations for the variation of heat called [[heat equations]].
### Second law
The second law was stated by Kelvin in this way:

> [!info] Second law of thermodynamics (Kelvin's statement)
> There exists no [[thermodynamic transformation]] whose *only* effect is to extract an amount of heat from a reservoir and convert it *entirely* into work.

Clausius stated it in a different way:

> [!info] Second law of thermodynamics (Clausius' statement)
> There exists no [[thermodynamic transformation]] whose *only* effect is to extract an amount of heat from a colder reservoir and transfer it all to a hotter reservoir.

These two statements are, for all purposes, identical. If one is true, then so is the other.

> [!example] Equality of statements
> Let's assume there are two reservoirs at temperatures $T_{1}$ and $T_{2}$, with $T_{2}>T_{1}$.
> - If Kelvin's statement is false, then we could extract heat from $T_{1}$ and transform it all into work. We could then reverse the process and convert that work back into heat, now placing into $T_{2}$. But now we have made a process whose only effect is to transfer heat from $T_{1}$ to $T_{2}$, which is prevented from Clausius' statement.
> - If Clausius' statement is false, then we could let some amount of heat $Q_{2}$ move from $T_{1}$ to $T_{2}$ spontaneously. We could then connect a [[Carnot engine]] between $T_{2}$ and $T_{1}$ to extract $Q_{2}$ from $T_{2}$ and return some heat $Q_{1}<Q_{2}$ to $T_{1}$. The net work output of the apparatus is $Q_{2}-Q_{1}>0$. Since this is the only output of the apparatus, Kelvin's statement is contradicted.

At a statistical level, heat is a transfer of energy residing in the random motion of [[Particella|particles]]. In contrast, work requires organized motion from the particles. The ability to convert heat entirely into work would imply a spontaneous tendency to move from chaos to order. Though technically not impossible, it is exceptionally unlikely, as the configuration that leads to order is typically only one, compared to the myriad of other configuration that lead to chaos. The second law of thermodynamics fundamentally describes this tendency at a high level. In fact, we can express this law in yet another form, invoking [[entropy]]:

> [!info] Second law of thermodynamics (Entropy formulation)
> There exists no thermodynamic transformation that can decrease the entropy of an [[Physical system|isolated system]]. For such a system, $\Delta S\geq 0$.
### Third law
The third law of thermodynamic was stated by Nernst in 1905 as follows:

> [!info] Third law of thermodynamics
> The [[entropy]] of a system at absolute zero temperature is a constant zero. In symbols:
> $$S(T=0)=0$$

This law implies that reaching absolute zero is impossible, as reaching zero entropy is itself not possible.

[^1]: Notably, $\delta Q$ and $\delta W$ are in general *not* exact, but their difference *is*.