---
wiki-publish: true
aliases:
  - catena di decadimento
  - equazione di Bateman
---
È possibile che un [[Nuclide|radionuclide]] [[Decadimento nucleare|decada]] in [[Nucleo atomico|specie nucleari]] che al loro volta sono instabili, e quindi queste a loro volta decadranno in nuove specie. Questo fenomeno è detto **decadimento a catena** e la successione di nuclei che vengono prodotti dai decadimenti è detta **catena di decadimento**. Il nucleo che dà origine alla catena è detto **nucleo madre** e i risultanti sono detti **figlie**, **nipoti**, etc.
### Decadimento a due passi
Se comincio con $N_{0}$ [[Atom|atomi]] madre e nessuna figlia, ho $N_{1}(t_{0})=N_{0}$, $N_{2}(t_{0})=0$, etc., con una [[Legge di decadimento radioattivo|costante di decadimento]] $\lambda_{i}$ per ciascun decadimento. Il nucleo madre decade secondo la [[legge di decadimento radioattivo]]:
$$dN_{1}=-\lambda_{1}N_{1}dt \quad \Rightarrow \quad N_{1}(t)=N_{0}e^{-\lambda_{1}t}$$
(risolta integrando direttamente). Il nucleo figlia cresce a pari passo con la diminuzione della madre, ma diminuisce per il suo decadimento:
$$dN_{2}=-dN_{1}-\lambda_{2}N_{2}dt=\lambda_{1}N_{1}dt-\lambda_{2}N_{2}dt$$
Questa equazione può essere risolta chiedendo una soluzione della forma
$$N_{2}(t)=Ae^{-\lambda_{1} t}+Be^{-\lambda_{2}t} \quad \Rightarrow \quad N_{2}(t)=N_{0} \frac{\lambda_{1}}{\lambda_{2}-\lambda_{1}}(e^{-\lambda_{1}t}-e^{-\lambda_{2}t})$$
usando la condizione iniziale $N_{2}(0)=0$. In forma di [[attività]] abbiamo
$$A_{2}(t)=\lambda_{2}N_{2}(t)=N_{0} \frac{\lambda_{1}\lambda_{2}}{\lambda_{2}-\lambda_{1}}(e^{-\lambda_{1}t}-e^{-\lambda_{2}t})$$

Se $\lambda_{1}\ll \lambda_{2}$, la madre vive talmente a lungo da decadere con un tasso quasi costante e quindi possiamo dire $e^{-\lambda_{1}t}\simeq1$, $\lambda_{1}\lambda_{2}\simeq \lambda_{1}$ e $\lambda_{2}-\lambda_{1}\simeq \lambda_{2}$. Allora
$$N_{2}(t)\simeq N_{0} \frac{\lambda_{1}}{\lambda_{2}}(1-e^{-\lambda_{2}t})$$
e quindi l'attività tende a diventare è costante
$$A_{2} \rightarrow \lambda_{1}N_{0} \quad \Rightarrow \quad \frac{dN_{2}}{dt}=0$$
Ciò significa che i nuclei figlie decadono ad un tasso pari a quello con cui sono create ($\lambda_{1}N_{1}=\lambda_{2}N_{2}$), rimanendo quindi in [[equilibrio secolare]]. Questo accade, ad esempio, nel decadimento $^{132}Te(78h) \rightarrow\ ^{132}I(2.28h) \rightarrow\ ^{132}Xe$ dopo circa 12 ore.

Se $\lambda_{1}<\lambda_{2}$, ma non di molto, posso calcolare il rapporto tra le attività:
$$\frac{\lambda_{2}N_{2}}{\lambda_{1}N_{1}}=\frac{\lambda_{2}}{\lambda_{2}-\lambda_{1}}(1-e^{-(\lambda_{2}-\lambda_{1})t}) \quad \xrightarrow{t \rightarrow \infty} \quad \frac{A_{2}}{A_{1}} \rightarrow \frac{\lambda_{2}}{\lambda_{2}-\lambda_{1}}$$
quindi col passare del tempo, le attività non diventano costanti, ma il rapporto tra le attività sì. Questo genere di equilibrio si dice [[equilibrio transiente]].

Se $\lambda_{1}>\lambda_{2}$, la madre decade velocemente e $A_{2}(t)$ cresce fino ad un massimo a causa dell'alta produzione di nuclei figlie e poi decade con $\lambda_{2}$. Dopo del tempo, il numero di nuclei $N_{1}$ diventa circa nullo e quindi $e^{-\lambda_{1}t}\rightarrow 0$. Si ha dunque
$$N_{2}(t)\simeq N_{0} \frac{\lambda_{1}}{\lambda_{1}-\lambda_{2}}e^{-\lambda_{2}t}$$
ossia le figlie decadono circa seguendo la legge di decadimento esponenziale.
### Decadimento ad $n$ passi
Se il decadimento continua per $n$ volte, allora avremo che la variazione dell'$n$-esima figlia sarà
$$dN_{n}=\lambda_{n-1}N_{n-1}dt-\lambda_{n}N_{n}dt$$
Questa equazione è risolta dall'**equazione di Bateman** nel caso in cui $N_{0}$ sia costituito solo da nuclei madre. L'attività $n$-esima è
$$A_{n}=N_{0}\sum\limits_{i=0}^{n}c_{i}e^{-\lambda_{i}t}=N_{0}(c_{1}e^{-\lambda_{1}t}+c_{2}e^{-\lambda_{2}t}+\ldots+c_{n}e^{-\lambda_{n}t})$$
dove $c_{i}$ è
$$c_{m}=\frac{\prod\limits_{i\neq m=1}^{n}\lambda_{i}}{\prod\limits_{i\neq m=1}^{n}(\lambda_{i}-\lambda_{m})}=\frac{\lambda_{1}\lambda_{2}\lambda_{3}\ldots\lambda_{n}}{(\lambda_{1}-\lambda_{m})(\lambda_{2}-\lambda_{m})\ldots(\lambda_{n}-\lambda_{m})}$$
dove nei produttori ometto il termine $i=m$. In questo caso, ho equilibrio secolare se le attività sono tutte uguali
$$\lambda_{1}N_{1}=\lambda_{2}N_{2}=\ldots=\lambda_{n}N_{n}$$