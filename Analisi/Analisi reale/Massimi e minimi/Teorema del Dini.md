---
tags:
  - massimi-minimi
---
Il **Teorema del Dini** ci dice che, sotto opportune condizioni, possiamo vedere un [[Insieme di livello]] come il grafico di una funzione.

Sia $F:A\subset\mathbb{R}^{2}\rightarrow\mathbb{R}$ con $A$ aperto, di classe $C^1$ su $A$. Sia $(x_{0},y_{0})\in A$ tale che
$$F(x_0,y_0)=0\;\mbox{e}\;\frac{\partial F}{\partial y}(x_0,y_0)\neq0$$
allora esistono
1. un intorno aperto $U$ di $x_0$
2. un intorno aperto $V$ di $y_0$
3. una funzione $\varphi:U \rightarrow V$ tale che $F(x,\varphi(x))=0\;\forall x\in U$
Inoltre per ogni $(x,y)\in U\times V$ vale $F(x,y)=0 \Leftrightarrow y=\varphi(x)$
$\varphi$ è di classe $C^1$ su $U$ e vale
$$\varphi'(x)=-\frac{\frac{\partial F}{\partial x}(x,\varphi(x))}{\frac{\partial F}{\partial y}(x,\varphi(x))}\quad\forall x\in U$$
