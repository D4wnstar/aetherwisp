---
tags:
  - serie
  - serie-nonneg-pos
---
Sia $\sum\limits_{n=1}^{\infty}a_{n}$ una [[Serie a termini non negativi o positivi|serie a termini positivi]] con $\{a_{n}\}_{n\in\mathbb{N}}$ successione decrescente. Allora ha lo stesso carattere della **serie condensata** $\sum\limits_{n=0}^{\infty}a_{2^{n}}2^{n}$
*Dimostrazione.* Consideriamo le ridotte delle due
$s_{n}=\sum\limits_{k=1}^{n}a_{k}\quad$e$\quad t_{m}=\sum\limits_{h=0}^{m}a_{2^{h}}2^{h}$
e osserviamo che, essendo $\{a_{n}\}_{n\in\mathbb{N}}$ decrescente,
$a_{1}\geq \frac{1}{2}a_{1}$
$a_{2}\geq \frac{1}{2}2a_{2}$
$a_{3}+a_{4}\geq2a_{4}=\frac{1}{2}4a_{4}$
$a_5+a_6+a_7+a_{8}\geq4a_{8}=\frac{1}{2}8a_{8}$
In generale si ha, per ogni $h\in\mathbb{N}$
$a_{2^{h-1}+1}+a_{2^{h-1}+2}+\cdots+a_{2^{h}-1}+a_{2^{h}}\geq \frac{1}{2}2^{h}a_{2^{h}}\quad\quad(1)$
Quindi abbiamo $s_{2^{m}}\geq \frac{1}{2}t_{m}$ per ogni $m\in\mathbb{N}$.
Similmente
$a_{1}\leq a_{1}$
$a_{2}+a_{3}\leq 2a_{2}$
$a_4+a_5+a_6+a_{7}\leq4a_{4}$
In generale si ha, per ogni $h\in\mathbb{N}$
$a_{2^h}+a_{2^{h}+1}+\cdots+a_{2^{h+1}-2}+a_{2^{h+1}-1}\leq2^{h}a_{2^{h}}\quad\quad(2)$
Quindi abbiamo $s_{2^{m+1}-1}\leq t_{m}$ per ogni $m\in\mathbb{N}$.
Usando il teorema del confronto fra successioni (da non confondersi con il [[criterio del confronto]]), se $\sum\limits_{n=0}^{\infty}a_{n}$ converge, converge anche al condensata grazie a (1), mentre se diverge, diverge anche la condenstata usando (2). Vale anche il contrario, sempre usando (1) e (2).