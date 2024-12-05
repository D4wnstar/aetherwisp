A **Gaussian integral** is an integral of the form
$$\int_{-\infty}^{\infty} e^{-a(x+b)^{2}} \ dx=\sqrt{ \frac{\pi}{a} } $$
Strictly speaking, *the* Gaussian integral is the one with $a=b=1$:
$$\int_{-\infty}^{\infty} e^{-x^{2}} \ dx =\sqrt{ \pi }$$
This integral commonly occurs in quantum mechanics (e.g. in the [[Oscillatore armonico quantistico|quantum harmonic oscillator]] [[Stato stazionario|energy eigenstates]]), statistical mechanics (e.g. in [[Canonical ensemble|canonical]] and [[Grand canonical ensemble|grand canonical]] [[Partition function|partition functions]]) and statistics (e.g. in calculating [[function moments]]).
### Solution
There are several methods for solving this integral. The simplest just consists of using the evenness of the function, making the substitution $x=\sqrt{ t }$ and noticing the definition of the [[Gamma function]]:
$$\int_{-\infty}^{\infty} e^{-x^{2}} \ dx =2\int_{0}^{\infty}e^{-x^{2}}\ dx=2\int_{0}^{\infty} \frac{1}{2}e^{-t}t^{-1/2} \ dt =\Gamma\left( \frac{1}{2} \right)=\sqrt{ \pi }$$
A related integral is
$$\int_{-\infty}^{\infty} x^{2}e^{-x^{2}} \ dx=\frac{\sqrt{ \pi }}{2a^{3/2}}$$
The relation between the two can be seen by applying [[Integrazione per parti|integration by parts]] on $1$ and $e^{-x^{2}}$ on the Gaussian integral:
$$\int_{-\infty}^{\infty} e^{-x^{2}} \ dx=2a\int_{-\infty}^{\infty} x^{2}e^{-x^{2}} \ dx$$
