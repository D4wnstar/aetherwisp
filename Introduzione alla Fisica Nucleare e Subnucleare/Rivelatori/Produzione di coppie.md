---
aliases:
  - sciame elettromagnetico
---
La **produzione di coppie** è un fenomeno ad altissima energia osservato nel quale si genera una coppia di una [[particella]] e la sua [[Antiparticella|antiparticella]].
### Produzione di coppie elettrone-positrone
Un caso noto è la produzione di coppie [[elettrone]]-[[Elettrone|positrone]] da parte di un [[fotone]]. Questo fenomeno avviene quando l'energia cinetica del fotone è almeno maggiore del doppio della massa dell'elettrone, quindi $E_{\gamma}>2m_{e}c^{2}$. Per generare la coppia, il fotone deve essere assorbito da qualche altra particella; non può avvenire nel vuoto dato che la [[massa invariante]] del fotone è nulla. Chiamando la particella assorbente $X$, il processo è
$$\gamma X\to Xe^{-}e^{+}$$

![[Schema Produzione elettrone-positrone|center]]

Il [[Legge di Beer-Lambert|coefficiente di assorbimento]] associato a questo fenomeno è
$$\mu _\text{PC}=\frac{7}{9} \frac{1}{L_{R}}$$
dove $L_{R}$ è la [[Potere frenante|lunghezza di radiazione]]. Questo lo rende quasi uguale al coefficiente di assorbimento del [[bremmstrahlung]], pari a $\mu _\text{PC}=L_{R}^{-1}$ (cambia solo di $7/9$).
#### Processi a cascata
Tipicamente, per fotoni ad energia abbastanza alta da compiere produzione di coppie, l'impatto con un materiale innesca un processo a cascata: mediamente ogni $L_{R}$, i fotoni creano una coppia elettrone-positrone, che a loro volta saranno deflessi per bremmstrahlung emettendo fotoni ad alta energia, che a loro volta possono creare coppie, e via avanti, moltiplicando i processi finché l'energia media non è sufficientemente diluita. Questo fenomeno è noto come **sciame elettromagnetico**.

Supponendo che l'energia iniziale $E_{\gamma}$ del fotone sia $E_{0}$, le prime particelle create avranno energia equipartita di $E_{0}/2$. Dopo $t$ lunghezze di radiazione, lo sciame è composto approssimativamente ad $N(t)=2^{t}$ particelle, ciascuna con energia $E/2^{t}$. Quando l'energia media degli elettroni scende sotto la soglia dell'energia critica (vedi [[Potere frenante#Perdita per radiazione]]), la moltiplicazione si ferma e gli elettroni perdono energia per ionizzazione più che per radiazione, diminuendo i fotoni prodotti per bremmstrahlung e ponendo fine alla catena. C'è quindi un tempo massimo $t_\text{max}=x_\text{max}/L_{R}$ (espresso in lunghezze di radiazione) tale che
$$E(t_\text{max})=E_{C}=\frac{E_{0}}{2^{t_\text{max}}}\quad \Rightarrow \quad t_\text{max}=\frac{ \ln\left( \frac{E_{0}}{E_{C}} \right)}{\ln 2}$$
La grandezza massima dello sciame aumenta solo logaritmicamente con l'energia della particella incidente. Questo è utile perché significa che l'energia della particella è dissipata in uno spazio piuttosto contenuto, il che rende gli assorbitori necessario per individuarla più piccoli (qualche lunghezza di radiazione).