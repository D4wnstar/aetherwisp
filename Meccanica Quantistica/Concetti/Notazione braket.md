---
aliases:
  - ket
  - bra
  - braket
---
Prendo un vettore $v$ in $\mathbb{C}^{N}$. Allora chiamo **bra** il vettore *riga* dei coniugati $\langle v|$ e **ket** il vettore *colonna* $|v\rangle$
$$\langle v|=(v_{1}^{*},v_{2}^{*},\ldots,v_{N}^{*})\quad;\quad |v\rangle=\pmatrix{v_{1} \\ v_{2} \\ \vdots \\ v_{N}}$$
Si usa la seguente notazione per rappresentare il [[prodotto scalare]] hermitiano
$$\langle v_{1}|v_{2}\rangle=(v_{11}^\ast,v_{12}^\ast,\ldots,v_{1N}^\ast)\left(\matrix{v_{11}\\v_{21}\\\vdots\\v_{N1}}\right)=\sum\limits_{i=1}^{N}v_{1i}^{\ast}v_{i1}$$
Un [[operatore]] $\hat{A}$ applicato ad un bra o ket può essere scritto dentro o fuori:
$$\hat{A}|\psi\rangle=|\hat{A}\psi\rangle$$
