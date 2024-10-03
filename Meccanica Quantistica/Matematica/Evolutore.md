Si chiama **evolutore** di un sistema quantistico l'[[operatore lineare]] $\hat{U}_{t}$ definito come
$$\hat{U}_{t}=e^{- \frac{i}{\hbar}\hat{H}t}=\sum\limits_{i=1}^{\infty}e^{- \frac{i}{\hbar}E_{i}t}|E_{i}\rangle\langle E_{i}|=\sum\limits_{i=1}^{\infty}e^{- \frac{i}{\hbar}E_{i}t}\hat{P}_{E_{i}}$$
con $\hat{H}$ la [[Hamiltoniana]] del sistema e $\hat{P}$ è l'[[operatore]] [[proiettore]]. L'evolutore genera l'evoluzione temporale (*time evolution*) di un sistema quantistico. Esso risolve l'[[equazione di Schrödinger]] dipendente dal tempo. Ci permette di trovare lo [[stato]] del sistema ad un tempo $t$ semplicemente applicandolo allo stato $|\psi\rangle$ iniziale
$$|\psi_{t}\rangle=\hat{U}_{t}|\psi\rangle=\sum\limits_{i=1}^{\infty}e^{- \frac{i}{\hbar}E_{i}t} \langle E_{i}|\psi\rangle |E_{i}\rangle$$
Nel caso in cui $|\psi\rangle$ siano un [[Equazione agli autovalori|autostato]] dell'[[Hamiltoniana]] con autovalore $E$, l'evolutore si semplifica a
$$|\psi_{t}\rangle=\hat{U}_{t}|\psi\rangle=e^{-iEt/\hbar}|\psi\rangle$$

> [!example] Dimostrazione
> Considerato uno stato generico $\ket{\psi}$, applicandogli l'evolutore, possiamo espanderlo in [[serie di Fourier]] dato che appartiene ad un [[sistema ortonormale completo]], ricordando che i coefficienti di Fourier sono $c_{E}=\braket{ \psi_{E} | \psi }$:
> $$\begin{align}
> \hat{U}_{t}\ket{\psi} &=\hat{U}_{t}\left( \sum_{E}\braket{ \psi_{E} | \psi } \ket{\psi_{E}}  \right) \\
> &=\sum_{E}\braket{ \psi_{E} | \psi } \hat{U}_{t}\ket{\psi_{E}}  \\
> &=\sum_{E}\braket{ \psi_{E} | \psi } e^{-(i/\hbar)Et} \ket{\psi_{E}} 
> \end{align}$$

Per il valor medio di un'[[osservabile]] al tempo $t$
$$\left\langle Q(t) \right\rangle=\langle \Psi(x,t)|\; \hat{Q}\; |\Psi(x,t)\rangle=\langle \Psi(x,0)|\;\hat{U}_{t}^{-1}\hat{Q}\hat{U}_{t}\;|\Psi(x,0)\rangle$$
difatti si dimostra che, presa una [[funzione d'onda]] che risolve l'equazione di Schrödinger, vale
$$\Psi(x,t+t_{0})=\Psi(x,t)e^{-\frac{i}{\hbar}\hat{H}t_{0}}=\Psi(x,t)\hat{U}_{t_{0}}$$

È quindi possibile trovare l'evoluzione temporale di un valor medio sia lasciando che la funzione d'onda tenga la dipendenza temporale, sia lasciando che l'operatore dell'osservabile la tenga. Queste sono le due principali [[rappresentazioni della meccanica quantistica]].
### Proprietà
L'evolutore è reversibile ed è un [[operatore unitario]], ossia
$$\hat{U}_{t}^{\dagger}\hat{U}_{t}=\hat{U}_{t}\hat{U}_{t}^{\dagger}=\mathbf{\hat{1}} \;\Rightarrow\; \hat{U}^{\dagger}_{t}=\hat{U}^{-1}_{t}$$
che è valido *solo* perché $\frac{i}{\hbar}t\hat{H}$ e $-\frac{i}{\hbar}t\hat{H}$ [[Commutatore|commutano]]. Questo è perché, esprimendo due esponenziali come [[serie esponenziale]], si trova
$$e^{\hat{A}}e^{\hat{B}}\neq e^{\hat{A}+\hat{B}}$$
in generale. Ciò è vero solo se $\hat{A}$ e $\hat{B}$ commutano.