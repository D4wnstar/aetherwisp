---
tags:
  - serie
  - serie-nonneg-pos
---
# Normale
Sia $\sum\limits_{n=0}^{\infty}a_n$ una [[Serie a termini non negativi o positivi|serie a termini positivi]] tale che esiste $q\in\;]0,1[$ tale che
$\frac{a_{n+1}}{a_{n}}\leq q, \quad\forall n\in \mathbb{N}$
Allora la serie converge.
*Dimostrazione:* Dall'ipotesi $a_{n+1}\leq a_{n}q$ quindi anche $a_{1}\leq a_0q$. Continuando si ha $a_{2}\leq qa_{1}\leq q^2q_{0}$. Per induzione si ha $a_{n}\leq q^{n}a_0$. Da questo si ha $\sum\limits_{n=0}^{k}a_{n}\leq \sum\limits_{n=0}^{k}q^{n}a_{0}=a_{0}\sum\limits_{n=0}^{k}q^{n}$, che è una serie geometrica (moltiplicata per $a_0$). Con $q<1$ essa converge nel limite $n\rightarrow \infty$ quindi converge anche la prima.
# Asinotico
Sia $\sum\limits_{n=0}^{\infty}a_{0}$ una serie a termini positivi tale che esiste il seguente limite:
$\lim\limits_{n} \frac{a_{n+1}}{a_{n}}=l \quad l\in[0,+\infty]$
Allora si ha
- Se $l\in [0,1[$ la serie converge
- Se $l\in]1,+\infty[$ la serie diverge
- Se $l=1$ il criterio non dà informazioni
*Dimostrazione.* Se vale $l<1$ allora possiamo trovare un reale $q\in\;]l,1[$ per cui, usando la definizione di limite, vale
$\exists\bar{n}\in\mathbb{N}\;|\;\forall n\geq\bar{n}\;\; \frac{a_{n+1}}{a_{n}}<q$
quindi la serie resto da $\bar{n}$ soddisfa il criterio del rapporto ed è convergente.
Se invece $l>1$ possiamo trovare $q\in]1,l[$ tale che
$\exists\bar{n}\in\mathbb{N}\;|\;\forall n\geq\bar{n}\;\; \frac{a_{n+1}}{a_{n}}>q>1$
Troviamo che $a_{n+1}>a_{n}\;\forall n>\bar{n}$ quindi la serie resto è crescente e diverge.