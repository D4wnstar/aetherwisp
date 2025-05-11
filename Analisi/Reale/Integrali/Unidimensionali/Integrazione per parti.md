---
wiki-publish: true
---
L'**integrazione per parti** è una tecnica di integrazione che segue dalla regola di derivazione dei prodotti
$$\frac{d}{dx}(fg)=f \frac{dg}{dx}+ \frac{df}{dx}g$$
da cui si trova, integrando da $a$ a $b$ entrambi i membri
$$\int_{a}^{b}f \frac{dg}{dx}dx=fg|_{a}^{b}-\int_{a}^{b} \frac{df}{dx}gdx$$
È utile per "spostare" la derivata da un termine dell'integrazione all'altro.
### Forma vettoriale
Questo metodo è estensibile anche al calcolo di quantità vettoriali. Per esempio, consideriamo il prodotto
$$\nabla\cdot f\mathbf{A}=f(\nabla\cdot\mathbf{A})+\mathbf{A}\cdot(\nabla f)$$
dove $f$ è una funzione a valori reali e $\mathbf{A}$ è un [[Vector field]]. Allora integrando su un volume abbiamo
$$\int \nabla\cdot(f\mathbf{A})d\tau=\int f(\nabla\cdot\mathbf{A})d\tau+\int\mathbf{A}\cdot(\nabla f)d\tau=\oint f\mathbf{A}\cdot d\mathbf{a}$$
dove abbiamo usato il [[Divergence theorem]]. Allora
$$\int_{V}f(\nabla\cdot\mathbf{A})=-\int_{V}\mathbf{A}\cdot(\nabla f)d\tau+\oint_{S}f\mathbf{A}\cdot d\mathbf{a}$$
dove $V$ è un volume e $S$ è la [[Surface]] di frontiera di quel volume. In modo analogo si trovano anche
$$\int_{S}f(\nabla\times\mathbf{A})\cdot d\mathbf{a}=\int_{S}[\mathbf{A}\times(\nabla f)]\cdot d\mathbf{a}+\oint_{\gamma}f\mathbf{A}\cdot d\mathbf{r}$$
dove $\gamma$ è la [[Curve]] di frontiera della superficie $S$, e anche
$$\int_{V}\mathbf{B}\cdot(\nabla\times\mathbf{A})d\tau=\int_{V}\mathbf{A}\cdot(\nabla\times\mathbf{B})d\tau+\oint_{S}(\mathbf{A}\times\mathbf{B})\cdot d\mathbf{a}$$
