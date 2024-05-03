---
aliases:
  - funzione di Legendre
  - polinomi associati di Legendre
  - funzione associata di Legendre
---
I **polinomi di Legendre** sono le soluzioni all'[[equazione differenziale di Legendre]]. Sono anche chiamati **funzioni di Legendre del primo tipo**, dato che più correttamente i polinomi di Legendre sono un caso specifico. Le funzioni di Legendre sono definite in funzione di un indice continuo $n$ e sono funzioni complesse.

Possono essere definite usando l'integrale su un percorso
$$P_{n}(z)=\frac{1}{2\pi i}\oint_{\gamma}(1-2tz+t^{2})^{-1/2}t^{-n-1}dt$$
con $\gamma$ una [[curva]] centrata attorno all'origine percorsa in senso antiorario e $n$ è un numero naturale.

Alternativamente, si può usare la **formula di Rodrigues**
$$P_{l}(z)=\frac{1}{2^{l}l!} \frac{d^{l}}{dx^{l}}(x^{2}-1)^{l}$$
dove $l$ è un numero naturale.

Esistono diverse altre rappresentazioni in serie dei polinomi di Legendre.
### Polinomi associati di Legendre
I **polinomi associati di Legendre**, anche chiamati **funzione associata di Legendre**, sono una generalizzazione dei polinomi di Legendre. Risultano come soluzione dell'equazione differenziale di Legendre associata. Presi un numero naturale $l$ e uno intero $m$, i polinomi associati sono
$$P_{l}^{m}(x)=(1-x^{2})^{m/2} \left(\frac{d}{dx}\right)^{m}P_{l}(x)$$
se $m>0$, dove $P_{l}(x)$ è l'$l$-esimo polinomio di Legendre.