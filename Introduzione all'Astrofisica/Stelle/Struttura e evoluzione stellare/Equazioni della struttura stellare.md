Che le [[stella|stelle]] siano in un qualche forma equilibrio è evidente dal fatto che osserviamo stelle con età stimate nei miliardi di anni. Per una prova più rigorosa, si può calcolare il [[tempo dinamico]] di una stella e notare quanto minuscolo sia in confronto alla sua aspettativa di vita. Per conoscere, quindi, le proprietà strutturali di una [[stella]] è necessario comprendere che tipo di equilibrio tiene le stelle stabili e come possiamo formare un modello matematico per descriverlo.

Dato che una stella, in fondo, è un sistema relativamente semplice[^1] (una "palla" di gas estremamente calda), siamo in grado di costruire un modello che ne descrive lo [[stato]] usando soltanto quattro equazioni. Queste sono:

1. L'**equazione di equilibrio idrostatico**: $$\frac{dP(r)}{dr}=- \frac{GM(r)\rho(r)}{r^{2}}$$dove $G$ è la [[constante gravitazionale]], $M$ è la massa della stella e $\rho$ è la sua densità. Tutto è in funzione della distanza dal centro $r$. Rappresenta l'equilibrio tra le uniche forze che si stanno considerando: la forza di gravità $F_{G}$ e le forze di pressione $F_{P}$, tali che $F_{G}+F_{P}=0$.
   
   Si può ottenere una stima della pressione con $$P\sim \frac{GM_{s}^{2}}{R^{4}}$$
2. L'**equazione di continuità di massa**: $$\frac{dM(r)}{dr}=4\pi r^{2}\rho(r)$$ che collega la massa e la densità di massa.
3. L'**equazione di stato dei gas perfetti**: $$P(r)=n(r)kT(r)\mbox{ con }n(r)=\frac{\rho(r)}{\mu m_{p}}$$con $k$ la [[costante di Boltzmann]]. $n$ è la densità di particelle per volume, ma non è una nuova variabile in quanto è ottenibile dalla densità di massa $\rho$ con $n(r)=\rho/\mu m_{p}$, con $m_{p}$ la massa del protone. L'equazione dei gas perfetti vale se approssimiamo una stella come fatta di gas perfetto.
   
   $\mu$ è il peso molecolare medio del gas, abbastanza simile a quella dell'atomo di idrogeno in questa approssimazione. $\mu$ dipende dalla composizione del gas: per una composizione solare altamente ionizzata si ha $\mu\simeq0.6$ e nel centro, dove l'idrogeno è parzialmente fuso con l'elio, si ha $\mu\simeq1$.
4. L'**equazione di generazione di energia** all'interno di una stella: $$\frac{dL}{dr}=4\pi r^{2}\rho(r)\epsilon(r)$$dove $\epsilon(\rho, T, \text{composizione})$ è l'energia generata per unità di massa e di tempo da un gas di composizione nota alla densità $\rho$ e temperatura $T$. $L(r)$ è l'energia che passa per una sfera di raggio $r$ dall'interno verso l'esterno. A $L(R_{\odot})$ rappresenta la [[Luminosità]] della stella.
5. L'**equazione di trasporto energetico radiativo** (irradiazione): $$\frac{dT(r)}{dr}=- \frac{3}{4c} \frac{\kappa L(r)\rho(r)}{4\pi r^{2}\sigma T^{3}(r)}$$dove $L$ è la luminosità della stella, $T$ è la sua temperatura, $\kappa(\rho,T,\text{composizione})=1/\rho l$ è l'opacità ($l$ è il cammino libero medio di un fotone nella stella) e $\sigma$ è la [[costante di Stefan-Boltzmann]].

L'*equazione politropica* suppone una relazione tra la pressione $P$ e la densità del gas $\rho$
$$P\propto\rho^{\gamma}$$
dove $\gamma$ si dice *indice politropico*.

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
$$A(P+dP)-AdP=F_{gr}-AdP=- \frac{GM(r)}{r^{2}}dm-AdP=0$$
dove $M(r)$ è la massa entro il raggio $r$[^2]. Ricordando che $dm=\rho(r)dV$, dove $\rho(r)$ è la densità della stella al raggio $r$, e che possiamo approssimare
$$P(r+dr)-P(r)\simeq \frac{dP}{dr}\times dr$$
possiamo trovare la variazione di pressione per unità di distanza:
$$\boxed{\frac{dP(r)}{dr}=- \frac{GM(r)\rho(r)}{r^{2}}}$$
che si dice **equazione di equilibrio idrostatico**.

Dati i moti caotici presenti all'interno della stella, trovare una formula esatta per la densità è impossibile. Si può però risolvere questa equazione in modo molto approssimato per ottenere una stima dell'ordine di grandezza della pressione interna. Il termine sinistro sarà $\sim P/R$, quello destro $\sim GM_{s}^{2}/R^{5}$, da cui
$$P\sim \frac{GM_{s}^{2}}{R^{4}}$$
### Equazione di continuità di massa
$$\int_{0}^{r_{\star}}4\pi r^{3} \frac{dP}{dr}=- \int_{0}^{r_{\star}} \frac{GM(r)\rho(r)4\pi r^{2}}{r}dr=P(r)4\pi r^{3}|_{0}^{r_{\star}}-3\int_{0}^{r_{\star}}P(r)4\pi r^{2}dr$$
sapendo che $dM(r)=\rho(r)4\pi r^{2}dr$. Allora l'energia gravitazionale della stella, cioè una delle due energie che mantengono l'equilibrio idrostatico, è
$$\boxed{E_{gr}=-3\bar{P}V}$$
che si tratta del **teorema viriale**, con $\bar{P}$ la pressione media del sistema. Assumendo un gas ideale e $PV=nk_{B}T$ 
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

Prendo un elemento di massa sferico (un "guscio")
$$dM(r)=\rho(r)4\pi r^{2}dr$$
e posso riscriverlo per trovare una forma dell'**equazione di continuità della massa** 
$$\boxed{\frac{dM(r)}{dr}=4\pi r^{2}\rho(r)}$$


[^1]: Qui si parla di stelle tipiche, prive di peculiarità come estrema velocità di rotazione o campi magnetici forti, come si vedrebbe ad esempio in una [[stella di neutroni]]. Per stelle più esotiche, bisogna avere modelli ad hoc.
[^2]: La massa esterna non viene considerata perché per il [[teorema di Gauss]] non esercita alcuna forza gravitazionale sulla massa più interna.