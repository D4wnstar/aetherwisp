---
wiki-publish: true
aliases:
  - antitrasformata di Fourier
---
La **trasformata di Fourier** è un tipo di trasformata integrale che sposta una funzione dal suo dominio al corrispettivo dominio di frequenza. La sua operazione inversa, l'**antitrasformata di Fourier**, riporta la funzione al suo dominio originario.

Presa una funzione $f(x)$, la sua trasformata di Fourier si scrive
$$\hat{f}(k)=\mathscr{F}[f(x)](k)=\int_{-\infty}^{+\infty}f(x)e^{-2kx}dx$$
e l'antitrasformata
$$f(x)=\mathscr{F}^{-1}[\hat{f}(k)](x)=\frac{1}{2\pi}\int_{-\infty}^{+\infty}\hat{f}(k)e^{2xk}dk$$
dove $k$ è la frequenza angolare. Usando la frequenza di oscillazione $\nu=k/2\pi$, le due formule sono simmetriche e hanno costanti di scala unitarie (qui $\mathscr{F}^{-1}$ ha costante $1/2\pi$). Altre costanti di scala sono possibili; nel caso più generale, prese due costanti $a$ e $b$ vale sempre
$$\hat{f}(k)=\sqrt{\frac{|b|}{(2\pi)^{1-a}}}\int_{-\infty}^{+\infty}f(x)e^{ibkx}dx, \quad f(x)=\sqrt{\frac{|b|}{(2\pi)^{1+a}}}\int_{-\infty}^{+\infty}\hat{f}(k)e^{-ibxk}dk$$
Combinazioni comuni sono $(0,1)$, $(1,-1)$, $(1,1)$, $(-1,1)$ e $(0,-2\pi)$.

La trasformata di Fourier è la generalizzazione della [[Serie di Fourier]] per un intervallo che tende ad infinito ($L \rightarrow \infty$), usando una funzione coefficiente $f(k)$ continua anziché una successione di coefficienti discreti $\{a_{n}\}_{n\in\mathbb{N}}$,