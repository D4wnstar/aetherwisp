Il **laplaciano** $\nabla^{2}$ è un [[Operatore]] differenziale definito come la [[divergenza]] del [[gradiente]] di una funzione a valori scalari in uno spazio euclideo. La forma canonica è definita in coordinate cartesiane ed è, presa una funzione $f$ che manda da $\mathbb{R}^{3}$ in $\mathbb{R}$ due volte [[Differenziabilità|differenziabile]],
$$\nabla^{2}f=\nabla\cdot\nabla f=\left(\frac{\partial ^{2}}{\partial x^{2}} + \frac{\partial ^{2}}{\partial y^{2}} + \frac{\partial ^{2}}{\partial z^{2}}\right)f$$
che è la somma di tutte le derivate seconde non miste della funzione $f$. Per uno spazio a dimensione finita arbitraria $N$ si ha
$$\nabla^{2}f=\sum\limits_{i=1}^{N}\frac{\partial ^{2}f}{\partial x_{i}^{2}}$$
### Coordinate polari
Il laplaciano in coordinate polari $(r,\theta)$ è
$$\nabla^{2}f=\frac{\partial ^{2}f}{\partial r^{2}} + \frac{1}{r}\frac{\partial f}{\partial r}+ \frac{1}{r^{2}}\frac{\partial ^{2}f}{\partial \theta^{2}}$$
con $r$ la distanza dal centro e $\theta$ l'angolo di rotazione.
### Coordinate cilindriche
Il laplaciano in coordinate cilindriche $(r,\varphi,z)$ è
$$\nabla^{2}f=\frac{1}{r}\frac{\partial }{\partial r}\left(r \frac{\partial f}{\partial r}\right)+ \frac{1}{r^{2}}\frac{\partial ^{2}f}{\partial \varphi^{2}}+ \frac{\partial ^{2}f}{\partial z^{2}}$$
con $r$ la distanza radiale, $\varphi$ l'angolo azimutale e $z$ l'altezza.
### Coordinate sferiche
Il laplaciano in coordinate polari sferiche $(r,\theta,\phi)$ è
$$\nabla^{2}f=\frac{1}{r^{2}}\frac{\partial }{\partial r}\left(r^{2}\frac{\partial f}{\partial r}\right)+ \frac{1}{r^{2}\sin\theta}\frac{\partial }{\partial \theta}\left(\sin\theta \frac{\partial f}{\partial \theta}\right)+ \frac{1}{r^{2}\sin^{2}\theta}\left(\frac{\partial ^{2}f}{\partial \phi^{2}}\right)$$
con $r$ la distanza radiale, $\theta$ l'angolo azimutale e $\phi$ l'angolo zenitale.