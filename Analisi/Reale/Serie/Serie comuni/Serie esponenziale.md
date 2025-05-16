---
wiki-publish: true
---
La **serie esponenziale** è la [[Serie]] che definisce la funzione esponenziale $e^{x}$:
$$\sum\limits_{n=0}^{\infty} \frac{x^n}{n!}=e^x$$
Converge solo per $x=1$. I primi termini sono
$$e^{x}=1+ x+ \frac{x^{2}}{2}+ \frac{x^{3}}{6}+\ldots$$
### Esponenziale di una matrice o operatore
Questa definizione può anche essere usata per estendere l'esponenziale a modo di fare l'esponenziale di una matrice o [[operatore]]. Preso una matrice o operatore lineare $A$, il suo esponenziale è
$$e^{A}=\sum_{n=0}^{\infty} \frac{A^{n}}{n!}$$
che è calcolabile ricordando che la potenza di un operatore non è altro che la ripetuta applicazione di quell'operatore:
$$A^{2}=AA,\quad A^{n}=\underbrace{ AA\ldots A }_{ n\text{ volte} }$$
Allora i primi termini sono
$$e^{A}=1+ A+ \frac{AA}{2}+ \frac{AAA}{6}+\ldots$$
Come per tutti gli operatori, l'esponenziale di un operatore (esso stesso un operatore) ha solo senso quando applicato a qualcosa.