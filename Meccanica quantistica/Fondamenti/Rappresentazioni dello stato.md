---
aliases:
  - rappresentazione della posizione
  - rappresentazione del momento
---
In meccanica quantistica, lo [[stato]] di un [[Physical system|sistema]] è un concetto che può essere descritto in diverse forme, in base all'[[osservabile]] che si vuole considerare. Questa è una conseguenza del fatto che un vettore può essere rappresentato in forme diverse, tutte equivalenti, a dipendenza della [[base]] che si sceglie nello [[Vector space]] di definizione.

Dato che i sistemi quantistici sono descritti dalla meccanica hamiltoniana, le due rappresentazioni più comuni dello stato sono quelle della posizione e del momento (lineare).
### Rappresentazione della posizione
Considerato uno stato generico $\ket{\psi}$, la sua rappresentazione in posizione è pari a
$$\psi(x)=\braket{ x | \psi }=\int_{-\infty}^{\infty} \delta(y-x)\psi(y) \ dy$$
dove $\psi$ è la [[funzione d'onda]] associata allo stato $\ket{\psi}$.
### Rappresentazione del momento
Considerato uno stato generico $\ket{\phi}$, la sua rappresentazione in momento è pari a
$$\phi(p)=\braket{ p | \phi }=\bra{p} \left( \int_{-\infty}^{\infty} \ket{x} \bra{x}  \ dx \right) \ket{\phi}=\int_{-\infty}^{\infty} \braket{ p | x } \braket{ x | \phi }  \ dx  = \int_{-\infty}^{\infty} \frac{e^{-ipx/\hbar}}{\sqrt{ 2\pi \hbar }}\psi (x) \ dx$$
dove $\phi(p)$ è la funzione d'onda in momento associata allo stato $\ket{\phi}$, $\psi(x)$ è la funzione d'onda in posizione, usando la [[Proiettore|relazione di completezza]]. La funzione interna all'integrale proviene dalla
$$\braket{ x | p } =\frac{e^{ipx/\hbar}}{\sqrt{ 2\pi \hbar }}$$
### Rappresentazione generica
Siano $\{ \phi_{i} \}_{i \in 1}^{N}$ e $\{ x \}$ una base discreta e una continua definita in due [[spazio di Hilbert|spazi di Hilbert]] $\mathcal{H}$ composte dagli [[Equazione agli autovalori|autostati]] di un [[operatore]] $\hat{T}$ rappresentante un'osservabile. Allora un generico stato $\ket{\psi}$ può essere rappresentato in queste basi come
$$\begin{align}
\text{(discreto)}\qquad \psi(x)&=\sum_{i=1}^{N} c_{i}\psi_{i}(x) ,\quad  c_{i}=\braket{ \phi_{i} | \psi } \\
\text{(continuo)}\qquad \psi(x)&=\braket{ x  | \psi }
\end{align}$$
dove $c_{i}$ sono i [[Serie di Fourier|coefficienti di Fourier]] rispetto alla base e autovalori di $\hat{T}$ e $\psi_{i}(x)$ sono le autofunzioni associate.
### Equivalenza
La scelta della rappresentazione è una questione di convenienza. Tutte le rappresentazioni contengono la stessa quantità di informazioni e sono del tutto equivalenti l'un l'altra. È possibile convertire da le rappresentazioni senza perdita di generalità. Per passare da posizione a momento, per esempio, basta compiere una [[Trasformata di Fourier]]:
$$\phi(p)=\mathscr{F}[\psi(x)](p)= \int_{-\infty}^{\infty} \frac{e^{-ipx/\hbar}}{\sqrt{ 2\pi \hbar }}\psi (x) \ dx$$
e da momento a posizione un'antitrasformata:
$$\psi(x)=\mathscr{F}^{-1}[\phi(p)](x)=\int_{-\infty}^{+\infty}\frac{e^{ipx/\hbar}}{\sqrt{2\pi\hbar}} \phi(p)\ dp$$
