Il **modello a gas di Fermi** è un modello del [[Nucleo atomico|nucleo]] nello stato fondamentale di un [[atomo]] o debolmente eccitato. Si basa su alcune supposizioni:
1. [[protone|protoni]] e [[neutrone|neutroni]] sono sistemi indipendenti.
2. i nucleoni si muovono liberamente nel nucleo.

Al di là del nucleo atomico, è utile per spiegare il comportamento di materia neutronica a scala macroscopica, principalmente il nucleo delle [[Stella di neutroni|stelle di neutroni]].
### Formulazione
Il [[Potenziale]] a cui ciascun [[nucleone]] è soggetto è una sovrapposizione di tutti gli altri potenziali prodotti da altri nucleoni. Per il gas di Fermi, *assumiamo che il potenziale risultante sia una [[Buca finita quantistica|buca finita]] rettangolare*:

![[Grafico Buca di potenziale rettangolare|70%|center]]

A causa del [[Disuguaglianza di Heisenberg|principio di indeterminazione]], una [[Particella]] occupa un volume $h^{3}=(2\pi\hbar)^{3}$ nello [[Phase space]] (6-dimensionale, posizione + impulso). Prendiamo un volume $V$ nello spazio e un volume $4\pi p^{2}dp$ con una calotta sferica di raggio $p$ e spessore $dp$ nell'impulso. Gli [[stato|stati]] accessibili allora sono
$$dn=\frac{4\pi p^{2}dp}{(2\pi\hbar)^{3}}V$$
Allo stato fondamentale (allo zero assoluto), tutti gli stati più bassi sono occupati fino ad un impulso massimo detto **impulso di Fermi** $p_{F}$. Il numero di questi stati si ottiene integrando l'equazione precedente ed è
$$n=\int_{0}^{p_{F}}n(p)dp=\frac{Vp_{F}^{3}}{6\pi^{2}\hbar^{3}}$$
Ricordando il [[Pauli exclusion principle]], abbiamo che uno stato può contenere al massimo due [[Fermion|fermioni]] dello stesso tipo. Dato che sia protoni che neutroni sono fermioni, il numero di stati effettivo è
$$n=2 \frac{Vp_{F}^{3}}{6\pi^{2}\hbar^{2}}$$
e il numero di neutroni e protoni è dato da
$$N=\frac{V(p_{F}^{n})^{3}}{3\pi^{2}\hbar^{3}}\quad;\quad Z=\frac{V(p_{F}^{p})^{3}}{3\pi^{2}\hbar^{3}}\quad\tag{1}$$
*Assumendo* che il raggio del nucleo sia quello sperimentalmente determinato $R=R_{0}A^{1/3}$ (con $A$ [[Atomo|numero di massa atomica]] e $R_{0}=121$ fm), vale anche
$$V=\frac{4}{3}\pi R^{3}=\frac{4}{3}\pi R_{0}^{3}A\tag{2}$$
*Assumo* che le buche di potenziale abbiano lo stesso raggio sia per protoni che neutroni e che l'atomo sia neutro, ossia $N=Z=A/2$. Utilizzando $(1)$ e $(2)$ posso calcolare l'impulso di Fermi
$$\boxed{p_{F}=p_{F}^{n}=p_{F}^{p}=\frac{\hbar}{R_{0}}\left(\frac{9\pi}{8}\right)^\frac{1}{3}\simeq250\text{ MeV/c}}$$
che è un impulso molto grande per un nucleo. Calcoliamo anche l'energia dello più alto stato occupato, detta **energia di Fermi** $E_{F}$:
$$\boxed{E_{F}=\frac{p_{F}^{2}}{2M}\simeq33\text{ MeV}}$$
con $M=m_{n}$ o $m_{p}$.

La profondità nella buca dello stato più alto $B'$ è pari all'[[energia di legame]] medio per nucleone $B/A$ e vale circa $7-8$ [[Elettronvolt|MeV]]/nucleone. Sommato all'energia di Fermi, il fondo della buca è $V_{0}=B'+E_{F}\simeq40$ MeV. Come si vede, è indipendente da $A$.

Lo stato più energetico occupato è lo stesso per protoni e neutroni (dato che $p_{F}^{n}=p_{F}^{p}$), ma l'energia di Fermi (e quindi la profondità della buca), è *leggermente* diversa dato che $m_{n}> m_{p}$ e dunque $E_{F}^{n}>E_{F}^{p}$. Infatti, la buca dei neutroni è un po' più profonda di quella dei protoni e quindi i protoni appaiono meno legati rispetto ai neutroni. Questo può essere causato dal fatto che i protoni sono carichi positivamente e si repellono per [[interazione elettromagnetica]]. Il modello a gas di Fermi ci permette anche di calcolare la dipendenza dall'energia di legame dell'eccesso di neutroni.

Anzitutto, calcoliamo anche l'energia cinetica media per nucleone
$$\langle E_{cin} \rangle=\frac{\int_{0}^{p_{F}}E_{cin}p^{2}dp}{\int_{0}^{p_{F}}p^{2}dp}=\frac{\frac{1}{5} \frac{1}{2m}p_{F}^{5}}{\frac{1}{3}p^{3}_{F}}=\frac{3}{10} \frac{p_{F}^{2}}{m}\sim20\text{ MeV}$$
L'energia cinetica totale sarà
$$E_{cin}=N \langle E_{n} \rangle+Z \langle E_{p} \rangle=\frac{3}{10M}[N(p_{F }^{n})^{2}+Z(p_{F}^{p})^{2}]=\frac{3}{10M}(N+Z)p_{F}^{2}$$
Mettendo dentro $p_{F}$ si ha
$$E_{cin}(N,Z)=\frac{3}{10M} \frac{\hbar^{2}}{R_{0}^{2}} \left(\frac{9}{4}\pi\right)^{2/3} \frac{N^{5/3}+Z^{5/3}}{A^{2/3}}$$
che è valida per $A$ fisso. Si trova però che, variando $N$ e $Z$, la funzione ha un minimo in $N=Z$, quindi l'energia di legame diminuisce per $N\neq Z$. In pratica, asimmetria nella composizione dei nucleoni causa un indebolimento del nucleo. Ponendo
$$N=\frac{A+\Delta}{2}, \quad Z=\frac{A-\Delta}{2}; \quad \Delta\equiv N-Z$$
si ottiene
$$E_{cin}(A)=\frac{3}{10M} \frac{\hbar^{2}}{R_{0}^{2}} \left(\frac{9}{4}\pi\right)^{2/3} \left(A+ \frac{5}{9} \frac{(N-Z)^{2}}{A}+\ldots\right)$$
dove $A$ contribuisce al termine di volume nella [[Formula semiempirica di massa]], mentre il secondo termine è la correzione di asimmetria, che cresce con il quadrato di neutroni in eccesso.