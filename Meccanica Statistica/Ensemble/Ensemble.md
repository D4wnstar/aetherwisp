Un **ensemble di Gibbs** è un *insieme di punti nello spazio delle fasi*.

Consideriamo lo spazio delle fasi a $6N$ dimensioni dei **punti rappresentativi**: $\Gamma:(q_{0},q_{1},\ldots,q_{3N};p_{1},p_{2},\ldots,p_{3N})\equiv (q,p)$. Per analizzare il sistema possiamo fare una media temporale delle posizioni delle particelle nel tempo: $\langle f(p,q)\rangle_{t}$. Vogliamo fare un'analisi più dettagliata di una semplice media temporale.

Diciamo che esiste una funzione $x(q,p)=E$ che è uguale ad una qualche costante. Denotiamo le derivate con $\dot{q}_{i}=\frac{\partial x}{\partial p_{i}}$ e $\dot{p}_{i}=\frac{\partial x}{\partial q_{i}}$. Allora la funzione $x$ ci descrive un'ipersuperficie in $6N-1$ dimensioni. Se troviamo questa funzione, possiamo trovare una media sullo spazio delle fasi, anziché usare la media nel tempo.

Ovviamente trattare ogni punto singolarmente è impossibile per il semplice numero di punti presenti ([[Numero di Avogadro]]), quindi possiamo semplificare assegnando un volumetto a ciascun punto. Definisco la **densità di punti rappresentativa in $\Gamma$**:
$$\rho(q;p;t)dq^{3N}dp^{3N}$$
che è un differenziale. Prendo una costante $h$ con le dimensioni di un'azione (un impulso, $J\times s$) e lo divido
$$\rho(q;p;t)\frac{dq^{3N}dp^{3N}}{h^{3N}}$$
che è il numero di punti rappresentativi in $dq^{3N}dp^{3N}$. Considero una funzione $f(q,p)$ sui punti rappresentativi. Allora la sua media sullo spazio delle fasi sarà
$$\langle f(p,q)\rangle=\frac{\int\rho(q,p,t)f(q,p)dp^{3N}dq^{3N}}{\int\rho(q,p,t)dp^{3N}dq^{3N}}$$
Se le traiettorie ricoprono lo spazio delle fasi in maniera uniforme, è soddisfatta l'**[[Ipotesi ergodica]]** e possiamo sostituire questa media a quella temporale.