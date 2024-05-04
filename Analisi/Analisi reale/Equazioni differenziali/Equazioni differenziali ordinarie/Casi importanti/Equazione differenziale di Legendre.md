L'**equazione differenziale di Legendre** è l'[[equazione differenziale ordinaria]] di secondo ordine
$$(1-x^{2}) \frac{d^{2}y}{dx^{2}}-2x \frac{dy}{dx}+l(l+1)y=0$$
o anche scritta
$$\frac{d}{dx}\left[(1-x^{2}) \frac{dy}{dx}\right]+l(l+1)y=0$$
L'equazione ha [[Singolarità isolata|singolarità]] non essenziali in -1, 1 e $\infty$. Dato che è di secondo ordine, ha due soluzioni [[lineare indipendenza|linearmente indipendenti]]:
$$y=C_{1}P_{l}(x)+C_{2}Q_{l}(x)$$
Una soluzione regolare in tutti i punti al finito $P_{l}$ è nota come *funzione di Legendre del primo tipo* e se $l$ è un intero, questa funzione diventa una polinomio noto come [[Polinomi di Legendre|polinomio di Legendre]]. Una soluzione con singolarità in $\pm1$ $Q_{l}$ è nota come *funzione di Legendre del secondo tipo*.
### Equazione associata
L'equazione di Legendre può essere generalizzata ad una forma nota come **equazione differenziale associata di Legendre**, che aggiunge un secondo termine $m$ ed ha la forma
$$(1-x^{2}) \frac{d^{2}y}{dx^{2}}-2x \frac{dy}{dx}+ \left[l(l+1)- \frac{m^{2}}{1-x^{2}}\right]y=0$$
o anche
$$\frac{d}{dx}\left[(1-x^{2}) \frac{dy}{dx}\right]+\left[l(l+1)- \frac{m^{2}}{1-x^{2}}\right]y=0$$
Si può tornare al caso cui sopra ponendo $m=0$. Le soluzioni hanno sempre la forma
$$y=C_{1}P_{l}^{m}(x)+C_{2}Q_{l}^{m}(x)$$
dove $P_{l}^{m}$ si dice *funzione di Legendre associata del primo tipo*, che diventa un polinomio per $l$ intero e $m$ naturale, detto [[Polinomi di Legendre#Polinomi associati di Legendre|polinomio di Legendre associato]].