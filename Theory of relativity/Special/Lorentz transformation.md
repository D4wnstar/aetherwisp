---
wiki-publish: true
aliases:
  - relativistic
  - ultrarelativistic
---
Le **trasformazioni di Lorentz** sono un insieme di trasformazioni poste ad un sistema di riferimento per le quali le [[equazioni di Maxwell]] non variano. Sono una generalizzazione delle [[trasformazioni di Newton]], per le quali le [[leggi di Newton]] erano invarianti, ma quelle di Maxwell no.

Preso un sistema con coordinate spazio-temporali $x$, $y$, $z$ e $t$, le trasformazioni danno un nuovo sistema di riferimento $x'$, $y'$, $z'$, $t'$ tale per cui
$$\begin{cases}
x'=\frac{x-vt}{\sqrt{1-v^2/c^{2}}} \\
y'=y \\
z'=z \\
t'=\frac{t-vx/c^{2}}{\sqrt{1-v^{2}/c^{2}}}
\end{cases}$$
o, definendo
$$\beta=\frac{v}{c}\in[0,1[\quad;\quad\gamma= \frac{1}{\sqrt{1-\beta^{2}}}\geq1$$
si ha
$$\begin{cases}
x'=\gamma(x-\beta ct) \\
y'=y \\
z'=z \\
ct'=\gamma(ct-\beta x)
\end{cases}$$
Nel caso non relativistico $v\ll c$, queste si riducono alle trasformazioni di Newton.

In forma [[tensore|tensoriale]], le trasformazioni di Lorentz sono
$$\Lambda(\beta)=\begin{pmatrix}\gamma & -\beta \gamma & 0 & 0 \\ -\beta \gamma & \gamma & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1\end{pmatrix}$$
applicate ad un [[Four-vector]] come
$$a'_{\mu}=\Lambda(\beta)a_{\mu}$$
### Limite relativistico
Gli effetti relativistici diventano importanti solo quando la velocità di un oggetto si avvicina a quella della luce. Si dice **limite relativistico** il limite oltre il quale bisogna usare la relatività per evitare errori grandi. Matematicamente, il limite equivale ad avere $\beta\sim1$ e $\gamma>1$. Si dice **regime ultrarelativistico** le condizioni $\beta\sim1$ e $\gamma\gg1$.
### Formalismo matematico
Dal punto di vista matematico, una trasformazione di Lorentz non è altro che una [[rotazione]] iperbolica nello [[Spacetime]], il cui angolo di rotazione è detto [[Rapidity]]. Le rotazioni sono [[Operatore unitario|unitarie]], quindi la [[Norma]] è conservata:
$$(x')^{2}+(y')^{2}+(z')^{2}-(ct')^{2}=x^{2}+y^{2}+z^{2}-(ct)^{2}$$
Ciò significa che la distanza spaziotemporale è un'[[Relativistic invariant]].

Il determinante del tensore di Lorentz vale
$$\det\Lambda=\gamma^{2}-\beta^{2}\gamma^{2}=1$$
### Contrazione e dilatazione dello spaziotempo
Le trasformazioni di Lorentz hanno due importanti conseguenze: all'avvicinarsi alla [[velocità della luce]], gli spazi si contraggono e il tempo si dilata.

Consideriamo due sistema di riferimento cartesiani, $O$ e $O'$. $O$ ha un osservatore fermo, $O'$ è in moto lungo la direzione $x$. Se misuriamo la distanza $L'$ nel sistema in moto, usando le trasformazioni di Lorentz, troviamo
$$L'=x_{2}'-x_{1}'=\gamma(x_{2}-x_{1})-\beta\gamma c(t_{2}-t_{1})=\gamma(x_{2}-x_{1})=\gamma L$$
dato che la misura è compiuta in simultanea al tempo $t_{1}=t_{2}$. La distanza è quindi contratta di un fattore $\gamma$.

Se invece diciamo che due eventi accadono nello stesso luogo $x_{1}'=x_{2}'$ in tempi diversi $t_{1}'\neq t_{2}'$ nel sistema fermo (ora diciamo che $O'$ è fermo per comodità di notazione), osservando gli eventi dal sistema in moto $O$ misuro una differenza di tempo
$$\Delta t=\gamma \Delta t'+ \frac{\beta\gamma}{c}\Delta x'=\gamma \Delta t'$$
dato che $\Delta x'=0$. Il tempo è quindi dilatato di un fattore $\gamma$.