---
wiki-publish: true
---
La **formula semiempirica di massa**, anche conosciuta come **formula di Weizsacker**, è una formula per stimare la massa e l'[[Binding energy]] di un [[Atom]]:
$$m(Z,A)=Nm_{n}+Zm_{p}+Zm_{e}- \frac{B(Z,A)}{c^{2}}$$
con
$$\frac{B(Z,A)}{c^{2}}=a_{v}A-a_{s}A^{\frac{2}{3}}-a_{c} \frac{Z(Z-1)}{A^{\frac{1}{3}}}-a_{a} \frac{(N-Z)^{2}}{4A}+\delta$$
dove
- $m_{n}$, $m_{p}$ e $m_{e}$ sono masse di [[neutrone]], [[protone]] ed [[elettrone]].
- $Z$, $N$ e $A$ sono il [[Atom|numero atomico]], il [[Atom|numero di neutroni]] e il [[Atom|numero di massa atomica]].
- $B(Z,A)$ è l'energia di legame.
- $c$ è la [[velocità della luce]].

La formula per l'energia di legame contiene cinque termini costanti misurati sperimentalmente con un particolare significato:
1. $a_{v}A$ è il **termine di volume** ed è proporzionale ad $A$. In teoria, se ogni [[nucleone]] interagisse con ogni altro nucleone, la proporzionalità sarebbe $B\propto A(A-1)\sim A^{2}$, dato sperimentalmente si trova che il raggio del nucleo vale $R\propto A^{1/3}$. In pratica, si trova $B\propto A$, che suggerisce che i nucleoni interagiscono solo con i loro vicini.
2. $a_{s}A^{2/3}$ è il **termine di superficie**. La discussione sulle interazioni con nucleoni vicini vale per quelli *dentro* il nucleo, ma quelli in superficie hanno meno "vicini", quindi sono legati meno fortemente. Questo termine viene sottratto per tenere conto di questa mancanza. È proporzionale alla superficie nucleare, che sperimentalmente è $R^{2}\propto A^{2/3}$.
3. $a_{c} \frac{Z(Z-1)}{A^{\frac{1}{3}}}$ è il **termine Coulombiano**. I protoni sono carichi e si respingono a vicenda mediante [[Electromagnetism]], che indebolisce il loro legame.$$E_{Coulombiana}\propto \frac{Z(Z-1)\alpha\hbar c}{R}\propto Z(Z-1)A^{-1/3}$$
4. $a_{a} \frac{(N-Z)^{2}}{4A}$ è il **termine di asimmetria**. Tiene conto del fatto che negli atomi più pesanti si rompe la simmetria tra neutroni e protoni per compensare l'aumento della repulsione Coulombiana dei neutroni. Se i protoni e neutroni sono in pari numero, il termine si annulla. Ha l'effetto di abbassare la curva per atomi grandi.
5. $\delta$ è il **termine di accoppiamento** ed ha origine sperimentale. Si è scoperto che i nuclei sono più stabili se contengono un numero pari di protoni e neutroni. Ciò suggerisce che protoni e neutroni tendano ad accoppiarsi. Infatti, dei 171 nuclei stabili noti, solo 4 hanno $N$ e $Z$ dispari. Tutti gli altri hanno $N$ e $Z$ pari. Vale$$\begin{align}
\delta=a_{p}A^{-3/4} \quad &\text{se }A,Z,N\text{ sono pari} \\
\delta = 0 \quad & \text{se }A\text{ è dispari} \\
\delta=-a_{p}A^{-3/4} \quad &\text{se }A\text{ è pari e }Z,N\text{ sono dispari}
\end{align}$$In questo caso, l'esponente $-3/4$ è completamente empirico e ottenuto da un fit.

Le costanti valgono
$$\begin{align}
a_{v} &= 15.67\,\frac{MeV}{c^{2}} \\
a_{s} &= 17.23\,\frac{MeV}{c^{2}} \\
a_{c} &= 0.714\,\frac{MeV}{c^{2}} \\
a_{a} &= 93.15\,\frac{MeV}{c^{2}} \\
a_{p} &= 34\,\frac{MeV}{c^{2}}
\end{align}$$

![[Grafico Energia di legame Semiempirica.png]]