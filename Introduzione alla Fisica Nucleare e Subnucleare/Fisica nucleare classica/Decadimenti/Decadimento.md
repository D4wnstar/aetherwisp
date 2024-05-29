Il **decadimento** è il processo stocastico per il quale un [[nucleo atomico]] instabile perde energia per emissione di radiazione. Un nucleo decade in una o più specie nucleari o [[Particella|particelle]]. Decadimenti che terminano in un numero maggiore di particelle sono più rari.
## Tipi
Esistono tre tipi principali di decadimento:
- **decadimento $\alpha$**
- **decadimento $\beta$**
- **decadimento $\gamma$**
Nei decadimenti $\alpha$ e $\beta$, un nuclide emette una particella $\alpha$ o $\beta$ per diventare più stabile. Nel decadimento $\gamma$, uno stato eccitato emette radiazione $\gamma$ per tornare allo stato fondamentale, senza cambiare la specie nucleare. Vedi le loro pagine: [[Decadimento Alpha]], [[Decadimento Beta]], [[Decadimento Gamma]].
### Fissione spontanea
Esiste un quarto tipo di decadimento, un po' diverso dagli altri, detto **[[fissione spontanea]]** che accade per nuclei molto pesanti ($Z\geq110$). Questi nuclei fissionano spontaneamente senza che la reazione sia indotta. Un nucleo pesante, come l'uranio, si divide in due più leggeri che, a differenza degli altri decadimenti non sono ben determinati. I nuclei in cui si può rompere sono un intero intervallo centrato attorno ad un peso medio, di cui si può misurare la distribuzione di probabilità.

Il fermio $^{256}Fm$ e il californio $^{254}Cf$ sono elementi che mostrano fissione spontanea.
### Meccanismo
Sebbene il meccanismo dipenda dal tipo di decadimento, una trattazione comune può essere svolta mediante la [[legge di decadimento radioattivo]], che rappresenta matematicamente il numero di decadimenti nel tempo.
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
