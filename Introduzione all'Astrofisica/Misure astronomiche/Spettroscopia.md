La spettroscopia usa strumenti che disperdono la luce in modo tale da separare i colori componenti e ne misurano l'intensità per trovare lo spettro della luce.

Gli strumenti principali della spettroscopia astrofisica sono le **righe spettrali**, ossia bande di luce in un certo intervallo di lunghezze d'onda in cui il flusso è considerevolmente più basso. Nel grafico del flusso si vedono come valli nella funzione, o come righe più scure se visualizzate come spettro arcobaleno.

Per un corpo nero, *l'intensità monocromatica (cioè di una singola lunghezza d'onda) dipende solo dalla temperatura*. La si trova usando
$$B_{\lambda}= \frac{2hc}{\lambda^{5}} \frac{1}{e^{\frac{ht}{\lambda}kt }-1}$$
La **legge di traslazione di Wien** è
$$\lambda_{p}=\frac{1}{\mu m}\frac{2900K}{T}$$
Le stelle non sono propriamente corpi neri. Forme di emissione non termiche importante per le stelle sono
- **Emissione da sincrotrone**: non è un effetto termico, viene generata da elettroni che viaggiano a velocità relativistiche entro campi magnetici molto forti (come quelli di una stella di neutroni).
- **Processo Compton inverso**: ha sempre a che fare con gli elettroni che si muovono a velocità relativistiche.
- **Bremsstrahlung termico** (o *radiazione di frenata*): accade quando un elettrone molto energetico passa attraverso il nucleo di una stella, viene affetto dal campo elettrico del nucleo e rallenta bruscamente, liberando energia sotto forma di luce.

Le linee di assorbimento accadono quando ho una sorgente calda che sto osservando e nel mezzo c'è *qualcosa* che sta assorbendo la luce. In genere, ci sono due modi per assorbire la luce (cioè energia): un gas che assorbe energia portando i suoi elettroni ad uno stato quantistico eccitato; o lo *scattering*, che ridirige parte della luce in moltissime direzioni, in generale non allineate con la mia vista.
Può succedere anche l'effetto contrario, ossia *linee di emissione*, per le stesse ragione, ma al contrario.

Misurare *esattamente* una riga di assorbimento è impossibile per qualche motivo:
1. **Allargamento naturale**: la banda è $\frac{\Delta\lambda}{\lambda}=\frac{v}{c}$, ossia misurare $\Delta\lambda$ ci richiede di misurare la velocità di un oggetto. Per la [[Disuguaglianza di Heisenberg]], è impossibile farlo con precisione arbitraria, quindi ci sarà necessariamente un errore. Ciò rende le bande delle distribuzioni.
2. **Allargamento termico**: i moti caotici delle particelle che compongono le stelle causano variazioni di lunghezza d'onda per effetto Doppler . Se si avvicina, si tratta di **blueshift**, se si allontana si tratta di **redshift**. Nello spettro ciò causa traslazioni nella banda, verso il blu o il rosso. $$v\sim\sqrt{\frac{kT}{\mbox{Amp}}}$$dove Amp è l'allargamento della banda (in questo caso simmetrico).
3. **Allargamento di pressione/collisione**: gli elettroni in stelle estremamente dense sono talmente vicini da loro che le interazioni con gli elettroni vicini causano modifiche nei loro livelli di energia.
4. **Allargamento per turbolenze**: dovuto ai moti turbolenti dei gas sulle superfici delle stelle. Causa sia blueshift che redshift
5. **Allargamento per rotazione stellare**: la rotazione fa si che metà della stella si stia allontanando da noi (e quindi produca redshift), mentre l'alta metà si avvicina (producendo blueshift). Più veloce è la rotazione, più forte è l'allargamento.
6. **Allargamento per moti stellari**: cluster di stelle (stelle fisicamente vicine fra loro nello spazio, vedi Pleiadi) molto lontani appaiono a noi come punti singoli. Alcune stelle nel cluster possono muoversi verso di noi (blueshift), altre lontane da noi (redshift) e la combinazione di questi moti è a sua volta una causa di allargamento.
7. **Allargamento di moti di gas caldi**: (questo ha solo a che fare con linee di emissione). I quasar (*quasi-stellar object*) eiettano gas a velocità estreme che causano distorsioni nello spettro.
8. **Effetto Zeeman**: di norma gli elettroni hanno stati energetici ben definiti. Quando si trovano in un campo magnetico, uno stato si "spezza" in tre stati vicini fra loro. Si nota dunque un fenomeno chiamato *Zeeman splitting*, dove la riga diventa tre righe una vicina all'altra.
![[Righe spettrali|80%|center]]
Una misura comune di $\Delta\lambda$ è la *Full-Width Half-Maximum*, o FWHM, dove si misura la larghezza della banda a metà dell'ampiezza.