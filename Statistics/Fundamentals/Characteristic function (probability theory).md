The **characteristic function** of a real-valued, continuous [[random variable]] $X$ is a complex-valued function that completely describes its [[probability distribution]]. It is defined as
$$\phi^{*}_{X}(t)=E[e^{itX}]=\int_{\Omega}e^{itx}f_{X}(x)\ dx$$
where $E[\cdot]$ is the [[expected value|expectation operator]] and $f_{X}(x)$ is the [[probability density function]] of $X$. Mathematically, this is the [[Trasformata di Fourier|Fourier transform]] of the PDF.

Unlike [[Moment-generating function|moment-generating functions]], which may not exist, the characteristic function is guaranteed to exist for any distribution with a probability density function. Like an MGF, it can be used to calculated the [[Function moments|moments]] of a distribution by series expanding the exponential in a [[serie di potenze|power series]] to get
$$i^{k}\mu^{*}_{k}=\left.\frac{ \partial ^{k}\phi^{*}_{X} }{ \partial t^{k} } \right|_{t=0}$$
