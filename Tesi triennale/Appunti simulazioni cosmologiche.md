Una simulazione cosmologica parte dal **campo di densità**. Il campo di densità è un [[Scalar field|campo scalare]] che descrive la densità di materia in ogni punto dello [[Spacetime|spaziotempo]], $\rho(\mathbf{x},t)$. Questo è importante perché l'attrazione gravitazionale dipende dalle differenze di densità: regioni più dense attraggono regioni meno dense. Similarmente, regioni a pari densità sono in globalmente in equilibrio (si attraggono con pari forza e stanno tutto sommato ferme, un po' come due gas perfetti a pari densità).

Il campo di densità dell'universo primordiale era quasi costante, ma c'erano delle *leggere* imperfezioni. Certe regioni erano *molto leggermente* più dense di altre; questo è tutto ciò che fu necessario per permettere alla gravità di attivare la dinamica dell'universo, anche se lentamente. Queste variazioni si chiamano **fluttuazioni di densità** $\delta(\mathbf{x},t)$ e sono generalmente considerate [[random]] all'inizio dell'universo. Nonostante non possiamo sapere esattamente che realizzazione delle fluttuazioni random aveva il nostro universo all'inizio, conosciamo le proprietà statistiche della distribuzione grazie al CMB, che è una proiezione delle fluttuazioni di densità primordiali all'epoca della ricombinazione (380,000 anni dopo il Big Bang). Di conseguenza, possiamo sapere quali campi di fluttuazioni iniziali sono *possibili*, ossia tutte le realizzazioni con proprietà statistiche che sono d'accordo con le osservazione sperimentali del CMB.

Le proprietà statistiche sono date scomponendo il campo di densità in una [[Trasformata di Fourier]] nello spazio, quindi passando da distanze $x$ a frequenze spaziali $k$. Come di norma, questo ci dà un insieme (infinito continuo) di onde il cui integrale su tutte le frequenze ci ridà il campo di densità. Chiamiamo **spettro di potenza** $P(k)$ la funzione che ci dice la [[Amplitude|ampiezza]] media (la "potenza") di queste onde in base alla loro frequenza spaziale. In pratica, $P(k)$ ci dice quanto importanti sono le fluttuazioni ad una certa scala di distanza fisica ed è ciò che prediciamo osservando il CMB. Le misure sperimentali sono in buonissimo accordo con le predizioni teoriche dei modelli odierni dell'universo primordiale.

All'atto pratico, la simulazione segue l'evoluzione della materia oscura non-collisionale e materia barionica collisionale secondo la loro interazione gravitazionale, a partire dalle condizioni iniziali e integrando numericamente campi di densità e velocità. Le condizioni al contorno sono ben specificate da osservazioni sperimentali, quindi la difficoltà primaria è seguire la dinamica gravitazionale e fluidodinamica dei gas in modo fedele.

La dinamica della materia oscura è data dall'**equazione di Boltzmann non-collisionale** (o **equazione di Vlasov**), che ha in input spazio e velocità (6 dimensioni). L'alta dimensionalità rende l'integrazione numerica a scala realistica praticamente impossibile; si usano spesso tecniche di Monte Carlo per approssimare. Inoltre, si trova che l'equazione di Vlasov è equivalente ad un insieme di *equazioni caratteristiche* la cui soluzione simultanea è equivalente a quella di Vlasov. Tipicamente si risolve un sottoinsieme di queste equazioni caratteristiche su un set di $N$ corpi.

La dinamica della materia barionica è fortemente collisionale e si simula dunque usando tecniche standard per la fluidodinamica.

Parametri cruciali per l'accuratezza di una simulazione cosmologica sono
- la risoluzione di massa, perché la minima massa simulabile rappresenta la più piccola fonte di gravità simulabile individualmente.
- la risoluzione spaziale, perché è la grandezza minima di una cella simulata e quindi il grado di informazione che si perde per quanto riguarda la distribuzione nello spazio.

La gravità e i fattori fluidodinamici sono gli aspetti più importanti della simulazione, ma ve ne sono altri. Ad esempio, la formazione stellare e l'accrescimento dei buchi neri, che vanno anch'essi simulati per essere corretti anche nei dettagli.
## Metodi
Nel contesto dei cluster di galassie, la gerarchia è importante. Oggetti più piccoli collassano prima, poi più grandi, formando strutture di crescente scala. Questi oggetti più piccoli determinano la meccanica di quelli più grandi, con il loro accrescimento, distruzione e fusione. Gli eventi di fusione in particolare creano shock, turbolenze e accelerazioni relativistiche che ridistribuiscono o amplificano campi magnetici e l'accelerazione di raggi cosmici, entrambi fattori secondari ma importanti nella dinamica interna di un cluster. Questa dinamica è altamente nonlineare e dunque inaccessibile mediante la teoria su carta e penna; servono simulazioni numeriche.

Il metodo usato per compiere la simulazione dipende da cosa si simula e che richieste si hanno. In particolare, è un baratto tra grandezza della regione simulata e risoluzione della cella più piccola. Grandezze tipiche sono:
- di regione:
	- megaparsec per una galassia
	- decine o centinaia di megaparsec per una popolazione di galassie
	- diverse centinaia di megaparsec per un cluster di galassie
- di risoluzione:
	- tra i $10^{5}$ e i $10^{10}\ M_{\odot}$ di massa in base agli oggetti d'interesse.
	- tra qualche centinaia di parsec e alcuni kiloparsec di spazio, rispettivamente per singole galassie e box cosmologici
### N-body
La simulazione più semplice possibile (in linea di principio) è una $N$-body. Prendi $N$ corpi, calcola l'attrazione gravitazionale fra di loro e risolvi numericamente le equazioni del moto. È una simulazione puramente gravitazione e dunque di particolare interesse per la CDM. La CDM è rappresentata come un fluido non-collisionale non-relativistico ("cold") di particelle di massa $m$, posizione $\mathbf{x}$ and momento $\mathbf{p}$. Per rispettare l'espansione dell'universo a fattore di scala $a=(1+z)^{-1}$, si usano coordinate comoventi. In questo modello, la distribuzione nello spazio delle fasi $f(\mathbf{x},\mathbf{p},t)$ è dato dall'**equazione di Vlasov**:
$$\boxed{\frac{ \partial f }{ \partial t } + \frac{\mathbf{p}}{ma^{2}}\cdot\nabla f-m\nabla \Phi\cdot \frac{ \partial f }{ \partial \mathbf{p} } =0}$$
accoppiata all'equazione di Poisson del potenziale gravitazionale $\Phi$:
$$\boxed{\nabla ^{2}\Phi(\mathbf{x},t)=4\pi Ga^{2} [\rho(\mathbf{x},t)-\bar{\rho}(t)]  }$$

> [!info]- Notazione
> Il gradiente è da assumersi rispetto alle sole coordinate spaziali:
> $$\nabla f(\mathbf{x},\mathbf{p},t)\equiv \frac{ \partial f(\mathbf{x},\mathbf{p},t) }{ \partial \mathbf{x} } \equiv\left( \frac{ \partial f }{ \partial x } ,\frac{ \partial f }{ \partial y } ,\frac{ \partial f }{ \partial z }  \right)$$
> La derivata rispetto ad un vettore è un'abbreviazione per il vettore di derivate parziali di ogni componente del vettore:
> $$\frac{ \partial f(\mathbf{x},\mathbf{p},t) }{ \partial \mathbf{p} } \equiv\left( \frac{ \partial f }{ \partial p_{x} } ,\frac{ \partial f }{ \partial p_{y} } ,\frac{ \partial f }{ \partial p_{z} }  \right)$$

Qui $\bar{\rho}(t)$ è la densità di sfondo al tempo $t$. La densità propria nel punto $\mathbf{x}$ è
$$\rho(\mathbf{x},t)=\int f(\mathbf{x},\mathbf{p},t)\ d^{3}p$$
Il momento è esprimibile come $\mathbf{p}=ma^{2}\dot{\mathbf{x}}$. Questo set di equazioni è tipicamente risolto campionando $N$ particelle traccianti nello spazio delle fasi, sotto l'assunzione che il comportamento di queste particle sia indicativo delle altre.

L'equazione è risolvibile mediante le equazioni del moto delle singole particelle in coordinate comoventi:
$$\frac{d\mathbf{p}}{dt}=-m\nabla \Phi,\qquad \frac{d\mathbf{x}}{dt}=\frac{\mathbf{p}}{ma^{2}}$$
Introducendo la **velocità propria peculiare** $\mathbf{v}=a \dot{\mathbf{x}}$, queste possono essere scritte come
$$\frac{d\mathbf{v}}{dt}+\mathbf{v} \frac{\dot{a}}{a}=- \frac{\nabla \Phi}{a}$$
dove la derivata del fattore scala è derivabile dalle equazioni di Friedmann
$$\dot{a}=H_{0}\sqrt{ 1+\Omega_{0}(a^{-1}-1)+\Omega_{\Lambda}(a^{2}-1) }$$
dove abbiamo assunto che l'energia oscura sia equivalente ad una costante cosmologica $\Lambda$.
#### Somma diretta
La soluzione più facile e diretta è sommare il contributo di ogni corpo al potenziale gravitazionale
$$\Phi(\mathbf{r})=-G\sum_{i=1}^{N-1} \frac{m_{i}}{\sqrt{ \lvert \mathbf{r}-\mathbf{r}_{i} \rvert ^{2}+\varepsilon ^{2} }}$$
$\varepsilon$ verrà spiegato in un attimo. In teoria, questo è l'esatto potenziale Newtoniano che genera la dinamica del sistema. In pratica, le "particelle" sono in realtà regioni di spazio contenenti un enorme numero di corpi gravitanti, quindi in realtà possiamo parlare solo di proprietà statistiche di ciascuna "particella." A questo scopo, si introduce l'**attenuazione gravitazionale** $\varepsilon$ per rendere più liscia l'interazione tra due "particelle." Tipicamente $\varepsilon$ si sceglie essere tra $1/20$ e $1/50$ della distanza media tra le particelle.

La somma diretta è il metodo più accurato, ma è anche quello più computazionalmente costoso (è $O(N^{2})$). Si usa per le simulazioni che richiedono precisione superiore. Esistono ASIC il cui scopo è calcolare questa somma diretta (**Gravity Pipe** a.k.a. **GRAPE**) e può essere usato su GPU.
#### Alberi
Un metodo molto comune per risolvere l'$N$-body in modo approssimato è usare un'espansione al multipolo gerarchica; l'algoritmo che lo fa è tipicamente detto **ad albero**. L'idea è raggruppare particelle distanti in celle e tratta la loro gravità come una singola forza di multipolo. Anziché necessitare $N-1$ operazioni di somma per particella come prima, le particelle distanti ora sono raggruppati in celle, diminuendo enormemente il numero di step. In pratica, questo riduce la complessità algoritmica a circa $O(N\log N)$ per distribuzioni di particelle omogenee (e.g. all'inizio della simulazione) e peggiora progressivamente a $O(N^{2})$ man mano che la distribuzione diventa disomogenea (e.g. molte particelle vicine, poche lontane, alla fine della simulazione).

In pratica, la suddivisione dello spazio è ottenuta dividendo ricorsivamente lo spazio. Si parte con un cubo che copre l'intera distribuzione. Il cubo è poi suddiviso in otto cubetti più piccoli di spigolo dimezzato. Si ripete ricorsivamente finché un cubetto figlio non contiene una sola particella. L'algoritmo scende dalla radice livello per livello, calcolando le forze per ogni strato. Se la forza sarebbe sufficientemente accurata (secondo qualche misura), si ferma e la usa, altrimenti scende di un livello e ricontrolla di nuovo finché non ne ha una buona. Tipicamente come misura si usa l'apertura angolare del nodo cubico in questione rispetto alla particella in esame.
#### Particle-Mesh (PM)
I metodi di **Particle-Mesh** trattano la forza come un campo definito su una maglia discreta. Gli operatori differenziali sono sostituiti da differenze finite. I valori alle effettive posizioni delle particelle sono ottenuti interpolando i valori ottenuti ai punti della maglia. Gli algoritmi PM sono molto più veloci, scalando come $N+N_{g}\log N_{g}$ con $N_{g}$ il numero di punti della maglia. Sono più limitati in risoluzione rispetto ad altri metodi, dato che è decisa a tavolino da $N_{g}$, che a sua volta dipende principalmente dalla memoria dell'hardware.

Sono migliorati da tecniche di **Adaptive Mesh Refinement** (**AMR**), nelle quali l'equazione di Poisson per $\Phi$ può essere considerata come un problema con condizione al contorno di Dirichlet, per i quali le condizioni sono ottenute interpolando il potenziale gravitazionale dalla maglia genitore, creando maglie ricorsive simili ai metodi ad albero. Queste maglie possono avere forme arbitrarie, il che pone limiti sui risolutori di PDE che possono essere usati.
#### Ibridi
Esistono metodi ibridi che combinano alberi e particle-mesh. Nei metodi **TreePM**, il potenziale è diviso nello spazio di Fourier in due componenti: lungo e corto raggio, $\Phi_{\mathbf{k}}=\Phi_{\mathbf{k}}^{\text{long}}+\Phi_{\mathbf{k}}^{\text{short}}$, dove $\Phi_{\mathbf{k}}^{\text{long}}=\Phi_{\mathbf{k}}e^{-\mathbf{k}r_{s}^{2}}$ e $r_{s}$ descrive la scala spaziale della suddivisione. Il potenziale a lungo raggio può essere calcolato molto efficientemente con metodi PM. Il potenziale a corto raggio può essere risolto in spazio reale notando che se $r_{s}\ll L$ (con $L$ lo spigolo della regione di simulazione), la parte short della soluzione in spazio reale dell'equazione di Poisson è
$$\Phi^{\text{short}}(\mathbf{x})=-G\sum_{i=1}^{N} \frac{m_{i}}{r_{i}}\text{erf}\left( \frac{r_{i}}{2r_{s}} \right)$$
dove $r_{i}=\lvert \mathbf{x}-\mathbf{r}_{i} \rvert$ è la distanza della $i$-esima particella dal punto $\mathbf{x}$ e $\text{erf}$ è la funzione errore (distribuzione cumulativa della Gaussiana). Il potenziale short può essere calcolato con un metodo ad albero, fino al cutoff di distanza.

I metodi ibridi hanno miglioramenti sostanziali su entrambi i metodi di cui sono composti, sia in termini di risoluzioni che di performance.

Il metodo $P^{3}M$ è una versione più vecchia, dove anziché usare un metodo ad albero per il potenziale short, usava la somma diretta. Di fatto, è un caso specifico di TreePM dato che l'albero si riduce a somma diretta se si richiede massima precisione.
#### Integrazione
Il timestep è tipicamente deciso con la regola
$$\Delta t=\alpha \sqrt{ \varepsilon/\lvert \mathbf{a} \rvert  }$$
dove $\mathbf{a}$ è la velocità ottenuta nel precedente timestep, $\varepsilon$ è la scala di lunghezza, tipicamente associata all'attenuazione gravitazionale, e $\alpha$ è un parametro di [[Tolerance|tolleranza]]. Per il metodi, si usano cose standard; vedi [[Numerical integration]].
#### Condizioni iniziali
Le condizioni iniziali sono un punto chiave. In simulazioni cosmologiche, le condizioni iniziali partono da un campo random gaussiano di fluttuazioni di densità. Questo campo random è descritto interamente dallo spettro di potenza, la cui forma analitica è motivata da parametri cosmologici e la natura della materia oscura.

Per generare le condizioni iniziali, si genera un set di numeri complessi con fase $\phi$ random e ampiezza anche random secondo una normale con varianza data dallo spettro desiderato. Questo set può essere ottenuto campionando due numeri random $\phi \in]0,1]$ e $A\in]0,1]$ per ogni punto in $k$-spazio:
$$\hat{\delta}_{\mathbf{k}}=\sqrt{ -2P(\lvert \mathbf{k} \rvert )\ln(A) }\ e^{i2\pi \phi}$$
Per ottenere il campo di perturbazioni di questa distribuzione, bisogna trovare il potenziale gravitazionale $\Phi(\mathbf{q})$ su una griglia $\mathbf{q}$ in spazio reale mediante una trasformata di Fourier
$$\Phi(\mathbf{q})=\sum_{k} \frac{\hat{\delta}_{\mathbf{k}}}{\lvert \mathbf{k} \rvert ^{2}}e^{i\mathbf{k}\cdot \mathbf{q}}$$
Si usa poi l'**approssimazione di Zel'dovich** per trovare le posizioni e velocità iniziali delle particelle mediante
$$\mathbf{x}=\mathbf{q}-D^{+}(z)\Phi(\mathbf{q}),\qquad \mathbf{v}=\dot{D}^{+}(z)\nabla \Phi(\mathbf{q})$$
$D^{+}(z)$ indica il fattore di crescita cosmologica lineare a redshift iniziale $z$.
##### Risoluzione
La risoluzione necessaria dipende molto dai dati che si vogliono ottenere dalla simulazione.
### Idrodinamica
A differenza della DM, che è non-collisionale, la materia barionica è collisionale ed è ben rappresentata come un fluido ideale. In particolare, l'evoluzione del fluido si segue risolvendo le **equazioni di Eulero**, qui riportate in forma Lagrangiana:
$$\begin{align}
&\frac{d\mathbf{v}}{dt}=- \frac{\nabla P}{\rho}-\nabla \Phi \\
&\frac{d\rho}{dt}+\rho \nabla\cdot\mathbf{v}=0 \\
& \frac{du}{dt}=- \frac{P}{\rho}\nabla\cdot \mathbf{v} - n^{2}\frac{\Lambda(u,\rho)}{\rho}
\end{align}$$
Rispettivamente sono:
1. l'equazione del momento
2. l'equazione di continuità di massa
3.  la prima legge di termodinamica

Queste sono chiuse da un'equazione di stato che lega la pressione $P$ alla densità di massa $\rho$ e l'energia interna per unità di massa $u$. Nel caso di un gas monatomico ideale, questa è $P=(\gamma-1)\rho u$, con indice politropico $\gamma=5/3$. La funzione $\Lambda(u,\rho)$ è una funzione di raffreddamento che descrive perdite termiche per radiazione e $n$ è la densità di numero del gas.

Data la forte nonlinearità della materia a scala cosmologica, si ergono due sfide che tipicamente non sono così problematiche nelle simulazioni idrodinamiche tipiche. Una è il moto estremamente supersonico attorno ai picchi di densità sviluppati da instabilità gravitazionali. Questo porta a discontinuità da shock piuttosto intense entro strutture complesse altrimenti lisce. L'altra è la presenza di un range dinamico enorme sia nello spazio che nel tempo, così come nelle quantità del gas. Per esempio, le scale di lunghezza nella struttura gerarchia della distribuzione di galassie vanno dai pochi kiloparsec di una singola galassia alle decine di megaparsec di ICM interno ai cluster.

Risolvere materia barionica collisionale e materia oscura non-collisionale in contemporanea è un problema considerevole. I metodi di risoluzioni si dividono in due categorie:
1. metodi a particelle, che discretizzano la massa
2. metodi a griglia, che discretizzano lo spazio
#### Metodi a griglia (Euleriani)
Il set di equazioni di Eulero in forma Euleriana per un universo in espansione è
$$\begin{align}
&\frac{ \partial \mathbf{v} }{ \partial t } + \frac{1}{a}(\mathbf{v}\cdot \nabla)\mathbf{v}+ \frac{\dot{a}}{a}\mathbf{v}=- \frac{1}{a\rho}\nabla P- \frac{1}{a}\nabla \Phi \\
& \frac{ \partial \rho }{ \partial t } + \frac{3\dot{a}}{a}\rho+ \frac{1}{a}\nabla \cdot(\rho \mathbf{v})=0 \\
&\frac{ \partial  }{ \partial t } (\rho u)+ \frac{1}{a}\mathbf{v}\cdot \nabla(\rho u)=-(\rho u+P)\left( \frac{1}{a}\nabla \cdot \mathbf{v} + 3 \frac{\dot{a}}{a}\right)
\end{align}$$
Il termine a destra della terza equazione rappresenta il lavoro dell'espansione, oltre a quello usuale $PdV$. I metodi a griglia risolvono queste equazioni basandosi su una griglia più o meno strutturata che rappresenta il fluido.

Si distinguono **variabili primitive**, che determinano la termodinamica (e.g. $\rho$, $\mathbf{v}$ o $P$) and **variabili conservative** che definiscono le leggi di conservazione (e.g. $\rho$, $\rho \mathbf{v}$ o $\rho u$).

Data la complessità delle equazioni in gioco, metodi a differenza centrale tipo quelli in [[Numerical integration]] cadono a pezzi alla prima comparsa di discontinuità. Se usati, si usa una viscosità virtuale per simulare gli shock. Questi metodi sono accurati solo al primo ordine. Approcci più moderni usano schemi a ricostruzione che tengono anche conto di celle vicine oltre per ricostruire il campo in ogni cella, in particolare i valori al contorno delle celle. Le celle extra usate in questa stima si chiamano **stencil**. Tre esempi di schemi, ad accuratezza crescente, sono **piecewise constant method** (**PCM**), **piecewise linear method** (**PLM**) e **piecewise parabolic method** (**PPM**). Ne esistono anche di ordine ancora maggiore. Il metodo decide come ottenere la funzione di ricostruzione $f_{n,u}(x)$ che viene poi integrata sulla cella e poi divisa per il volume della cella per ottenere una stima $\hat{u}_{n}$ migliore del valore rispetto ad una semplice differenza centrale $u_{n}$:
$$\hat{u}_{n}=\int_{x_{n}-0.5}^{x_{n}+0.5}f_{n,u}(x)dx$$
È possibile anche aggiungere vincoli aggiuntivi alla ricostruzione per evitare oscillazioni. Per esempio, in PLM si aggiungono **slope limiters** che impediscono alla derivata (di fatto: differenza finita) di $f_{n,u}$ di eccedere certi valori. In PPM, prendono la forma di vincoli aggiuntivi nei parametri per trovare il polinomio che fitta meglio l'andamento di $u$. Metodi di ricostruzione moderni usano almeno 5 celle di stencil e hanno proprietà utili implementate come garanzie nella preservazione della monotonicità.

Per ogni ricostruzione $f_{n,u}$ è possibile definire un **indicatore di liscezza** $S_{n}^{m}$. Questa metrica è utile per esempio per poter creare più ricostruzioni per la stessa cella e poi selezionare quella con liscezza minore. Questo migliora la stabilità attorno a discontinuità e sopprime le oscillazioni. Questo metodo si chiama **essentially non-oscillatory methods** (**ENO methods**). Un metodo più raffinato è prendere la media pesata di tutte le ricostruzioni, i cui pesi sono definiti in base alla liscezza. Questo metodo si chiama **weighted essentially non-oscillatory methods** (**WENO methods**).

Una volta ricostruiti i valori al contorno, si ottengono discontinuità ad ogni cella. Queste discontinuità sono legate fra loro in una singola funzione continua risolvendo il **problema di Riemann**, ossia determinare l'evoluzione di due pezzi costanti di una funzione separate da una discontinuità. Questo può essere fatto sia analiticamente che numericamente, ed esistono numerosi metodi per farlo. Una volta risolto, i flussi attraverso i bordi delle celle possono essere usati per aggiornare il valore di $u$ in ogni cella.
#### Metodi a particelle (Lagrangiani)
I metodi a particelle consistono in varianti di idrodinamica a particelle lisciate (**smoothed particle hydrodynamics**, **SPH**). I metodi SPH risolvono le equazioni di Eulero in forma Lagrangiana. Hanno risoluzione buona in regioni ad alta densità, ma scarsa in regioni a bassa densità. Hanno anche problemi in zone con shock a causa dell'aggiunta di viscosità artificiale piuttosto alta e in generale non si comportano bene in presenza di instabilità dinamiche. Nonostante tutto, la loro adattività innata è sufficiente a compensare queste mancanze e dunque sono i metodi più usati in idrodinamica numerica cosmologica.

L'idea di base è discretizzare il fluido in elementi di massa (i.e. particelle) anziché elementi di volume come in una griglia. Di conseguenza, la risoluzione spaziale si adatta automaticamente in base allo stato fisico della simulazione: oggetti collassati avranno naturalmente più particelle vicine e quindi migliore risoluzione spaziale.

L'idea di base è rappresentare quantità $A(\mathbf{x})$ su un fluido continuo mediante una media lisciata tramite un kernel $W(\mathbf{x},h)$. Questa è una funzione normalizzata su $x$ ($\int W(\mathbf{x},h)d\mathbf{x}=1$) che rappresenta come viene lisciata $A$ su una distanza $h$. La media di $A$ viene dunque definita come un **kernel density estimate**
$$\langle A(\mathbf{x}) \rangle =\int W(\mathbf{x}-\mathbf{x}',h)A(\mathbf{x}')d\mathbf{x}'$$
Il kernel $W$ tende ad una delta di Dirac man mano che $h$ tende a 0, ossia $\lim_{ h \to 0 }W(\mathbf{x},h)=\delta(\mathbf{x})$. Questa funzione è poi scritta in base alle coordinate discrete $\mathbf{x}_{i}$ delle particelle come una somma anziché un integrale. Le derivate di $\langle A_{i} \rangle$ a loro volta diventano somme discrete. Il kernel è tipicamente scelto come la spline $B_{2}$ perché si trova essere la scelta ottimale nella maggioranza delle situazioni. In casi speciali esistono altre scelte.

Sviluppando questo metodo si trova che l'equazione di Eulero può essere scritta come
$$\frac{d\mathbf{v}_{i}}{dt}=-\sum_{j=1}^{N-1} -m_{j}\left( \frac{P_{j}}{\rho_{j}^{2}}+ \frac{P_{i}}{\rho_{i}^{2}}+\Pi_{ij} \right)\nabla_{i}W(\mathbf{x}_{i}-\mathbf{x}_{j},h)$$
dove $\Pi_{ij}$ è un termine di **viscosità artificiale**, che serve per descrivere shock anche in questo schema discretizzato. Esistono studi fatti su che forma dovrebbe avere $\Pi_{ij}$ (e.g. Monaghan & Gingold 1983 o Monaghan 1997). La prima legge della termodinamica può anche essere scritta come
$$\frac{du_{i}}{dt}=\frac{1}{2}\sum_{j=1}^{N-1} m_{j}\left( \frac{P_{j}}{\rho_{j}^{2}}+ \frac{P_{i}}{\rho_{i}^{2}}+\Pi_{ij} \right)(\mathbf{v}_{j}-\mathbf{v}_{i})\nabla_{i}W(\mathbf{x}_{i}-\mathbf{x}_{j},h)$$
L'equazione di continuità non ha bisogno di essere evoluta perché è automaticamente vera sempre in un metodo Lagrangiano dato che simuliamo ogni singola particella individualmente.
#### Paragoni
I due schemi sono stati paragonati numerose volte nella letteratura sugli stessi problemi e si è trovato che i due metodi convergono in modo soddisfacente quando utilizzati sulle stesse dinamiche e condizioni iniziali. Le discrepanze tra i risultati sono ben spiegate dalle debolezze di ciascun metodo in uso.
### Fisica aggiuntiva
I metodi qui descritti si occupano principalmente di descrive l'azione della gravità o dei fenomeni idrodinamici, ma un sistema realistico contiene altra fisica oltre a questi effetti. Esempi importanti sono il raffreddamento radiativo, già menzionato nel termine $\Lambda(u,\rho)$ all'inizio di [[#Idrodinamica]], la formazione stellare, il feedback stellare come le supernove e i venti stellari, campi magnetici, raggi cosmici, fenomeni di trasporto e accrescimento di buchi neri.
## Collegare simulazioni alle osservazioni
Una volta compiuta una simulazione, bisogna assicurarsi che i dati che ne otteniamo siano equivalenti a quelli che otterremmo da una misura sperimentale con un telescopio. Questo non è un dato di fatto, dato che la strumentazione sperimentale ha un suo set di problematiche come risoluzione, rumore e altro. Paragonare direttamente i risultati di una simulazione ad un'osservazione sperimentale è dunque fuorviante, dato che la simulazione sarà "pura", mentre l'osservazione sarà affetta dai problemi di strumentazione imperfetta. Per paragonare le cose è importante dunque simulare gli effetti della strumentazione e applicarli sui risultati della simulazione per ottenere dati che sono fedeli alla nostra tecnologia e dunque paragonabili ai nostri esperimenti.
## Fonti
- Dolag et al., 2008, Simulation techniques for cosmological simulations
- Borgani & Kravtsov, 2009, Cosmological simulations of galaxy clusters