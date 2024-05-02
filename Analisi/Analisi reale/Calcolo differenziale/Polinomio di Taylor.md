---
tags:
  - calcolo-differenziale
aliases:
  - serie di Taylor
---
Il **polinomio di Taylor** $n$-dimensionale in $\mathbb{R}^{n}$ è
$$P_k(x)=\sum\limits_{d=0}^{k} \frac{1}{d!}Q_d^f(x-x^0)=\sum\limits_{d=0}^{k} \frac{1}{d!}\left[\sum\limits_{|\alpha|=d} \frac{|\alpha|!}{\alpha!}D^{\alpha}f(x^{0})(x-x^{0})^\alpha\right]=$$
$$=\sum\limits_{|\alpha|\leq k} \frac{1}{\alpha!}D^{\alpha}f(x^{0})(x-x^{0})^\alpha$$
dove $\alpha$ è il [[Multi-indice]].