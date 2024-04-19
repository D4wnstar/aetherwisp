Le [[Equazione agli autovalori|autofunzioni]] di [[Operatore autoaggiunto|operatori autoaggiunti]] svolgono un ruolo cruciale nella meccanica quantistica, dato che corrispondono a [[Stato determinato|stati determinati]] di un'[[osservabile]] e quindi ci permettono di "bypassare" il [[Disuguaglianza di Heisenberg|principio di indeterminazione]].

Prendiamo un'osservabile $Q$ con operatore associato $\hat{Q}$. Se lo [[spettro]] di $\hat{Q}$ è discreto, le autofunzioni esistono in [[Spazi Lp#Spazio $L {2}$|L^2]] e corrispondono a stati fisicamente realizzabili. Se lo spettro è continuo, le autofunzioni non sono normalizzabili e non rappresentano alcuna [[funzione d'onda]], anche se una loro combinazione lineare forse sì.
### Spettro discreto
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
