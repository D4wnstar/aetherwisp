Il **modello a gas di Fermi** è un modello del nucleo nello stato fondamentale di un [[atomo]]. Si basa su alcune supposizioni:
1. [[protone|protoni]] e [[neutrone|neutroni]] sono [[fermioni]].
2. i nucleoni si muovono liberamente nel nucleo.
### Formulazione
Consideriamo una [[particella]]. A causa del [[principio di indeterminazione]], essa occupa una volume $h^{3}=(2\pi\hbar)^{2}$ nello spazio delle fasi (6-dimensionale, posizione + impulso). Prendiamo un volume $V$ nello spazio e un volume $4\pi p^{2}dp$ con una calotta sferica di raggio $\bar{p}$ e spessore $d\bar{p}$ nell'impulso. Gli stati accessibili allora sono
$$dn=\frac{4\pi p^{2}dp}{2\pi\hbar^{2}}V$$
Allo stato fondamentale, la particella occupa tutti gli stati fino all'[[impulso di Fermi]] $p_{F}$. Dunque, integrando l'equazione precedente si trova
$$n=\frac{Vp_{F}^{3}}{6\pi^{2}\hbar^{3}}$$
Ricordando il [[principio di esclusione di Pauli]], abbiamo che uno stato può contenere al massimo due fermioni dello stesso tipo:
$$N=\frac{V(p_{F}^{n})^{3}}{3\pi^{2}\hbar^{3}}\quad;\quad Z=\frac{V(p_{F}^{p})^{3}}{3\pi^{2}\hbar^{3}}\quad;\quad R=R_{0}A^{1/3}=(121\text{ fm})A^{1/3}\tag{1}$$
Allora vale anche
$$V=\frac{4}{3}\pi R^{3}=\frac{4}{3}\pi R_{0}^{3}A\tag{2}$$
Posso continuare usando la semplificazione $N=Z=A/2$. Utilizzando $(1)$ e $(2)$ posso calcolare l'impulso di Fermi
$$p_{F}=p_{F}^{n}=p_{F}^{p}=\frac{\hbar}{R_{0}}=\left(\frac{9\pi}{8}\right)^\frac{1}{3}\sim250\text{ MeV/c}$$
che è un impulso molto grande se paragonato alla grandezza del nucleo. Calcoliamo anche l'[[energia di Fermi]]
$$E_{F}=\frac{p_{F}^{2}}{2M}\sim33\text{ MeV}$$
con $M=m_{n},m_{p}$.

Consideriamo una buca di potenziale rettangolare

![[Grafico Buca di potenziale rettangolare|center]]
con $B'=B/A\sim7-8\text{ MeV}$ e la profondità della buca è $V_{0}=B'+E_{F}\sim40\text{ MeV}$.

Calcoliamo anche l'energia cinetica media per nucleone
$$\langle E_{cin} \rangle=\frac{\int_{0}^{p_{F}}E_{cin}p^{2}dp}{\int_{0}^{p_{F}}p^{2}dp}=\frac{\frac{1}{5} \frac{1}{2m}p_{F}^{5}}{\frac{1}{3}p^{3}_{F}}=\frac{3}{10} \frac{p_{F}^{2}}{m}\sim20\text{ MeV}$$
L'energia cinetica totale sarà
$$E_{cin}=N \langle E_{n} \rangle+Z \langle E_{p} \rangle=\frac{3}{10M}[N(p_{F }^{n})^{2}+Z(p_{F}^{p})^{2}]$$
Mettendo dentro $p_{F}$ si ha
$$E_{cin}(N,Z)=\frac{3}{10M} \frac{\hbar^{2}}{R_{0}^{2}} \left(\frac{9}{4}\pi\right)^{2/3} \frac{N^{5/3}+Z^{5/3}}{A^{2/3}}$$
Nell'approssimazione $A=N+Z$ diventa
$$E_{cin}(A)=\frac{3}{10M} \frac{\hbar^{2}}{R_{0}^{2}} \left(\frac{9}{4}\pi\right)^{2/3}(A+\ldots)$$
dove $A$ contribuisce al termine di volume nella formula di massa.


