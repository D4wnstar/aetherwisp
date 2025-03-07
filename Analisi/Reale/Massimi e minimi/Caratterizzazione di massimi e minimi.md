---
tags:
  - massimi-minimi
aliases:
  - punto di sella
---
Sia $f : C ⊆ \mathbb{R}^{N} → \mathbb{R}$ di classe $C^2$ in $C$, sia $x_0 ∈ \mathring{C}$ tale che $∇f (x^0 ) = 0$. Siano $λ_1, . . . , λ_N$ gli autovalori della matrice Hessiana $H_f (x^0 )$. Allora
1. se $x^0$ è punto di minimo locale allora $λ_k ≥ 0$ per ogni $k$;
2. se $x^0$ è punto di massimo locale allora $λ_k ≤ 0$ per ogni $k$;
3. se $λ_k > 0$ per ogni $k$ allora $x^0$ è punto di minimo locale stretto;
4. se $λ_k < 0$ per ogni $k$ allora $x^0$ è punto di massimo locale stretto;
5. se esiste $λ_i < 0$ e $λ_j > 0$ allora non è un punto di estremo per $f$, ma si tratta di un *punto di sella*.
### Dimostrazione
1. $x^0$ è min loc. Fisso $j=1,\cdots,N$ e considero la funzione $g_{j}(t)=x^0+tB^{T}e_{j}$ dove $B$ è una matrice tale che $H_f(x^0)=B^{T}DB$ e $e_{j}$  il $j$-esimo vettore della base canonica definita in un intorno di 0.
$B(g_{j}(t)-x^{0})=tBB^{T}e_{j}=te_{j}$
...