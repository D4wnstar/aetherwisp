Si chiama **evolutore** l'[[Operatore]] $\hat{U}_{t}$ tale che
$$\hat{U}_{t}=e^{- \frac{i}{\hbar}\hat{H}t}=\sum\limits_{i=1}^{\infty}e^{- \frac{i}{\hbar}E_{i}t}|E_{i}\rangle\langle E_{i}|$$
che rappresenta l'evoluzione temporale (*time evolution*) di un sistema quantistico. Esso risolve l'[[equazione di Schrödinger]]. Ci permette di trovare lo [[stato]] del sistema ad un tempo $t$ semplicemente applicandolo allo stato $|\psi\rangle$ iniziale
$$|\psi_{t}\rangle=\hat{U}_{t}|\psi\rangle=\sum\limits_{i=1}^{\infty}e^{- \frac{i}{\hbar}E_{i}t} \langle E_{i}|\psi\rangle |E_{i}\rangle$$
o più in generale il valor medio di un'[[osservabile]] al tempo $t$
$$\left\langle Q(t) \right\rangle=\langle \Psi(x,t)|\; \hat{Q}\; |\Psi(x,t)\rangle=\langle \Psi(x,0)|\;\hat{U}_{t}^{-1}\hat{Q}\hat{U}_{t}\;|\Psi(x,0)\rangle$$
difatti si dimostra che, presa una [[funzione d'onda]] che risolve l'equazione di Schrödinger, vale
$$\Psi(x,t+t_{0})=\Psi(x,t)e^{\frac{-i}{\hbar}\hat{H}t_{0}}=\Psi(x,t)\hat{U}_{t_{0}}$$

È quindi possibile trovare l'evoluzione temporale di un valor medio sia lasciando che la [[funzione d'onda]] tenga la dipendenza temporale, sia lasciando che l'operatore dell'osservabile la tenga. La prima opzione si dice **Schrödinger picture**, mentre la seconda **Heisenberg picture**. Queste due forme sono equivalenti e la loro equivalenza viene detta [[dualità]].

Si trova che l'evolutore è reversibile ed è un [[Operatore unitario]], ossia
$$\hat{U}_{t}^{\dagger}\hat{U}_{t}=\hat{U}_{t}\hat{U}_{t}^{\dagger}=\hat{\mathbb{1}} \;\Rightarrow\; \hat{U}^{\dagger}_{t}=\hat{U}^{-1}_{t}$$
che è valido *solo* perché $\frac{i}{\hbar}t\hat{H}$ e $-\frac{i}{\hbar}t\hat{H}$ [[Commutatore|commutano]]. Questo è perché, esprimendo due esponenziali come serie esponenziale, si trova
$$e^{\hat{A}}e^{\hat{B}}\neq e^{\hat{A}+\hat{B}}$$
in generale. Ciò è vero solo se $\hat{A}$ e $\hat{B}$ commutano.