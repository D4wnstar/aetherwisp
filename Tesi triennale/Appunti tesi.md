Lo scopo dell'introduzione è dare tutte le basi teoriche necessarie per capire la tesi. Lo scopo della tesi è analizzare la metallicità di ammassi simulati mediante l'analisi dei dati e la produzione di profili, sia da dati 3D sia da mappe 2D. Dunque, l'introduzione teorica deve trattare di
- Ammassi di galassie
- La loro formazione e evoluzione
- Le loro componenti interne (e.g., ICM)
- Caratteristiche osservative (e.g., emissione, da cui mappe)
- Metallicità
- Metallicità dell'ICM
- Perché la metallicità ci interessa (paragonare con quelle osservate per )
- Metodi di simulazione (N-body, SPH)

**Scaletta**
1. Ammassi di galassie
	1. Introduzione
	2. Formazione ed evoluzione (cenni)
	3. Componenti (principalmente l'ICM, cenni di sottostrutture)
	4. Metodi simulativi (N-body per DM, SPH per barionica, perché ci servono)
2. Osservazioni e metallicità
	1. Caratteristiche osservative (e.g., emissione visiva, X, mappe)
	2. Metallicità (cos'è, perché ci interessa)
	3. Profili, mappe, particelle (come creare i profili, cosa ci dicono)
3. Analisi
	1. Dati utilizzati
	2. Metodo di analisi
	3. Risultati e discussione
4. Conclusioni

**Scaletta con argomenti**
1. **Ammassi di galassie**
	1. *Introduzione*
		* Definizione e scala dimensionale: dalle galassie ($10^5$ pc) ai filamenti cosmici ($10^7$ pc), con focus sui cluster ($3\text{-}4 \cdot 10^6$ pc).
		* Ruolo cosmologico: strutture più grandi collassate, strumenti per tracciare l'evoluzione del cosmo e vincolare i parametri cosmologici ($\Omega_m, \Omega_\Lambda$).
		* Proprietà fisiche generali: masse ($10^{14}\text{-}10^{15} M_\odot$), emissione X (luminosità $10^{43}\text{-}10^{45}$ erg/s, temperatura $10^7$ K), composizione (Materia Oscura, barioni, ICM).
	2. *Formazione ed evoluzione (cenni)*
		* Condizioni iniziali: campo di densità $\delta(\mathbf{x})$, spettro di potenza $P(k)$, varianza smussata $\sigma(R)$.
		* Fasi di evoluzione: fase lineare (fattore di crescita $D_+(a)$), fase non lineare (collasso gerarchico), equilibrio idrostatico e viriale (equazione dell'energia).
		* Modello autosimilare (gravità pura, relazioni massa-temperatura $M \propto T^{3/2}$, luminosità $L_X \propto T^2$).
		* Collasso sferico (top-hat).
		* Deviazioni dall'autosimilarità: pre-riscaldamento, raffreddamento, feedback (SN, AGN).
	3. *Componenti (principalmente l'ICM, cenni di sottostrutture)*
		* Materia Oscura: Componente dominante del potenziale gravitazionale.
		* ICM: Definizione, stato del plasma (quasi neutro, continuo), proprietà termodinamiche (densità $n_e$, temperatura $T$, entropia $K$).
		* Sottostrutture: Cool Cores (CC) vs Non-Cool Cores (NCC), merger e accrescimento, turbolenza, shock.
	4. *Metodi simulativi*
		* Dinamica non lineare e complessità dei processi fisici (feedback, idrodinamica).
		* N-body: Equazione di Vlasov-Poisson discretizzata. Metodi di calcolo del potenziale: Somma Diretta, Alberi (Tree), Particle-Mesh (PM), Ibridi (TreePM).
		* Idrodinamica: Equazioni di Eulero.
		    * Metodi Euleriani (Griglia, AMR, Riemann solvers).
		    * Metodi Lagrangiani (SPH).
		* Fisica aggiuntiva sub-grid: Raffreddamento radiativo, formazione stellare, feedback stellare e da AGN.

2. **Osservazioni e metallicità**
	1. *Caratteristiche osservative*
		- Cenni di emissione visiva
		* Emissione X: Meccanismi (Bremsstrahlung termico, righe spettrali di ioni pesanti come ferro).
		* Effetto Sunyaev-Zeldovich (SZE) come marcatore: Scattering Compton inverso dei fotoni CMB, indipendenza dalla distanza.
		* Mappe e sintesi: Creazione di osservazioni sintetiche dalle simulazioni per confronto diretto con i dati sperimentali (gestione di risoluzione e rumore strumentale).
	2. *Metallicità*
		* Definizione, importanza come tracciatore dell'evoluzione chimica e dei processi astrofisici.
		* Sorgenti di arricchimento:
		    * Feedback stellare: Supernovae (SNII, SNIa), stelle AGB (rami asintotici).
		    * Feedback AGN: Ruolo nel trasporto di metalli e riscaldamento.
		    * Pre-arricchimento: Metallicità presente prima della formazione del cluster.
		* Funzione di Massa Iniziale (IMF), rendimenti stellari, tempi di vita delle stelle.
	3. *Profili, mappe, particelle*
		* Definizione di profili radiali (binning, scelta del centro es. minimo del potenziale).
		* Differenza tra metallicità mediata sulla massa ($w=m$) e mediata sull'emissività ($w=m\rho\Lambda$). Formula $Z_w = \frac{\sum Z_i w_i}{\sum w_i}$.
		* Distribuzione spaziale (picchi centrali vs code piatte).
		* Correlazioni Metallicità-Entropia (anticorrelazione), CC vs NCC.
		* Universalità, piattezza delle code e invarianza evolutiva ($z \sim 2$ a oggi).

3. **Analisi**
	1. *Dati utilizzati*
		* Nome del set di dati, volume della scatola, risoluzione (massa particella, forza softening $\epsilon$), cosmologia sottostante.
		* Snapshot utilizzata e redshift d'interesse ($z=0$).
		* Fisica inclusa nel codice di simulazione (quali modelli di feedback/raffreddamento sono attivi).
	2. *Metodo di analisi*
		* Linguaggio usato e librerie (Python, SMAC, ecc.).
		* Definizione delle quantità (es. $R_{500}$, $R_{200}$).
		* Identificazione degli ammassi: Strumento utilizzato per trovare gli aloni (SUBFIND), criteri di selezione.
		* Algoritmo di binning (lineare, logaritmico).
		* Gestione delle particelle di gas (ICM) e delle stelle.
	3. *Risultati e discussione*
		* Presentazione dei profili, grafici di $Z(r)$ vs $r/R_{500}$.
		* Analisi delle tendenze, dipendenza dalla massa/temperatura, andamento delle code.
		* Validazione dei modelli di feedback (stellare vs AGN) e del pre-arricchimento sulla base dei risultati ottenuti.
		* I profili concordano con le misure X?

4. **Conclusioni**
	* Riassunto dei risultati principali ottenuti dall'analisi dei profili radiali.
	* Implicazioni cosmologiche/astrofisiche (es. conferma del ruolo dominante del pre-arricchimento o dell'efficienza dell'AGN).
	* Limitazioni dello studio (risoluzione della simulazione, fisica non inclusa).
	* Sviluppi futuri (miglioramenti della risoluzione, inclusione di nuova fisica nei modelli).
