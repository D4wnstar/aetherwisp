---
wiki-publish: true
aliases:
  - funzione di Bessel sferica del primo tipo
  - funzione di Bessel sferica del secondo tipo
---
Le **funzioni di Bessel sferiche** sono le due funzioni [[lineare indipendenza|linearmente indipendenti]] che risolvono l'[[Equazione differenziale di Bessel sferica]]. Si distinguono in *primo tipo* $j_{n}(x)$ e *secondo tipo* $n_{n}(x)$ per ogni $n$ intero. Sono una forma riscalata delle [[funzioni di Bessel]] $J_{n}$ e $Y_{n}$ con ordine a mezzo intero e valgono[^1]
$$\begin{align}
j_{n}(z)&\equiv \sqrt{\frac{\pi}{2}} \frac{J_{n+1/2}(z)}{\sqrt{z}}=(-x)^{l}\left(\frac{1}{x} \frac{d}{dx}\right)^{l} \frac{\sin x}{x} \\
n_{n}(z)&\equiv \sqrt{\frac{\pi}{2}} \frac{Y_{n+1/2}(z)}{\sqrt{z}} = -(-x)^{l}\left(\frac{1}{x} \frac{d}{dx}\right)^{l} \frac{\cos x}{x}
\end{align}$$

Per $x\ll1$, possono essere scritte in forma asintotica come
$$j_{n} \rightarrow \frac{2^{n}n!}{(2n+1)!}x^{n}, \quad n_{n} \rightarrow - \frac{(2n)!}{2^{n}n!} \frac{1}{x^{n+1}}$$

[^1]: Il secondo termine di ciascuna definizione è preso da *Introduction to Quantum Mechanics di Griffiths, p. 144*, anche se non trovo un'espansione delle funzioni di Bessel che combacia con la sua su MathWorld.