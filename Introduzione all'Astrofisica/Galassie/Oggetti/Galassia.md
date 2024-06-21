Una **galassia** è un sistema di [[Stella|stelle]], [[Relitto stellare|relitti stellari]], [[Mezzo interstellare]] e (teoricamente) [[Materia oscura]] legati fra loro dalla gravità. Tali oggetti orbitano attorno ad un nucleo luminoso costituito da un [[Buco nero]] particolarmente massivo, la cui forza di gravità è sufficiente da mantenerli in orbita stabile.

Le galassie vengono categorizzate in [[Classi galattiche]] in base alla loro morfologia apparente. Diverse classi hanno diverse caratteristiche morfologiche, ma tutte hanno una rigonfiamento centrale chiamato *bulge*.

In molte galassie si nota un'emissione nucleare molto intensa: il bulge centrale, puntiforme nella risoluzione angolare del telescopio, possiede una luminosità ben superiore di quanto il profilo di luminosità non suggerirebbe. In alcuni casi, è talmente luminoso da rendere il resto della galassia completamente indistinguibile dalla [[Point Spread Function]] del nucleo.

Lo spettro ottico di questi nuclei può assumere alcune forme: i nuclei a energia più bassa solitamente mostrano [[Riga spettrale|linee di emissione]] simili a quelle delle [[regione H II|regioni H II]] del [[Mezzo interstellare]] e dunque possono essere spiegate come regioni di forte formazione stellare. Le [[supernova|supernove]] possono complicare ulteriormente lo spettro. Questi sono detti **nuclei starburst**.

Gli spettri ottici più luminosi non sono riconducibili a questo genere di attività. Questi prendono il nome di **[[Nucleo galattico attivo|Nuclei Galattici Attivi]]** (AGN). Le galassie che non presentano spettri con linee di emissione di questo genere prendono il nome di **galassie passive**.
### Rotazione e massa
La rotazione di una galassia è una parte molto importante e informativa della sua struttura, quindi è utile spiegare come funziona. È particolarmente importante nel caso di galassie a spirale, dove la rotazione è molto apparente (e perché la [[Via Lattea]] è a spirale barrata).
#### Galassie a spirale
Consideriamo una galassia a spirale, come la Via Lattea. Osservativamente, notiamo che è affetta da rotazione differenziale, quindi la velocità angolare aumenta man mano che ci si avvicina al nucleo galattico. Per una discussione più completa, vedi [[Via Lattea#Rotazione]].

La velocità di rotazione $v$ ad un certo raggio $r$ ci permette di calcolare indirettamente la sua massa. Usando la [[leggi di Newton|seconda legge di Newton]] e la [[Interazione gravitazionale|legge di gravitazione universale]] si ha:
$$\frac{v^{2}}{r}=a=\frac{F}{m_{ogg}}=G \frac{Mm_{ogg}}{r^{2}} \frac{1}{m_{ruota}}=G \frac{M}{r^{2}}$$
dove $M$ è la massa della galassia entro il raggio $r$ (si assume la simmetria sferica) e $G$ è la [[costante gravitazionale]]. Riordinando
$$v(r)=\sqrt{\frac{GM(r)}{r}} \quad \Rightarrow \quad M(r)=\frac{rv^{2}(r)}{G}\tag{1}$$
che è la velocità di rotazione di una galassia nell'approssimazione di campo debole della relatività generale o, in altre parole, la gravità newtoniana. Compiendo molte misure di massa (anche con ampi errori), è possibile fare un grafico con la velocità misurata sperimentalmente sovrapposte alla stima di velocità data dalla formula sopra. Si trova che, a quasi tutte le velocità al di fuori di quelle molto basse, la stima della formula è consistentemente sempre più bassa del valore misurato. Dev'esserci dunque qualcosa che è stato mancato. Ad oggi ci sono due possibilità riconosciute:
1. **MOND**, Modified Newtonian Dynamics. In altre parole, assumiamo che la migliore teoria della gravitazione che abbiamo oggi, la relatività generale, sia imperfetta e che non funzioni in queste condizioni. Bisogna dunque modificare la teoria per sistemare questa discrepanza.
2. **Materia oscura**. Possiamo assumere che, nelle parti estreme della galassia, sia presente una grande quantità di qualche sostanza che genera un campo gravitazionale, seppur senza emettere alcuna forma di radiazione visibile (o interagire con quella già presente). Chiamiamo questa sostanza *materia oscura* e la maggior parte dei risultati sperimentali sembra confermarne l'esistenza.
#### Misurazione
Le informazioni principali sulla cinematica di una galassia provengono dalle [[Riga spettrale|righe spettrali]] del suo spettro. Operativamente si pone una fessura lungo l'immagine della galassia, orientata sull'asse maggiore, e si misura la luce così ottenuta con uno spettrografo. Lo spessore delle righe dipende dalla velocità di rotazione.

Nel caso di galassie spirali, le righe di emissione associate ad emissione stellare sono strette e soggette a [[Redshift]] Doppler a causa della rotazione differenziale del disco, la cui rotazione dipende dalla posizione sulla fenditura (che rappresenta la distanza dal nucleo). Di conseguenza, la misura è migliore se fatta vedendo una galassia di taglio e impossibile se vista di piatto.
### Luminosità
Esistono metodi analitici per calcolare l'[[irradianza]] emessa da una galassia. Partiamo cercando di definire il profilo di brillanza superficiale di una galassia, sull'asse maggiore dell'immagine della galassia. Per le [[Classi galattiche|galassie ellittiche]], questo segue in genere una **legge di de Vaucouleurs**:
$$I(r)=I(0)\exp\left[- \left( \frac{r}{r_{0}} \right)^{1/4}\right]\tag{1}$$
mentre per le [[Classi galattiche|galassie a spirale]] si ha una curva esponenziale
$$I(r)=I(0)\exp\left(- \frac{r}{r_{0}}\right)\tag{2}$$
Spesso questi profili vengono modellati tramite un **profilo di Sérsic**
$$I(r)=I_{e}\exp \left\{-b_{n} \left[\left(\frac{r}{R_{e}}\right)^{1/n}-1\right]\right\}$$
dove $R_{e}$ è il [[Raggio effettivo]]. $I_{e}$ è la brillanza superficiale calcolata in $R_{e}$. $b_{n}$ è un coefficiente sperimentale tabulato in funzione di $n$ e mette in relazione $r_{0}$ e $R_{e}$. Per $n=1$ si ha il profilo $(1)$, mentre per $n=4$ si ha $(2)$. Una misura di $n$ può dare una vaga approssimazione della morfologia.

La [[relazione Tully-Fisher]] collega velocità di rotazione con luminosità di una galassia a spirale. La [[relazione del piano fondamentale]] invece lega la luminosità di una galassia ellittica con il suo raggio effettivo e la dispersione di velocità.
#### Funzione di luminosità delle galassie
Ben oltre la luminosità di una singola galassia, esistono anche modelli per misurare l'irradianza in funzione della distribuzione di galassie nello spazio. Si consideri un volume di spazio $V$ e si dica $dN$ il numero di galassie con luminosità nell'intervallo $[L,L+dL]$. Allora la **funzione di luminosità delle galassie** $\Phi(L)$ è definita come $dN=V\Phi(L)dL$. La **funzione di luminosità di Schechter** dà una buona approssimazione della precedente funzione
$$\Phi(L)dL=\Phi_{\star}\left(\frac{L}{L_{\star}}\right)^{\alpha}\exp\left(- \frac{L}{L_{\star}}\right) \frac{dL}{L_{\star}}$$
con $L_{\star}$ è la luminosità galattica caratteristica (la luminosità della galassia brillante tipica) e $\Phi_{\star}$ è la normalizzazione (l'abbondanza tipica delle galassie brillanti). Questa funzione ha forme leggermente diverse in base alla [[Classi galattiche|classe galattica]]:
- Tipo 1: galassie E/S0
- Tipo 2: galassie Sa/Sb
- Tipo 3: galassie Sc/Sd
- Tipo 4: galassie irregolari
### Popolazioni
Esiste una correlazione fra la classe galattica di una galassia e la popolazione di [[Stella|stelle]] di cui è composta. Le galassie ellittiche e lenticolari hanno stelle vecchie e molto [[Metallicità|metalliche]] ($Z>Z_{\odot}$) e questo è vero anche per il bulge delle galassie a spirale. I dischi delle spirali invece presentano stelle giovani e blu, con relativamente ($Z\sim Z_{\odot}$). Le galassie nane infine presentano stelle giovani con metallicità molto bassa ($Z\ll Z_{0}$).

Queste variazioni di popolazione stellare sono visibili nella distribuzione del [[colore]] delle galassie vicine. Mettendo [[magnitudine]] in ascissa e colore in ordinata, si trova che le galassie tendono a stare in due regioni principali:
- la **sequenza rossa** è popolata da ellittiche, lenticolari e diverse spirali dei primi tipi
- la **nuvola blu** è popolata da spirali e irregolari

![[Colour-magnitude-diagram-for-spiral-and-elliptical-galaxies.png]]
*Da [Galaxy morphology, luminosity and, environment in the SDSS DR7](https://www.researchgate.net/publication/47866115_Galaxy_morphology_luminosity_and_environment_in_the_SDSS_DR7?_tp=eyJjb250ZXh0Ijp7ImZpcnN0UGFnZSI6Il9kaXJlY3QiLCJwYWdlIjoiX2RpcmVjdCJ9fQ), Tempel et al. 2010*

Si nota che tutte le galassie più luminose sono ellittiche rosse e quelle meno luminose spirali blu. Questo potrebbe essere causato dalla popolazione stellare: stelle vecchie sono più rosse e hanno rapporti massa/luminosità superiori.
### Abbondanze
L'abbondanza di certi elementi chimici è utile per ottenere informazioni sulla galassia. Un'alta presenza di elementi $\alpha$, formati da [[Supernova|supernove di tipo II]], indica la presenza di un alto numero di stelle massive a vita breve, mentre un'alta abbondanza di ferro, associata a [[Supernova|supernove di tipo Ia]], indica la presenza di [[Stella binaria|sistemi binari]] a lunga vita. Il rapporto tra questi elementi è utile per comprendere le tempistiche di [[formazione stellare]].

Per le ellittiche più massive, che hanno rapporti elevati $\alpha/Fe$, si hanno tempi evolutivi brevi, a modo che il ferro prodotto dalle supernove Ia non venga riciclato nelle prossime formazioni stellari.
### Spettro
Lo [[Spettro (astrofisica)|spettro]] è la fonte delle maggior parte delle informazioni che abbiamo su una galassia. Lo spettro è dato dalla sovrapposizione degli spettri di tutte le stelle e quindi sarà simile alla popolazione stellare dominante.

Gli spettri delle ellittiche tendono a mostrare solo [[Riga spettrale|righe di assorbimento]] associate a stelle intermedie, mentre gli spettri delle spirali e irregolari mostrano righe di assorbimento di stelle giovani, ma anche righe di emissione caratteristiche delle [[regione H II|regioni H II]]. Questo ci dà informazioni sulla composizione della galassia.

Nelle spirali, le righe di emissione di formazione stellare sono abbastanza strette
### Mezzo interstellare
Si nota una correlazione fra la classe galattica e l'abbondanza di [[Mezzo interstellare]]. Le galassie ellittiche e lenticolari sono povere di ISM e anche il loro bulge tende ad averne poco, al di là del vero e proprio nucleo galattico dove si accumula gas con facilità. Le galassie a spirale invece sono molto più ricche di ISM e la frazione di gas e polvere aumenta nei tipi più tardi di spirali (verso Sd/SBd). Il gas è ancora più comune in galassie nane e irregolari.
### Relazioni strutturali
Laddove le stelle possiedono una relazione strutturale ben descritta con il [[Diagramma Hertzsprung-Russell]], le galassie non hanno una relazione così universale e quelle che esistono sono più ristrette e di interpretazione più difficile. Queste relazioni collegano quantità dipendenti dalla distanza a quantità indipendenti da essa e dunque possono essere usate come stimatori di distanza, da cui la loro importanza.

Per le galassie spirali, è nota la [[Relazione Tully-Fisher]], mentre le per le ellittiche vale la [[Relazione del piano fondamentale]]. I bulge sono particolari in quanto hanno relazioni strutturali proprie, diverse dal resto della galassia. Si dividono in due categorie:
1. I bulge *classici* sono tipici delle lenticolari e delle spirali dei primi tipi e hanno relazioni strutturale simili alle galassie ellittiche.
2. I *pseudobulge* sono tipici delle spirali degli ultimi tipi e hanno profili esponenziali e cinematica più semplici, dato che ruotano con il disco e questa rotazione li appiattisce.