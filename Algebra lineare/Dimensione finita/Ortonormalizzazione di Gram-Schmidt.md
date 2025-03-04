L'**ortonormalizzazione di Gram-Schmidt** è un algoritmo per trovare un sistema ortonormale di vettori a partire da un sistema di vettori [[lineare indipendenza|linearmente indipendenti]].

Questo metodo è applicabile in qualunque [[Vector space]], anche in quelli di dimensione infinita come gli [[Spazio di Hilbert|spazi di Hilbert]].
### Procedimento
Sia $\{v_{1},v_{2},\ldots,v_{n},\ldots\}$ un sistema possibilmente infinito di vettori linearmente indipendenti. Allora prendiamo il primo vettore $v_{1}$ e poniamo
$$e_{1}=\frac{v_{1}}{||v_{1}||}$$
Poi sottraiamo al secondo vettore $v_{2}$ la componente "parallela" a $e_{1}$, ossia
$$e_{2}'=v_{2}-(e_{1},v_{2})e_{1}$$
dove $(\cdot,\cdot)$ è il [[Prodotto scalare]]. Poniamo poi
$$e_{2}=\frac{e_{2}'}{||e_{2}'||}$$
Ora $e_{1}$ e $e_{2}$ sono ortonormali fra loro. Il procedimento ora si ripete con ogni altro vettore del sistema, con la cruciale differenza che all'$n$-esimo vettore si tolgono tutte le componenti "parallele" dei precedenti vettori, cioè
$$e'_{k}=v_{k}-\sum\limits_{i=1}^{k-1}(e_{i},v_{k})e_{i}\quad,\quad e_{k}=\frac{e_{k}'}{||e_{k}'||}$$
Il sistema $\{e_{1},e_{2},\ldots,e_{n},\ldots\}$ è ortonormale.