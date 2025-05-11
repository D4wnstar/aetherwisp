---
wiki-publish: true
tags:
  - equazioni-differenziali-ordinarie
---
Sia $f: \Omega ⊆ \mathbb{R} × \mathbb{R}^n → \mathbb{R}^n$ , con $\Omega$ aperto. La funzione $f$ si dice **localmente Lipschitziana nella seconda variabile** se per ogni $(t_0, x_0) ∈ \Omega$ esiste un intorno $U ⊆ \Omega$ di questo punto e una costante $L > 0$ tale che
$$||f(t, x_1) − f(t, x_2)|| \leq L||x_1 − x_2||$$
per ogni coppia $(t, x_1), (t, x_2) ∈ U$. Il tempo $t$ viene mantenuto fisso a sinistra della disuguaglianza.

**Caratterizzazione.** Sia $f: \Omega ⊆ \mathbb{R} × \mathbb{R}^n → \mathbb{R}^n$ con $\Omega$ aperto. Supponiamo che esistano in $\Omega$ le derivate parziali $\frac{\partial f}{\partial x_k}$ rispetto alla seconda variabile $x = (x_1 , . . . , x_n )$ e che le derivate parziali siano continue per $k = 1, . . . , n$. Allora la funzione è localmente Lipschitziana nella seconda variabile.