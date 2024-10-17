La **rappresentazione spettrale** di un operatore è una decomposizione in [[serie]] dell'operatore nella base creata dai suoi stessi autostati.
### Spettro discreto
Consideriamo un [[operatore autoaggiunto]] $\hat{A}=\hat{A}^{+}$ nello [[spazio di Hilbert]] $\mathcal{H}=\mathbb{C}^{n}$. Diciamo che questo operatore ha [[spettro]] discreto. Allora, i suoi [[Equazione agli autovalori|autostati]] (che sono [[Ortonormalità|ortonormali]]) costituiscono una [[base]] ortonormale in $\mathcal{H}$, $\{ \ket{a_{i}} \}_{i=1}^{n}$. ha autovalori reali, infatti presa l'[[equazione agli autovalori]]
$$\hat{A}\ket{a_{i}} =a_{i}\ket{a_{i}} $$
vale
$$a_{i}=\overline{a_{i}}\quad\Leftrightarrow\quad a_{i}\in \mathbb{R}$$
e anche
$$\braket{ a_{i} | a_{j} } =\delta_{ij}$$
usando la [[delta di Kronecker]]. Un qualunque vettore $\ket{\psi}\in \mathcal{H}$ può essere rappresentato come [[serie di Fourier]] in questa base:
$$\ket{\psi} =\sum_{i=1}^{n} \braket{ a_{i} | \psi } \ket{a_{i}}=\left( \sum_{i=1}^{n} \ket{a_{i}} \bra{a_{i}}  \right)\ket{\psi} =\sum_{i=1}^{n} \hat{P}_{a_{i}}\ket{\psi}  $$
usando il [[proiettore]] $\hat{P}_{a_{i}}=\ket{a_{i}} \bra{a_{i}}$ sull'autostato $\ket{a_{i}}$ (un proiettore su un autostato è detto **autoproiettore**). Allora possiamo esprimere l'azione dell'operatore come
$$\hat{A}\ket{\psi} =\sum_{i=1}^{n} a_{i}\braket{ a_{i} | \psi } \ket{a_{i}} =\sum_{i=1}^{n} a_{i}\ket{a_{i}} \bra{a_{i}} \ket{\psi} =\left( \sum_{i=1}^{n} a_{i}\hat{P}_{a_{i}} \right)\ket{\psi} $$
ma allora possiamo scrivere
$$\hat{A}=\sum_{i=1}^{n} a_{i}\hat{P}_{a_{i}}$$
che è la **rappresentazione spettrale**, ossia una decomposizione in [[serie]] di un operatore nella base creata dai suoi stessi autostati.


---



$$\Pi_{A,\psi}=\{ P_{\psi}^{A}(a_{i})=|\langle a_{i}|\psi\rangle|^{2}\},\; \hat{A}=\hat{A}^{\dagger}$$
$$\hat{A}|a_{i}\rangle=a_{i}|a_{i}\rangle,a_{i}\in\mathbb{R},\langle a_{i}|a_{j}\rangle=\delta_{ij}$$
$$\sum\limits_{i=1}^{\infty}P_{\psi}^{A}(a_{i})=\sum\limits_{i=1}^{\infty}\langle a_{i}\overbrace{|\psi\rangle \langle \psi|}\limits^{\hat{P}_\psi}a_{i}\rangle=\sum\limits_{i=1}^{\infty}\langle \psi\overbrace{|a_{i}\rangle \langle a_{i}|}\limits^{\hat{P}_{a_{i}}}\psi\rangle=\langle \psi|\left( \sum\limits_{i=1}^{\infty}\hat{P}_{a_{i}} \right)|\psi\rangle=\langle \psi|\psi\rangle=1$$
$$\langle \hat{A} \rangle_\psi=\sum\limits_{i=1}^{\infty}a_{i}P_{\psi}(a_{i})=\sum\limits_{i=1}^{\infty}a_{i}\langle \psi|a_{i}\rangle\langle a_{i}|\psi\rangle=\langle \psi|\underbrace{\left( \sum\limits_{i=i}^{\infty}a_{i}|a_{i}\rangle\langle a_{i}|\right)}\limits_\hat{A} |\psi\rangle$$
Il prodotto di proiettori di autovettori (*autoproiettori*) è
$$\hat{P}_{a_{i}}^{A}\hat{P}^{A}_{a_{j}}=|a_{i}\rangle\langle a_{i}|a_{j}\rangle\langle a_{j} |=\delta_{ij}|a_{i}\rangle\langle a_{j}|=\delta_{ij}\hat{P}^{A}_{a_{i}}$$
Quella che abbiamo trovato è la **notazione spettrale**.
$$|\psi\rangle=\sum\limits_{i=1}^{\infty}\langle a_{i}|\psi\rangle |a_{i}\rangle=\overbrace{\left( \sum\limits_{i=1}^{\infty}|a_{i}\rangle\langle a_{i}| \right)}\limits^{\mathbb{1}}|\psi\rangle$$
$$\begin{align}
\hat{A}|\psi\rangle&=\hat{A}\left( \sum\limits_{i=i}^{\infty}\langle a_{i}|\psi\rangle |a_{i}\rangle \right) = \sum\limits_{i=1}^{\infty}\langle a_{i}|\psi\rangle\hat{A} |a_{i}\rangle \\
&=\sum\limits_{i=1}^{\infty}\langle a_{i}|\psi\rangle a_{i} |a_{i}\rangle = \left( \sum\limits_{i=1}^{\infty}a_{i}\hat{P}^{A}_{a_{i}} \right)|\psi\rangle
\end{align}$$
Per fare l'ultima operazione bisogna che $a_{i}$ sia continua. Allora, espandendo in [[serie di potenze]] abbiamo che
$$\hat{A}=\hat{A}^{\dagger}=\sum\limits_{i=1}^{\infty}a_{i}|a_{i}\rangle\langle a_{i}|$$
$$f(x)=\sum\limits_{n=0}^{\infty}c_{n}x^{n}$$
$$\boxed{f(\hat{A})=\sum\limits_{i=1}^{\infty}f(a_{i})|a_{i}\rangle\langle a_{i}|}$$
che è una formulazione più generale del [[Teorema spettrale]].

**Dimostrazione.**
Sapendo che
$$\hat{A}^{2}=\hat{A}\hat{A}=\sum\limits_{i,j=1}^{\infty}a_{i}a_{j}|a_{i}\rangle\underbrace{\langle a_{j}|a_{i}\rangle}\limits_{\delta_{ij}}\langle a_{j}|=\sum\limits_{i=1}^{\infty}a_{i}^{2}|a_{i}\rangle\langle a_{i}|$$
più in generale posso scambiare i quadrati con l'$n$-esima derivata. Posso dimostrare la generalizzazione del teorema spettrale in questo modo
$$f(\hat{A})=\sum\limits_{n=0}^{\infty}c_{n}\hat{A}^{n}=\sum\limits_{n=0}^{\infty}\sum\limits_{i=1}^{\infty}c_{n}a_{i}^{n}|a_{i}\rangle\langle a_{i}|=\sum\limits_{i=1}^{\infty}\left( \sum\limits_{n=0}^{\infty}c_{n}a_{i}^{n} \right)|a_{i}\rangle\langle a_{i}|$$
$$\boxed{f(\hat{A})=\sum\limits_{i=1}^{\infty}f(a_{i})|a_{i}\rangle\langle a_{i}|}$$

Per esempio, torniamo all'[[uguaglianza di Schroedinger]] 
$$\begin{cases}
i\hbar\partial_{t}|\psi_{t}\rangle=-\hat{H}|\psi_{t}\rangle \Rightarrow^{\ast}\\ 
|\psi_{t=0}\rangle=|\psi\rangle
\end{cases}$$
$$^{\ast}\Rightarrow \partial_{t}|\psi_{t}\rangle=-\frac{i}{\hbar}\hat{H}|\psi_{t}\rangle = \partial_{t}\left( e^{- \frac{i}{\hbar}\hat{H}t} \right)|\psi\rangle=- \frac{i}{\hbar}\hat{H}e^{- \frac{i}{\hbar}\hat{H}t} |\psi\rangle$$
$$e^{- \frac{i}{\hbar}\hat{H}t}=\sum\limits_{n=0}^{\infty}\left( - \frac{i}{\hbar}t \right)^{n} \frac{\hat{N}^{n}}{n!}$$
$$\partial_{t}e^{- \frac{i}{\hbar}\hat{H}t}=- \frac{i}{\hbar}\hat{H}\sum\limits_{n=1}^{\infty}\left( - \frac{i}{\hbar} \right)^{n-1} \frac{t^{n-1}}{(n-1)!}H^{(n-1)}=$$
$$=- \frac{i}{\hbar}\hat{H}\sum\limits_{p=0}^{\infty}\left( - \frac{i}{\hbar} \right)^{p} \frac{t^{p}}{p!}H^{p}$$
Quindi troviamo che
$$\hat{H}=\sum\limits_{i=1}^{\infty}E_{i} |E_{i}\rangle\langle E_{i}|$$
dove $E_{i}$ sono le autofunzioni dell'Hamiltoniana. Dunque se riusciamo a trovare queste autofunzioni riusciamo a trovare esattamente l'evoluzione del sistema. Da qui possiamo definire l'[[evolutore]], che ci dà la descrizione dell'evoluzione temporale di un sistema quantistico.