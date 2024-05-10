Classicamente, il momento angolare è dato dalla formula vettoriale
$$\vec{L}=\vec{r}\times\vec{p}$$
che suddiviso nelle sue componenti dà
$$L_{x}=yp_{z}-zp_{y}, \quad L_{y}=zp_{x}-xp_{z}, \quad L_{z}=xp_{y}-yp_{x}$$
Quantizzando queste quantità con l'[[operatore]] quantità di moto si trova
$$\hat{L}_{x}=\frac{\hbar y}{i}\frac{\partial }{\partial z}- \frac{\hbar z}{i}\frac{\partial }{\partial y}, \quad \hat{L}_{y}=\frac{\hbar z}{i}\frac{\partial }{\partial x}- \frac{\hbar x}{i}\frac{\partial }{\partial z}, \quad \hat{L}_{z}=\frac{\hbar x}{i}\frac{\partial }{\partial y}- \frac{\hbar y}{i}\frac{\partial }{\partial x}$$
### Commutatività
Per trovare gli [[Equazione agli autovalori|autovalori]] di questi operatori, anzitutto calcoliamo il loro [[commutatore]]:
$$[L_{x},L_{y}]=[yp_{z}-zp_{y}, zp_{x}-xp_{z}]=[yp_{z},zp_{x}]-[yp_{z},xp_{z}]-[zp_{y},zp_{x}]+[zp_{y},xp_{z}]=\ldots$$
Gli unici commutatori che non commutano sono $x$ con $p_{x}$, $y$ con $p_{y}$ e $z$ con $p_{z}$, quindi
$$\ldots=[yp_{z},zp_{x}]-[zp_{y},xp_{z}]=yp_{x}[p_{z},z]+xp_{y}[z,p_{z}]=i\hbar(xp_{yu}-yp_{x})=i\hbar L_{z}$$
Quindi il commutatore di $L_{x}$ e $L_{y}$ dipende da $L_{z}$. Invero, per ottenere tutti i commutatori è sufficiente compiere una permutazione ciclica nell'indice delle variabili:
$$[L_{x},L_{y}]=i\hbar L_{z}, \quad [L_{y},L_{z}]=i\hbar L_{x}, \quad [L_{z},L_{x}]=i\hbar L_{y}$$
Ciò significa le coppie di momenti angolari sono [[Disuguaglianza di Heisenberg|osservabili incompatibili]]. Secondo il principio di indeterminazione generalizzato si ha
$$\sigma_{L_{x}}^{2}\sigma_{L_{y}}^{2}\geq \frac{\hbar^{2}}{4}\left\langle L_{z} \right\rangle^{2} \quad\Rightarrow\quad \sigma_{L_{x}}\sigma_{L_{y}}\geq \frac{\hbar}{2}|\left\langle L_{z} \right\rangle|$$

Se però prendiamo il quadrato del momento angolare *totale*
$$L^{2}\equiv L_{x}^{2}+L_{y}^{2}+L_{z}^{2}$$
si trova che commuta con tutte le componenti
$$\begin{align}
[L^{2},L_{x}]&=[L^{2}_{x},L_{x}]+[L^{2}_{y},L_{x}]+[L^{2}_{z},L_{x}] \\
&=L_{y}[L_{y},L_{x}]+[L_{y},L_{x}]L_{y}+L_{z}[L_{z},L_{x}]+[L_{z},L_{x}]L_{z} \\
&=L_{y}(-i\hbar L_{z}) + (-i\hbar L_{z})L_{y} + (-i\hbar L_{z})L_{y} + (i\hbar L_{y})L_{z} \\
&=0
\end{align}$$
(per le altre componenti basta compiere una permutazione ciclica come sopra). In una forma più compatta, si ha
$$[L^{2},\vec{L}]=0$$
Ciò significa che è possibile trovare [[Stato stazionario|autostati]] simultanei di $L^{2}$ e (per esempio) $L_{z}$.
### Autovalori
Per trovare gli autovalori, usiamo un approccio simile a quello dell'[[oscillatore armonico quantistico]], usando degli [[operatori di creazione e distruzione]]. Definiamo
$$L_{\pm}\equiv L_{x}\pm iL_{y}$$
Il commutatore con $L_{z}$ è
$$[L_{z},L_{\pm}]=[L_{z},L_{x}]\pm i[L_{z},L_{y}]=i\hbar L_{y}\pm i(-i\hbar L_{x})=\pm\hbar(L_{x}\pm iL_{y})=\pm\hbar L_{\pm}$$
e anche
$$[L^{2},L_{\pm}]=0$$
Voglio dimostrare che se $f$ è un'autofunzione di $L^{2}$ e $L_{z}$, lo è anche $L_{\pm}f$. Dalla commutatività qui sopra
$$L^{2}(L_{\pm}f)=L_{\pm}(L^{2}f)=L_{\pm}(\lambda f)=\lambda(L_{\pm}f)$$
che è un'equazione agli autovalori con autofunzione appunto $L_{\pm}f$. Controlliamo anche $L_{z}$ con la sua commutatività:
$$L_{z}(L_{\pm}f)=[L_{z},L_{\pm}]f+L_{\pm}L_{z}f=\pm\hbar L_{\pm}f+L_{\pm}(\mu f)=(\mu\pm\hbar)(L_{\pm}f)$$
che è un'altra equazione agli autovalori, ma con un nuovo autovalore $\mu\pm\hbar$. Chiamiamo $L_{+}$ l'operatore di creazione (o di salita) perché *aumenta* l'autovalore di $\hbar$, mentre $L_{-}$ l'operatore di distruzione (o di discesa) perché lo *diminuisce* di $\hbar$. Questi operatori ci permettono di costruire una "scaletta" di autovalori a partire da qualunque valore $\lambda$, con passi di $\hbar$.

Questa scaletta deve avere un termine, dato che il momento angolare totale è finito e quindi nessuna sua componente può essere più grande di essa. Formalmente vale  $\left\langle L^{2} \right\rangle=\left\langle L_{x}^{2} \right\rangle+\left\langle L_{y}^{2} \right\rangle+\left\langle L_{z}^{2} \right\rangle$, ma $\left\langle L_{x}^{2} \right\rangle=\langle f|L_{x}^{2}f\rangle=\langle L_{x}f|L_{x}f\rangle\geq0$ (lo stesso per $L_{y}$), dunque $\lambda=\left\langle L_{x}^{2} \right\rangle+\left\langle L_{y}^{2} \right\rangle+\mu^{2}\geq\mu^{2}$.

In cima alla scaletta, a $f_{top}$, deve valere
$$L_{+}f_{top}=0$$
Chiamiamo $\hbar l$ l'autovalore in $f_{top}$. Allora
$$L_{z}f_{top}=\hbar lf_{top} \quad\Rightarrow\quad L^{2}f_{top}=\lambda f_{top}$$
Sappiamo che
$$L_{\pm}L_{\mp}=(L_{x}\pm iL_{y})(L_{x}\mp iL_{y})=L^{2}_{x}+L^{2}_{y}\mp i(L_{x}L_{y}-L_{y}L_{x})=L^{2}-L_{z}^{2}\mp i(i\hbar l)$$
e girando la formula
$$L^{2}=L_{\pm}L_{\mp}+L^{2}_{z}\mp\hbar L_{z}$$
Sostituendo nell'equazione agli autovalori di $L^{2}$ si trova
$$L^{2}f_{top}=(L_{-}L_{+}+L^{2}_{z}+\hbar L_{z})f_{top}=(0+\hbar^{2}l^{2}+\hbar^{2}l)f_{t}=\hbar^{2}l(l+1)f_{top}$$
quindi
$$\lambda=\hbar^{2}l(l+1)$$
Quindi abbiamo un'espressione per l'autovalore di $L^{2}$ in funzione del massimo autovalore di $L_{z}$.

Per la stessa ragione di sopra esiste uno "scalino di fondo" $f_{bottom}$ tale che
$$L_{-}f_{bottom}=0$$
Se chiamo $\hbar\bar{l}$ l'autovalore di $f_{bottom}$, usando lo stesso procedimento trovo
$$\lambda=\hbar^{2}\bar{l}(\bar{l}-1)$$
quindi eguagliando i due risultati ho
$$l(l+1)=\bar{l}(\bar{l}-1)$$
Le uniche due soluzioni sono $\bar{l}=l+1$ e $\bar{l}=-l$. La prima però non ha alcun senso, perché vorrebbe dire che lo scalino di fondo è più alto dello scalino di cima, quindi per forza deve essere $\bar{l}=-l$. Evidentemente gli autovalori di $L_{z}$ hanno la forma $m\hbar$, dove $m$ è un valore che va da $-l$ a $l$ in $N$ passi interi. In particolare, vale $l=-l+N$, dunque $l=N/2$. $l$ deve perciò essere un intero o un mezzo intero. Usando questi risultati nelle equazioni agli autovalori abbiamo
$$\boxed{L^{2}f_{lm}=\hbar^{2}l(l+1)f_{lm}, \quad L_{z}f_{lm}=\hbar mf_{lm}}$$
con
$$l=0,\;1/2,\;1,\;3/2,\;2,\ldots\quad; \quad m=-l,-l+1,\ldots,0,\ldots,l-1,l$$

È possibile mostrare graficamente i valori accettabili momento angolare sull'asse $z$ in questo modo.

![[Stati di momento angolare.png]]
*Da Introduction to Quantum Mechanics di Griffiths, p. 167*

I vettori sono (o meglio, dovrebbero essere) $\vec{L}$, tutti di lunghezza $\sqrt{l(l+1)}$ (in unità di $\hbar$). Allora è fisicamente impossibile che il momento angolare sia allineato proprio sull'asse $z$ e la spiegazione è, come al solito, il [[Disuguaglianza di Heisenberg|principio di indeterminazione]]. Per far sì che $L_{z}$ sia ben definito, allora dobbiamo accettare che $L_{x}$ e $L_{y}$ saranno completamente indeterminati dato che le tre componenti *non commutano*. Infatti, non è solo impossibile che il momento angolare sia su un certo asse, ma il *vettore stesso* del momento angolare non è definibile dato che fare ciò richiede tutte e tre le componenti, che *non possono* essere definite simultaneamente. Di fatto, i vettori mostrati nell'immagine sopra sono fuorvianti, dato che stiamo definendo $L_{z}$ e quindi $L_{x}$ e $L_{y}$ non sono definibili. Una rappresentazione più corretta sarebbe "spalmare" i vettori su tutto la linea latitudinale a modo che sia chiara l'indeterminatezza.
### Autofunzioni
Ora vogliamo sapere quali sono le autofunzioni degli operatori. Conviene scrivere gli operatori in coordinate sferiche. Dato che $\hat{\vec{L}}=(\hbar/i)(\vec{r}\times\nabla)$, possiamo usare l'operatore nabla in forma sferica
$$\nabla=\hat{r}\frac{\partial }{\partial r}+\hat{\theta} \frac{1}{r}\frac{\partial }{\partial \theta}+\hat{\phi} \frac{1}{r\sin\theta}\frac{\partial }{\partial \phi}$$
e il fatto che $\vec{r}=r\hat{r}$ per scrivere (omettendo il cappuccio su $\vec{L}$ per semplicità)
$$\vec{L}=\frac{\hbar}{i}\left[r(\hat{r}\times\hat{r})\frac{\partial }{\partial r}+\left(\hat{r}\times\hat{\theta}\right)\frac{\partial }{\partial \theta}+\left(\hat{r}\times\hat{\phi}\right) \frac{1}{\sin\theta}\frac{\partial }{\partial \phi}\right]$$
Sappiamo che $\hat{r}\times\hat{r}=0$, $\hat{r}\times\hat{\theta}=\hat{\phi}$ e $\hat{r}\times\hat{\phi}=-\hat{\theta}$, quindi
$$\vec{L}=\frac{\hbar}{i}\left(\hat{\phi}\frac{\partial }{\partial \theta}-\hat{\theta} \frac{1}{\sin\theta}\frac{\partial }{\partial \phi}\right)$$
Possiamo convertire i versori alle loro equivalenti cartesiane (a modo di trovare le componenti $x$, $y$ e $z$ in variabili sferiche $r$, $\theta$ e $\phi$):
$$\hat{\theta}=\cos\theta\cos\phi\;\hat{i}+\cos\theta\sin\phi\;\hat{j}-\sin\theta\;\hat{k}$$
$$\hat{\phi}=-\sin\phi\;\hat{i}+\cos\theta\;\hat{j}$$
Dunque
$$\vec{L}=\frac{\hbar}{i}\left[(-\sin\theta\;\hat{i}+\cos\phi\;\hat{j})\frac{\partial }{\partial \theta} - \cos\theta\cos\phi\;\hat{i}+\cos\theta\sin\phi\;\hat{j}-\sin\theta\;\hat{k} \frac{1}{\sin\theta}\frac{\partial }{\partial \phi}\right]$$
Estraendo le componenti si ha
$$\hat{L}_{x}=\frac{\hbar}{i}\left(-\sin\phi \frac{\partial }{\partial \theta}-\sin\theta\cot\theta \frac{\partial }{\partial \phi}\right)$$
$$\hat{L}_{y}=\frac{\hbar}{i}\left(\cos\phi \frac{\partial }{\partial \theta}-\sin\phi\cot\theta \frac{\partial }{\partial \phi}\right)$$
$$\boxed{\hat{L}_{z}=\frac{\hbar}{i}\frac{\partial }{\partial \phi}}$$
Gli operatori di creazione e distruzione possono essere espressi come
$$L_{\pm}=\pm\hbar e^{\pm i\phi}\left(\frac{\partial }{\partial \theta}\pm i\cot\theta \frac{\partial }{\partial \phi} \right)$$
usando $\cos\phi\pm i\sin\phi=e^{\pm i\phi}$. Allora trovando $L_{+}L_{-}$ abbiamo
$$\boxed{\hat{L}^{2}=-\hbar^{2}\left[\frac{1}{\sin\theta} \frac{\partial }{\partial \theta}\left(\sin\theta \frac{\partial }{\partial \theta}\right)+ \frac{1}{\sin^{2}\theta}\frac{\partial ^{2}}{\partial \phi^{2}}\right]}$$
Ora che sappiamo la forma di $L_{z}$ e $L^{2}$ e i loro autovalori possiamo risolvere le loro equazioni agli autovalori.

Per $L^{2}$ si trova
$$L^{2}f_{lm}=-\hbar^{2}\left[\frac{1}{\sin\theta} \frac{\partial }{\partial \theta}\left(\sin\theta \frac{\partial }{\partial \theta}\right)+ \frac{1}{\sin^{2}\theta}\frac{\partial ^{2}}{\partial \phi^{2}}\right]f_{lm}=\hbar^{2}l(l+1)f_{lm}$$
Ma se eliminiamo le $\hbar^{2}$ e moltiplichiamo tutto per $\sin^{2}\theta$, questo non è altro che l'equazione della [[Equazione di Schrödinger#Parte angolare|parte angolare dell'equazione di Schrödinger]].

Per $L_{z}$ si trova
$$L_{z}f_{lm}=\frac{\hbar}{i}\frac{\partial }{\partial \phi}f_{lm}=\hbar m f_{lm}$$
ma ancora, questa è l'equazione azimutale in $\Phi$ della parte angolare cui sopra.

In altre parole, queste equazioni sono già state risolte nel caso generale dell'equazione di Schrödinger tempo-indipendente in coordinate sferiche. Ciò significa che le autofunzioni di $\hat{L}^{2}$ e $\hat{L}_{z}$ sono le [[armoniche sferiche]]. Infatti, risolvendo quel caso generale non si è fatto altro che creare autofunzioni simultanee per gli operatori $\hat{H}$, $\hat{L}^{2}$ e $\hat{L}_{z}$, con equazioni
$$\hat{H}\psi=E\psi , \quad \hat{L}^{2}\psi=\hbar^{2}l(l+1)\psi, \quad \hat{L}_{z}\psi=\hbar m\psi$$

È anche possibile usare $\hat{L}^{2}$ per esprimere l'equazione di Schrödinger in coordinate sferiche in un modo più conciso:
$$\frac{1}{2mr}\left[-\hbar^{2}\frac{\partial }{\partial r}\left(r^{2}\frac{\partial}{\partial r}\right)+ \hat{L}^{2}\right]\psi + V\psi=E\psi$$

C'è una differenza importante tra queste due derivazioni tuttavia: sebbene la soluzione dell'equazione di Schrödinger prevedeva solo $l$ e $m$ *interi*, questa soluzione permette anche *mezzi interi*.