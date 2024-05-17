### Formulazione semiclassica
La formulazione semiclassica dell'interazione tra radiazione e materia usa campi classici e [[Atomo|atomi]] quantistici, trascurando il feedback dell'atomo sul campo.

Partiamo dalla [[forza di Lorentz]]
$$\vec{F}=q(\vec{E}+\vec{v}\times\vec{B})$$
da cui otteniamo la [[Lagrangiana]]
$$L=\frac{1}{2}mv^{2}-qV(r,t)+q\vec{v}\cdot\vec{A}(r,t)$$
con cui possiamo esprimere le leggi del moto
$$\frac{d}{dt}\left(\frac{\partial L}{\partial v_{x}}\right)- \frac{\partial L}{\partial x}=0$$
Vale
$$p_{x}=\frac{\partial L}{\partial v_{x}}=mv_{x}+qA_{x}$$
da cui l'[[Hamiltoniana]] di una [[particella]] in un campo
$$H=\vec{v}\cdot\vec{p}-L=\frac{(p-q\vec{A})^{2}}{2m}+qV$$
e l'[[Equazione di Schrödinger]]
$$i\hbar \frac{\partial }{\partial t}\Psi(\vec{r},t)=\left[\frac{1}{2m}(-i\hbar\nabla+e\vec{A})^{2}- \frac{Ze^{2}}{(4\pi\epsilon_{0})r}\right]\Psi(\vec{r},t)$$

L'equazione di Schrödinger è invariante per scelta di [[gauge]]
$$H=- \frac{\hbar^{2}\nabla^{2}}{2m} \frac{i\hbar q}{2m}(\vec{A}\cdot\vec{\nabla}+\vec{\nabla}\cdot\vec{A})+ \frac{q}{2m}A^{2}+qV$$
la divergenza $\vec{\nabla}\cdot\vec{A}=0$, quindi (???) traslando i potenziali
$$\vec{A}(\vec{r},t)=\vec{A}'(\vec{r},t)+\nabla\chi(\vec{r},t)$$
$$V(\vec{r},t)=V'(\vec{r},t)+ \frac{\partial }{\partial t}\chi(\vec{r},t)$$
l'Hamiltoniana non cambia.

Espandendo il quadrato, l'Hamiltoniana diventa
$$H(t)=\underbrace{\ \frac{\hbar^{2}}{2m}\nabla^{2}- \frac{Ze^{2}}{4\pi\epsilon_{0}r}}\limits_{H_{0}}-\underbrace{i\hbar \frac{e}{m}\vec{A}\cdot\vec{\nabla}+ \frac{e^{2}}{2m}\vec{A}^{2}}\limits_{H_{\text{in t}}(t)}$$
Il termine $\frac{e^{2}}{2m}\vec{A}^{2}$ è trascurabile. Scrivendo l'equazione agli autovalori
$$i\hbar \frac{\partial }{\partial t}\Psi(\vec{r}, t)=H(t)\Psi(\vec{r},t)$$
la cui soluzione più generale è
$$\Psi(\vec{r},t)=\sum\limits_{k}C_{k}(t)\Psi_{k}(\vec{r})e^{-i \frac{E_{k}t}{\hbar}}$$
con $C_{k}$ l'[[evolutore]].