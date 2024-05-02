---
tags:
  - serie
  - serie-qualunque
---
Sia $\sum\limits_{n=0}^{\infty}a_{n}$ una [[Serie]] con successione delle ridotte $\{s_n\}_{n\in\mathbb{N}}$ limitata. Considero una successione $\{q_n\}_{n\in\mathbb{N}}$ di reali *non negativi*, *decrescente*, *infinitesima*. Allora la seguente serie converge
$$\sum\limits_{n=0}^{\infty}q_{n}a_{n}$$
*Dimostrazione.* Essendo $\{s_n\}_{n\in\mathbb{N}}$ limitata, possiamo trovare $M>0$ tale che $|s_n|<M\;\forall n\in\mathbb{N}$. Gli elementi della successione $\{\sigma_n\}_{n\in\mathbb{N}}$ delle ridotte nella serie $\sum\limits_{n=0}^{\infty}q_{n}a_{n}$ può essere riscritta nel seguente modo:
$$\begin{align}\sigma_{n}=&\;q_{o}a_{0}+q_{1}a_{1}+\cdots+q_{n}a_{n}\\
=&\;q_{0}s_{0}+q_{1}(s_{1}-s_{0})+\cdots+q_{k}(s_{k}-s_{k-1})+\cdots+q_{n}(s_{n}-s_{n-1})\\
=&\;s_{0}(q_{0}-q_{1})+s_{1}(q_{1}-q_{2})+\cdots+s_{k}(q_{k}-q_{k+1+})+\cdots+s_{n-1}(q_{n-1}-q_{n})+s_{n}q_{n})
\end{align}$$
Quindi avremo
$$\sigma_{n}=\sum\limits_{k=0}^{n-1}s_{k}(q_{k}-q_{k+1})+s_{n}q_{n}$$
dove $s_{n}q_{n}$ va a 0 per ipotesi. Per mostrare che le $\sigma_{n}$ convergano ci rimane da mostrare che anche $\sum\limits_{n=0}^{\infty}s_{n}(q_{n}-q_{n+1})$ converga. Usiamo l'assoluta convergenza. Vale
$$|s_{k}(q_{k}-q_{k+q})|\leq M(q_{k}-q_{k+1})$$
$$\lim\limits_{n}\sum\limits_{k=0}^{n}M(q_{k}-q_{k+1})=\lim\limits_{n}M(q_{0}-q_{n+1})=Mq_{0}$$
$$\sum\limits_{n=0}^{\infty}|s_{n}(q_{n}-q_{n+1})|\leq M\sum\limits_{n=0}^{\infty}(q_{n}-q_{n+1})=Mq_{0}$$
quindi converge.