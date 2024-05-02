---
tags:
  - calcolo-differenziale
aliases:
  - differenziabile
  - differenziale
---
Sia data una funzione $f: A ⊆ \mathbb{R}^N → \mathbb{R}^M$ con $A$ aperto e un punto $x_0 ∈ A$. Diremo che $f$ è **differenziabile** in $x_0$ se esiste un’applicazione lineare $L: \mathbb{R}^N → \mathbb{R}^M$ tale che
$$\lim\limits_{h \to 0} \frac{f(x^{0}+h) - f(x^{0})-L[h]}{\|h\|} = 0\in\mathbb{R}^M$$
L’applicazione $L$ si dice **differenziale** di $f$ in $x^0$.