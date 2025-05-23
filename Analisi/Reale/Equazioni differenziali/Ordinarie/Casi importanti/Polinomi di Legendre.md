---
wiki-publish: true
aliases:
  - funzione di Legendre
  - funzione di Legendre associata
  - polinomi di Legendre associati
---
I **polinomi di Legendre** sono le soluzioni all'[[Equazione differenziale di Legendre]]. Sono anche chiamati **funzioni di Legendre del primo tipo**, dato che più correttamente i polinomi di Legendre sono un caso specifico. Le funzioni di Legendre sono definite in funzione di un indice continuo $n$ e sono funzioni complesse.

Possono essere definite usando l'[[Integrale su una curva]]
$$P_{n}(z)=\frac{1}{2\pi i}\oint_{\gamma}(1-2tz+t^{2})^{-1/2}t^{-n-1}dt$$
con $\gamma$ una [[Curve]] centrata attorno all'origine percorsa in senso antiorario e $n$ è un numero naturale.

Alternativamente, si può usare la **formula di Rodrigues**
$$P_{l}(z)=\frac{1}{2^{l}l!} \left(\frac{d}{dx}\right)^{l}(x^{2}-1)^{l}$$
dove $l$ è un numero naturale.

Esistono diverse altre rappresentazioni in serie dei polinomi di Legendre.

I primi polinomi di Legendre sono
$$\begin{align}
P_{0}(x)&=1 \\
P_{1}(x)&=x \\
P_{2}(x)&=\frac{1}{2}(3x^{2}-1) \\
P_{3}(x)&=\frac{1}{2}(5x^{3}-3x) \\
P_{4}(x)&=\frac{1}{8}(35x^{4}-30x^{2}+3) \\
P_{5}(x)&=\frac{1}{8}(63x^{5}-70x^{3}+15x) \\
P_{6}(x)&=\frac{1}{16}(231x^{6}-315x^{4}+105x^{2}-5)
\end{align}$$

:::image
![[Polinomi di Legendre.png]]
Da Introduction to Quantum Mechanics di Griffiths, p.139
:::
### Polinomi associati di Legendre
I **polinomi di Legendre associati**, anche chiamati **funzione di Legendre associata del primo tipo**, sono una generalizzazione dei polinomi di Legendre. Risultano come soluzione dell'equazione differenziale di Legendre associata. Presi un numero naturale $l$ e uno intero $m$, i polinomi associati sono
$$P_{l}^{m}(x)=(1-x^{2})^{|m|/2} \left(\frac{d}{dx}\right)^{|m|}P_{l}(x)$$
se $m>0$, dove $P_{l}(x)$ è l'$l$-esimo polinomio di Legendre. Talvolta alla formula si aggiunge il termine $(-1)^{m}$, detta **fase di Condon-Shortley**, che è una convenzione di segno diversa. Poiché, preso un polinomio di grado $l$, la sua $m$-esima derivata con $m>l$ è sempre zero, i polinomi associati con $m>l$ sono sempre zero. Dunque, per ogni $l=0,1,2,\ldots$, i valori permessi di $m$ sono $\{-l,-l-1,\ldots,0,\ldots,l-1,l\}$.

Le prime funzioni di Legendre associati sono (senza la fase)
$$\begin{align}
P_{0}^{0}&=1 \\
P_{1}^{0}&=x \\
P_{1}^{1}&=(1-x^{2})^{1/2} \\
P_{2}^{0}&=\frac{1}{2}(3x^{2}-1) \\
P_{2}^{1}&=3x(1-x^{2})^{1/2} \\
P_{2}^{2}&=3(1-x^{2}) \\
P_{3}^{0}&=\frac{1}{2}x(5x^{2}-3) \\
P_{3}^{1}&=\frac{3}{2}(1-5x^{2})(1-x^{2})^{1/2} \\
P_{3}^{2}&=15x(1-x^{2}) \\
P_{3}^{3}&=15(1-x^{2})^{3/2}
\end{align}$$

I termini con $m$ dispari presentano un termine $\sqrt{1-x^{2}}$, quindi non sono polinomi (la potenza è frazionaria). Per questa ragione, è comune esprimere la funzione di Legendre associata in funzione di $\cos\theta$ anziché di $x$. Così facendo, si ha $\sqrt{1-\cos^{2}\theta}=\sin\theta$. Allora tutte le funzioni associate in $\cos\theta$ sono polinomi, casomai moltiplicati per $\sin\theta$. Con questa convenzione, i primi polinomi diventano
$$\begin{align}
P_{0}^{0}(\cos\theta)&=1 \\
P_{1}^{0}(\cos\theta)&=\cos\theta \\
P_{1}^{1}(\cos\theta)&=\sin\theta \\
P_{2}^{0}(\cos\theta)&=\frac{1}{2}(3\cos^{2}\theta-1) \\
P_{2}^{1}(\cos\theta)&=3\sin\theta\cos\theta \\
P_{2}^{2}(\cos\theta)&=3\sin^{2}\theta \\
P_{3}^{0}(\cos\theta)&=\frac{1}{2}\cos\theta(5\cos^{2}\theta-3) \\
P_{3}^{1}(\cos\theta)&=\frac{3}{2}(5\cos^{2}\theta-1)\sin\theta \\
P_{3}^{2}(\cos\theta)&=15\cos\theta\sin^{2}\theta \\
P_{3}^{3}(\cos\theta)&=15\sin^{3}\theta
\end{align}$$

:::image
![[Polinomi di Legendre associati.png]]
Da Introduction to Quantum Mechanics di Griffiths, p. 140
:::