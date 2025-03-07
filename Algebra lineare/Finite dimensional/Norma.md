---
aliases:
  - disuguaglianza triangolare
---
Si definisce **norma** una legge $V \rightarrow \mathbb{R}^{+}$ definita per ogni $v\in V$ su un [[Vector space]] $V$, indicata con $||\cdot||$, che soddisfa le seguenti proprietà per ogni vettore $v,w\in V$ e scalare $\lambda\in\mathbb{C}$:
1. $||v||\geq0$
2. $||v||=0 \Leftrightarrow v=0$
3. $||\lambda v||=|\lambda|\;||v||$
4. $||v+w||\leq||v||+||w||$ (detta **disuguaglianza triangolare**)

Si ha che un [[Scalar product]] definito su un campo $V$ *implica* una norma, definita come
$$||v||=\sqrt{(v,v)}$$
con $(\cdot,\cdot)$ il prodotto scalare. Tuttavia, non tutte le norme hanno un prodotto scalare associato. Ad esempio, la seguente valida norma
$$||v||=|v_{1}|+|v_{2}|+\ldots+|v_{n}|$$
non è indotta da alcun prodotto scalare.

Vale inoltre la regola del parallelogramma
$$||v+w||^{2}+||v-w||^{2}=2||v||^{2}+2||w||^{2}$$
per ogni $v,w\in V$.

Nel caso di spazi di funzioni a dimensione infinita, la definizione di norma vale se consideriamo *equivalenti* le funzioni *uguali quasi ovunque*. Ciò è necessario in quanto la proprietà 2 sarebbe falsa, dato che l'integrale di una funzione non nulla in numero finito o numerabile di punti è anch'esso uguale a zero, oltre al caso voluto $f\equiv0$.
### Norme canoniche
Sebbene sia possibile definire un numero infinito di norme, fintantoché soddisfano le condizioni sopra, di solito si usa una sola norma, chiamata **norma canonica**. Nel caso di spazi vettoriali a dimensione finita, si usa la **norma 2** o **norma euclidea**
$$||v||_{2}=\sqrt{v_{1}^{2}+v_{2}^{2}+\ldots+v_{n}^{2}}$$
Nel caso a dimensione infinita, bisogna stare attenti, in quanto è possibile che la norma non converga. Preso un intervallo $I$, si definiscono le norme $L^{1}$ e $L^{2}$
$$||f||_{1}=\int_{I}|f(x)|dx\quad;\quad ||f||_{2}=\int_{I}|f(x)|^{2}dx$$
È utile notare che se $I=]-\infty,+\infty[$ e l'integrale converge, allora $f$ appartiene per definizione allo spazio $L^{1}$ (primo caso) o $L^{2}$ (secondo caso).