Le **armoniche sferiche** $Y_{l}^{m}(\theta,\phi)$ sono la parte angolare della soluzione dell'[[Laplace's equation]] in [[Spherical coordinates|coordinate sferiche]] e valgono
$$Y_{l}^{m}(\theta,\phi)=\sqrt{\frac{2l+1}{4\pi} \frac{(l-m)!}{(l+m)!}}e^{im\phi}P_{l}^{m}(\cos\theta)$$
dove $\theta$ è l'angolo polare con $\theta\in[0,\pi]$ e $\phi$ è l'angolo azimutale con $\phi\in[0,2\pi[$. $P_{l}^{m}(\cos\theta)$ è il $lm$-esimo [[Polinomi di Legendre#Polinomi associati di Legendre|polinomio di Legendre associato]].

La normalizzazione è scelta a modo che le armoniche sferiche siano a due a due [[Ortogonalità|ortogonali]], ossia
$$\int_{0}^{2\pi}\int_{0}^{\pi}Y_{l}^{m}(\theta,\phi)(Y_{l'}^{m'})^{*}(\theta,\phi)\sin\theta d\theta d\phi=\delta_{mm'}\delta_{ll'}$$
con $*$ il coniugato complesso e $\delta$ la [[delta di Kronecker]].

Le prime armoniche sferiche sono
$$\begin{align}
Y_{0}^{0}&=\sqrt{\frac{1}{4\pi}} \\
Y_{1}^{0}&=\sqrt{\frac{3}{4\pi}}\cos\theta \\
Y_{1}^{\pm1}&=\mp\sqrt{\frac{3}{8\pi}}\sin\theta e^{\pm i\phi} \\
Y_{2}^{0}&=\sqrt{\frac{5}{16\pi}}(3\cos^{2}\theta-1) \\
Y_{2}^{\pm1}&=\mp\sqrt{\frac{15}{8\pi}}\sin\theta\cos\theta e^{\pm i\phi} \\
Y_{2}^{\pm2}&=\sqrt{\frac{15}{32\pi}}\sin^{2}\theta e^{\pm2i\phi}
\end{align}$$