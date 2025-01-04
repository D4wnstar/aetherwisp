The **Sommerfeld expansion** is an approximation method for a certain class of integrals related to the [[Fermi-Dirac distribution]]. It leads to a [[serie di potenze|power series]] representation where each term contains an integral. The general form of the integral that can be expanded with this method is
$$\int_{-\infty}^{\infty} \frac{H(\varepsilon)}{z^{-1}e^{\beta\varepsilon}
+1} \ d\varepsilon $$
where the integrand is the Fermi-Dirac distribution multiplied by some factor $H(\varepsilon)$, which must vanish when $\varepsilon\to-\infty$ and rise no faster than a polynomial when $\varepsilon\to \infty$. This approximation is accurate for high $z$, which means for low [[temperature]].
### Fermi functions
The [[Fermi and Bose functions|Fermi functions]] (in integral form) are all eligible for this method since $H(\varepsilon)$ is a monomial in them. The following is a derivation for $f_{3/2}(z)$ specifically. We start from the integral representation:
$$f_{3/2}(z)=\frac{4}{\sqrt{ \pi }}\int_{0}^{\infty} \frac{x^{2}}{z^{-1}e^{x^{2}}+1}dx$$
If we take $z$ to be the fugacity $e^{\beta \mu}$, we can write $z^{-1}e^{x^{2}}=e^{x^{2}-\beta \mu}$ call $\beta \mu=\nu$ and make the substitution $x^{2}=y$. All of these give us
$$f_{3/2}(z)=\frac{4}{\sqrt{ \pi }}\int_{0}^{\infty} \frac{x^{2}}{e^{x^{2}-\nu}+1}dx=\frac{4}{2\sqrt{ \pi }}\int_{0}^{\infty} \frac{\sqrt{ y }}{e^{y-\nu}+1}dy=\ldots$$
For $\nu$, the the factor $\frac{1}{e^{y-\nu}+1}$ (the Fermi-Dirac distribution) is almost a [[theta di Heaviside|Heaviside step function]][^1], the derivative of which would more or less be akin to a [[Delta di Dirac|Dirac delta]]. If we can rework the integral to have that derivative, then we could solve it by approximating it around the neighborhood of $\nu$ with little error. A good way of manifesting a derivative out of thin air is [[Integrazione per parti|integration by parts]], which we'll do on the distribution and the numerator $\sqrt{ y }$:
$$\begin{align}
\ldots=\frac{2}{\sqrt{ \pi }}\int_{0}^{\infty} \frac{\sqrt{ y }}{e^{y-\nu}+1}dy&=\frac{2}{\sqrt{ \pi }}\left[ \frac{2}{3}\left( \frac{y^{3/2}}{e^{y-\nu}+1} \right)_{0}^{\infty}- \frac{2}{3}\int_{0}^{\infty} y^{3/2}\frac{ \partial  }{ \partial y } \frac{1}{e^{y-\nu}+1} \right] \\
&=\frac{4}{3\sqrt{ \pi }}\int_{0}^{\infty} y^{3/2} \frac{e^{y-\nu}}{(e^{y-\nu}+1)^{2}}dy
\end{align}$$
As the above discussion, this integral is now peaked around $\nu$ due to the derivative. This justifies an accurate approximation around $\nu$. First, we make the substitution $y=\nu+t$, which yields
$$\ldots=\frac{4\nu^{3/2}}{3\sqrt{ \pi }}\int_{-\nu}^{\infty} \left( 1+ \frac{t}{\nu} \right)^{3/2} \frac{e^{t}}{(e^{t}+1)^{2}}dt=\ldots$$
We care about high $z$ and since $z=e^{\nu}$, this means high $\nu$. This means that the lower bounds approaches negative infinity. Since the integral is almost completely around $\nu$, we set the lower bound to $-\infty$:
$$\ldots\simeq\frac{4\nu^{3/2}}{3\sqrt{ \pi }}\int_{-\infty}^{\infty} \left( 1+ \frac{t}{\nu} \right)^{3/2} \frac{e^{t}}{(e^{t}+1)^{2}}dt=\ldots$$
To get a power series, we use the [[Serie di Taylor|Taylor series]] expansion about $0$ of $t/\nu$ for
$$\left( 1+ \frac{t}{\nu} \right)^{3/2}=\sum_{n=0}^{\infty} \frac{1}{n!}\left( \frac{t}{\nu} \right)^{n} \frac{d^{n}}{d(t/\nu)^{n}}\left( 1+ \frac{t}{\nu} \right)^{3/2}= 1+ \frac{3}{2} \frac{t}{\nu}+ \frac{3}{8} \frac{t^{2}}{\nu ^{2}}+\ldots$$
With this, we have
$$\ldots= \frac{4\nu^{3/2}}{3\sqrt{ \pi }}\int_{-\infty}^{\infty}\left( 1+ \frac{3}{2} \frac{t}{\nu} + \frac{3}{8} \frac{t^{2}}{\nu ^{2}}+ \ldots \right) \frac{e^{t}}{(e^{t}+1)^{2}}dt=\ldots$$
Using integral linearity, we can invert the sum with the integral to write
$$\ldots=\frac{4\nu^{3/2}}{3\sqrt{ \pi }} \left( I_{0}+ \frac{3}{8\nu ^{2}}I_{2}+\ldots \right)$$
where each $I_{n}$ terms in an integral that looks like
$$\boxed{I_{n}=\int_{-\infty}^{\infty} \frac{t^{n}e^{t}}{(e^{t}-1)^{2}} \ dt }$$
You'll notice that $I_{1}$ is gone: in fact, all odd terms are gone. This is because all of those integrals evaluate to zero, leaving only even powers. The first two non-zero integrals are $I_{0}=1$ and $I_{2}=\pi ^{2}/3$.[^2] The full approximate form when $z\gg 1$ is
$$\boxed{f_{3/2}(z)\simeq \frac{4\nu^{3/2}}{3\sqrt{ \pi }}\sum_{n=0,\text{ even}}^{\infty} \frac{I_{n}}{\nu^{n}n!} \frac{d^{n}}{d\nu^{n}}(1+\nu^{-1})}$$
In practice, we only care about the first few terms, which are
$$f_{3/2}(z)\simeq \frac{4}{3\sqrt{ \pi }}\left[ (\ln z)^{3/2}+ \frac{\pi ^{2}}{8} \frac{1}{\sqrt{ \ln z }}+\ldots \right]$$
since $\nu=\ln z$.

[^1]: This is due to the [[Pauli exclusion principle]], which constrains [[Occupation number|occupation numbers]] to be $0$ or $1$ for fermions.
[^2]: As it happens, these integrals have another nice form: $I_{n}=(n-1)!(2n)(1-2^{1-n})\zeta(n)$. Here, $\zeta(n)$ is the [[Riemann zeta function]].