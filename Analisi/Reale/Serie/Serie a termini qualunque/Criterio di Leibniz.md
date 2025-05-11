---
wiki-publish: true
tags:
  - serie
  - serie-qualunque
---
Sia $\{a_{n}\}_{n\in\mathbb{N}}$ una successione di *numeri positivi*, *decresente* e *infinitesima* (ossia $\lim\limits_{n}a_{n}=0$). Allora la seguente [[Serie]] converge
$$\sum\limits_{n=0}^{\infty}(-1)^{k}a_{n}$$
*Dimostrazione.* La successione delle ridotte $\{s_n\}_{n\in\mathbb{N}}$ ha termini $s_{n}=\sum\limits_{k=0}^{n}(-1)^{k}a_{k}$. Consideriamo le sottosuccessioni $\{s_{2n}\}_{n\in\mathbb{N}}$ e $\{s_{2n+1}\}_{n\in\mathbb{N}}$ pari e dispari. Valgono
$$s_{2(n+1)}=s_{2n+2}=s_{2n}-a_{2n+1}+a_{2n+2}\leq s_{2n}$$
perche $-a_{2n+1}+a_{2n+2}\leq0$. Inoltre
$$s_{2(n+1)+1}=s_{2n+3}=s_{2n+1}+a_{2n+2}-a_{2n+3}\leq s_{2n+1}$$
perche $a_{2n+2}-a_{2n+3}\geq0$.
Quindi i termini pari sono decrescenti, mentre quelli dispari sono crescenti. Vale inoltre
$$s_{1}\leq s_{2n+1}\leq s_{2n}\leq s_{0}$$
Abbiamo quindi che esistono i seguenti limiti in $\mathbb{R}$
$$D:=\lim\limits_{n}s_{2n+1}\quad P:=\lim\limits_{n}s_{2n}$$
dal quale sicuramente $D\leq P \Rightarrow D-P=\lim\limits_{n}s_{2n+1}-s_{2n}=\lim\limits_{n}(-1)^{2n+1}a_{2n+1}=0$
Quindi $D=P$ e vale $\lim\limits_{n}s_{n}=D=P\in\mathbb{R}$ ossia la serie converge.