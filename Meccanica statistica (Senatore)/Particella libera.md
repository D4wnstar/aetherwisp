## Una dimensione
Considero una singola particella in una dimensione. Prendo 0 come punto di origine e un punto $L>0$. Considero l'[[Equazione di Schrödinger]] con $E\geq0$ 
$$- \frac{\hbar^{2}}{2m} \frac{\partial ^{2}}{\partial x^{2}}\psi(x)=E\psi(x)$$
Definendo $k^{2}=\frac{2mE}{\hbar^{2}}$ si trova
$$-\psi''(x)= \frac{2mE}{\hbar^{2}}\psi(x) \Rightarrow \psi''(x)+k^{2}\psi(x)=0$$
che è una [[EDO lineare]] al secondo ordine. Si può risolvere in uno di due modi
$$\begin{align*}
\psi(x) &= \sin(kx),\cos(kx) \\
\psi(x) &= e^{ikx},e^{-ikx}
\end{align*}$$
Dobbiamo fissare delle condizioni al contorno: usiamo la [[Periodic boundary condition]] o la [[Homogenous Boundary Condition]].

Usando la HBC, deve essere
$$\psi(x)=A\sin(kx)+B\cos(kx)$$
con $B=0$, $A\neq0$ e $\sin(kL)=0$ dove $k= \frac{\pi}{L}n$ e $n\in\mathbb{N}$.

Nel caso della PCB si ha
$$e^{\pm ikx}=e^{\pm ik(x+L)}=1$$
con $k=\frac{2\pi}{L}n$ e $n\in\mathbb{Z}$. Allora si giunge all'espressione per l'energia
$$E=\frac{\hbar^{2}}{2m} \left(\frac{2\pi}{L}\right)^{2}n^{2}$$
## Tre dimensioni
Ora considero lo stesso problema in tre dimensioni. Prendo come spazio un cubo di spigolo $L$. L'equazione di Schroedinger diventa
$$- \frac{\hbar^{2}}{2m}\left[\frac{\partial ^{2}\psi}{\partial x^{2}}+\frac{\partial ^{2}\psi}{\partial y}+\frac{\partial \psi^{2}}{\partial z^{2}}\right]=E\psi$$
Per risolvere l'equazione differenziale, proviamo ad usare la separazione delle variabili. Scelgo $\psi(x,y,z)=\alpha(x)\beta(y)\gamma(z)$. Allora
$$- \frac{\hbar^{2}}{2m} [\alpha''(x)\beta(y)\gamma(z)+\alpha(x)\beta''(y)\gamma(z)+\alpha(x)\beta(y)\gamma''(z)]=E\alpha(x)\beta(y)\gamma(z)$$
$$- \frac{\hbar^{2}}{2m}\left[ \frac{\alpha''(x)}{\alpha(x)}+\frac{\beta''(y)}{\beta\left(y\right)}+ \frac{\gamma''(z)}{\gamma(z)}\right]=E$$
Proviamo a risolvere con $\frac{\alpha''(x)}{\alpha(x)}=E_{1}$, $\frac{\beta''(y)}{\beta(y)}=E_{2}$ e $\frac{\gamma''(z)}{\gamma(z)}=E_{3}$. Allora ho $\alpha''(x)=E_{1}\alpha(x)$, $\beta''(y)=E_{2}\beta(y)$ e $\gamma''(z)=E_{3}\beta(z)$, che sono tre equazioni differenziali della stessa forma. Vale
$$E=- \frac{\hbar^{2}}{2m}(-|E_{1}|-|E_{2}|-|E_{3}|)$$
Risolvendo le differenziali
$$\alpha(x)=e^{ik_{1}x};\quad \beta(y)=e^{ik_{2}y};\quad\gamma(z)=e^{ik_{3}z}$$
Allora l'equazione di Schroedinger si risolve con
$$\psi(x,y,z)=e^{i(k_{1}x+k_{2}y+k_{3}z)}=e^{i\bar{k}\cdot\bar{r}}$$
con $\bar{k}=(k_{1},k_{2},k_{3})=\frac{2\pi}{L}(n_{1},n_{2},n_{3})$. L'energia diventa
$$E_{\bar{k}}=\frac{\hbar^{2}}{2m}\bar{k}^{2}=\frac{\hbar^{2}}{2m}\left(\frac{2\pi}{L}\right)^{2}(n_{1}^{2}+n_{2}^{2}+n_{3}^{2})$$
Prendendo $n_{1},n_{2},n_{3}\neq0$ e tutti diversi fra loro, si hanno 48 stati diversi che danno la stessa energia, ossia si ha degenerazione.