---
aliases:
  - ket
  - bra
  - braket
---
La **notazione braket** è una notazione utilizzata per rappresentare vettori e [[operatore|operatori]] in algebra lineare, specificamente per la meccanica quantistica, in spazi vettoriali complessi.

Prendo un vettore $v$ in $\mathbb{C}^{N}$ o in uno spazio a dimensione infinita come uno [[spazio di Hilbert]]. Allora chiamo **bra** il vettore *riga* dei coniugati $\langle v|$ e **ket** il vettore *colonna* $|v\rangle$
$$v_{\text{riga}}\equiv\langle v|=(v_{1}^{*},v_{2}^{*},\ldots,v_{N}^{*})\quad;\quad v_{\text{colonna}}\equiv|v\rangle=\pmatrix{v_{1} \\ v_{2} \\ \vdots \\ v_{N}}$$
Si usa la seguente notazione per rappresentare il [[prodotto scalare]] hermitiano
$$(v_{1},v_{2})\equiv\langle v_{1}|v_{2}\rangle=(v_{11}^\ast,v_{12}^\ast,\ldots,v_{1N}^\ast)\left(\matrix{v_{11}\\v_{21}\\\vdots\\v_{N1}}\right)=\sum\limits_{i=1}^{N}v_{1i}^{\ast}v_{i1}$$
Un operatore $\hat{A}$ applicato ad un bra o ket può essere scritto dentro o fuori
$$\hat{A}|\psi\rangle=|\hat{A}\psi\rangle$$
e identifica un prodotto matriciale
$$\mathbf{\hat{A}\psi}\equiv \hat{A}|\psi\rangle = \pmatrix{A_{11} & A_{12} & \ldots & A_{1N} \\ A_{21} & \ddots &  & \vdots \\ \vdots & & \ddots & \vdots \\ A_{N1} & \ldots & \ldots & A_{NN}} \pmatrix{\psi_{1} \\ \psi_{2} \\ \vdots \\ \psi_{N}}$$

La rappresentazione come vettore riga/colonna e come prodotto matriciale sussiste in spazi a dimensione finita, ma è facilmente estensibile, perlomeno intuitivamente, a spazi di dimensione infinita. Lo stesso vale nel caso, onnipresente in meccanica quantistica, dove i vettori in realtà sono funzioni $|f\rangle$ e per i quali la notazione vettoriale (rappresentante le componenti in [[serie di Fourier]]) sarebbe scomoda.