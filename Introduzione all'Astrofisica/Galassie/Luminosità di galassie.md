Esistono metodi analitici per calcolare l'irradianza emessa da una [[galassia]]. Partiamo cercando di definire il profilo di brillanza superficiale di una galassia, sull'asse maggiore dell'immagine della galassia. Per le [[Classi galattiche|galassie ellittiche]], questo segue in genere una legge di de Vaucouleurs:
$$I(r)=I(0)\exp\left[- \left( \frac{r}{r_{0}} \right)^{0.25}\right]\tag{1}$$
mentre per le galassie a spirale si ha una curva esponenziale
$$I(r)=I(0)\exp\left(- \frac{r}{r_{0}}\right)\tag{2}$$
Spesso questi profili vengono modellati tramite un profilo di Sérsic
$$I(r)=I_{e}\exp \left\{-b_{n} \left[\left(\frac{r}{R_{e}}\right)^{1/n}-1\right]\right\}$$
dove $R_{e}$ è il [[raggio effettivo]]. $I_{e}$ è la brillanza superficiale calcolata in $R_{e}$. $b_{n}$ è un coefficiente sperimentale tabulato in funzione di $n$ e mette in relazione $r_{0}$ e $R_{e}$. Per $n=1$ si ha il profilo $(1)$, mentre per $n=4$ si ha $(2)$. Una misura di $n$ può dare una vaga approssimazione della morfologia.

### Funzione di luminosità delle galassie
Al di là della luminosità di una singola galassia, esistono anche modelli per misurare l'irradianza in funzione della distribuzione di galassie nello spazio. Si consideri un volume $V$ e si dica che il numero di galassie con luminosità nell'intervallo $[L,L+dL]$ è $dN$. Allora la *funzione di luminosità delle galassie* $\Phi(L)$ è definita come $dN=V\Phi(L)dL$. La *funzione di luminosità di Schechter* dà una buona approssimazione della precedente funzione
$$\Phi(L)dL=\Phi_{\star}\left(\frac{L}{L_{\star}}\right)^{\alpha}\exp\left(- \frac{L}{L_{\star}}\right) \frac{dL}{L_{\star}}$$
con $L_{\star}$ è la luminosità galattica caratteristica (la luminosità della galassia brillante tipica) e $\Phi_{\star}$ è la normalizzazione (l'abbondanza tipica delle galassie brillanti). Questa funzione ha forme leggermente diverse in base alla [[Classi galattiche|classe galattica]]:
- Tipo 1: galassie E/S0
- Tipo 2: galassie Sa/Sb
- Tipo 3: galassie Sc/Sd
- Tipo 4: galassie irregolari

Si trova che la luminosità $L$ è proporzionale alla [[Rotazione di una galassia]] alla quarta
$$L\propto v^{4}$$
Possiamo misurare l'irradianza di tutta la galassia come integrale di luminosità per "anelli" della galassia
$$I(r)=\int_{0}^{\infty}I(0)2\pi rdr$$
da questo possiamo affermare che vale $L\propto R^{2}$. Se assumo che il rapporto massa-luminosità sia costante $M/L=\mbox{cost.}$ ho che $L\propto Rv^{2}$. Invertendo ho $R\propto\sqrt{L}$ che diventa $L\propto v^{4}$.

Partendo dal teorema del viriale, $2k+\Omega=0$, abbiamo $k\sim \frac{M\sigma^{2}}{2}$ e $\Omega\sim - \frac{GM^{2}}{R}$. Viene $M\sim \frac{R\sigma^{2}}{G}$ e $M\propto I_{e}R_{e}^{2}$. Allora si trova $I_{e}R_{e}\propto \sigma^{2}_{0}$, che descrive il **piano fondamentale** di una galassia. Viene usato per misurare la distanza di galassie ellittiche.