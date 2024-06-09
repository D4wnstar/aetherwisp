Le **trasformazioni di Lorentz** sono un insieme di trasformazioni poste ad un sistema di riferimento per le quali le [[equazioni di Maxwell]] non variano. Sono una generalizzazione delle [[trasformazioni di Newton]], per le quali le [[leggi di Newton]] erano invarianti, ma quelle di Maxwell no.

Preso un sistema con coordinate spazio-temporali $x$, $y$, $z$ e $t$, le trasformazioni danno un nuovo sistema di riferimento $x'$, $y'$, $z'$, $t'$ tale per cui
$$\begin{cases}
x'=\frac{x-vt}{\sqrt{1-v^2/c^{2}}} \\
y'=y \\
z'=z \\
t'=\frac{t-vx/c^{2}}{\sqrt1-v^{2}/c^{2}}
\end{cases}$$
o, definendo $\beta=v/c$ e $\gamma=(1-\beta^{2})^{-1/2}$,
$$\begin{cases}
x'=\gamma(x-\beta ct) \\
y'=y \\
z'=z \\
ct'=\gamma(ct-\beta x)
\end{cases}$$

Nel caso non relativistico $v\ll c$, queste si riducono alle trasformazioni di Newton.

In forma [[tensore|tensoriale]], le trasformazioni di Lorentz sono
$$\Lambda(\beta)=\begin{pmatrix}\gamma & -\beta \gamma & 0 & 0 \\ -\beta \gamma & \gamma & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1\end{pmatrix}$$
applicate ad un [[quadrivettore]] come
$$a'_{\mu}=\Lambda(\beta)a_{\mu}$$

Dal punto di vista matematico, una trasformazione di Lorentz non è altro che una [[rotazione]] nello [[spaziotempo]]. Le rotazioni sono [[Operatore unitario|unitarie]], quindi la [[norma]] è conservata:
$$(x')^{2}+(y')^{2}+(z')^{2}-(ct')^{2}=x^{2}+y^{2}+z^{2}-(ct)^{2}$$
Ciò significa che la distanza spaziotemporale è un'[[invariante relativistica]].