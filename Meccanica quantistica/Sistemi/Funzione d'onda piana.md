---
wiki-publish: true
---
In generale, la descrizione di un sistema quantistico parte dalla scelta della funzione [[Potential]] che fa parte dell'[[equazione di Schrödinger]], che poi si risolve per trovare la [[funzione d'onda]] associata. Può essere interessante anche andare a ritroso, annullando il potenziale (e quindi considerando una [[particella libera (quantistica)]]) e decidendo a priori la funzione d'onda d'interesse, vedendo poi cosa ne deriva. Per questo caso, consideriamo il sistema di una particella libera $V=0$ con una funzione d'onda descritta da una [[Plane wave|onda piana]] della forma
$$\psi_{p}(x)=A_{p}e^{(i/\hbar)px}$$
dove $A_{p}$ è un coefficiente di [[Normalization]].

Sappiamo che in meccanica quantistica, la posizione e il momento sono definiti come [[operatore|operatori]] $\hat{q}$ e $\hat{p}$. L'operatore momento si applica cambiando il segno e moltiplicando per $i\hbar$:
$$(\hat{p}\psi)(x)=-i\hbar \partial_{x}  \psi(x)\tag{1}$$
dove $\psi$ è una [[funzione d'onda]]. Allora usando l'onda piana trovo
$$(\hat{p}\psi)(x)=p\psi_{p}(x)$$
che è un'[[equazione agli autovalori]].

Tuttavia, il modulo di un'onda piana è costante, quindi non è a [[Spazi Lp#Spazio $L {2}$|quadrato sommabile]]. Ma abbiamo bisogno che lo sia per rappresentare uno stato fisico, quindi quindi ci serve una costante di normalizzazione $A_{p}$ che possa normalizzare lo stato. Prendiamo due funzioni
$$\psi_{p_{1}}(x)=A_{p_{1}}e^{(i/\hbar)p_{1}x},\qquad\psi_{p_{2}}(x)=A_{p_{2}}e^{(i/\hbar)p_{2}x}$$
e cerchiamo il prodotto scalare
$$\braket{ \psi_{p_{1}} | \psi_{p_{2}} } =\int_{-\infty}^{\infty} \overline{\psi_{p_{1}}(x)}\psi_{p_{2}}(x) \, dx =\overline{A_{p_{1}}}A_{p_{2}}\int_{-\infty}^{\infty} \frac{e^{(i/\hbar)x(p_{2}-p_{1})}}{2\pi \hbar}(2\pi \hbar) \, dx =$$
ma le $\psi$ non sono integrabili: per raggiungere un risultato dobbiamo accettare di andare al di là del dominio delle funzioni e introdurre una [[distribuzione]] in cui mettere l'integrale:
$$=\overline{A_{p_{1}}}A_{p_{2}}2\pi \hbar \delta(p_{1}-p_{2})=\delta(p_{1}-p_{2})$$
dove $\delta$ è la [[delta di Dirac]] e allora
$$A_{p_{1}}=A_{p_{2}}=A_{p}=\frac{1}{\sqrt{ 2\pi \hbar }}$$
Allora la funzione d'onda piana che descrive un [[Particella libera (quantistica)|particella quantistica libera]] in una dimensione $x$ con un dato momento costante $p$ è
$$\boxed{\psi_{p}(x)=\frac{e^{(i/\hbar)px}}{\sqrt{ 2\pi \hbar }}}$$
e come tutte le funzioni non-$L^{2}$, non ha uno [[Spettro]] discreto, ma continuo. Ciò significa che non ha autostati discreti (ossia specifici scalari) ma solo una funzione continua. La [[Particle]] descritta da una funzione d'onda piana non è localizzata in nessun particolare luogo dello spazio: è distesa attraverso tutto l'asse reale. Infatti, si comporta allo stesso modo di un'onda piana come vista dall'ottica: c'è un vettore di direzione (il [[wave vector|vettore d'onda]]), ma non "è" in nessun particolare luogo. In altre parole, non c'è un [[wave packet|pacchetto d'onda]] che può *localizzare* l'onda in nessun luogo. Dalla dualità particella-onda, lo stesso può essere applicato alla meccanica quantistica: non esiste un pacchetto d'onda per localizzare nello una particella descritta da una funzione d'onda piana. In generale, la meccanica quantistica è una generalizzazione della meccanica analitica canonica secondo Hamilton in forma ondulatoria, tant'è che originariamente era stato proposto il nome "meccanica ondulatoria".

Se cerchiamo la funzione d'onda rispetto alla posizione $x_{0}$ anziché al momento $p$, abbiamo
$$(\hat{q}\tilde{\psi}_{x_{0}})(x)=x_{0}\tilde{\psi}_{x_{0}}(x)$$
dove
$$\tilde{\psi}_{x_{0}}(x)=\delta(x-x_{0})$$
che, non essendo una funzione, non può essere trattata in modo normale.

Va notato che la rappresentazione in posizione $(\hat{q}\psi)(x)=x\psi(x)$, in questo caso, *non è* un'equazione agli autovalori.

### Evoluzione temporale
Ora che abbiamo la descrizione dello stato, possiamo occuparci della dinamica, almeno in un modo euristico. Vogliamo evolvere lo stato $\ket{\psi}$ nello stato $\ket{\psi_{t}}$ nel tempo secondo un'[[Hamiltonian]]. Questo viene fatto attraverso l'[[equazione di Schrödinger]]:
$$i\hbar \partial_{t} \ket{\psi_{t}} =\hat{H}\ket{\psi_{t}} $$
Per una particella libera, l'Hamiltoniana è
$$H=\frac{p^{2}}{2m}\quad\to \quad \hat{H}=\frac{\hat{p}^{2}}{2m}$$
La nostra funzione d'onda nel momento è
$$\psi_{p}(x)=\frac{e^{(i/\hbar)px}}{\sqrt{ 2\pi \hbar }}$$
Un'onda piana generica nel tempo è
$$e^{i(kx-\omega t)}=e^{i/\hbar(px-\hbar \omega t)}$$
usando la [[formula di de Broglie]]. Ma $\hbar \omega$ è un'energia, quindi possiamo dire
$$e^{i/\hbar(px-Et)}$$
e esprimendo la funzione piana d'onda in questo modo abbiamo
$$\psi_{p}(x,t)=\frac{e^{(i/\hbar)(px-Et)}}{\sqrt{ 2\pi \hbar }}=\frac{e^{(i/\hbar)(px-(p^{2}/2m)t)}}{\sqrt{ 2\pi \hbar }}$$
sapendo che $E=\frac{p^{2}}{2m}$ per una particella nel vuoto.

---

ossia come il prodotto scalare tra un autoket di posizione $x$ e un autoket di momento $p$, cioè la rappresentazione di $p$ su $x$. Ma prendendo il coniugato posso trovare anche la forma simmetrica $\langle p|x\rangle$ che ci dà la rappresentazione di $x$ su $p$, che è del tutto equivalente in termini fisici. Matematicamente, non è altro che una [[Trasformata di Fourier]] da $x$ a $p$ o viceversa:
$$\psi:L^{2}(\mathbb{R},dx)\rightarrow L^{2}(\mathbb{R},dx),\quad \psi(x)\rightarrow\tilde{\psi}(p)=\int_{-\infty}^{+\infty}dx \frac{e^{\frac{i}{\hbar}px}}{\sqrt{2\pi\hbar}}\psi(x)$$
Valgono anche $\langle x_{0}|x\rangle=\delta(x-x_{0})$ e l'antitrasformata
$$\psi(x)=\int_{-\infty}^{+\infty}dp \frac{e^{-\frac{i}{\hbar}xp}}{\sqrt{2\pi\hbar}}\tilde{\psi}(p)$$
La trasformata di Fourier ci fa passare dalla *rappresentazione delle posizioni* alla *rappresentazione dei momenti* e l'antitrasformata ci riporta indietro. L'onda piana fa da tramite.

Valutando il ket $\psi$ nel punto $x$ si ha
$$\langle x|\psi\rangle=\int_{-\infty}^{\infty}dp \langle x|p\rangle \langle p|\psi\rangle$$
ma l'$x$ è libero quindi deve essere
$$|\psi\rangle=\int_{-\infty}^{\infty}dp |p\rangle \langle p|\psi\rangle \Leftrightarrow \int_{-\infty}^{\infty}dp |p\rangle\langle p|=\hat{\mathbb{1}}$$
Ricapitolando abbiamo
$$\boxed{\langle x|p\rangle=\frac{e^{\frac{i}{\hbar}px}}{\sqrt{2\pi\hbar}}}$$
$$\boxed{\langle p|x\rangle=\frac{e^{-\frac{i}{\hbar}px}}{\sqrt{2\pi\hbar}}}$$
Ossia $\hat{p}=-i\hbar \partial_{x}$ e $\hat{x}=i\hbar\partial_{p}$.

Le completezze sono *molto utili* per cambiare rappresentazione
$$\langle x|\hat{x}\psi\rangle=\langle x|p\rangle \langle p|\hat{x}\psi\rangle=\ldots$$
usando che $\int_{-\infty}^{\infty}dp |p\rangle\langle p|=\hat{\mathbb{1}}$. Allora troviamo la rappresentazione di $\hat{x}\psi$ in $p$, che possiamo risolvere
$$\ldots=\int_{-\infty}^{\infty}dp \langle x|p\rangle\langle p|\hat{x}\psi\rangle=\int_{-\infty}^{\infty}dp \langle p|x\rangle=\int_{-\infty}^{\infty}dp\frac{e^{-\frac{i}{\hbar}px}}{\sqrt{2\pi\hbar}}i\hbar\partial_{p}\langle p|\psi\rangle=\ldots$$
dato che c'è una derivata dentro l'integrale nella stessa variabile di integrazione, conviene integrare per parti
$$\begin{align}
\ldots=\int_{-\infty}^{\infty}dp\frac{i\hbar}{\sqrt{2\pi\hbar}}\left[ \partial_{p}\left(e^{\frac{i}{\hbar}px}\langle p|\psi\rangle\right) -\left( \partial_{p}e^{\frac{i}{\hbar}px}\langle p|\psi\rangle\right)\right] =\\
=\frac{i\hbar}{\sqrt{2\pi\hbar}}e^{\frac{i}{\hbar}px}\langle p|\psi\rangle \Big|_{-\infty}^{\infty}+x\underbrace{\int_{-\infty}^{\infty}dp\frac{e^{\frac{i}{\hbar}px}}{\sqrt{2\pi\hbar}}\langle p|\psi\rangle}\limits_{\psi(x)}
\end{align}$$
Notando che $\langle p|\psi\rangle\in L^{2}(\mathbb{R},dx)$, sappiamo che all'infinito tende a zero, quindi i termini al bordo sono entrambi nulli. Abbiamo quindi trovato
$$(\hat{x}\psi)(x)=\langle x|\hat{x}\psi\rangle=x\psi(x)$$
Valgono anche
$$(\hat{p}\psi)(p)=\langle p|\hat{p}\psi\rangle=p\tilde{\psi}(p)=p\langle p|\psi\rangle=p\tilde{\psi}(p)$$
$$(\hat{p}\psi)(x)=\langle x|\hat{p}\psi\rangle=-i\hbar\partial_{x}\langle x|\psi\rangle=-\hbar\partial_{x}\psi(x)$$
$$\langle p|\hat{x}\psi\rangle=i\hbar\partial_{p}\langle p|\psi\rangle$$

Riassumendo i prodotti scalari:
- Nella stessa rappresentazione: $\langle \bar{x}|x\rangle=\delta(x-\bar{x})$
- In una diversa rappresentazione: $\langle p|x\rangle=\frac{e^{-\frac{i}{\hbar}px}}{\sqrt{2\pi\hbar}}$
- Con una base ortonormale $\{\phi_{i}\}_{i=1}^{n}$: $\langle \phi_{i}|x\rangle=\overline{\langle x|\phi_{i}\rangle}=\phi_{i}^{\ast}(x)$

Prendiamo il commutatore
$$[\hat{x},\hat{p}]=\hat{x}\hat{p}-\hat{p}\hat{x}$$
$$\langle x|[\hat{x},\hat{p}]|\psi\rangle=\langle x|\hat{x}\hat{p}\psi\rangle-\langle x|\hat{p}\hat{x}\psi\rangle=\ldots$$
Usando le relazioni precedenti
$$\ldots=x \langle x|\hat{p}\psi\rangle+i\hbar\partial_{x}\langle x|\hat{x}\psi\rangle=-i\hbar x\partial_{x}\langle x|\psi\rangle+i\hbar\partial_{x}(x \langle x|\psi\rangle)=i\hbar \langle x|\psi\rangle$$
Ma allora abbiamo scoperto che
$$\boxed{[\hat{x},\hat{p}]=i\hbar\hat{\mathbb{1}}=i\hbar}$$
dove tendenzialmente si tralascia l'operatore identico, per comodità. Un altro esempio di questo è $\alpha|\psi\rangle=\alpha\hat{\mathbb{1}}|\psi\rangle$.

## Onda dipendente dal tempo
Considero un'onda piana ora dipendente dal tempo e la sviluppo
$$\begin{align}
e^{ik(x-vt)}&=e^{\frac{i}{\hbar}px-i \frac{2\pi}{\lambda} vt} \\
&=e^{\frac{i}{\hbar}px-i2\pi\nu t}\\
&=e^{\frac{i}{\hbar}(px- \hbar\nu t)}\\
&=e^{\frac{i}{\hbar}px-Et}=\psi_{t}(x)
\end{align}$$
$$\left( \frac{\hat{p}^{2}}{2m}\psi_{t} \right)(x)=i\hbar\partial_{t}\psi_{t}(x)=E\psi_{t}(x)=- \frac{\hbar^{2}}{2m}\partial_{x}^{2}\psi_{t}(x)=\frac{p^{2}}{2m}\psi_{t}(x)$$
Onda piana particella libera -> si trova l'energia -> si vede che la si ottiene derivando rispetto al tempo ma anche rispetto alla posizione due volte.
$$i\hbar\partial_{t}|\psi_{t}\rangle=\frac{\hat{p}^{2}}{2m}|\psi_{t}\rangle=\hat{H}|\psi_{t}\rangle$$

