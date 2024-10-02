---
aliases:
  - pulsar
---
Una **stella di neutroni** è un [[relitto stellare]] formato quando una [[stella]] il cui nucleo supera il [[limite di Chandrasekhar]], ma non quello di [[limite di Tolman-Oppenheimer-Volkoff|Tolman-Oppenheimer-Volkoff]], collassa [[interazione gravitazionale|gravitazionalmente]] in un oggetto principalmente composto da [[Pressione degenere|materia degenere]] di [[neutrone|neutroni]].

Le stelle di neutroni sono in rotazione molto rapida, con periodi dai pochi secondi fino anche ai millisecondi. Questo fatto, assieme al getto di radiazioni che viene eiettato ai poli della stella per [[radiazione da sincrotrone]] che non è perfettamente allineato all'asse di rotazione, rende alcune stelle di neutroni delle [[stella variabile|stelle variabili]] con periodo molto basso e luminosità molto alta: questi oggetti sono detti **pulsar**.

Il motivo per cui i neutroni non [[Decadimento Beta#$ beta {-}$ nel vuoto|decadono]] $\beta^{-}$ è dovuto all'occupazione di tutti gli [[stato|stati]] quantistici possibili degli [[elettrone|elettroni]]. La densità del nucleo stellare è talmente alta che anche solo pochi decadimenti $\beta^{-}$ sono sufficienti per saturare i pochi stati disponibili. Per gli altri neutroni, il decadimento non è energeticamente viabile e quindi rimangono stabili come se fossero in un [[nucleo atomico]]. La percentuale di neutroni che decadono $\beta^{-}$ è circa il 0.5%.
### Formazione del nucleo
La presenza di soli neutroni ha conseguenze particolari:
- non c'è [[Interazione elettromagnetica|repulsione Coulombiana]].
- c'è solo [[interazione gravitazionale]].

La densità neutronica è $\sim10\rho_{N}$ (ottenuta da massa e volume della stella). Dato che sono create da [[supernova|supernove]], il nucleo contiene quasi esclusivamente $^{56}Fe$, di massa tra le 1 e 2 masse solari. A causa dell'enorme forza gravitazionale, il nucleo collassa in un volume molto piccolo e l'energia di Fermi degli elettroni aumenta a tal punto da permettere il [[Decadimento Beta|cattura elettronica]] $p+e^{-} \rightarrow n+\nu_{e}$. Applicato al ferro si ha
$$^{56}_{26}Fe+26e^{-}\rightarrow56n+26\nu_{e}$$
Questo processo si ferma soltanto quando la pressione di Fermi dei neutroni è sufficientemente alta ($\sim10^{18}kg/m^{3}$).
### Struttura interna
La massa è $M\sim1.3-1.5M_{\odot}$ e il raggio è $R\sim10$ km. La struttura interna di una stella di neutroni non è conosciuta; il meglio che possiamo fare sono predizioni teoriche. Usiamo allora un modello relativamente semplice, che afferma che in queste condizioni il nucleo sia un *liquido di neutroni degenere* a densità costante. La densità di questo liquido è elevatissima, a tal punto che la principale componente di repulsione è il [[principio di esclusione di Pauli]] che impedisce a più [[Fermione|fermioni]] di ricadere nello stesso stato energetico. Riducendo il volume, i neutroni sono dunque obbligati a occupare stati eccitati oltre a quello fondamentale.

Secondo questo modello, la crosta della stella è spessa circa 1 km ed è composta da atomi compressi allo stato solido dalla forza gravitazionale.

Cerchiamo di stimare il raggio della stella usando il [[modello a gas di Fermi]].. Per una massa $M=1.5M_{\odot}=3\times10^{30}$ kg sono presenti $N=1.8\times10^{57}$ neutroni (usando $m_{n}\sim1.67\times10^{-27}$ kg). Calcoliamo l'impulso di Fermi
$$p_{F}=\left(\frac{9}{4}\pi N\right)^{1/3} \frac{\hbar}{R}$$
dato che non ci sono protoni. L'energia cinetica media per ogni neutrone è
$$\left\langle \frac{E_{cin}}{N} \right\rangle=\frac{3}{5} \frac{p_{F}^{2}}{2M_{n}}=\frac{3\hbar^{2}}{10M_{n}} \left(\frac{9}{4}\pi N\right)^{2/3} \frac{1}{R^{2}}=\frac{c}{R^{2}}$$
con
$$c=\frac{3\hbar^{2}}{10M_{n}} \left(\frac{9}{4}\pi N\right)^{2/3}$$
L'energia [[potenziale]] (gravitazionale) media di un singolo neutrone, a partire dal potenziale gravitazionale di una stella a densità costante, è
$$\left\langle \frac{E_{pot}}{N} \right\rangle=- \frac{3}{5} \frac{GNM_{n}^{2}}{R}$$
con $G$ la [[Costante gravitazionale]] (il termine 3/5 deriva dall'integrale per la media). Allora la stella è all'equilibrio quando l'energia per [[nucleone]] è minima, ossia cerco il [[Punto critico|punto stazionario]]:
$$\frac{d}{dR} \left\langle \frac{E}{N} \right\rangle= \frac{d}{dR}\left[ \left\langle \frac{E_{cin}}{N} \right\rangle + \left\langle \frac{E_{pot}}{N} \right\rangle\right]=0$$
da cui possiamo stimare il raggio della stella
$$R=\frac{\hbar^{2}(\frac{9}{4}\pi)^{2/3}}{GM_{n}^{3}N^{1/3}}\sim12\text{ km}$$
che è molto simile a quello misurato sperimentalmente di $\sim10$ km. Per la densità invece ottengo
$$\rho=\frac{N}{V}=\frac{1.8\times10^{57}}{\frac{4}{3}\pi R^{3}}\simeq0.25\frac{\text{nucleoni}}{\text{fm}^{3}}$$
che è circa 1.5 volte la densità nucleonica del [[nucleo atomico]], di circa $0.17$ nucleoni/fm$^{3}$.

In realtà, la situazione è più complicata e la densità non è costante. Si possono giungere a valori fino a $\sim10\rho$, ai quali $R$ sarebbe molto minore. In quei casi, ci sarebbe una forte componente di repulsione neutrone-neutrone che li potrebbe a riallontanarsi. Allora, in conclusione, l'equilibrio della stella contro la forza gravitazionale è dato in egual parti dalla pressione di Fermi e dalla repulsione neutrone-neutrone. La sovrapposizione di neutroni è massima al suo centro, dove le condizioni sono talmente estreme da possibilmente creare una regione di [[plasma di quark e gluoni]].