La **teoria delle perturbazioni degenere** è una forma della [[Meccanica quantistica/Tecniche/Teoria delle perturbazioni]] indipendente dal tempo nella quale gli [[Equazione agli autovalori|autovalori]] dell'[[Hamiltoniana]] imperturbata sono [[degenerazione|degeneri]]. Ciò vale a dire che, presi due o più [[stato|stati]] distinti del sistema non perturbato $\psi_{a}^{0}$ e $\psi_{b}^{0}$, questi hanno la stessa energia. In questo caso, la forma [[Teoria delle perturbazioni non degenere|non degenere]] della teoria fallisce, dato che il denominatore $E_{n}^{0}-E_{m}^{0}$ è zero per $n=a$ e $m=b$.

Consideriamo un'Hamiltoniana del tipo
$$\hat{H}=\hat{H}^{0}+\lambda \hat{V}$$
con $\hat{V}$ la perturbazione e $\lambda$ una costante. $\hat{H}^{0}$ è l'Hamiltoniana non perturbata, che risolve il sistema descritto dall'[[Equazione di Schrödinger#Potenziale indipendente dal tempo|equazione di Schrödinger indipendente dal tempo]]
$$\hat{H}^{0}\psi_{n}^{0}=E_{n}^{0}\psi_{n}^{0}$$
La dinamica del sistema perturbato invece è descritto da
$$\hat{H}\psi_{n}=E_{n}\psi_{n}\tag{1}$$
### Formulazione
#### Due volte degenere
Supponiamo che
$$H^{0}\psi_{a}^{0}=E^{0}\psi_{a}^{0}, \quad H^{0}\psi_{b}^{0}=E^{0}\psi_{b}^{0}, \quad \langle \psi_{a}^{0}|\psi_{b}^{0} \rangle=0$$
dove $\psi_{a}^{0}$ e $\psi_{b}^{0}$ sono [[Normalizzazione|normalizzati]] e fra loro degeneri. Dato che autostati degeneri formano una [[base]] del loro autospazio, una loro combinazione lineare è sempre un autostato
$$\psi^{0}=\alpha \psi_{a}^{0}+\beta \psi_{b}^{0}\tag{2}$$
con lo stesso autovalore, a modo che valga
$$H^{0}\psi^{0}=E^{0}\psi^{0}$$

Tipicamente, la perturbazione $\hat{V}$ "rompe" la degenerazione, creando due stati diversi con autovalori di energia diversi. Man mano che $\lambda$ aumenta, l'autostato non perturbato $E^{0}$ si divide in due: uno ad energia più alta, uno ad energia più bassa. Al contrario, se rimuoviamo la perturbazione, lo stato più energetico ritorna ad essere una *specifica* combinazione lineare di due stati $\psi_{a}^{0}$ e $\psi_{b}^{0}$, mentre quello meno energetico diventa una combinazione lineare [[Ortogonalità|ortogonale]]. Il problema sta nel fatto che, a priori, noi non sappiamo quali sono questi stati specifici.

![[Divisione autostati in perturbazione.png]]
*Da Introduction to Quantum Mechanics di Griffiths, p. 260*

Per ora, scriviamo gli stati "buoni" nella forma generica, senza pensare a $\alpha$ e $\beta$. Vogliamo risolvere l'[[equazione di Schrödinger]]
$$H\psi=E\psi$$
con $H=H^{0}+\lambda \hat{V}$. Espandendo $E$ e $\psi$ in [[serie di potenze]] in $\lambda$ abbiamo
$$\psi=\psi^{0}+\lambda\psi^{1}+\lambda^{2}\psi^{2}+\ldots=\sum\limits_{i=0}^{\infty}\lambda^{i}\psi^{i}$$
$$E=E^{0}+\lambda E^{1}+\lambda^{2}E^{2}+\ldots=\sum\limits_{i=0}^{\infty}\lambda^{i}E^{i}$$
Sostituendo
$$(H^{0}+\lambda \hat{V})\left(\sum\limits_{i=0}^{\infty}\lambda^{i}\psi^{i}\right)=\left(\sum\limits_{i=0}^{\infty}\lambda^{i}E^{i}\right)\left(\sum\limits_{i=0}^{\infty}\lambda^{i}\psi^{i}\right)$$
e come nella teoria degenere si trova
$$H^{0}\psi^{0}+\sum\limits_{k=1}^{\infty}\lambda^{k}(H^{0}\psi^{k}+\hat{V}\psi^{k-1})=E^{0}\psi^{0}+\sum\limits_{k=1}^{\infty}\lambda^{k}\sum\limits_{j=0}^{k}E^{j}\psi^{k-j}$$
Ma $H^{0}\psi^{0}=E^{0}\psi^{0}$, quindi il primo termine si annulla e rimane
$$\sum\limits_{k=1}^{\infty}\lambda^{k}(H^{0}\psi^{k}+\hat{V}\psi^{k-1})=\sum\limits_{k=1}^{\infty}\lambda^{k}\sum\limits_{j=0}^{k}E^{j}\psi^{k-j}$$
per il $k$-esimo ordine.
##### Primo ordine
Il primo ordine è
$$H^{0}\psi^{1}+\hat{V}\psi^{0}=E^{0}\psi^{1}+E^{1}\psi^{0}$$
Prendendo il [[prodotto scalare]] con $\psi_{a}^{0}$ troviamo
$$\langle \psi_{a}^{0}|H^{0}\psi^{1}\rangle+\langle \psi_{a}^{0}|\hat{V}\psi^{0}\rangle=E^{0}\langle \psi_{a}^{0}|\psi^{1}\rangle+E^{1}\langle \psi_{a}^{0}|\psi^{0}\rangle$$
Usando l'[[Operatore autoaggiunto|autoaggiuntezza]] di $H^{0}$, il primo termine a sinistra si semplifica con il primo a destra, lasciando
$$\langle \psi_{a}^{0}|\hat{V}\psi^{0}\rangle=E^{1}\langle \psi_{a}^{0}|\psi^{0}\rangle$$
Espandendo $\psi_{0}$ in $(2)$ troviamo
$$\alpha \langle \psi_{a}^{0}|\hat{V}\psi_{a}^{0}\rangle+\beta \langle \psi_{a}^{0}|\hat{V}\psi_{b}^{0}\rangle=\alpha E^{1}$$
Chiamando
$$W_{ij}\equiv \langle \psi_{i}^{0}|\hat{V}|\psi_{j}^{0}\rangle$$
abbiamo una forma più compatta
$$\alpha W_{aa}+\beta W_{ab}=\alpha E^{1}\tag{3}$$
Se invece prendiamo il prodotto scalare con $\psi_{b}^{0}$ troviamo
$$\alpha W_{ba}+\beta W_{bb}=\beta E^{1}\tag{4}$$

In principio, i $W_{ij}$ sono tutti noti: non sono altro gli elementi di matrice dell'[[operatore lineare]] Hamiltoniano espressi nella base dei suoi autostati non perturbati. Possiamo moltiplicare la $(4)$ equazione per $W_{ab}$ e poi sostituire la $(3)$ per trovare
$$\alpha[W_{ab}W_{ba}-(E^{1}-W_{aa})(E^{1}-W_{bb})]=0$$
Se $\alpha$ non è zero, possiamo trovare un'equazione per $E^{1}$:
$$(E^{1})^{2}-E^{1}(W_{aa}+W_{bb})+(W_{aa}W_{bb}-W_{ab}W_{ba})=0$$
che può essere risolto con la formula per polinomi di secondo grado, ricordando che per definizione $W_{ba}=W_{ab}^{*}$:
$$\boxed{E_{\pm}^{1}= \frac{1}{2}\left[W_{aa}+W_{bb}\pm\sqrt{(W_{aa}-W_{bb})^{2}+4|W_{ab}|^{2}}\right]}\tag{5}$$
Questo è il risultato principale della teoria degenere. Le correzione di primo ordine dell'energia sono due, a differenza della teoria non degenere. Ma c'è un altro caso da seguire.

Se $\alpha$ è zero, allora segue che $\beta=1$ (perché deve valere $|\alpha|^{2}+|\beta|^{2}=1$ nella combinazione lineare se vogliamo la normalizzazione) e la $(3)$ e la $(4)$ diventano
$$W_{ab}=0, \quad W_{bb}=E^{1}$$
Ma in realtà, questo caso è incluso nella $(5)$, dove assumendo $W_{aa}>W_{bb}$, il segno meno corrisponde appunto a $\alpha=0$ e $\beta=1$. E anche il segno più è interessante, dato che corrisponde a $\alpha=1$ e $\beta=0$, per il quale
$$W_{aa}=E^{1}, \quad W_{ba}=0$$
e quindi si ha
$$\boxed{E_{+}^{1}=W_{aa}=\langle \psi_{a}^{0}|\hat{V}|\psi_{a}^{0}\rangle, \quad E_{-}^{1}=W_{bb}=\langle \psi_{b}^{0}|\hat{V}|\psi_{b}^{0}\rangle}\tag{6}$$
che sono proprio le correzioni date dalle teoria non degenere, solo per gli stati "buoni". Allora, se avessimo un modo per scoprire quali sono gli stati "buoni" a priori, potremmo semplicemente usare la teoria non degenere nei due casi per trovare le correzioni. Questo modo esiste e si enuncia con il seguente teorema:

> [!info] Teorema
> Sia $\hat{A}$ un [[operatore autoaggiunto]] che [[Commutatore|commuta]] con $\hat{H}^{0}$ e $\hat{H}'$ (ossia è una [[costante del moto]]). Se $\psi_{a}^{0}$ e $\psi_{b}^{0}$ sono [[Equazione agli autovalori|autofunzioni]] [[Degenerazione|degeneri]] di $\hat{H}^{0}$ e sono anche autofunzioni di $\hat{A}$ con autovalori distinti$$\hat{A}\psi_{a}^{0}=\mu \psi_{a}^{0},\quad \hat{A}\psi_{b}^{0}=\nu\psi_{b}^{0},\quad \text{con }\mu\neq\nu$$allora $W_{ab}=0$ e vale la $(6)$.
> 
> **Dimostrazione.** Per assunzione, vale $[\hat{A},\hat{H}']=0$, quindi$$\begin{align}
\langle \psi_{a}^{0}|[\hat{A},\hat{H}']|\psi_{b}^{0}\rangle &= 0 \\
&= \langle \psi_{a}^{0}|\hat{A}\hat{H}'\psi_{b}^{0}\rangle-\langle \psi_{a}^{0}|\hat{H}'\hat{A}\rangle \\
&=\langle \hat{A}\psi_{a}^{0}|\hat{H}'\psi_{b}^{0}\rangle-\langle \psi_{a}^{0}|\hat{H}'\nu \psi_{b}^{0}\rangle\\
&=(\mu-\nu)\langle \psi_{a}^{0}|\hat{H}'\psi_{b}^{0}\rangle \\
&=(\mu-\nu)W_{ab}
\end{align}$$ma $\mu\neq\nu$ per definizione, quindi $W_{ab}=0$.

> [!success] Risultato
> Se si hanno stati degeneri, conviene cercare un operatore autoaggiunto $\hat{A}$ che commuta con $\hat{H}^{0}$ e $\hat{H}'$ e poi scegliere come stati non perturbati $\psi_{a}^{0}$ e $\psi_{b}^{0}$ due che sono simultaneamente autofunzioni di $\hat{A}$ e $\hat{H}^{0}$. In questo modo, si può usare direttamente la $(6)$. Altrimenti, è necessario fare tutti i calcoli per la $(5)$, che è universalmente valida.
#### Degenerazione qualunque
Per trovare la correzione per un grado di degenerazione qualunque, conviene riscrivere la $(3)$ e la $(4)$ come un'unica equazione matriciale
$$\mathbf{W}\begin{pmatrix}
\alpha \\
\beta
\end{pmatrix}=\pmatrix{W_{aa} & W_{ab} \\ W_{ba} & W_{bb}}\pmatrix{\alpha \\ \beta}=E^{1}\pmatrix{\alpha \\ \beta}$$
Le correzioni di primo ordine all'energia non sono altro che gli autovalori della matrice $\mathbf{W}$ e i parametri delle combinazioni lineari "buone" sono gli autovettori ad essi associati. La $(5)$ è solo la soluzione dell'[[Equazione agli autovalori|equazione caratteristica]] di $\mathbf{W}$.

Per uno stato $n$-volte degenere, dobbiamo cercare gli autovalori della matrice $n\times n$ definita dagli elementi
$$W_{ij}=\langle \psi_{i}^{0}|\hat{V}|\psi_{j}^{0}\rangle$$
Dato che vogliamo avere $W_{ij}=0$ per ogni $i\neq j$ per il teorema precedente, ciò che stiamo cercando di fare è [[diagonalizzazione|diagonalizzare]] la matrice. Se troviamo una base per la quale $\mathbf{W}$ è diagonale, allora gli $n$ elementi di quella base sono gli $n$ autostati "buoni" che ci danno le $n$ correzioni di primo ordine all'energia usando le formule della teoria non degenere.

> [!success] Risultato
> Gli autostati non perturbati degeneri si spezzano in un numero di autostati perturbati pari al loro grado di degenerazione. Le correzioni degli autostati sono date dalla base di autostati che diagonalizza la matrice $\mathbf{W}$ usando la teoria non degenere, e le correzione delle energie sono gli autovalori associati.
