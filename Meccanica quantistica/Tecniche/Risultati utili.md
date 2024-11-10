## Matematica
### Equazione di Schrödinger e funzione d'onda
Equazione di Schrödinger dipendente dal tempo:
$$i\hbar \partial_{t} |\Psi\rangle=\hat{H}|\Psi\rangle=- \frac{\hbar^{2}}{2m} \frac{\partial ^{2}}{\partial x^{2}}|\Psi\rangle+V |\Psi\rangle$$
Indipendente dal tempo:
$$\hat{H}\ket{\psi} =E\ket{\psi} $$
$$- \frac{\hbar^{2}}{2m} \frac{ \partial ^{2}  }{ \partial x^{2} } \psi(x) + V(x)\psi(x)=E\psi(x)$$
Se $V(x)$ è pari, allora $\psi(x)$ è o pari o dispari. Caso dipendente da quello indipendente per spettro discreto di energie $\{ E_{n} \}$ e autostati $\{ \Psi_{n} \}$:
$$\Psi(q,t)=\sum\limits_{n=1}^{\infty}c_{n}\psi_{n}(q)e^{iE_{n}t/\hbar}=\sum\limits_{n=1}^{\infty}c_{n}\Psi_{n}(q,t)$$
In coordinate sferiche
$$- \frac{\hbar^{2}}{2m}\left[\frac{1}{r^{2}}\frac{\partial }{\partial r}\left(r^{2}\frac{\partial \psi}{\partial r}\right)+ \frac{1}{r^{2}\sin\theta}\frac{\partial }{\partial \theta}\left(\sin\theta \frac{\partial \psi}{\partial \theta}\right)+ \frac{1}{r^{2}\sin^{2}\theta}\left(\frac{\partial ^{2}\psi}{\partial \phi^{2}}\right)\right] + V\psi=E\psi$$
La probabilità di misurare un certo autostato $|\phi\rangle$ al tempo $t$ è
$$P_{\psi_{t}}(\phi)=|\langle \phi|\psi_{t}\rangle|^{2}$$
### Equazioni di Heisenberg
Generale
$$\frac{d}{dt}\hat{A}(t)=\frac{i}{\hbar}[\hat{H},\hat{A}(t)]$$
Per posizione e momento
$$\frac{d\hat{q}_{t}}{dt}=\frac{i}{\hbar}[\hat{H},\hat{q}_{t}]\quad;\quad\frac{d \hat{p}_{t}}{dt}=\frac{i}{\hbar}[\hat{H},\hat{p}_{t}]$$
### Disuguaglianza di Heisenberg
In posizione e momento
$$\Delta \hat{q}\Delta \hat{p}\geq \frac{\hbar}{2}$$
In più dimensioni vale solo nella stessa componente. Componenti diversi commutano.
Caso generale tra due operatori autoaggiunti $\hat{A}$ e $\hat{B}$:
$$\Delta \hat{A}\Delta \hat{B}\geq -\frac{1}{4} \left(\bra{\psi} [\hat{A},\hat{B}]\ket{\psi} \right)^{2}$$
In tempo ed energia
$$\Delta E \Delta t\geq \frac{\hbar}{2}$$
### Operatori
In una dimensione
$$\hat{q}=q, \quad \hat{p}= -i\hbar \partial_{x} , \quad\hat{H}=- \frac{\hbar^{2}}{2m} \partial_{x} ^{2}+V(q)$$
In tre dimensioni
$$\hat{\mathbf{q}}=\mathbf{q}, \quad \hat{\mathbf{p}}=\frac{\hbar}{i}\nabla, \quad \hat{H}=- \frac{\hbar^{2}}{2m}\nabla^{2}+V(\vec{r})$$
Evolutore
$$\hat{U}_{t}=\exp\left(- i \frac{\hat{H}}{\hbar} t\right)=\sum\limits_{i=1}^{\infty}e^{- \frac{i}{\hbar}E_{i}t}|E_{i}\rangle\langle E_{i}|$$
da cui
$$|\psi_{t}\rangle=\hat{U}_{t}|\psi\rangle \text{ (Schrödinger picture)},\qquad\hat{Q}_{t}=\hat{U}_{t}^{+}\hat{Q}\hat{U}_{t} \text{ (Heisenberg picture)}$$
Propagatore
$$\bra{x} \hat{U}_{t}\ket{y} $$
Generatore di traslazioni di momento
$$\hat{U}_{p_{0}}=e^{-ip_{0}\hat{q}/\hbar}$$
tale che
$$\hat{U}_{p_{0}}^{+}\hat{p}\hat{U}_{p_{0}}=e^{ip_{0}\hat{q}/\hbar}\hat{p}e^{-ip_{0}\hat{q}/\hbar}=\hat{p}+ \frac{i}{\hbar}p_{0}[\hat{q},\hat{p}]=\hat{p}-p_{0}$$
Se $|\psi_{E}\rangle$ è un autostato di $H$ con autovalore $E$
$$|\psi_{E,t}\rangle=\hat{U}_{t}|\psi_{E}\rangle=e^{-iEt/\hbar}|\psi_{E}\rangle$$
Decomposizione spettrale di un qualunque operatore $T$ in una base ortonormale $\{\psi_{n}\}$
$$T=\sum\limits_{n}t_{n}|\psi_{n}\rangle \langle \psi_{n}|=\sum\limits_{n}t_{n}\hat{P}_{\psi_{n}}$$
dove deve valere
$$T\ket{\psi_{n}} =t_{n}\ket{\psi_{n}} $$
In genere è la base di autostati di un operatore, come l'Hamiltoniana. Se l'operatore modifica l'autostato (come quelli di creazione/distruzione) del tipo
$$T \ket{\psi_{n}^{(i)}} =t_{n}\ket{\psi_{n}^{(j)}} $$
allora
$$T=\sum\limits_{n}t_{n}|\psi_{n}^{(j)}\rangle \langle \psi_{n}^{(i)}|$$
La rappresentazione matriciale in questo caso è data dagli "autovalori" $t_{n}$ nella cella $ij$, indicizzando righe e colonne in base al numero quantico cambiato. Per esempio, per l'operatore $\hat{L}_{+}$, vale $\hat{L}_{+}\ket{1,0}=\sqrt{ 2 }\hbar \ket{1,1}$. Allora nella forma matriciale, $\hat{L}_{+}$ avrà $\sqrt{ 2 }\hbar$ nella cella $(0,1)$, dove righe e colonne sono indicizzate come $-1,0,1$ perché è il numero quantico magnetico di spin per spin 1.
### Commutatori
Identità utili
$$[A+B,C]=[A,C]+[B,C],\qquad[AB,C]=ABC-CAB,\qquad[A,A]=0$$
$$[A,B]=-[B,A],\qquad[A,B]^{+}=-[A,B]$$
Commutatori annidati con $\hat{B}$ contenente $\hat{A}$
$$f(\hat{B})^{+}\hat{A}f(\hat{B})=e^{-\hat{B}}\hat{A}e^{\hat{B}}=\hat{A}+[-\hat{B},\hat{A}]$$
Posizione/momento
$$[q_{i},p_{j}]=-[p_{i},q_{j}]=i\hbar\delta_{ij}, \quad [q_{i},q_{j}]=[p_{i},p_{j}]=0$$
La posizione commuta sempre con la posizione; la quantità di moto commuta sempre con la quantità di moto; tra di loro commutano solo in coordinate diverse, altrimenti si ha $i\hbar$. Due coordinate possono identificarsi come posizione e momento se il loro commutatore è $i\hbar$.
$$[\hat{q},\hat{p}]=i\hbar; \quad [\hat{H},\hat{q}]=- \frac{i\hbar}{m}\hat{p}; \quad [\hat{H},\hat{p}]=0$$
Se $[\hat{H},\hat{Q}]=0$, allora $\hat{Q}$ è una costante del moto.

Operatori relativi a gradi di libertà differenti commutano sempre. Per esempio, $[\vec{J},\vec{S}]$ o $[\vec{J},\vec{L}]$.
### Proiettori
Autoaggiunti, traccia unitaria, autovalori 0 e 1.
$$\hat{P}_\psi=|\psi\rangle\langle\psi| \quad ; \quad \hat{P}_{\psi}|\phi\rangle=\langle\psi|\phi\rangle|\psi\rangle$$
Presa una base ortonormale ${|i\rangle}_{i\in\mathbb{N}}$, il proiettore dà l'$i$-esimo coefficiente di Fourier (i.e. la componente $i$-esima) di un ket
$$\hat{P}_{i}|\phi\rangle=|i\rangle\langle i|\phi\rangle=|\phi_{i}\rangle$$
e se stesso se proiettato su se stesso
$$\hat{P}_{\psi}|\psi\rangle=\langle \psi|\psi\rangle|\psi\rangle=|\psi\rangle$$
Relazione di completezza (discreta e continua)
$$\sum\limits_{i=1}^{n}\hat{P}_{\psi_{i}}=\hat{\mathbf{1}} \quad ; \quad \int_{-\infty}^{+\infty}|e_{z}\rangle\langle e_{z}|dz=\hat{\mathbf{1}}$$
Idempotenza
$$\hat{P}^{2}=\hat{P}$$
Tutti gli operatori idempotenti hanno come unici autovalori 0 e 1. Infatti
$$T |\psi\rangle=t |\psi\rangle , \quad T^{2}=T$$
implica
$$t |\psi\rangle=T |\psi\rangle=TT |\psi\rangle=Tt |\psi\rangle=tT |\psi\rangle=t^{2}|\psi\rangle \quad \Rightarrow \quad t=t^{2} \quad \Rightarrow \quad t=0,1$$
### Matrici di Pauli
Forma standard:
$$\hat{\sigma}_{x}=\begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix},\;\hat{\sigma}_{y}=\begin{pmatrix}0 & -i \\ i & 0\end{pmatrix},\;\hat{\sigma}_{z}=\begin{pmatrix}1 & 0 \\ 0 & -1\end{pmatrix}$$
tutte con autovalori $\pm1$. Sono autoaggiunte: $\hat{\sigma}_{i}^{\dagger}=\hat{\sigma}_{i}$. I quadrati sono unitari: $\hat{\sigma}_{i}^{2}=\hat{\mathbf{1}}$. Gli autovettori sono
$$x_{+}: \frac{1}{\sqrt{2}}\begin{pmatrix}1 \\ 1\end{pmatrix}, \quad x_{-}: \frac{1}{\sqrt{2}}\begin{pmatrix}1 \\ -1\end{pmatrix}$$
$$y_{+}: \frac{1}{\sqrt{2}}\begin{pmatrix}1 \\ i\end{pmatrix}, \quad y_{-}: \frac{1}{\sqrt{2}}\begin{pmatrix}1 \\ -i\end{pmatrix}$$
$$z_{+}: \begin{pmatrix}1 \\ 0\end{pmatrix}, \quad z_{-}: \begin{pmatrix}0 \\ 1\end{pmatrix}$$
Vale
$$\sigma_{x}|\uparrow\,\rangle=|\downarrow\;\rangle, \quad \sigma_{x}|\downarrow\;\rangle=|\uparrow\;\rangle$$
### Matrice di Hadamard
$$U= \frac{1}{\sqrt{2}}\begin{pmatrix}1 & 1 \\ 1 & -1\end{pmatrix}=(|\uparrow x\;\rangle |\downarrow x\;\rangle)$$
### Matrice di densità
$$\hat{\rho}=\begin{pmatrix}\rho & \sigma \\ \sigma^{*} & 1-\rho\end{pmatrix}$$
dove $\rho\in[0,1]$ e $\sigma\in\mathbb{C}$. Ha traccia unitaria, è autoaggiunta.
### Prodotto tensoriale
$$v\otimes w=\begin{pmatrix}v_{1}\\ v_{2}\end{pmatrix}\otimes\begin{pmatrix}w_{1} \\ w_{2}\end{pmatrix}=\begin{pmatrix}v_{1} & \begin{pmatrix}w_{1} \\ w_{2}\end{pmatrix} \\ v_{2} & \begin{pmatrix}w_{1} \\ w_{2}\end{pmatrix}\end{pmatrix}=\begin{pmatrix}v_{1}w_{1} \\ v_{1}w_{2} \\ v_{2}w_{1} \\ v_{2}w_{2}\end{pmatrix}$$
### Momento angolare
$$\hat{L}_{x}=\frac{\hbar y}{i}\frac{\partial }{\partial z}- \frac{\hbar z}{i}\frac{\partial }{\partial y}, \quad \hat{L}_{y}=\frac{\hbar z}{i}\frac{\partial }{\partial x}- \frac{\hbar x}{i}\frac{\partial }{\partial z}, \quad \hat{L}_{z}=\frac{\hbar x}{i}\frac{\partial }{\partial y}- \frac{\hbar y}{i}\frac{\partial }{\partial x}$$
Tutto il seguente vale anche per spin sostituendo $L$ con $S$ ed $l$ con $s$.
$$[L_{x},L_{y}]=i\hbar L_{z}, \quad [L_{y},L_{z}]=i\hbar L_{x}, \quad [L_{z},L_{x}]=i\hbar L_{y}$$
$$[L^{2},L_{z}]=0; \quad L^{2}=\hbar^{2}l(l+1)$$
$$L^{2}\ket{lm} =\hbar^{2}l(l+1)\ket{lm} , \quad L_{z}\ket{lm} =\hbar m\ket{lm} $$
$$l=0,\;1/2,\;1,\;3/2,\;2,\ldots\quad; \quad m=-l,-l+1,\ldots,0,\ldots,l-1,l$$
Gli autovalori sono $\hbar m$. Operatori di innalzamento e abbassamento
$$L_{\pm}\equiv L_{x}\pm iL_{y}$$
$$L_{\pm}|sm\rangle=\hbar\sqrt{l(l+1)-m(m\pm1)}|l(m\pm1)\rangle$$
$$L^{2}=L_{\pm}L_{\mp}+L^{2}_{z}\mp\hbar L_{z},\quad L_{x}=\frac{L_{+}+L_{-}}{2},\quad L_{y}=\frac{L_{+}-L_{-}}{2i}$$
Gli autovalori sono gli stessi per tutte le componenti $L_{x}$, $L_{y}$ e $L_{z}$. Infatti, sono gli stessi per qualunque direzione arbitraria $\hat{\mathbf{n}}$ come momento $\hat{\mathbf{L}}\cdot \hat{\mathbf{n}}$, dato che $[L^{2},\hat{\mathbf{L}}\cdot \hat{\mathbf{n}}]=0$.
### Spin
Per spin 1/2
$$\hat{\mathbf{S}}=\frac{\hbar}{2}\hat{\boldsymbol{\sigma}}$$
con $\hat{\boldsymbol{\sigma}}=(\hat{\sigma}_{x},\hat{\sigma}_{y},\hat{\sigma}_{z})$ le matrici di Pauli.
$$\mathbf{S}_{+}|\downarrow\;\rangle=\hbar |\uparrow\;\rangle, \quad \mathbf{S}_{-}|\uparrow\;\rangle=\hbar |\downarrow\;\rangle, \quad \mathbf{S}_{+}|\uparrow\;\rangle=\mathbf{S}_{-}|\downarrow\;\rangle=0$$

La somma di spin in un sistema a due particelle con spin $s_{1}$ e $s_{2}$ è tra $|s_{1}-s_{2}|$ e $s_{1}+s_{2}$, a passi interi. Per una coppia di due particelle con $s=1/2$ è 0 o 1.
### Momento angolare totale
$$\vec{J}=\vec{L}+\vec{S}, \quad [\vec{J},\vec{L}]=0, \quad [\vec{J},\vec{S}]=0$$
$$J^{2}|jm_{j}\rangle=\hbar^{2}j(j+1)|jm_{j}\rangle,\quad J_{z}|jm_{j}\rangle=\hbar m_{j}|jm_{j}\rangle$$
### Rappresentazioni di stato
Posizione e momento di uno stato $\ket{\psi_{t}}$
$$\psi_{t}(x)=\langle x|\psi_t\rangle,\qquad \psi_{t}(p)=\braket{ p | \psi_{t} } $$
### Rappresentazioni di evoluzione
Di Schrödinger (con equazione di Schrödinger)
$$|\psi_{t,S}\rangle=U_{t}|\psi\rangle$$
Di Heisenberg (con equazione di Heisenberg)
$$\hat{A}_{t,H}=U_{t}^{+}\hat{A}U_{t}$$
Di interazione
$$H_{I}=H_{0}+H_{1}; \quad i\hbar \partial_{t} |\psi_{I}(t)\rangle=H_{I}(t)|\psi_{I}(t)\rangle$$
dove
$$|\psi_{I}(t)\rangle=U_{t,0}^{+}|\psi_{S}(t)\rangle; \quad \hat{A}_{I}(t)=U_{t,0}^{+}\hat{A}_{S}(t)U_{t,0}$$
### Armoniche sferiche
Le prime armoniche sferiche sono
$$Y_{0}^{0}=\sqrt{\frac{1}{4\pi}};\quad Y_{1}^{0}=\sqrt{\frac{3}{4\pi}}\cos\theta;\quad Y_{1}^{\pm1}=\mp\sqrt{\frac{3}{8\pi}}\sin\theta e^{\pm i\phi}$$
e sono ortonormali fra loro
$$\int_{0}^{2\pi}\int_{0}^{\pi}(Y_{l}^{m})^{*}Y_{l'}^{m'}\sin\theta d\theta d\phi=\langle Y_{l}^{m}|Y_{l'}^{m'}\rangle=\delta_{mm'}\delta_{ll'}$$
Vale che
$$\int_{0}^{\pi}(Y_{l}^{m})^{*}Y_{l'}^{m'}\sin\theta d\theta d\phi=0$$
per ogni $(l,m)\neq(0,0)$. Per $(l,m)=(0,0)$ l'integrale vale $2\sqrt{\pi}$. Infatti, $2\sqrt{\pi}\langle Y_{0}^{0}|Y_{l}^{m}\rangle=0$ per ortogonalità.

La dipendenza angolare di uno stato $\psi$ in un sistema sferico si trova come
$$\langle Y_{l}^{m}|\psi(r,\theta,\phi)\rangle$$
### Stati coerenti
Autostati $\ket{z}$ dell'operatore di distruzione $\hat{a}\ket{z}=z\ket{z}$
$$|z_{t}\rangle=\hat{U}_{t}|z\rangle=e^{-|z|^{2}/2}\sum\limits_{k=0}^{\infty} \frac{z^{k}}{\sqrt{k!}}\hat{U}_{t}|k\rangle\quad \text{con} \quad z=e^{-i\omega t}$$
Normalizzati, ma non ortogonali fra loro. La norma è
$$|\langle z_{1}|z_{2}\rangle|^{2}=e^{-|z_{1}-z_{2}|^{2}}$$
Evoluzione temporale (viene da Schrödinger picture e autostato dell'operatore numero)
$$|z_{t}\rangle=e^{-i\omega t/2}|e^{-i\omega t}z\rangle$$
Probabilità
$$P(n|z)=|\langle n|z\rangle|^{2}=e^{-|z|^{2}} \frac{|z|^{2n}}{n!}, \quad \left\langle P(n|z) \right\rangle=|z|^{2}$$
## Sistemi
Due stati sono degeneri se sono due autostati linearmente indipendenti dell'Hamiltoniana del sistema che hanno lo stesso autovalore. $\ket{\psi}$ e $\ket{\phi}$ sono degeneri se $\braket{ \psi | \phi }=0$ e $\hat{H}\ket{\psi}=E\ket{\psi}$ e $\hat{H}\ket{\phi}=E\ket{\phi}$.
### Buca infinita
Larghezza $a$. Ammette solo stati legati
$$V=\begin{cases}
0,&\text{ se }0\leq x \leq a \\
\infty,& \text{ altrimenti}
\end{cases}; \quad E_{n}=\frac{\hbar^{2}k_{n}^{2}}{2m}=\frac{n^{2}\pi^{2}\hbar^{2}}{2ma^{2}};\quad \psi_{n}=\sqrt{\frac{2}{a}}\sin\left(\frac{n\pi}{a}x\right)$$
### Buca finita
Larghezza $a$. Ammette sia stati legati che stati liberi
$$V(x)=\begin{cases}
- V_{0} & \text{se }-a<x<a \\
0 & \text{altrove}
\end{cases}$$
Le soluzioni degli stati legati sono trascendentali. Se la buca è profonda e larga, gli autovalori sono simili alla buca infinita
$$E_{n}+V_{0}\simeq \frac{n^{2}\pi^{2}\hbar^{2}}{2m(2a)^{2}}$$
se è poco profonda e stretta ha sempre meno stati legati finché non ne rimane solo uno, che è il minimo indifferentemente dal potenziale. Per gli stati liberi, il coefficiente di trasmissione è
$$T^{-1}=1 + \frac{V_{0}^{2}}{4E(E+V_{0})}\sin^{2}\left(\frac{2a}{\hbar}\sqrt{2m(E+V_{0})}\right)$$
e diventa uno agli autovalori visti sopra.
### Oscillatore armonico
Ammette solo stati legati
$$\hat{H}=\frac{\hat{p}^{2}}{2m}+ \frac{m\omega ^{2}}{2}\hat{q}^{2}=\hbar\omega\left(\hat{a}^{+}\hat{a}+ \frac{1}{2}\right)$$
Autostati
$$\psi_{n}(x)=\frac{1}{\sqrt{n!}}(\hat{a}^{+})^{n}\left(\frac{m\omega}{2\hbar}\right)^{1/4}e^{-(m\omega/2\hbar)x^{2}};\quad E_{n}=\left(n+ \frac{1}{2}\right)\hbar\omega$$
con operatori di creazione e distruzione
$$\hat{a}=\sqrt{ \frac{m\omega}{2\hbar} }\hat{q}+i \frac{1}{\sqrt{ 2m\omega \hbar }}\hat{p},\qquad \hat{a}^{+}=\sqrt{ \frac{m\omega}{2\hbar} }\hat{q}-i \frac{1}{\sqrt{ 2m\omega \hbar }}\hat{p}$$
$$\hat{a}^{+}\ket{\psi_{n}} =\sqrt{n+1}\ket{\psi_{n+1}} ,\quad \hat{a}\ket{\psi_{n}} =\sqrt{n}\ket{\psi_{n-1}} $$
Operatore numero $\hat{a}^{+}\hat{a}$
$$\hat{a}^{+}\hat{a}=\frac{\hat{p}^{2}}{2m\omega \hbar}+ \frac{m\omega}{2\hbar}\hat{q}^{2}- \frac{1}{2}$$
$$\hat{a}^{+}\hat{a}\ket{\psi_{n}} =n\ket{\psi_{n}} ,\quad \hat{a}\hat{a}^{+}\ket{\psi_{n}} =(n+1)\ket{\psi_{n}} $$
Autostati dell'operatore numero
$$|n\rangle= \frac{(\hat{a}^{+})^{n}}{\sqrt{n!}}|0\rangle$$
Posizione e momento in termini di operatori di creazione e distruzione
$$\hat{q}=\sqrt{\frac{\hbar}{2m\omega}}(\hat{a}^{+}+\hat{a})\quad;\quad \hat{p}=i\sqrt{\frac{\hbar m\omega}{2}}(\hat{a}^{+}-\hat{a})$$
Caso classico
$$\ddot{q}=- \frac{k}{m}q=-\omega^{2}q \quad ; \quad q(t)=A\cos(\omega t)+B\sin(\omega t)=C\cos(\omega t+\varphi)$$
### Particella libera
Ammette solo stati liberi
$$\hat{H}=\frac{\hat{p}^{2}}{2m}$$
Non ha autostati normalizzabili. Evoluzione temporale
$$\psi_{t}(x)=\int_{-\infty}^{\infty}\sqrt{ \frac{m}{2it\pi \hbar} } e^{im(x-y)^{2}/2\hbar t}\psi(y) \ dy $$
### Potenziale delta di Dirac
La buca ammette esattamente uno stato legato e stati liberi
$$\hat{H}=\frac{\hat{p}^{2}}{2m}-\gamma \delta(x)$$
Stati liberi barriera
$$\psi_{E}(x)=A_{L}\left( e^{ikx}- i \frac{m\gamma}{\hbar ^{2}k-im\gamma}e^{-ikx} \right)\Theta(-x)+A_{L} \frac{\hbar^{2}k}{\hbar ^{2}k+im\gamma}\Theta(x)$$
con $A_{L}$ qualche valore non costante perché non normalizzabile. Stato legato buca ad energia $E<0$
$$\psi_{\lvert E \rvert }(x)\sqrt{ \frac{m\gamma}{\hbar ^{2}} }e^{-(i/\hbar)\sqrt{ 2m\lvert E \rvert  }\,\lvert x \rvert },\qquad\lvert E \rvert =\frac{m\gamma ^{2}}{2\hbar ^{2}}$$
## Teoria delle perturbazioni
Non degenere, primo e secondo ordine, autovalori $E$ e autostati $\ket{\psi}$, perturbazione $H'$
$$E_{n}^{1}=\langle \psi_{n}^{0}|H'|\psi_{n}^{0}\rangle, \quad  E_{n}^{2}=\sum\limits_{m\neq n} \frac{|\langle \psi_{m}^{0}|H'|\psi_{n}^{0}\rangle|^{2}}{E_{n}^{0}-E_{m}^{0}}, \quad \ket{\psi_{n}^{1}} =\sum\limits_{m\neq n} \frac{\langle \psi_{m}^{0}|H'|\psi_{n}^{0}\rangle}{E_{n}^{0}-E_{m}^{0}}\ket{\psi_{m}^{0}} $$
Degenere, primo ordine, autovalori $2$-volte degeneri
$$\mathbf{W}\begin{pmatrix}
\alpha \\
\beta
\end{pmatrix}=\begin{pmatrix}W_{aa} & W_{ab} \\ W_{ba} & W_{bb}\end{pmatrix}\begin{pmatrix}\alpha \\ \beta\end{pmatrix}=E^{1}\begin{pmatrix}\alpha \\ \beta\end{pmatrix} \quad \text{con}\quad W_{ij}=\langle \psi_{i}^{0}|\hat{V}|\psi_{j}^{0}\rangle$$
Per $n$-volte degeneri basta aumentare la dimensione della matrice e del vettore. Le correzioni di primo ordine all'energia sono gli autovalori della matrice $\mathbf{W}$. Gli autovettori invece sono i parametri della combinazione lineare degli stati perturbati, a modo che lo stato misto $\ket{\psi}$ sia pari a $\ket{\psi}=\alpha \ket{\psi_{\alpha}}+\beta \ket{\psi_{\beta}}$, dove $\ket{\psi_{\alpha}}$ e $\ket{\psi_{\beta}}$ sono i due autostati degeneri prima della perturbazione. In pratica, si vuole diagonalizzare $\mathbf{W}$ per tirare fuori gli autovalori.
## Consigli
- Usa le proprietà degli operatori (unitarietà $\hat{D}\hat{D}^{+}=\hat{\mathbf{1}}$ e hermitianità $\braket{ \psi | \hat{D}\phi }=\braket{ \hat{D}\psi | \phi }$ sono le più importanti).
- Usa i risultati dell'algebra lineare, anche al di là di quantistica. Vedi:
	- Disuguaglianza di Schwarz: $\langle v|w\rangle\leq||v||\,||w||$.
	- Decomposizione spettrale (vedi sopra)
	- Traccia: $\mbox{Tr}(\hat{A})=\sum\limits_{n}^{\infty}\langle\phi_{n}| \hat{A}|\phi_{n}\rangle$, con $\phi_{n}$ autovettori di $\hat{A}$.
- Conviene sempre controllare la forma delle equazioni prima di usare formule fatte e finite (ad es. sostituire la perturbazione nell'Hamiltoniana prima di cercare le correzioni). Le sostituzioni aiutano a ritrovare forme note.
- L'integrazione per parti è utile casomai si debba risolvere un integrale: $\int_{a}^{b} fg'=fg|_{a}^{b}-\int_{a}^{b}f'g$.
- Cambiare forma all'equazione è utile per vedere nuove relazioni (ad es. prendere la norma di qualcosa, specialmente un operatore su un vettore).
- Identificare i vettori su cui proiettano dei proiettori può essere estremamente laborioso, quindi conviene vedere se è ovvio.
- La fase è arbitraria, ma la differenza di fase no! È importante soprattutto cercando i moduli quadri di coefficienti, tipo in $|\alpha|^{2}+|\beta|^{2}=1$. Se ad es. $\alpha=1/\sqrt{2}$, allora $\beta=e^{i\phi}/\sqrt{2}$, perché abbiamo deciso fase nulla in $\alpha$ e quindi la fase in $\beta$ non la possiamo più decidere.
- L'energia potenziale in un'Hamiltoniana è tutta la parte che non include termini con $\hat{p}$, che sono invece di energia cinetica.
- La normalizzazione dei parametri $\lvert \alpha \rvert^{2}+\lvert \beta \rvert^{2}+\ldots=1$ è obbligatoria per tutti gli stati normalizzati ed è un'equazione utile per determinarli (ad es. risolvendo un'equazione agli autovalori direttamente).
## Metodi
- Buca infinita → Raccogli costanti come $-k^{2}$ → Risolvi come oscillatore armonico classico → Quantizzazione compare nelle condizioni al contorno.
- Oscillatore armonico → Raccogli $1/2m$ nell'Hamiltoniana → Definisci $a$ e $a^{+}$ → Trova l'operatore numero $a^{+}a$ per semplice prodotto → Esprimi Hamiltoniana in funzione di $a^{+}a$ → Trova stato fondamentale $|0\rangle$ sviluppando $a |0\rangle=0$ → Esce differenziale, risolvi integrando direttamente → Normalizza → Autovalore sostituendo → Autostati successivi applicando $a^{+}$ ripetutamente.
- Normalizzazione $a^{+}$ e $a$ → Vale $a^{+}|n\rangle=c_{n}|n+1\rangle$ e $a |n\rangle=d_{n}|n-1\rangle$ → $\langle a_{\pm}\psi_{n}|a_{\pm}\psi_{n}\rangle=\langle a_{\mp}a_{\pm}\psi_{n}|\psi_{n}\rangle$ → $\langle \hat{a}^{+}\hat{a}\psi_{n}|\psi_{n}\rangle=n\langle \psi_{n}|\psi_{n}\rangle$ e $\langle \hat{a}\hat{a}^{+}\psi_{n}|\psi_{n}\rangle=(n+1)\langle\psi_{n}|\psi_{n}\rangle$ → $|c_{n}|^{2}=n$ e $|d_{n}|^{2}=n+1$.