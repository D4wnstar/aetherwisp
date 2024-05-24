La **radiazione Cherenkov** è un fenomeno di radiazione legato alle proprietà dielettriche del materiale che avviene quando la velocità di propagazione di una [[particella]] in un mezzo è maggiore alla [[velocità della luce]] in quel mezzo.

Causa una perdita ridotta di energia, ma è utile per misurare la velocità delle particelle.
### Meccanismo
Consideriamo un mezzo con [[indice di rifrazione]] $n(\omega)$. Quando una particella carica passa al suo interno, il campo elettrico generato da essa [[polarizzazione|polarizza]] il mezzo stesso mentre essa si propaga a velocità $c/n$. Se la velocità della particella è $\beta\ll c/n$, allora non vi è perdita di energia da parte della particella, ma se $\beta> c/n$ il materiale polarizzato comincia ad emettere radiazione. Questa emissione è causata dalla polarizzazione e depolarizzazione del mezzo, che genera lungo la traccia una serie di onde sferiche il cui [[inviluppo]] costituisce un [[fronte d'onda]] conico. Questo fenomeno è equivalente al boom supersonico o alla formazione di una scia da parte di una barca che si muove a velocità maggiore delle onde del mare.

Gli [[atomo|atomi]] del mezzo si deformano a causa del campo elettromagnetico della particella e i centri di gravità della carica positiva e negativa dell'atomo non coincidono più. Con velocità sufficientemente alta (oltre la velocità della luce nel mezzo), questa differenza crea una polarizzazione a simmetria assiale e gli atomi agiscono come singoli dipoli elettrici che creano campi di dipolo. Questo campo di dipolo è quello responsabile per l'emissione Cherenkov.

L'apertura angolare $\theta_{C}$ del fronte d'onda conico rispetto alla direzione di moto della particella è
$$\cos\theta_{C}=\frac{1}{n\beta}$$
da cui segue che
- deve essere $\beta>1/n$, quindi il fenomeno avviene solo per questi valori.
- sapendo l'indice di rifrazione, misurare $\theta_{C}$ equivale a misurare la velocità della particella (estraendola da $\beta$).

La radiazione Cherenkov è inversamente proporzionale alla lunghezza d'onda della particella, per cui viene emessa uno spettro continuo a cavallo dell'ultravioletto e della luce visibile, con un picco a 420 mm. Per questo, la radiazione Cherenkov è visible a occhio nudo e appare blu/azzurra.
#### Perdita di energia
La perdita di energia per radiazione Cherenkov dipende dal numero di fotoni emessi per unità di percorso. Questi a loro volta dipendo da $\theta_{C}$ (infatti si ha $dN/dx\propto \sin^{2}\theta_{C}$). Risulta che l'energia persa per unità di percorso è
$$\frac{dE}{dx}\simeq z^{2}\sin^{2}\theta_{C}$$
solitamente misurato in [[Elettronvolt|keV]]/cm$^{2}$, quindi molto minore alla perdita per collisione.
### Rivelatori
Qualunque mezzo trasparente può essere usato come [[rivelatore]] Cherenkov, come per esempio acqua o plastica trasparente. Ciò rende possibile costruire rivelatori Cherenkov molto grandi usando ad esempio una vasca d'acqua (come anche accade nei reattori nucleari moderati ad acqua).

Al valore di soglia per $\beta_{s}$ vale
$$\gamma_{s}=\frac{1}{\sqrt{1-\beta_{s}^{2}}}=\frac{n}{\sqrt{n^{2}-1 }}$$
quindi prendendo un materiale con $n\sim1$ (come un gas ad opportuna pressione), è possibile costruire un rivelatore con soglia estremamente alta, che è utile per discriminare particelle relativistiche con massa diversa (per esempio misurando $\theta_{C}$ e impulso in contemporanea).