Un **laser** (*Light Amplification by Stimulated Emission of Radiation*) è uno strumento che sfrutta l'[[emissione stimolata]] di radiazione per emettere [[Photon|fotoni]] in un raggio altamente collimato.
### Funzionamento
Un laser è composto da una cavità contenente un mezzo attivo circondato da specchi. Una spira circonda il mezzo attivo e una corrente viene generata da un alimentatore. Il campo elettromagnetico prodotto dalla spira causa l'emissione di fotoni dal mezzo. Uno degli specchi è semitrasparente: la maggior parte dei fotoni che lo colpiscono sono riflessi, ma alcuni rifrangono e sono convogliati verso l'esterno. Ciò crea un raggio di fotoni altamente collimato e possibilmente di altissima intensità.
![[Schema Laser|80%|center]]
Il laser sfrutta un sistema a tre livelli. Chiamiamo lo stato fondamentale 3 e gli stati eccitati 1 e 2, in quell'ordine. La tecnica per emettere radiazioni consiste nel "svuotare" lo stato eccitato 1, "spostando" i fotoni allo stato fondamentale 3. Ciò crea un eccesso di fotoni nello stato eccitato 2.

![[Schema Sistema a tre livelli|center]]

Chiamiamo $N_{1},N_{2},N_{3}$ il numero di fotoni in un certo stato. Allora nel tempo variano come
$$\frac{dN_{2}}{dt}=-N_{2}A_{21}-N_{2}A_{23}+u(\omega_{p})(N_{3}-N_{2})B_{23}-u(\omega)B_{21}(N_{2}-N_{1})$$
$$\frac{dN_{1}}{dt}=N_{2}A_{21}-N_{1}A_{13}+u(\omega)B_{21}(N_{2}-N_{1})$$
$$\frac{dN_{3}}{dt}=N_{2}A_{23}+N_{1}A_{13}-u(\omega_{p})B_{23}(N_{3}-N_{2})$$
con $\omega_{p}$ la frequenza di pompa (???). Chiamiamo $N=N_{1}+N_{2}+N_{3}$ e il tasso di pompaggio (*pumping rate*)
$$r=\frac{u(\omega_{p})B_{23}(N_{3}-N_{2})}{N}$$
Come nel [[sistema a due livelli]], deve valere $B_{23}=B_{32}$. Imponiamo una condizione di stazionarietà, ossia le tre derivate devono essere tutte uguali. Allora possiamo esprimere il numero di fotoni in un certo livello come
$$N_{1}=\frac{N(A_{21}+B_{21}u(\omega))r}{A_{13}(A_{23}+A_{21})+B_{21}u(\omega)(A_{13}+A_{23})}$$
$$N_{2}=\frac{N(A_{13}+B_{21}u(\omega))r}{A_{13}(A_{23}+A_{21})+B_{21}u(\omega)(A_{13}+A_{23})}$$
La *condizione di inversione di popolazione* è una condizione in cui uno stato di maggiore energia ha una popolazione maggiore di uno stato a minore energia. In questo caso la posso ottenere se $A_{21}<A_{13}$, ossia l'emissione spontanea dello stato 1 è più alta di quella dello stato 2.