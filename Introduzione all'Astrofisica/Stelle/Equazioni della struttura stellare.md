La struttura delle [[stelle]] viene descritta da quattro equazioni.
1. L'**equazione di equilibrio idrostatico**: $$\frac{dP(r)}{dr}=- \frac{GM(r)\rho(r)}{r^{2}}$$dove $G$ è la [[constante gravitazionale]], $M$ è la massa della stella e $\rho$ è la sua densità. Tutto è in funzione della distanza dal centro $r$.
2. L'**equazione di continuità di massa**: $$\frac{dM(r)}{dr}=4\pi r^{2}\rho(r)$$
3. L'**equazione di trasporto energetico radiativo**: $$\frac{dT(r)}{dr}= \frac{3}{4\pi} \frac{\kappa L(r)\rho(r)}{r^{2}4\sigma T^{3}}$$dove $L$ è la [[luminosità]] della stella, $T$ è la sua temperatura, $\kappa$ è l'opacità e $\sigma$ è la [[costante di Stefan-Boltzmann]].
4. La **conservazione di energia** all'interno di una stella: $$\frac{dL}{dr}=4\pi r^{2}\rho(r)\epsilon(r)$$dove $\epsilon$ è il coefficiente di produzione energetica.

Esistono altre relazioni che possiamo sfruttare per capire le stelle. L'equazione dei gas perfetti vale se approssimiamo una stella come fatta di gas perfetto.
$$P(r)=n(r)T(r)\mbox{ con }n(r)=\frac{\rho(r)}{\mu m_{p}}$$
$\mu$ è il peso molecolare medio del gas e $m_{p}$ è la massa del protone.

L'opacità e il coefficiente di produzione energetica dipendono dalla densità, la temperatura e la composizione della stella:
$$\kappa,\epsilon\propto \rho,T,\mbox{composizione}$$

Abbiamo anche delle condizioni al contorno:
$$\begin{cases}
M(r=0)=0 \\
L(r=0)=0 \\
P(r=r_{\star})=0 \\
M(r=r_{\star})=M_{\star}
\end{cases}$$
Dunque in totale abbiamo 7 equazioni, di cui 4 principali, e 4 condizioni al contorno. Dalla teoria di analisi matematica sappiamo che se esiste una soluzione di questo problema con queste condizioni al contorno, allora la soluzione è unica. Che questa soluzione esista forma la base della **congettura di Vogt-Russel**, che dice che la nascita e l'intera evoluzione di una stella dipende solo e unicamente dalla sua massa e dalle sue condizioni iniziali. Questa è una semplificazione che non tiene conto di due fattori: rotazione e magnetismo. Sono comunque fattori minori che sono importanti solo in alcune stelle.