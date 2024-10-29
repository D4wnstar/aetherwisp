---
aliases:
  - ortonormale
  - ortonormalità di Dirac
  - Dirac-ortonormale
---
Preso un insieme di funzioni $\{f_{n}\}_{n\in\mathbb{N}}$ o di vettori $\{v_{n}\}_{n\in\mathbb{N}}$ appartenenti ad uno spazio dotato di [[prodotto scalare]], l'insieme si dice **ortonormale** se tutti gli elementi sono [[Normalizzazione|normalizzati]] e [[Ortogonalità|ortogonali]] fra loro. In altre parole, il prodotto scalare tra qualunque due elementi è pari alla [[delta di Kronecker]], cioè
$$(f_{m},f_{n})=\delta_{mn}=\begin{cases}
1 & \text{se }m=n \\
0 & \text{se }m\neq n
\end{cases}$$

Il concetto di ortonormalità si applica solo a sistemi discreti, siano essi finiti o infiniti. È possibile costruire una forma debole di ortonormalità anche per sistemi infiniti continui, chiamata **ortonormalità di Dirac**[^1]. Presi due valori $z$ e $w$ che rappresentano due funzioni o vettori (un'indice continuo), allora vale
$$(f_{z},f_{w})=\delta(z-w)=\begin{cases}
\infty & \text{se }z=w \\
0 & \text{se }z\neq w 
\end{cases}$$
dove la delta ora è la [[delta di Dirac]].

[^1]: Il nome proviene da *Introduction to Quantum Mechanics, 2nd ed.* di Griffiths.