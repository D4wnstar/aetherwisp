---
aliases:
  - buca sferica infinita
---
La **buca sferica infinita** è un sistema quantistico definito da una [[Particella]] immersa nel [[potenziale]]
$$V(r)=\begin{cases}
0 \quad &\text{se }r<a \\
\infty \quad &\text{se }r>a
\end{cases}$$
È la versione sferica della [[Buca infinita quantistica|buca infinita]].

Vogliamo risolvere l'equazione radiale dell'[[Equazione di Schrödinger#Parte radiale|equazione di Schrödinger]]. Allora, entro la buca dove $V=0$, l'equazione radiale diventa
$$\frac{d^{2}u}{dr^{2}}=\left[\frac{l(l+1)}{r^{2}}-k^{2}\right]u$$
dove
$$k\equiv \frac{\sqrt{2mE}}{\hbar}$$
Vogliamo risolvere questa equazione, con la condizione al contorno $u(a)=0$.
### Caso $l=0$
Il caso $l=0$ è l'[[Oscillatore armonico]]:
$$\frac{d^{2}u}{dr^{2}}=-k^{2}u \Rightarrow u(r)=A\sin(kr)+B\cos(kr)$$
L'effettiva [[Funzione d'onda]] radiale è $R(r)=u/r$ quindi
$$R(r)=A \frac{\sin(kr)}{r}+ B \frac{\cos(kr)}{r}$$
ma $\cos(kr)/r \rightarrow \infty$ per $r \rightarrow 0$, che rendere la soluzione non normalizzabile, quindi[^1] $B=0$. La condizione al contorno quindi richiede $\sin(ka)=0$, cioè $ka=n\pi$ con $n$ intero. Allora le energie permesse sono
$$E_{n0}=\frac{n^{2}\pi^{2}\hbar^{2}}{2ma^{2}}$$
che sono le stesse della buca infinita.

Normalizzare $u(r)$ ci dà $A=\sqrt{2/a}$. Allora, la funzione d'onda è
$$\boxed{\psi_{n00}(r)=R(r)Y_{0}^{0}(\theta,\phi)=\frac{1}{\sqrt{2\pi a}} \frac{\sin\left(\frac{n\pi r}{a}\right)}{r}}$$
### Caso generale
La soluzione generica per un $l$ intero qualsiasi è molto più complicata:
$$u(r)=Arj_{l}(kr)+Brn_{l}(kr)$$
dove $j_{l}(x)$ è la [[funzioni di Bessel sferiche|funzione di Bessel sferica del primo tipo]] e $n_{l}(x)$ è quella del secondo tipo. $n_{l}$ va all'infinito all'origine, quindi deve essere $B=0$. Allora, sostituendo per $R$, si ha
$$R(r)=Aj_{l}(kr)$$

La condizione al contorno $R(a)=0$ obbliga ad avere una $k$ tale che
$$j_{l}(ka)=0$$
La $j_{l}$ è una funzione (pseudo)periodica, quindi ha un numero infinito (numerabile) di zeri. Purtroppo, non esiste una forma analitica per questi zeri, che invece vanno calcolati con metodi numerici. In ogni caso, deve essere
$$k=\frac{1}{a}\beta_{nl}$$
con $\beta_{nl}$ l'$n$-esimo zero della funzione sferica di $l$-esimo ordine. Dunque, le energie permesse sono date da
$$\boxed{E_{nl}=\frac{\hbar^{2}}{2ma^{2}}\beta^{2}_{nl}}$$

Combinando la parte radiale con le [[armoniche sferiche]] si ottiene la funzione d'onda
$$\boxed{\psi_{nlm}(r,\theta,\phi)=A_{nl}\,j_{l}\left(\frac{\beta_{nl}}{a}r\right)Y_{l}^{m}(\theta,\phi)}$$
con $A_{nl}$ la costante di normalizzazione. Ciascuno livello energetico è $(2l+1)$ volte degenere, dato che ci sono $(2l+1)$ valori di $m$ per ogni $l$.

[^1]: Sulla carta, $B=0$ è una richiesta eccessiva dato che rende la funzione *finita*, che è una condizione più forte di *normalizzabile*. Infatti, anche $R(r)\sim 1/r$ all'origine è normalizzabile, poiché che la condizione di normalizzazione è $\int|R|^{2}r^{2}dr$ e il $r^{2}$ si annulla anche in questo caso. Tuttavia, deve proprio essere $B=0$. Per una dimostrazione, vedi *Principles of Quantum Mechanics di R. Shankar, p. 342*.