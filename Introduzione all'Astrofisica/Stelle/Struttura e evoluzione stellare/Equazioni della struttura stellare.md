Che le [[stella|stelle]] siano in un qualche forma equilibrio è evidente dal fatto che osserviamo stelle con età stimate nei miliardi di anni. Per una prova più rigorosa, si può calcolare il [[tempo dinamico]] di una stella e notare quanto minuscolo sia in confronto alla sua aspettativa di vita. Per conoscere, quindi, le proprietà strutturali di una [[stella]] è necessario comprendere che tipo di equilibrio tiene le stelle stabili e come possiamo formare un modello matematico per descriverlo.

Dato che una stella, in fondo, è un sistema relativamente semplice[^1] (una "palla" di gas estremamente calda), siamo in grado di costruire un modello che ne descrive completamente lo [[stato]] usando cinque equazioni in cinque variabili. Queste sono:
1. L'**equazione di equilibrio idrostatico**[^2]:
$$\frac{dP(r)}{dr}=- \frac{GM(r)\rho(r)}{r^{2}}$$
2. L'**equazione di continuità di massa**:
$$\frac{dM(r)}{dr}=4\pi r^{2}\rho(r)$$
3. L'**equazione di stato dei gas perfetti**:
$$P(r)=n(r)k_{B}T(r)\quad\text{con}\quad n(r)=\frac{\rho(r)}{\mu m_{p}}$$
4. L'**equazione di generazione di energia**:
$$\frac{dL}{dr}=4\pi r^{2}\rho(r)\epsilon(\rho,T,\text{comp.})$$
5. L'**equazione di trasporto radiativo**:
$$\frac{dT(r)}{dr}=- \frac{3}{4c} \frac{\kappa L(r)\rho(r)}{4\pi r^{2}a T^{3}(r)} \quad \text{con}\quad \kappa=\frac{1}{\rho l}, \quad a=\frac{4\sigma}{c}$$

e le variabili sono:
1. la pressione $P$
2. la massa $M$
3. la densità $\rho$
4. la "luminosità" $L$
5. la temperatura $T$

assieme a:
- la distanza dal centro della stella $r$
- la [[costante gravitazionale]] $G$
- la [[Boltzmann constant]] $k_{B}$
- la densità di [[particella|particelle]] per unità di volume $n$, con $\mu$ il peso molecolare medio e $m_{p}$ la massa del [[protone]]
- l'energia generata per unità di massa $\epsilon$
- l'opacità del gas $\kappa$, con $l$ il cammino libero medio dei [[Photon|fotoni]]
- la [[costante di Stefan-Boltzmann]] $\sigma$

Abbiamo anche delle condizioni al contorno:
$$\begin{cases}
M(r=0)=0 \\
L(r=0)=0 \\
P(r=r_{\star})=0 \\
M(r=r_{\star})=M_{\star}
\end{cases}$$
Dunque in totale abbiamo 7 equazioni, di cui 4 principali, e 4 condizioni al contorno. Dalla teoria di analisi matematica sappiamo che se esiste una soluzione di questo problema con queste condizioni al contorno, allora la soluzione è unica. Che questa soluzione esista forma la base della **congettura di Vogt-Russel**, che dice che la nascita e l'intera evoluzione di una stella dipende solo e unicamente dalla sua massa e dalle sue condizioni iniziali. Questa è una semplificazione che non tiene conto di due fattori: rotazione e magnetismo. Sono comunque fattori minori che sono importanti solo in alcune stelle.
## Derivazioni
### Equilibrio idrostatico
Consideriamo una stella come un sistema a simmetria sferica e prendiamo un elemento di massa $dm$ di volume $dV=dSdr$ ad una distanza $r$ dal centro. Ci saranno due tipi di forze applicate su questo elemento: una forza attraente, che attrae lo verso il centro e determinata dalla [[Interazione gravitazionale|forza gravitazionale]] della stella stessa, e una forza repellente, che lo respinge e di trattazione più complessa. Possiamo rappresentare genericamente la forza repellente come una pressione applicata su un'area: $AdP$, dove $dP$ è il gradiente di pressione verso il centro.

![[Schema Equilibrio idrostatico|Equilibrio idrostatico|50%|center]]

Per avere equilibrio, la forza totale (con verso positivo verso il centro) dovrà essere nulla, ossia
$$F_{gr}-AP(r+dr)+AP(r)=- \frac{GM(r)}{r^{2}}dm-AP(r+dr)+AP(r)=0$$
dove $M(r)$ è la massa entro il raggio $r$[^3]. Ricordando che $dm=\rho(r)dV$, dove $\rho(r)$ è la densità della stella al raggio $r$, e che possiamo approssimare
$$P(r+dr)-P(r)\simeq \frac{dP}{dr}\times dr$$
possiamo trovare la variazione di pressione per unità di distanza:
$$\boxed{\frac{dP(r)}{dr}=- \frac{GM(r)\rho(r)}{r^{2}}}$$
che si dice **equazione di equilibrio idrostatico**.

Dati i moti caotici presenti all'interno della stella, trovare una formula esatta per la densità è impossibile. Si può però risolvere questa equazione in modo molto approssimato per ottenere una stima dell'ordine di grandezza della pressione interna. Il termine sinistro sarà $\sim P/R$, quello destro $\sim GM_{s}^{2}/R^{5}$, da cui
$$P\sim \frac{GM_{s}^{2}}{R^{4}}$$
### Continuità di massa
Considero un elemento di massa sferico (un "guscio")
$$dM(r)=\rho(r)4\pi r^{2}dr$$
Posso riscriverlo per trovare l'**equazione di continuità della massa**:
$$\boxed{\frac{dM(r)}{dr}=4\pi r^{2}\rho(r)}$$
### Equazione di stato dei gas perfetti
Una stella è, su grande scala, considerabile come un gas perfetto. Possiamo quindi sfruttare l'[[equazione di stato dei gas perfetti]]:
$$\boxed{P(r)=n(r)k_{B}T(r)\mbox{ con }n(r)=\frac{\rho(r)}{\mu m_{p}}}$$
con $k_{B}$ la [[Boltzmann constant]]. $n(r)$ è la densità di particelle per volume, ma non è una nuova variabile in quanto è ottenibile dalla densità di massa $\rho(r)$ con $n(r)=\rho(r)/\mu m_{p}$, con $m_{p}$ la massa del protone.

$\mu$ è il peso molecolare medio del gas, abbastanza simile a quella dell'[[atomo di idrogeno]] in questa approssimazione. $\mu$ dipende dalla composizione del gas: per idrogeno completamente [[ionizzazione|ionizzato]], vale $\mu=0.5$; per una composizione solare altamente ionizzata si ha $\mu\simeq0.6$ nella maggior parte della stella, tranne nel centro dove l'idrogeno è parzialmente fuso con l'elio e vale $\mu\simeq1$.
### Generazione di energia
Le tre equazioni precedenti contengono quattro variabili, quindi abbiamo bisogno di una quarta equazione per chiudere il sistema.

Un modo per aggirare il problema è usare l'**equazione politropica**, che suppone una relazione tra la pressione $P$ e la densità del gas $\rho$
$$P\propto\rho^{\gamma}$$
dove $\gamma$ è una costante detta **indice politropico**. Con questa quarta equazione possiamo dire di aver chiuso il sistema. Tuttavia, sebbene questa aggiunta possa dare buoni risultati (l'indice politropico è un parametro libero che si adatta automaticamente), non dà alcuna spiegazione su un aspetto fondamentale della stabilità di una stella: la generazione di energia e il suo trasporto dal centro della stella fino alla sua superficie.

Questo porta alla domanda: è la contrazione predetta dal teorema del viriale a determinare la produzione energetica della stella? Per provare a capirlo, calcoliamo il [[tempo scala di Kelvin-Helmholtz]], che è il tempo necessario per irradiare tutta l'energia gravitazionale ottenuta dal collasso gravitazionale:
$$t_{KH}=\frac{|\Omega_{\star}|}{L_{\star}}\sim \frac{GM_{\star}^{2}}{R_{\star}L_{\star}}$$
con $\Omega_{\star}$ $M_{\star}$, $R_{\star}$ e $L_{\star}$ il potenziale gravitazionale, massa, raggio e [[luminosità]] della stella. Nel caso del Sole, questo vale $3.08\times10^{7}$ anni, che darebbe al sole un'aspettativa di vita di qualche decina milione di anni. Evidenza geologica della formazione del Sistema Solare indica con buona precisione che il Sole abbia diversi miliardi di anni di età, ben superiore a quella assunta del tempo scala. La conclusione, dunque, è che deve per forza esserci un qualche processo di produzione energetica che possa contrastare la perdita di energia per irradiazione. Se così non fosse, il Sole si sarebbe già spento centinaia di milioni di anni fa.

Il processo deve essere necessariamente due cose: stabile e estremamente efficiente. In mancanza di questi due fattori, la stella non potrebbe durare così a lungo come evidentemente fa. Questo processo deve dipendere dalle condizioni interne della stella, quindi densità e temperatura del gas, ma anche dalla composizione chimica della stella. Possiamo formalizzare questa dipendenza in una variabile $\epsilon(\rho,T,\text{comp.})$ che descrive l'energia prodotta da un gas in queste condizioni. Allora chiamiamo $L(r)$ l'energia che attraversa una superficie sferica (un "guscio") della stella a distanza $r$. La variazione di questa energia in funzione della distanza è detta **equazione della generazione di energia** e si scrive
$$\frac{dL(r)}{dr}=4\pi r^{2} \rho(r) \epsilon(\rho,T,\text{comp.})$$
la cui derivazione completa si trova in [[Trasporto radiativo stellare]].

Purtroppo, anche questa equazione aggiunge una nuova variabile, $L(r)$, che è un [[flusso energetico]], non troppo differente da quelli misurati da un telescopio. Tuttavia, per raggi interni alla superficie, il trasporto avviene da strato a strato della stella. È solo alla superficie $R_{\star}$ che lo scambio avviene con lo spazio circostante: $L(R_{\star})$ è infatti la luminosità della stella $L_{\star}$.

Il processo effettivo con cui le stelle producono energia è la [[fusione nucleare]].
### Trasporto energetico
Abbiamo bisogno di una quinta equazione per chiudere definitivamente il sistema. La termodinamica insegna che il trasporto di calore avviene attraverso tre meccanismi: [[conduzione]], [[convezione]] e [[irradiazione|irraggiamento]]. La conduzione per [[elettrone|elettroni]] è molto inefficiente e trascurabile. La convezione è di maggiore importanza. L'irraggiamento, anche noto come **trasporto radiativo** nel contesto dell'astrofisica, è di gran lunga il più interessante dei tre, per via dell'altissima opacità del gas stellare.

Per via dell'altissima densità del gas, i [[Photon|fotoni]] hanno una probabilità molto alta di interagire con gli [[atomo|atomi]] e anche con gli elettroni liberi mediante [[diffusione di Thompson]]. Ciò significa che il percorso medio di un fotone emesso dentro una stella è molto piccolo. Se i fotoni emessi non escono dalla superficie, allora il gas è opaco. In queste condizioni, si raggiunge un equilibrio termodinamico locale, a differenza dello stato globale che sta irradiando verso l'esterno.

Dato che i fotoni vengono emessi e riassorbiti di continuo, un singolo fotone[^5] impiega tempi enormi per uscire dalla superficie. Nel Sole, si teorizzano tempi medi di circa 30,000 anni. Questo tempo è cruciale perché determina il numero di fotoni che effettivamente escono dalla superficie, ossia quelli irradiati verso l'esterno, ossia quelli che vediamo e che determinano la luminosità stellare. Di fatto, la lentezza con cui escono i fotoni dalla stella agisce come un smorzatore della luminosità; se tutti i fotoni uscissero direttamente, la luminosità stellare sarebbe altissima.

Studiando il moto medio dei fotoni (per una derivazione formale vedi [[Trasporto radiativo stellare]]), si trova una relazione che descrive l'andamento della temperatura di una stella in funzione della distanza dal centro, detta **equazione di trasporto radiativo**:
$$\frac{dT(r)}{dr}=- \frac{3}{4\sigma c} \frac{\kappa\rho(r)L(r)}{4\pi r^{2}T^{3}(r)}$$
dove $\kappa=1/\rho l$ è l'opacità del gas, con $l$ il cammino libero medio dei fotoni, e $\sigma$ è la [[costante di Stefan-Boltzmann]]. Si tratta di un'[[equazione differenziale ordinaria]] di primo ordine che, fortunatamente, non introduce nessuna nuova variabile. Il sistema, quindi, è chiuso e risolvibile.
## Conseguenze
### Temperatura nel nucleo solare
Dall'equazione di equilibrio idrostatico possiamo ottenere una stima della pressione interna del Sole. Sapendo che la densità centrale è approssimativamente 110 volte superiore a quella media, possiamo usare l'equazione dei gas perfetti per stimare la temperatura:
$$T_{centro}=\frac{P}{nk_{B}}=1.5\times10^{7}\ K$$
Questo stesso calcolo può essere esteso a tutte le altre stelle ed è particolarmente importante dato che la temperatura determina, assieme alla pressione, lo stato di materia del centro, che a sua volta determina il metodo di produzione di energia.
### Equilibrio termico
Una nube di gas in quasi-equilibrio idrostatico aumenta e diminuisce contraendosi ed espandendosi. Nel contrarsi, la temperatura del gas diventa molto in fretta maggiore del [[Radiazione cosmica nelle microonde|fondo cosmico nelle microonde]] ($\sim2.7$ K), quindi si instaura uno scambio di calore tra il gas e lo spazio circostante. Data la mancanza di materia nello spazio, lo scambio avviene solo per [[irradiazione]]. Questo processo è regolato dal [[teorema del viriale]], per il quale
$$2K+\Omega=0$$
L'energia totale è semplicemente $E=K+\Omega$, quindi le uniche due soluzioni sono
$$E=-K, \quad E=\frac{\Omega}{2}$$
Se la nube si trova in uno [[Stati in meccanica quantistica|stato legato]] gravitazionalmente, l'energia deve essere negativa. Ma irradiare energia significa che diventerà ancora più negativa, quindi il sistema sarà ancora più legato e continuerà a diventarlo sempre di più. A diminuire è il potenziale gravitazionale, mentre l'energia termica aumenta per conservare il teorema del viriale. Ciò significa che la temperatura della nube di gas aumenta spontaneamente, allontanandosi sempre di più dall'equilibrio idrostatico.[^4]
### Energia totale
Calcoliamo la pressione in una stella
$$\int_{0}^{r_{\star}}4\pi r^{3} \frac{dP}{dr}=- \int_{0}^{r_{\star}} \frac{GM(r)\rho(r)4\pi r^{2}}{r}dr=P(r)4\pi r^{3}|_{0}^{r_{\star}}-3\int_{0}^{r_{\star}}P(r)4\pi r^{2}dr$$
sapendo che $dM(r)=\rho(r)4\pi r^{2}dr$ dalla continuità di massa. Allora l'energia gravitazionale della stella, cioè una delle due energie che mantengono l'equilibrio idrostatico, è
$$\boxed{E_{gr}=-3\bar{P}V}$$
che si tratta del [[teorema del viriale]], con $\bar{P}$ la pressione media del sistema. Assumendo un gas ideale e $PV=nk_{B}T$ 
$$\boxed{\bar{P}= - \frac{E_{gr}}{3V}=\frac{2}{3} \frac{E_{T}}{V}}$$
con $E_{T}=\frac{3}{2}Nk_{B}T$ l'energia termica della stella. In altre parole
$$\bar{P}V= \frac{2}{3}E_{T}$$
L'energia totale della stella è
$$E_{tot}=E_{T}+E_{gr} = -E_{T} \Rightarrow \boxed{E_{T}=-\frac{E_{gr}}{2}}$$
Se la stella si scalda, la stella si espande e diventa meno densa.

Analizziamo l'energia gravitazionale di una stella
$$E_{gr}=-\int_{0}^{r_{\star}} \frac{GM(r)\rho(r)4\pi^{2}}{r}dr=\ldots$$
Assumiamo che la densità $\rho$ sia costante (cosa non vera, ma semplifica)
$$\ldots=\int_{0}^{r_{\star}} \frac{G\frac{4\pi}{3}r^{3}\rho^{2}4\pi r^{2}}{r}dr=- \frac{3}{5} \frac{GM^{2}}{r_{\star}}$$
Il valore vero (ottenuto senza assumere che $\rho$ sia costante) è
$$\boxed{E_{gr}=- \frac{GM^{2}}{r_{\star}}}$$
Usando il teorema viriale si può giungere alla pressione. Per esempio troviamo la pressione media del sole
$$\bar{P}_{\odot}\simeq \frac{1}{3} \frac{E_{gr}}{2} \frac{1}{V}\simeq \frac{1}{3} \frac{GM^{2}_{\odot}}{\frac{4}{3}\pi r^{4}_{\odot}}$$
che mettendo i numeri si trova essere circa $10^{9}$ Atm (o $1.013\cdot10^6$ nel sistema CGS), che è meno della pressione necessaria per formare un diamante.

Cerco ora la **temperatura viriale**, che non è altro che la temperatura trovata dal teorema del viriale. Possiamo calcolare l'energia potenziale del Sole
$$U= \frac{3}{2}Nk_{B}T= \frac{1}{2} \frac{GM^{2}_{\odot}}{r_{\odot}}\simeq \frac{1}{2} \frac{GM_{\odot}N\bar{m}}{r_{\odot}}$$
dove abbiamo semplificato una massa solare come massa delle particelle che lo compongono: $\bar{m}$ è la massa media delle particelle, in questo caso protoni e elettroni (cioè quella dell'idrogeno) e $N$ è il numero di particelle. Dato che la massa dell'elettrone è minuscola in paragone a quella del protone, si ha
$$\bar{m}= \frac{m_{p}+m_{e}}{2}= \frac{m_{H}}{2}\simeq 1.7\cdot10^{-24}$$
con $m_{H}$ la massa dell'idrogeno.
$$kT_{vir}\simeq \frac{GM_{\odot}m_{H}}{6r_{\odot}}=5.4\times10^{-10}\mbox{erg}$$
estraendo la temperatura si trova la temperatura (media)
$$T_{vir}=4\times10^{6}\mbox{ K}$$


[^1]: Qui si parla di stelle tipiche, prive di peculiarità come estrema velocità di rotazione o campi magnetici forti, come si vedrebbe ad esempio in una [[stella di neutroni]]. Per stelle più esotiche, bisogna avere modelli ad hoc.
[^2]: Una stella non è propriamente in equilibrio idrostatico, in quanto la stella si contrae nel procedere della sua vita. Tuttavia, il tempo di contrazione è enorme rispetto al tempo dinamico della stella, quindi ad ogni dato momento, la stella è sostanzialmente in equilibrio. Il termine più corretto sarebbe *quasi-equilibrio idrostatico*.
[^3]: La massa esterna non viene considerata perché per il [[teorema di Gauss]] non esercita alcuna forza gravitazionale sulla massa più interna.
[^4]: Questo processo è il motivo per cui l'Universo non è uniforme: se fosse per la termodinamica da sola, l'Universo si appiattirebbe ad una singola sostanza omogenea. La "competizione" tra gravità e termodinamica è sostanzialmente il motore che determina l'evoluzione dell'Universo.
[^5]: Inteso come la catena di emissione e assorbimento che crea e distrugge fotoni. Di fatto, un fotone cessa di esistere quando è assorbito e la riemissione ne crea uno nuovo, ma dato che la meccanica quantistica dimostra che i fotoni sono particelle indistinguibili fra loro, possiamo considerare intuitivamente la catena con un singolo fotone che "rimbalza" più e più volte tra gli elettroni.