---
wiki-publish: true
---
La **scala delle distanze cosmica** è la successione di metodi usati in astronomia per misurare le distanze di corpi celesti. La misura diretta della distanza di un oggetto è possibile sono per oggetti molto vicini alla Terra (in scala cosmica), il che vale a dire meno di $\sim1000$ [[Parsec]] grazie al telescopio Gaia.

Al di là di questo raggio, si devono usare [[Candela standard|candele standard]] o [[Regolo standard|regoli standard]]. Alternativamente, le distanze sono in genere misurate a partire da relazioni che collegano due quantità osservate: una dipendente dalla distanza, come [[Luminosità]] o diametro, e una indipendente, come [[Colore]] o periodo di oscillazione (per stelle variabili). Queste relazioni agiscono di fatto come candele e regoli standard e sono preferite, dato che è più facile usare una relazione che cercare un oggetto di proprietà note a priori e perché può essere usata su numerosi oggetti, diminuendo l'errore sulla misura.
## Metodi
### Indicatori primari
Gli **indicatori primari di distanza** sono metodi o oggetti che possiamo usare o individuare nella [[Via Lattea]] o al più in [[Galassia|galassie]] vicinissime. Questi metodi possono essere calibrati usando il [[Diagramma Hertzsprung-Russell|diagramma HR]] delle [[Stella|stelle]] osservate e dunque anche se fossero osservabili da più lontano, non possono essere spinti a luoghi così lontani da non riuscire a osservarne il diagramma HR.
#### Parallasse
L'osservazione del parallasse è il metodo più diretto per la misura della distanza, ma è applicabile solo a [[Stella|stelle]] vicine ($<1000$ parsec). Le stelle vicine mostrano un moto apparente con periodo annuale rispetto alle stelle "fisse" di sfondo. La stella verrà vista muoversi su un ellisse con semiasse maggiore di diametro angolare pari all'angolo che l'orbita terrestre sottende se osservata da quella stella. Chiamiamo **parallasse** $\pi$ l'angolo corrispondente al semiasse maggiore dell'ellisse tracciata dalla stella. In radianti, vale la relazione $\pi d=1$ AU, con $d$ la distanza.

![[Schema Distanza con parallasse|100%]]

#### Metodo dell'ammasso mobile
Per [[Ammasso stellare|ammassi stellari]] vicini (come quello delle Iadi), si può misurare la velocità di recessione media $v$ in funzione della velocità media delle stelle lungo la linea di vista (tramite lo [[effetto Doppler|spostamento Doppler]] delle [[Riga spettrale|righe spettrali]]). Dato che l'ammasso è vicino, possiamo misurare una diminuzione della sua diametro medio angolare $\theta$. Se varia di $\Delta\theta$ in un intervallo $\Delta t$ e gli angoli sono piccoli, si ha circa
$$d\simeq v \Delta t \frac{\theta}{\Delta\theta}$$
#### Fit della sequenza principale
Per stimare la distanza di ammassi stellari lontani si usa un metodo noto come *fit della sequenza principale*. Misurando il colore per stimare la temperatura e la [[Magnitudine]] apparente come luminosità, è possibile produrre un [[Diagramma Hertzsprung-Russell]] che mostri la [[Sequenza principale]] delle stelle dell'ammasso. Riscalando questo in verticale, è possibili ricondursi al diagramma HR dell'ammasso delle Iadi (o di qualunque ammasso di distanza nota) e quindi stimare la distanza.
#### Stelle variabili
Esistono alcune stelle, dette [[stella variabile|stelle variabili]], il cui inviluppo esterno è instabile e la cui luminosità varia molto regolarmente nel tempo. I tipi più importanti di stelle variabili sono le [[Cefeide|Cefeidi]] e le [[RR-Lyrae]]. In particolare, sono note per mostrare una stretta correlazione tra luminosità e periodo di oscillazione, che è indipendente dalla distanza. Ciò ci da una relazione per poter stimarne la distanza. Le Cefeidi in particolare sono molto luminose e possono anche essere osservate in [[Galassia|galassie]] vicine, fino a qualche decina di megaparsec.
### Indicatori secondari
Gli **indicatori secondari di distanza** sono quegli oggetti o metodi che ci permettono di misurare distanza anche in scale cosmologiche, nelle centinaia di megaparsec e oltre. Devono essere calibrati su galassie vicine, ma non così vicine da riuscire a ricostruire il diagramma HR.
#### Relazione Tully-Fisher
Per le [[Classi galattiche|galassie a spirale]] si usa la [[Relazione di Tully-Fisher]], che lega luminosità e velocità di rotazione del disco galattico.
#### Relazione del piano fondamentale
Per le [[Classi galattiche|galassie ellittiche]] si usa la [[Relazione del piano fondamentale]], che lega [[Raggio effettivo]], [[Brillanza superficiale]] e dispersione di velocità.
#### Fluttuazioni di brillanza superficiale
Sempre per le ellittiche si usa un metodo detto **fluttuazioni di brillanza superficiale** che consiste nel misurare la differenza di luminosità tra pixel di un sensore CCD: se in un pixel cade la luce di $N$ stelle, allora la fluttuazione tra pixel sarà di $\sqrt{N}$. Siccome $N\propto d^{2}$, possiamo estrarne una stima di distanza.
#### Supernove di tipo 1a
Le [[Supernova|supernove di tipo Ia]] sono una candela standard particolarmente importante. La loro luminosità non è proprio costante in tutti gli eventi, ma le deviazioni di questa correlano con l'ampiezza della curva di luce e possono essere corrette. La difficoltà sta nel trovarle al momento giusto: questi eventi rimangono visibili per qualche mese prima di scomparire per sempre.