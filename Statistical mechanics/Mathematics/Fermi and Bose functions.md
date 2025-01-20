---
aliases:
  - Fermi functions
  - Bose functions
---
The **Fermi and Bose functions** or **complete Fermi and Bose integrals** are classes of functions that make quantum [[ensemble|ensembles]] easier to manage mathematically. The Fermi functions $f_{k}$ and Bose functions $g_{k}$ are defined as
$$f_{k}(z)\equiv \sum_{l=1}^{\infty}(-1)^{l+1} \frac{z^{l}}{l^{k}},\qquad g_{k}(z)\equiv \sum_{l=1}^{\infty} \frac{z^{l}}{l^{k}}$$
where $k$ is a real number. Both of these are specific forms of the [[polylogarithm]]:
$$f_{k}(z)=-\text{Li}_{k+1}(-e^{z}),\qquad G_{k}(z)=\text{Li}_{k+1}(e^{z})$$
They obey the recurrence relations
$$z \frac{d}{dz}f_{k}(z)=f_{k-1}(z),\qquad z \frac{d}{dz}g_{k}(z)=g_{k-1}(z)$$
They have an integral representation through the [[Gamma function]]:
$$\left.\begin{align}
f_{k}(z) \\
g_{k}(z)
\end{align}\ \right\}= \frac{1}{\Gamma(k)}\int_{0}^{\infty} \frac{x^{k-1}}{z^{-1}e^{x}\pm 1}dx$$
where $+$ is for Fermi functions and $-$ for Bose functions. In a physical context, $z$ is the [[fugacity]] and the integration variable is typically momentum. The [[Fermi-Dirac distribution|Fermi-Dirac]] and [[Bose-Einstein distribution]] appear in the integral.
### Origin
These functions are convenience functions defined from integrals that occur in [[quantum statistical mechanics]] when dealing with [[Fermion|fermions]] and [[Boson|bosons]]. They appear, for instance, in the [[equation of state]] of a quantum [[ideal gas]] in both the [[quantum microcanonical ensemble]] and the [[quantum grand canonical ensemble]] derivations. For example, in the latter, they come up when taking the derivative of the [[Partition function|grand canonical partition function]] $\mathcal{Z}$ in the [[thermodynamic limit]]:
$$\ln \mathcal{Z}=\frac{4\pi V}{h^{3}}\int_{0}^{\infty}p^{2}\ln(1+ze^{-\beta \varepsilon_{p}})dp$$
This integral can't be solved analytically, but we can expand $\ln(1+x)$ in a [[Serie di Taylor|Taylor series]] about $0$ to find
$$\begin{align}
\frac{1}{V}\ln \mathcal{Z}&=\frac{4\pi}{h^{3}}\int_{0}^{\infty}p^{2}\sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}e^{-j\beta\varepsilon_{p}}}{j} \\
&=\frac{4\pi}{h^{3}}\sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}}{j}\int_{0}^{\infty}p^{2}e^{-j\beta p^{2}/2m} \\
&=\frac{4\pi}{h^{3}}\sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}}{j} \frac{\sqrt{ \pi }}{4(j\beta/2m)^{3/2}} \\
&=\left( \frac{2m\pi}{\beta h^{2}} \right)^{3/2}\underbrace{ \sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}}{j^{5/2}} }_{ f_{5/2}(z) }
\end{align}$$
We can see the Fermi function $f_{5/2}(z)$. From this we can retroactively state
$$f_{5/2}(z)=\frac{4}{\sqrt{ \pi }} \left( \frac{\beta}{2m} \right)^{3/2}\int_{0}^{\infty}p^{2}\ln(1+ze^{-\beta \varepsilon_{p}})dp$$
### Sommerfeld expansion
Fermi functions have an alternative [[serie di potenze|power series]] representation known as a [[Sommerfeld expansion]] that comes in handy in physical applications. It is accurate for high $z$. For $f_{3/2}(z)$ and $f_{5/2}(z)$ it yields
$$f_{3/2}(z)\simeq \frac{4}{3\sqrt{ \pi }}\left[ (\ln z)^{3/2}+ \frac{\pi ^{2}}{8} \frac{1}{\sqrt{ \ln z }}+\ldots \right]$$
$$f_{5/2}(z)=\frac{8}{15\sqrt{ \pi }}(\ln z)^{5/2}\left[ 1+ \frac{5\pi^{2}}{8} \frac{1}{(\ln z)^{2}}+\ldots \right]$$
The full proof is in the Sommerfeld expansion page.
### Low $z$ approximation
For low $z$, there is no need for a fancy method like the Sommerfeld expansion: the first few terms of the definition are accurate:
$$f_{k}(z)=z- \frac{z^{2}}{2^{k}}+ \frac{z^{3}}{3^{k}}-\ldots$$
