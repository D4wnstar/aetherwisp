L'**esperimento di Stern-Gerlach** è un esperimento che ha scoperto quasi accidentalmente lo [[spin]] dell'[[elettrone]]. Il vero scopo dell'esperimento era misurare se le [[Particella|particelle]] avessero un momento angolare intrinseco.
### Teoria
Si consideri una spira circolare attraversata da una corrente $I$. Questa spira ha un momento di dipolo magnetico perpendicolare alla spira pari a $\vec{\mu}=I\vec{A}$.

![[Spira con momento di dipolo|40%|center]]
Per una spira di raggio $R$ con cariche $q$ a velocità $\vec{v}$ e lunghezza d'onda $\lambda$ si ha
$$I=\lambda v=\frac{q}{2\pi R} v$$
$$IA=\frac{q}{2\pi R}v\pi R^{2}=\frac{1}{2}qvR$$
Se la [[particella]] carica ha massa $M$, ha momento angolare $L=MvR$ e quindi
$$\vec{\mu}=\frac{1}{2} \frac{q}{M}\vec{L}$$
che è una *relazione generale tra un momento di dipolo magnetico e un momento angolare*. Per un elettrone, deve valere
$$\mu_{e}=\frac{1}{2} \frac{e}{m_{e}} S_{e}$$
con $S_{e}$ è lo spin dell'elettrone. In realtà questa relazione non è proprio corretta: la meccanica quantistica ci dice che esiste un fattore, detto *fattore giromagnetico* $g$, che riscala questa equazione, tale che
$$\mu_{e}=\frac{g}{2}\frac{e}{m_{e}}S_{e}$$
In questo caso, $g=2$.

Alternativamente, la relazione viene scritta nel modo equivalente
$$\mu_{e}=\frac{g}{2}\frac{e\hbar}{m_{e}} \frac{S_{e}}{\hbar}$$
e si definisce $e\hbar/m_{e}$ il [[magnetone di Bohr]] $\mu_{B}$. Una forma più generale ci dà la [[magnetizzazione]]:
$$\vec{M}=-g\mu_{B} \frac{\vec{J}}{h}$$
### Esperimento
L'esperimento consiste nel sparare un raggio di atomi di argento attraverso dei collimatori e poi far passare gli atomi attraverso due magneti polarizzati (uno nord, uno sud) con forma creata in modo tale da creare un campo magnetico disomogeneo. La disomogeneità produce una forza netta sugli atomi che ci passano attraverso. Gli atomi poi colpiscono un rivelatore per misurarne la traiettoria.

Classicamente, si dovrebbe osservare una distribuzione di tutti i possibili momenti: alcuni atomi vengono spinti verso l'alto, altri verso il basso, in base al loro momento. Ciò che si osserva è che ci sono solo due piccole regione del rivelatore in cui finiscono gli atomi: alcuni sono spinti verso l'alto, altri verso il basso, tutti più o meno alla stessa distanza dal centro. Ciò significa che gli atomi hanno un momento angolare intrinseco quantizzato con soli due possibili valori: uno che va "su" (*spin up*) e uno che va "giù" (*spin down*).