---
tags:
  - integrali
  - integrali-fisica
aliases:
  - path integral
---
## Prima specie
Siano $\gamma:[a,b]\rightarrow\mathbb{R}^N$ una [[Curva]] regolare e $f:A\subset\mathbb{R}^N\rightarrow\mathbb{R}$ una funzione continua con $A$ aperto. Supponiamo che il sostegno di $\gamma$ sia contenuto in $A$, allora l'**integrale di prima specie di $f$ lungo $\gamma$** risulta

$\int_{\gamma}fds:=\int_a^bf(\gamma(t))||\gamma'(t)||dt$

Se $f(t)=1$ allora si ha la misura (cioè la lunghezza) di $\gamma$. Questo integrale è *invariante* per curve equivalenti. Per provarlo, basti trovare un $C^1$-diffeomorfismo $\varphi$ tale che $\eta(t)=\varphi(\gamma(t))$, con $\gamma(t)$ e $\eta(t)$ le due curve e calcolare l'integrale.
## Seconda specie
Siano $\gamma:[a,b]\rightarrow\mathbb{R}^N$ una curva regolare e $F:A\subset\mathbb{R}^N\rightarrow\mathbb{R}^N$ una funzione continua con $A$ aperto. Supponiamo che il sostegno di $\gamma$ sia contenuto in $A$, allora l'**integrale di seconda specie di $F$ lungo $\gamma$** risulta

$\int_{\gamma}F\cdot\hat{\tau}ds:=\int_{a}^{b}\langle F(\gamma(t)),\gamma'(t)\rangle dt$

dove $\langle a, b \rangle$ è il prodotto scalare. Questo integrale è invariante se le due curve hanno la stessa orientazione. Altrimenti l'integrale inverte segno.