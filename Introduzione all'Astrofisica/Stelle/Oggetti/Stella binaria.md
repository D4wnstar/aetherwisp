---
aliases:
  - sistema binario
  - coppia ottica
  - binaria visuale
  - binaria astrometrica
  - binaria spettroscopica
  - binaria ad eclissi
---
Una **stella binaria** o **sistema binario** è un sistema di due [[Stella|stelle]] che sono gravitazionalmente vincolate e orbitano l'una attorno all'altra. I sistemi binari sono molto comuni: si stima che la metà di tutte le stelle dell'universo siano in realtà sistemi binari.
### Classificazione
La classificazione di una stella binaria segue dal metodo usato per identificarla.
1. **Coppie ottiche.** Una coppia ottica è una coppia di stelle visibili, talvolta anche a occhio nudo, apparentemente vicine fra loro. Queste *non* sono sistemi binari, in quanto non sono gravitazionalmente vincolate. Il fatto che appaiano vicine è una coincidenza causata dalla prospettiva.
2. **Binarie visuali.** Una binaria è simile ad una coppia ottica, ma è effettivamente un sistema di due stelle vincolate. Anche queste sono otticamente risolvibili con uno strumento sufficientemente sensibile.
3. **Binarie astrometriche.** Una binaria astrometrica è un sistema binario con una sola stella visibile. L'altra stella è rilevata osservando che quella visibile presenta un moto apparente lungo un'ellissi. Ciò indica che sta orbitando un'altra stella.
4. **Binarie spettroscopiche.** Una binaria spettroscopica è un sistema binario non otticamente risolvibile. Si distingue da una stella solitaria dal fatto che le [[Riga spettrale]] occasionalmente si sdoppiano, indicando la presenza di due stelle.
5. **Binarie ad eclissi.** Anche una binaria ad eclissi è un sistema non otticamente risolvibile. Si rilevano dal fatto che la luminosità del sistema diminuisce ad intervalli regolari, quando una delle due stelle eclissa l'altra.
### Misure
È possibile sfruttare la dinamica di un sistema binario per calcolare delle stima sulle stelle che lo compongono. Chiamiamo $m_{1}$ e $m_{2}$ le masse delle stelle e $v_{1}$ e $v_{2}$ le loro velocità attorno al centro di massa, assumendo un'orbita circolare. Allora sia $r=r_{1}+r_{2}$ la loro distanza, $P$ il periodo, $\Omega=2\pi/P$ la frequenza orbitale. Utilizzando le equazioni del moto circolare uniforme, del periodo orbitale e del centro di massa, si ha
$$\frac{m_{1}v_{1}^{2}}{r_{1}}=\frac{m_{2}v_{2}^{2}}{r_{2}}=G \frac{m_{1}m_{2}}{r}$$
$$P=\frac{2\pi r_{1}}{v_{1}}=\frac{2\pi r_{2}}{v_{2}}$$
$$m_{1}r_{1}-m_{2}r_{2}=0$$
da cui si ottiene (derivazione completa in [[Misure di massa stellare]])
$$\Omega^{2}=G\frac{m_{1}+m_{2}}{r^{3}}$$
$$v_{1}=\Omega r \frac{m_{2}}{m_{1}+m_{2}}$$
$$\frac{m_{2}}{m_{1}}=\frac{v_{1}}{v_{2}}$$
Alle sei incognite qui presenti, va aggiunta l'inclinazione $i$ dell'orbita, definita come l'angolo tra la normale del piano dell'orbita e la linea di vista. Dunque abbiamo tre equazioni per sette incognite. Ciò significa che per risolvere il sistema, dobbiamo avere stime per almeno quattro di questi valori.

Ci sono tre casi noti in cui si possono ottenere queste stime:
1. Per le binarie visuali, se la distanza da noi è nota, possiamo studiare l'orbita apparente e ricavarne il periodo $P$, la distanza $r$ e le velocità perpendicolari alla linea di vista $v_{1}\cos i$ e $v_{2}\cos i$.
2. Per le binarie spettroscopiche che sono anche binarie ad eclissi, se la fase di eclissi è breve rispetto al periodo orbitale, possiamo essere sicuri di osservare l'orbita quasi di taglio ($i\simeq90°$). Sapendo l'inclinazione, possiamo stimare massa e distanza a partire da $v_{1}\sin i$ e $v_{2}\sin i$ (calcolate al valore massimo) e $P$, così come il raggio delle stelle.
3. Per le binarie visuali, se si misura la differenza di velocità lungo la linea di vista. Gli spettri delle stelle delle binarie visuali possono mostrare differenze di velocità, portando ad una misura di $v\sin i$. In questo caso si possono ricavare, oltre a $P$, anche le componenti della velocità e da queste l'inclinazione. Si può ricavare anche la distanza da noi del sistema.

Studiando la curva di velocità di una binaria spettroscopica o l'orbita di una binaria visuale, è possibile ottenere informazioni sull'ellitticità dell'orbita.