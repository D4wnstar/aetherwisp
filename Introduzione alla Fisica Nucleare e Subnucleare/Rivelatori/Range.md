---
aliases:
  - percorso residuo
  - picco di Bragg
  - range straggling
---
In fisica delle particelle e dei rivelatori, il **range** o **percorso (medio) residuo** $R$ di una [[particella]] in un certo mezzo è la distanza che questa può percorrere prima di perdere tutta la sua energia. È definito come
$$R(E)=\int_{0}^{R}dx=-\int_{0}^{E_{0}} \frac{dE}{dE/dx}=\int_{0}^{E_{0}} \frac{1}{S(E)}dE$$
dove $R$ è il range medio, $E_{0}$ è l'energia iniziale della particella e $S(E)$ il [[potere frenante]].

Si misura in g/cm$^{2}$. A parità di energia cinetica, il range è fortemente dipendente dalla massa della particella, il che lo rende molto utile per determinarla una volta nota l'energia o impulso della particella.

Per una particella di carica $z$, massa $M$ ed energia non relativistica $E_{0}$, possiamo esprimere $dE/dx$ con la [[Potere frenante|formula di Bethe-Bloch]], trascurando il termine logaritmico abbiamo
$$\frac{dE}{dx}\sim \frac{z^{2}}{\beta^{2}}\sim \frac{KMz^{2}}{E}$$
dove $K$ è la costante in cui viene assorbito il logaritmo. Allora
$$R(E)=\int_{0}^{E_{0}}- \frac{dE}{dE/dx}\simeq \frac{K}{Mz^{2}}\int_{E_{0}}^{0}EdE=\frac{K}{Mz^{2}}E_{0}^{2}$$
Si vede che, data una certa energia cinetica iniziale, il range varia considerevolmente in funzione della massa. Più massiva è la particella, maggiore è la perdita di energia e meno materia attraversa. Proprio come la curva di Bethe-Bloch, questo fatto è molto utile per misurare la massa delle particelle.
### Range straggling
Come conseguenza del fatto che l'energia persa nel materiale non è costante ([[Potere frenante|energy straggling]]), il range è anch'esso soggetto alle stesse fluttuazioni. In realtà, sono anche presenti fluttuazioni dovute all'occasionale urto con un [[nucleo atomico]]. Come la controparte energetica, questo fenomeno è detto **range straggling**.
### Picchi di Bragg
Usando particelle pesanti ([[adrone|adroni]]), il range dipende da $\sim1/v^{2}\sim1/E$. Ciò implica che la perdita di energia non è lineare, bensì si accumula nei punti in cui la particella è più lenta. In altre parole, la maggior parte dell'energia è rilasciata quando la particella sta per fermarsi, ossia attorno alla distanza di range stesso. In un grafico, si può notare questo picco di energia attorno al range e vengono chiamati **picchi di Bragg**.