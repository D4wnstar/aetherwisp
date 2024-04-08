La **struttura fine** è la struttura ottenuta applicando correzioni relativistiche ottenute dalla [[funzione d'onda]] relativistica al modello dell'[[atomo]] di idrogeno.
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
$$\Delta E_{1}=-E_{n} \frac{(Z\alpha)^{2}}{n^{2}} \left[\frac{3}{4} - \frac{n}{l-\frac{1}{2}} \right]$$
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
$$H_{so}=- \frac{1}{2}\vec{\mu_{S}}\cdot\vec{B}= \frac{1}{2m^{2}c^{2}r} \frac{dV}{dr}\vec{L}\cdot\vec{S}$$
Questa forma più corretta esce naturalmente seguendo il formalismo di Dirac.

$H_{so}$ commuta con $L^{2}$, ma non con $L_{z}$ o $S_{z}$. Introduciamo l'*[[operatore]] momento angolare* $\vec{J}=\vec{L}+\vec{S}$. Dalla definizione $\vec{J}^{2}=\vec{L}^{2}+\vec{S}^{2}+2\vec{L}\cdot\vec{S}$ ricaviamo $\vec{L}\cdot\vec{S}=(1/2) [\vec{J}^{2}-\vec{L}^{2}-\vec{S}^{2}]$. Da questo, si vede che vale
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