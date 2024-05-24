Il **modello a gas di Fermi** è un modello del [[Nucleo atomico|nucleo]] nello stato fondamentale di un [[atomo]] o debolmente eccitato. Si basa su alcune supposizioni:
1. [[protone|protoni]] e [[neutrone|neutroni]] sono sistemi indipendenti.
2. i nucleoni si muovono liberamente nel nucleo.
### Formulazione
Il [[potenziale]] a cui ciascun [[nucleone]] è soggetto è una sovrapposizione di tutti gli altri potenziali prodotti da altri nucleoni. Per il gas di Fermi, assumiamo che il potenziale risultante sia una [[Buca finita quantistica|buca finita]] rettangolare:

![[Grafico Buca di potenziale rettangolare|70%|center]]

A causa del [[Disuguaglianza di Heisenberg|principio di indeterminazione]], una [[particella]] occupa un volume $h^{3}=(2\pi\hbar)^{2}$ nello [[spazio delle fasi]] (6-dimensionale, posizione + impulso). Prendiamo un volume $V$ nello spazio e un volume $4\pi p^{2}dp$ con una calotta sferica di raggio $p$ e spessore $p$ nell'impulso. Gli [[stato|stati]] accessibili allora sono
$$dn=\frac{4\pi p^{2}dp}{2\pi\hbar^{2}}V$$
Allo stato fondamentale (allo zero assoluto), tutti gli stati più bassi sono occupati fino ad un impulso massimo detto **impulso di Fermi** $p_{F}$. Il numero di questi stati si integrando l'equazione precedente ed è
$$\int_{0}^{p_{F}}n(p)dp=\frac{Vp_{F}^{3}}{6\pi^{2}\hbar^{3}}$$
Ricordando il [[principio di esclusione di Pauli]], abbiamo che uno stato può contenere al massimo due [[fermione|fermioni]] dello stesso tipo. Dato che sia protoni che neutroni sono fermioni, il numero di stati effettivo è
$$n=2 \frac{Vp_{F}^{2}}{6\pi^{2}\hbar^{2}}$$
e il numero di neutroni e protoni è dato da
$$N=\frac{V(p_{F}^{n})^{3}}{3\pi^{2}\hbar^{3}}\quad;\quad Z=\frac{V(p_{F}^{p})^{3}}{3\pi^{2}\hbar^{3}}\quad\tag{1}$$
Assumendo che il raggio del nucleo sia quello sperimentalmente determinato $R=R_{0}A^{1/3}=(121\text{ fm})A^{1/3}$ (con $A$ [[Atomo|numero di massa atomica]] e $R_{0}=121$ fm), vale anche
$$V=\frac{4}{3}\pi R^{3}=\frac{4}{3}\pi R_{0}^{3}A\tag{2}$$
*Assumo* che le buche di potenziale abbiamo lo stesso raggio sia per protoni che neutroni e che l'atomo sia neutro, ossia $N=Z=A/2$. Utilizzando $(1)$ e $(2)$ posso calcolare l'impulso di Fermi
$$\boxed{p_{F}=p_{F}^{n}=p_{F}^{p}=\frac{\hbar}{R_{0}}\left(\frac{9\pi}{8}\right)^\frac{1}{3}\simeq250\text{ MeV/c}}$$
che è un impulso molto grande per un nucleo. Calcoliamo anche l'energia del più alto stato occupato, detta **energia di Fermi** $E_{F}$:
$$\boxed{E_{F}=\frac{p_{F}^{2}}{2M}\simeq33\text{ MeV}}$$
con $M=m_{n}$ o $m_{p}$.

La profondità nella buca dello stato più alto $B'$ è pari all'[[energia di legame]] per nucleone $B/A$ e vale circa $7-8$ [[Elettronvolt|MeV]]/nucleone. Sommato all'energia di Fermi, il fondo della buca è $V_{0}=B'+E_{F}\simeq40$ MeV. Come si vede, è indipendente da $A$.

Lo stato più energetico occupato è lo stesso per protoni e neutroni (dato che $p_{F}^{n}=p_{F}^{p}$), ma l'energia di Fermi (e quindi la profondità della buca), è *leggermente* diversa in virtù del fatto che la massa del protone è un pochino minore di quella del neutrone. Ciò significa che la buca dei protoni ???

Calcoliamo anche l'energia cinetica media per nucleone
$$\langle E_{cin} \rangle=\frac{\int_{0}^{p_{F}}E_{cin}p^{2}dp}{\int_{0}^{p_{F}}p^{2}dp}=\frac{\frac{1}{5} \frac{1}{2m}p_{F}^{5}}{\frac{1}{3}p^{3}_{F}}=\frac{3}{10} \frac{p_{F}^{2}}{m}\sim20\text{ MeV}$$
L'energia cinetica totale sarà
$$E_{cin}=N \langle E_{n} \rangle+Z \langle E_{p} \rangle=\frac{3}{10M}[N(p_{F }^{n})^{2}+Z(p_{F}^{p})^{2}]$$
Mettendo dentro $p_{F}$ si ha
$$E_{cin}(N,Z)=\frac{3}{10M} \frac{\hbar^{2}}{R_{0}^{2}} \left(\frac{9}{4}\pi\right)^{2/3} \frac{N^{5/3}+Z^{5/3}}{A^{2/3}}$$
Nell'approssimazione $A=N+Z$ diventa
$$E_{cin}(A)=\frac{3}{10M} \frac{\hbar^{2}}{R_{0}^{2}} \left(\frac{9}{4}\pi\right)^{2/3}(A+\ldots)$$
dove $A$ contribuisce al termine di volume nella formula di massa.


