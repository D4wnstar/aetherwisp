---
aliases:
  - first law of thermodynamics
  - second law of thermodynamics
  - third law of thermodynamics
---
The **laws of thermodynamics** are a set of experimentally derived laws that describe the fundamental behavior of thermodynamics. They are very useful for predicting thermal behavior.
### First law
The first law states that the difference between [[heat]] $Q$ absorbed by a system and the [[work]] $W$ done by that system is a variation of the system's [[internal energy]] $U$:
$$\Delta U=\Delta Q-\Delta W$$
This is a form of conservation of energy and shows that heat is "just another type" of energy.

It can also be expressed in differential form as
$$dU=dQ-dW$$
$dU$ is an [[exact differential]], which is useful as it proves that $U$ is such that $\int dU$ is independent of the path taken and is uniquely determined by the boundaries[^1]. The boundaries in this case are system [[stato|states]], so $U$ is uniquely determined by the state(s) of the system. This makes $U$ an [[equation of state]], $U(P,V,T)$, where $P$ is [[pressure]], $V$ is volume and $T$ is [[temperature]].

The first law can be used by itself to determine three equations for the variation of heat called [[heat equations]].
### Second law
The second law was stated by Kelvin in this way:

> [!info] Second law of thermodynamics (Kelvin's statement)
> There exists no [[thermodynamic transformation]] whose *only* effect is to extract an amount of heat from a reservoir and convert it *entirely* in work.

Clausius stated it in a different way;

> [!info] Second law of thermodynamics (Clausius' statement)
> There exists no [[thermodynamic transformation]] whose *only* effect is to extract an amount of heat from a reservoir and transfer *all* of it to a hotter reservoir.

These two statements are, for all purposes, identical. If one is true, then so is the other.

> [!example] Equality of statements
> 1. Let's assume K's statement is false. Then the transformation converts heat entirely in work. This leaves temperature completely unchanged.
> 2. Let's assume C's is false and also a [[thermodynamic machine]] which carries out a cyclical transformation (i.e. the start state is identical to the end state). In order:
> 	1. The machine absorbs heat $Q_{2}$ from the second reservoir at temperature $T_{2}$.
> 	2. The machine moves heat $Q_{1}$ from the first reservoir at temperature $T_{1}<T_{2}$.
> 	3. The machine does work $W$ to enact this movement.
### Third law
The third law of thermodynamic was stated by Nernst in 1905 as follows:

> [!info] Third law of thermodynamics
> The [[entropy]] of a system at absolute zero temperature is a constant zero. In symbols:
> $$S(T=0)=0$$

This law implies that reaching absolute zero is impossible, as reaching zero entropy is itself not possible.

[^1]: Notably, $dQ$ and $dW$ are in general *not* exact, but their difference *is*.