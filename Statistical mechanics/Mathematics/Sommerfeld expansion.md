---
wiki-publish: true
---
The **Sommerfeld expansion** is an approximation used to solve a certain class of integrals related to the [[Fermi-Dirac distribution]]. It leads to a [[serie di potenze|power series]] representation where each term contains an integral. The general form of the integral that can be expanded with this method is
$$\int_{-\infty}^{\infty} \frac{H(\varepsilon)}{z^{-1}e^{\beta\varepsilon}
+1} \ d\varepsilon $$
where the integrand is the Fermi-Dirac distribution multiplied by some factor $H(\varepsilon)$, which must vanish when $\varepsilon\to-\infty$ and rise no faster than a polynomial when $\varepsilon\to \infty$.  The lower bound may be $0$ instead of $-\infty$, in which case the vanishing at $\varepsilon\to -\infty$ need not be respected. This approximation is accurate for high $z$, which means for low [[temperature]].
### Fermi functions
The [[Fermi and Bose functions|Fermi functions]] (in integral form) are all eligible for this method since $H(\varepsilon)$ is a monomial in them. The following is a derivation for $f_{3/2}(z)$ specifically. We start from the integral representation:
$$f_{3/2}(z)=\frac{2^{2}}{\sqrt{ \pi }} \frac{\Gamma(1)}{\Gamma(2)} \int_{0}^{\infty} \frac{x^{2}}{z^{-1}e^{x^{2}}+1}dx=\frac{4}{\sqrt{ \pi }}\int_{0}^{\infty} \frac{x^{2}}{z^{-1}e^{x^{2}}+1}dx=\ldots$$
If we take $z$ to be the [[fugacity]] $e^{\beta \mu}$, we can write $z^{-1}e^{x^{2}}=e^{x^{2}-\beta \mu}$ call $\beta \mu=\ln z=\nu$ and make the substitution $x^{2}=y$. All of these give us
$$\ldots=\frac{4}{\sqrt{ \pi }}\int_{0}^{\infty} \frac{x^{2}}{e^{x^{2}-\nu}+1}dx=\frac{4}{2\sqrt{ \pi }}\int_{0}^{\infty} \frac{\sqrt{ y }}{e^{y-\nu}+1}dy=\ldots$$
At high $z$, therefore high $\nu$, the factor $\frac{1}{e^{y-\nu}+1}$ (the Fermi-Dirac distribution) is almost a [[theta di Heaviside|Heaviside step function]][^1], the derivative of which would be almost a [[Delta di Dirac|Dirac delta]]. We can see this graphically if we plot the distribution at zero and low temperatures:

![[Fermi-Dirac distribution at low temperatures.png]]
*From David Tong's lecture notes on statistical physics. $E_{F}$ is the [[Fermi energy]]. The dashed line is our approximation.*

If we can rework the integral to include that derivative, then we could solve it by just calculating it around the neighborhood of $\nu$, since the function would nonzero only around there. A good way of manifesting a derivative out of thin air is with [[Integrazione per parti|integration by parts]], which we'll do on the distribution and the numerator $\sqrt{ y }$:
$$\begin{align}
\ldots&=\frac{2}{\sqrt{ \pi }}\int_{0}^{\infty} \frac{\sqrt{ y }}{e^{y-\nu}+1}dy \\
&=\frac{2}{\sqrt{ \pi }}\left[ \frac{2}{3}\left( \frac{y^{3/2}}{e^{y-\nu}+1} \right)_{0}^{\infty}- \frac{2}{3}\int_{0}^{\infty} y^{3/2}\frac{ \partial  }{ \partial y } \frac{1}{e^{y-\nu}+1} \right] \\
&=\frac{4}{3\sqrt{ \pi }}\int_{0}^{\infty} y^{3/2} \frac{e^{y-\nu}}{(e^{y-\nu}+1)^{2}}dy
\end{align}$$
The boundary integral on the left of the second step vanishes at both bounds because the numerator is either zero, or the denominator shoots up to infinity faster than the numerator. Now that we have our derivative, we can safely state that this integral is now peaked around $\nu$. This justifies an accurate approximation around $\nu$. First, we make the substitution $t=y-\nu$, which yields
$$\ldots=\frac{4\nu^{3/2}}{3\sqrt{ \pi }}\int_{-\nu}^{\infty} \left( 1+ \frac{t}{\nu} \right)^{3/2} \frac{e^{t}}{(e^{t}+1)^{2}}dt=\ldots$$
Recall that we care only about high $z$ and so high $\ln z=\nu$. This means that the lower bounds approaches negative infinity. We can therefore safely set the lower bound to $-\infty$:
$$\ldots\simeq\frac{4\nu^{3/2}}{3\sqrt{ \pi }}\int_{-\infty}^{\infty} \left( 1+ \frac{t}{\nu} \right)^{3/2} \frac{e^{t}}{(e^{t}+1)^{2}}dt=\ldots$$
To get a power series, we use the [[Taylor series|Taylor series]] expansion about $0$ of $t/\nu$ for
$$\left( 1+ \frac{t}{\nu} \right)^{3/2}=\sum_{n=0}^{\infty} \frac{1}{n!}\left( \frac{t}{\nu} \right)^{n} \frac{d^{n}}{d(t/\nu)^{n}}\left( 1+ \frac{t}{\nu} \right)^{3/2}= 1+ \frac{3}{2} \frac{t}{\nu}+ \frac{3}{8} \frac{t^{2}}{\nu ^{2}}+\ldots$$
With this, we have
$$\ldots= \frac{4\nu^{3/2}}{3\sqrt{ \pi }}\int_{-\infty}^{\infty}\left( 1+ \frac{3}{2} \frac{t}{\nu} + \frac{3}{8} \frac{t^{2}}{\nu ^{2}}+ \ldots \right) \frac{e^{t}}{(e^{t}+1)^{2}}dt=\ldots$$
Using integral linearity, we can bring the sum out to write
$$\ldots=\frac{4\nu^{3/2}}{3\sqrt{ \pi }} \left( I_{0}+ \frac{3}{8\nu ^{2}}I_{2}+\ldots \right)$$
where each $I_{n}$ terms in an integral that looks like
$$I_{n}=\int_{-\infty}^{\infty} \frac{t^{n}e^{t}}{(e^{t}-1)^{2}} \ dt$$
You'll notice that $I_{1}$ is gone: in fact, all odd terms are gone. This is because all of those integrals evaluate to zero, leaving only even powers. The first two non-zero integrals are $I_{0}=1$ and $I_{2}=\pi ^{2}/3$.[^2] The approximate series representation when $z\gg 1$ is
$$\boxed{f_{3/2}(z)\simeq \frac{4}{3\sqrt{ \pi }}(\ln z)^{3/2}\left[ 1+ \frac{\pi ^{2}}{8} \frac{1}{(\ln z)^{2}}+\ldots \right]}$$
since $\nu=\ln z$.

In a similar manner, we can find the expansion for $f_{5/2}(z)$:
$$\boxed{f_{5/2}(z)=\frac{8}{15\sqrt{ \pi }}(\ln z)^{5/2}\left[ 1+ \frac{5\pi^{2}}{8} \frac{1}{(\ln z)^{2}}+\ldots \right]}$$
and more generally for some $f_{k}(z)$:
$$\boxed{f_{k}(z)=\frac{(\ln z)^{k}}{\Gamma(k+1)}\left[ 1+ \frac{\pi ^{2}}{6} \frac{k(k-1)}{(\ln z)^{2}} +\ldots\right]}$$

[^1]: This is due to the [[Pauli exclusion principle]], which constrains [[Occupation number|occupation numbers]] to be $0$ or $1$ for fermions. Recall that at low temperatures, where random thermal forces are small, fermions pile up at the lowest state they can, up until the [[Fermi energy]]. At exactly zero temperature, there is a perfect cutoff between all states below this energy being occupied, and no state above being occupied. As the temperature increases, thermal fluctuations blur this cutoff, but if they are weak enough, it's still very close to a straight vertical line, making the distribution almost a Heaviside step function.
[^2]: As it happens, these integrals have another nice form: $I_{n}=(n-1)!(2n)(1-2^{1-n})\zeta(n)$. Here, $\zeta(n)$ is the [[Riemann zeta function]].