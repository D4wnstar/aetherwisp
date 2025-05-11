---
wiki-publish: true
tags:
  - massimi-minimi
---
Siano $F:A\subseteq \mathbb{R}^{N}\rightarrow\mathbb{R}^{M}$ con $1\leq M\leq N$ e $f:A\subseteq\mathbb{R}^{N}\rightarrow\mathbb{R}^{M}$. Definiamo **insieme vincolato** l'insieme $C=\{P\in A\;|\;F(P)=0\}\subseteq A$, ossia l'insieme di tutti i punti che annullano la funzione $F$. Prendiamo un punto $P_{0}\in C$. Supponiamo che $F$ sia di classe $C^1$ su $A$ con [[Jacobian|Jacobiana]] $J_{F}(P_{0})$ di rango massimo e che $f$ sia [[Differential|differenziabile]] in $P_{0}$.

Se $P_{0}$ è punto di estremo locale per $f$ relativo al vincolo $C$, allora esistono $\lambda_{1},\cdots,\lambda_{M}$ coefficienti reali detti **moltiplicatori di Lagrange** tali che
$$\nabla f(P_{0})=\lambda_{1}\nabla F_{1}(P_{0})+\cdots+\lambda_{M}F_{M}(P_{0})$$
dove $F_{k}$ sono le componenti di $F$.

Nel caso più semplice $M=1$, si ha
$$\nabla f(P_{0})=\lambda \nabla F(P_{0})$$
### Dimostrazione
Consideriamo senza perdere di generalità il caso in cui $P_{0}$ sia minimo locale per $f$ relativo al vincolo $C$. Riordiniamo le variabili di $\mathbb{R}^{N}$ in modo da individuare le coordinate $P=(x,y)\in\mathbb{R}^{N-M}\times\mathbb{R}^{N}$ tali che la sottomatrice $\frac{\partial F}{\partial y}(x_{0},y_{0})$ della matrice Jacobiana sia invertibile. Usando il [[Teorema del Dini]] troviamo che l'insieme
$$C\;\cap(U\times V)=\{(x,y)\in\mathbb{R}^{N- M}\times\mathbb{R}^{M}\;|\;y=\varphi(x),x\in U\}$$
contiene il punto $P_{0}=(x_{0},y_{0})=(x_{0},\varphi(x_{0}))$. Poichè $P_{0}$ è minimo locale per $f$ relativo a $C$, esiste un insieme aperto $W=U_{1}\times V_{1}\subset U\times V$ tale che $f(P_{0})\leq f(P)$ per ogni $P\in W\cap C$. Quindi, per ogni $x\in U_{1}$, abbiamo $P=(x,\varphi(x))\in W\cap C$, quindi $f(P_{0})=f(x_{0},\varphi(x_{0}))\leq f(x,\varphi(x))\;\forall x\in U_{1}$.
In pratica abbiamo trovato una funzione $f_{1}:U_{1}\subset \mathbb{R}^{N-M}\rightarrow\mathbb{R}$ definita come $f_{1}(x)=f(x,\varphi(x))$, che ha un punto di minimo in $x_{0}$. $f_{1}$ eredita la differenziabilità in $x_{0}$ di $f$ e vale
$$0=\nabla f_{1}(x_{0})=\underbrace{\nabla f(x_{0},\varphi(x_{0}))}\limits_{=v_{0}\in\mathbb{R}^{N}}\cdot\underbrace{\left(\begin{array}{cc}I_{N-M}\\ J_{\varphi}(x_{0})\end{array}\right)}\limits_{=A}$$
trovato usando la derivata della composta su $f(\varphi(x))$. $I_{N-M}$ è la matrice identica di ordine $N-M$, quindi $v_{0}$ deve essere ortogonale ai $N-M$ vettori colonna linearmente indipendenti della matrice $A$.
Introduciamo $W$ come sottospazio vettoriale generato dalle colonne di $A$ e notiamo che esso ha dimensione $N-M$. Da quanto appena visto, abbiamo $\nabla f(P_{0})\in W^{\perp}$.
Mostriamo che vale lo stesso anche per i vettori $\nabla F_{k}(P_{0})$ per ogni $k=1,\ldots,M$. Per ipotesi sono linearmente indipendenti, in quanto la Jacobiana di $F$ ha rango massimo. Abbiamo che $F(x,\varphi(x))=0$ per ogni $x\in U_{1}$ e in particolare per $k=1,\ldots,M$,
$$F_{k}(x,\varphi(x))=0\;\forall x\in U_{1}$$
quindi definendo $\tilde{f}_{k}:U_{1}\rightarrow\mathbb{R}$ come $\tilde{f}_{k}(x)=F_{k}(x,\varphi(x))$ vale $\tilde{f}_{k}\equiv0$ e troviamo
$$0=\nabla\tilde{f}_{k}(x)=\nabla F_{k}(x,\varphi(x))\cdot\left(\begin{array}{cc}I_{N-M}\\ J_{\varphi}(x)\end{array}\right)\quad\forall x\in U_{1}$$
In particolare in $x_{0}$ si ha
$$0=\nabla\tilde{f}_{k}(x_{0})=\nabla F_{k}(x_{0},\varphi(x_{0}))\cdot\underbrace{\left(\begin{array}{cc}I_{N-M}\\ J_{\varphi}(x_{0})\end{array}\right)}\limits_{=A}$$
quindi $\nabla F_{k}(P_{0})\in W^{\perp}\;\forall k=1,\ldots,M$. Sapendo che sia $\nabla f(P_{0})$ e $\nabla F_{k}(P_{0})$ appartengono allo stesso spazio vettoriale e che i $\nabla F_{k}$ formano una base di $W^{\perp}$, possiamo esprimere il primo come combinazione lineare degli altri, da cui la tesi.