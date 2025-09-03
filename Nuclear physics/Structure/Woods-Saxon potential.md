---
wiki-publish: true
---
The **Woods-Saxon potential** is a mean-field [[potential]] for the nucleons in an [[atomic nucleus]], motivated by the observation that nuclei are not perfect [[sphere|spheres]] with sharply defined surfaces. Rather, the charge density smoothly falls off as the surface is approached instead of cutting out abruptly. This potential is meant to be used in the [[nuclear shell model]] to replace the more basic [[Oscillatore armonico quantistico|quantum harmonic oscillator]].

Mathematically, it reads
$$V(r)=-\frac{V_{0}}{1+e^{(r-R)/a}},$$
where
- $r$ is the distance from the nuclear center;
- $V_{0}$ is the potential well depth, typically $\sim50\text{ MeV}$;
- $a$ is the nuclear surface thickness, typically $\sim0.5\text{ fm}$;
- $R$ is the [[mean]] nuclear radius, $\sim1.25A^{1/3}$, and $A$ is the atomic [[Atom|mass number]].

![[Plot Woods-Saxon potential|center]]

This form is derived from describing the charge distribution of the nucleus through a two-parameter [[Fermi-Dirac distribution]]
$$\rho(r)=\frac{\rho(0)}{1+e^{(r-c)/a}},$$
where $c$ is the radius at which $\rho(c)=\rho(0)/2$ and $a$ is the aforementioned nuclear surface thickness.