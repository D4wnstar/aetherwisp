---
tags:
  - integrali
  - integrali-fisica
aliases:
  - teorema di Stokes
  - teorema di Green
---
Il **teorema della rotore** o **teorema di Stokes-Kelvin** è un risultato che permette di trasformare l'integrale del [[rotore]] di un [[campo vettoriale]] su una [[superficie]] in un integrale sulla [[curva]] che racchiude la superficie, passando quindi da due ad una dimensioni.

Sia dato un campo vettoriale $F : U ⊂ \mathbb{R}^{3} → \mathbb{R}^{3}$. Consideriamo una superficie regolare $\Sigma\subset U$ orientata con un campo di versori normali $ν̂$. Orientiamo positivamente il suo bordo $∂^+\Sigma$ e supponiamo che esso sia il sostegno di una curva regolare (a tratti) chiusa. Allora
$$\iint_{\Sigma}(\nabla\times F)\cdot\hat{\nu}\;dS=\oint_{\partial^+\Sigma}F\times\hat{\tau}\;ds$$

Nel caso bidimensionale prende il nome di **teorema di Gauss-Green**:
Dato un campo vettoriale $F = (F1 , F2) : U ⊆ \mathbb{R}^{2} → \mathbb{R}^{2}$ e un dominio
chiuso $D ⊂ U$ allora vale
$$\iint_{D}\left(\frac{\partial F_2}{\partial x}- \frac{\partial F_{1}}{\partial y}\right)\ dxdy=\oint_{\partial^+D}F\times\hat{\tau}\;ds$$
