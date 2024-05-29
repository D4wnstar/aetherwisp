---
aliases:
  - costante di decadimento
  - tempo di dimezzamento
  - vita media
---
La **legge di decadimento radioattivo** è una legge esponenziale che descrive il [[decadimento]] di una [[Nucleo atomico|specie nucleare]] nel tempo, indifferentemente dal tipo di decadimento.

Questa legge si basa sull'assunzione che il nucleo non ha "memoria", ossia lo stato di nucleo ad ogni dato tempo è indipendente dai suoi stati precedenti. Ciò significa che il suo tasso di decadimento è una costante nel tempo, ma l'esatto tasso dipende dalla specie nucleare.
### Formulazione
Considero un oggetto macroscopico composto da $N$ nuclei radioattivi e la lascio decadere naturalmente per un tempo $t$ *senza introdurre nuovi nuclei*. Questa legge descrive solo il decadimento di una specie e non dice nulla su cosa succede ai risultati del decadimento. Per questo, i prodotti del decadimento devono essere stabili.

Consideriamo anzitutto il caso in cui avviene solo un tipo di decadimento.

Il numero $dN$ di nuclei che decade in un certo tempo $dt$ è proporzionale al numero di atomi $N$ nell'oggetto. Dato che il tasso di decadimento $dN/dt$ deve essere costante e $N$ è anch'esso costante, il loro rapporto
$$\lambda=- \frac{1}{N}\frac{dN}{dt}$$
è a sua volta una costante, detta **costante di decadimento**. Questo risultato è sostenuto da evidenza sperimentale. Questa è un'[[equazione differenziale ordinaria]] di primo ordine, quindi possiamo risolverla per quadratura. Integrando si ha
$$\boxed{N(t)=N_{0}e^{-\lambda t}}$$
che è la **legge esponenziale del decadimento radioattivo**, con $N_{0}$ il numero di nuclei a $t=0$, ossia il numero di nuclei che compongono l'oggetto all'inizio delle osservazioni.

Per comodità si definisce si dice **tempo di dimezzamento** $t_{\frac{1}{2}}$ il tempo per il quale vale il numero di nuclei è dimezzato, ossia $N=N_{0}/2$, e vale
$$\boxed{t_{\frac{1}{2}}=\frac{0.693}{\lambda}}$$
Inoltre, si dice **vita media** $\tau$ il tempo medio di vita di un *singolo nucleo* prima di decadere
$$\boxed{\tau=\frac{\int_{0}^{\infty}t| \frac{dN}{dt}|dt}{\int_{0}^{\infty}| \frac{dN}{dt}|dt}=\frac{1}{\lambda}}$$
ottenuta integrando $| \frac{dN}{dt}|dt$, cioè il numero di nuclei che decadono tra $t$ e $t+dt$.

$N$ è difficile da misurare. È più facile misurare la radiazione emessa tra tempo $t_{1}$ e $t_{2}$ e da lì estrarre il numero di decadimenti. Per fare ciò, calcoliamo il cambiamento di numero di nuclei per unità di tempo
$$|\Delta N|=N(t)-N(t+dt)=N_{0}e^{-\lambda t}(1-e^{-\lambda\Delta t})$$
Allora se $\Delta t\ll \tau \ll t_{\frac{1}{2}}$ posso ignorare i termini superiori dell'esponenziale:
$$|\Delta N|=\lambda N_{0}e^{-\lambda t}\Delta t$$
che in forma differenziale diventa
$$\left|\frac{dN}{dt}\right|=\lambda N(t)=\lambda N_{0}e^{-\lambda t}$$
Usando l'[[attività]] $A$ e sempre nell'approssimazione $\Delta t\ll t_\frac{1}{2}$ possiamo esprimere $\Delta N$ come
$$\Delta N=\int_{t_{1}}^{t_{2}=t_{1}+\Delta t}Adt=A\Delta t$$
Dato che il decadimento nucleare è esponenziale, per descriverlo mediante questa approssimazione ho bisogno di molte misure per brevi $\Delta t$ (altrimenti troveremmo una legge lineare).
#### Validità
Questo metodo funziona se la vita media dell'elemento è entro limiti ragionevoli, ossia $1\text{ sec}<\tau<\text{ vita umana}$. Altrimenti
- se $\tau>\text{ vita umana}$, il tempo di decadimento è talmente lungo che servirebbero diverse generazioni umane solo per avere risultati decenti. A questi punti misuro direttamente la massa del campione e ne estrapolo il numero di atomi nel tempo.
- se $1\ll\tau$, è comunque possibile misurare il decadimento (fino a 1 picosecondo con tecniche moderne), ma bisogna usare un metodo diverso poiché l'accendere e spegnere l'apparato di misura azzera l'attività e quindi non è possibile prendere prenderne una misura.

Inoltre, i prodotti di decadimento devono essere stabili. Ciò significa che per una specie 1 con costante di decadimento $\lambda_{1}$ che decade in una specie 2 il numero di nuclei sarà
$$N_{1}=N_{0}e^{-\lambda t}\quad;\quad N_{2}=N_{0}(1-e^{-\lambda t})$$
ossia
$$N_{2}=N_{0}-N_{1} \quad \rightarrow \quad N_{0}=N_{1}+N_{2}$$
quindi il numero di nuclei rimane costante, vengono solo modificati dalla specie 1 alla 2.
#### Decadimenti multipli
Consideriamo il caso più complesso in cui ci sono due tipi di decadimento. Chiamiamoli $a$ e $b$. Entrambi hanno una **costante di decadimento parziale**
$$\lambda_{a}=- \frac{1}{N}\left(\frac{dN}{dt}\right)_{a}\quad;\quad\lambda_{b}=- \frac{1}{N}\left(\frac{dN}{dt}\right)_{b}$$
e vale $\lambda_{a}+\lambda_{b}=\lambda_{t}$ la **costante di decadimento totale**. Sperimentalmente non si osservano *mai* attività separate: i nuclei decadono sempre secondo la costante totale come la legge esponenziale normale
$$N(t)=N_{0}e^{-\lambda_{t}t}$$
Le costanti parziali servono per descrivere le frazioni di decadimento per ciascun tipo. Una frazione dei nuclei decade con modo $a$ e un'altra frazione con modo $b$ e questa frazione è determinata da $\lambda_{a}/\lambda_{t}$ e $\lambda_{b}/\lambda_{t}$.

Il numero di nuclei presenti nelle specie 1 e 2 è
$$N_{1}=N_{0}e^{-\lambda_{1}t}$$
$$N_{2a}=N_{0} \left(\frac{\lambda_{a}}{\lambda_{t}}\right)(1-e^{-\lambda_{1}t})\quad;\quad N_{2b}=N_{0} \left(\frac{\lambda_{b}}{\lambda_{t}}\right)(1-e^{-\lambda_{1}t})$$

> **Esempio.** Assumiamo di avere un campione di radionuclidi con due schemi di decadimento
$$^{64}\text{Cu}\rightarrow t_\frac{1}{2}=12.7\text{ h}\quad;\quad ^{61}\text{Cu}\rightarrow t_\frac{1}{2}=3.4\text{ h}$$
> Misurando l'attività trovo un grafico del genere
>
>![[Grafico Attività multiple|60%|center]]
>
>Inizialmente trovo una curva di decrescita. Dato che le vite medie sono molto diverse, ci sarà un momento in cui l'elemento con vita media inferiore sarà (quasi) completamente decaduto. Ciò lascia solo il decadimento dell'elemento con vita media più lunga. Possiamo quindi fare un fit su quest'ultima parte del grafico e trovare l'attività di un radionuclide, poi sottrarre questa dal resto del grafico e quindi rimanere solo con l'attività dell'altro radionuclide. Questo metodo funziona con un qualunque numero di radionuclidi diversi, a patto che le loro vite media siano sufficientemente diverse.