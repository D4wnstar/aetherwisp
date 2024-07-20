## Campi
### Equazioni di Maxwell
Nel vuoto:
$$\begin{align}
\nabla\cdot\mathbf{E} & =\frac{\rho}{\varepsilon_{0}} &
\nabla\times\mathbf{E} & = -\frac{ \partial \mathbf{B} }{ \partial t } \\
\nabla\cdot\mathbf{B} & =\mathbf{0} &
\nabla\times\mathbf{B} &= \mu_{0}\mathbf{J}+\mu_{0}\varepsilon_{0}\frac{ \partial \mathbf{E} }{ \partial t } 
\end{align}$$
Nella materia:
$$\begin{align}
\nabla\cdot\mathbf{D}&=\rho_{f} & \nabla\times\mathbf{E}&=-\frac{ \partial \mathbf{B} }{ \partial t }  \\
\nabla\cdot\mathbf{B} & =0 & \nabla\times\mathbf{\mathbf{H}} & =\mathbf{J}_{f}+\frac{ \partial \mathbf{D} }{ \partial t } 
\end{align}$$
### Campo elettrico
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\sum\limits_{i=1}^{n} \frac{q_{i}}{\mathfrak{r}_{i}^{2}}\hat{\mathfrak{r}}_{i},\qquad\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{\gamma} \frac{\lambda(\mathbf{r}')}{\mathfrak{r}^{2}}\hat{\mathfrak{r}}\ dt'$$
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{\Phi}\frac{\sigma(\mathbf{r}')}{\mathfrak{r}^{2}}\hat{\mathfrak{r}}\ da',\qquad\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{V}\frac{\rho(\mathbf{r}')}{\mathfrak{r}^{2}}\hat{\mathfrak{r}}\ d\tau'$$
Discontinuità:
$$E_{\text{above}}^{\perp}-E_{\text{below}}^{\perp}=\frac{\sigma}{\varepsilon_{0}},\qquad\mathbf{E}_\text{above}^{\parallel}=\mathbf{E}_\text{below}^{\parallel}$$
Piano infinito
$$\mathbf{E}=\frac{\sigma}{2\varepsilon_{0}}\hat{\mathbf{z}}$$
Carica puntiforme, sfera o palla da fuori
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
Discontinuità:
$$V_\text{above}=V_\text{below},\qquad \frac{ \partial V_\text{above} }{ \partial n } - \frac{ \partial V_\text{below} }{ \partial n }=- \frac{1}{\varepsilon_{0}}\sigma $$
Monopolo è carica puntiforme. Dipolo:
$$V_\text{dip}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{\mathbf{p}\cdot\hat{\mathbf{r}}}{r^{2}}$$
Per un dipolo fisico $\mathbf{p}=q\mathbf{d}$. Per un sistema di cariche $\mathbf{p}=\sum_{i=1}^{n} q_{i}\mathbf{r}_{i}'$. Dipende dalla scelta di origine. Se si sposta l'origine di un vettore $\mathbf{a}$ si ha $\tilde{\mathbf{p}}=\mathbf{p}-Q\mathbf{a}$.
### Legge di Gauss
$$\oint_{S}\mathbf{E}\cdot d\mathbf{S}=\frac{Q_{\text{enc}}}{\varepsilon_{0}},\qquad\oint_{S} \mathbf{D}\cdot d\mathbf{a}=Q_{f,\text{enc}}$$
con $S$ la superficie Gaussiana e $Q_\text{enc}$ le cariche racchiuse dentro. Utile in simmetria sferica (superficie: sfera concentrica), cilindrica (superficie: cilindro coassiale) e planare (superficie: scatoletta che passa attraverso il piano). Permettono di estrarre il modulo del campo elettrico dall'integrale. Un sistema composto da sistemi singolarmente simmetrici può essere risolto come somma delle soluzioni date dalla legge (tipo le armature di un condensatore).
### Energia di un sistema
Elettrica
$$W=\frac{1}{2}\int _{\mathcal{V}} \rho V\ d\tau=\frac{\varepsilon_{0}}{2}\int _\text{all space} E^{2}\ d\tau$$
Magnetica
$$W=\frac{1}{2}\int_{\mathcal{V}}(\mathbf{A}\cdot \mathbf{J})\ d\tau=\frac{1}{2\mu_{0}}\int _\text{all space}B^{2}\  d\tau=\frac{1}{2}LI^{2}$$
## Materia
### Conduttori
Hanno "infinite" cariche libere di muoversi all'interno.
1. Il campo elettrico è sempre nullo all'interno.
2. La densità volumica di carica è zero all'interno.
3. Tutta la carica risiede sulla superficie.
4. Un conduttore è un volume equipotenziale. Qualunque due punti all'interno hanno lo stesso potenziale.
5. Il campo elettrico è normale alla superficie in ogni punto.
### Dielettrici
Le cariche sono legate a atomi/molecole e al massimo si ruotano e stirano un po'. Subiscono una polarizzazione $\mathbf{P}$ tale per cui
$$\sigma_{b}=\mathbf{P}\cdot \hat{\mathbf{n}}\qquad \rho_{b}=-\nabla'\cdot\mathbf{P}$$
Se sono lineari vale
$$\mathbf{P}=\varepsilon_{0}\chi_{e}\mathbf{E},\qquad \mathbf{D}=\varepsilon \mathbf{E}=\varepsilon_{0}(1+\chi_{e})\mathbf{E}$$
Se il dielettrico è omogeneo e si rimane al suo interno (non varia $\chi_{e}$) si ha
$$\mathbf{E}=\frac{1}{\varepsilon}\mathbf{D}=\frac{1}{\varepsilon_{r}}\mathbf{E}_\text{vac}$$
con $\mathbf{E}_\text{vac}$ il campo elettrico che si avrebbe se non ci fosse il dielettrico. Sempre in questo caso
$$\rho_{b}=-\nabla\cdot\mathbf{P}=-\nabla \cdot\left( \varepsilon_{0} \frac{\chi_{e}}{\varepsilon}\mathbf{D} \right)=-\left( \frac{\chi_{e}}{1+\chi_{e}} \right)\rho_{f}$$
## Circuiti
### Condensatori
Capacità $C=Q/V$, strettamente positiva. Armature parallele, sfere concentriche:
$$C=\frac{A\varepsilon_{0}}{d},\qquad C=4\pi \varepsilon_{0} \frac{ab}{b-a}$$
con $A$ area delle armature, $d$ distanza tra di esse. $a$ e $b$ raggi delle sfere concentriche. Se le armature sono riempite di dielettrico, vale $C=\varepsilon_{r}C_\text{vac}$.
Energia immagazzinata
$$W=\frac{1}{2}CV^{2}$$
Carica in circuito RC:
$$q(t)=C\mathcal{E}(1-e^{ -t/RC }),\qquad I=\frac{\mathcal{E}}{R}e^{-t/RC}$$
Scarica in circuito RC:
$$q(t)=C\mathcal{E}e^{-t/RC},\qquad I(t)=- \frac{\mathcal{E}}{R}e^{-t/RC}$$
## Metodi
### Metodo delle immagini
Sfrutta l'unicità dell'equazione di Laplace per risolvere sistemi "a occhio".
1. Trova le condizioni al contorno: dov'è $\rho$ e dove si annulla $V$?
2. Rimuovi il conduttore.
3. Trova un posto dove aggiungere una carica puntiforme a modo che le condizioni al contorno non siano cambiate. NON AGGIUNGERE CARICHE DOVE STAI CALCOLANDO $V$.
4. Trova il potenziale del nuovo sistema. È uguale a quello del sistema originale.