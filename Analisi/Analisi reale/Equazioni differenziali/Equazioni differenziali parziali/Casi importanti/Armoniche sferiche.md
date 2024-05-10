Le **armoniche sferiche** $Y_{l}^{m}(\theta,\phi)$ sono la parte angolare della soluzione dell'[[equazione di Laplace]] in coordinate sferiche e valgono
$$Y_{l}^{m}(\theta,\phi)=\sqrt{\frac{2l+1}{4\pi} \frac{(l-m)!}{(l+m)!}}e^{im\phi}P_{l}^{m}(\cos\theta)$$
dove $\theta$ è l'angolo polare con $\theta\in[0,\pi]$ e $\phi$ è l'angolo azimutale con $\phi\in[0,2\pi[$. $P_{l}^{m}(\cos\theta)$ è il $lm$-esimo [[Polinomi di Legendre#Polinomi associati di Legendre|polinomio di Legendre associato]].

La normalizzazione è scelta a modo che le armoniche sferiche siano a due a due [[Ortogonalità|ortogonali]], ossia
$$\int_{0}^{2\pi}\int_{0}^{\pi}Y_{l}^{m}(\theta,\phi)(Y_{l'}^{m'})^{*}(\theta,\phi)\sin\theta d\theta d\phi=\delta_{mm'}\delta_{ll'}$$
con $*$ il coniugato complesso e $\delta$ la [[delta di Kronecker]].