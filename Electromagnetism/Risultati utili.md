## Campi
### Equazioni di Maxwell
Nel vuoto:
$$\begin{align}
\nabla\cdot\mathbf{E} & =\frac{\rho}{\varepsilon_{0}} &
\nabla\times\mathbf{E} & = -\frac{ \partial \mathbf{B} }{ \partial t } \\
\nabla\cdot\mathbf{B} & =\mathbf{0} &
\nabla\times\mathbf{B} &= \mu_{0}\mathbf{J}+\mu_{0}\varepsilon_{0}\frac{ \partial \mathbf{E} }{ \partial t } 
\end{align}$$
### Forza di Lorentz
$$\mathbf{F}=Q[\mathbf{E}+(\mathbf{v}\times \mathbf{B})]$$
### Campo elettrico
Legge di Coulomb
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\sum\limits_{i=1}^{n} \frac{q_{i}}{\mathfrak{r}_{i}^{2}}\hat{\mathfrak{r}}_{i},\qquad\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{\gamma} \frac{\lambda(\mathbf{r}')}{\mathfrak{r}^{2}}\hat{\mathfrak{r}}\ dt'$$
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{\Phi}\frac{\sigma(\mathbf{r}')}{\mathfrak{r}^{2}}\hat{\mathfrak{r}}\ da',\qquad\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{V}\frac{\rho(\mathbf{r}')}{\mathfrak{r}^{2}}\hat{\mathfrak{r}}\ d\tau'$$
Discontinuità, interamente normale alla superficie:
$$E_{\text{above}}^{\perp}-E_{\text{below}}^{\perp}=\frac{\sigma}{\varepsilon_{0}},\qquad \mathbf{E}_\text{above}^{\parallel}=\mathbf{E}_\text{below}^{\parallel},\qquad\mathbf{E}_\text{above}-\mathbf{E}_\text{below}=\frac{\sigma}{\varepsilon_{0}}\hat{\mathbf{n}}$$
Piano infinito, cavo/cilindro fine
$$\mathbf{E}=\frac{\sigma}{2\varepsilon_{0}}\hat{\mathbf{z}},\qquad \mathbf{E}=\frac{\lambda}{2\pi \varepsilon_{0}s}\hat{\mathbf{s}}$$
Carica puntiforme, sfera o palla di raggio $R$ da fuori
$$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{Q}{r^{2}}\hat{\mathbf{r}} \qquad \text{se }r>R,\qquad\mathbf{E}=0 \qquad \text{se }r<R\text{ (solo sfera)}$$
Palla da dentro ($r<R$)
$$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{r}{R^{3}}Q\hat{\mathbf{r}} \qquad \text{se }r<R$$
Dipolo
$$\mathbf{E}_\text{dip}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{1}{r^{3}}[3(\mathbf{p}\cdot \hat{\mathbf{r}})\hat{\mathbf{r}}-\mathbf{p}]$$
### Potenziale elettrico
$$V(\mathbf{r})=-\int_{\mathcal{O}}^{\mathbf{r}}\mathbf{E}\cdot d\mathbf{r}'=\frac{1}{4\pi\varepsilon_{0}}\int\frac{\rho(\mathbf{r}')}{\mathfrak{r}}d\tau'\qquad \mathbf{E}=-\nabla V\qquad\nabla ^{2}V=- \frac{\rho}{\varepsilon_{0}}$$
Carica puntiforme, sfera o palla da fuori ($r>R$)
$$V(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{q}{r}$$
Potenziale dentro una sfera è costante (difatti il campo è nullo).
Discontinuità: nessuna, ma la derivata normale sì:
$$V_\text{above}=V_\text{below},\qquad \frac{ \partial V_\text{above} }{ \partial n } - \frac{ \partial V_\text{below} }{ \partial n }=- \frac{1}{\varepsilon_{0}}\sigma $$
Monopolo è carica puntiforme. Dipolo:
$$V_\text{dip}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{\mathbf{p}\cdot\hat{\mathbf{r}}}{r^{2}}$$
Per un dipolo fisico $\mathbf{p}=q\mathbf{d}$. Per un sistema di cariche $\mathbf{p}=\sum_{i=1}^{n} q_{i}\mathbf{r}_{i}'$. Dipende dalla scelta di origine. Se si sposta l'origine di un vettore $\mathbf{a}$ si ha $\tilde{\mathbf{p}}=\mathbf{p}-Q\mathbf{a}$.
### Legge di Gauss
$$\oint_{S}\mathbf{E}\cdot d\mathbf{S}=\frac{Q_{\text{enc}}}{\varepsilon_{0}},\qquad\oint_{S} \mathbf{D}\cdot d\mathbf{a}=Q_{f,\text{enc}}$$
con $S$ la superficie Gaussiana e $Q_\text{enc}$ le cariche racchiuse dentro. Utile in simmetria **sferica** (superficie: sfera concentrica), **cilindrica** (superficie: cilindro coassiale) e **planare** (superficie: scatoletta che passa attraverso il piano). Permettono di estrarre il modulo del campo elettrico dall'integrale. Un sistema composto da sistemi singolarmente simmetrici può essere risolto come somma delle soluzioni date dalla legge (tipo le armature di un condensatore).
### Legge di Faraday
$$\mathcal{E}=\oint_{\gamma} \mathbf{E}\cdot d\mathbf{r}=-\int_{S} \frac{ \partial \mathbf{B} }{ \partial t }\cdot d\mathbf{a}$$
dove $\mathcal{E}$ è l'emf indotta. La **legge di Lenz** dice che la direzione del campo elettrico indotto è sempre tale da contrastare la variazione di flusso magnetico. Se il flusso aumenta, il campo indotto crea una corrente che crea un campo magnetico opposto a quello originale.
### Correnti
Stazionaria se $d\mathbf{J}/dt=0$. Lineari, superficiali, volumiche:
$$\mathbf{I}=\lambda \mathbf{v},\quad \mathbf{K}=\sigma \mathbf{v}= \frac{d\mathbf{I}}{dl_{\perp}},\quad \mathbf{J}=\rho \mathbf{v}=\frac{d\mathbf{I}}{da_{\perp}}$$
Forze magnetiche delle correnti
$$\mathbf{F}_\text{mag}=\int(\mathbf{I}\times \mathbf{B})\ dl,\quad \mathbf{F}_\text{mag}=\int(\mathbf{K}\times \mathbf{B})\ da,\quad \mathbf{F}_\text{mag}=\int(\mathbf{J}\times \mathbf{B})\ d\tau$$
Equazione di continuità
$$\nabla\cdot\mathbf{J}=- \frac{ \partial \rho }{ \partial t } (=0\text{ se magnetostatica})$$
### Campo magnetico
Legge di Biot-Savart
$$\mathbf{B}(\mathbf{r})=\frac{\mu_{0}}{4\pi}I\int_{\gamma} \frac{d\mathbf{I}\times \hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}}\ dl',\qquad\mathbf{B}(\mathbf{r})=\frac{\mu_{0}}{4\pi}\int \frac{\mathbf{K}(\mathbf{r}')\times \hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}}\ da'$$
$$\mathbf{B}(\mathbf{r})=\frac{\mu_{0}}{4\pi}\int \frac{\mathbf{J}(\mathbf{r}')\times \hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}}\ d\tau'$$
Discontinuità (interamente parallela alla corrente)
$$B^{\perp}_\text{above}=B^{\perp}_\text{below}=0,\qquad B_\text{above}^{\parallel}-B_\text{below}^{\parallel}=\mu_{0}K,\qquad\mathbf{B}_\text{above}-\mathbf{B}_\text{below}=\mu_{0}(\mathbf{K}\times \hat{\mathbf{n}})$$

Attorno ad un filo (circumferenziale), dentro un solenoide con $n$ giri/lunghezza (dritto)
$$\mathbf{B}=\frac{\mu_{0}I}{2\pi s}\hat{\boldsymbol{\phi}},\qquad B=\mu_{0}nI$$
### Potenziale vettore magnetico
$$\nabla\times\mathbf{A}=\mathbf{B},\quad \nabla ^{2}\mathbf{A}=-\mu_{0}\mathbf{J}$$
$$\mathbf{A}(\mathbf{r})=\frac{\mu_{0}}{4\pi}\int \frac{\mathbf{I}(\mathbf{r}')}{\mathfrak{r}}\ dl',\quad \mathbf{A}(\mathbf{r})=\frac{\mu_{0}}{4\pi}\int \frac{\mathbf{K}(\mathbf{r})'}{\mathfrak{r}}\ da',\quad \mathbf{A}(\mathbf{r})=\frac{\mu_{0}}{4\pi}\int \frac{\mathbf{J}(\mathbf{r}')}{\mathfrak{r}}\ d\tau'$$
Discontinuità. Nessuna, ma la derivata normale sì:
$$\mathbf{A}_\text{above}=\mathbf{A}_\text{below},\quad\frac{ \partial \mathbf{A}_\text{above} }{ \partial n } -\frac{ \partial \mathbf{A}_\text{below} }{ \partial n } =-\mu_{0}\mathbf{K}$$
### Legge di Ampere
$$\oint_{\gamma} \mathbf{B}\cdot d\mathbf{r}=\mu_{0}I_\text{enc},\quad \nabla ^{2}\mathbf{A}=-\mu_{0}\mathbf{J}$$
con $\gamma$ il loop amperiano entro cui passa corrente $I_\text{enc}$. Utile attorno ad un **filo infinito dritto**, attraverso una **superficie piatta**, attraverso un **solenoide infinito** e attraverso un **toro**. Valida solo in magnetostatica, in elettrodinamica va corretta con la corrente di spostamento:
$$\oint \mathbf{B}\cdot d\mathbf{r}=\mu_{0}I_\text{enc}+\mu_{0}\varepsilon_{0}\int\left( \frac{ \partial \mathbf{E} }{ \partial t }  \right)\cdot d\mathbf{a}$$
### Energia di un sistema
Elettrica
$$W=\frac{1}{2}\int _{\mathcal{V}} \rho V\ d\tau=\frac{\varepsilon_{0}}{2}\int _\text{all space} E^{2}\ d\tau$$
Magnetica
$$W=\frac{1}{2}\int_{\mathcal{V}}(\mathbf{A}\cdot \mathbf{J})\ d\tau=\frac{1}{2\mu_{0}}\int _\text{all space}B^{2}\  d\tau=\frac{1}{2}LI^{2}$$
Il volume di integrazione $\mathcal{V}$ è il volume che contiene tutta la carica/corrente.
## Materia
### Quantità
Spostamento (displacement) elettrico
$$\mathbf{D}=\varepsilon_{0}\mathbf{E}+\mathbf{P},\quad \nabla\cdot\mathbf{D}=\rho_{f},\quad \nabla\times\mathbf{D}=\nabla\times\mathbf{P}$$
Discontinuità
$$D_\text{above}^{\perp}-D_\text{below}^{\perp}=\sigma_{f},\qquad\mathbf{D}_\text{above}^{\parallel}-\mathbf{D}_\text{below}^{\parallel}=\mathbf{P}_\text{above}^{\parallel}-\mathbf{P}_\text{below}^{\parallel}$$

Campo ausiliario
$$\mathbf{H}=\frac{1}{\mu_{0}}\mathbf{B}-\mathbf{M},\quad \nabla\cdot\mathbf{H}=-\nabla\cdot\mathbf{M},\quad \nabla\times\mathbf{H}=\mathbf{J}_{f}$$
Discontinuità
$$H_\text{above}^{\perp}-H_\text{below}^{\perp}=-(M_\text{above}^{\perp}-M_\text{below}^{\perp}),\qquad\mathbf{H}^{\parallel}_\text{above}-\mathbf{H}^{\parallel}_\text{below}=\mathbf{K}_{f}\times \hat{\mathbf{n}}$$
### Conduttori
Hanno "infinite" cariche libere di muoversi all'interno.
1. Il campo elettrico è sempre nullo all'interno.
2. La densità volumica di carica è zero all'interno.
3. Tutta la carica risiede sulla superficie.
4. Un conduttore è un volume equipotenziale. Qualunque due punti all'interno hanno lo stesso potenziale.
5. Il campo elettrico è normale alla superficie in ogni punto.
### Dielettrici e polarizzazione
Le cariche sono legate a atomi/molecole e al massimo si ruotano e stirano un po'. Subiscono una polarizzazione $\mathbf{P}$ tale per cui
$$\sigma_{b}=\mathbf{P}\cdot \hat{\mathbf{n}}\qquad \rho_{b}=-\nabla'\cdot\mathbf{P}$$
e con esse
$$V=\frac{1}{4\pi\varepsilon_{0}}\oint_{\mathcal{S}} \frac{\sigma_{b}}{\mathfrak{r}}\ da'+\frac{1}{4\pi\varepsilon_{0}}\int_{\mathcal{V}} \frac{\rho_{b}}{\mathfrak{r}}\ d\tau'$$
Se sono lineari vale
$$\mathbf{P}=\varepsilon_{0}\chi_{e}\mathbf{E},\qquad \mathbf{D}=\varepsilon \mathbf{E}=\varepsilon_{0}(1+\chi_{e})\mathbf{E}$$
Se il dielettrico è omogeneo e si rimane al suo interno (non varia $\chi_{e}$) si ha
$$\mathbf{E}=\frac{1}{\varepsilon}\mathbf{D}=\frac{1}{\varepsilon_{r}}\mathbf{E}_\text{vac}$$
con $\mathbf{E}_\text{vac}$ il campo elettrico che si avrebbe se non ci fosse il dielettrico. Sempre in questo caso
$$\rho_{b}=-\nabla\cdot\mathbf{P}=-\nabla \cdot\left( \varepsilon_{0} \frac{\chi_{e}}{\varepsilon}\mathbf{D} \right)=-\left( \frac{\chi_{e}}{1+\chi_{e}} \right)\rho_{f}$$
### Magnetizzazione
Un paramagnete o diamagnete sottoposto ad un campo magnetico esibisce una magnetizzazione $\mathbf{M}$ tale per cui
$$\mathbf{K}_{b}=\mathbf{M} \times \hat{\mathbf{n}},\quad \mathbf{J}_{b}=\nabla\times\mathbf{M}$$
e con esse
$$\mathbf{A}(\mathbf{r})=\frac{\mu_{0}}{4\pi}\int_{\mathcal{V}} \frac{\mathbf{J}_{b}}{\mathfrak{r}}\ d\tau'+ \frac{\mu_{0}}{4\pi}\int_{\mathcal{S}} \frac{\mathbf{K}_{b}}{\mathfrak{r}}\ da'$$
Se sono lineari vale
$$\mathbf{M}=\chi_{m}\mathbf{H},\quad \mathbf{B}=\mu_{0}(1+\chi_{m})=\mu \mathbf{H}$$
Se il diamagnete/paramagnete è lineare e omogeneo vale anche
$$\mathbf{J}_{b}=\nabla\times\mathbf{M}=\nabla \times(\chi_{m}\mathbf{H})=\chi_{m}\mathbf{J}_{f}$$
## Circuiti
### Equazioni di Maxwell
Nella materia:
$$\begin{align}
\nabla\cdot\mathbf{D}&=\rho_{f} & \nabla\times\mathbf{E}&=-\frac{ \partial \mathbf{B} }{ \partial t }  \\
\nabla\cdot\mathbf{B} & =0 & \nabla\times\mathbf{\mathbf{H}} & =\mathbf{J}_{f}+\frac{ \partial \mathbf{D} }{ \partial t } 
\end{align}$$
### Resistenze
Si sommano in serie e si somma il reciproco in parallelo
$$\underbrace{ R=\sum_{i=1}^{N} R_{i} }_{ \text{serie} },\qquad \underbrace{ \frac{1}{R}=\sum_{i=1}^{N} \frac{1}{R_{i}} }_{ \text{parallelo} }$$
### Condensatori
Capacità $C=Q/V$, strettamente positiva. Armature parallele, sfere concentriche:
$$C=\frac{A\varepsilon_{0}}{d},\qquad C=4\pi \varepsilon_{0} \frac{ab}{b-a}$$
con $A$ area delle armature, $d$ distanza tra di esse. $a$ e $b$ raggi delle sfere concentriche. Se le armature sono riempite di dielettrico, vale $C=\varepsilon_{r}C_\text{vac}$.
Si somma il reciproco in serie e si sommano in parallelo
$$\underbrace{ \frac{1}{C}=\sum_{i=1}^{N} \frac{1}{C_{i}} }_{ \text{serie} },\qquad\underbrace{ C=\sum_{i=1}^{N} C_{i} }_{ \text{parallelo} }$$
Energia immagazzinata
$$W=\frac{1}{2}CV^{2}$$
Carica in circuito RC:
$$q(t)=C\mathcal{E}(1-e^{ -t/RC }),\qquad I(t)=\frac{ \partial q(t) }{ \partial t } =\frac{\mathcal{E}}{R}e^{-t/RC}$$
Scarica in circuito RC:
$$q(t)=C\mathcal{E}e^{-t/RC},\qquad I(t)=\frac{ \partial q(t) }{ \partial t } =- \frac{\mathcal{E}}{R}e^{-t/RC}$$
### Legge di Ohm
Forma generale per correnti, forma pratica per circuiti. La forza per unità di carica $\mathbf{f}$ si riduce al campo elettrico $\mathbf{E}$ al di fuori dell'elettrodinamica relativistica.
$$\mathbf{J}=\sigma_{C}\mathbf{f}=\sigma_{C}\mathbf{E},\qquad \Delta V=RI$$
Se la conduttività $\sigma_{C}$ del materiale è uniforme ed è soggetto a corrente stazionaria, allora $\nabla\cdot\mathbf{J}=0$ dentro il materiale e vale l'equazione di Poisson.
### Leggi di Kirchhoff
**Legge dei nodi.** La somma direzionata di correnti entro un nodo è sempre nulla. La corrente che entra è sempre uguale e opposta alla corrente che esce.
$$\sum_{i=1}^{N} I_{i}=0$$
**Legge delle maglie.** La somma direzionata dei potenziali in una maglia è sempre nulla. Gli aumenti e le cadute di potenziale in una maglia si bilanciano sempre.
$$\sum_{i=1}^{N} \Delta V_{i}=0$$
### Effetto Joule
L'energia che passa attraverso una resistenza viene trasformata in calore con potenza dipendente dalla resistenza in sé e della corrente/potenziale.
$$P=I\Delta V=RI^{2}$$
### Forza elettromotiva
Mette in moto un circuito. È necessariamente non conservativa.
$$\mathcal{E}=\int_{A}^{B}\mathbf{f}\cdot d\mathbf{r}=\oint_{\gamma} \mathbf{f}\cdot d\mathbf{r}$$
Il primo integrale è tra i terminali $A$ e $B$ del generatore, il secondo su tutto il circuito $\gamma$. $\mathbf{f}$ è una forza non conservativa per unità di carica e non può essere un campo elettrostatico. Nel caso di un flusso magnetico $\Phi$ che varia nel tempo in un loop si ha la emf di spostamento
$$\mathcal{E}=- \frac{d\Phi}{dt}$$
### Induttanza mutua
Descrive la corrente indotta da un loop ad un altro secondo
$$\Phi_{2}=MI_{1}\quad\Rightarrow \quad \mathcal{E}_{2}=-M \frac{dI_{1}}{dt}$$
dove $\Phi_{2}$ è il flusso magnetico sul secondo, $I_{1}$ e la corrente del primo $\mathcal{E}_{2}$ è la emf sul secondo.
### Autoinduttanza
Descrive la corrente indotta da un loop in sé stesso. Di fatto, mutua induttanza su sé stesso.
$$\Phi =LI\quad\Rightarrow \quad \mathcal{E}=-L \frac{dI}{dt}$$
In un circuito RL, la corrente carica come
$$I(t)=\frac{\mathcal{E}_{0}}{R}[1-e^{-R/L}t]$$
## Metodi
### Metodo delle immagini
Sfrutta l'unicità dell'equazione di Laplace per risolvere sistemi "a occhio".
1. Trova le condizioni al contorno: dov'è $\rho$ e dove si annulla $V$?
2. Rimuovi il conduttore.
3. Trova un posto dove aggiungere una carica puntiforme a modo che le condizioni al contorno non siano cambiate. Non aggiungere cariche dove stai calcolando $V$!
4. Trova il potenziale del nuovo sistema. È uguale a quello del sistema originale.
### Legge di Gauss/Ampere
Sfrutta la simmetria del sistema. Particolarmente utile quando il sistema va all'infinito.
1. Trova una delle simmetrie utili.
2. Poni una superficie gaussiana o loop amperiano dove vuoi calcolare la quantità.
3. Sfrutta la simmetria per tirare fuori dall'integrale il modulo del campo.
4. Risolvi l'altro integrale.
5. Ricostruisci il vettore ragionando su quale potrebbe essere la direzione.
### Circuiti
Tutti i circuiti sono in un modo o nell'altro risolti dalle leggi di Kirchhoff e quella di Ohm. Fai attenzione ai segni delle correnti arbitrarie nella legge delle maglie!
## Analisi
### Teorema del gradiente/divergenza/rotore
$$\int_{\mathbf{a}}^{\mathbf{b}}(\nabla f)\cdot d\mathbf{r}=f(\mathbf{b})-f(\mathbf{a}),\quad \int_{V}(\nabla\cdot\mathbf{A})\ d\tau=\oint_{S} \mathbf{A}\cdot d\mathbf{a},\quad \int_{S}(\nabla\times\mathbf{A})\cdot d\mathbf{a}=\oint_{\gamma}\mathbf{A}\cdot d\mathbf{r}$$
Integrati sulle corrispettive frontiere.
### Coordinate sferiche
$$\begin{cases}
x=r\sin \theta \cos \phi \\
y=r\sin \theta \sin \phi \\
z=r\cos \theta
\end{cases}
\qquad
\begin{cases}
r=\sqrt{ x^{2}+y^{2}+z^{2} } \\
\theta=\arctan( \sqrt{x^{2}+y^{2}}/z ) \\
\phi=\arctan(y/x)
\end{cases}$$
Funzione di cambio da cartesiane a sferiche: $d\tau=r^{2}\sin \theta\ drd\theta d\phi$.
### Coordinate cilindriche
$$\begin{cases}
x=s\cos \phi \\
y=s\sin \phi \\
z=z
\end{cases}
\qquad
\begin{cases}
s=\sqrt{ x^{2}+y^{2} } \\
\phi=\arctan(y/x) \\
z=z
\end{cases}$$
Funzione di scambio da cartesiane a cilindriche: $d\tau=s\ dsd\phi dz$.
### Legge dei coseni
Triangolo di lati $a$, $b$ e $c$:
$$c^{2} =a^{2}+b^{2}-2ab\cos \gamma$$
con $\gamma$ l'angolo opposto ad $a$ e $b$.