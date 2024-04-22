Le [[Equazione agli autovalori|autofunzioni]] di [[Operatore autoaggiunto|operatori autoaggiunti]] svolgono un ruolo cruciale nella meccanica quantistica, dato che corrispondono a [[Stato determinato|stati determinati]] di un'[[osservabile]] e quindi ci permettono di "bypassare" il [[Disuguaglianza di Heisenberg|principio di indeterminazione]].

Prendiamo un'osservabile $Q$ con operatore associato $\hat{Q}$. Se lo [[spettro]] di $\hat{Q}$ è discreto, le autofunzioni esistono in [[Spazi Lp#Spazio $L {2}$|L^2]] e corrispondono a stati fisicamente realizzabili. Se lo spettro è continuo, le autofunzioni non sono normalizzabili e non rappresentano alcuna [[funzione d'onda]], anche se una loro combinazione lineare forse sì.
## Spettro discreto
Le autofunzioni di un operatore autoaggiunto hanno due importanti proprietà:
1. Hanno autovalori reali.
2. Autofunzioni corrispondenti ad autovalori diversi sono [[Ortogonalità|ortogonali]].
#### Dimostrazioni
*Autovalori reali.* Consideriamo l'equazione agli autovalori $\hat{Q}f=qf$. Dato che lo spettro è discreto per costruzione, le autofunzioni sono $L^{2}$, quindi appartengono ad uno spazio dotato di [[prodotto scalare]]. Allora, per l'autoaggiuntezza, vale
$$\langle f|\hat{Q}f\rangle=\langle \hat{Q}f|f\rangle$$
Dunque dall'equazione agli autovalori si ha
$$q\langle f|f\rangle=q^{*}\langle f|f\rangle$$
Questa equazione è vera solo se $q=q^{*}$ o $f=0$, ma le autofunzioni non possono essere nulle per definizione, quindi segue che $q=q^{*}$, ossia $q\in\mathbb{R}$.

*Autofunzioni ortogonali.* Consideriamo l'equazione agli autovalori per due autovalori distinti $q$ e $q'$ e due autofunzioni $f$ e $g$:
$$\hat{Q}f=qf,\quad \hat{Q}g=q'g$$
Per l'autoaggiuntezza di $\hat{Q}$ e perché $f,g\in L^{2}$ vale
$$\langle f|\hat{Q}g\rangle=\langle \hat{Q}f|g\rangle \quad\rightarrow\quad q'\langle f|g\rangle=q^{*}\langle f|g\rangle$$
Se $q$ è reale per il punto uno e $q'\neq q^{*}$, deve valere $\langle f|g\rangle=0$.  $\square$

L'unico dettaglio che manca ai due risultati è cosa accade quando ci sono due stati degeneri, tali per cui $q'=q$. Fortunatamente non è un grande problema, dato che la combinazione lineare di due autofunzioni con lo stesso autovalore è essa stessa un'autofunzione con lo stesso autovalore. Allora, sfruttando l'[[ortonormalizzazione di Gram-Schmidt]], è sempre possibile costruire una [[base]] [[Ortonormalità|ortonormale]] nell'(auto)spazio degenere. Ciò implica che, degenerazione o meno, le autofunzioni possono essere sempre scelte come tutte ortogonali; al peggio basta ortonormalizzare.

Esiste una terza proprietà in dimensione *finita*: gli autovettori di una matrice autoaggiunta generano lo spazio. La dimostrazione, purtroppo, non è valida per spazi a dimensione infinita. Tuttavia, questa proprietà è assolutamente necessaria affinché i fondamenti matematici della meccanica quantistica rimangano coerenti, così, seguendo la guida di Dirac, decidiamo che questa proprietà sia vera come un'*assioma* (che in realtà è dimostrabile in certi casi, come la [[Buca infinita quantistica|buca infinita]]).

>**Assioma.** Le autofunzioni di un'osservabile formano un [[sistema completo]].

## Spettro continuo
I due risultati ottenuti rispetto allo spettro discreto non valgono poiché non c'è alcuna garanzia che le autofunzioni esistano in uno spazio dotato di prodotto scalare. È dunque necessario aggiungere delle condizioni.
###  $p$ non ha autofunzioni in $L^{2}$
Consideriamo l'[[equazione agli autovalori]]
$$\frac{\hbar}{i} \frac{d}{dx}f_{p}(x)=pf_{p}(x)$$
la cui soluzione generale è $f_{p}(x)=Ae^{ipx/\hbar}$. Questa soluzione non è normalizzabile, quindi le autofunzioni non sono [[Spazi Lp|L^2]]. Vale che
$$\int_{-\infty}^{+\infty}f_{p'}(x)f_{p}(x)dx=|A|^{2}\int_{-\infty}^{+\infty}e^{i(p-p')x/\hbar}dx=|A|^{2}2\pi\hbar\delta(p-p')$$
con $p$ e $p'$ due autovalori che decidiamo siano reali e $\delta$ la [[delta di Dirac]]. Scelta $A=1/\sqrt{2\pi\hbar}$ si ha
$$f_{p}(x)=\frac{1}{\sqrt{2\pi\hbar}}e^{ipx/\hbar}\tag{1}$$
e quindi
$$\langle f_{p'}|f_{p}\rangle=\delta(p-p')$$
Questo risultato è molto simile all'[[ortonormalità]], ma con variabili continue anziché discrete e la delta di Dirac anziché quella [[Delta di Kronecker|di Kronecker]]. Possiamo chiamarla **Dirac-ortonormalità**. Dato che le autofunzioni formano un [[sistema completo]] e in un sistema continuo vale
$$f(x)=\int_{-\infty}^{+\infty}c(p)f_{p}(x)dp=\frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^{+\infty}c(p)e^{ipx/\hbar}dp$$
che è una [[trasformata di Fourier]].

Le autofunzioni $(1)$ sono sinusoidali con lunghezza d'onda
$$\lambda=\frac{2\pi\hbar}{p}$$
che non è altro che la [[formula di de Broglie]]. Queste autofunzioni non rappresentano stati fisicamente ottenibili, ma in certi casi (se le funzioni ammettono autovalore reale), possono comunque tornare utili nel trattamento matematico di un sistema; vedi [[particella libera]].
### Autofunzioni di $x$
Consideriamo l'equazione agli autovalori
$$xg_{y}(x)=yg_{y}(x)$$
con $y$ gli autovalori e $x$ la posizione. L'unica funzione per la quale è valida questa equazione è la delta di Dirac, dato che deve essere 0 ovunque tranne che in $x=y$. Allora si ha
$$g_{y}(x)=A\delta(x-y)$$
Qui l'autovalore deve essere reale, quindi sebbene le autofunzioni non siano $L^{2}$, comunque ammettono la Dirac-ortonormalità
$$\int_{-\infty}^{+\infty}g^{*}_{y'}(x)g_{y}(x)dx=|A|^{2}\int_{-\infty}^{+\infty}\delta(x-y')\delta(x-y)dx=|A|^{2}\delta(y-y')$$
e con $A=1$
$$g_{y}(x)=\delta(x-y), \quad \langle g_{y'}|g_{y}\rangle=\delta(y-y')$$
e il sistema è completo
$$f(x)=\int_{-\infty}^{+\infty}c(y)g_{y}(x)dy=\int_{-\infty}^{+\infty}c(y)\delta(x-y)dy$$

### Conclusioni
Abbiamo quindi che se lo spettro di un operatore autoaggiunto è continuo, allora le sue autofunzioni non sono normalizzabili e non rappresentano una soluzione fisica. Queste autofunzioni:
- sono indicizzate da una variabile continua e non una discreta
- non sono normalizzabili
- non sono $L^{2}$
- non rappresentano soluzioni fisiche

Ciò non significa siano inutili. Se restringiamo l'insieme alle autofunzioni con autovalore reale si ha che:
- sono Dirac-ortonormali
- formano un sistema completo
Queste due proprietà sono sufficienti a renderle utili.