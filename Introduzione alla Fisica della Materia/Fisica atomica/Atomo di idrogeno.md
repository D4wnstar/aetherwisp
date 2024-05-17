L'**atomo di idrogeno** consiste in un [[protone]] sostanzialmente fermo di carica $e$ legato dall'[[Interazioni fondamentali|interazione elettromagnetica]] con un [[elettrone]] di carica $-e$. È l'[[atomo]] dalla struttura più semplice e l'unico ad essere risolvibile analiticamente (assieme a tutti gli atomi *idrogenoidi*, ossia con un solo elettrone, che si riconducono a quello di idrogeno).
### Formulazione di Schrödinger
Consideriamo l'[[Hamiltoniana]]
$$H=- \frac{\hbar^{2}}{2M}\nabla^{2}_{R}- \frac{\hbar^{2}}{2m}\nabla^{2}_{r_{e}}- \frac{Ze^{2}}{4\pi\epsilon_{0}|R-r_{e}|}$$
dove $M$ è la massa del nucleo, $m$ la masse dell'[[elettrone]], $Z$ è il numero atomico e $|R-r_{e}|$ la distanza orbitale dell'elettrone. I tre termini rappresentano, in ordine, l'energia cinetica dei nuclei, quella degli elettroni e l'energia [[potenziale]].

![[Schema modello idrogeno|center]]

Si nota che l'Hamiltoniana non dipende esplicitamente dallo [[spin]] dell'elettrone. La [[Funzione d'onda]] è esprimibile come prodotto della componente spaziale e di spin
$$\psi(q)=\chi_{s,m_{s}}\psi(r)$$
dove $\chi_{ms}$ sono gli autostati dell'[[operatore]] $S_{z}$ ed $S^{2}$ con autovalori $s=1/2$ e $m_{s}=\pm1/2$. Cerchiamo questi autostati.

Prendiamo il momento angolare orbitale $\vec{L}=\vec{r}\times\vec{p} =-i\hbar(\vec{r}\times\nabla)$. Per componenti
$$\begin{cases}
L_{x}=yp_{z}-zp_{y}=-i\hbar\left(y \frac{\partial }{\partial z} -z \frac{\partial }{\partial y}\right) \\
L_{y}=-i\hbar\left(z \frac{\partial }{\partial x} -x \frac{\partial }{\partial z}\right) \\
L_{z}=-i\hbar\left(x \frac{\partial }{\partial y} -y \frac{\partial }{\partial x}\right) \\
\end{cases}$$
Usando il [[commutatore]] si trova
$$\begin{cases}
[L_{x},L_{y}]=i\hbar L_{z} \\
[L_{y},L_{z}]=i\hbar L_{x} \\
[L_{z},L_{x}]=i\hbar L_{y}
\end{cases}$$
e dato che i commutatori non sono nulli, non è possibile costruire autostati simultanei su più momenti angolari, quindi non è possibili misurarli insieme con arbitraria precisione. Tuttavia, è possibile costruire autostati simultanei per $L^{2}=L_{x}^{2}+L_{y}^{2}+L_{z}^{2}$ e $L_{z}$ dato che $[L^{2},L_{z}]=0$. Lo stesso vale per lo spin.

Si ha
$$S^{2}\alpha=\frac{3}{4}\hbar^{2}\alpha\quad;\quad S_{z}\alpha=\frac{\hbar}{2}\alpha$$
$$S^{2}\beta=\frac{3}{4}\hbar^{2}\beta\quad;\quad S_{z}\beta=-\frac{\hbar}{2}\beta$$
Quindi per sovrapposizione degli [[Stato|stati]]
$$\chi=\chi_{+}\alpha+\chi_{-}\beta\quad;\quad|\chi_{+}|^{2}+|\chi_{-}|^{2}=1$$
$$\langle \alpha|\alpha\rangle=1\quad;\quad \langle \beta|\beta\rangle=1\quad; \quad \langle \alpha|\beta\rangle=\langle \beta|\alpha\rangle=0$$
Usando le [[matrici di Pauli]]
$$S^{2}=\frac{3}{4}\hbar^{2}\pmatrix{1 & 0 \\ 0 & 1}$$
$$S_{x}=\frac{\hbar}{2}\pmatrix{0 & 1 \\ 1 & 0}=\frac{\hbar}{2}\sigma_{x}\quad;\quad S_{y}=\frac{\hbar}{2}\pmatrix{0 & -i \\ i & 0}=\frac{\hbar}{2}\sigma_{y}\quad;\quad S_{z}=\frac{\hbar}{2}\pmatrix{1 & 0 \\ 0 & -1}=\frac{\hbar}{2}\sigma_{z}$$
Possiamo scrivere la soluzione dell'[[Equazione di Schrödinger]] in coordinate polari come
$$\left[- \frac{\hbar^{2}}{2\mu} \frac{1}{r^{2}} \frac{\partial }{\partial r}\left(r^{2}\frac{\partial }{\partial r}\right)+ \frac{\vec{L}^{2}}{2\mu r^{2}} - \frac{Ze^{2}}{4\pi\epsilon_{0}r}\right]\Psi(r,\theta,\phi)=E\Psi(r,\theta,\phi)$$
e troviamo le autofunzioni dell'operatore $L$
$$L^{2}Y_{l,m}(\theta,\phi)=l(l+1)\hbar^{2}Y_{l,m}(\theta,\phi)$$
$$L_{z}Y_{l,m}(\theta,\phi)=m\hbar Y_{l,m}(\theta,\phi) \rightarrow L_{z}\phi(\phi)=m\hbar\phi(\phi)$$
con
$$\phi_{m}(\phi)=\frac{1}{\sqrt{2\pi}}e^{im\phi};\quad \phi_{m}(0)=\phi_{m}(2\pi)$$
dove $Y$ sono le *armoniche sferiche*. $l$ è il *numero quantico del momento angolare* e $m$ è il *numero quantico del momento magnetico*.

Le armoniche sferiche descrivono la distribuzione angolare della carica nei vari orbitali. Possono essere rappresentate in un grafico polare eliminando la dipendenza da $\phi$
$$|Y_{l,m}(\theta,\phi)|^{2}=\frac{1}{2\pi}|\theta_{l,m}(\theta)|^{2}$$
Facendo ciò, si ottengono i grafici della distribuzione di probabilità attorno al nucleo. Si può anche rappresentare le armoniche sferiche in forma reale: queste sono usate per mostrare la direzionalità di un legame chimico e sono autostati di $L^{2}$ e $L^{2}_{z}$, ma non $L_{z}$. Altrimenti la direzionalità della distribuzione di carica può essere mostrata mettendo in grafico il valore dell'armonica in forma reale in tutte le direzioni dello spazio.

La forma dell'orbitale è data dalla distorsione della orbitale dovuto ad un'eccitazione lungo una linea nodale. Il numero quantico $l$ determina il numero di linee nodali. Con $l=0$, non ci sono linee nodali e quindi l'orbitale non è perturbato: si tratta di dunque di una sfera. Con $l=1$, si ha una linea nodale, etc..

Il numero quantico $m$ rappresenta invece una rotazione delle linee nodali. Con $m=0$, le linee nodali sono tutte fisse. Con $m=\pm1$, una linea nodale ruota in direzione (anti)oraria. $m$ può aumentare fino a $m=\pm l$, al quale punto tutte le linee nodali ruotano nella stessa direzione.

A livello pratico, un orbitale può essere pensato come un palloncino che viene schiacciato su certe linee nodali. Il palloncino non si ingrandisce o rimpicciolisce, cambia solo forma nello spazio tridimensionale. Se schiacciato ai lati $xy$, si ingrandirà lungo l'asse $z$, formando due lobi.

Le funzioni $R(r)$ e gli autovalori di energia possono essere ricavati risolvendo l'equazione radiale
$$\left[- \frac{\hbar^{2}}{2\mu} \frac{1}{r^{2}} \frac{\partial }{\partial r}\left(r^{2}\frac{\partial }{\partial r}\right)+ \frac{\hbar^{2}l(l+1)}{2\mu r^{2}} - \frac{Ze^{2}}{4\pi\epsilon_{0}r}\right]R(r)=ER(r)$$
Sostituendo $R(r)=X(r)/r$ si ottiene
$$\left[- \frac{\hbar^{2}}{2\mu} \frac{d}{dr^{2}}+ \frac{\hbar^{2}l(l+1)}{2\mu r^{2}} - \frac{Ze^{2}}{4\pi\epsilon_{0}r}\right]u(r)=Eu(r)$$
Il potenziale effettivo è
$$V_{eff}(r)=V(r)+ \frac{l(l+1)\hbar^{2}}{2mr^{2}}=\ldots$$
per atomi idrogenoidi diventa
$$\ldots=- \frac{Ze^{2}}{4\pi\epsilon_{0}r}+ \frac{l(l+1)\hbar^{2}}{2\mu r^{2}}$$
![[Potenziale atomi idrogenoidi|70%|center]]
Allora per trovare gli autovalori $u$ dobbiamo risolvere un'equazione differenziale
$$\frac{d^{2}u_{E,l}}{dr^{2}}+ \frac{2\mu}{\hbar^{2}}[E-V_{eff}(r)]=0$$
Usiamo la sostituzione
$$\begin{cases}
\rho=\left(- \frac{8\mu E}{\hbar^{2}}\right)^{\frac{1}{2}}r \\
\lambda= \frac{Ze^{2}}{4\pi\epsilon_{0}\hbar}\left(- \frac{\mu}{2E}\right)^\frac{1}{2}
\end{cases}$$
da cui otteniamo
$$\left[\frac{d^{2}}{d \rho^{2}} - \frac{l(l+1)}{\rho^{2}} + \frac{\lambda}{\rho} - \frac{1}{4}\right]u_{E,l}(\rho)=0$$
Questa equazione ha soluzioni esponenziali $u_{E,l}(\rho)\propto e^{-\rho/2}$. Per $\rho \rightarrow \infty$, diventa una soluzione del tipo $u_{E,l}(\rho)=e^{-\rho/2}P_{e,l}(\rho)$, dove $P$ è un polinomio. Compiendo una sostituzione magica e incredibile da $u$ a $g$ (???) si trova
$$\left[\rho \frac{d^{2}}{d\rho^{2}}+\left(2l+2-\rho\right) \frac{d}{d\rho} + (\lambda - l - 1)\right]g(\rho)=0$$
le cui soluzioni sono dei [[polinomi di Laguerre]]
$$L_{q}^{p}(\rho)=\frac{d^{p}}{d\rho^{p}}L_{q}(\rho)\quad;\quad L_{q}(\rho)=e^{\rho} \frac{d^{q}}{d\rho^{q}}(\rho^{q}e^{-\rho})$$
Di fatto si giunge alla soluzione
$$R_{n,l}(r)=N_{n,l}e^{-\rho/2}L_{n+l}^{2l+1}(\rho)\text{ con }\rho=\frac{2Zr}{na_{\mu}}\text{ e }n=1,2,\ldots;\;l=0,\ldots,n-1$$
dove $a_{\mu}$ è una correzione del [[raggio di Bohr]].

La funzione d'onda risolta diventa quindi dipendente dai tre numeri quantici $n,l,m$ e ha la forma semplice
$$\Psi(r,\theta,\phi)=R_{n,l}(r)Y_{l,m}(\theta,\phi)$$
Gli autovalori di energia possono essere espressi come
$$E_{n}=-R(\mu) \frac{Z^{2}}{n^{2}}=- \frac{\mu}{m}R_{\infty} \frac{Z^{2}}{n^{2}}$$
dove $R_{\infty}$ è la [[costante di Rydberg]]. Si nota che sono presenti stati discreti infiniti e che si infittiscono per $n \rightarrow \infty$ quando il potenziale Coulombiano tende a zero. Gli stati risultano degeneri in $l$ ed $m$. La degenerazione dei livelli è data da
$$d=\underbrace{2}\limits_{m_{s}}\sum\limits_{l=0}^{n-1}\underbrace{2l+1}\limits_{m}=2n^{2}$$
che racchiude tutti i numeri quantici: abbiamo che $l$ varia da $0$ a $n-1$, per ogni $l$ sono possibili $2l+1$ valori di $m$ e tutto è possibile per entrambi i numeri di [[spin]] $m_{s}=\pm\frac{1}{2}$.
### Trattamento di Griffiths
Anzitutto, determiniamo il [[potenziale]]. Dalla [[legge di Coulomb]] abbiamo il potenziale (in unita SI)
$$V(r)=- \frac{e^{2}}{4\pi\epsilon_{0}} \frac{1}{r}$$
quindi l'equazione radiale da risolvere per trovare la [[Funzione d'onda]] è
$$- \frac{\hbar^{2}}{2m}\frac{d^{2}u}{dr^{2}}+ \left[- \frac{e^{2}}{4\pi\epsilon_{0}} \frac{1}{r}+\frac{\hbar^{2}}{2m} \frac{l(l+1)}{r^{2}} \right]u(r)=Eu(r)\tag{1}$$

Il potenziale Coulombiano ammette sia stati con [[spettro]] continuo con $E>0$ (che rappresentano la [[diffusione di particelle|diffusione]] protone-elettrone), sia con spettro discreto con $E<0$, i cui [[Stato stazionario|stati stazionari]] rappresentano i livelli di energia dell'elettrone legato. A noi interessano questi ultimi.
#### Funzione d'onda radiale
Consideriamo la costante
$$\kappa\equiv \frac{\sqrt{-2mE}}{\hbar} $$
Per gli stati legati abbiamo $E<0$, quindi $\kappa$ è reale. Dividendo la $(1)$ per $E$ troviamo
$$\frac{1}{\kappa^{2}} \frac{d^{2}u}{dr^{2}}=\left[1- \frac{me^{2}}{2\pi\epsilon_{0}\hbar^{2}\kappa} \frac{1}{\kappa r} + \frac{l(l+1)}{(\kappa r)^{2}}\right]u$$
Possiamo compiere le sostituzioni
$$\rho\equiv \kappa r, \quad \rho_{0}\equiv \frac{me^{2}}{2\pi\epsilon_{0}\hbar^{2}\kappa}$$
da cui troviamo
$$\frac{d^{2}u}{d\rho^{2}}=\left[1 - \frac{\rho_{0}}{\rho}+ \frac{l(l+1)}{\rho^{2}}\right]u\tag{2}$$
Esaminiamo il comportamento asintotico[^1]. Per $\rho \rightarrow \infty$, i termini $\rho^{-1}$ e $\rho^{-2}$ tendono a zero, quindi rimane
$$\frac{d^{2}u}{d\rho^{2}}=u$$
la cui soluzione generale è
$$u(\rho)=Ae^{-\rho}+Be^{\rho}$$
Poiché $e^{\rho} \rightarrow \infty$, deve essere $B=0$. Allora
$$u(\rho)\simeq Ae^{-\rho} \quad \text{per }\rho\gg1$$
Per $\rho \rightarrow 0$, domina il termine centrifugale $\rho^{-2}$ (eccetto per $l=0$), quindi si ha
$$\frac{d^{2}u}{dr^{2}}=\frac{l(l+1)}{\rho^{2}}u$$
la cui soluzione generale è
$$u(\rho)=C\rho^{l+1}+D\rho^{-l}$$
Poiché $\rho^{-l} \rightarrow \infty$, deve essere $D=0$. Allora
$$u(\rho)\simeq C\rho^{l+1}\quad \text{per }\rho\ll1$$

Introduciamo la funzione $v(\rho)$ come
$$u(\rho)=\rho^{l+1}e^{-\rho}v(\rho)$$
che sostanzialmente rappresenta il comportamento di $u(\rho)$ al di fuori degli asintoti. Calcoliamone le derivate per risolvere l'equazione radiale esplicitamente:
$$\frac{du}{d\rho}=\rho^{l}e^{-\rho}\left[(l+1-\rho)v+\rho \frac{dv}{d\rho}\right]$$
$$\frac{d^{2}u}{dr^{2}}=\rho^{l}e^{-\rho}\left\{\left[ -2l-2+\rho+ \frac{l(l+1)}{\rho}\right]v + 2(l+1-\rho) \frac{dv}{d\rho} + \rho \frac{d^{2}v}{d\rho^{2}}\right\}$$
Sostituendo nella $(2)$ abbiamo
$$\rho \frac{d^{2}v}{d\rho^{2}}+2(l+1-\rho) \frac{dv}{d\rho}+[\rho_{0}-2(l+1)]v=0\tag{3}$$
Assumiamo che la soluzione $v(\rho)$ possa essere espressa in [[serie di potenze]] in $\rho$:
$$v(\rho)=\sum\limits_{j=0}^{\infty}c_{j}\rho^{j}$$
Quindi il nostro problema ora è cercare i coefficienti $c_{j}$. Differenziando termine per termine si ha
$$\frac{dv}{d\rho}=\sum\limits_{j=0}^{\infty}jc_{j}\rho^{j-1}=\sum\limits_{j=0}^{\infty}(j+1)c_{j+1}\rho^{j}$$
dove nel secondo passaggio l'indice è stato modificato da $j$ a $j+1$. La seconda serie comincia da $j=0$ e non da $-1$ perché il termine $-1$ è nullo a causa di $(j+1)$. Differenziando ancora
$$\frac{d^{2}v}{d\rho^{2}}=\sum\limits_{j=0}^{\infty}j(j+1)c_{j+1}\rho^{j-1}$$
Sostituendo nella $(3)$ abbiamo
$$\sum\limits_{j=0}^{\infty}j(j+1)c_{j+1}\rho^{j}+2(l+1)\sum\limits_{j=0}^{\infty}(j+1)c_{j+1}\rho^{j}-2\sum\limits_{j=0}^{\infty}jc_{j}\rho^{j}+$$
$$+[\rho_{0}-2(l+1)]\sum\limits_{j=0}^{\infty}c_{j}\rho^{j}=0$$
Equivalendo i coefficienti delle serie si ha
$$j(j+1)c_{j}+2(l+1)c_{j+1}+2jc_{j}+[\rho_{0}-2(l+1)]c_{j}=0$$
e invertendo
$$c_{j+1}=\left[\frac{2(j+l+1)-\rho_{0}}{(j+1)(j+2l+2)}\right]c_{j}\tag{4}$$
che è una formula ricorsiva per i coefficienti.

Per $j\gg1$ possiamo approssimare i coefficienti
$$c_{j+1}\simeq \frac{2j}{j(j+1)}c_{j}=\frac{2}{j+1}c_{j}$$
(il $+1$ rimane la denominatore perché rende l'algebra a seguire più facile). Se questi fossero esatti e non un'approssimazione, si avrebbe
$$c_{j}=\frac{2^{j}}{j!}c_{0}$$
e quindi
$$v(\rho)=c_{0}\sum\limits_{j=0}^{\infty} \frac{2^{j}}{j!}\rho^{j}=c_{0}e^{2\rho}$$
e infine
$$u(\rho)=c_{0}\rho^{l+1}e^{\rho}$$
che va all'infinito per $\rho$ grande. L'esponenziale positivo è esattamente il termine che abbiamo rimosso nel risolvere il comportamento per $\rho \rightarrow \infty$. Dunque, l'unica soluzione qui è che la serie non è infinita. Deve quindi esserci un certo indice $j_{\text{max}}$  tale per cui
$$c_{j_\text{max}+i}=0 \quad \forall i=1,2,\ldots$$
Allora dalla $(4)$ vale
$$2(j_{\text{max}}+l+1)-\rho_{0}=0$$
Definendo il **numero quantico principale**
$$n\equiv j_{\text{max}}+l+1\tag{5}$$
si ha
$$\rho_{0}=2n$$
e dato che da $\rho_{0}$ possiamo risalire a $\kappa$ e quindi ad $E$:
$$E=- \frac{\hbar^{2}\kappa^{2}}{2m}=- \frac{me^{4}}{8\pi^{2}\epsilon_{0}^{2}\hbar^{2}\rho_{0}^{2}}$$
da cui troviamo gli autostati di energia permessa
$$\boxed{E_{n}=-\left[ \frac{m}{2\hbar^{2}}\left( \frac{e^{2}}{4\pi\epsilon_{0}}\right)^{2}\right] \frac{1}{n^{2}}=\frac{E_{1}}{n^{2}}}$$
Questa si chiama **formula di Bohr**.

Se invece combiniamo la definizione di $\rho_{0}$ con $\rho_{0}=2n$ possiamo trovare $\kappa$ come
$$\kappa=\left( \frac{me^{2}}{4\pi\epsilon_{0}\hbar^{2}}\right) \frac{1}{n}= \frac{1}{a_{0}n}$$
dove abbiamo definito
$$a_{0}\equiv \frac{4\pi\epsilon_{0}\hbar^{2}}{me^{2}}=0.529\times10^{-10}\text{m}$$
il cosiddetto **[[raggio di Bohr]]**. Dalla definizione $\rho\equiv\kappa r$ abbiamo
$$\rho= \frac{r}{a_{0}n}$$
Possiamo infine trovare la forma della funzione d'onda, che sarà determinata da tre [[numero quantico|numeri quantici]] ($n$, $l$, $m$):
$$\psi_{nlm}(r,\theta,\phi)=R_{nl}(r)Y_{l}^{m}(\theta,\phi)$$
dove
$$R_{nl}(r)=\frac{1}{r}\rho^{l+1}e^{-\rho}v(\rho)$$
e $v(\rho)$ è un polinomio di grado $j_{\text{max}}=n-l-1$ in $\rho$, i cui coefficienti sono determinati dalla formula ricorsiva $(4)$.

Lo stato fondamentale $n=1$ è
$$E_{1}=-\left[ \frac{m}{2\hbar^{2}} \left(\frac{e^{2}}{4\pi\epsilon_{0}}\right)^{2}\right]=-13.6\text{ eV}$$
che è l'[[energia di legame]] dell'elettrone nello stato fondamentale dell'atomo di idrogeno. Per $n=1$, $l=0$ per la $(5)$, quindi anche $m=0$ poiché $|m|\leq l$. Dobbiamo trovare
$$\psi_{100}(r,\theta,\phi)=R_{10}(r)Y_{0}^{0}(\theta,\phi)$$
La $(4)$ ci dice che la serie termine appena dopo il primo termine, quindi $v(\rho)$ è una costante $c_{0}$ e la parte radiale è
$$R_{10}(r)=\frac{c_{0}}{a_{0}}e^{-r/a_{0}}$$
Normalizzandola si trova
$$\int_{0}^{\infty}|R_{10}|^{2}r^{2}dr= \frac{|c_{0}|^{2}}{a_{0}^{2}}\int_{0}^{\infty} e^{-2r/a_{0}} r^{2}dr=|c_{0}|^{2} \frac{a_{0}}{4}=1$$
che significa $c_{0}=2/\sqrt{a_{0}}$. L'[[Armoniche sferiche|armonica sferica]] con $l=0$ e $m=0$ è $Y_{0}^{0}=1/\sqrt{4\pi}$, quindi la funzione d'onda dello stato fondamentale dell'atomo di idrogeno è
$$\boxed{\psi_{100}(r,\theta,\phi)=\frac{1}{\sqrt{\pi a^{3}}}e^{-r/a_{0}}}$$
Livelli di energia più alti ($n\geq2$) presentano degenerazione pari a
$$d(n)=\sum\limits_{l=0}^{n-1}(2l+1)=n^{2}$$

La serie di potenze $v(\rho)$ definita con la formula ricorsiva $(4)$ può essere scritta come
$$v(\rho)=L_{n-l-1}^{2l+1}(2\rho)$$
con
$$L_{q-p}^{p}(x)\equiv(-1)^{p}\left(\frac{d}{dx}\right)^{p}L_{q}(x)$$
i [[polinomi di Laguerre|polinomi di Laguerre associati]] e
$$L_{q}(x)\equiv e^{x}\left(\frac{d}{dx}\right)^{q}(e^{-x}x^{q})$$
i [[polinomi di Laguerre]]. Possiamo quindi scrivere la funzione d'onda radiale nella forma generica
$$\boxed{R_{nl}(r)=\frac{1}{na_{0}}\left(\frac{r}{na_{0}}\right)^{l}e^{-r/(na_{0})}L_{n-l-1}^{2l+1}\left(\frac{2r}{na_{0}}\right)}$$

Possiamo anche normalizzare la funzione d'onda nel suo caso più generico. Così facendo si trova la funzione d'onda di un qualsiasi stato dell'atomo di idrogeno
$$\boxed{\psi_{nlm}(r,\theta,\phi)=\sqrt{\left(\frac{2}{na_{0}}\right)^{3} \frac{(n-l-1)!}{2n[(n+l)!]^{3}}}e^{-r/na_{0}} \left(\frac{2r}{na_{0}}\right)^{l}\left[L_{n-l-1}^{2l+1}\left(\frac{2r}{na_{0}}\right)\right]Y_{l}^{m}(\theta,\phi)}$$
Questa è una delle pochissime funzioni d'onda di casi realistici che possono essere risolte in forma chiusa. Le diverse funzioni d'onda sono fra loro [[Ortogonalità|ortogonali]]:
$$\int \psi_{nlm}^{*}\psi_{n'l'm'}r^{2}\sin\theta dr d\theta d\phi=\delta_{nn'}\delta_{ll'}\delta_{mm'}$$
usando la [[delta di Kronecker]]. Questo segue dall'ortogonalità delle armoniche sferiche e dal fatto che sono [[Equazione agli autovalori|autofunzioni]] di $\hat{H}$ con autovalori distinti.
### Transizioni
Dato che gli [[Stato stazionario|stati stazionari]] sono ben noti, è possibile calcolare facilmente l'energia assorbita o emessa dall'elettrone durante una [[transizione di stato]]. L'energia di transizione è
$$E_{\gamma}=E_{i}-E_{f}=-13.6\text{ eV }\left( \frac{1}{n_{i}^{2}}- \frac{1}{n_{f}^{2}}\right)$$
dove $n_{i}$ e $n_{f}$ sono i numeri quantici principali degli stato di inizio e fine.

Usando la [[formula di Planck]] e il fatto che la lunghezza d'onda per un [[fotone]] sia $\lambda=c/\nu$, abbiamo anche
$$\frac{1}{\lambda}=R\left(\frac{1}{n^{2}_{f}}- \frac{1}{n_{i}^{2}}\right)$$
dove $R$ è la [[costante di Rydberg]]. Questo risultato si dice **[[formula di Rydberg]]** per lo spettro dell'atomo di idrogeno.

[^1]: Ci sono due motivi per controllare e poi estrarre il comportamento asintotico anziché lavorare direttamente con $u(r)$. Estrarre $\rho^{l+1}$ serve a far si che la serie a cui giungiamo alla fine parta con termini non nulli (altrimenti i primi $l+1$ termini sarebbero tutti zeri). Estrarre $e^{-\rho}$ è utile perché il risultato ottenuto senza questa estrazione è molto più complicato.