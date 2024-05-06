La struttura di una [[stella]] comune (ossia senza peculiarità dovute a estrema rotazione, campi magnetici forti, ecc.) viene descritta da quattro equazioni:
1. L'**equazione di equilibrio idrostatico**: $$\frac{dP(r)}{dr}=- \frac{GM(r)\rho(r)}{r^{2}}$$dove $G$ è la [[constante gravitazionale]], $M$ è la massa della stella e $\rho$ è la sua densità. Tutto è in funzione della distanza dal centro $r$. Rappresenta l'equilibrio tra le uniche forze che si stanno considerando: la forza di gravità $F_{G}$ e le forze di pressione $F_{P}$, tali che $F_{G}+F_{P}=0$.
   
   Si può ottenere una stima della pressione con $$P\sim \frac{GM_{s}^{2}}{R^{4}}$$
2. L'**equazione di continuità di massa**: $$\frac{dM(r)}{dr}=4\pi r^{2}\rho(r)$$ che collega la massa e la densità di massa.
3. L'**equazione di stato dei gas perfetti**: $$P(r)=n(r)kT(r)\mbox{ con }n(r)=\frac{\rho(r)}{\mu m_{p}}$$con $k$ la [[costante di Boltzmann]]. $n$ è la densità di particelle per volume, ma non è una nuova variabile in quanto è ottenibile dalla densità di massa $\rho$ con $n(r)=\rho/\mu m_{p}$, con $m_{p}$ la massa del protone. L'equazione dei gas perfetti vale se approssimiamo una stella come fatta di gas perfetto.
   
   $\mu$ è il peso molecolare medio del gas, abbastanza simile a quella dell'atomo di idrogeno in questa approssimazione. $\mu$ dipende dalla composizione del gas: per una composizione solare altamente ionizzata si ha $\mu\simeq0.6$ e nel centro, dove l'idrogeno è parzialmente fuso con l'elio, si ha $\mu\simeq1$.
4. L'**equazione di generazione di energia** all'interno di una stella: $$\frac{dL}{dr}=4\pi r^{2}\rho(r)\epsilon(r)$$dove $\epsilon(\rho, T, \text{composizione})$ è l'energia generata per unità di massa e di tempo da un gas di composizione nota alla densità $\rho$ e temperatura $T$. $L(r)$ è l'energia che passa per una sfera di raggio $r$ dall'interno verso l'esterno. A $L(R_{\odot})$ rappresenta la [[luminosità]] della stella.
5. L'**equazione di trasporto energetico radiativo** (irradiazione): $$\frac{dT(r)}{dr}=- \frac{3}{4c} \frac{\kappa L(r)\rho(r)}{4\pi r^{2}\sigma T^{3}(r)}$$dove $L$ è la luminosità della stella, $T$ è la sua temperatura, $\kappa(\rho,T,\text{composizione})=1/\rho l$ è l'opacità ($l$ è il cammino libero medio di un fotone nella stella) e $\sigma$ è la [[costante di Stefan-Boltzmann]].

L'*equazione politropica* suppone una relazione tra la pressione $P$ e la densità del gas $\rho$
$$P\propto\rho^{\gamma}$$
dove $\gamma$ si dice *indice politropico*.

Abbiamo anche delle condizioni al contorno:
$$\begin{cases}
M(r=0)=0 \\
L(r=0)=0 \\
P(r=r_{\star})=0 \\
M(r=r_{\star})=M_{\star}
\end{cases}$$
Dunque in totale abbiamo 7 equazioni, di cui 4 principali, e 4 condizioni al contorno. Dalla teoria di analisi matematica sappiamo che se esiste una soluzione di questo problema con queste condizioni al contorno, allora la soluzione è unica. Che questa soluzione esista forma la base della **congettura di Vogt-Russel**, che dice che la nascita e l'intera evoluzione di una stella dipende solo e unicamente dalla sua massa e dalle sue condizioni iniziali. Questa è una semplificazione che non tiene conto di due fattori: rotazione e magnetismo. Sono comunque fattori minori che sono importanti solo in alcune stelle.