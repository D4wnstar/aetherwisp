---
wiki-publish: true
aliases:
  - microstate
  - macrostate
  - pure state
  - mixed state
---
Lo **stato** è l'insieme di informazioni che definiscono completamente il sistema. Si distinguono **stati puri**, individuati da un singolo punto nello [[Phase space|spazio delle fasi]], e **stati misti**, individuati da una [[Probability distribution|distribuzione di probabilità]] nello spazio delle fasi. In altre parole, uno stato puro è determinato univocamente dai suoi parametri, mentre uno stato misto è una *miscela* di più stati puri. Un esempio di stato misto è un fascio di [[elettrone|elettroni]] con [[spin]] up e down, presumibilmente divisi al 50% l'un l'altro, mentre uno di stato puro sarebbe lo stesso fascio di elettroni selezionato da un [[Stern-Gerlach experiment|apparato di Stern-Gerlach]] a modo di avere solo spin up o down. Uno stato misto può nascere sia da un [[ensemble]] di stati puri, campionati a caso (come il fascio di elettroni), ma anche da due stati [[entanglement quantistico|intrecciati]].

In meccanica classica, conoscere lo stato puro significa sapere con esattezza tutte le [[Osservabile|osservabili]] di quel sistema. In meccanica quantistica, significa conoscere le distribuzioni di probabilità delle osservabili del sistema. Uno stato puro quantistico non può essere descritto come [[Convex combination]] di altri stati.

In sistemi composti da grandi numeri di [[particella|particelle]] (come quelli della meccanica statistica), si distinguono due tipi di stato, per convenienza. Si dice **microstato** l'insieme di tutti gli stati delle singole particelle, e **macrostato** lo stato del sistema in generale, identificato da alcune proprietà macroscopiche e un'[[Equation of state|equazione di stato]]. Il macrostato è uno stato misto composto dai microstati accessibili.
### Rappresentazione vettoriale
Uno stato può essere rappresentato da un vettore in un certo [[Vector space]], che dipende dal sistema in esame (o meglio, dalla matematica che si usano per formalizzarlo). In meccanica quantistica, il vettore esiste in uno [[spazio di Hilbert]] $\mathcal{H}$ ed è spesso rappresentato usando un [[Notazione braket|ket]]. Dunque, uno stato $\mathcal{S}$ può quindi essere scritto $|\mathcal{S}(t)\rangle\in \mathcal{H}$ (assumendo che vari nel tempo).

Come tutti i vettori, può essere espresso in termini di una [[base]] arbitraria dello spazio. Infatti, la [[funzione d'onda]] non è altro che il coefficiente dell'espansione nella base (o meglio, [[sistema ortonormale completo]]) delle [[Equazione agli autovalori|autofunzioni]] di una certa quantità. Per esempio, per la posizione
$$\Psi(x,t)=\langle x|\mathcal{S}(t)\rangle$$
e per la quantità di moto
$$\Phi(p,t)=\langle p|S(t)\rangle$$
dove $|x\rangle$ e $|p\rangle$ rappresentano l'autofunzione di $\hat{x}$ e $\hat{p}$ associata all'autovalore $x$ e $p$. Come ci si aspetta, otteniamo un coefficiente continuo. Nel caso di un'osservabile con [[Spettro]] discreto, come l'energia, troviamo coefficienti discreti:
$$c_{n}(t)=\langle n|\mathcal{S}(t)\rangle$$
con $|n\rangle$ l'$n$-esima autofunzione dell'[[operatore]] [[Hamiltoniana]] $\hat{H}$. La cosa più importante qui è che *sono tutti completamente equivalenti*. La funzione d'onda in posizione, quella in momento e i coefficienti dell'energia contengono tutti le stesse identiche informazioni; cambia solo il modo in cui vengono espressi. Infatti, è assolutamente possibile convertire tra queste quantità senza alcuna perdita di informazione:
$$\Psi(x,t)=\int_{-\infty}^{+\infty}\Psi(y,t)\delta(x-y)dy=\int_{-\infty}^{+\infty}\Phi(p,t) \frac{1}{\sqrt{2\pi\hbar}}e^{ipx/\hbar}dp=\sum\limits_{n=1}^{\infty}c_{n}e^{-iE_{n}t/\hbar}\psi_{n}(x)$$
### Rappresentazione proiettiva
I termini di operatori, gli stati puri corrispondono ad un [[proiettore]] che proietta su quello stato. Per esempio, uno stato puro $\psi$ è associato al proiettore
$$\hat{P}_{\psi}=\ket{\psi} \bra{\psi} \qquad\text{(stato puro)}$$
Uno stato misto, invece, è associato ad una [[Convex combination]] di proiettori:
$$\hat{\rho}=\sum_{i=1}^{d} \lvert \braket{ a_{i} | \psi }  \rvert ^{2}\hat{P}_{a_{i}}\qquad\text{(stato misto)}$$
dove $\ket{a_{i}}$ sono i singoli stati della miscela con i loro proiettori $\hat{P}_{a_{i}}$. La lettera $\rho$ è una lettera standard per denotare stati misti e rappresenta la [[matrice di densità]]. Algebricamente possiamo scrivere
$$\hat{\rho}=\sum_{i=1}^{d} \braket{ a_{i} | \psi } \ket{a_{i}} \bra{a_{i}} \braket{ \psi | a_{i} } =\sum_{i=1}^{d} \ket{a_{i}} \bra{a_{i}} \ket{\psi} \bra{\psi} \ket{a_{i}} \bra{a_{i}} =\sum_{i=1}^{d} \hat{P}_{a_{i}}\hat{P}_{\psi}\hat{P}_{a_{i}}$$
Quindi anche uno stato misto può essere visto esclusivamente in funzione dei proiettori sugli stati della miscela.

> [!example] Matrici di Pauli
> Consideriamo le [[matrici di Pauli]] rappresentate nella [[base]] delle $z$. I proiettori sugli autostati di $z$ sono
> $$\hat{P}_{\uparrow z}=\begin{pmatrix}
> 1 & 0  \\
> 0 & 0
> \end{pmatrix}\qquad \hat{P}_{\downarrow z}=\begin{pmatrix}
> 0 & 0  \\
> 0 & 1
> \end{pmatrix}$$
> Consideriamo uno stato generico $\ket{\psi}$ in $\mathbb{C}^{2}$ e il suo proiettore
> $$\hat{P}_{\psi}=\ket{\psi} \bra{\psi}=\begin{pmatrix}
> \alpha \\
> \beta
> \end{pmatrix}(\alpha^{*}\ \beta^{*})=\begin{pmatrix}
> \lvert \alpha \rvert ^{2} & \alpha \beta^{*} \\
> \alpha^{*}\beta & \lvert \beta \rvert ^{2}
> \end{pmatrix} $$
> Ricordiamo che
> $$\begin{pmatrix}
> \alpha  \\
> \beta
> \end{pmatrix}=\alpha \ket{\uparrow z} +\beta \ket{\downarrow z} $$
> quindi $\psi$ è una miscela convessa di stati up e down. Vogliamo rappresentare lo stato misto usando quanto abbiamo appena visto. Allora
> $$\hat{\rho}=\begin{pmatrix}1 & 0 \\
> 0 & 0\end{pmatrix}\begin{pmatrix}
> \lvert \alpha \rvert ^{2} & \alpha \beta^{*} \\
> \alpha^{*}\beta & \lvert \beta \rvert ^{2}
> \end{pmatrix}\begin{pmatrix}
> 0 & 0 \\
> 0 & 1
> \end{pmatrix}+\begin{pmatrix}
> 0 & 0 \\
> 0 & 1
 >\end{pmatrix}\begin{pmatrix}
> \lvert \alpha \rvert ^{2} & \alpha \beta^{*} \\
> \alpha^{*}\beta & \lvert \beta \rvert ^{2}
> \end{pmatrix}\begin{pmatrix}
> 1 & 0 \\
> 0 & 0
> \end{pmatrix}=$$
> $$=\begin{pmatrix}
> \lvert \alpha \rvert ^{2} & \alpha \beta^{*} \\
> 0 & 0
> \end{pmatrix}\begin{pmatrix}
> 1 & 0 \\
> 0 & 0
> \end{pmatrix}+\begin{pmatrix}
> 0 & 0 \\
> \alpha^{*}\beta & \lvert \beta \rvert ^{2}
> \end{pmatrix}\begin{pmatrix}
> 0 & 0 \\
> 0 & 1
> \end{pmatrix}=$$
> $$=\begin{pmatrix}
> \lvert \alpha \rvert ^{2} & 0 \\
> 0 & 0
> \end{pmatrix}+\begin{pmatrix}
> 0 & 0 \\
> 0 & \lvert \beta \rvert ^{2}
> \end{pmatrix}=\begin{pmatrix}
> \lvert \alpha \rvert ^{2} & 0 \\
> 0 & \lvert \beta \rvert ^{2}
> \end{pmatrix}$$
> che ci dà una matrice diagonale che rimuove i termini $\alpha \beta$, generalmente detti *termini di interferenza*.
