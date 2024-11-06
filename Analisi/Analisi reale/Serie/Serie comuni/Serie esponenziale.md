La **serie esponenziale** è la [[serie]] che definisce la funzione esponenziale $e^{x}$:
$$\sum\limits_{n=0}^{\infty} \frac{x^n}{n!}=e^x$$
Converge con $x=1$. I primi termini sono
$$e^{x}=1+ x+ \frac{x^{2}}{2}+ \frac{x^{3}}{6}+\ldots$$
### Esponenziale di un operatore
Questa definizione può anche essere usata per estendere l'esponenziale a modo di fare l'esponenziale di una matrice o [[operatore]]. Preso un operatore lineare $\hat{A}$, il suo esponenziale è
$$e^{\hat{A}}=\sum_{n=0}^{\infty} \frac{\hat{A}^{n}}{n!}$$
che è calcolabile ricordando che la potenza di un operatore non è altro che la ripetuta applicazione di quell'operatore:
$$\hat{A}^{2}=\hat{A}\hat{A},\quad \hat{A}^{n}=\underbrace{ \hat{A}\hat{A}\ldots\hat{A} }_{ n\text{ volte} }$$
Allora i primi termini sono
$$e^{\hat{A}}=1+ \hat{A}+ \frac{\hat{A}\hat{A}}{2}+ \frac{\hat{A}\hat{A}\hat{A}}{6}+\ldots$$
Come per tutti gli operatori, l'esponenziale di un operatore (esso stesso un operatore) ha solo senso quando applicato a qualcosa.