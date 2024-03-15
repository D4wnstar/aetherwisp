Una **funzione d'onda** $\Psi(x,t)$ (anche $\psi(x,t)$) è una funzione che descrive lo stato di una [[particella]] quantistica. È la soluzione dell'[[equazione di Schrödinger]]. Esistono diverse interpretazioni fisiche della funzione d'onda.
### Interpretazione di Born
Un modo per spiegare a livello fisico la funzione d'onda è l'**interpretazione statistica di Born**. Questa afferma che la [[norma]] della funzione d'onda ci dà la *probabilità* che la particella si trovi in un determinato punto $x$ allo spazio $t$. In simboli
$$\int_{a}^{b}|\Psi(x,t)|^{2}dx=\text{probabilità di trovare la particella tra }a\text{ e }b\text{ al tempo }t$$
Ciò significa che, anche conoscendo la funzione d'onda di una particella, quello che sappiamo del suo moto è al più la *probabilità* che si trovi in un certo punto (o insieme di punti) ad un certo tempo. Questo fatto si chiama [[indeterminatezza quantistica]].
#### Normalizzazione
Se $\Psi$ è una distribuzione di probabilità, allora deve essere normalizzata
$$\int_{-\infty}^{+\infty}|\Psi(x,t)|^{2}dx=1\tag{1}$$
ma $\Psi$ è ottenuta dall'equazione di Schrödinger, che di per sé non dà alcuna garanzia che $\Psi$ sia normalizzata. Per le proprietà delle equazioni differenziali, sappiamo però che se $\Psi(x,t)$ è soluzione, lo sono anche tutte le $A\Psi(x,t)=\tilde{\Psi}(x,t)$, con $A$ costante complessa. Allora è quasi sempre possibile trovare una $A$ tale per cui $(1)$ è soddisfatta.

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
### Formalizzazione matematica
Matematicamente, è un elemento di uno [[spazio di Hilbert]] che è il coefficiente di sviluppo degli autostati di posizione di un oggetto. In altre parole, è la *rappresentazione* dell'evoluzione (della posizione) di quell'oggetto in una base. In una dimensione ha la forma
$$\psi(x)=\langle x|\psi\rangle$$
$$\sum\limits_{x}|x\rangle\langle x|\psi\rangle=\sum\limits_{x}\psi(x)|x\rangle$$
In più dimensioni ha la forma
$$\psi(\bar{r})=\langle \bar{r}|\psi\rangle$$
$$\sum\limits_{\bar{r}}|\bar{r}\rangle\langle \bar{r}|\psi\rangle=\sum\limits_{\bar{r}}\psi(\bar{r})|\bar{r}\rangle$$
