L'[[atomo]] di idrogeno (e tutti gli atomi *idrogenoidi*, ossia con un solo elettrone), sono gli atomi dalla struttura più semplice e gli unici ad essere risolvibili analiticamente.
### Formulazione di Schroedinger
Consideriamo l'[[Hamiltoniana]]
$$H=- \frac{\hbar^{2}}{2M}\nabla^{2}_{R}- \frac{\hbar^{2}}{2m}\nabla^{2}_{r_{e}}- \frac{Ze^{2}}{4\pi\epsilon_{0}|R-r_{e}|}$$
dove $M$ è la massa del nucleo, $m$ la masse dell'[[elettrone]], $Z$ è il numero atomico e $|R-r_{e}|$ la distanza orbitale dell'elettrone. I tre termini rappresentano, in ordine, l'energia cinetica dei nuclei, quella degli elettroni e l'energia potenziale.

![[Schema modello idrogeno|center]]

Si nota che l'Hamiltoniana non dipende esplicitamente dallo [[spin]] dell'elettrone. La [[funzione d'onda]] è esprimibile come prodotto della componente spaziale e di spin
$$\psi(q)=\chi_{s,m_{s}}\psi(r)$$
dove $\chi_{ms}$ sono gli autostati dell'[[Operatore]] $S_{z}$ ed $S^{2}$ con autovalori $s=1/2$ e $m_{s}=\pm1/2$. Cerchiamo questi autostati.

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
Possiamo scrivere la soluzione dell'[[equazione di Schrödinger]] in coordinate polari come
$$\left[- \frac{\hbar^{2}}{2\mu} \frac{1}{r^{2}} \frac{\partial }{\partial r}\left(r^{2}\frac{\partial }{\partial r}\right)+ \frac{\vec{L}^{2}}{2\mu r^{2}} - \frac{Ze^{2}}{4\pi\epsilon_{0}r}\right]\Psi(r,\theta,\phi)=E\Psi(r,\theta,\phi)$$
e troviamo le autofunzioni dell'operatore $L$
$$L^{2}Y_{l,m}(\theta,\phi)=l(l+1)\hbar^{2}Y_{l,m}(\theta,\phi)$$
$$L_{z}Y_{l,m}(\theta,\phi)=m\hbar Y_{l,m}(\theta,\phi) \rightarrow L_{z}\phi(\phi)=m\hbar\phi(\phi)$$
con
$$\phi_{m}(\phi)=\frac{1}{\sqrt{2\pi}}e^{im\phi};\quad \phi_{m}(0)=\phi_{m}(2\pi)$$
dove $Y$ sono le *armoniche sferiche*. $l$ è il *numero quantico del momento angolare* e $m$ è il *numero quantico del momento magnetico*.

Le armoniche sferiche descrivono la distribuzione angolare della carica nei vari orbitali. Possono essere rappresentate in un grafico polare eliminando la dipendenza da $\phi$
$$|Y_{l,m}(\theta,\phi)|^{2}=\frac{1}{2\pi}|\theta_{l,m}(\theta)|^{2}$$
Facendo ciò, si ottengono i grafici della distribuzione di probabilità attorno al nucleo. Si può anche rappresentare le armoniche sferiche in forma reale: queste sono usate per mostrare la direzionalità di un legame chimico e sono autostati di $L^{2}$ e $L^{2}_{z}$, ma non $L_{z}$. Altrimenti la direzionalità della distribuzione di carica può essere mostrata mettendo in grafico il valore dell'armonica in forma reale in tutte le direzioni dello spazio.

La forma dell'orbitale è data dalla distorsione della orbitale dovuto ad un'eccitazione lungo una linea nodale. Il numero quantico $l$ determina il numero di linee nodali. Con $l=0$, non ci sono linee nodali e quindi l'orbitale non è perturbato: si tratta di dunque di una sfera. Con $l=1$, si ha una linea nodale, etc..

Il numero quantico $m$ rappresenta invece una rotazione delle linee nodali. Con $m=0$, le linee nodali sono tutte fisse. Con $m=\pm1$, una linea nodale ruota in direzione (anti)oraria. $m$ può aumentare fino a $m=\pm l$, al quale punto tutte le linee nodali ruotano nella stessa direzione.

A livello pratico, un orbitale può essere pensato come un palloncino che viene schiacciato su certe linee nodali. Il palloncino non si ingrandisce o rimpicciolisce, cambia solo forma nello spazio tridimensionale. Se schiacciato ai lati $xy$, si ingrandirà lungo l'asse $z$, formando due lobi.

Le funzioni $R(r)$ e gli autovalori di energia possono essere ricavati risolvendo l'equazione radiale
$$\left[- \frac{\hbar^{2}}{2\mu} \frac{1}{r^{2}} \frac{\partial }{\partial r}\left(r^{2}\frac{\partial }{\partial r}\right)+ \frac{\hbar^{2}l(l+1)}{2\mu r^{2}} - \frac{Ze^{2}}{4\pi\epsilon_{0}r}\right]R(r)=ER(r)$$
Sostituendo $R(r)=X(r)/r$ si ottiene
$$\left[- \frac{\hbar^{2}}{2\mu} \frac{d}{dr^{2}}+ \frac{\hbar^{2}l(l+1)}{2\mu r^{2}} - \frac{Ze^{2}}{4\pi\epsilon_{0}r}\right]u(r)=Eu(r)$$
Il potenziale effettivo è
$$V_{eff}(r)=V(r)+ \frac{l(l+1)\hbar^{2}}{2mr^{2}}=\ldots$$
per atomi idrogenoidi diventa
$$\ldots=- \frac{Ze^{2}}{4\pi\epsilon_{0}r}+ \frac{l(l+1)\hbar^{2}}{2\mu r^{2}}$$
![[Potenziale atomi idrogenoidi|70%|center]]
Allora per trovare gli autovalori $u$ dobbiamo risolvere un'equazione differenziale
$$\frac{d^{2}u_{E,l}}{dr^{2}}+ \frac{2\mu}{\hbar^{2}}[E-V_{eff}(r)]=0$$
Usiamo la sostituzione
$$\begin{cases}
\rho=\left(- \frac{8\mu E}{\hbar^{2}}\right)^{\frac{1}{2}}r \\
\lambda= \frac{Ze^{2}}{4\pi\epsilon_{0}\hbar}\left(- \frac{\mu}{2E}\right)^\frac{1}{2}
\end{cases}$$
da cui otteniamo
$$\left[\frac{d^{2}}{d \rho^{2}} - \frac{l(l+1)}{\rho^{2}} + \frac{\lambda}{\rho} - \frac{1}{4}\right]u_{E,l}(\rho)=0$$
Questa equazione ha soluzioni esponenziali $u_{E,l}(\rho)\propto e^{-\rho/2}$. Per $\rho \rightarrow \infty$, diventa una soluzione del tipo $u_{E,l}(\rho)=e^{-\rho/2}P_{e,l}(\rho)$, dove $P$ è un polinomio. Compiendo una sostituzione magica e incredibile da $u$ a $g$ (???) si trova
$$\left[\rho \frac{d^{2}}{d\rho^{2}}+\left(2l+2-\rho\right) \frac{d}{d\rho} + (\lambda - l - 1)\right]g(\rho)=0$$
le cui soluzioni sono dei [[polinomi di Laguerre]]
$$L_{q}^{p}(\rho)=\frac{d^{p}}{d\rho^{p}}L_{q}(\rho)\quad;\quad L_{q}(\rho)=e^{\rho} \frac{d^{q}}{d\rho^{q}}(\rho^{q}e^{-\rho})$$
Di fatto si giunge alla soluzione
$$R_{n,l}(r)=N_{n,l}e^{-\rho/2}L_{n+l}^{2l+1}(\rho)\text{ con }\rho=\frac{2Zr}{na_{\mu}}\text{ e }n=1,2,\ldots;\;l=0,\ldots,n-1$$
dove $a_{\mu}$ è una correzione del [[raggio di Bohr]].

La funzione d'onda risolta diventa quindi dipendente dai tre numeri quantici $n,l,m$ e ha la forma semplice
$$\Psi(r,\theta,\phi)=R_{n,l}(r)Y_{l,m}(\theta,\phi)$$
Gli autovalori di energia possono essere espressi come
$$E_{n}=-R(\mu) \frac{Z^{2}}{n^{2}}=- \frac{\mu}{m}R_{\infty} \frac{Z^{2}}{n^{2}}$$
dove $R_{\infty}$ è la [[costante di Rydberg]]. Si nota che sono presenti stati discreti infiniti e che si infittiscono per $n \rightarrow \infty$ quando il potenziale Coulombiano tende a zero. Gli stati risultano degeneri in $l$ ed $m$. La degenerazione dei livelli è data da
$$d=\underbrace{2}\limits_{m_{s}}\sum\limits_{l=0}^{n-1}\underbrace{2l+1}\limits_{m}=2n^{2}$$
che racchiude tutti i numeri quantici: abbiamo che $l$ varia da $0$ a $n-1$, per ogni $l$ sono possibili $2l+1$ valori di $m$ e tutto è possibile per entrambi i numeri di [[spin]] $m_{s}=\pm\frac{1}{2}$.