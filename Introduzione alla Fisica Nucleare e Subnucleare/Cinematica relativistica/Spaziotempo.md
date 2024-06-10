---
aliases:
  - spazio di Minkowski
---
Lo **spaziotempo** è un modello matematico per descrivere simultaneamente le tre dimensioni spaziali e l'una temporale dell'Universo, rendendolo quindi uno spazio in quattro dimensioni.

In assenza di [[Interazione gravitazionale|gravitazione]], lo spaziotempo è descritto da uno **spazio di Minkowski**, che è uno [[spazio metrico]] che ammette un [[prodotto scalare]], detto [[tensore metrico]], usato per descrivere il concetto di distanza nello spaziotempo. In presenza di gravitazione, bisogna fare uso della relatività generale.
### Causalità
La distanza tra due eventi nello spaziotempo può essere descritta mediante il segno della metrica. Allora presi due eventi $E_{1}=(t_{1},\vec{x}_{1})$ e $E_{2}=(t_{2},\vec{x}_{2})$, la loro distanza è
$$S_{12}^{2}=(c\Delta t)^{2}-(\Delta\vec{x})^{2}$$
e si hanno tre casi:
1. $S_{12}^{2}<0$: si ha $t_{1}=t_{2}$, ossia gli eventi avvengono allo stesso tempo e sono spazialmente separati: $S_{12}=\sqrt{-\Delta x^{2}}$. Gli eventi non sono legati causalmente. Si dicono **space-like events**.
2. $S^{2}_{12}>0$: gli eventi non avvengono in contemporanea e sono legati causalmente. Si dicono **time-like events**.
3. $S^{2}_{12}=0$: gli eventi sono connessi solo da un raggio di luce. Si dicono **light-like events**.

È possibile rappresentare questo concetto graficamente mediante un **cono di luce**, ossia il cono prodotto nello spazio tempo un'oggetto che si muove alla velocità della luce e che non è superabile in alcun modo.

![[Schema Cono di luce|80%|center]]
### Sistemi di riferimento
In un esperimento, si usano due sistemi di riferimento fondamentali:
1. Il sistema di riferimento del laboratorio è solidale all'osservatore (e ai [[Rivelatore|rivelatori]]). È quello che si usa quando si fa collidere una [[Particella]] con un bersaglio fisso.
2. Il sistema di riferimento del [[centro di massa]] è il sistema tale per cui la somma degli impulsi delle particelle che collidono è nulla: $\sum\vec{p}=0$.

Considerando i [[Quadrivettore energia-impulso|quadri-impulsi]] per due particelle (o un bersaglio), si ha per il laboratorio
$$\begin{cases}
p_{1} = (E_{1},\vec{p}_{1})  \\
p_{2} = (M_{2},0)
\end{cases} \quad \Rightarrow \quad p_{tot,lab}=(E_{1}+M_{2},\vec{p}_{1})$$
e per il centro di massa
$$\begin{cases}
p_{1}=(E_{1},\vec{p})  \\
p_{2}=(E_{2},-\vec{p})
\end{cases} \quad \Rightarrow \quad p_{tot,CM}=(E_{1}+E_{2},0)$$
Nel caso di $n$ particelle, si ha $p_{tot,CM}=(\sum E_{i},0)$. In particolare, si ha $p_{tot,CM}=(\sqrt{s},0)$, dove $\sqrt{s}$ è l'[[energia del centro di massa]].

Applicando le [[trasformazioni di Lorentz]] al sistema del laboratorio, possiamo trovare come sono legate energia e impulso. Ad esempio, trasformando lungo $x$ da lab a CM:
$$\begin{pmatrix}\sqrt{s} \\ 0 \\ 0 \\ 0 \end{pmatrix}=g_{\mu\nu}\begin{pmatrix}\sum\limits_{k}E_{k} \\ \sum\limits_{k}p_{k} \\ 0 \\ 0\end{pmatrix} \quad \Rightarrow \quad \beta=\frac{\sum\limits_{k}p_{k}}{\sum\limits_{k}E_{k}}= \frac{p_{tot,lab}}{E_{tot,lab}};\quad \gamma=\frac{E_{tot,lab}}{\sqrt{s}}$$
Se invece applichiamo una trasformazione su $z$ da lab a CM:
$$\begin{pmatrix}E \\ p_{x} \\ p_{y} \\ p_{z}\end{pmatrix}_{LAB}=\begin{pmatrix}E \\ p\sin\theta\cos\varphi \\ p\sin\theta\sin\varphi \\ p\cos\theta\end{pmatrix}_{LAB}=\begin{pmatrix}\gamma & 0 & 0 & \beta\gamma \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ \beta \gamma & 0 & 0 & \gamma\end{pmatrix}\begin{pmatrix}E^{*} \\ p^{*}\sin\theta^{*}\cos\varphi^{*} \\ p^{*}\sin\theta^{*}\sin\varphi^{*} \\ p^{*}\cos\varphi^{*}\end{pmatrix}$$
da cui
$$\begin{pmatrix}E \\ p\sin\theta\cos\varphi \\ p\sin\theta\sin\varphi \\ p\cos\theta\end{pmatrix}_{LAB}=\begin{pmatrix}E^{*}\gamma+\beta\gamma\cos\theta^{*} \\ p^{*}\sin\theta^{*}\cos\varphi^{*} \\ p^{*}\sin\theta^{*}\sin\varphi^{*} \\ \beta\gamma E^{*}+\gamma p^{*}\cos\theta^{*}\end{pmatrix}_{CM}$$
da cui si vede $p_{T}=p\sin\theta=p^{*}\sin\varphi^{*}$, ossia si conserva l'*impulso trasverso*, che è quindi un'[[invariante relativistica]] per una trasformazione lungo $z$, così come $\varphi=\varphi^{*}$ l'*angolo azimutale*.