I telescopi più antichi sono **telescopi rifrattori**, hanno la forma di un cannocchiale e cercano di assorbire tutta la luce in arrivo sulla superficie più ampia possibile e poi concentrarla sull'occhio. Il [[flusso energetico]] che arriva all'occhio è
$$\frac{f_{tele}}{f_{occhio}}=\frac{S_{tele}}{S_{occhio}}$$
con $S$ la superficie.

![[Telescopio Rifrangente|center]]

Uno dei problemi con questi telescopi è che vedono solo nello spettro ottico, in quanto essendo usati dall'occhio umano, si perdono tutti i dettagli di altri spettri.

I telescopi moderni usano degli *specchi* per convogliare la luce su un punto. Il vantaggio è che non è importante se gli specchi sono imperfetti o se si compone il telescopio di diversi specchi con spazi tra loro, basta convogliare la luce. Il problema con questo design è che il punto di fuoco è *davanti* al telescopio. Quindi si mette un buco negli specchi e uno specchio secondario davanti agli altri per riflettere la luce nella direzione originale. Ci sono diversi design: i più comuni sono il **cassegrain** e il **newtoniano**.

![[Telescopio Cassegrain|center]]

L'angolo minimo che il telescopio riesce a captare correttamente, il **limite di rifrazione** è
$$\theta_{diff}=\frac{1.22\lambda}{D}$$
con $\lambda$ la lunghezza d'onda della luce e $D$ il diametro del telescopio. La costante è un misto di altre costanti ottiche. Ovviamente l'atmosfera causa effetti di distorsione che generalmente impediscono al telescopio di raggiungere il limite di rifrazione. Si può sistemare il problema usando un sistema chiamato **Adaptive Optics**.

Per contesto, al limite di rifrazione dell'occhio umano, si riuscirebbe a riconoscere la spazio tra due parole da circa 16 metri di distanza, eppure anche con vista perfetta è difficile farlo già da pochi metri. Ciò è dovuto agli vari effetti dell'atmosfera, come fluttuazioni termiche, effetti cromatici e altro.

L'atmosfera non è uguale ovunque, quindi i posti migliori per costruire i telescopi sono
- in montagna (meno atmosfera da perforare)
- in posti dove non c'è inquinamento luminoso
- in posti dove il cielo è privo di nuvole molto spesso

Il limite di rifrazione di un telescopio dipende dalla lunghezza d'onda $\lambda$ di un segnale, quindi per lunghezze diverse, dovranno essere usate tecniche diverse. Vedi [[Misurazione astronomiche di lunghezze d'onda]].