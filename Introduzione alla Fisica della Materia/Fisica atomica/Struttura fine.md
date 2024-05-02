La **struttura fine** è la struttura ottenuta applicando correzioni relativistiche ottenute dalla [[funzione d'onda]] relativistica al modello dell'[[atomo di idrogeno]].
## Trattamento perturbativo
È composta da tre correzioni (tutte relativistiche):
1. correzione relativistica dell'energia cinetica
2. correzione spin-orbita
3. termine di Darwin
Queste tre si sommano per darci l'[[Hamiltoniana]] corretta.
### Correzione relativistica dell'energia cinetica
Possiamo sostituire l'energia cinetica classica $p^{2}/2m_{e}$ con l'energia cinetica relativistica
$$T=\sqrt{p^{2}c^{2}+m_{e}^{2}c^{4}}-m_{e}^{2}c^{2}=m_{e}c^{2}\sqrt{1+ \frac{p^{2}}{m_{e}c^{2}}}-m_{e}c^{2}=\ldots$$
con $m_{e}$ la [[massa dell'elettrone]]. Possiamo espandere in [[Polinomio di Taylor|serie di Taylor]] la radice quadrata della forma $\sqrt{1+x}$ con
$$\ldots=m_{e}c^{2}\left(1+ \frac{1}{2} \frac{p^{2}}{m_{e}^{2}c^{2}} - \frac{p^{4}}{8m_{e}^{4}c^{4}}+\ldots\right)=m_{e}c^{2}+ \underbrace{\frac{p^{2}}{2m_{e}}}\limits_{E_{cin}} - \frac{p^{4}}{8m_{e}^{3}c^{2}}+\ldots$$
dove $E_{cin}$ è l'energia classica e i termini ulteriori sono termini correttivi. Questa correzione è proporzionale a $(Z\alpha)^{2}$, con $Z$ la carica nucleare e $\alpha$ è la [[costante di struttura fine]]. Dunque, le correzioni diventano prevalenti per atomi grandi.

È diagonale in $L^{2}$, $S^{2}$, $L_{z}$ e $S_{z}$, quindi la correzione è data al primo ordine perturbativo da $-\frac{1}{2m_{e}c^{2}}\langle \psi_{nlm}|T^{2}|\psi_{nlm}\rangle$ da cui la differenza di energia
$$\boxed{\Delta E_{1}=-E_{n} \frac{(Z\alpha)^{2}}{n^{2}} \left[\frac{3}{4} - \frac{n}{l-\frac{1}{2}} \right]}$$
### Interazione spin-orbita
L'interazione tra il momento di dipolo magnetico di [[spin]] di un elettrone e il campo magnetico interno di un atomo che dipende dal momento angolare orbitale dell'elettrone.

Una descrizione efficace di questo fenomeno si può ricavare ponendosi nel sistema di riferimento dell'elettrone in cui il [[Nucleo atomico|nucleo]] con carica $Ze$ in movimento genera un campo magnetico che interagisce con gli spin degli elettroni. Considero il campo magnetico visto dall'elettrone
$$\vec{B}=- \frac{1}{c^{2}} \vec{v}\times\vec{E}$$
e quello elettrico
$$\vec{E}=\frac{\vec{F}}{-e}=\frac{1}{er} \frac{dV}{dr}\vec{r}$$
Allora
$$\vec{B}=- \frac{1}{c^{2}}\vec{v}\times\vec{E}=- \frac{1}{c^{2}} \frac{1}{er} \frac{dV}{dr} \vec{v}\times\vec{r}=\frac{1}{mc^{2}er} \frac{dV}{dr}\vec{L}$$
Se associamo allo spin un momento magnetico intrinseco $\mu_{S}=- \frac{e}{m}\vec{S}$, spiegato dall'[[esperimento di Stern-Gerlach]], possiamo ricavare la Hamiltoniana semplicemente con
$$H_{so}=- \vec{\mu_{S}}\cdot\vec{B}= \frac{1}{m^{2}c^{2}r} \frac{dV}{dr}\vec{L}\cdot\vec{S}$$
In realtà il termine correttivo giusto ha un termine 2 iniziale, detto *fattore di Thomas*, che si è perso nelle approssimazioni fatte (il trattamento con elettrodinamica classica e non quantistica):
$$\boxed{H_{so}=- \frac{1}{2}\vec{\mu_{S}}\cdot\vec{B}= \frac{1}{2m^{2}c^{2}r} \frac{dV}{dr}\vec{L}\cdot\vec{S}}$$
Questa forma più corretta esce naturalmente seguendo il formalismo di Dirac.

$H_{so}$ commuta con $L^{2}$, ma non con $L_{z}$ o $S_{z}$. Introduciamo l'*[[Operatore]] momento angolare* $\vec{J}=\vec{L}+\vec{S}$. Dalla definizione $\vec{J}^{2}=\vec{L}^{2}+\vec{S}^{2}+2\vec{L}\cdot\vec{S}$ ricaviamo $\vec{L}\cdot\vec{S}=(1/2) [\vec{J}^{2}-\vec{L}^{2}-\vec{S}^{2}]$. Da questo, si vede che vale
$$H_{so}=\frac{1}{2}\xi(r)[\vec{J}^{2}-\vec{L}^{2}-\vec{S}^{2}]$$
e che è diagonale nel sottospazio degenere. Ci interessa solo la correzione di energia
$$\Delta E_{so}=\langle \psi_{nljm}|H_{so}|\psi_{nljm}\rangle=\frac{\hbar^{2}}{2} \langle R_{n}|\xi(r)|R_{n}\rangle[j(j+1)-l(l+1)-(s+1)]$$
Usando il potenziale Coulombiano
$$V=- \frac{Ze^{2}}{4\pi\epsilon_{0} r}$$
ho che la perturbazione è
$$\xi(r)=\frac{1}{2m_{e}^{2}c^{2}} \frac{1}{r} \frac{dV}{dr}=\frac{1}{2m_{e}^{2}c^{2}} \frac{Ze^{2}}{4\pi\epsilon_{0}} \frac{1}{r^{3}}$$
Otteniamo così una correzione
$$\left\langle \frac{1}{r^{3}} \right\rangle= \frac{Z^{3}}{a_{0}^{3}n^{3}l(l+ \frac{1}{2})(l+1)}$$
Da cui si ricava una differenza di energia che si scrive in modo orribile.
### Termine di Darwin
Il termine di Darwin è
$$\boxed{H_{D}'=\frac{\pi\hbar^{2}}{2m^{2}c^{2}} \left(\frac{Ze^{2}}{4\pi\epsilon_{0}}\right)\delta(r)}$$
Considero un [[protone]] al centro del mio sistema di riferimento. L'elettrone dista $\vec{r}$ da esso. Allora l'energia potenziale Coulombiana è
$$V(\vec{r})=-e\phi(\vec{r})\propto -e\left( \frac{e}{r}\right)\simeq- \frac{e^{2}}{r}$$
con $\phi(\vec{r})$ il potenziale Coulombiano. Introduciamo un [[Campo vettoriale]] $\vec{u}$ che definisce una regione di carica attorno all'elettrone. Allora un qualunque punto nello spazio (in particolare attorno all'elettrone) può essere espresso come $\vec{r}+\vec{u}$.
![[Schema Termine di Darwin|60%|center]]
Chiamo $\tilde{V}(\vec{r})$ l'energia potenziale "vera", pari a $\tilde{V}(\vec{r})=\int\phi dq$, integrando sul volume dell'elettrone[^1]. Definisco $\rho(\vec{u})=-e\rho_{0}(\vec{u})$ la densità di carica, tramite $\rho_{0}$ la densità di carica "a meno delle unità di misura". Deve valere $\int\rho_{0}(\vec{u})d^{3}\vec{u}$, sempre sul volume. Allora si ha
$$\tilde{V}(\vec{r})=\int_{elettrone}\rho(\vec{u})\phi(\vec{r}+\vec{u})d^{3}\vec{u}=\int \rho_{0}(\vec{u})V(\vec{r}+\vec{u})d^{3}\vec{u}$$
Possiamo calcolare l'energia potenziale in serie di potenze fino al secondo ordine
$$V(\vec{r}+\vec{u})=V(\vec{r})+\sum\limits_{i}^{\infty} \left.\frac{\partial V}{\partial x_{i}}\right|_{\vec{r}} u_{i}+ \frac{1}{2} \sum\limits_{i,j}^{\infty} \left.\frac{\partial ^{2}V}{\partial x_{i}\partial x_{j}}\right|_{\vec{r}}u_{i}u_{j}$$
quindi l'energia potenziale vera diventa
$$\tilde{V}(\vec{r})=\underbrace{\int\rho_{0}(\vec{u})d^{3}\vec{u}}\limits_{0}+\sum\limits_{i}^{\infty}\left.\frac{\partial V}{\partial x_{i}}\right|_{\vec{r}}\int \rho_{0}(\vec{u})u_{i}d^{3}\vec{u}+ \frac{1}{2}\sum\limits_{i,j}^{\infty}\left.\frac{\partial ^{2}V}{\partial x_{i}\partial x_{j}}\right|_{\vec{r}} \underbrace{\int \rho_{0}(\vec{u})u_{i}u_{j}d^{3}\vec{u}}\limits_{*}$$
dove $*$ diventa
$$\delta_{ij}\frac{1}{3}\int \rho_{0}(\vec{u})u^{2}d^{3}\vec{u}$$
con $\delta_{ij}$ la [[Delta di Kronecker]]. Rimangono allora solo gli indici uguali $i=j$, il che rende la somma di derivate seconde un [[Laplaciano]]. Dunque possiamo scrivere
$$\tilde{V}(\vec{r})=V(\vec{r})+ \frac{1}{6}\nabla^{2}V(\vec{r})\int \rho_{0}(\vec{u})u^{2}d^{3}\vec{u}$$
Si può modellare $\rho_{0}$ come
$$\newcommand\lambdabar{
\raise1.5pt{\moveright2.0pt\unicode{0x0335}}\moveleft1pt\lambda
}
\rho_{0}(\vec{u})=\begin{cases}
\frac{1}{\frac{4}{3}\pi\lambdabar^{3}}&\text{se } u<\lambdabar \\
0&\text{se }u>\lambdabar
\end{cases}$$
con $\lambdabar$ la [[lunghezza d'onda di Compton]].
### Combinazione delle correzioni
Sommando le tre correzioni ottenute, si trova che dipendono solo dal valore del momento angolare totale $j$. La differenza di energia è
$$\Delta E_{nj}=E_{n} \frac{(Z\alpha)^{2}}{n^{2}}\left(\frac{n}{j+ \frac{1}{2}} - \frac{3}{4}\right)$$
e quindi i livelli $n$ di energia si dividono in $n$ livelli per ciascun valore di $j=1/2,\;3/2,\;5/2,\;\ldots$
$$E_{nj}=E_{n}\left[1+ \frac{(Z\alpha)^{2}}{n^{2}}\left(\frac{n}{j+ \frac{1}{2}} - \frac{3}{4}\right)\right]$$


[^1]: Inteso come regione di esistenza di $\rho_{0}$