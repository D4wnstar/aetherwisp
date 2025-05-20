---
wiki-publish: true
aliases:
  - riga di assorbimento
  - riga di emissione
  - larghezza equivalente
---
Le **righe** o **linee spettrali** sono bande di luce in un intervallo ristretto di lunghezze d'onda in cui il flusso è considerevolmente più basso o più alto. Nel primo caso si parla di **righe di assorbimento**; nel secondo di **righe di emissione**. Nel grafico del [[flusso energetico]] si vedono come valli o picchi nella funzione, o come righe più scure o chiare se visualizzate come spettro arcobaleno.

Le linee di assorbimento accadono quando ho una sorgente calda che sto osservando e nel mezzo c'è uno stato di materia non completamente opaca e non completamente [[ionizzazione|ionizzata]] che sta assorbendo la luce. In genere, ci sono due fenomeni che creano le linee di assorbimento:
1. **Assorbimento**: il [[Photon]] viene assorbito da un [[elettrone]], che passa ad uno [[stato]] quantistico eccitato. Se la densità è sufficientemente alta, come nell'atmosfera di una [[Stella]], l'atomo eccitato colpisce a breve un altro [[Atom]], diseccitandosi collisionalmente tramutando l'energia assorbita in energia cinetica.
2. **Scattering**: l'atomo eccitato si diseccita radiativamente, ridirigendo il fotone in una direzione casuale in un angolo solido.

Può succedere anche l'effetto contrario, ossia *linee di emissione*, per le stesse ragioni, ma al contrario. Inoltre, le linee di emissione possono anche essere causate da **fluorescenza**. Questo è tipico delle [[Regione H II|regioni H II]].

Il centro di una riga spettrale coincide con una transizione atomica ben precisa, traslata di una certa quantità $\Delta\lambda$. Tale spostamento è spiegabile in funzione dell'[[effetto Doppler]]. Nel caso di velocità non [[Lorentz transformation|relativistiche]] ($v\ll c$) si ha
$$z=\frac{\Delta\lambda}{\lambda}\simeq\frac{v}{c}\tag{1}$$
La quantità $z$ viene chiamata **[[Redshift]]** nel caso lo spostamento sia verso il rosso (aumento di $\lambda$) o **blueshift** nel caso contrario.
### Larghezza
In teoria, una riga è un picco infinitesimo descrivibile come una [[delta di Dirac]]. In pratica, si osserva una curva liscia con una certa larghezza (vedi sotto). Come tutte le distribuzioni, la definizione di larghezza è sostanzialmente arbitraria e dipende da cosa si sta cercando di esprimere.

Si definisce **larghezza equivalente** (EW) di una riga di assorbimento come la larghezza di quella riga immaginaria che, assorbendo tutti i fotoni del continuo in un intervallo $\Delta\lambda$ e nessun fotone al di fuori di esso, produca esattamente lo stesso assorbimento (in termini di energia) della riga in questione. Nel caso di righe di emissione, si usa la larghezza che produce lo stesso eccesso di energia. La EW non è una misura utile perché non tiene conto della profondità della riga.

Un'altra quantità più utile è la **Full-Width Half-Maximum** (FWHM), dove si misura la larghezza della banda a metà del massimo di assorbimento/emissione. La EW è comunque usata perché richiede meno dati ed è più resistente a rumore e imprecisioni.

![[Schema righe spettrali|80%|center]]

### Allargamento delle righe
Come accennato sopra, le misure di righe spettrali danno luogo a picchi e valli con una certa pendenza. Le ragioni sono diverse, ma sono tutte o di natura quantistica, o di natura statistica. Infatti, la riga che vediamo è l'aggregato di innumerevoli [[particella|particelle]] che vanno a formare i corpi celesti. Le lunghezze d'onda di transizione, poi, sono tali nel sistema di riferimento della particella, quindi risulteranno diverse in quello dell'osservatore.

Dei seguenti, l'allargamento naturale e quello termico sono quelli con effetto maggiore e universale. L'allargamento della maggior parte delle righe spettrali può essere spiegato con buona precisione come la somma di questi due.
#### Allargamento naturale
La banda è $\frac{\Delta\lambda}{\lambda}=\frac{v}{c}$, ossia misurare $\Delta\lambda$ ci richiede di misurare la velocità di una particella. Per la [[disuguaglianza di Heisenberg]], è impossibile farlo con precisione arbitraria senza incontrare altri problemi, quindi ci sarà necessariamente una certa dispersione.
#### Allargamento termico
I moti caotici delle particelle che compongono gas caldi come le [[Stella|stelle]] causano variazioni di lunghezza d'onda per effetto Doppler. In un gas a temperatura $T$ di molecole di massa $Am_{p}$, con $A$ il [[Atom|numero di massa atomica]] e $m_{p}$ la massa del [[protone]], esse si muovono isotropicamente (e quindi sulla linea di vista) a
$$v\sim\sqrt{\frac{kT}{Am_{p}}}$$
che messa nella $(1)$ dà un'allargamento.
#### Allargamento di pressione/collisione
Gli elettroni in gas densi, come le atmosfere stellari, sono talmente vicini da loro che le l'emissione di fotoni va a perturbare atomi vicini.
#### Allargamento per micro- e macro-turbolenze
I moti turbolenti, sia su piccola che grande scala, dei gas, questi ultimi in genere i moti convettivi sulle superfici delle stelle, hanno una velocità caratteristica. Questa velocità causa un effetto Doppler che tramite la $(1)$ causa allargamento. Paragonabili agli effetti termici.
#### Allargamento per rotazione stellare
La rotazione fa si che metà della stella si stia allontanando da noi (e quindi redshift), mentre l'alta metà si avvicina (blueshift). Più veloce è la rotazione, più forte è l'allargamento. C'è inoltre un legame biunivoco tra allargamento e distanza dall'asse di rotazione. È rilevante solo per stelle con rotazioni eccezionali, come le [[Stella di neutroni|stelle di neutroni]].
#### Allargamento per venti stellari
Stelle che emettono forti venti stellari causano allargamenti sempre per effetto Doppler. Il gas che si muove verso l'osservatore genera assorbimento blueshiftato e quella che va in altre direzioni causa emissione redshiftata. Il profilo creato da questo allargamento è caratteristico e prende il nome di *P-Cygni*, dal nome della stella esemplare di questo fenomeno.
#### Allargamento per moti stellari
[[Ammasso stellare|Ammassi stellari]] molto lontani appaiono a noi come punti singoli. Alcune stelle nel cluster possono muoversi verso di noi (blueshift), altre lontane da noi (redshift) e la combinazione di questi moti è, ancora una volta per effetto Doppler, una causa di allargamento. L'effetto è molto diverso se il moto è ordinato (come in una [[Galassia]] a spirale) o disordinato (come in una galassia ellittica).
#### Allargamento di moti di gas caldi
I [[Quasar]] e in generale molti [[Nucleo galattico attivo|AGN]] eiettano gas a velocità estreme (anche $\sim10,000$km/s) che causano distorsioni nello spettro per effetto Doppler. Questo si applica solo per linee di emissione.
#### Allargamento per effetto Zeeman, struttura fine e isotopi
È noto dalla fisica atomica che in alcuni casi, gli [[Equazione agli autovalori|autostati]] di energia si spezzano in più stati molto vicini fra loro ma comunque distinti, come per la [[struttura fine]] dell'idrogeno. L'allargamento naturale o la risoluzione insufficiente del telescopio può far ammassare questi stati in unica riga, che apparirà come più (di solito tre) picchi vicini o una curva molto ampia. L'[[effetto Zeeman]] in particolare dipende da forti campi magnetici.