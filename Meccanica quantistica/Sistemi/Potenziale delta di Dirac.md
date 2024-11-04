Consideriamo una [[Particella]] immersa in un [[potenziale]] della forma
$$V(x)=-\alpha \delta(x)$$
con $\alpha$ una costante positiva e $\delta(x)$ la [[delta di Dirac]]. Questo potenziale è una [[Buca infinita quantistica|buca infinita]] localizzata interamente nell'origine, a differenza della buca infinita vera e propria, che ha un'estensione spaziale. L'[[equazione di Schrödinger]] diventa
$$- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}} - \alpha\delta(x)\psi=E\psi$$
Per la definizione di delta di Dirac, possiamo ricavare sia [[stato|stati]] legati che liberi.
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
$$\boxed{E=- \frac{\hbar^{2}\kappa^{2}}{2m}=- \frac{m\alpha^{2}}{2\hbar^{2}}}$$

Ora normalizziamo $\psi$:
$$\int_{-\infty}^{+\infty}|\psi|^{2}dx=2|B|^{2}\int_{0}^{+\infty}e^{-2\kappa x}dx= \frac{|B|^{2}}{\kappa}=1 \quad \rightarrow \quad B=\sqrt{\kappa}=\frac{\sqrt{m\alpha}}{\hbar}$$
La funzione d'onda ha quindi la forma
$$\boxed{\psi(x)=\frac{\sqrt{m\alpha}}{\hbar}e^{-m\alpha|x|/\hbar^{2}}}$$
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
### Soluzione alternativa
Sappiamo che la delta di Dirac è una [[distribuzione]] singolare, ma sappiamo anche che integrare rimuove le singolarità. Infatti, integrando la delta di Dirac otteniamo la [[theta di Heaviside]], e se la integriamo di nuovo otteniamo una funzione senza singolarità. L'idea è quindi integrare due volte per ottenere una funzione liscia. Partiamo da
$$-  \frac{\hbar^{2}}{2m}\psi''_{E}(x)+\gamma \delta(x)\psi_{E}(x)=E\psi_{E}(x)$$
Allora estraendo $\psi''_{E}$
$$\psi''_{E}(x)=\frac{2m\gamma}{\hbar ^{2}}\delta(x)\psi_{E}(x)- \frac{2mE}{\hbar ^{2}}\psi_{E}(x)$$
In notazione di distribuzioni abbiamo
$$\delta_{x_{0}}[f]=f(x_{0})=\int_{-\infty}^{\infty} \delta(x-x_{0})f(x) \ dx $$
Allora se integriamo $\psi''_{E}$ in un intervallo $[-\varepsilon,\varepsilon]$ attorno all'origine abbiamo
$$\int _{-\varepsilon}^{\varepsilon}\psi''_{E}(x) \ dx =\psi'_{E}(\varepsilon)-\psi'_{E}(-\varepsilon)=\frac{2m\gamma}{\hbar ^{2}}\psi_{E}(0)- \frac{2mE}{\hbar ^{2}}\int_{-\varepsilon}^{\varepsilon}\psi_{E}(x)\ dx$$
usando il [[fundamental theorem of calculus|teorema fondamentale del calcolo]]. Andando al limite $\varepsilon\to 0^{+}$ e $-\varepsilon\to 0^{-}$, l'integrale svanisce e rimane
$$\psi_{E}'(0^{+})-\psi'_{E}(0^{-})=\frac{2m\gamma}{\hbar ^{2}}\psi_{E}(0)$$
Questa è una condizione di discontinuità sulla derivata. La soluzione generale di un'equazione differenziale lineare è una combinazione lineare di esponenziali complessi, che in termini fisici è una somma di [[plane wave|onde piane]], una a destra e una a sinistra della barriera di potenziale. A sinistra
$$\psi_{E}^{L}(x)=A_{L}e^{ikx}+B_{L}e^{-ikx}$$

Dove un'onda piana arriva da $-\infty$ e collide con la barriera (l'onda entrante) e che parte dalla barriera e va in direzione opposta, verso $-\infty$ (l'onda riflessa). A destra è analogo
$$\psi_{E}^{R}(x)=A_{R}e^{ikx}$$
ma in questo caso c'è solo un'onda che va a destra a partire dalla barriera (l'onda trasmessa). In queste equazioni,
$$k=\frac{\sqrt{ 2mE }}{\hbar}=\frac{p}{\hbar}$$
Derivando $\psi_{E}^{R}(x)$ e $\psi_{E}^{L}(x)$ e valutandole in $0^{+}$ e $0^{-}$ si trovano condizioni al contorno
$$\psi'_{E}(0^{+})=ikA_{R},\qquad \psi'_{E}(0^{-})=ik(A_{L}-B_{R})$$
ma deve anche valere $\psi_{E}^{L}(0)=\psi_{E}^{R}(0)$ (la derivata è discontinua, ma la funzione in sé no). Ciò implica
$$A_{L}+B_{L}=A_{R}\tag{1}$$
Mettendo queste cose insieme abbiamo
$$ikA_{R}-ik(A_{L}-B_{L})=\frac{2m\gamma}{\hbar ^{2}}A_{R}$$
Allora
$$-A_{R}+A_{L}-B_{L}= \frac{2mi\gamma}{\hbar ^{2}k}A_{R}$$
$$A_{L}-B_{L}=A_{R}+ \frac{2mi\gamma}{\hbar ^{2}k}A_{R}=A_{R}\left( 1+ \frac{2mi\gamma}{\hbar ^{2}k} \right)\tag{2}$$
Quindi dividendo $(1)$ e $(2)$ per $A_{L}$, valgono le condizioni al contorno per le costanti
$$\boxed{\begin{align}
1+ \frac{B_{L}}{A_{L}}&=\frac{A_{R}}{A_{L}} \\
1- \frac{B_{L}}{A_{L}} &= \left( 1+ \frac{2mi\gamma}{\hbar ^{2}k} \right) \frac{A_{R}}{A_{L}}
\end{align}}$$
Sommandole possiamo anche trovare un rapporto tra onda entrante $A_{L}$ e trasmessa $A_{R}$:
$$2=2\left( 1+ \frac{mi\gamma}{\hbar ^{2}k} \right) \frac{A_{R}}{A_{L}}\quad\Rightarrow \quad\boxed{\frac{A_{R}}{A_{L}}= \frac{1}{1+ \frac{mi\gamma}{\hbar ^{2}k}}}$$
e sottraendole anche tra onda entrante $A_{L}$ e riflessa $B_{L}$:
$$2 \frac{B_{L}}{A_{L}}=- \frac{2mi\gamma}{\hbar ^{2}k} \frac{A_{R}}{A_{L}}\quad\Rightarrow \quad\boxed{\frac{B_{L}}{A_{L}}=-i \frac{m\gamma}{\hbar ^{2}k+im\gamma}}$$
Quindi sapendo l'onda entrante $A_{L}$ (non normalizzabile), possiamo trovare anche quella riflessa e quella trasmessa. Come ultima cosa, possiamo raccordare funzione d'onda sinistra e destra con la theta di Heaviside $\Theta$:
$$\boxed{\psi_{E}(x)=A_{L}\left( e^{ikx}- i \frac{m\gamma}{\hbar ^{2}k-im\gamma}e^{-ikx} \right)\Theta(-x)+A_{L} \frac{\hbar^{2}k}{\hbar ^{2}k+im\gamma}\Theta(x)}$$
Queste sono le [[Equazione agli autovalori|autofunzioni]] di stato di una particella soggetta ad una barriera a delta di Dirac ad energia $E$. Esse formano un sistema continuo e quindi non sono normalizzabili. Rappresentano stati liberi. $A_{L}$ non è una costante di normalizzazione (l'onda non è normalizzabile) ma è una funzione che dà [[ampiezza di probabilità]].

Dato che stiamo parlando di onde, è interessante vedere qual è la [[corrente di probabilità]] del sistema. Dato che $\psi$ è nota, la [[Probability distribution|distribuzione di probabilità]] è $\lvert \psi \rvert^{2}$. Per arrivare alla corrente, dobbiamo moltiplicarla per la velocità di propagazione della corrente (cioè della particella), che in questo caso proviene da $k=p/\hbar$ ed è $v=\hbar k/m$. Allora
$$J_\text{in}=\lvert A_{L} \rvert ^{2} \frac{\hbar k}{m},\qquad J_\text{rif}=\lvert A_{L} \rvert ^{2} \frac{m^{2}\gamma ^{2}}{\hbar^{4}k^{2}+m^{2}\gamma ^{2}} \frac{\hbar k}{m},\qquad J_\text{tras}=\lvert A_{L} \rvert ^{2} \frac{\hbar^{4}k^{2}}{\hbar^{4}k^{2}+m^{2}\gamma ^{2}} \frac{\hbar k}{m}$$
#### Buca di potenziale
Consideriamo ora il caso inverso, in cui il potenziale è $V=-\gamma \delta(x)$. In questo caso, è possibile anche avere energie totali negative $E=T-V<0$, con $T$ l'[[kinetic energy|energia cinetica]], che portano a stati legati. Se $E<0$ abbiamo
$$k=\frac{\sqrt{ 2mE }}{\hbar}=\frac{i\sqrt{ 2m\lvert E \rvert  }}{\hbar}$$
da cui
$$\hbar^{4}k^{2}+m^{2}\gamma ^{2}=\hbar^{4} \frac{2m\lvert E \rvert}{\hbar ^{2}}+m^{2}\gamma ^{2}=2m\hbar ^{2}\left( -\lvert E \rvert + \frac{m\gamma ^{2}}{2\hbar ^{2}} \right)$$
e estraendo $\lvert E \rvert$:
$$\lvert E \rvert =\frac{m\gamma ^{2}}{2\hbar ^{2}}$$
In questo caso, l'equazione di Schrödinger è
$$-  \frac{\hbar^{2}}{2m} \psi_{E}''(x)-\gamma \delta(x)\psi_{E}(x)=-\lvert E \rvert \psi_{E}(x)$$
Estraiamo la derivata seconda
$$\psi_{E}''(x)=- \frac{2m}{\hbar ^{2}}\gamma \delta(x)\psi_{E}(x)+ \frac{2m\lvert E \rvert}{\hbar ^{2}}\psi_{E}(x) $$
e integriamo in $[-\varepsilon,\varepsilon]$ come prima
$$\int _{-\varepsilon}^{\varepsilon}\psi''(x) \ dx =\psi'(\varepsilon)-\psi'(-\varepsilon)$$
Mandando $\varepsilon\to 0$ si ha
$$\psi'_{E}(0^{+})-\psi'_{E}(0^{-})=- \frac{2m\gamma}{\hbar ^{2}}\psi_{E}(0)$$
cioè il salto della derivata, sempre con la continuità della funzione $\psi_{E}(0^{+})=\psi_{E}(0^{-})$. Finora tutto come prima. La differenza inizia quando subentrano le energie negative. Per essere uno stato legato nella buca, l'autofunzione deve essere a quadrato sommabile. Consideriamo l'equazione a destra dell'origine (in $x>0$) o anche a sinistra (in $x<0$). In questi casi, il termine con la delta svanisce e abbiamo
$$\begin{align}
\text{R}:x>0\quad&- \frac{\hbar^{2}}{2m}\psi''_{E}(x)=-\lvert E \rvert \psi_{E}(x) \\
\text{L}:x<0\quad&- \frac{\hbar^{2}}{2m}\psi''_{E}(x)=-\lvert E \rvert \psi_{E}(x)
\end{align}$$
Allora la funzione in generale sarà un esponenziale (per ansatz generale da equazione differenziale, come prima). Per decidere il segno degli esponenti, sfruttiamo il fatto che devono essere funzioni a quadrato sommabile:
$$\psi_{E}(x)=\begin{cases}
\psi_{E}^{L}(x)=A_{L}e^{(i/\hbar)\sqrt{ 2m\lvert E \rvert  }x} \\
\psi_{E}^{R}(x)=A_{R}e^{-(i/\hbar)\sqrt{ 2m\lvert E \rvert  }x}
\end{cases}$$
Ora sfruttiamo le condizioni al contorno di prima. La continuità della funzione ci dà $A_{L}=A_{R}=A=\psi_{E}(0)$. Derivando le equazioni prima abbiamo
$$\begin{align}
\psi'_{E}(0^{+})&=- \frac{i}{\hbar}\sqrt{ 2m\lvert E \rvert  }A \\
\psi'_{E}(0^{-})&=\frac{i}{\hbar}\sqrt{ 2m\lvert E \rvert  }A
\end{align}$$
e paragonandole alla condizione sulla derivata troviamo
$$\psi'_{E}(0^{+})-\psi'_{E}(0^{-})=-\frac{2m\gamma}{\hbar ^{2}}A=- \frac{2}{\hbar}\sqrt{ 2m\lvert E \rvert  }A$$
da cui troviamo
$$\frac{m\gamma}{\hbar}=\sqrt{ 2m\lvert E \rvert  }\quad\Rightarrow \quad \boxed{\lvert E \rvert =\frac{m\gamma ^{2}}{2\hbar ^{2}}}$$
Ora che sappiamo sia gli autovalori che le autofunzioni, possiamo raccordare sinistra e destra una singola funzione d'onda totale:
$$\psi_{\lvert E \rvert }(x)=Ae^{-(i/\hbar)\sqrt{ 2m\lvert E \rvert  }\,\lvert x \rvert }$$
dove abbiamo sfruttato la simmetria del sistema per usare $\lvert x \rvert$. Ci manca solo da trovare il valore della costante di normalizzazione $A$:
$$1=\int_{-\infty}^{\infty} \lvert \psi_{-\lvert E \rvert }(x) \rvert ^{2} \ dx =2\lvert A \rvert ^{2}\int _{0}^{\infty}e^{- 2m\gamma/\hbar ^{2}x} \ dx =\frac{2\hbar^{2}}{2m\gamma}\underbrace{ \int _{0}^{\infty} e^{-t} \ dt }_{ 1 }= \frac{\hbar^{2}}{m\gamma}$$
Allora
$$A=\sqrt{ \frac{m\gamma}{\hbar ^{2}} }$$
e mettendo tutto insieme
$$\boxed{\psi_{\lvert E \rvert }(x)\sqrt{ \frac{m\gamma}{\hbar ^{2}} }e^{-(i/\hbar)\sqrt{ 2m\lvert E \rvert  }\,\lvert x \rvert }}$$
Dato che é uno stato legato, non c'è corrente di probabilità.

[^1]: La probabilità *assoluta* è data sempre da $|\Psi|^{2}$, ma qui non è normalizzabile, quindi non ha molto senso parlarne.
[^2]: Nel caso di un fascio di particelle, questi rappresentano la frazione di particelle che vengono mediamente riflesse e trasmesse.