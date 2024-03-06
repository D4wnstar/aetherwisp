### Formulazione di Schroedinger
Consideriamo l'[[Hamiltoniana]]
$$H=- \frac{\hbar^{2}}{2M}\nabla^{2}_{R}- \frac{\hbar^{2}}{2m}\nabla^{2}_{r_{e}}- \frac{Ze^{2}}{4\pi\epsilon_{0}|R-r_{e}|}$$
dove $M$ è la massa del nucleo, $m$ la masse dell'[[elettrone]], $Z$ è il numero atomico e $|R-r_{e}|$ la distanza orbitale dell'elettrone. I tre termini rappresentano, in ordine, l'energia cinetica dei nuclei, quella degli elettroni l'energia potenziale.

![[Schema modello idrogeno|center]]

Si nota che l'Hamiltoniana non dipende esplicitamente dallo [[spin]] dell'elettrone. La [[funzione d'onda]] è esprimibile come prodotto della componente spaziale e di spin
$$\psi(q)=\chi_{s,m_{s}}\psi(r)$$
dove $\chi_{ms}$ sono gli autostati dell'[[operatore]] $S_{z}$ ed $S^{2}$ con autovalori $s=1/2$ e $m_{s}=\pm1/2$. Cerchiamo questi autostati.

Prendiamo il momento angolare orbitale $\vec{L}=\vec{r}\times\vec{p} =-i\hbar(\vec{r}\times\nabla)$. Per componenti
$$\begin{cases}
L_{x}=yp_{z}-zp_{y}=-i\hbar\left(y \frac{\partial }{\partial z} -z \frac{\partial }{\partial y}\right) \\
L_{y}=-i\hbar\left(z \frac{\partial }{\partial x} -x \frac{\partial }{\partial z}\right) \\
L_{z}=-i\hbar\left(x \frac{\partial }{\partial y} -y \frac{\partial }{\partial x}\right) \\
\end{cases}$$
Usando il [[commutatore]] si trova
$$\begin{cases}
[L_{x},L_{y}]=i\hbar L_{z} \\
[L_{y},L_{z}]=i\hbar L_{x} \\
[L_{z},L_{x}]=i\hbar L_{y}
\end{cases}$$
e dato che i commutatori non sono nulli, non è possibile costruire autostati simultanei su più momenti angolari, quindi non è possibili misurarli insieme con arbitraria precisione. Tuttavia, è possibile costruire autostati simultanei per $L^{2}=L_{x}^{2}+L_{y}^{2}+L_{z}^{2}$ e $L_{z}$ dato che $[L^{2},L_{z}]=0$. Lo stesso vale per lo spin.

Si ha
$$S^{2}\alpha=\frac{3}{4}\hbar^{2}\alpha\quad;\quad S_{z}\alpha=\frac{\hbar}{2}\alpha$$
$$S^{2}\beta=\frac{3}{4}\hbar^{2}\beta\quad;\quad S_{z}\beta=-\frac{\hbar}{2}\beta$$
Quindi per sovrapposizione degli [[stato|stati]]
$$\chi=\chi_{+}\alpha+\chi_{-}\beta\quad;\quad|\chi_{+}|^{2}+|\chi_{-}|^{2}=1$$
$$\langle \alpha|\alpha\rangle=1\quad;\quad \langle \beta|\beta\rangle=1\quad; \quad \langle \alpha|\beta\rangle=\langle \beta|\alpha\rangle=0$$
Usando le [[matrici di Pauli]]
$$S^{2}=\frac{3}{4}\hbar^{2}\pmatrix{1 & 0 \\ 0 & 1}$$
$$S_{x}=\frac{\hbar}{2}\pmatrix{0 & 1 \\ 1 & 0}=\frac{\hbar}{2}\sigma_{x}\quad;\quad S_{y}=\frac{\hbar}{2}\pmatrix{0 & -i \\ i & 0}=\frac{\hbar}{2}\sigma_{y}\quad;\quad S_{z}=\frac{\hbar}{2}\pmatrix{1 & 0 \\ 0 & -1}=\frac{\hbar}{2}\sigma_{z}$$
Possiamo scrivere la soluzione dell'[[equazione di Schrödinger]] come
$$\left[- \frac{\hbar^{2}}{2\mu} \frac{1}{r^{2}} \frac{\partial }{\partial r}\left(r^{2}\frac{\partial }{\partial r}\right)+ \frac{\vec{L}^{2}}{2\mu r^{2}} - \frac{Ze^{2}}{4\pi\epsilon_{0}r}\right]\Psi(r,\theta,\phi)=E\Psi(r,\theta,\phi)$$
e troviamo le autofunzioni dell'operatore $L$
$$L^{2}Y_{l,m}(\theta,\phi)=l(l+1)\hbar^{2}Y_{l,m}(\theta,\phi)$$
$$L_{z}Y_{l,m}(\theta,\phi)=m\hbar Y_{L,m}(\theta,\phi) \rightarrow L_{z}\phi(\phi)=m\hbar\phi(\phi)$$
con
$$\phi_{m}(\phi)=\frac{1}{\sqrt{2\pi}}e^{im\phi};\quad \phi_{m}(0)=\phi_{m}(2\pi)$$
$l$ è il *numero quantico del momento angolare* e $m$ è il *numero quantico del momento magnetico*.