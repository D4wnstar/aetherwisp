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
### Serie di decadimenti
Nel caso di una serie di decadimenti, e quindi di generazione di nuclei, ho
$$dN_{i}=\lambda_{i-1}N_{i-1}dt-\lambda_{i}N_{i}dt$$
dette le **equazioni di Bateman**, che danno una soluzione generale nel caso in cui $N_{0}$ sia costituito solo da nuclei madre. L'attività è
$$A_{n}=N_{0}\sum\limits_{i=0}^{n}c_{i}e^{-\lambda_{i}t}=N_{0}(c_{1}e^{-\lambda_{1}t}+c_{2}e^{-\lambda_{2}t}+\ldots+c_{n}e^{-\lambda_{n}t})$$
dove $c_{i}$ è
$$c_{m}=\frac{\prod_{i=1}^{n}\lambda_{i}}{\prod_{i=1}^{n}(\lambda_{i}-\lambda_{m})}=\frac{\lambda_{1}\lambda_{2}\lambda_{3}\ldots\lambda_{n}}{(\lambda_{1}-\lambda_{m})(\lambda_{2}-\lambda_{m})\ldots(\lambda_{n}-\lambda_{m})}$$
dove nei produttori ometto il termine $i=m$. Si ha equilibrio secolare nel caso
$$\lambda_{1}N_{1}=\lambda_{2}N_{2}=\ldots=\lambda_{n}N_{n}$$
## Tipi di decadimento
Esistono tre tipi principali di decadimento:
- **decadimento $\alpha$**
- **decadimento $\beta$**
- **decadimento $\gamma$**
Nei decadimenti $\alpha$ e $\beta$, un nuclide emette una particella $\alpha$ o $\beta$ per diventare più stabile. Nel decadimento $\gamma$, uno stato eccitato emette radiazione $\gamma$ per tornare allo stato fondamentale, senza cambiare la specie nucleare.
### Decadimento $\alpha$
Nel decadimento $\alpha$, un nuclide emette una particella $\alpha$, come un nucleo di $_{2}^{4}He_{2}$. Il nucleo rilasciato è molto legato, quindi l'energia cinetica rilasciata è massimizzata. Il processo di decadimento è
$$_{Z}^{A}X_{N} \rightarrow _{Z-2}^{A-4}X'_{N-2}+\alpha$$
dove $X$ e $X'$ sono simboli chimici di specie nucleari diverse nello stato iniziale e finale. Il numero di protoni e neutroni deve conservarsi. L'energia cinetica tipica di una tale reazione è nell'ordine dei [[Elettronvolt|MeV]].

Una reazione tipo è
$$_{88}^{226}Ra_{138}\rightarrow _{86}^{222}Rn_{136}+_{2}^{4}He_{2}$$
che ha un tempo di dimezzamento di 1600 anni e la particella $\alpha$ ha un'energia cinetica di $4.8$ MeV.
#### Meccanismo
Protoni e neutroni hanno energie di legami attorno agli 8 MeV, quindi non possono scappare dal nucleo. Può però succedere che l'emissione di un gruppo di nucleoni sotto forma di un sistema legato sia energeticamente favorita.

Studiamo l'energia potenziale $V(r)$ di una particella $\alpha$ in funzione della distanza $r$ dal nucleo

![[Schema Decadimento Alpha|80%|center]]
A grandi distanze, $\alpha$ è soggetta a repulsione Coulombiana dei protoni, come si vede in $V_{C}$. $Z$ è il numero atomico del nucleo, $Z-2$ è il numero dopo il decadimento $\alpha$.
- $Q$ è l'energia di disintegrazione.
- In $r<a$ si ha una buca di potenziale che rappresenta l'interno del nucleo. La barriera di potenziale è alta $-V_{0}$. In meccanica classica, il nucleone può muoversi dentro questa buca, ma non può uscirne.
- In $a<r<b$ si forma una seconda barriera di potenziale perché l'energia potenziale supera quella disponibile $Q$. $\alpha$ non può entrare in questa regione.
- La regione $r>b$ è quella normale fuori dalla barriera.
L'unico modo che la particella $\alpha$ ha per entrare o uscire dal nucleo è tramite il [[tunneling quantistico]].

Chiamiamo *costante di disintegrazione* $\lambda$ di un emettitore $\alpha$
$$\lambda=fp\text{ con }f\sim \frac{v}{a}$$
dove $f$ è la frequenza con cui $\alpha$ si presenta alla barriera, $p$ è la probabilità di trasmissione oltre la barriera e $v$ è la velocità della particella $\alpha$ sulla barriera.

Per comprendere il fenomeno, dobbiamo risolvere l'[[equazione di Schrödinger]] in una dimensione per una particella sottoposta ad una barriera di potenziale $V(x)$. Consideriamo l'[[autostato]] $\Psi$. Allora
$$\frac{\hbar^{2}}{2m} \frac{d^{2}\Psi(x)}{dx^{2}}+V(x)\Psi(x)=E\Psi(x)$$
A causa della barriera di potenziale, abbiamo tre soluzione per tre regioni dello spazio, determinate dalle condizione al contorno:
- $V(x)=0$ per $x<0$ ci dà $\Psi_{1}(x)=Ae^{ik_{1}x}+Be^{-ik_{1}x}$
- $V(x)=V_{0}$ per $0\leq x\leq a$ ci dà $\Psi_{2}(x)=Ce^{k_{2}x}+De^{-k_{2}x}$
- $V(x)=0$ per $x>a$ ci dà $\Psi_{3}(x)=Ee^{ik_{3}x}+Fe^{-ik_{3}x}$
dove
$$k_{1}=k_{3}=\sqrt{\frac{2mE}{\hbar^{2}}}\quad;\quad k_{2}=\sqrt{\frac{2m(V_{0}-E)}{\hbar^{2}}}$$
Possiamo chiamare $P$ la probabilità di trasmissione
$$P=\frac{j_{trasmesso}}{j_{incidente}}$$
con $j_{trasmesso}$ la corrente nell'onda trasmessa e $j_{incidente}$ la corrente nell'onda incidente. Quindi $P$ è la frazione della corrente incidente e trasmessa oltre la barriera. Si ha
$$P=\frac{1}{1+ \frac{1}{4} \frac{V_{0}^{2}}{E(V_{0}-E)}\sinh^{2}(k_{2}a)}$$
In meccanica classica, $P=0$, quindi penetrare la barriera è impossibile. L'onda quantistica invece può penetrare la barriera con probabilità $P$, fenomeno detto *tunnelling quantistico*.
#### Conservazione dell'energia
non so, farò prima o poi
### Decadimento $\beta$
Nel decadimento $\beta$, il nucleo corregge l'eccesso di protoni $p$ o neutroni $n$ convertendoli l'uno nell'altro.
$$\text{decadimento }\beta^{-}\text{: }\quad n \rightarrow p+e^{-}+\nu_{e}^{-}$$
$$\text{decadimento }\beta^{+}\text{: }\quad p \rightarrow n+e^{+}+\nu_{e}$$
dove $e^{-}$ è un [[elettrone]] e $e^{+}$ è un [[positrone]]. Vengono emessi anche (anti)[[neutrino|neutrini]] elettronici $\nu_{e}$. Esiste anche una terza reazione, chiamata *cattura elettronica*
$$p+e^{-}\rightarrow n+\nu_{e}$$
che "promuove" un protone ad un neutrone. È importante ricordare che il protone decade *solo nel nucleo*, non nel vuoto.

Una reazione tipo $\beta^{-}$ è
$$_{53}^{131}I_{78} \rightarrow _{54}^{131}Xe_{77}$$
con tempo di dimezzamento di 8.0 giorni.
### Decadimento $\gamma$
Nel decadimento $\gamma$,  uno stato eccitato decade in uno stato diseccitato o in quello fondamentale emettendo radiazione $\gamma$. Spesso segue il decadimento $\alpha$ o $\beta$ dato che questi di solito lasciano nuclei figli in stati eccitati.
### Fissione spontanea
Alcuni nuclei fissionano spontaneamente senza che la reazione sia indotta. Un nucleo pesante, come l'uranio, si divide in due più leggeri che, a differenza degli altri decadimenti non sono ben determinati. I nuclei in cui si può rompere sono un intero intervallo centrato attorno ad un peso medio, di cui si può misurare la distribuzione di probabilità.

Il fermio $^{256}Fm$ e il californio $^{254}Cf$ sono elementi che mostrano fissione spontanea.