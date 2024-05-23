La **teoria delle perturbazioni non degenere** è una forma della [[teoria delle perturbazioni]] indipendente dal tempo nella quale gli [[Equazione agli autovalori|autovalori]] dell'[[Hamiltoniana]] imperturbata non sono [[degenerazione|degeneri]].

Consideriamo un'Hamiltoniana del tipo
$$\hat{H}=\hat{H}^{0}+\lambda \hat{H}'$$
con $\hat{H}'$ la perturbazione e $\lambda$ una costante. $\hat{H}^{0}$ è l'Hamiltoniana non perturbata, che risolve il sistema descritto dall'[[Equazione di Schrödinger#Potenziale indipendente dal tempo|equazione di Schrödinger indipendente dal tempo]]
$$\hat{H}^{0}\psi_{n}^{0}=E_{n}^{0}\psi_{n}^{0}$$
La dinamica del sistema perturbato invece è descritto da
$$\hat{H}\psi_{n}=E_{n}\psi_{n}\tag{1}$$
### Formulazione
Scriviamo $\psi_{n}$ e $E_{n}$ come [[serie di potenze]] in $\lambda$:
$$\psi_{n}=\psi_{n}^{0}+\lambda\psi_{n}^{1}+\lambda^{2}\psi_{n}^{2}+\ldots=\sum\limits_{i=0}^{\infty}\lambda^{i}\psi_{n}^{i}$$
$$E_{n}=E_{n}^{0}+\lambda E_{n}^{1}+\lambda^{2}E_{n}^{2}+\ldots=\sum\limits_{i=0}^{\infty}\lambda^{i}E_{n}^{i}$$
$\psi_{n}^{0}$ e $E_{n}^{0}$ sono i termini non perturbati, mentre quelli successivi sono le correzioni di $i$-esimo ordine. Sostituendo queste due nella $(1)$ e omettendo i cappucci si ha
$$(H^{0}+\lambda H')\left(\sum\limits_{i=0}^{\infty}\lambda^{i}\psi_{n}^{i}\right)=\left(\sum\limits_{i=0}^{\infty}\lambda^{i}E_{n}^{i}\right)\left(\sum\limits_{i=0}^{\infty}\lambda^{i}\psi_{n}^{i}\right)$$
E usando il prodotto di Cauchy
$$\sum\limits_{i=0}^{\infty}\lambda^{i}H^{0}\psi_{n}^{i}+\sum\limits_{i=0}^{\infty}\lambda^{i+1}H'\psi_{n}^{i}=\sum\limits_{i=0}^{\infty}\sum\limits_{j=0}^{i}\lambda^{j}\lambda^{i-j}E_{n}^{j}\psi_{n}^{i-j}=\sum\limits_{i=0}^{\infty}\lambda^{i}\sum\limits_{j=0}^{i}E_{n}^{j}\psi_{n}^{i-j}$$
Definiamo $k=i+1$ e Nella sommatoria con $H'$ e estraiamo i primi termini nelle altre due sommatorie
$$H^{0}\psi_{n}^{0}+\sum\limits_{k=1}^{\infty}\lambda^{k}(H^{0}\psi_{n}^{k}+H'\psi_{n}^{k-1})=E_{n}^{0}\psi_{n}^{0}+\sum\limits_{k=1}^{\infty}\lambda^{k}\sum\limits_{j=0}^{k}E_{n}^{j}\psi_{n}^{k-j}$$
Esplicitando i primi termini si ha
$$\begin{align}
H^{0}\psi_{n}^{0}+\lambda (H^{0}\psi_{n}^{1}+H'\psi_{n}^{0})+\lambda^{2}(H^{0}\psi_{n}^{2}+H'\psi_{n}^{1})+\ldots \\
=E^{0}_{n}\psi_{n}^{0}+\lambda(E_{n}^{0}\psi_{n}^{1}+H^{1}_{n}\psi_{n}^{0})+\lambda^{2}(E_{n}^{0}\psi_{n}^{2}+E_{n}^{1}\psi_{n}^{1}+E_{n}^{2}\psi_{n}^{0})+\ldots
\end{align}$$
Eguagliando i termini con $k$ uguale ritroviamo
$$H^{0}\psi_{n}^{0}=E_{n}^{0}\psi_{n}$$
che è il sistema non perturbato, ma anche
$$\boxed{\sum\limits_{k=1}^{\infty}\lambda^{k}(H^{0}\psi_{n}^{k}+H'\psi_{n}^{k-1})=\sum\limits_{k=1}^{\infty}\lambda^{k}\sum\limits_{j=0}^{k}E_{n}^{j}\psi_{n}^{k-j}}$$
Dato che l'uguaglianza deve valere termine a termine[^1], queste sono le correzioni di $k$-esimo ordine. Questa equazione è vera per ogni $\lambda$. Per esempio, al primo ordine:
$$H^{0}\psi_{n}^{1}+H'\psi_{n}^{0}=E_{n}^{0}\psi_{n}^{1}+E_{n}^{1}\psi_{n}^{0}\tag{2}$$
Al secondo ordine:
$$H^{0}\psi_{n}^{2}+ H'\psi_{n}^{1}=E_{n}^{0}\psi_{n}^{2}+E^{1}_{n}\psi_{n}^{1}+E_{n}^{2}\psi_{n}^{0}\tag{3}$$
#### Primo ordine
Compiendo il [[prodotto scalare]] tra la $(2)$ e $\psi_{n}^{0}$ (ossia moltiplicando per $(\psi_{n}^{0})^{*}$ e poi integrando) si ha
$$\langle \psi_{n}^{0}|H^{0}\psi_{n}^{1}\rangle+\langle \psi_{n}^{0}|H'\psi_{n}^{0}\rangle=E_{n}^{0}\langle \psi_{n}^{0}|\psi_{n}^{1}\rangle+E_{n}^{1}\langle \psi_{n}^{0}|\psi_{n}^{0}\rangle$$
Ricordando che $H$ qui è l'[[operatore]] Hamiltoniana e che è [[Operatore autoaggiunto|autoaggiunto]], vale
$$\langle \psi_{n}^{0}|H^{0}\psi_{n}^{1}\rangle=\langle H^{0}\psi_{n}^{0}|\psi_{n}^{1}\rangle=E_{n}^{0}\langle \psi_{n}^{0}|\psi_{n}^{1}\rangle=0$$
per [[ortogonalità]]. Inoltre, $\langle \psi_{n}^{0}|\psi_{n}^{0}\rangle=1$ per [[normalizzazione]]. Allora
$$\boxed{E_{n}^{1}=\langle \psi_{n}^{0}|H'|\psi_{n}^{0}\rangle}$$
Questo è il risultato principale della teoria delle perturbazioni non degenere di primo ordine.

> **Risultato.** La correzione di primo ordine all'energia è pari al valor medio della perturbazione nello stato non perturbato.

Troviamo ora la correzione alla [[funzione d'onda]]. Riscriviamo la $(2)$ come
$$(H^{0}-E_{n}^{0})\psi_{n}^{1}=-(H'-E_{n}^{1})\psi_{n}^{0}\tag{4}$$
La parte destra è nota (conosciamo la perturbazione e la funzione d'onda non perturbata per definizione, mentre la correzione all'energia l'abbiamo trovata sopra). L'unica incognita è $\psi_{n}^{1}$. Sfruttiamo il fatto che la funzione d'onda non perturbata costituisce un [[sistema ortonormale completo]] per esprimere $\psi_{n}^{1}$ in funzione di $\psi_{n}^{0}$:
$$\psi_{n}^{1}=\sum\limits_{m\neq n}c_{m}^{(n)}\psi_{m}^{0}$$
Non c'è bisogno di aggiungere $m=n$ nella somma poiché se $\psi_{n}^{1}$ soddisfa la $(4)$, allora lo fa anche $(\psi_{n}^{1}+\alpha\psi_{n}^{0})$ con $\alpha$ costante. Allora possiamo togliere $\psi_{n}^{0}$ dall'equazione senza perdita di generalità. Vogliamo trovare i coefficienti $c_{m}^{(n)}$. Sostituendo l'espansione nella $(4)$ e usando che la $\psi_{m}^{0}$ soddisfa l'equazione di Schrödinger non perturbata $H^{0}\psi_{m}^{0}=E_{m}^{0}\psi_{m}^{0}$ abbiamo
$$\sum\limits_{m\neq n}(E_{m}^{0}-E_{n}^{0})c_{m}^{(n)}\psi_{m}^{0}=-(H'-E_{n}^{1})\psi_{n}^{0}$$
e compiendo il prodotto scalare con $\psi_{l}^{0}$ abbiamo
$$\sum\limits_{m\neq n}(E_{m}^{0}-E_{n}^{0})c_{m}^{(n)}\langle \psi_{l}^{0}|\psi_{m}^{0}\rangle=-\langle \psi_{l}^{0}|H'|\psi_{n}^{0}\rangle+E_{n}^{1}\langle \psi_{l}^{0}|\psi_{n}^{0}\rangle$$
Per $l=n$ il membro sinistro è nullo e riotteniamo la correzione di primo ordine di energia. Nel caso $l\neq n$ abbiamo
$$(E_{l}^{0}-E_{n}^{0})c_{l}^{(n)}=-\langle \psi_{l}^{0}|H'|\psi_{n}^{0}\rangle$$
da cui (rinominando $l$ a $m$)
$$c_{m}^{(n)}=\frac{\langle \psi_{m}^{0}|H'|\psi_{n}^{0}\rangle}{E_{n}^{0}-E_{m}^{0}}$$
e quindi
$$\boxed{\psi_{n}^{1}=\sum\limits_{m\neq n} \frac{\langle \psi_{m}^{0}|H'|\psi_{n}^{0}\rangle}{E_{n}^{0}-E_{m}^{0}}\psi_{m}^{0}}$$
Questa equazione ci dà la correzione di primo ordine alla funzione d'onda. C'è un dettaglio importante: è valida solo se lo [[spettro]] di energia non perturbato è *non degenere*. Se fosse degenere, dovremmo dividere per zero per ottenere l'espressione per i coefficienti. Infatti, qui stiamo supponendo che $E_{n}^{0}\neq E_{m}^{0}$ per ogni $n$, $m$, che è equivalente a chiedere la non degenerazione.
##### Perturbazione costante
Consideriamo una perturbazione costante del tipo
$$H'=V_{0}$$
come per esempio "alzare il fondo" della [[Buca infinita quantistica|buca infinita]] di un potenziale predefinito $V_{0}$. Allora, la correzione di primo ordine sarà
$$E_{n}^{1}=\langle \psi_{n}^{0}|V_{0}|\psi_{n}^{0}\rangle=V_{0}\langle \psi_{n}^{0}|\psi_{n}^{0}\rangle=V_{0}$$
e quindi il livello d'energia corretto sarà
$$E_{n}\simeq E_{n}^{0}+V_{0}$$
che capita essere non una soluzione approssimata, bensì quella esatta.

> **Risultato.** Per una perturbazione costante, tutti le correzioni di ordine superiore al primo svaniscono. La correzione di primo ordine è la perturbazione stessa.
##### Precisione
La correzione di primo ordine è quella più semplice. La correzione all'energia è solitamente piuttosto accurata, nel senso che $E_{n}^{1}+E_{n}^{1}$ è solitamente piuttosto vicina ad $E_{esatta}$. Tuttavia, la correzione alla funzione d'onda è scarsa e non è sufficiente ad una buona approssimazione.
#### Secondo ordine
Possiamo compiere l'esatto procedimento di sopra per trovare le correzioni di secondo ordine. La correzione alle energie si trova prendendo il prodotto scalare della $(3)$ e poi sfruttando l'autoaggiuntezza di $H^{0}$ per ottenere
$$E_{n}^{2}=\langle \psi_{n}^{0}|H'|\psi_{n}^{1}\rangle-E_{n}^{1}\langle \psi_{n}^{0}|\psi_{n}^{1}\rangle$$
ma
$$\langle \psi_{n}^{0}|\psi_{m}^{1}\rangle=\sum\limits_{m\neq n}c_{m}^{(n)}\langle \psi_{n}^{0}|\psi_{m}^{0}\rangle=0$$
quindi
$$E_{n}^{2}=\langle \psi_{n}^{0}|H'|\psi_{n}^{1}\rangle=\sum\limits_{m\neq n}c_{m}^{(n)}\langle \psi_{n}^{0}|H'|\psi_{m}^{0}\rangle=\sum\limits_{m\neq n}\frac{\langle \psi_{m}^{0}|H'|\psi_{n}^{0}\rangle \langle \psi_{n}^{0}|H'|\psi_{m}^{0}\rangle}{E_{n}^{0}-E_{m}^{0}}$$
da cui
$$\boxed{E_{n}^{2}=\sum\limits_{m\neq n} \frac{|\langle \psi_{m}^{0}|H'|\psi_{n}^{0}\rangle|^{2}}{E_{n}^{0}-E_{m}^{0}}}$$
Questo è il risultato principale della teoria delle perturbazioni non degenere di secondo ordine. È possibile anche calcolare la correzione alla funzione d'onda di secondo ordine, ma in genere le correzione di primo ordine assieme a questa di secondo sono quelle usate all'atto pratico.
#### Ordine qualunque
Si trova che la correzione di $k$-esimo ordine all'energia è pari a
$$E_{n}^{k}=\langle \psi_{n}^{0}|H'|\psi_{n}^{k-1}\rangle$$
e quella alla funzione d'onda
$$\psi_{n}^{k}=\sum\limits_{m\neq n} \frac{1}{E_{n}^{0}-E_{m}^{0}}\left(\langle \psi_{m}^{0}|H'|\psi_{n}^{k-1}\rangle - \sum\limits_{l=1}^{k-1}E_{n}^{l}\langle \psi_{n}^{0}|\psi_{n}^{(k-l)}\rangle\right)\psi_{m}^{0}$$
Le correzioni alle funzioni d'onda sono tutte normalizzate.

[^1]: Questo segue dall'unicità della serie di potenze.