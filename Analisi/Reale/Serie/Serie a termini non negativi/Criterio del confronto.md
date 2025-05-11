---
wiki-publish: true
tags:
  - serie
  - serie-nonneg-pos
---
# Normale
Siano $\sum\limits_{n=0}^{\infty}a_n$ e $\sum\limits_{n=0}^{\infty}b_n$ due [[Serie a termini non negativi o positivi|serie a termini non negativi]]. Se $a_{n}\leq b_{n}\;\forall n\in \mathbb{N}$ allora
- se $\sum\limits_{n=0}^{\infty}b_{n}$ converge, allora anche $\sum\limits_{n=0}^{\infty}a_n$ converge
- se $\sum\limits_{n=0}^{\infty}a_{n}$ diverge, allora anche $\sum\limits_{n=0}^{\infty}b_n$ diverge
# Asintotico
Siano $\sum\limits_{n=0}^{\infty}a_n$ e $\sum\limits_{n=0}^{\infty}b_n$ due [[Serie a termini non negativi o positivi|serie a termini positivi]]. Calcoliamo $l:=\lim\limits_{n} \frac{b_{n}}{a_{n}}$
- Se $l\in]0,+\infty[$ le due serie hanno lo stesso carattere
- Se $l=0$ e $\sum\limits_{n=0}^{\infty}b_{n}$ converge, allora anche $\sum\limits_{n=0}^{\infty}a_n$ converge
- Se $l=+\infty$ e $\sum\limits_{n=0}^{\infty}a_n$ diverge, allora anche $\sum\limits_{n=0}^{\infty}b_n$ diverge
*Dimostrazione.* Proviamo il primo punto. Basta usare la definizione del limite per l:
$$\forall \varepsilon>0,\;\exists\bar{n}\in \mathbb{N}\;|\;\forall n \geq\bar{n}\;\; \left| \frac{b_{n}}{a_{n}}-l\right|<\varepsilon$$
Scegliendo $\varepsilon=\frac{l}{2}$ si trova
$$\exists\bar{n}\in \mathbb{N}|\forall n \geq\bar{n}\;\; \left| \frac{b_{n}}{a_{n}}-l\right|<\frac{l}{2}$$
Ossia
$$\exists\bar{n}\in \mathbb{N}|\forall n \geq\bar{n}\;\; \frac{1}{2}l< \frac{b_{n}}{a_{n}}<\frac{3}{2}l$$
Sapendo che $a_n>0\;\forall n\in \mathbb{N}$ si ha
$$\frac{1}{2}a_{n}l< b_{n}<\frac{3}{2}a_{n}l \quad\forall n\geq\bar{n}$$
Dunque usiamo il criterio del confronto normale.
Per il secondo punto uso la stessa tecnica, ma con $\varepsilon=1$:
$$\lim\limits_{n} \frac{b_{n}}{a_{n}}=0 \Rightarrow \exists\bar{n}\in \mathbb{N}\;|\;\forall n \geq\bar{n}\;\; \frac{b_{n}}{a_{n}}<1$$
da cui $b_{n}<a_{n}\;\forall n$ quindi se $a_{n}$ converge lo fa anche $b_n$.
Per il terzo punto usiamo di nuovo la definizione di limite:
$$\lim\limits_{n} \frac{b_{n}}{a_{n}}=+\infty \Rightarrow \forall M>0\;|\;\forall n \geq\bar{n}\;\; \frac{b_{n}}{a_{n}}>M$$
Prendendo $M=1$ segue che $b_{n}>a_{n}\;\forall n$ quindi se diverge $b_n$ lo fa anche $a_n$.