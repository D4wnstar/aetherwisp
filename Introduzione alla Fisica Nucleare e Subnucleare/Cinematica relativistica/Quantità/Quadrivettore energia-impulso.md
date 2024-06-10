---
aliases:
  - quadri-impulso
---
Il **quadrivettore energia-impulso**, o **quadri-impulso**, è il [[quadrivettore]]
$$p=\left(\frac{E}{c},\; \vec{p}\right)$$
con energia $E=\gamma mc^{2}$ e impulso $\vec{p}=\gamma m\vec{v}$. In forma completa
$$p=(\gamma mc,\;\gamma m\vec{v})$$
### Energia relativistica
La sua [[norma]] è
$$\sqrt{p\cdot p}=\sqrt{\frac{E^{2}}{c^{2}}-|\vec{p}|^{2}}=\sqrt{\frac{\gamma^{2}m^{2}c^{4}}{c^{2}}-\gamma^{2}m^{2}\vec{v}^{2}}=\sqrt{m^{2}\gamma^{2}(c^{2}-v^{2})}=m\gamma\sqrt{c^{2}-v^{2}}=$$
$$=\frac{m}{\sqrt{1- \frac{v^{2}}{c^{2}}}}\sqrt{c^{2}-v^{2}}=\frac{m\sqrt{c^{2}\left(1 - \frac{v^{2}}{c^{2}}\right)}}{\sqrt{1 - \frac{v^{2}}{c^{2}}}}=mc$$
Dunque si ha
$$m^{2}c^{2}=\frac{E^{2}}{c^{2}}-|\vec{p}|^{2}$$
quindi ho una relazione tra massa, energia e impulso di una [[Particella]]. Invertendo la relazione si ha
$$E^{2}=|\vec{p}|^{2}c^{2}+m^{2}c^{4}$$
che si dice **energia relativistica totale**. Da questa possiamo anche ridefinire $\beta$ e $\gamma$ come
$$\gamma=\frac{E}{mc^{2}}\quad;\quad\beta=\frac{|\vec{p}|c}{E}$$
da cui otteniamo anche
$$\beta\gamma=\frac{|\vec{p}|}{mc}$$

Si può anche considerare solo la parte cinetica
$$K=E-mc^{2}=\gamma mc^{2} -mc^{2}=mc^{2}(\gamma-1)$$
Sviluppando $\gamma$ in serie per $\beta\ll1$ e prendendo il primo ordine, si torna alla formula classica per l'energia cinetica
$$K\sim\left(1+ \frac{\beta^{2}}{2} -1\right)\simeq \frac{mc^{2}\beta^{2}}{2}\simeq \frac{v^{2}}{2c^{2}}mc^{2}=\frac{1}{2}mv^{2}$$
### Sotto trasformazioni di Lorentz
Prendiamo una particella $p$ in un sistema di riferimento in coordinate sferiche.

![[Coordinate Sferiche Particella|center]]

Allora
$$\pmatrix{\frac{E'}{c} \\ p_{x}' \\ p_{y}' \\ p_{z}'}=\pmatrix{\gamma & 0 & 0 & \beta\gamma \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ \beta\gamma & 0 & 0 & \gamma}\pmatrix{\frac{E}{c} \\ p_{x} \\ p_{y} \\ p_{z}}$$
con
$$\begin{cases}
p_{x}=p\sin\theta\cos\phi \\
p_{y}=p\sin\theta\sin\phi \\
p_{z}=p\cos\theta
\end{cases}$$
Allora
$$\begin{cases}
E'=\gamma E+\beta\gamma p\cos\theta \\
p'\cos\theta'\cos\phi'=p\sin\theta\cos\phi \\
p'\sin\theta'\sin\phi'=p\sin\theta\sin\phi \\
p'\cos\theta=\gamma p\cos\theta+\beta\gamma E
\end{cases}$$
$$p^{2}\sin^{2}\theta'(\cos^{2}\phi'+\sin^{2}\phi')=p^{2}\sin^{2}\theta(\cos^{2}\phi+\sin^{2}\phi)$$
Da cui si ottiene
$$p'\sin\theta=p\sin\theta$$
che si chiama **impulso trasverso** e vale
$$p'_{T}=p_{T}$$
ed è un'[[invariante relativistica]]. Dalla stessa equazione si trova anche $\phi'=\phi$, quindi anche l'angolo azimutale è un'invariante relativistica.