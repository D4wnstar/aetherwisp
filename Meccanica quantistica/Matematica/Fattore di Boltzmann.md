Il **fattore di Boltzmann** è un termine che compare in meccanica statistica. Vale
$$e^{-\beta E}$$
con $\beta$ la **temperatura inversa**
$$\beta=\frac{1}{k_{B}T}$$
e $k_{B}$ la [[Boltzmann constant]]. $E$ è l'energia del sistema, generalmente descritta come il valore dell'[[Hamiltoniana]] $E=H(q,p)$. In questo caso, abbiamo
$$e^{-\beta H(q,p)}$$
### Oscillatore armonico
Nel caso dell'[[oscillatore armonico]], l'Hamiltoniana vale
$$H(q,p)=\frac{p^{2}}{2m}+ \frac{m\omega ^{2}}{2}q^{2}$$
con $m$ massa della [[particella]] e $\omega$ la frequenza angolare. Allora il fattore di Boltzmann è
$$e^{-\beta((p^{2}/2m) + (m\omega^{2}/2)q^{2})}$$
Integrando su posizione e momento troviamo il valore di normalizzazione
$$\begin{align}
Z_{\beta}=& \int_{-\infty}^{\infty}  \, dq \int_{-\infty}^{\infty} \exp\left( -\beta\left( \frac{p^{2}}{2m}+ \frac{m\omega^{2 }}{2}p^{2} \right) \right) \, dp= \\
=& \int_{-\infty}^{\infty} \exp\underbrace{ \left( \frac{-\beta m\omega^{2}}{2}q^{2} \right) }_{ -x^{2} } \, dq\int_{-\infty}^{\infty} \exp\underbrace{ \left( \frac{-\beta p^{2}}{2} \right) }_{ -y^{2} } \, dp = \\
=& \int_{-\infty}^{\infty} \exp(-x^{2}) \, dx \int_{-\infty}^{\infty} \exp(-y^{2}) \, dy\sqrt{ \frac{2}{bm\omega ^{2}} }\sqrt{ \frac{2m}{\beta} }= \\
=& \frac{2\pi}{\beta \omega}
\end{align}$$
dove $Z_{\beta}$ è la [[funzione di partizione]]. Il fattore di Boltzmann normalizzato è una densità di [[stato|stati]]
$$\rho_{\beta}(q,p)\equiv \frac{\exp\left( -\beta\left( \frac{p^{2}}{2m}+ \frac{m\omega ^{2}}{2}p^{2} \right) \right)}{Z_{\beta}}$$
detto [[stato di Gibbs]].

L'energia nello stato $\beta$ è il valor medio dell'Hamiltoniana in quello stato:
$$\begin{align}
\langle H \rangle_{\beta}&=\frac{1}{Z_{\beta}}\int_{-\infty}^{\infty}  \, dq \int_{-\infty}^{\infty} He^{-\beta H} \, dp   \\
&=\frac{\beta \omega}{2\pi}\int_{-\infty}^{\infty}  \, dq \int_{-\infty}^{\infty} \left( \frac{p^{2}}{2m}+ \frac{m\omega^{2}}{2}q^{2} \right)\exp\left( -\beta\left( \frac{p^{2}}{2m}+ \frac{m\omega ^{2}}{2}p^{2} \right) \right) \, dp \\
&=\frac{\beta \omega}{2\pi}\left( \int_{-\infty}^{\infty}  \, \exp\left( \frac{-\beta m\omega ^{2}}{2}q^{2} \right)\, dq\int_{-\infty}^{\infty} \frac{p^{2}}{2m}\exp\left( \frac{-\beta p^{2}}{2m} \right) \, dp \int_{-\infty}^{\infty} \exp\left( \frac{-\beta p^{2}}{2m} \right) \, dp   \right) \\
&=\frac{\beta \omega}{2\pi}\left( \sqrt{ \frac{2\pi}{m\omega ^{2}\beta} } \int_{-\infty}^{\infty} \frac{p^{2}}{2m}\exp\left( \frac{-\beta p^{2}}{2m} \right) \, dp+\sqrt{ \frac{2\pi m}{\beta} }\int_{-\infty}^{\infty} \frac{m\omega ^{2}}{2}q^{2}\exp\left( \frac{-\beta m\omega ^{2}}{2}q^{2} \right) \, dq  \right) \\
&=\frac{\beta \omega}{2\pi}\left( \sqrt{ \frac{2\pi}{m\omega ^{2}\beta} } \frac{1}{\beta} \sqrt{ \frac{2m}{\beta} }\int_{-\infty}^{\infty} y^{2}e^{-y^{2}} \, dy +\sqrt{ \frac{2\pi m}{\beta} } \frac{1}{\beta}\sqrt{ \frac{2}{m\omega ^{2}\beta} }\int_{-\infty}^{\infty} x^{2}e^{-x^{2}} \, dx  \right)
\end{align}$$
Risolviamo gli integrali separatamente
$$I=\int_{-\infty}^{\infty} y^{2}e^{-y^{2}} \, dy=\ldots$$
Possiamo usare la [[funzione gamma]]
$$\Gamma(z)=\int_{-\infty}^{\infty} t^{z-1}e^{-t} \, dt $$
con $z$ complesso e $t$ reale. Vale $t^{z-1}=t^{x-1+iy}=t^{x-1}t^{iy}$. Il problema è il termine con l'esponenziale reale $t^{x-1}$, che può divergere, quindi deve essere strettamente positivo. Possiamo anche sfruttare il fatto che la funzione sia pari per cambiare il dominio di integrazione
$$\ldots=2\int_{0}^{\infty }y^{2}e^{-y^{2}}dy=\int_{0}^{\infty}ye^{-y^{2}}d(y^{2})=\int_{0}^{\infty}\sqrt{ t }e^{-t}\, dt=\Gamma\left( \frac{3}{2} \right)=\ldots$$
e usando $\Gamma(z+1)=z\Gamma(z)$ abbiamo
$$\ldots=\frac{1}{2 }\Gamma\left( \frac{1}{2} \right)=\frac{\sqrt{ \pi }}{2}$$
usando che $\Gamma\left( \frac{1}{2} \right)=\sqrt{ \pi }$. Tornando all'energia
$$\langle H \rangle _{\beta}=\frac{\beta \omega}{2\pi}\left( \frac{\pi}{\beta ^{2}\omega}+ \frac{\pi}{\beta ^{2}\omega} \right)=\frac{1}{\beta}=k_{B}T$$
### Catastrofe ultravioletta
Da qui possiamo derivare l'energia associata ad una certa temperatura
$$E(T)=\int_{0}^{\infty} \frac{\omega ^{2}}{2\pi ^{2}c^{3}}\langle H_{\omega} \rangle_{\beta}\, d\omega=k_{B}T\int_{0}^{\infty} \frac{\omega ^{2}}{2\pi ^{2}c^{3}}\,d\omega=+\infty$$
Purtroppo l'integrale diverge, quindi è impossibile integrare l'energia per alte frequenze. Questo fatto, chiaramente falso dato che in energia le alte frequenze esistono senza divergere, è detto **catastrofe ultravioletta**. La soluzione è venuta originariamente da Planck modificando l'espressione dell'energia media dello stato affermando che gli stati di energia non sono in realtà continui, bensì discreti e pesati da una nuova costante $h$:
$$E_{n}=h\nu n=\hbar \omega n,\quad n=0,1,2,\ldots,\quad \hbar=\frac{h}{2\pi}$$
L'integrale dunque diventa una [[serie]], in particolare una [[serie geometrica]]:
$$\sum_{h=0}^{\infty}e^{-\beta h\omega n}=\frac{1}{1-e^{-\beta h\omega}}=Z_{\beta}$$
La costante $h$ è detta [[costante di Planck]] e $\hbar$ è la [[Costante di Planck|forma ridotta]]. Il calcolo del valor medio diventa dunque
$$\begin{align}
\langle H_{\omega} \rangle _{\beta}&=(1-e^{-\beta \hbar \omega})\sum_{n=0}^{\infty} \hbar \omega ne^{-\beta \hbar \omega n} \\
&=\hbar \omega(1-e^{-\beta \hbar \omega n})\sum_{n=0}^{\infty} ne^{-\beta \hbar \omega n} \\
&=(1-e^{-\beta \hbar \omega n})\frac{ \partial  }{ \partial \beta } \sum_{n=0}^{\infty} e^{-\beta \hbar \omega n} \\
&=-(1-e^{-\beta \hbar \omega n})\frac{ \partial }{ \partial \beta } \frac{1}{1-e^{-\beta \hbar \omega}} \\
&=\frac{\hbar\omega e^{-\beta \hbar \omega}}{1-e^{-\beta \hbar \omega}} \\
&=\frac{\hbar\omega}{e^{\beta \hbar \omega-1}}
\end{align}$$
Allora tornando all'energia per temperatura si ha
$$E(T)=\int_{0}^{\infty} \frac{\hbar\omega ^{3}}{2\pi ^{2}c^{3}} \frac{1}{e^{\beta \hbar \omega}-1}$$
La seconda frazione è approssimabile con una [[Polinomio di Taylor|serie di Taylor]] come
$$\frac{1}{e^{\beta \hbar \omega}}\simeq\begin{cases}
e^{-\beta \hbar \omega}\quad &\omega\gg 1 \\
\frac{1}{\beta \hbar \omega}\quad &\omega\ll 1
\end{cases}$$
quindi per frequenze molto, si trova un decadimento esponenziale che risolve automaticamente la divergenza catastrofica.