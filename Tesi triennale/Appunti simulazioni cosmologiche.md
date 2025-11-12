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
## Fonti
- Dolag et al., 2008, Simulation techniques for cosmological simulations
- Borgani & Kravtsov, 2009, Cosmological simulations of galaxy clusters