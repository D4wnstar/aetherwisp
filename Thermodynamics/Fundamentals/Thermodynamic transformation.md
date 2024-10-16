---
aliases:
  - reversible transformation
  - irreversible transformation
  - isothermal transformation
  - isobaric transformation
  - adiabatic transformation
  - isotherm
---
A **thermodynamic transformation** or **process** is a change to a [[physical system]]'s [[thermodynamic state]], going from one state of [[thermal equilibrium]] to another. They can be represented as [[curva|paths]] taken in [[spazio delle fasi|phase space]]. They may be *reversible* or *irreversible*: a transformation is said to be reversible if the system will retrace the exact path, only in reverse, if the external forces causing the transformation are themselves reversed. An irreversible one will instead not retrace the exact path, thus causing a permanent change in the system.

If the system transforms very slowly, it is possible to consider it as if it were in equilibrium throughout the transformation itself. This type of transformation is said to be **quasi-static**. Quasi-static transformation are *usually* reversible.
### Types
Specific transformations have been given special names:
- For constant $T$ we have **isothermal transformations**. The path traced by one of these in phase space is called an **isotherm**.
- For constant $P$ we have **isobaric transformations**.
- For constant $V$ we have **constant-volume transformations**.
- With no heat exchanged $\Delta Q=0$ we have **adiabatic transformations**.
### Work done
For reversible transformations, we can consider infinitesimal paths. The mechanical [[work]] done by the system over such a path is given by
$$dW=PdV$$
We can extend this to a path from points $A$ to $B$ in phase space by concatenating many infinitesimal paths together. The work done over this path therefore is
$$\Delta W=\int_{A}^{B}PdV$$
In a non-cyclical transformation, this is the area under the curve in the $PV$ graph. In a cyclical transformation, this is the area inside of the closed shape.

![[Graph Work in thermodynamic transformation|90%|center]]

This does not hold for irreversible transformations, whose work is usually not $\int PdV$. For example, in the [[free expansion of an ideal gas]], the system does not perform any work to expand, so $\Delta W=0$ despite the volume and pressure both not changing.