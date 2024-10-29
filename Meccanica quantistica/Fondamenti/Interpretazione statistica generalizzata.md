L'**interpretazione statistica generalizzata** è una spiegazione probabilistica della meccanica quantistica e dei suoi meccanismi.

Consideriamo un'[[osservabile]] $Q(x,p)$ per una [[Particella]] nello [[Stato]] denotato dalla [[funzione d'onda]] $\Psi(x,t)$. Se compiamo una misura, siamo certi di ottenere uno degli [[Equazione agli autovalori|autovalori]] dell'[[operatore autoaggiunto]] $\hat{Q}\left(x,-i\hbar \frac{d}{dx}\right)$.
- Se lo [[spettro]] di $\hat{Q}$ è discreto, la probabilità di ottenere un certo autovalore $q_{n}$ associato all'autofunzione [[Ortonormalità|ortonormale]] $f_{n}(x)$ è$$|c_{n}|^{2},\quad\text{con}\quad c_{n}=\langle f_{n}|\Psi\rangle$$
- Se lo spettro è continuo con autovalori reali $q(z)$ e autofunzioni [[Ortonormalità|Dirac-ortonormali]] associate $f_{z}(x)$, la probabilità di ottenere un risultato in un intervallo infinitesimo $dz$ è$$|c(z)|^{2}dz,\quad\text{con}\quad c(z)=\langle f_{z}|\Psi\rangle$$
Una volta completata la misura, la funzione d'onda collassa nell'autostato corrispondente.

Essendo parte di uno [[spazio di Hilbert]], una funzione d'onda $\Psi$ può essere scritta come [[Serie di Fourier|serie]] o [[trasformata di Fourier]] di un qualunque [[sistema ortonormale completo]]. Ciò permette alla funzione d'onda di essere [[Rappresentazioni dello stato|rappresentata]] in numerosi modi, in base a quale osservabile ci conviene (di solito la posizione):
$$\Psi(x,t)=\sum\limits_{n=1}^{\infty}c_{n}f_{n}(x)\quad\text{(con spettro discreto)}$$
$$\Psi(x,t)=\int_{-\infty}^{+\infty}c(k)e^{i(kx-at)}dk\quad\text{(con spettro continuo)}$$
e i coefficienti possono essere trovati come ci dice l'analisi di Fourier
$$c_{n}=\langle f_{n}|\Psi\rangle\quad \text{(discreto)},\quad c(k)=\langle f_{k}|\Psi\rangle\quad \text{(continuo)}\tag{1}$$
In entrambi i casi è possibile trovare $c$ usando la funzione d'onda a $t=0$. Questi coefficienti in realtà nascondono la componente temporale della funzione d'onda, quindi più correttamente andrebbero scritti $c_{n}(t)$ e $c(k,t)$.

I coefficienti rappresentano il "peso" di una autofunzione rispetto alle altre e di fatto sono la probabilità di ottenere un certo autovalore (o intervallo, se spettro continuo) durante una misura. I moduli quadri dei coefficienti si sommano/integrano a 1.
$$\sum\limits_{n=1}^{\infty}|c_{n}|^{2}=1\quad\text{(discreto)}, \quad \int_{-\infty}^{+\infty}|c(k)|^{2}dk=1 \quad\text{(continuo)}$$
quindi la successione di coefficienti discreti è in [[Spazi di successioni lp#Spazio $ ell {2}$|l^2]] e la funzione coefficiente continua è in [[Spazi Lp#Spazio $L {2}$|L^2]].

Il valore di aspettazione di un'osservabile è esprimibile in funzione di questi coefficienti
$$\left\langle Q \right\rangle=\sum\limits_{n=1}^{\infty}q_{n}|c_{n}|^{2}=1\quad\text{(discreto)}, \quad \left\langle Q \right\rangle =\int_{-\infty}^{+\infty}q(k)|c(k)|^{2}dk=1 \quad\text{(continuo)}$$
e più comunemente dalla funzione d'onda
$$\left\langle Q \right\rangle=\langle \Psi|\hat{Q}| \Psi\rangle$$

Controlliamo i casi importanti degli [[Operatore|operatori]] posizione e momento. Come visto in [[Autofunzioni di operatori autoaggiunti]], la posizione accetta qualunque numero reale $y$ come autovalore e ha come autofunzioni la [[delta di Dirac]]. Controlliamo che valga la $(1)$ continua:
$$c(y)=\langle \delta(x-y)|\Psi\rangle=\int_{-\infty}^{+\infty}\delta(x-y)\Psi(x,t)dx=\Psi(y,t)$$
e quindi la probabilità di trovare una particella in un intervallo $dy$ è $|\Psi(x,t)|^{2}dy$, esattamente come si era originariamente predetto. Allo stesso modo, controlliamo la quantità di moto, che ha autofunzioni $f_{p}(x)=(1/\sqrt{2\pi\hbar})\exp(ipx/\hbar)$:
$$c(p)=\langle f_{p}|\Psi\rangle=\frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^{+\infty}\Psi(x,t)e^{-ipx/\hbar}dx=\Phi(p,t)$$
Questa funzione, detta **funzione d'onda nello spazio dei momenti** rappresenta lo stesso identico stato fisico della **funzione d'onda nello spazio delle posizioni**, solo con una matematica diversa. Occasionalmente è più semplice risolvere un sistema fisico usando la rappresentazione dei momenti. Le due funzioni d'onda sono la trasformata l'una dell'altra:
$$\boxed{\begin{align}
\Phi(p,t)&=\frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^{+\infty}\Psi(x,t)e^{-ipx/\hbar}dx \\
\Psi(x,t)&=\frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^{+\infty}\Phi(p,t)e^{ixp/\hbar}dp
\end{align}}$$
Nella rappresentazione dei momenti, la probabilità di misurare una particella in un intervallo di momento $dp$ è $|\Phi(p,t)|^{2}$, analogo alla posizione.