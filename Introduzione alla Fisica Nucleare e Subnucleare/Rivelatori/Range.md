---
aliases:
  - percorso residuo
  - picco di Bragg
  - range straggling
---
In fisica delle particelle e dei rivelatori, il **range** o **percorso (medio) residuo** $R$ di una [[particella]] in un certo mezzo è la distanza che questa può percorrere prima di perdere tutta la sua energia. È definito come
$$R(E)=\int_{0}^{R}dx=\int_{E_{0}}^{0} \frac{dE}{dE/dx}$$
Si misura in g/cm$^{2}$. A parità di energia cinetica, il range è fortemente dipendente dalla massa della particella, il che lo rende molto utile per determinarla una volta nota l'energia o impulso della particella.

Per una particella di carica $z$, massa $M$ ed energia $E_{0}$, possiamo esprimere $dE/dx$ con la [[Stopping power|formula di Bethe-Bloch]], trascurando il termine logaritmico abbiamo
$$\frac{dE}{dx}\sim \frac{z^{2}}{v^{2}}\sim \frac{Mz^{2}}{E}$$
da cui
$$R(E)=\int_{0}^{E_{0}}- \frac{dE}{dE/dx}\simeq \frac{K}{Mz^{2}}\int_{E_{0}}^{0}EdE=\frac{K}{Mz^{2}}E_{0}^{2}$$
### Range straggling
Come conseguenza del fatto che l'energia persa nel materiale non sia costante, ma descritta da una distribuzione, il range è anch'esso soggetto alle stesse fluttuazioni. In realtà, sono anche presenti fluttuazioni dovute all'occasionale urto con un [[Nucleo atomico]]. Come la controparte energetica, questo fenomeno è detto **range straggling**.
### Picchi di Bragg
Usando particelle pesanti ([[adrone|adroni]]), il range dipende da $\sim1/v^{2}\sim1/E$. Ciò implica che la perdita di energia non è lineare, bensì si accumula nei punti in cui la particella è più lenta. In altre parole, la maggior parte dell'energia è rilasciata quando la particella sta per fermarsi, ossia attorno alla distanza di range stesso. In un grafico, si può notare questo picco di energia attorno al range e vengono chiamati **picchi di Bragg**.