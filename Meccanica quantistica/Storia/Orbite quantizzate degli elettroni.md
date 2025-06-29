---
wiki-publish: true
---
Osservando l'assorbimento della luce da parte di un gas di idrogeno, si è notata la presenza di [[Riga spettrale|righe di assorbimento]] ad intervalli discreti e ben spaziati, anziché continui come ci si aspettava. Inoltre, una carica come un [[elettrone]] in rotazione attorno al [[nucleo atomico]] è in perpetua accelerazione centripeta, e una carica in accelerazione emette [[radiazione]] per [[Bremmstrahlung]]. Per quale motivo l'elettrone non cadeva sul nucleo non era noto, però era chiaro che per qualche ragione, l'elettrone non perdeva energia come di norma.

Bohr ha assunto che solo certe orbite fossero permesse, nelle quali l'elettrone non emetteva energia. Ha supposto che il momento angolare associato a queste orbite fosse un multiplo della [[Planck constant]] a modo che valesse
$$mvr=pr=\hbar n$$
L'elettromagnetismo classico di consiglia di usare la [[Interazione elettromagnetica|legge di Coulomb]] (qui in unità Gaussiane senza $4\pi \epsilon_{0}$) per ottenere
$$\frac{e^{2}}{r^{2}} = \frac{mv^{2}}{r}$$
con $e$ la [[Elementary charge|carica dell'elettrone]]. Riordinando, trovo l'energia dell'orbita che è quella cinetica più il potenziale Coulombiano
$$mv^{2}=\frac{e^{2}}{r}\quad\Rightarrow \quad E=\frac{mv^{2}}{2}- \frac{e^{2}}{2}=- \frac{e^{2}}{2r}$$
che è l'energia cinetica associata all'orbita a distanza $r$. Posso anche trovare
$$m^{2}v^{2}r^{2}=m \frac{e^{2}}{r}r^{2}=\hbar^{2}n^{2}\quad\Rightarrow \quad \boxed{r_{n}=\frac{\hbar^{2}}{me^{2}}n^{2}}$$
Ciò significa che, in questa ipotesi, le orbite permesse sono quantizzate, a intervalli interi pesati dalla costante di Planck con energia ben nota. Il primo raggio possibile è
$$r_{B}=\frac{\hbar^{2}}{me^{2}}$$
detto [[Bohr radius]]. Trovando la derivata parziale dell'energia potenziale $U(r)=- \frac{e^{2}}{r}$ si ha $F(r)=- \frac{e^{2}}{r^{2}}$ cioè una forza *repulsiva*, come deve essere. Il segno meno nella formula dell'energia deriva da questo. Sostituendo il raggio con quelli quantizzati abbiamo le energie possibili
$$E_{n}=- \frac{e^{2}}{2r_{n}}=- \frac{me^{4}}{2\hbar^{2}}\frac{1}{n^{2}}$$

Questo spiega ragionevolmente la presenza di righe spettrali: il gas (o meglio, gli elettroni) assorbono la luce solo se la luce trasporta *esattamente* la differenza di energia tra un'orbita e un'altra. A livello sperimentale, le energie trovate empiricamente combaciano con questa teoria solo quanto $h$ vale esattamente lo stesso valore trovato inizialmente nella teoria del [[corpo nero]] e poi quella dell'[[effetto fotoelettrico]].

Più avanti, De Broglie ha avuto la seguente intuizione: un [[Photon]] trasporta energia pari a $E=\hbar \omega$ e momento $p=E/c$ (dalla conservazione massa-energia relativistica $E^{2}-p^{2}c^{2}=m^{2}c^{4}$ con $m_{\gamma}=0$). Allora
$$p=\frac{E}{c}=\frac{\hbar\omega}{c}=\frac{h}{cT}=\frac{h}{\lambda}$$
con $T$ il periodo di oscillazione e $\lambda$ la lunghezza d'onda. Allora
$$\boxed{\lambda=\frac{h}{p}}$$
detta [[formula di De Broglie]]. Egli colse la conclusione: se la luce si comporta sia come onda (con lunghezza d'onda $\lambda$) ma anche come corpo (con un momento lineare ben definito), perché qualunque altro non può essere anch'esso descritto come onda, con lunghezza d'onda determinata dalla relazione sopra? Da qui è nata l'idea della **dualità corpo-onda**, valida per qualunque [[particella]], non solo i fotoni.

Di fatto, sperimentalmente si è trovato che, lanciando elettroni a due fenditure, essi formano una figura di diffrazione pari a quella che avrebbe la luce con lunghezza d'onda $\lambda = \frac{h}{p}$, con $p$ l'impulso dell'elettrone. Questo era completamente inaspettato: ragionevolmente, ci si aspettava che gli elettroni si accumulassero in concomitanza con le fenditure, come lanciare un sasso attraverso una finestra e trovarlo dall'altra parte della finestra. Eppure il pattern era identico a quello della luce, con tanto di interferenze e diffrazione.

Si può estrarre ancora più ancora informazione dalle orbite. Queste devono essere multipli della lunghezza d'onda, ma allora possiamo usare la formula di De Broglie:
$$2\pi r = n\lambda=n \frac{h}{p}$$
da cui
$$r = \frac{nh}{2\pi p}$$
che sono i raggi delle orbite permesse in funzione del momento lineare della particella orbitante.