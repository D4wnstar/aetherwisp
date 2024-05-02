Un sistema di vettori ortonormali $\{e_{i}\}$ si dice **completo** in uno [[Spazio di Hilbert]] $H$ se per ogni $v\in H$ la [[Serie di Fourier]] di $v$ rispetto a tale sistema converge a $v$ stesso nella norma di $H$, ossia $||\overline{v}_{n}-v|| \rightarrow 0$, e si scrive
$$v=\sum\limits_{i=1}^{\infty}a_{i}e_{i}\quad;\quad a_{i}=(e_{i},x)$$
Vale inoltre l'[[Identità di Parseval]].

I sistemi ortonormali completi sono la generalizzazione a dimensione infinita del concetto di [[base]].

L'insieme
$$\left[\frac{1}{\sqrt{2L}},\; \frac{1}{\sqrt{L}} \cos\left(\frac{n\pi}{L}x\right),\; \frac{1}{\sqrt{L}}\sin\left(\frac{n\pi}{L}x\right)\right]\quad\forall n\in\mathbb{N}$$
è un sistema ortonormale completo.
### Proprietà
Le seguenti proprietà sono equivalenti, ossia se ne vale una, valgono anche tutte le altre:
1. Il sistema ortonormale $\{e_{i}\}$ in uno spazio di Hilbert $H$ è completo.
2. L'insieme delle combinazioni lineari finite $$\sum\limits_{i=1}^{n}a_{i}e_{i}$$è denso in $H$ al variare di $n$ e dei coefficienti $a_{i}$, ossia ogni vettore $v\in H$ può essere approssimato in norma con precisione arbitraria da una combinazione lineare degli $\{e_{i}\}$. Tra queste, la migliore approssimazione è quella data dai coefficienti di Fourier.
3. Vale l'identità di Parseval per ogni $v\in H$
4. L'unico vettore ortogonale a tutti gli $e_{i}$ è il vettore nullo
