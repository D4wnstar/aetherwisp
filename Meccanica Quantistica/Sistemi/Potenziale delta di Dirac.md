Consideriamo una [[particella]] immersa in un [[potenziale]] della forma
$$V(x)=-\alpha \delta(x)$$
con $\alpha$ una costante positiva e $\delta(x)$ la [[delta di Dirac]]. Questo potenziale è una [[Buca infinita quantistica|buca infinita]] localizzata interamente nell'origine, a differenza della buca infinita vera e propria, che ha un'estensione spaziale. L'[[equazione di Schrödinger]] diventa
$$- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}} - \alpha\delta(x)\psi=E\psi$$
Per la definizione di delta di Dirac, possiamo ricavare sia stati legati che liberi.
### Stati legati
Nella regione $x<0$ si ha $V(x)=0$ e vale
$$\frac{d^{2}\psi}{dx^{2}}=- \frac{2mE}{\hbar^{2}}\psi=\kappa^{2}\psi$$
con la costante $\kappa\equiv \sqrt{-2mE}/\hbar$. Dato che $E$ è negativa (siamo in uno stato legato), $\kappa$ è reale e positiva. La soluzione generale è
$$\psi(x)=Ae^{-\kappa x}+Be^{\kappa x}$$
Per $x \rightarrow \infty$, il primo termine va anch'esso a infinito, quindi per non incappare in una soluzione non-normalizzabile bisogna che $A=0$. Quindi in $x<0$ vale
$$\psi(x)=Be^{\kappa x}\quad\text{per }x<0$$

Nella regione $x>0$ si ha ancora $V(x)=0$ e $E<0$, con la stessa soluzione generale. Stavolta è il secondo termine ad andare all'infinito, quindi l'altra costante va posta a zero. Troviamo dunque
$$\psi(x)=Ce^{-\kappa x}\quad\text{per }x>0$$

Manca solo la condizione al contorno all'origine. Le condizioni al contorno standard per la [[funzione d'onda]] indipendente dal tempo sono $\psi$ continua e $d\psi/dx$ continua tranne che in punti con potenziale infinito.

La continuità di $\psi$ ci dice che
$$Be^{\kappa 0}=Ce^{-\kappa 0} \rightarrow B=C$$
La continuità di $d\psi/dx$ purtroppo non ci dà informazioni, dato che è discontinua solo e proprio nel punto al contorno. La funzione d'onda allora è
$$\psi(x)=\begin{cases}
Be^{\kappa x} & \text{se } x\leq0 \\
-Be^{\kappa x} & \text{se } x\geq0
\end{cases}$$
Quello che possiamo fare, però, è integrare l'equazione di Schrödinger da $-\varepsilon$ e $+\varepsilon$ e prendere il limite $\varepsilon \rightarrow 0$:
$$- \frac{\hbar^{2}}{2m}\int_{-\varepsilon}^{+\varepsilon} \frac{d^{2}\psi}{dx^{2}}dx+\int_{-\varepsilon}^{+\varepsilon}V(x)\psi(x)dx=E\int_{-\varepsilon}^{+\varepsilon}\psi(x)dx$$
Il primo integrale è banale, mentre il terzo è nullo dato che per $\epsilon \rightarrow 0$, l'intervallo di integrazione diventa infinitesimo e la funzione è continua e limitata. Allora si ha
$$\lim\limits_{\varepsilon \rightarrow 0}\int_{-\varepsilon}^{+\varepsilon}V(x)\psi(x)dx=\frac{\hbar^{2}}{2m} \left(\frac{d\psi}{dx}\right)_{-\varepsilon}^{+\varepsilon}$$
Solitamente, anche questo integrale è nullo, dato che di solito $V(x)\psi(x)$ è continua e limitata al contorno, ma adesso l'integrale include la delta di Dirac e quindi ci dà
$$\lim\limits_{\varepsilon \rightarrow 0}\int_{-\varepsilon}^{+\varepsilon}-\alpha \delta(x)\psi(x)=-\alpha \psi(0)$$
e quindi
$$\left(\frac{d\psi}{dx}\right)_{-\varepsilon}^{+\varepsilon}=-\frac{2m \alpha}{\hbar^{2}}\psi(0)$$
Sostituendo l'effettiva derivata $B\kappa e^{-\kappa x}$ troviamo i due casi
$$\begin{cases}
-B\kappa e^{-\kappa \varepsilon} \rightarrow -B\kappa & \text{per }x>0 \\
B\kappa e^{-\kappa \varepsilon} \rightarrow B\kappa & \text{per }x<0
\end{cases}$$
e anche $\psi(0)=B$. Allora
$$\left(\frac{d\psi}{dx}\right)_{-\varepsilon}^{+\varepsilon}=-2B\kappa=-\frac{2m \alpha}{\hbar^{2}}B \quad \rightarrow \quad \kappa= \frac{m\alpha}{\hbar^{2}}$$
e invertendo la formula per $\kappa$ si trovano energie permesse
$$E=- \frac{\hbar^{2}\kappa^{2}}{2m}=- \frac{m\alpha^{2}}{2\hbar^{2}}$$

Ora normalizziamo $\psi$:
$$\int_{-\infty}^{+\infty}|\psi|^{2}dx=2|B|^{2}\int_{0}^{+\infty}e^{-2\kappa x}dx= \frac{|B|^{2}}{\kappa}=1 \quad \rightarrow \quad B=\sqrt{\kappa}=\frac{\sqrt{m\alpha}}{\hbar}$$
La funzione d'onda ha quindi la forma
$$\psi(x)=\frac{\sqrt{m\alpha}}{\hbar}e^{-m\alpha|x|/\hbar^{2}},\quad E=- \frac{m\alpha^{2}}{2\hbar^{2}}$$
Non è comparsa alcuna dipendenza da indici come nel caso, per esempio, della buca infinita, quindi esiste uno ed uno solo stato legato, con energia $E$.
### Stati liberi
Nella regione $x>0$, l'equazione di Schrödinger è
$$\frac{d^{2}\psi}{dx^{2}}=- \frac{2mE}{\hbar^{2}}\psi=-k^{2}\psi$$
con $k=\sqrt{2mE}/\hbar$. Questo è lo stesso caso della buca infinita. Le soluzioni generali nei casi $x>0$ e $x<0$ sono
$$\psi(x)=Ae^{ikx}+Be^{-ikx}\quad\text{e}\quad \psi(x)=Ce^{ikx}+De^{-ikx}$$
La continuità di $\psi$ obbliga ad avere
$$A+B=C+D\tag{1}$$
Mentre la continuità di $d\psi/dx$ ci dà
$$\begin{cases}
ik(Ce^{ik0^{+}}-De^{-ik0^{+}})=ik(C-D) & \text{per }x>0 \\
ik(Ae^{ik0^{-}}-Be^{-ik0^{-}})=ik(A-B) & \text{per }x<0
\end{cases}$$
Quindi
$$\left(\frac{d\psi}{dx}\right)_{-\varepsilon}^{+\varepsilon}=ik(C-D-A+B)=- \frac{2m\alpha}{\hbar^{2}}(A+B)$$
o scritta in un altro modo
$$C-D=A(1+2i\beta)-B(1-2i\beta)\quad\text{con}\quad\beta\equiv \frac{m\alpha}{\hbar^{2}k}\tag{2}$$
Ci troviamo in una situazione complicata: abbiamo due equazioni, la $(1)$ e la $(2)$, in quattro incognite. Cinque, se si conta anche $k$. Inoltre, lo stato non è normalizzabile. Cerchiamo allora il significato fisico di queste incognite.

Se accoppiati con il termine temporale $e^{-iEt/\hbar}$, i termini della forma $e^{ikx}$ danno luce ad un'onda propagante a $+x$, mentre $e^{-ikx}$ a onde propaganti a $-x$. Allora, $A$ è l'ampiezza dell'onda da $-\infty$ verso $0$ e $B$ è quella dell'onda da 0 verso $-\infty$. Analogamente, $C$ è l'ampiezza dell'onda da 0 verso $+\infty$ e $D$ quella dell'onda da $+\infty$ a 0.

![[Schema Costanti potenziale delta di Dirac|100%]]

Nel caso di una particella sola, le cose si semplificano. Se consideriamo una particella che si muove verso destra da $-\infty$, abbiamo
- $A$ è la costante dell'**onda incidente**.
- $B$ è la costante dell'**onda riflessa**.
- $C$ è la costante dell'**onda trasmessa**.
- $D=0$.
Usando conoscenze di ottica ondulatoria, si ha
$$B= \frac{i\beta}{1-i\beta}A, \quad C=\frac{1}{1-i\beta}A$$
La probabilità *relativa*[^1] che una particella incidente sia riflessa è
$$R\equiv \frac{|B|^{2}}{|A|^{2}}=\frac{\beta^{2}}{1+\beta^{2}}$$
mentre la probabilità che venga trasmessa è
$$T\equiv \frac{|C|^{2}}{|A|^{2}}=\frac{1}{1+\beta^{2}}$$
che sono rispettivamente il **coefficiente di riflessione** e di **trasmissione**[^2]. Come di norma, vale $R+T=1$. Sostituendo $\beta$ troviamo
$$R=\frac{1}{1+ \left(\frac{2\hbar^{2}E}{m\alpha^{2}}\right)},\quad T=\frac{1}{1+\left(\frac{m\alpha^{2}}{2\hbar^{2}E}\right)}$$
da cui possiamo intuire che più alta è l'energia, più alta è la probabilità di trasmissione.

C'è ancora il problema di fondo: nulla di tutto questo è normalizzabile e quindi *nessuno di questi stati può esistere singolarmente*. Possiamo però risolvere il problema come di norma: trovare la combinazione lineare di stati stazionari, che può invece esistere. Il problema è che risolvere il problema analiticamente è generalmente impossibile; si usano allora soluzioni numeriche al computer.

Va anche ricordato che una soluzione non-normalizzabile considera solo intervalli di energia (valori specifici non sono fisicamente realizzabili!), quindi $R$ e $T$ in realtà sono approssimazioni delle probabilità di riflessione e trasmissione per energie *vicine* ad $E$.
### Barriera di potenziale
Un ragionamento analogo può essere fatto per una barriera di potenziale della forma $V(x)=\alpha \delta(x)$. In questo caso, lo stato legato svanisce, ma le costanti $R$ e $T$ non cambiano, dato che dipendono solo da $\alpha^{2}$. Ciò significa che esiste una possibilità non nulla che la particella venga trasmessa attraverso una barriera di potenziale anche se l'energia della particella è minore del potenziale. Più alta è l'energia, più alta è la probabilità. Curiosamente, anche se l'energia della particella è superiore del potenziale, non è garantito che superi la barriera. Questo fenomeno si dice **[[tunneling quantistico]]**.

[^1]: La probabilità *assoluta* è data sempre da $|\Psi|^{2}$, ma qui non è normalizzabile, quindi non ha molto senso parlarne.
[^2]: Nel caso di un fascio di particelle, questi rappresentano la frazione di particelle che vengono mediamente riflesse e trasmesse.