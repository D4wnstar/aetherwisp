---
wiki-publish: true
tags:
  - serie
  - serie-nonneg-pos
---
# Normale
Sia $\sum\limits_{n=0}^{\infty}a_n$ una [[Serie a termini non negativi o positivi|serie a termini non negativi]] tale che esiste $q ∈ ]0, 1[$ con la seguente proprietà: $\sqrt[n]{a_{n}}\leq q\;\forall n\in\mathbb{N}$.
Allora la serie è convergente.
*Dimostrazione.* Dall'ipotesi si ha che $a_{n}\leq q^{n}\;\forall n\in\mathbb{N}$ quindi per $q\in]0,1[$ la serie converge nel limite.
# Asintotico
Sia $\sum\limits_{n=0}^{\infty}a_n$ una serie a termini non negativi tale che esiste il limite $\lim\limits_{n}\sqrt[n]{a_{n}}=l,\quad l\in[0,+\infty[$
- Se $l\in[0,1[$ allora la serie converge
- Se $l\in]1,+\infty[$ la serie diverge
- Se $l=1$ il criterio non ci dà informazioni
*Dimostrazione.* Se vale $l<1$ allora possiamo trovare un reale $q\in]l,1[$ per cui, usando la definizione di limite, vale
$\exists\bar{n}\in\mathbb{N}\;|\;\forall n\geq\bar{n}\quad\sqrt[n]{a_{n}}<q$
il che soddisfa il criterio della radice normale, quindi converge.