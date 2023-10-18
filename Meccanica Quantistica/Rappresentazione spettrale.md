
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
dove $E_{i}$ sono le autofunzioni dell'Hamiltoniana. Dunque se riusciamo a trovare queste autofunzioni riusciamo a trovare esattamente l'evoluzione del sistema. Chiamo inoltre **evolutore** la funzione
$$\boxed{\hat{U}_{t}=e^{- \frac{i}{\hbar}\hat{H}t}=\sum\limits_{i=1}^{\infty}e^{- \frac{i}{\hbar}E_{i}t}|E_{i}\rangle\langle E_{i}| }$$
$$\hat{U}_{t}|\psi\rangle=|\psi_{t}\rangle=\sum\limits_{i=1}^{\infty}e^{- \frac{i}{\hbar}E_{i}t} \langle E_{i}|\psi\rangle |E_{i}\rangle$$
quindi se abbiamo l'evolutore, abbiamo lo stato (probabilistico) del sistema in ogni dato tempo $t$.
$$\hat{A}^{2}=\hat{A}\hat{A}=\sum\limits_{i,j=1}^{\infty}a_{i}a_{j}|a_{i}\rangle\underbrace{\langle a_{j}|a_{i}\rangle}\limits_{\delta_{ij}}\langle a_{j}|=\sum\limits_{i=1}^{\infty}a_{i}^{2}|a_{i}\rangle\langle a_{i}|$$
più in generale posso scambiare i quadrati con l'$n$-esima derivata. Posso dimostrare la generalizzazione del teorema spettrale in questo modo
$$f(\hat{A})=\sum\limits_{n=0}^{\infty}c_{n}\hat{A}^{n}=\sum\limits_{n=0}^{\infty}\sum\limits_{i=1}^{\infty}c_{n}a_{i}^{n}|a_{i}\rangle\langle a_{i}|=\sum\limits_{i=1}^{\infty}\left( \sum\limits_{n=0}^{\infty}c_{n}a_{i}^{n} \right)|a_{i}\rangle\langle a_{i}|$$
$$\boxed{f(\hat{A})=\sum\limits_{i=1}^{\infty}f(a_{i})|a_{i}\rangle\langle a_{i}|}$$
