

Consideriamo un [[Potential]] descritto da una [[theta di Heaviside]]:
$$V(q)=\begin{cases}
0\quad &q<0 \\
V_{0}\quad &q\geq 0
\end{cases}$$
e l'[[equazione di Schrödinger]]:
$$- \frac{\hbar^{2}}{2m}\partial_{x} ^{2}\psi_{t}(x)+V(x)\psi_{t}(x)=(\hat{H}\psi_{t})(x)=i\hbar \partial_{t} \psi_{t}(x)$$
Per una [[particella]] ad energia costante $E$, $\psi_{t}$ è lo [[stato]] [[evolutore|evoluto]] all'energia $E$:
$$\psi_{t}(x)=e^{-(i/\hbar)Et}\psi_{E}(x)$$
allora
$$- \frac{\hbar^{2}}{2m}e^{-(i/\hbar)Et}\psi''_{E}(t)+e^{-(i/\hbar)Et}V(x)\psi_{E}(x)=Ee^{-(i/\hbar)Et}\psi_{E}(x)$$
$$\underbrace{ - \frac{\hbar^{2}}{2m}\psi''_{E}(x)+V(x)\psi_{E}(x) }_{ (\hat{H}\psi_{E})(x) }=E\psi_{E}(x)$$
Abbiamo due parti, una a sinistra del potenziale (con $V=0$) e una destra ($V=V_{0}$):
$$\text{Sinistra}: - \frac{\hbar^{2}}{2m}\psi''_{EL}(x)=E\psi_{EL}(x)$$
$$\text{Destra}: - \frac{\hbar^{2}}{2m}\psi''_{ER}(x)+ V_{0}\psi_{ER}(x)=E\psi_{ER}(x)$$
La parte sinistra è facilmente risolvibile
$$\psi_{EL}''(x)=- \frac{2mE}{\hbar ^{2}}\psi_{EL}(x)$$
La soluzione può essere espressa come somma di un'onda verso destra e una verso sinistra:
$$\psi_{EL}(x)=A_{EL}e^{(i/\hbar)\sqrt{ 2mE }\ x}+B_{EL}e^{(-(i/\hbar)\sqrt{ 2mE })\ x}$$
dove $\sqrt{ 2mE }=p$ è un momento. Come per tutti i coefficienti di un'espansione, i moduli quadri rappresentano probabilità. In questo caso $\lvert A_{EL} \rvert^{2}$ e $\lvert B_{EL} \rvert^{2}$ possono essere interpretate come la probabilità di oltrepassare e rimbalzare dalla barriera di potenziale. In termini di ottica ondulatoria, sono i coefficienti di trasmissione e riflessione dell'onda quantistica.

La parte destra diventa
$$\psi''_{ER}(x)=- \frac{2m}{\hbar ^{2}}(E-V_{0})\psi_{ER}(x)$$
ci interessa solo il caso in cui l'energia è superiore al potenziale
$$\begin{align}
&(E>V_{0}): \psi_{ER}^{I}(x)=A_{ER}e^{(i/\hbar)\sqrt{ 2m(E-V_{0}) }\ x}
\end{align}$$
Qui $\sqrt{ 2m(E-V_{0}) }=\tilde{p}$ è un altro momento.

Dobbiamo individuare le condizioni di raccordo in 0 tra il lato sinistro e destro:
$$\begin{cases}
\psi_{EL}(0)=\psi_{ER}(0) \\
\psi'_{EL}(0)=\psi'_{ER}(0)
\end{cases}$$
Per la prima condizione, basta avere
$$A_{EL}+B_{EL}=A_{ER}$$
Per la seconda
$$\frac{i}{\hbar}p(A_{EL}-B_{EL})=\frac{i}{\hbar}\tilde{p}A_{ER}$$
Insieme
$$\begin{cases}
A_{EL}+B_{EL}=A_{ER} \\
A_{EL}-B_{EL}=\frac{\tilde{p}}{p}A_{ER}
\end{cases} \quad\to \quad
\begin{cases}
1+ \frac{B_{EL}}{A_{EL}}=\frac{A_{ER}}{A_{EL}} \\
1- \frac{B_{EL}}{A_{EL}}=\frac{\tilde{p}}{p} \frac{A_{ER}}{A_{EL}}
\end{cases}$$
Sommando i termini in colonna
$$2= \frac{A_{ER}}{A_{EL}}\left( 1+ \frac{\tilde{p}}{p} \right)\quad\to \quad \frac{A_{ER}}{A_{EL}}=\frac{2p}{p+\tilde{p}}\quad\to$$
$$\to \quad\frac{B_{EL}}{A_{EL}}=\frac{A_{ER}}{A_{EL}}-1=\frac{2p}{p+\tilde{p}}=\frac{p-\tilde{p}}{p+\tilde{p}}$$
che sono sostanzialmente in [[Fresnel coefficients|coefficienti di Fresnel]], solo con il momento di una particella. Allora in generale, possiamo legare le due parti tramite una theta di Heaviside:
$$\psi_{E}(x)=A_{EL}\left[ (e^{(i/\hbar)px})+ \frac{p-\tilde{p}}{p+\tilde{p}}e^{-(i/\hbar)px}\Theta(-x)+ \frac{2p}{p+\tilde{p}}e^{(i/\hbar)px}\Theta(x) \right]$$
