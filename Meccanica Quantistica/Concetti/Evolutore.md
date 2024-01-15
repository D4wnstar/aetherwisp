Si chiama **evolutore** la funzione $\hat{U}_{t}$ tale che
$$\hat{U}_{t}=e^{- \frac{i}{\hbar}\hat{H}t}=\sum\limits_{i=1}^{\infty}e^{- \frac{i}{\hbar}E_{i}t}|E_{i}\rangle\langle E_{i}|$$
che rappresenta l'evoluzione temporale (*time evolution*) di un sistema quantistico. Esso risolve l'[[Equazione di Schrödinger]]. Ci permette di trovare lo [[stato]] del sistema ad un tempo $t$ semplicemente applicandolo allo stato $|\psi\rangle$ iniziale
$$|\psi_{t}\rangle=\hat{U}_{t}|\psi\rangle=\sum\limits_{i=1}^{\infty}e^{- \frac{i}{\hbar}E_{i}t} \langle E_{i}|\psi\rangle |E_{i}\rangle$$
Si trova che l'evolutore è reversibile ed è un operatore unitario, ossia
$$\hat{U}_{t}^{\dagger}\hat{U}_{t}=\hat{U}_{t}\hat{U}_{t}^{\dagger}=\hat{\mathbb{1}} \;\Rightarrow\; \hat{U}^{\dagger}_{t}=\hat{U}^{-1}_{t}$$
che è valido *solo* perché $\frac{i}{\hbar}t\hat{H}$ e $-\frac{i}{\hbar}t\hat{H}$ commutano. Questo è perché, esprimendo due esponenziali come serie esponenziale, si trova
$$e^{\hat{A}}e^{\hat{B}}\neq e^{\hat{A}+\hat{B}}$$
in generale. Ciò è vero solo se $\hat{A}$ e $\hat{B}$ commutano.