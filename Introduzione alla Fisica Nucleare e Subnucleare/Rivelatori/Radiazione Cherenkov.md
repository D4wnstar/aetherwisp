---
wiki-publish: true
aliases:
  - effetto Cherenkov
  - angolo di emissione di Cherenkov
---
La **radiazione Cherenkov** o **effetto Cherenkov** è un fenomeno di [[radiazione]] legato alle proprietà dielettriche del materiale che avviene quando la velocità di propagazione di una [[Particle]] [[Electric charge|carica]] in un mezzo è maggiore alla [[velocità della luce]] in quel mezzo. La particella emette radiazione dal colore azzurro in un cono che si espande ad un angolo ben definito attorno alla sua traccia.

Causa una perdita ridotta di energia, ma è utile per misurare la velocità delle particelle.
### Meccanismo
Consideriamo un mezzo con [[indice di rifrazione]] $n(\omega)$. La particella in sé si propaga a velocità $c/n$. Se la velocità della particella è $\beta\ll c/n$, allora non vi è perdita di energia da parte della particella, ma se $\beta> c/n$ il materiale polarizzato comincia ad emettere radiazione. Quando la particella carica passa al suo interno, il [[electric field|campo elettrico]] generato da essa sposta i centri di gravità delle cariche positive e negative degli [[Atom|atomi]] del mezzo, creando [[Electric dipole|dipoli elettrici]] che [[polarizzazione|polarizzano]] il mezzo. L'emissione è causata dalla polarizzazione e depolarizzazione del mezzo, che genera lungo la traccia della particella una serie di onde sferiche il cui [[inviluppo]] costituisce un [[fronte d'onda]] conico. Questo fenomeno è equivalente al boom supersonico o alla formazione di una scia da parte di una barca che si muove a velocità maggiore delle onde del mare.

L'apertura angolare $\theta_{C}$ del fronte d'onda conico è detto **angolo di emissione di Cherenkov** e, rispetto alla direzione di moto della particella, è
$$\cos\theta_{C}=\frac{1}{n\beta}$$
da cui segue che deve essere $\beta>1/n$, quindi il fenomeno avviene solo se la velocità della particella è maggiore di quella della luce nel mezzo, come già osservato.

> [!info] Risultato
> Sapendo l'indice di rifrazione, misurare $\theta_{C}$ equivale a misurare la velocità della particella, estraendola da $\beta$. Maggiore è l'angolo, maggiore è la velocità.

La radiazione Cherenkov è inversamente proporzionale alla lunghezza d'onda della particella, per cui viene emessa uno spettro continuo a cavallo dell'ultravioletto e della luce visibile, con un picco a 420 mm. Per questo, la radiazione Cherenkov è visible a occhio nudo e appare blu/azzurra.
#### Perdita di energia
La perdita di energia per radiazione Cherenkov dipende dal numero di fotoni emessi per unità di percorso. Questi a loro volta dipendo da $\theta_{C}$ (infatti si ha $dN/dx\propto \sin^{2}\theta_{C}$). Risulta che l'energia persa per unità di percorso è
$$\frac{dE}{dx}\simeq z^{2}\sin^{2}\theta_{C}$$
solitamente misurato in [[Elettronvolt|keV]]/cm, mille volte minore della [[Potere frenante|perdita per collisione]]. Per questo, è possibile trascurarla senza grande errore.
### Rivelatori
L'angolo di emissione può essere misurato tramite uno schermo fotosensibile su cui "impatta" il cono della radiazione. Dal raggio della circonferenza misurata sullo schermo, possiamo ricondurci all'angolo di emissione.

Per causare la radiazione Cherenkov in sé, qualunque mezzo trasparente può essere usato come [[rivelatore]] Cherenkov, come per esempio acqua o plastica trasparente, dato che l'unica cosa che ci interessa è l'indice di rifrazione. Ciò rende possibile costruire rivelatori Cherenkov molto grandi a basso costo usando, ad esempio, una piscina d'acqua entro il quale si immerge l'emettitore (come anche accade nei reattori nucleari moderati ad acqua).

Alla minima velocità per emettere radiazione Cherenkov $\beta_{s}$ vale
$$\gamma_{s}=\frac{1}{\sqrt{1-\beta_{s}^{2}}}=\frac{n}{\sqrt{n^{2}-1 }}$$
quindi prendendo un materiale con $n\sim1$ (come un gas ad opportuna pressione), è possibile costruire un rivelatore con soglia estremamente alta, che è utile per discriminare particelle con massa diversa (per esempio misurando $\theta_{C}$ e impulso in contemporanea). Questo diventa particolarmente utile per particelle ultra-relativistiche, dato che la Bethe-Bloch non è molto buona a discriminare masse in questo regime.