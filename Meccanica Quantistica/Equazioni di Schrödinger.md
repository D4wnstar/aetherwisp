L'**equazione di Schrödinger** astratta è
$$i\hbar\partial_{t}|\psi_{t}\rangle=\hat{H}|\psi_{t}\rangle\quad;\quad |\psi_{t=0}\rangle=|\psi\rangle\mbox{ condizione iniziale}$$
Prendiamo l'[[Hamiltoniana]] di una particella libera
$$H(\bar{q},\bar{p})= \frac{\bar{p}^{2}}{2m}=\frac{1}{2m}(p_{x}^{2}+p_{y}^{2}+p_{z}^{2})$$
e il suo operatore associato
$$\hat{H}=\frac{\hat{\bar{p}}^{2}}{2m}=\frac{1}{2m}(\hat{p}^{2}_{x}+\hat{p}^{2}_{y}+\hat{p}^{2}_{z})$$
Vogliamo risolvere l'equazione di Schrodinger.

## Rappresentazione dei momenti
Usiamo la rappresentazione dei momenti, con $|r\rangle=|x,y,z\rangle$.
$$\hat{\bar{p}}|\bar{p}\rangle=\bar{p}|\bar{p}\rangle$$
$$\langle x|p\rangle=\frac{e^{\frac{i}{\hbar}px}}{(\sqrt{2\pi\hbar})^{3}}\mbox{ in una dimensione}$$
$$\langle \bar{r}|\bar{p}\rangle= \frac{e^{\frac{i}{\hbar}\bar{p}\cdot\bar{r}}}{(\sqrt{2\pi\hbar})^{3}}\mbox{ in tre dimensioni}$$
Sostituiamo nell'equazione
$$i\hbar\partial_{t}\langle \bar{p}|\psi_{t}\rangle=\langle \bar{p}|\hat{H}|\psi_{t}\rangle=\langle \hat{H}\bar{p}|\psi_{t}\rangle=\frac{\bar{p}^{2}}{2m}\langle \bar{p}|\psi_{t}\rangle$$
allora
$$i\hbar\partial_{t}\tilde{\psi}_{t}(\bar{p})=\frac{\bar{p}^{2}}{2m}\tilde{\psi}_{t}(\bar{p})$$
risolvendo la differenziale
$$\tilde{\psi}_{t}(\bar{p})=e^{- \frac{\frac{i}{\hbar}p^{2}}{2m}t}\tilde{\psi}(\bar{p})$$
con $\tilde{\psi}(\bar{p})$ la condizione iniziale, dipendente solo dal momento.

Prendiamo per esempio
$$\psi(x)= \begin{cases}
\frac{1}{\sqrt{(\Delta)}}\mbox{ se }x\in\Delta  \\
0\mbox{ altrimenti }
\end{cases}$$
la funzione scalino in $\Delta$ *normalizzata*.
$$P_{\psi}^{\hat{A}}(a_{i})=|\langle a_{i}|\psi\rangle|^{2}$$
che è una probabilità. Vale anche
$$P_{\psi}^\hat{x}(x)=|\langle x|\psi\rangle|^{2}$$
che è una *densità di probabilità*. Integrando su di essa su un intervallo, troviamo la probabilità di trovare $x$ nell'intervallo $\Delta$ partendo da un sistema preparato nello stato $\psi$:
$$\int_{\Delta}|\langle x|\psi\rangle|^{2}dx=P_{\Delta}(\hat{x}|\psi)$$
dove $P_{\Delta}(\hat{x}|\psi)$ è la *probabilità condizionata* di $\hat{x}$ da $\psi$. In rappresentazione dei momenti vale
$$P_{\psi}^{\hat{p}}(p)=|\langle p|\psi\rangle|^{2}=|\tilde{\psi}(p)|^{2}$$
e, analogamente, integrando
$$\int_{\tilde{\Delta}}|\tilde{\psi}(p)|^{2}dp=P_{\tilde{\Delta}}(\hat{p}|\psi)$$
Se invece prendo un operatore $\hat{A}$, esso ha un numero finito di autovalori $a_{i}$ 
$$\hat{A}=\sum\limits_{i=1}^{\infty}a_{i}|a_{i}\rangle\langle a_{i}|$$
Come prima, vogliamo trovare la probabilità di trovare gli autovalori in un certo intervallo $\Delta_{A}$, che ora però è *discreto*.
$$\Delta_{A}=\{a_{k},\ldots,a_{k+N}\}$$
Dunque la probabilità discreta sarà
$$P_{\Delta_{A}}(\hat{A}|\psi)=\sum\limits_{j=0}^{N}|\langle a_{k+j}|\psi\rangle|^{2}=\langle \psi|\left( \sum\limits_{j=0}^{N}\hat{P}^{\hat{A}}_{a_{k+j}}\right)\psi\rangle$$
Ora prendiamo un secondo intervallo $\Delta'=a'-b'$. Partendo dalla rappresentazione dei momenti $\tilde{\psi}(\bar{q})$, che è più naturale dato che la [[Hamiltoniana]] è funzione dei momenti, dobbiamo fare l'[[antitrasformata]] per tornare alla rappresentazione delle posizioni $\psi(\bar{r})$ 
$$\psi_{t}(\bar{r})= \frac{1}{(\sqrt{2\pi\hbar})^{3}}\int_{\mathbb{R}^{3}}d \bar{p}e^{\frac{i}{\hbar}\bar{p}\cdot\bar{r}}\tilde{\psi}_{t}(\bar{p})=\frac{1}{(\sqrt{2\pi\hbar})^{\frac{3}{2}}}\int_{\mathbb{R}^{3}}d \bar{p}e^{\frac{i}{\hbar}\bar{p}\cdot\bar{r}}e^{-\frac{i}{\hbar} \frac{p^{2}}{2m}t}\tilde{\psi}(\bar{p})=$$
$$=\frac{1}{(2\pi\hbar)^{3}}\int_{\mathbb{R}^{3}}d\bar{p}\int_{\mathbb{R}^{3}}d\bar{q}e^{\frac{i}{\hbar}\bar{p}(\bar{r}-\bar{q})- \frac{i}{\hbar} \frac{p^{2}}{2m}t}\psi(\bar{q})=\int_{\mathbb{R}^{3}}d\bar{p}\left(\int_{\mathbb{R}^{3}}d\bar{q}\frac{e^{\frac{i}{\hbar}\bar{p}(\bar{r}-\bar{q})- \frac{i}{\hbar} \frac{p^{2}}{2m}t}}{(2\pi\hbar)^{3}}\right)\psi(\bar{q})=\ldots$$
che è un [[integrale di Fresnel]]. Allora risolvendolo per ogni dimensione
$$I_{x}=\int_{\mathbb{R}}dp_{x}e^{\frac{i}{\hbar}p_{x}(r-q_{x})- \frac{i}{\hbar} \frac{p_{x}^{2}}{2m}t}=\int_{\mathbb{R}}dp_{x}e^{\frac{i}{\hbar} \frac{t}{2m} \left( p^{2}_{x}- 2 \frac{m}{t}p_{x}(x-q_{x})+ \frac{m^{2}}{t^{2}}(x-q_{x})^{2} \right)}=$$
$$=\frac{e^{\frac{i}{\hbar}{\frac{m}{2t}(x-q_{x})^{2}}}}{2\pi\hbar} \int_{\mathbb{R}}dp_{x} e^{- \frac{it}{2\hbar m}(p_{x}- \frac{m}{t}(x-q_{x}))^{2}}=\ldots$$
che è un integrale Gaussiano, che possiamo risolvere con il teorema dei residui
$$\ldots=\frac{e^{\frac{i}{\hbar}{\frac{m}{2t}(x-q_{x})^{2}}}}{2\pi\hbar}\sqrt{\frac{2\hbar m\pi}{it}}$$
Riunendo le tre dimensioni
$$\psi_{t}(\bar{r})=\int d\bar{q} U_{r}(\bar{r},\bar{q})\psi_{r}(\bar{q})\mbox{ con }U_{r}(\bar{r},\bar{q})=I_{x}I_{y}I_{z}$$
$U_{t}(\bar{r},\bar{q})$ si chiama **propagatore libero**, perché prende la funzione al tempo 0 e la propaga al punto $\bar{r}$ al tempo $t$, quindi la propaga sia nel tempo che nello spazio. Il "libero" viene dal fatto che usa la *dinamica libera* dell'Hamiltoniana.

## Rappresentazione delle posizioni
Ora parto invece dalla rappresentazione delle posizioni
$$i\hbar\partial_{t}|\psi_{t}\rangle= \frac{\hat{\bar{p}}^{2}}{2m}|\psi_{t}\rangle\quad;\quad |\psi_{t=0}\rangle=|\psi\rangle$$
$$i\hbar\partial_{t}(\bar{r})=\frac{1}{2m}\langle \bar{r}|\hat{\bar{p}}^{2}|\psi_{t}\rangle=\frac{1}{2m}\langle \bar{r}|\hat{\bar{p}}\cdot\hat{\bar{p}}|\psi_{t}\rangle=\frac{1}{2m}\langle \bar{r}|(\hat{p}^{2}_{x}+\hat{p}^{2}_{y}+\hat{p}^{2}_{z})|\psi_{t}\rangle$$
Usando il Laplaciano
$$- \frac{\hbar^{2}}{2m}\overline{\nabla}^{2}\psi_{t}(\bar{r})=i\hbar\partial_{t}\psi_{t}(\bar{r})$$
Per essere risolta dobbiamo fare la [[trasformata di Fourier]], poi tornare indietro con l'antitrasformata, quindi torneremmo comunque dov'eravamo prima nella rappresentazione dei momenti, quindi non conviene.

## Autoaggiuntezza di $\hat{x}$, $\hat{p}$
$$\langle \phi|\hat{x}\psi\rangle=\langle \phi|\hat{x}\left( \int_{\mathbb{R}}dx |x\rangle\langle x| \right)\psi\rangle=\langle \phi|\int_{\mathbb{R}}dx x |x\rangle\langle x| \psi\rangle$$
con $\hat{x}:L^{2}(\mathbb{R})\rightarrow L^{2}(\mathbb{R})$ [[Operatore autoaggiunto|autoaggiunto]]
Nel caso dei momenti $\hat{p}$ 
$$\langle \phi|\hat{p}\psi\rangle=\int_{\mathbb{R}}dx \phi^{\ast}(x)(-i\hbar\partial_{x}\psi(x))=\int_{-\infty}^{\infty}dx(-i\hbar\partial_{x}\phi(x))^{\ast}\cdot\psi(x)=\langle \hat{p}\phi^{\ast}|\psi\rangle$$
Avremmo anche potuto usare la completezza dei [[Proiettore|proiettori]] come sopra.
