Considero un'onda piana $\psi_{p}(x)=A_{p}e^{\frac{i}{\hbar}px}$ e la descrivo come [[prodotto scalare]]
$$\psi_{p}(x)=\langle x|\psi_{p}\rangle=\langle x|p\rangle$$
abbreviando $\psi_{p}$ a $p$. Allora trovo il prodotto scalare tra due onde
$$\begin{align}
\langle p_{1}|p_{2}\rangle&=\int_{-\infty}^{\infty}\langle p_{1}|x\rangle \langle x|p_{2}\rangle dx=\int_{-\infty}^{\infty}dx A^\ast_{p_{1}}e^{- \frac{i}{\hbar}p_{1}x}A_{p_{2}}e^{- \frac{i}{\hbar}p_{2}x}\\
	&=A^{\ast}_{p_{1}}A_{p_{2}}2\pi\hbar \int_{-\infty}^{\infty}dx \frac{e^{- \frac{i}{\hbar}(p_{1}-p_{2})x}}{2\pi\hbar} =A^{\ast}_{p_{1}}A_{p_{2}}2\pi\hbar \delta(p_{1}-p_{2})
\end{align}$$
Allora possiamo esprimere l'onda *piana* come
$$\psi_{p}=\frac{e^{\frac{i}{\hbar}px}}{\sqrt{2\pi\hbar}}=\langle x|p\rangle$$
ossia come il prodotto scalare tra un autoket di posizione $x$ e un autoket di momento $p$, cioè la rappresentazione di $p$ su $x$. Ma prendendo il coniugato posso trovare anche la forma simmetrica $\langle p|x\rangle$ che ci dà la rappresentazione di $x$ su $p$, che è del tutto equivalente in termini fisici. Matematicamente, non è altro che una [[trasformata di Fourier]] da $x$ a $p$ o viceversa:
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