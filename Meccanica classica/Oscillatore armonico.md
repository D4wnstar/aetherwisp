---
aliases:
  - legge di Hooke
---
Un **oscillatore armonico** è un sistema dotato di un [[punto di equilibrio]] che, dopo aver subito una perturbazione, sperimenta una forza di ritorno $F$ proporzionale alla distanza di spostamento $x$ secondo la **legge di Hooke**:
$$\vec{F}=-k\vec{x}$$
con $k$ una costante positiva detta **costante elastica**.
## Moto armonico semplice
Se la forza $F$ è l'unica che agisce sul sistema, esso prende il nome di **oscillatore armonico semplice** e l'oggetto in movimento descrive un **moto armonico semplice**. In questo caso, possiamo usare la [[Leggi del moto|seconda legge del moto]] per analizzare il sistema:
$$F=ma=m\ddot{x}=-kx$$
che ci dà un'equazione differenziale lineare di secondo ordine
$$\ddot{x}=- \frac{k}{m}x=-\omega^{2}x$$
dove $\omega=\sqrt{k/m}$ è la frequenza angolare. La soluzione generale è della forma
$$x(t)=A\cos(\omega t)+B\sin(\omega t)$$
con le costanti determinate dalle condizioni al contorno, come di norma. Questo moto è periodico e il periodo è $T=2\pi/\omega$.

La velocità e l'accelerazione oscillano con la stessa frequenza, ma hanno fase diversa dalla posizione. In particolare, la velocità è minima quando lo spostamento è massimo e viceversa.

L'oscillatore ha energia [[Potenziale]] in posizione $x$ pari a
$$V=\frac{1}{2}kx^{2}\tag{1}$$
e la forza è conservativa.
## Approssimazioni
L'oscillatore armonico è estremamente importante perché *qualunque* potenziale $V(x)$ associato ad un moto oscillatorio può essere approssimato come una parabola della forma $(1)$ fintantoché l'oscillazione è piccola. Per dimostrarlo, espandiamo $V(x)$ in [[Polinomio di Taylor|serie di Taylor]] centrata in un minimo locale $x_{0}$:
$$V(x)=V(x_{0})+V'(x_{0})(x-x_{0})+ \frac{1}{2}V''(x_{0})(x-x_{0})^{2}+O(x^{3})$$
Dato che la costante $V(x_{0})$ si annulla derivando per ottenere la forza, possiamo sottrarla senza perdita di generalità. Inoltre, dato che $x_{0}$ è un [[Punto critico]], $V'(x_{0})=0$. Dunque ci rimane la forma esatta
$$V(x)=\frac{1}{2}V''(x_{0})(x-x_{0})^{2}+O(x^{3})$$
che possiamo approssimare troncando tutti i termini di terzo ordine e superiore, che sono piccoli se anche le oscillazioni lo sono:
$$V(x)\simeq \frac{1}{2}V''(x_{0})(x-x_{0})^{2}$$
che ha la stessa forma di $(1)$. $V''(x_{0})>0$ perché $x_{0}$ è un minimo per costruzione. Ciò significa che, per piccole oscillazioni, ogni moto oscillatorio può essere trattato come se fosse un oscillatore armonico.