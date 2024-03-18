Il **decadimento** è il processo per il quale il [[nucleo atomico]] si autodistrugge, non lo so cambia dopo
### Legge di decadimento radioattivo
Consideriamo
- $N$ nuclei radioattivi
- un tempo $t$ in cui decade senza introdurre nuovi nuclei
- un solo modo di decadimento ($\alpha$, $\beta$, ...)
- il prodotto del decadimento è stabile
Allora sperimentalmente il numero di nuclei $dN$ che decade in $dt$ è proporzionale ad $N$. Posso trovare la costante di decadimento
$$\lambda\equiv - \frac{1}{N}\frac{dN}{dt}$$
che rappresenta la probabilità in unità di tempo che il nucleo decada. Integrando si ha
$$\boxed{N(t)=N_{0}e^{-\lambda t}}$$
che è la **legge esponenziale del decadimento radioattivo**, con $N_{0}$ il numero di nuclei a $t=0$. Il tempo per il quale vale $N=\frac{N_{0}}{2}$ si dice **tempo di dimezzamento** $t_{\frac{1}{2}}$ e vale
$$t_{\frac{1}{2}}=\frac{0.693}{\lambda}$$
ed è il tempo necessario per far decadere metà dei nuclei.

Si dice **vita media** $\tau$ il tempo medio di vita di un [[nuclide]]
$$\tau=\frac{\int_{0}^{\infty}t| \frac{dN}{dt}|dt}{\int_{0}^{\infty}| \frac{dN}{dt}|dt}=\frac{1}{\lambda}$$
ottenuta integrando $| \frac{dN}{dt}|dt$, cioè il numero di nuclei che decadono tra $t$ e $t+dt$.

$N$ è difficile da misurare. Possiamo contare il numero di decadimenti tra tempo $t_{1}$ e $t_{2}$ osservando la radiazione emessa. Calcoliamo il cambiamento di numero di nuclei per unità di tempo
$$|\Delta N|=N(t)-N(t+dt)=N_{0}e^{-\lambda t}(1-e^{-\lambda\Delta t})$$
Allora se $\Delta t\ll \frac{1}{\lambda} \ll t_{\frac{1}{2}}$ posso ignorare i termini superiori dell'espressione:
$$|\Delta N|=\lambda N_{0}e^{-\lambda t}\Delta t$$
che in forma differenziale diventa
$$\left|\frac{dN}{dt}\right|=\lambda N(t)=\lambda N_{0}e^{-\lambda t}$$
Usando l'[[attività]] e se $\Delta t\ll t_\frac{1}{2}$ possiamo misurare $\Delta N$
$$\Delta N=\int_{t_{1}}^{t_{2}=t_{1}+\Delta t}Adt=A\Delta t$$
L'attività si misura in **Becquerel**: $1\text{ Bq}=1 \frac{\text{dec}}{\text{s}}$. Storicamente si è usato anche il **Curie**: $1\text{ Cu}=3.7\times10^{10}\frac{\text{dec}}{\text{s}}$, che è l'attività di un giorno del radio.

Questo metodo funziona se la vita media dell'elemento è entro limiti ragionevoli
$$1\text{ s}<\tau<\text{ vita umana}$$
#### Validità
La legge di decadimento radioattivo è valida se il nuclide 2 nel decadimento $1 \rightarrow 2$ è stabile. Il numero di nuclei sarà
$$N_{1}=N_{0}e^{-\lambda t}\quad;\quad N_{2}=N_{0}(1-e^{-\lambda t})$$
#### Più modi
Consideriamo il caso più complesso in cui ci sono due, $a$ e $b$. Entrambi hanno una costante di decadimento parziale
$$\lambda_{a}=- \frac{1}{N}\left(\frac{dN}{dt}\right)_{a}\quad;\quad\lambda_{b}=- \frac{1}{N}\left(\frac{dN}{dt}\right)_{b}$$
e vale $\lambda_{a}+\lambda_{b}=\lambda_{t}$ la costante di decadimento totale. Sperimentalmente non si osservano *mai* attività separate: i nuclei decadono sempre come
$$N(t)=N_{0}e^{-\lambda_{t}t}$$
Le costanti parziali servono per descrivere le frazioni di decadimento per ciascun tipo. Una frazione dei nuclei decade con modo $a$ e un'altra frazione con modo $b$. Possiamo scrivere
$$N_{1}=N_{0}e^{-\lambda_{1}t}$$
$$N_{2a}=N_{0} \left(\frac{\lambda_{a}}{\lambda_{t}}\right)(1-e^{-\lambda_{1}t})\quad;\quad N_{2b}=N_{0} \left(\frac{\lambda_{b}}{\lambda_{t}}\right)(1-e^{-\lambda_{1}t})$$
Assumiamo di avere un campione di radionuclidi con due schemi di decadimento
$$^{64}\text{Cu}\rightarrow t_\frac{1}{2}=12.7\text{ h}\quad;\quad ^{61}\text{Cu}\rightarrow t_\frac{1}{2}=3.4\text{ h}$$
Misurando l'attività trovo un grafico del genere

![[Grafico Attività multiple|60%|center]]
Inizialmente trovo una curva di decrescita. Dato che le vite medie sono molto diverse, ci sarà un momento in cui l'elemento con vita media inferiore sarà (quasi) completamente decaduto. Ciò lascia solo il decadimento dell'elemento con vita media più lunga. Possiamo quindi fare un fit su quest'ultima parte del grafico e trovare l'attività di un radionuclide, poi sottrarre questa dal resto del grafico e quindi rimanere solo con l'attività dell'altro radionuclide. Questo metodo funziona con un qualunque numero di radionuclidi diversi, a patto che le loro vite media siano sufficientemente diverse.
### Produzione e decadimento della radioattività
Consideriamo un reattore in cui produco radionuclidi che decadono inserendo una targhetta (ossia un qualche foglio di materiale, di solito metallico. Non deve essere solido). Definendo $R$ il tasso di produzione, $N_{0}$ il numero di atomi inseriti nella targhetta, $I$ il flusso di [[Particella|particelle incidenti]] e $\sigma$ la *sezione d'urto*, cioè la probabilità che una particella ha collidere con la targhetta, abbiamo in un caso tipico
$$I\propto10^{14}\text{ particelle/s}$$
$$\sigma\propto10^{-24}\text{ cm}^{2}$$
La probabilità di convertire una particella stabile in radioattività è $\sim10^{-10}\text{ s}^{-1}$. In queste condizioni posso considerare $N_{0}$ costante. Il tasso di formazione è $R=N_{0}\sigma I$. Chiamo $N_{1}$ il numero di radionuclidi formati da decadimento con $\lambda_{1}$ in $N_{2}$ stabili. $N_{1}$ cresce con $R$, ma decresce per decadimento.
$$dN_{1}=Rdt-\lambda_{1}N_{1}dt \rightarrow N_{1}(t)=\frac{R}{\lambda_{1}}(1-e^{-\lambda_{1}t}) \rightarrow A_{1}(t)=\lambda_{1}N_{1}(t)=R(1-e^{-\lambda_{1}t})$$
- Se $t\ll t_\frac{1}{2}$ allora $A_{1}(t)\sim R\lambda_{1}t$, cioè cresce linearmente con il tempo.
- Se $t\gg t_\frac{1}{2}$ allora $A_{1}(t)\sim R$, il tasso di produzione è uguale al tasso di decadimento. Questo stato si dice **equilibrio secolare**.