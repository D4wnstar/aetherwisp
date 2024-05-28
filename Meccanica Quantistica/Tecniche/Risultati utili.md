## Matematica
### Equazione di Schrödinger e funzione d'onda
Equazione di Schrödinger dipendente dal tempo:
$$i\hbar \frac{\partial }{\partial t}|\Psi\rangle=\hat{H}|\Psi\rangle$$
Indipendente dal tempo:
$$\hat{H}\psi=E\psi$$
Caso dipendente da quello indipendente 1D e 3D:
$$\Psi(q,t)=\sum\limits_{n=1}^{\infty}c_{n}\psi_{n}(q)e^{iE_{n}t/\hbar}=\sum\limits_{n=1}^{\infty}c_{n}\Psi_{n}(q,t); \quad \Psi(\vec{r},t)=\sum\limits_{n=1}^{\infty}c_{n}\Psi_{n}(\vec{r},t)$$
In $\hat{q}_{t}$
$$\frac{d\hat{q}_{t}}{dt}=\frac{i}{\hbar}[\hat{H},\hat{q}_{t}]$$
In coordinate sferiche
$$- \frac{\hbar^{2}}{2m}\left[\frac{1}{r^{2}}\frac{\partial }{\partial r}\left(r^{2}\frac{\partial \psi}{\partial r}\right)+ \frac{1}{r^{2}\sin\theta}\frac{\partial }{\partial \theta}\left(\sin\theta \frac{\partial \psi}{\partial \theta}\right)+ \frac{1}{r^{2}\sin^{2}\theta}\left(\frac{\partial ^{2}\psi}{\partial \phi^{2}}\right)\right] + V\psi=E\psi$$
La probabilità di misurare un certo autostato $|\phi\rangle$ al tempo $t$ è
$$P_{\psi_{t}}(\phi)=|\langle \phi|\psi_{t}\rangle|^{2}$$
### Disuguaglianza di Heisenberg
In posizione e momento
$$\Delta \hat{q}\Delta \hat{p}\geq \frac{\hbar}{2}$$
In più dimensioni vale solo nella stessa componente. Componenti diversi commutano.
Caso generale tra due operatori autoaggiunti $\hat{A}$ e $\hat{B}$:
$$\Delta \hat{A}\Delta \hat{B}\geq \frac{1}{2i}\left\langle [\hat{A},\hat{B}] \right\rangle$$
In tempo ed energia
$$\Delta E \Delta t\geq \frac{\hbar}{2}$$
### Operatori
In una dimensione
$$\hat{q}=q, \quad \hat{p}= \frac{\hbar}{i}\frac{\partial }{\partial q}, \quad\hat{H}=- \frac{\hbar^{2}}{2m} \frac{d^{2}}{dq^{2}}+V(q)$$
In tre dimensioni
$$\hat{\vec{q}}=\vec{q}, \quad \hat{\vec{p}}=\frac{\hbar}{i}\nabla, \quad \hat{H}=- \frac{\hbar^{2}}{2m}\nabla^{2}+V(\vec{r})$$
Evolutore
$$\hat{U}_{t}=\exp\left(- i \frac{\hat{H}}{\hbar} t\right)=\sum\limits_{i=1}^{\infty}e^{- \frac{i}{\hbar}E_{i}t}|E_{i}\rangle\langle E_{i}|$$
da cui
$$|\psi_{t}\rangle=\hat{U}_{t}|\psi\rangle \text{ (Schrödinger picture)}$$
$$\hat{Q}_{t}=\hat{U}_{t}^{+}\hat{Q}\hat{U}_{t} \text{ (Heisenberg picture)}$$
### Commutatori
$$[r_{i},p_{j}]=-[p_{i},r_{j}]=i\hbar\delta_{ij}, \quad [r_{i},r_{j}]=[p_{i},p_{j}]=0$$
La posizione commuta sempre con la posizione; la quantità di moto commuta sempre con la quantità di moto; tra di loro commutano solo in coordinate diverse, altrimenti si ha $i\hbar$. Due coordinate possono identificarsi come posizione e momento se il loro commutatore è $i\hbar$.

$$[\hat{q},\hat{p}]=i\hbar; \quad [\hat{H},\hat{q}]=- \frac{i\hbar}{m}\hat{p}; \quad [\hat{H},\hat{p}]=0$$
Se $[\hat{H},\hat{Q}]=0$, allora $\hat{Q}$ è una costante del moto.
### Matrici di Pauli
$$\hat{\sigma}_{x}=\pmatrix{0 & 1 \\ 1 & 0},\;\hat{\sigma}_{y}=\pmatrix{0 & -i \\ i & 0},\;\hat{\sigma}_{z}=\pmatrix{1 & 0 \\ 0 & -1}$$
tutte con autovalori $\pm1$. Sono autoaggiunte: $\hat{\sigma}_{i}^{\dagger}=\hat{\sigma}_{i}$. I quadrati sono unitari: $\hat{\sigma}_{i}^{2}=\hat{\mathbb{1}}$. Gli autovettori sono
$$x_{+}: \frac{1}{\sqrt{2}}\pmatrix{1 \\ 1}, \quad x_{-}: \frac{1}{\sqrt{2}}\pmatrix{1 \\ -1}$$
$$y_{+}: \frac{1}{\sqrt{2}}\pmatrix{1 \\ i}, \quad y_{-}: \frac{1}{\sqrt{2}}\pmatrix{1 \\ -i}$$
$$z_{+}: \pmatrix{1 \\ 0}, \quad z_{-}: \pmatrix{0 \\ 1}$$
### Matrice di Hadamard
$$U= \frac{1}{\sqrt{2}}\pmatrix{1 & 1 \\ 1 & -1}=(|\uparrow x\;\rangle |\downarrow x\;\rangle)$$
### Momento angolare
$$\hat{L}_{x}=\frac{\hbar y}{i}\frac{\partial }{\partial z}- \frac{\hbar z}{i}\frac{\partial }{\partial y}, \quad \hat{L}_{y}=\frac{\hbar z}{i}\frac{\partial }{\partial x}- \frac{\hbar x}{i}\frac{\partial }{\partial z}, \quad \hat{L}_{z}=\frac{\hbar x}{i}\frac{\partial }{\partial y}- \frac{\hbar y}{i}\frac{\partial }{\partial x}$$
$$[L_{x},L_{y}]=i\hbar L_{z}, \quad [L_{y},L_{z}]=i\hbar L_{x}, \quad [L_{z},L_{x}]=i\hbar L_{y}$$
$$[L^{2},L_{z}]=0$$
$$L^{2}Y_{lm}=\hbar^{2}l(l+1)Y_{lm}, \quad L_{z}Y_{lm}=\hbar mY_{lm}$$
Operatori di creazione e distruzione
$$L_{\pm}\equiv L_{x}\pm iL_{y}$$
$$L^{2}=L_{\pm}L_{\mp}+L^{2}_{z}\mp\hbar L_{z}$$
Gli autovalori sono gli stessi per tutte le componenti $L_{x}$, $L_{y}$ e $L_{z}$.
### Spin
$$[S^{2},S_{z}]=0$$
$$\boxed{\hat{\mathbf{S}}=\frac{\hbar}{2}\hat{\sigma}}$$
con $\hat{\sigma}$ le matrici di Pauli.

Equazioni agli autovalori
$$S^{2}|sm_{s}\rangle=\hbar^{2}s(s+1)|sm_{s}\rangle, \quad S_{z}|sm_{s}\rangle=\hbar m_{s} |sm_{s}\rangle$$
Operatori di creazione e distruzione
$$S_{\pm}|sm\rangle=\hbar\sqrt{s(s+1)-m(m\pm1)}|s(m\pm1)\rangle$$
$$S_{\pm}=S_{x}\pm iS_{y}$$
Per spin 1/2
$$\mathbf{S}_{+}|\downarrow\;\rangle=\hbar |\uparrow\;\rangle, \quad \mathbf{S}_{-}|\uparrow\;\rangle=\hbar |\downarrow\;\rangle, \quad \mathbf{S}_{+}|\uparrow\;\rangle=\mathbf{S}_{-}|\downarrow\;\rangle=0$$

La somma di spin in un sistema a due particelle con spin $s_{1}$ e $s_{2}$ è tra $|s_{1}-s_{2}|$ e $s_{1}+s_{2}$, a passi interi. Per una coppia di due particelle con $s=1/2$ è 0 o 1.

Gli autovalori sono gli stessi per tutte le componenti $S_{x}$, $S_{y}$ e $S_{z}$.
### Rappresentazioni
Posizione
$$\Psi(x,t)=\langle x|\psi(t)\rangle$$
Momento
$$\Phi(p,t)=\langle p|\psi(t)\rangle$$
Coefficienti dell'Hamiltoniana
$$c_{n}(t)=\langle n|\psi(t)\rangle$$
Interazione
$$i\hbar \frac{\partial }{\partial t}|\psi_{I}(t)\rangle=H_{I}(t)|\psi_{I}(t)\rangle$$
dove
$$H_{I}(t)=\hat{U}^{+}H\hat{U}; \quad |\psi_{I}(t)\rangle=\hat{U}^{+}|\psi(t)\rangle$$
Decomposizione spettrale di un qualunque operatore in una base ortonormale $\{e_{n}\}$
$$T=\sum\limits_{n}t_{n} e_{n}^{*}\cdot e_{n}=\sum\limits_{n}t_{n}|e_{n}\rangle \langle e_{n}|=\sum\limits_{n}t_{n}\hat{P}_{e_{n}}$$
dove deve valere
$$Te_{n}=t_{n}e_{n}$$
Se l'operatore modifica l'autovettore (come quelli di creazione/distruzione) del tipo
$$T e_{n}^{(1)}=t_{n}e_{n}^{(2)}$$
allora
$$T=\sum\limits_{n}t_{n}|e_{n}^{(2)}\rangle \langle e_{n}^{(1)}|$$
### Armoniche sferiche
Le prime armoniche sferiche sono
$$\begin{align}
Y_{0}^{0}&=\sqrt{\frac{1}{4\pi}} \\
Y_{1}^{0}&=\sqrt{\frac{3}{4\pi}}\cos\theta \\
Y_{1}^{\pm1}&=\mp\sqrt{\frac{3}{8\pi}}\sin\theta e^{\pm i\phi} \\
Y_{2}^{0}&=\sqrt{\frac{5}{16\pi}}(3\cos^{2}\theta-1) \\
Y_{2}^{\pm1}&=\mp\sqrt{\frac{15}{8\pi}}\sin\theta\cos\theta e^{\pm i\phi} \\
Y_{2}^{\pm2}&=\sqrt{\frac{15}{32\pi}}\sin^{2}\theta e^{\pm2i\phi}
\end{align}$$
e sono ortonormali fra loro
$$\int_{0}^{2\pi}\int_{0}^{\pi}(Y_{l}^{m})^{*}Y_{l'}^{m'}\sin\theta d\theta d\phi=\langle Y_{l}^{m}|Y_{l'}^{m'}\rangle=\delta_{mm'}\delta_{ll'}$$
Vale che
$$\int_{0}^{\pi}(Y_{l}^{m})^{*}Y_{l'}^{m'}\sin\theta d\theta d\phi=0$$
per ogni $(l,m)\neq(0,0)$. Per $(l,m)=(0,0)$ l'integrale vale $2\sqrt{\pi}$. Infatti, $2\sqrt{\pi}\langle Y_{0}^{0}|Y_{l}^{m}\rangle=0$ per ortogonalità.

La dipendenza angolare di uno stato $\psi$ in un sistema sferico si trova come
$$\langle Y_{l}^{m}|\psi(r,\theta,\phi)\rangle$$
## Sistemi
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
$$V(x)=\frac{1}{2}m\omega^{2}x^{2}; \quad \psi_{n}=\frac{1}{\sqrt{n!}}(a_{+})^{n}\left(\frac{m\omega}{2\hbar}\right)^{1/4}e^{-(m\omega/2\hbar)x^{2}};\quad E_{n}=\left(n+ \frac{1}{2}\right)\hbar\omega$$
con gli operatori di creazione e distruzione $a=a_{-}$ e $a^{\dagger}=a_{+}$
$$a_{\pm}\equiv \frac{1}{\sqrt{2\hbar m\omega}}(\mp ip+m\omega x)$$
$$a_{+}\psi_{n}=\sqrt{n+1}\psi_{n+1},\quad a_{-}\psi_{n}=\sqrt{n}\psi_{n-1}$$
$$a_{+}a_{-}\psi_{n}=n\psi_{n},\quad a_{-}a_{+}\psi_{n}=(n+1)\psi_{n}$$
$$q=\sqrt{\frac{\hbar}{2m\omega}}(a_{+}+a_{-})\quad;\quad p=i\sqrt{\frac{\hbar m\omega}{2}}(a_{+}-a_{-})$$
### Particella libera
Ammette solo stati liberi
$$V=0; \quad \phi(k)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\Psi(x,0)e^{-ikx}dx; \quad \Psi(x,t)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\phi(k)e^{ik[x-(\hbar k/2m)t]}dk$$
### Potenziale delta di Dirac
Ammette esattamente uno stato legato e stati liberi
$$V=-\alpha \delta(x); \quad E=- \frac{m\alpha^{2}}{2\hbar^{2}}; \quad \psi(x)=\frac{\sqrt{m\alpha}}{\hbar}e^{-m\alpha|x|/\hbar^{2}}$$
I coefficienti di trasmissione e riflessione degli stati liberi sono
$$R=\frac{1}{1+ \left(\frac{2\hbar^{2}E}{m\alpha^{2}}\right)},\quad T=\frac{1}{1+\left(\frac{m\alpha^{2}}{2\hbar^{2}E}\right)}$$
## Teoria delle perturbazioni
Non degenere, primo ordine, autovalori
$$E_{n}^{1}=\langle \psi_{n}^{0}|H'|\psi_{n}^{0}\rangle$$
Non degenere, primo ordine, autovettori
$$\psi_{n}^{1}=\sum\limits_{m\neq n} \frac{\langle \psi_{m}^{0}|H'|\psi_{n}^{0}\rangle}{E_{n}^{0}-E_{m}^{0}}\psi_{m}^{0}$$
Non degenere, secondo ordine, autovalori
$$E_{n}^{2}=\sum\limits_{m\neq n} \frac{|\langle \psi_{m}^{0}|H'|\psi_{n}^{0}\rangle|^{2}}{E_{n}^{0}-E_{m}^{0}}$$
Degenere, primo ordine, autovalori $2$-volte degeneri
$$\pmatrix{W_{aa} & W_{ab} \\ W_{ba} & W_{bb}}\pmatrix{\alpha \\ \beta}=E^{1}\pmatrix{\alpha \\ \beta}$$
con
$$W_{ij}=\langle \psi_{i}^{0}|H'|\psi_{j}^{0}\rangle$$
Per $n$-volte degeneri basta aumentare la dimensione della matrice.
## Metodi
- Usa le proprietà degli operatori (unitarietà e autoaggiuntezza sono le più importanti).
- Usa i risultati dell'algebra lineare, anche al di là di quantistica. Vedi:
	- Disuguaglianza di Schwarz: $\langle v|w\rangle\leq||v||\,||w||$.
- Conviene sempre controllare la forma delle equazioni prima di usare formule fatte e finite (ad es. sostituire la perturbazione nell'Hamiltoniana prima di cercare le correzioni).