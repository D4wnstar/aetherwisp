Lo **spin** $\hat{S}$ è l'equivalente quantistico del momento angolare di spin di un corpo. È rappresentato da un [[operatore]] vettoriale in tre dimensioni
$$\hat{S}=(\hat{S}_{x},\hat{S}_{y},\hat{S}_{z})$$

In meccanica classica esistono due tipi di momenti angolare: quello *orbitale*, $\vec{L}=\vec{r}\times\vec{p}$, che rappresenta il momento di un oggetto attorno ad un punto esterno (come la Terra che orbita attorno al Sole), e quello di *spin*, che rappresenta il momento di un oggetto attorno al proprio asse (come la Terra che ruota su se stessa ogni giorno). Se il [[momento angolare quantistico]] spiega il momento orbitale, lo spin rappresenta, appunto, il momento di spin.

Il problema di fondo è che in meccanica classica, il momento di spin è sostanzialmente un'astrazione di comodità; d'altronde, ogni momento di spin di un oggetto esteso può essere spiegato come momento orbitale delle sue componenti rispetto al centro di massa[^1]. In meccanica quantistica, tuttavia, lo spin ha un suo significato intrinseco. Dato che le [[particella|particelle]] elementari sono modellate come oggetti puntiformi prive di struttura interna, è impossibile decomporre lo spin in somma di momenti orbitali delle componenti interne, dato che non ci sono componenti interne. Allora, lo spin quantistico è una proprietà indipendente della particella con un suo significato fisico.
### Commutatività
Applicando il [[commutatore]] alle componenti e omettendo il cappuccio si ottiene
$$\begin{cases}
[S_{x},S_{y}]=i\hbar S_{z} \\
[S_{y},S_{z}]=i\hbar S_{x} \\
[S_{z},S_{x}]=i\hbar S_{y}
\end{cases}$$
che sono tutti non nulli. Non è quindi possibile costruire [[Equazione agli autovalori|autostati]] simultanei per le componenti dello spin e quindi non è possibile misurarle simultaneamente. Si prova con lo stesso metodo del [[momento angolare quantistico]] che $[S^{2},S_{z}]=0$.
### Autovalori
Come per il momento angolare orbitale, si trova che valgono le equazioni
$$S^{2}|sm_{s}\rangle=\hbar^{2}s(s+1)|sm_{s}\rangle, \quad S_{z}|sm_{s}\rangle=\hbar m_{s} |sm_{s}\rangle\tag{1}$$
dove si usano i [[Notazione braket|ket]] per ricordare che gli autostati dello spin *non sono funzioni* e quindi non dovrebbero essere rappresentati come tali[^2]. Gli [[operatori di creazione e distruzione]] usati nella dimostrazione sono
$$S_{\pm}|sm\rangle=\hbar\sqrt{s(s+1)-m(m\pm1)}|s(m\pm1)\rangle$$
con $S_{\pm}=S_{x}\pm iS_{y}$. In questo caso le autofunzioni non sono le [[armoniche sferiche]] (di fatto, non c'è neanche una dipendenza da $\theta$ e $\phi$) e non c'è alcuna ragione per escludere valori di mezzo intero per $s$ e $m_{s}$, che possono quindi avere valori
$$s=0,\frac{1}{2},1,\frac{3}{2},\ldots; \quad m_{s}=-s,-s+1,\ldots,0,\ldots,s-1,s$$
$s$ è detto il **[[numero quantico]] di spin** e si trova che ogni singola particella elementare ha un valore costante e immutabile di $s$, che si dice essere lo spin della particella. Questo è diverso dal momento orbitale, che invece dipende dallo [[Stato]] in cui si trova la particella.
### Spin 1/2
Il caso dello spin $s=1/2$ è di gran lunga il più importante, dato che tutte le particelle che compongono la materia ordinaria ([[protone]], [[neutrone]], [[elettrone]]) hanno spin 1/2, così come tutti i [[quark]] e tutti i [[Leptone|leptoni]].

Ha anche la fortuna di essere il caso più facile possibile, grazie al fatto che esistono solo due possibili autostati per $s$ e $m_{s}$: $| \frac{1}{2},\frac{1}{2}\rangle$ e $| \frac{1}{2}, -\frac{1}{2}\rangle$. Questi due stati vengono comunemente chiamati **spin up** $\uparrow$ e **spin down** $\downarrow$. I vettori che rappresentano questi due stati compongono una [[base]] in $\mathbb{C}^{2}$ e possono dunque essere combinati linearmente per creare stati misti espressi come vettori colonna bidimensionali (ossia degli [[spinore|spinori]]):
$$\chi=\pmatrix{a \\ b}=a |\uparrow\;\rangle+b |\downarrow\;\rangle$$
con
$$|\uparrow\;\rangle=\pmatrix{1 \\0 }, \quad |\downarrow\;\rangle=\pmatrix{0 \\ 1}$$
$\chi$ è anche detto [[qubit]], dato che generalizza il concetto di bit classico.

In questo spazio, gli operatori di spin non sono altro che matrici $2\times 2$, che possiamo esprimere tramite il loro effetto su $|\uparrow\;\rangle$ e $|\downarrow\;\rangle$. Dalla $(1)$ si trova
$$\mathbf{S}^{2}|\uparrow\;\rangle=\frac{3}{4}\hbar^{2}|\uparrow\;\rangle, \quad \mathbf{S}^{2}|\downarrow\;\rangle=\frac{3}{4}\hbar^{2}|\downarrow\;\rangle$$
Se scriviamo $\mathbf{S}^{2}$ come una matrice di incognite abbiamo
$$\mathbf{S}^{2}=\pmatrix{c & d \\ e & f}$$
e calcolando esplicitamente le equazioni sopra
$$\pmatrix{c & d \\ e & f}\pmatrix{1 \\ 0}=\frac{3}{4}\hbar^{2}\pmatrix{1 \\ 0}\quad \Rightarrow \quad \pmatrix{c \\ e}=\pmatrix{\frac{3}{4}\hbar^{2} \\ 0}$$
$$\pmatrix{c & d \\ e & f}\pmatrix{0 \\ 1}=\frac{3}{4}\hbar^{2}\pmatrix{0 \\ 1}\quad \Rightarrow \quad \pmatrix{d \\ f}=\pmatrix{0 \\ \frac{3}{4}\hbar^{2}}$$
Allora vale
$$\mathbf{S}^{2}=\frac{3}{4}\hbar^{2}\pmatrix{1 & 0 \\ 0 & 1}$$

Con lo stesso procedimento si trova
$$\mathbf{S}_{z}|\uparrow\;\rangle=\frac{\hbar}{2}|\uparrow\;\rangle, \quad \mathbf{S}_{z}|\downarrow\;\rangle=-\frac{\hbar}{2}|\downarrow\;\rangle$$
e quindi
$$\mathbf{S}_{z}=\frac{\hbar}{2}\pmatrix{1 & 0 \\ 0 & -1}$$
Anche per gli operatori $S_{\pm}$ si ha
$$\mathbf{S}_{+}|\downarrow\;\rangle=\hbar |\uparrow\;\rangle, \quad \mathbf{S}_{-}|\uparrow\;\rangle=\hbar |\downarrow\;\rangle, \quad \mathbf{S}_{+}|\uparrow\;\rangle=\mathbf{S}_{-}|\downarrow\;\rangle=0$$
da cui
$$\mathbf{S}_{+}=\hbar\pmatrix{0 & 1 \\ 0 & 0}, \quad \mathbf{S}_{-}=\hbar\pmatrix{0 & 0 \\ 1 & 0}$$
da cui si possono estrarre
$$\mathbf{S}_{x}=\frac{\hbar}{2}\pmatrix{0 & 1 \\ 1 & 0}, \quad \mathbf{S}_{y}=\frac{\hbar}{2}\pmatrix{0 & -i \\ i & 0}$$

Capita che $\mathbf{S}_{x}$, $\mathbf{S}_{y}$ e $\mathbf{S}_{z}$ hanno tutte un fattore di $\hbar/2$, quindi è possibile esprimere l'operatore di spin nella forma compatta
$$\boxed{\hat{\mathbf{S}}=\frac{\hbar}{2}\hat{\sigma}}$$
dove $\hat{\sigma}$ sono le matrici delle tre componenti, dette [[matrici di Pauli]]. È anche notevole il fatto che $\mathbf{S}_{+}$ e $\mathbf{S}_{-}$ non siano [[Operatore autoaggiunto|autoaggiunte]], il che significa che non sono [[osservabile|osservabili]].

Gli autovettori (tecnicamente autospinori) di $\mathbf{S}_{z}$ sono $|\uparrow\;\rangle$ e $|\downarrow\;\rangle$, con autovalori rispettivamente $\pm \hbar/2$. Se si andasse a misurare $S_{z}$ su una particella nello stato $\chi$, si avrebbe la probabilità $|a|^{2}$ di ottenere $\hbar/2$ e $|b|^{2}$ di ottenere $-\hbar/2$. Dato che sono gli unici casi permessi e la probabilità deve essere normalizzata, vale
$$|a|^{2}+|b|^{2}=1$$
In altre parole, $|a|^{2}$ è la probabilità che la [[funzione d'onda]] della particella collassi in $|\uparrow\;\rangle$, mentre $|b|^{2}$ è la probabilità che collassi in $|\downarrow\;\rangle$.

È possibile trovare gli autovalori e autovettori di $\mathbf{S}_{x}$ e $\mathbf{S}_{y}$ allo stesso modo, e quindi anche le probabilità di collasso associate. Spesso, per evitare confusione tra le componenti, i loro autovettori vengono scritti come $|\uparrow x\rangle$, $|\uparrow y\rangle$ e $|\uparrow z\rangle$. In genere, tuttavia, si parla solo di $|\uparrow z\rangle$ ed è normale tralasciare la $z$ e scrivere solo $|\uparrow\;\rangle$.
### Interazione con il campo magnetico
Una particella carica in rotazione costituisce un dipolo magnetico. Il suo [[momento di dipolo magnetico]] $\vec{\mu}$ è proporzionale al suo momento angolare di spin $\vec{S}$ secondo la relazione
$$\vec{\mu}=\gamma\vec{S}$$
dove $\gamma$ è il cosiddetto **rapporto giromagnetico**. Per l'elettrone, la teoria quantistica relativistica ci dice che è (circa) $\gamma=-e/m$[^3]. Quando un dipolo magnetico è piazzato in un campo magnetico $\vec{B}$, sperimenta un momento di forza $\vec{\mu}\times\vec{B}$ che tende a orientarlo parallelamente alle linee di campo (come una bussola). L'energia dovuta a questo momento di forza è
$$H=-\vec{\mu}\cdot\vec{B}$$
e quindi l'[[Hamiltoniana]] di una particella carica con spin non-zero a riposo in un campo magnetico $\vec{B}$ è
$$H=-\gamma\vec{B}\cdot\vec{S}$$
Queste relazioni sono molto utili non solo per studiare la meccanica di una particella con spin noto, ma anche perché è possibile invertire queste relazioni per studiare lo spin a partire dal campo magnetico, molto più facile da manipolare. L'[[esperimento di Stern-Gerlach]] sfrutta proprio questa interazione.

---

Vale
$$\frac{\hat{S}}{\frac{\hbar}{2}}|\sigma\rangle=\sigma |\sigma\rangle;\quad\sigma=\pm 1$$
Considero
$$\hat{I}=\sum\limits_{x}|x\rangle\langle x|\sum\limits_{\sigma}|\sigma\rangle\langle \sigma|$$
$$\hat{I}|\psi\rangle=\sum\limits_{x,\sigma}(|x\rangle\otimes |\sigma\rangle)(\langle x|\otimes \langle \sigma|)|\psi\rangle$$
Allora
$$\psi(x,\sigma)=(\langle x|\otimes \langle \sigma|)|\psi\rangle$$
che ci dà la generalizzazione della [[Funzione d'onda]] che tiene conto anche dello spin per una singola particella. Nel caso di tante particelle, diventa
$$\psi(x_{1},\sigma_{1};x_{2},\sigma_{2};\ldots;x_{N},\sigma_{N})=\langle \bar{r}_{i},\sigma_{i}|\equiv x_{i}$$
Si hanno casi diversi in base alla particella che si considera. Per i bosoni si ha
$$\psi(x_{1},x_{2},\ldots,x_{i},\ldots,x_{j},\ldots,x_{N})=\psi(x_{1},x_{2},\ldots,x_{j},x_{i},\ldots,x_{N})$$
Nel caso di fermioni si ha
$$\psi(x_{1},x_{2},\ldots,x_{i},\ldots,x_{j},\ldots,x_{N})=-\psi(x_{1},x_{2},\ldots,x_{j},x_{i},\ldots,x_{N})$$
dove c'è un segno meno rispetto a quella dei bosoni.

[^1]: Per esempio, lo spin della Terra può essere pensato come la somma di tutti i momenti orbitali di ciascun pezzetto di roccia, metallo, terra, albero, ecc. che compone il pianeta.
[^2]: Se lo fosse, $|sm_{s}\rangle$ rappresenterebbe una funzione determinata dai numeri $s$ e $m_{s}$. Per esempio, le [[armoniche sferiche]] $Y_{l}^{m}$ potrebbero essere scritte come $|lm\rangle$.
[^3]: Per essere più precisi, il rapporto giromagnetico può essere espresso in funzione del [[magnetone di Bohr]] $\mu_{B}=e\hbar/2mc$, scalato per un fattore detto *fattore g* pari a $g=2.0023$. Così facendo, il momento di dipolo magnetico è $\gamma=-g\mu_{B}$. Se si approssima $g\simeq2$ e si esprime $\mu_{B}$ in [[unità naturali]] si ottiene $\gamma=-e/m$.