---
aliases:
  - formula di Bethe-Bloch
  - energy straggling
  - lunghezza di radiazione
---
Lo **stopping power** $S$ è la capacità di un materiale di rallentare una [[particella]] che ci passa attraverso mediante l'interazione con la materia, diminuendo la sua energia. Matematicamente, è la media della diminuzione di energia $E$ della particella per unità di spazio $x$, inteso come lo spazio occupato da materia entro il quale passa la particella:
$$S(E)=- \left\langle\frac{dE}{dx}\right\rangle$$
per un sistema del tipo
![[Schema Rivelatore generico|40%|center]]
### Energy straggling
L'esatto valore della diminuzione di energia fluttua con una distribuzione gaussiana, come si trova anche sperimentalmente. Infatti, la perdita di energia è dovuta alla molte collisioni con gli elettroni del mezzo. Dato che l'energia trasferita in una collisione non è costante e dipende dai parametri dell'urto, otteniamo una distribuzione di perdite di energia. L'esatta distribuzione in realtà non è perfettamente gaussiana (si osservano distribuzione poissoniane), ma per il [[teorema del limite centrale]], avendo una statistica sufficientemente ampia (ossia un materiale abbastanza spesso), converge ad una gaussiana. Questo fenomeno è detto **energy straggling**.
### Perdita per collisione
In fisica nucleare e delle particelle, si può misurare lo stopping power di un materiale dovuto alle *collisioni* (o per *ionizzazione*) usando la **formula di Bethe-Bloch**:
$$S(E)=- \left.\frac{dE}{dx}\right|_{\text{ion}}=0.15 \frac{Z}{A}\rho \frac{z^{2}}{\beta^{2}}\left[\ln\left(\frac{2\beta^{2}\gamma^{2}mc^{2}E_{M}}{I^{2}}\right)-2\beta^{2}-\delta(\gamma)\right]$$
o la sua forma più semplice, detta **formula di Bohr**, che trascura alcune correzioni e funziona comunque bene per atomi pesanti
$$S(E)=- \frac{dE}{dx}=\underbrace{4\pi r^{2}_{e}mc^{2}}\limits_{1} \underbrace{\frac{N_{A}Z\rho}{A} \frac{z^{2}}{\beta^{2}}}\limits_{2}\underbrace{\ln\left(\frac{mc^{2}\beta^{2}\gamma^{2}}{lv}\right)}\limits_{3}$$
dove
- $Z$ è il [[Atomo|numero atomico]].
- $A$ è il [[Atomo|numero di massa atomica]].
- $\beta$ e $\gamma$ rappresentano il [[limite relativistico]].
- $\rho$ è la densità del materiale.
- $z$ è la carica della particella.
- $E_{M}$ è l'energia massima trasferibile in un urto.
- $I$ è il *potenziale di eccitazione*.

Il $0.15$ proviene dal termine di *perdita di energia per ionizzazione* $4\pi mc^{2}N_{A}r_{e}^{2}=0.3$ [[Elettronvolt|MeV]] cm$^{2}$/g diviso per due, con $N_{A}$ il [[numero di Avogadro]]. Il termine logaritmico, che cresce lentamente, diventa grande solo per $\gamma$ molto grandi, ossia in regimi ultrarelativistici.

Dato che $\rho$ è il parametro più semplice da manipolare, è comune usare la formula di Bethe-Bloch in una forma alternativa che porta fuori il termine di densità. Definendo $X=\rho x$, vale
$$- \frac{dE}{dX}=\frac{1}{\rho} \frac{dE}{dx}$$
dove $[X]=g/cm^2$. Questa forma non rappresenta più la perdita di energia per distanza oltrepassata nel materiale, bensì una distanza pesata per la densità.

Le uniche due proprietà intrinseche della particella da cui la formula dipende sono $z$ e $m$, il che significa che il comportamento in termini di *stopping power* di un materiale non distingue tra particelle con stessa massa e carica. La massa è anche presente solo nel termine logaritmico, il che vuol dire che è rilevante solo in casi ultrarelativistici. Per velocità minori, è importante solo la carica, dato che la variazione del logaritmo può essere trascurata[^1]. Nel caso $z=1$, la decaduta di energia ha una forma del genere:

![[Grafico Stopping power per z=1|80%|center]]
*L'asse $x$ è in scala log10*

Lo stopping power ha un minimo, per poi risalire nuovamente per effetti relativistici. Una particella con diminuzione di energia minima viene detta *minimum ionizing particle* (o *MIP*) e per tutte le MIP vale che $\beta\gamma\simeq3$.
### Perdita per radiazione
Lo stopping power relativo ad un [[elettrone]] non è ben descritto dalla formula di Bethe-Bloch e richiede una derivazione diversa. Questo è dovuto al fatto che gli elettroni del fascio sono identici a quelle del bersaglio e anche da quanto piccola è la loro massa. Infatti, per gli elettroni la perdita di energia dovuta a radiazione (in particolare [[bremmstrahlung]]) è molto più importante.

La perdita di energia per radiazione di una particella di energia $E_{0}$ è
$$- \left.\frac{dE}{dx}\right|_{\text{rad}}=\frac{E}{L_{R}}$$
ovvero
$$E(x)=E_{0}e^{-x/L_{R}}$$
con
$$L_{R}^{-1}=\left[\ln\left(\frac{183}{Z^{\frac{1}{3}}}\right)\right] \frac{4 r_{0}^{2}N_{A}Z^{2}\alpha\rho}{A}$$
dove
- $r_{0}$ è il raggio classico dell'elettrone.
- $N_A$ è il [[numero di Avogadro]].
- $\alpha$ è la [[costante di struttura fine]].
- $\rho$ è la densità del materiale.
- $Z$ è il numero atomico del materiale.
- $A$ è il numero di massa atomica del materiale.

$L_{R}$ si dice **lunghezza di radiazione** ed è la distanza alla quale l'energia dell'elettrone si diminuisce a $1/e$ di quella iniziale. È fortemente dipendente dal numero atomico del mezzo.

L'andamento della perdita di energia per radiazione va come

![[Grafico Stopping power e radiazione|80%|center]]
*L'asse $x$ è in scala log10*

dove $E_{C}$ è l'energia critica alla quale la perdita per collisione e radiazione è uguale. È chiaro che la perdita di energia per bremmstrahlung, essendo esponenziale, è molto più veloce di quella per ionizzazione. Alcuni esempi di $L_{R}$ per certi materiali sono 36 cm per $H_{2}O$, 9 cm per $Al$, 1.7 cm per $Fe$ e 0.56 cm per $Pb$.

Lo [[spettro di energia]] dei [[fotone|fotoni]] emessi va da 0 a $E_{0}$ con $\left\langle \theta \right\rangle\simeq mc^{2}/E_{0}$, indipendente dall'energia del fotone emesso. L'energia critica è circa di $\sim600/Z$ MeV.

Dato che la perdita per radiazione è $\propto 1/m_{e}^{2}$ nel caso dell'elettrone, per particelle di massa $M$ si ha che è $\propto1/M^{2}$. Ciò significa che la perdita di energia per radiazione è rilevante soltanto per particelle di massa molto piccola (appunto come elettroni) o in casi ad altissima energia (ultrarelativistici).


[^1]: Dato che si tratta di un prodotto, il logaritmo in sé non può essere trascurato (bisognerebbe avere una somma). È però possibile trascurare la variazione del logaritmo e quindi rimanere con una costante.