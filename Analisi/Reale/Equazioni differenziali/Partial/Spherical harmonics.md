---
wiki-publish: true
---
The **spherical harmonics** $Y_{l}^{m}(\theta,\phi)$ are the angular part of the solution to [[Laplace's equation]] in [[Spherical coordinates|spherical coordinates]]. They are
$$Y_{l}^{m}(\theta,\phi)=\sqrt{\frac{2l+1}{4\pi} \frac{(l-m)!}{(l+m)!}}e^{im\phi}P_{l}^{m}(\cos\theta)$$
where $\theta\in[0,\pi]$ is the polar angle, $\phi\in[0,2\pi[$ is the azimuthal angle and $P_{l}^{m}(\cos\theta)$ is the [[Polinomi di Legendre#Polinomi associati di Legendre|associated Legendre polynomial]].

The normalization is chosen such that the spherical harmonics are pairwise [[Orthogonality|orthogonal]], that is
$$\int_{0}^{2\pi}\int_{0}^{\pi}Y_{l}^{m}(\theta,\phi)(Y_{l'}^{m'})^{*}(\theta,\phi)\sin\theta d\theta d\phi=\delta_{mm'}\delta_{ll'}$$
with $^{*}$ being the complex conjugate and $\delta$ the [[Kronecker delta]].

The first spherical harmonics are
$$\begin{align}
Y_{0}^{0}&=\sqrt{\frac{1}{4\pi}} \\
Y_{1}^{0}&=\sqrt{\frac{3}{4\pi}}\cos\theta,\quad Y_{1}^{\pm1}=\mp\sqrt{\frac{3}{8\pi}}\sin\theta e^{\pm i\phi} \\
Y_{2}^{0}&=\sqrt{\frac{5}{16\pi}}(3\cos^{2}\theta-1),\quad Y_{2}^{\pm1}=\mp\sqrt{\frac{15}{8\pi}}\sin\theta\cos\theta e^{\pm i\phi},\quad Y_{2}^{\pm2}=\sqrt{\frac{15}{32\pi}}\sin^{2}\theta e^{\pm2i\phi}
\end{align}$$
### Symmetry
In quantum mechanics, a rather useful property of the harmonics is the following: the square modulus over all $m$ for a given $l$
$$\sum_{m=-l}^{l} \lvert Y_{l}^{m}(\theta,\phi) \rvert ^{2}$$
is spherically symmetrical. This is quite useful because any quantity whose shape is given by the harmonics is automatically also spherically symmetrical. For instance, the [[Electric charge|charge]] distribution in the [[hydrogen atom]].

Another useful property is that the harmonics have alternating [[Parity|parity]] $(-1)^{l}$. This means that the harmonic inherits the evenness of $l$:
- if $l$ is even, the harmonic is even, $Y_{l}^{m}(\pi-\theta,\phi+\pi)=Y_{l}^{m}(\theta,\phi)$
- if $l$ is odd, the harmonic is odd, $Y_{l}^{m}(\pi-\theta,\phi+\pi)=-Y_{l}^{m}(\theta,\phi)$
