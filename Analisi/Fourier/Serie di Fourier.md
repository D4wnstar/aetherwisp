---
wiki-publish: true
aliases:
  - coefficienti di Fourier
---
Data una [[Funzione generalmente continua]] $f(x)$ definita su un intervallo $]-L,L[$, la sua espansione in **serie trigonometrica di Fourier** canonica è
$$f(x)=\alpha_{0}+\sum\limits_{n=1}^{\infty}\alpha_{n}\cos\left(\frac{n\pi}{L}x\right)+\sum\limits_{n=1}^{\infty}\beta_{n}\sin\left(\frac{n\pi}{L}x\right)$$
dove i coefficienti $\alpha_{0}$, $\alpha_{n}$ e $\beta_{n}$ sono detti **coefficienti di Fourier** e valgono
$$\begin{cases}
\alpha_{0}=\frac{1}{2L}\int_{-L}^{+L}f(x)dx \\
\alpha_{n}=\frac{1}{L}\int_{-L}^{+L}f(x)\cos(\frac{n\pi}{L}x)dx \\
\beta_{n}=\frac{1}{L}\int_{-L}^{+L}f(x)\sin(\frac{n\pi}{L}x)dx
\end{cases}$$

La funzione $f$ così trovata può essere vista intuitivamente come una "combinazione lineare infinita" di una "base" costituita dai vettori
$$\left[1,\;\cos\left(\frac{n\pi}{L}x\right),\;\sin\left(\frac{n\pi}{L}x\right)\right]\quad\forall n\in\mathbb{N}$$
che più correttamente costituiscono un [[Sistema completo]], ossia il sistema canonico della serie di Fourier. Possiamo anche normalizzare questi vettori
$$\left[\frac{1}{\sqrt{2L}},\; \frac{1}{\sqrt{L}} \cos\left(\frac{n\pi}{L}x\right),\; \frac{1}{\sqrt{L}}\sin\left(\frac{n\pi}{L}x\right)\right]\quad\forall n\in\mathbb{N}$$
e ottenere un [[Sistema ortonormale completo]], per il quale valgono proprietà più generali. In questo sistema, i coefficienti diventano $a_{0}=\sqrt{2L}\alpha_{0}$, $a_{2n}=\sqrt{L}\alpha_{n}$ e $a_{2n-1}=\sqrt{L}\beta_{n}$.
### Proprietà
Valgono le seguenti proprietà
1. se $f(x)$ è continua con derivata generalmente continua e vale $f(L)=f(-L)$, allora la serie [[Convergenza uniforme|converge uniformemente]].
2. se $f(x)$ è generalmente continua con derivata generalmente continua, la serie [[Convergenza puntuale|converge in ogni punto]] e ha per somma la $f(x)$ in tutti i punti in cui è continua. Nei punti in cui non è continua e agli estremi, ha per somma la "media" $\frac{1}{2}[f(x_{0}^{+})+f(x_{0}^{-})]$.
3. se $f(x)$ è pari, allora $\alpha_{0}=\frac{1}{L}\int_{0}^{L}f(x)dx$, $\alpha_{n}=\frac{2}{L}\int_{0}^{L}f(x)\cos\left(\frac{n\pi}{L}x\right)dx$ e $\beta_{n}=0$; un risultato analogo vale se $f(x)$ è dispari.
4. se vale $\sum\limits_{n}|\alpha_{n}|+\sum\limits_{n}|\beta_{n}|<\infty$, allora $f(x)$ è continua e $f(L)=f(-L)$. Questo segue dalla definizione di convergenza totale.
### Generalizzazione
È possibile costruire la serie di Fourier di una funzione $f$ definita su un intervallo qualsiasi per qualunque sistema (ortonormale) completo. Preso un sistema completo $\{f^{(n)}\}_{n\in\mathbb{N}}$ in uno [[Spazio di Hilbert]], la funzione $f$ può essere espressa con la sua serie di Fourier
$$f=\sum\limits_{n=1}^{\infty}a_{n}f^{(n)}$$
Se poi il sistema è anche ortonormale, vale $(f^{(m)}, f^{(n)})=\delta_{mn}$ (dove le parentesi denotano il [[Scalar product]]) e se si conosce $f$, è possibile ottenere i coefficienti con
$$a_{n}=(f^{(n)},f)$$

Se $f$ è [[Spazi Lp#Spazio $L {2}$|L^2]] e vale $\int |f(x)|^{2}dx=1$, vale anche l'importante proprietà di [[Normalization]]
$$\sum\limits_{n=1}^{\infty}|a_{n}|^{2}=1$$
e $|a_{n}|^{2}$ può essere vista come una sorta di rappresentazione di "importanza" della $f_{n}$-esima componente: più alto è $|a_{n}|^{2}$, più è importante $f_{n}$ nell'espansione funzione $f$.
#### Dimostrazione
$$1=\int|f(x)|^{2}dx=\int f(x)^{*}f(x)dx=\int \left(\sum\limits_{m=1}^{\infty}c_{m}f_{m}(x)\right)^{*}\left(\sum\limits_{n=1}^{\infty}c_{n}f_{n}(x)\right)dx=$$
$$=\sum\limits_{m=1}^{\infty}\sum\limits_{n=1}^{\infty}c_{m}^{*}c_{n}\int f_{m}^{*}(x)f_{n}(x)dx=\sum\limits_{m=1}^{\infty}\sum\limits_{n=1}^{\infty}c_{m}^{*}c_{n}\delta_{mn}=\sum\limits_{n=1}^{\infty}c_{n}^{*}c_{n}=\sum\limits_{n=1}^{\infty}|c_{n}|^{2}$$
Più in generale, se $\int |f(x)|^{2}=A$, allora $\sum\limits_{n=1}^{\infty}|c_{n}|^{2}=A$.