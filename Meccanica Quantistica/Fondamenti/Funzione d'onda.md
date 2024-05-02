Una **funzione d'onda** $\Psi(x,t)$ (anche $\psi(x,t)$) è una funzione che descrive lo stato di una [[particella]] quantistica. È la soluzione dell'[[equazione di Schrödinger]]. Esistono diverse interpretazioni fisiche della funzione d'onda.
### Interpretazione di Born
Un modo per spiegare a livello fisico la funzione d'onda è l'**interpretazione statistica di Born**. Questa afferma che la [[Norma]] della funzione d'onda ci dà la *probabilità* che la particella si trovi in un determinato punto $x$ allo spazio $t$. In simboli
$$\int_{a}^{b}|\Psi(x,t)|^{2}dx=\text{probabilità di trovare la particella tra }a\text{ e }b\text{ al tempo }t$$
Ciò significa che, anche conoscendo la funzione d'onda di una particella, quello che sappiamo del suo moto è al più la *probabilità* che si trovi in un certo punto (o insieme di punti) ad un certo tempo. Questo fatto si chiama [[indeterminatezza quantistica]].
#### Normalizzazione
Se $\Psi$ è una distribuzione di probabilità, allora deve essere normalizzata
$$\boxed{\int_{-\infty}^{+\infty}|\Psi(x,t)|^{2}dx= \langle \Psi|\Psi\rangle =1\tag{1}}$$
(dove il secondo termine usa la [[notazione braket]]) ma $\Psi$ è ottenuta dall'equazione di Schrödinger, che di per sé non dà alcuna garanzia che $\Psi$ sia normalizzata. Per le proprietà delle equazioni differenziali, sappiamo però che se $\Psi(x,t)$ è soluzione, lo sono anche tutte le $A\Psi(x,t)=\tilde{\Psi}(x,t)$, con $A$ costante complessa. Allora è quasi sempre possibile trovare una $A$ tale per cui $(1)$ è soddisfatta.

È possibile che per alcune soluzioni dell'equazione di Schrödinger, l'integrale $(1)$ sia infinito o zero. In questi casi, non esiste nessuna $A$ capace di normalizzare $\Psi$. Queste soluzioni *non-normalizzabili* non hanno significato fisico e vanno scartate. Vista in un altro modo, tutte le $\Psi$ rappresentanti soluzioni fisiche sono funzioni [[Spazi Lp#Spazio $L {2}$|L^2]].

L'equazione di Schrödinger ha la cruciale proprietà di conservare la normalizzazione nel tempo. Ciò significa che se si trova una costante di normalizzazione $A$ al tempo $t_{0}$, quella costante varrà per qualunque $t\in\mathbb{R}$. Questa proprietà garantisce che la costante $A$ sia davvero una costante - se non lo fosse, $A$ diventerebbe una funzione in $t$ e $A(t)\Psi(x,t)$ non sarebbe più una soluzione dell'equazione di Schrödinger, dunque invalidando tutta l'interpretazione di Born.
##### Dimostrazione
Prendiamo
$$\frac{d}{dt}\int_{-\infty}^{+\infty}|\Psi(x,t)|^{2}dx=\int_{-\infty}^{+\infty}\frac{\partial }{\partial t}|\Psi(x,t)|^{2}dx\tag{2}$$
La derivata passa da una totale a una parziale perché l'integrale è funzione solo di $t$, ma all'interno $\Psi$ è funzione sia di $t$ che di $x$. Vale
$$\frac{\partial }{\partial t}|\Psi|^{2}=\frac{\partial }{\partial t}(\Psi^{*}\Psi)=\Psi^{*}\frac{\partial \Psi}{\partial t}+\frac{\partial \Psi^{*}}{\partial t}\Psi$$
Prendiamo l'equazione di Schrödinger
$$\frac{\partial \Psi}{\partial t}=\frac{i\hbar}{2m}\frac{\partial ^{2}\Psi}{\partial x^{2}}- \frac{i}{\hbar}V\Psi$$
di cui possiamo prendere il complesso coniugato
$$\frac{\partial \Psi^{*}}{\partial t}=- \frac{i\hbar}{2m}\frac{\partial ^{2}\Psi^{*}}{\partial x^{2}}- \frac{i}{\hbar}V\Psi^{*}$$
Dunque
$$\frac{\partial }{\partial t}|\Psi|^{2}=\frac{i\hbar}{2m}\left(\Psi^{*}\frac{\partial ^{2}\Psi}{\partial x^{2}}-\frac{\partial ^{2}\Psi}{\partial x^{2}}\Psi\right)=\frac{\partial }{\partial x}\left[\frac{i\hbar}{2m}\left(\Psi^{*}\frac{\partial \Psi}{\partial x}-\frac{\partial \Psi^{*}}{\partial x}\Psi\right)\right]$$
che possiamo usare per calcolare l'integrale $(2)$
$$\frac{d}{dt}\int_{-\infty}^{+\infty}|\Psi(x,t)|^{2}dx=\frac{i\hbar}{2m}\left.\left(\psi^{*}\frac{\partial \Psi}{\partial x}-\frac{\partial \Psi^{*}}{\partial x}\Psi\right)\right|_{-\infty}^{+\infty}=\ldots$$
usando che $\Psi\in L^{2}$ deve valere $\Psi(\pm\infty) \rightarrow 0$ e allora l'integrale $(2)$ è identicamente nullo. Ciò significa che l'integrale è costante nel tempo e quindi se è normalizzato da $A$ in $t_{0}$, lo è per qualunque altro $t$.
### Collasso
Il **collasso della funzione d'onda** è un fenomeno quantistico osservato dopo la misura di una particella. Immediatamente dopo aver compiuto una misura, la funzione d'onda della particella *collassa*, cambiando radicalmente forma e diventando un singolo picco attorno al valore misurato. Ciò implica che, compiendo misure rapide una dopo l'altra, si otterrà sempre lo stesso risultato (o comunque uno quasi uguale).

![[Grafico Collasso funzione d'onda|100%|center]]
### Valori di aspettazione
Prendiamo una particella in uno stato $\Psi$. Allora, possiamo determinare il valore di aspettazione della posizione $x$ come
$$\left\langle x \right\rangle=\int_{-\infty}^{+\infty}x|\Psi(x,t)|^{2}dx=\langle \Psi|x |\Psi\rangle$$
Cos'è $\left\langle x \right\rangle$? A causa del collasso dopo un'osservazione, misure ripetute daranno sempre lo stesso risultato. Dunque, $\left\langle x \right\rangle$ non può il risultato che ci si aspetta dalla media di molte misure. Invece, $\left\langle x \right\rangle$ è la media di risultati ottenuti da misure su particelle *nello stato* $\Psi$. In altre parole, bisogna misurare particelle che sono nello stato indeterminato, *prima* del collasso. Ciò significa o trovare un modo per "resettare" una particella e farla tornare indeterminata dopo il collasso per misurarla più volte, o misurare un intero ensemble di particelle, tutte nello stesso stato $\Psi$. Allora, il *valore di aspettazione è la media di misure ripetute su un ensemble di sistemi preparati allo stesso modo*.

La funzione d'onda varia nel tempo. Allora, anche il valore di aspettazione dipende da $t$. Possiamo trovarne la derivata temporale
$$\frac{d\left\langle x \right\rangle}{dt}=\int_{-\infty}^{+\infty}x \frac{\partial }{\partial t}|\Psi(x,t)|^{2}dx=\frac{i\hbar}{2m}\int_{-\infty}^{+\infty}x\frac{\partial }{\partial x}\left(\Psi^{*}\frac{\partial \Psi}{\partial x}-\frac{\partial \Psi^{*}}{\partial x}\Psi\right)dx=\ldots$$
usando un'[[Integrazione per parti]] e usando che $\lim\limits_{x \rightarrow \pm\infty}\Psi(x,t)=0$
$$\ldots=-\frac{i\hbar}{2m}\int_{-\infty}^{+\infty}\left(\Psi^{*}\frac{\partial \Psi}{\partial x}-\frac{\partial \Psi^{*}}{\partial x}\Psi\right)dx=\ldots$$
e ancora un'integrazione per parti, su $\partial\Psi^{*}/\partial x$
$$\ldots=- \frac{i\hbar}{m}\int_{-\infty}^{+\infty}\Psi^{*}\frac{\partial \Psi}{\partial x}dx$$
Intuitivamente, questo ci dà qualche sorta di velocità. D'altronde, la derivata di una posizione è proprio la velocità. Tuttavia, il concetto stesso di velocità, così come la posizione non è ben definito. Si può costruire tuttavia la distribuzione di probabilità delle velocità. Si dimostra poi che quanto appena trovato è il valore di aspettazione di questa distribuzione:
$$\left\langle v \right\rangle=\frac{d\left\langle x \right\rangle}{dt}=- \frac{i\hbar}{m}\int_{-\infty}^{+\infty}\Psi^{*}\frac{\partial \Psi}{\partial x}dx$$
Di norma si lavora con il momento, o quantità di moto, $p=mv$ della particella:
$$\left\langle p \right\rangle=m \frac{d\left\langle x \right\rangle}{dt}=- i\hbar\int_{-\infty}^{+\infty}\Psi^{*}\frac{\partial \Psi}{\partial x}dx$$
$\left\langle x \right\rangle$ e $\left\langle p \right\rangle$ sono solitamente scritte in questo modo
$$\boxed{\begin{align}
\left\langle x \right\rangle &=\int_{-\infty}^{+\infty}\Psi^{*}(x)\Psi dx &= \int_{-\infty}^{+\infty}\Psi^{*}\;\hat{q}\;\Psi dx & = \langle \Psi|\hat{q}|\Psi\rangle \\
\left\langle p \right\rangle &=\int_{-\infty}^{+\infty}\Psi^{*}\left(\frac{\hbar}{i}\frac{\partial }{\partial x}\right)\Psi dx &= \int_{-\infty}^{+\infty}\Psi^{*}\;\hat{p}\;\Psi dx &= \langle \Psi|\hat{p}|\Psi\rangle
\end{align}}$$
dove $\hat{q}\equiv x$ e $\hat{p}\equiv(\hbar/i)\partial/\partial x$ sono [[Operatore|operatori]] associati alle [[Osservabile|osservabili]] posizione e quantità di moto e possiamo calcolarne la media ponendoli in mezzo[^1] a $\Psi^{*}$ e $\Psi$ e poi integrando il risultato su tutto $\mathbb{R}$.

Qualunque [[variabile dinamica]] classica $Q$ è esprimibile in funzione di $q$ e $p$. Allora, per calcolare il valore di aspettazione (nello stato $\Psi$) di $Q$, basta sostituire $p$ con $(\hbar/i)\partial/\partial x$ e integrare come sopra. La formula generale è
$$\boxed{\left\langle Q(q,p) \right\rangle=\int_{-\infty}^{+\infty}\Psi^{*}Q\left(q, \frac{\hbar}{i}\frac{\partial }{\partial x}\right)\Psi dx=\langle \Psi|\hat{Q} |\Psi\rangle}$$
### Caso tridimensionale
La funzione d'onda e le sue proprietà sono facilmente estese a tre dimensioni. Per una funzione d'onda in tre dimensioni $\Psi(\vec{r},t)$ valgono le stesse proprietà del caso unidimensionale. La normalizzazione è su un volume
$$\int |\Psi(\vec{r},t)|^{2}d^{3}\vec{r}=1$$
Se il potenziale è indipendente dal tempo, può essere comunque espressa in funzione degli stati stazionari e l'[[evolutore]]
$$\Psi_{n}(\vec{r},t)=\psi_{n}(\vec{r})\hat{U}_{t}=\psi_{n}(\vec{r})e^{-iE_{n}t/\hbar}$$
dove gli stati stazionari $\psi_{n}$ sono la soluzione della forma indipendente dal tempo dell'equazione di Schrödinger e la soluzione generale è sempre
$$\Psi_{n}(\vec{r},t)=\sum\limits_{n=1}^{\infty}c_{n}\psi_{n}(\vec{r})e^{-iE_{n}t/\hbar}$$
Ovviamente se gli stati sono continui e non discreti, la somma diventa un integrale.
### Formalizzazione matematica
Matematicamente, è un elemento di uno [[Spazio di Hilbert]] che è il coefficiente di sviluppo degli autostati di posizione di un oggetto. In altre parole, è la *rappresentazione* dell'evoluzione (della posizione) di quell'oggetto in una base. La funzione d'onda indipendente dal tempo in una dimensione ha la forma
$$\psi(x)=\langle x|\psi\rangle$$
$$\hat{P}_{x}|\psi\rangle=\sum\limits_{x}|x\rangle\langle x|\psi\rangle=\sum\limits_{x}\psi(x)|x\rangle$$
usando il [[Proiettore]]. In più dimensioni
$$\psi(\bar{r})=\langle \bar{r}|\psi\rangle$$
$$\hat{P}_{\vec{r}}|\psi\rangle=\sum\limits_{\bar{r}}|\bar{r}\rangle\langle \bar{r}|\psi\rangle=\sum\limits_{\bar{r}}\psi(\bar{r})|\bar{r}\rangle$$


[^1]: L'esatta operazione da compiere è un [[Prodotto scalare]] tra $\Psi$ e l'operatore.