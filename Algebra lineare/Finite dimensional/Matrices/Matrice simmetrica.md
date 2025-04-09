---
aliases:
  - matrice antisimmetrica
---
Si dice **matrice simmetrica** una [[matrice]] quadrata che è uguale alla propria trasposta, ovvero chiamando $M$ la matrice si ha
$$A=A^{T}$$
Si dice invece **antisimmetrica** se è invece uguale all'opposto della sua trasposta, cioè
$$A=-A^{T}$$
### Properties
Antisymmetric matrices (a.m.) are rather special. The sum of two a.ms is itself an a.m., and the product between a [[scalar]] and an a.m. is again an a.m. This means that the sum and scalar product operations between a.ms are closed: this is sufficient condition to state that the space of all a.ms is a [[vector space]]. More info on this can be found in [[Rotation#Exponentiation]].

Actually, it's something more than this. If we invoke the [[Commutatore]] and take two a.ms $\Omega_{1}$ and $\Omega_{2}$, we can calculate
$$([\Omega_{1},\Omega_{2}])^{T}=(\Omega_{1}\Omega_{2}-\Omega_{2}\Omega_{1})^{T}=\underbrace{ \Omega_{2}^{T} }_{ -\Omega_{2} }\underbrace{ \Omega_{1}^{T} }_{ -\Omega_{1} }-\Omega_{1}^{T}\Omega_{2}^{T}=\Omega_{2}\Omega_{1}-\Omega_{1}\Omega_{2}=-[\Omega_{1},\Omega_{2}]$$
From this we can claim that the commutator of two a.ms is itself an a.m. This, combined with the vector space nature we found above, is sufficient to state that the space of antisymmetric matrices is a [[Lie algebra]].