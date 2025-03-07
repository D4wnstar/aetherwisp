---
aliases:
  - l^1
  - l^2
  - l^p
---
Si chiamano **spazi** $\ell^{p}$ gli spazi di successioni di numeri complessi che godono della seguente proprietà
$$\sum\limits_{i=1}^{\infty}|a_{i}|^{p}<+\infty$$
Tutti gli spazi $\ell^{p}$ sono [[Spazio di Banach|spazi di Banach]].
### Spazio $\ell^{1}$
Si definisce **spazio** $\ell^{1}$ lo spazio di tutte le successioni $\{a_{i}\}$ tali che
$$\sum\limits_{i=1}^{\infty}|a_{i}|<+\infty$$
Si ha che se una successione è $\ell^{1}$, è anche $\ell^{2}$, ma non viceversa.
### Spazio $\ell^{2}$
Si definisce **spazio** $\ell^{2}$ lo spazio di tutte le successioni $\{a_{i}\}$ tali che
$$\sum\limits_{i=1}^{\infty}|a_{i}|^{2}<+\infty$$
È uno [[Spazio di Hilbert]] con definito il seguente [[Scalar product]]: prese due successioni $a\equiv\{a_{n}\}$ e $b\equiv\{b_{n}\}$ di $\ell^{2}$, il prodotto scalare fra le due è
$$(a,b)=\sum\limits_{i=1}^{\infty}a_{i}^{*}b_{n}$$
Questo spazio è particolarmente importante per un motivo: preso un vettore $v$ di uno spazio di Hilbert separabile, si ha che può essere rappresentato univocamente in una successione di coefficienti di Fourier, e questa successione appartiene a $\ell^{2}$. Esiste dunque un *isomorfismo biunivoco* tra un qualunque spazio di Hilbert separabile $H$ e $\ell^{2}$, quindi un qualunque vettore individua una successione unica in $\ell^{2}$ e viceversa. Vale inoltre, grazie all'[[Identità di Parseval]], che la [[Norma]] calcolata in $H$ è sempre uguale alla norma calcolata in $\ell^{2}$ usando la successione associata.

Un esempio semplice di [[Sistema ortonormale completo]] in $\ell^{2}$ è il sistema canonico
$$e_{1}\equiv(1,0,0,\ldots),\;e_{2}\equiv(0,1,0,\ldots),\;\ldots,\;e_{n}=(0,\ldots,1,0,\ldots),\;\ldots$$
