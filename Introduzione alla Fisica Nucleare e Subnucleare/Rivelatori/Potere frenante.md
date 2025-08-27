---
wiki-publish: true
aliases:
  - formula di Bethe-Bloch
  - energy straggling
  - lunghezza di radiazione
  - stopping power
  - perdita per collisione
  - perdita per ionizzazione
  - perdita per radiazione
---
Il **potere frenante** o **stopping power** $S$ è la capacità di un materiale di rallentare una [[Particle]] che ci passa attraverso mediante l'interazione con la materia, diminuendo la sua energia. Matematicamente, è la media della diminuzione di energia $E$ della particella per unità di spazio $x$, inteso come lo spazio occupato da materia entro il quale passa la particella:
$$S(E)=- \left\langle\frac{dE}{dx}\right\rangle$$
per un sistema del tipo

![[Schema Rivelatore generico|40%|center]]

Esiste più di un tipo di meccanismo di perdita di energia.
### Energy straggling
La perdita di energia è dovuta a molte collisioni con gli elettroni del mezzo entro il quale il fascio incidente sta entrando. Dato che l'energia trasferita in una collisione dipende dai parametri dell'urto, si trova che il numero di urti, e quindi l'energia persa, seguirà un [[distribuzione poissoniana]]. Per il [[teorema del limite centrale]], se il numero di urti è abbastanza alto (ossia il materiale è abbastanza spesso), la statistica converge ad una gaussiana. Questo fenomeno è detto **energy straggling**. Per materiali fini, si osserva invece una [[distribuzione di Landau e Vavilon]].
### Perdita per collisione
Consideriamo una particella carica pesante che impatta con un elettrone legato. Assumiamo che la particella abbia velocità costante e molto maggiore a quella dell'elettrone a modo di poter considerare quest'ultimo come approssimativamente fermo. Inoltre, assumiamo che l'impulso trasferito sia piccolo abbastanza da non causare una deviazione tangibile nella traiettoria della particella.

La componente trasversa del campo elettrico è $\vec{E}_{\perp}$ e l'impulso trasverso trasferito all'elettrone dalla forza $\vec{F}=-e\vec{E}$ della particella incidente è
$$\Delta\vec{p}=\int\vec{F}dt=-e\int\vec{E}_{\perp}dt=-e\int\vec{E}_{\perp} \frac{dx}{dx/dt}=- \frac{e}{v}\int\vec{E}_{\perp}dx$$
Se consideriamo un cilindro infinitamente esteso con asse coincidente alla traiettoria della particella e raggio pari al *parametro di impatto* $b$, il [[teorema di Gauss]] ci dice che il flusso $\Phi$ del campo elettrico attraverso la superficie del cilindro è
$$\Phi(\vec{E})=\int_{S}\vec{E}\cdot d\vec{S}=2\pi b\int\vec{E}_{\perp}dx=\frac{ze}{\varepsilon_{0}}$$
da cui
$$|\Delta\vec{p}|=\Delta p=\frac{ze^{2}}{2\pi b\varepsilon_{0}v}=\left(\frac{ze^{2}}{4\pi b^{2}\varepsilon_{0}}\right)\left(\frac{2b}{v}\right)$$
dove la prima parentesi è la [[Electromagnetism|forza Coulombiana]] nel punto di massimo avvicinamento e la seconda è il *tempo caratteristico dell'interazione*. L'energia cinetica acquistata dall'elettrone sarà
$$E_{x}(b)=\frac{\Delta p^{2}}{2m}=\frac{z^{2}e^{4}}{8\pi^{4}\varepsilon_{0}b^{2}mv^{2}}=\frac{2mc^{2}r_{c}^{2}z^{2}}{\beta^{2}b^{2}}$$
da qui possiamo affermare che:
- l'energia trasferita diminuisce all'aumentare di $b$.
- le particelle incidenti perdono meno energie più sono veloci.
- la dipendenza dall'inverso della massa suggerisce che gli impatti con i [[Nucleo atomico|nuclei]] sono trascurabili, dato che sono molto più massivi degli elettroni.

Se vogliamo considerare la perdita di energia passando in uno spessore $dx$ di un materiale con $N_{0}$ elettroni per unità di volume, allora dobbiamo considerare il contributo di tutti gli elettroni ad una distanza tra $b$ e $b+db$, che sarà pari alla somma di tutti gli $N_{0}2\pi b\,db\,dx$ contributi, che è
$$-dE(b)=N_{0}2\pi b\,db\,dx\,E_{x}(b)$$
e integrando in $dx$ fra i limite inferiore e superiore del parametro d'impatto
$$- \frac{dE}{dx}=\int_{b_{min}}^{b_{max}}2\pi N_{0}E_{x}(b)N_{0}z\,db=\frac{4\pi N_{0}zre^{2}mc^{2}z^{2}}{\beta^{2}}\ln\left(\frac{b_{max}}{b_{min}}\right)$$
I limiti $b_{max}$ e $b_{min}$ devono essere presi con cognizione di causa, dato che modificano il tempo caratteristico dell'interazione:
- possiamo assumere $b_{max}$ come $\sim \tau v/\nu$, dove $\tau$ è il tempo tipico di interazione, $v$ è la velocità della particella e $\nu$ è la frequenza orbitale dell'elettrone. Questo segue dal [[principio di invarianza adiabatica]], secondo il quale la perturbazione all'elettrone deve risolversi in tempi piccoli rispetto al periodo orbitale dell'elettrone $T=1/\nu$.
- $b_{min}$ non può essere minore del raggio dell'elettrone, dato dalla [[Formula di de Broglie|lunghezza d'onda di De Broglie]]. L'impulso dell'elettrone è $p=\beta\gamma mc$, ma $b\geq\lambda$, quindi $b_{min}\sim h/\beta\gamma mc$.

Chiamando
$$N_{0}=\frac{n_{mol}N_{A}}{V}=\frac{\rho V}{VA}N_{A}=\frac{\rho N_{A}}{V}$$
con $N_{A}$ il [[Avogadro number]], $\rho$ la densità del materiale e $A$ il [[Atom|numero di massa atomica]] del materiale, possiamo esprimere la **formula di Bohr**:
$$S(E)=- \frac{dE}{dx}=4\pi r^{2}_{e}mc^{2} \frac{N_{A}Z\rho}{A} \frac{z^{2}}{\beta^{2}}\ln\left(\frac{mc^{2}\beta^{2}\gamma^{2}}{\nu h}\right) \quad \left[\frac{\text{MeV}}{\text{cm}}\right]$$
che può essere espressa in funzione dello *spessore massiccio* $X=\rho x$, come
$$S(E)=- \frac{dE}{dX}=0.3 \frac{z^{2}Z}{\beta^{2}A}\ln\left(\frac{mc^{2}\beta^{2}\gamma^{2}}{I}\right) \quad \left[\frac{\text{MeV}}{\text{g cm}}\right]$$
dove le costanti sono espressi in forma numerica e
- $I=\nu h$ è il **potenziale di eccitazione**.
- $Z$ è il [[Atom|numero atomico]] del materiale.

Una forma più corretta e accurata che tiene conto di effetti quantistici è la **formula di Bethe-Bloch**:
$$\boxed{S(E)=- \left\langle \left.\frac{dE}{dx}\right|_{\text{ion}}  \right\rangle=0.3 \frac{Z}{A}\rho \frac{z^{2}}{\beta^{2}}\left[\ln\left(\frac{\beta^{2}\gamma^{2}mc^{2}}{I}\right)-\beta^{2}-\frac{\delta(\gamma)}{2}\right]}$$
e anche nello spessore massiccio:
$$\boxed{S(E)=- \left\langle \left.\frac{dE}{dX}\right|_{\text{ion}} \right\rangle=0.3 \frac{Z}{A} \frac{z^{2}}{\beta^{2}}\left[\ln\left(\frac{\beta^{2}\gamma^{2}mc^{2}}{I}\right)-\beta^{2}- \frac{\delta(\gamma)}{2}\right]}$$
dove $\delta(\gamma)$ è una correzione di densità dovuta alla [[polarizzazione]] del mezzo. Dipende dalla densità e limita la crescita relativistica al punto da poterla considerare costante.

Il $4\pi mc^{2}N_{A}r_{e}^{2}=0.3$ MeV cm$^{2}$/g viene detto di *perdita di energia per ionizzazione*. Il termine logaritmico, che cresce lentamente, diventa grande solo per $\gamma$ molto grandi, ossia in regimi ultrarelativistici.

> [!info] Risultato
> La formula di Bethe-Bloch descrive la perdita di energia per ionizzazione di una particella incidente. Nella forma di spessore massiccio, è quasi indipendente dall'assorbitore, se si trascura la dipendenza logaritmica contenuta nel potenziale di ionizzazione. Infatti, $Z/A\simeq0.5$ per tutti gli elementi tranne l'idrogeno, per il quale è 1.

> [!info] Osservazione
> Le uniche due proprietà della particella nella formula sono $z$ e $m$, il che significa che un materiale non distingue tra particelle con stessa massa e carica per quanto riguarda il potere frenante. Una volta fissate queste due, la curva ha validità universale. Inoltre, il potere frenante è quadratico nella carica della particella.

 La massa è anche presente solo nel termine logaritmico, il che vuol dire che è rilevante solo in casi ultrarelativistici. Per velocità minori, è importante solo la carica, dato che la variazione del logaritmo può essere trascurata[^1]. Nel caso $z=1$, la decaduta di energia ha una forma del genere:

![[Grafico Stopping power per z=1|80%|center]]
*L'asse $x$ è in scala log10*

Lo stopping power ha un minimo, per poi risalire nuovamente per effetti relativistici. Una particella con diminuzione di energia minima viene detta *minimum ionizing particle* (o *MIP*) e per tutte le MIP vale che $\beta\gamma\simeq3$.

> [!info] Risultato
> La perdita di energia per ionizzazione cambia molto, a parità di impulso, tra particelle diverse, ossia per masse diverse. Questo si vede come una sorta di traslazione sull'asse $x$ della curva, dove più alta è la massa, più alta è la perdita di energia. Comprendere questa alta variabilità è uno strumento chiave per misurare la massa della particella incidente.
### Perdita per radiazione
Lo stopping power relativo ad un [[elettrone]] non è ben descritto dalla formula di Bethe-Bloch. Il motivo è cercarsi nel fatto che gli elettroni del fascio sono identici a quelle del bersaglio e che la loro massa è molto piccola. Infatti, la Bethe-Bloch funzione solo per particelle pesanti. Per gli elettroni è molto più importante la perdita di energia dovuta a radiazione, in particolare dal [[Bremmstrahlung]]. Questa è invece trascurabile nelle particelle pesanti perché la deviazione delle loro traiettorie è molto piccola.

La perdita di energia per radiazione di una particella di energia $E_{0}$ è ben descritta da un'applicazione della [[legge di Beer-Lambert]]:
$$- \left.\frac{dE}{dx}\right|_{\text{rad}}=\frac{E}{L_{R}}$$
ovvero
$$E(x)=E_{0}e^{-x/L_{R}}$$
con
$$L_{R}^{-1}=\ln\left(\frac{183}{Z^{\frac{1}{3}}}\right) \frac{4 r_{0}^{2}N_{A}Z^{2}\alpha\rho}{A}$$
dove
- $r_{0}$ è il raggio classico dell'elettrone.
- $N_A$ è il [[Avogadro number]].
- $\alpha$ è la [[Fine-structure constant]].
- $\rho$ è la densità del materiale.
- $Z$ è il numero atomico del materiale.
- $A$ è il numero di massa atomica del materiale.

$L_{R}$ si dice **lunghezza di radiazione** ed è la distanza alla quale l'energia dell'elettrone si diminuisce a $1/e$ di quella iniziale. È fortemente dipendente dal numero atomico del mezzo.

L'andamento della perdita di energia per radiazione è esponenziale e per alte energie porta ad una perdita di energia molto più importante dell'ionizzazione. A basse energie, invece, la ionizzazione domina di molto. Si dice *energia critica* $E_{C}$ è l'energia alla quale la perdita per collisione e radiazione è uguale. 

![[Grafico Stopping power e radiazione|80%|center]]
*L'asse $x$ è in scala log10*

Alcuni esempi di $L_{R}$ per certi materiali sono 3.6 cm per $H_{2}O$, 9 cm per $Al$, 1.7 cm per $Fe$ e 0.56 cm per $Pb$. Questo evidenzia perché il piombo è uno schermante così buono.

Lo [[spettro di energia]] dei [[Photon|fotoni]] emessi va da 0 a $E_{0}$ con $\left\langle \theta \right\rangle\simeq mc^{2}/E_{0}$, indipendente dall'energia del fotone emesso. L'energia critica è circa di $\sim600/Z$ MeV.

Per particelle di massa $M$ si ha che la perdita per bremmstrahlung è $\propto1/M^{2}$. Ciò significa che la perdita di energia per radiazione è rilevante soltanto per particelle di massa molto piccola (appunto come elettroni) o in casi ad altissima energia (ultrarelativistici).

[^1]: Dato che si tratta di un prodotto, il logaritmo in sé non può essere trascurato (bisognerebbe avere una somma). È però possibile trascurare la variazione del logaritmo e quindi rimanere con una costante.