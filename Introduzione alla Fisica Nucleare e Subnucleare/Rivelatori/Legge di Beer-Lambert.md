---
wiki-publish: true
aliases:
  - coefficiente di assorbimento
---
La **legge di Beer-Lambert** descrive l'attenuazione di un raggio di luce (più correttamente[[Photon|fotoni]]) durante il passaggio attraverso la materia. È una legge esponenziale dalla forma
$$I=I_{0}e^{-\mu x}$$
dove $I_{0}$ è l'intensità del raggio iniziale, $\mu$ è il **coefficiente di assorbimento** e $x$ è lo spazio percorso entro il materiale.
### In fisica delle particelle
Consideriamo un fascio di [[Particle|particelle]] che attraversa un sottile strato di materia. Si distinguono due casi:
1. Le particelle subiscono molte interazioni e in ciascuna perdono un po' di energia, oltre ad essere deviate leggermente. In questo caso, il fascio uscente non sarà più monoenergetico, ma avrà una distribuzione di energie e uno sparpagliamento angolare. Questo comportamento è tipico delle particelle pesanti (s'intende qualunque cosa nelle centinaia di [[Elettronvolt|MeV]] e più).
2. Le particelle non interagiscono o, se interagiscono, spariscono dal fascio incidente, per esempio perché sono assorbite. In questo caso, sia l'energia, sia l'angolo del fascio uscente sono uguali a quelle del fascio entrante. Questo comportamento è tipico dei fotoni.

Il primo caso è meglio descritto dalla [[Potere frenante|formula di Bethe-Bloch]]. Nel secondo caso, per ciascun elemento di spessore $dx$ del materiale, il numero di particelle che interagisce è proporzionale al numero di particelle incidenti $N(x)$ su quello spessore:
$$dN=-N(x)\mu dx$$
dove $\mu$ è detto coefficiente di assorbimento. Integrando, si ha
$$N(x)=N(0)e^{-\mu x}=N(0)e^{- x/\lambda}$$
dove $\lambda$ è detto **cammino libero medio**. Il coefficiente di assorbimento è la probabilità di interazione per unità di cammino, esprimibile come $\mu=N\sigma$, dove $N$ è il numero di [[Sezione d'urto|centri diffusori]] e $\sigma$ è la [[sezione d'urto]]. $\lambda$ è invece la distanza media percorsa prima di subire una collisione.

> [!info] Risultato
> Passando attraverso ad un materiale, un fascio di particelle cariche pesanti non subisce variazioni di intensità (numero di particelle), ma viene degradato energeticamente. Un fascio di fotoni non subisce variazioni di energia, ma il numero di fotoni cala esponenzialmente.

Le particelle cariche pesanti interagiscono principalmente per collisione con [[elettrone|elettroni]] legati, mentre quelle leggere per [[radiazione]].