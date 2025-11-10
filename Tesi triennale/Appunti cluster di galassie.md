La distribuzione di materia luminosa è non-uniforme e concentrata in "isole" che chiamiamo [[galassia|galassie]] (~$10^{5}\text{ pc}$). Le galassie a loro volta si concentrano in gruppi di due o più (~$10^{6}\text{ pc}$), poi gruppi di centinaia o migliaia che chiamiamo **[[galaxy cluster|cluster di galassie]]** (~$3\textendash4\cdot10^{6}\text{ pc}$) e poi filamenti cosmici che li collegano (~$10^{7}\text{ pc}$).

I cluster di galassie sono le strutture più grandi che hanno avuto tempo di compiere il collasso gravitazionale. Sono strumenti utili per tracciare l'evoluzione del cosmo.

Hanno masse nel range di $10^{14}$-$10^{15}\ M_{\odot}$ e emettono [[Photon|fotoni]] intensamente nel range dei raggi X, quindi una manciata di [[Electronvolt|keV]] e luminosità nel range di $10^{43}$-$10^{45}\text{ erg/s}$. L'emissione è dovuta a gas a [[Temperature|temperature]] di $10^{7}\text{ K}$ e densità di numero di particelle nel range $10^{-1}$-$10^{-4}\text{ cm}^{-3}$ in cui accade [[Bremmstrahlung]] e emissione di [[Riga spettrale|righe spettrali]] di ioni pesanti tipo ferro. Questo mezzo *non* fa parte di galassie ed è dunque detto **intra-cluster medium** (**ICM**). L'ICM contiene la stragrande maggioranza della massa dei cluster (~98%). La velocità delle galassie è consistente con la temperatura dell'ICM, il che indica che il sistema sia in equilibrio (termodinamico) in una buca di potenziale gravitazionale comune. La profondità di questa buca è troppo alta per essere causata solo dalla massa visibile: c'è bisogno di una grande quantità di [[materia oscura]].

L'emissione X dei cluster è utile per identificarli anche a distanze cosmologiche. Per esempio, i fotoni X dei cluster che fanno [[Compton scattering]] inverso con i fotoni del [[Radiazione cosmica nelle microonde|CMB]] causano una leggera ma misurabile distorsione nel profilo da [[Black body|corpo nero]] del CMB quando si guarda nella direzione di un cluster, un effetto noto come **Sunyaev-Zeldovich effect** (**SZE**). La misura dello SZE è praticamente distanza-indipendente dato che è una misura del CMB.

I cluster sono utili perché la loro distribuzione e rarità contiene informazioni sulle caratteristiche dell'universo. Per esempio, modelli $\Lambda\text{CDM}$ che usano una densità di massa $\Omega_{m}=0.3$ e costante cosmologica $\Omega_{\Lambda}=0.7$ evolvono più lentamente che modelli Einstein-de Sitter puramente di materia $\Omega_{m}=1$. Di conseguenza, misurazioni della distribuzione reale miste a simulazioni con parametri noti ci permettono di scartare tutti parametri che danno vita a universi con distribuzioni di cluster galattici incompatibili con quella reale. Si trovano alla soglia tra astrofisica e cosmologia: la loro dinamica è principalmente governata dalla gravità, ma i processi astrofisici interni nelle galassie hanno effetti misurabili sul gas ICM interno.
## Modello autosimilare di cluster
Il modello più semplice di cluster assume che tutte le proprietà dei cluster e le loro correlazioni sono dovute esclusivamente dalla gravità, e che il cluster sia in equilibrio viriale. La gravità non ha scale preferenziali, quindi cluster di ogni grandezza sono validi sotto questo modello a patto che si scali la massa allo stesso modo (sono *autosimilari*). La loro massa determina esclusivamente le proprietà termodinamiche del gas ICM.

Al [[redshift]] $z$, chiamo $M_{\Delta_{c}}$ la massa contenuto nel raggio $r_{\Delta_{c}}$ dal centro del cluster a sovradensità media $\Delta_{c}$ volte la densità critica cosmica $\rho_{c}(z)$ al redshift d'osservazione. Allora $M_{\Delta_{c}}\propto \Delta_{c}\rho_{c}(z)r^{3}_{\Delta_{c}}$.
- La sovradensità è il rapporto tra densità di una regione e la densità di sfondo cosmico, $\Delta\equiv \rho _\text{regione}/\rho _\text{sfondo}$. Realisticamente è sempre maggiore di uno.
- Il raggio $r_{\Delta_{c}}$ è definito a mano perché un cluster è una struttura aperta senza un chiaro bordo. Si definisce scegliendo $\Delta_{c}$ e trovando $r_{\Delta_{c}}$ tale che per cui la densità media entro quel raggio sia proprio $\Delta_{c}\rho_{c}$.

La densità critica dell'universo è data dalle [[Equazioni di Friedmann]]
$$\rho_{c}(z)=\frac{3H(z)^{2}}{8\pi G}$$
dove $H(z)$ è il [[Legge di Hubble|parametro di Hubble]]. Alternativamente, può essere espressa partendo dalla densità critica odierna $\rho_{c0}$ come
$$\rho_{c}(z)=\rho_{c0}E(z)^{2}\quad\text{dove}\quad E(z)=\frac{H(z)}{H_{0}}=\sqrt{ (1+z)^{3}\Omega_{m}+(1+z)^{2}\Omega_{\kappa}+\Omega_{\Lambda} }$$
dove $\Omega_{\kappa}=1-\Omega_{m}-\Omega_{\Lambda}$ è il contributo della curvatura dell'universo. Allora, il raggio del cluster può essere espresso anche come $r_{\Delta_{c}}\propto M_{\Delta_{c}}^{1/3}E^{-2/3}(z)$. Dato che il gas è considerato in equilibrio entro il potenziale gravitazionale $\Phi$ del cluster, si ha $k_{B}T\propto \Phi \propto M_{\Delta_{c}}/r_{\Delta_{c}}$, dunque la massa può essere espressa in funzione della temperatura del gas nel cluster come
$$\boxed{M_{\Delta_{c}}\propto T^{3/2}/E(z)}$$
Assumendo che il bremmstrahlung termico domini l'emissione, la luminosità X può essere espressa come
$$L_{X}\propto n_{e}^{2}T^{1/2}r_{\Delta_{c}}^{3}$$
con densità di numero elettronica $n_{e}\propto M/r_{\Delta_{c}}^{3}=\text{cost}$ e $T\propto M_{\Delta_{c}}/r_{\Delta_{c}}$. Usando la relazione massa-temperatura cui sopra possiamo anche dire
$$\boxed{L_{X}\propto T^{2}E(z)}$$
L'entropia dell'ICM nei studi di raggi X è tipicamente definita come
$$S=\frac{k_{B}T}{\mu m_{p}\rho _\text{gas}^{2/3}}$$
Qui $S$ è la costante di proporzionalità nell'equazione di stato di gas perfetto monoatomico adiabatico, $P=S\rho _\text{gas}^{5/3}$. Un'altra quantità (purtroppo anche chiamata "entropia" negli studi di cluster) è
$$K=k_{B}Tn^{-2/3}_{e}$$
Questa quantità nel modello autosimilare, calcolata a sovradensità fissa $\Delta_{c}$, scala con temperatura e redshift come
$$\boxed{K_{\Delta_{c}}\propto TE^{-4/3}(z)}$$
### Migliorie non-autosimilari
Il modello autosimilare (e il suo vicino modello a simmetria sferica) manca di alcuni fenomeni ulteriori alla gravità che descrivono l'evoluzione dell'ICM. Per esempio, processi di feedback dovuti alla formazione stellare, supernove e l'accrescimento dei buchi neri, che producono e trasportano metalli e li diffondono nel cluster mediante processi di gasdinamica. Questi processi paiono essere specialmente importanti nel centro del cluster, dove le simulazioni e i modelli divergono di più.

Una miglioria è aggiungere un pre-riscaldamento del gas ICM a causa di AGN e venti galattici. Questo inietta un'energia termica $E_{h}$ nel sistema che contrasta il collasso gravitazionale. L'effetto è massimo per cluster piccoli e minimo per quelli grandi. Aggiungere questo fenomeno migliora notevolmente le predizioni di luminosità X delle simulazioni. Il problema sta che l'energia necessaria $E_{h}$ per ottenere predizioni realistiche è superiore a quella che le supernove possono realisticamente dare, anche assumendo alta efficienza termica.

Un'altra migliora, apparentemente paradossale, è aggiungere il raffreddamento del gas come spiegazione per l'elevata entropia centrale. La spiegazione è che il raffreddamento rimuove gas a bassa entropia dalla fase calda, che dunque smette di emettere X. L'unico gas che rimane ad emettere X è quello ad alta entropia, che noi osserviamo.