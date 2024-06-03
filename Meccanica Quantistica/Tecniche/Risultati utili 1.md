## Matematica
### Equazione di Schrödinger e funzione d'onda
Equazione di Schrödinger dipendente dal tempo:
$$i\hbar \frac{\partial }{\partial t}|\Psi\rangle=\hat{H}|\Psi\rangle=- \frac{\hbar^{2}}{2m} \frac{\partial ^{2}}{\partial x^{2}}|\Psi\rangle+V |\Psi\rangle$$
Indipendente dal tempo:
$$\hat{H}\psi=E\psi$$
$$- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}}(x) + V(x)\psi(x)=E\psi(x)$$
Caso dipendente da quello indipendente 1D e 3D:
$$\Psi(q,t)=\sum\limits_{n=1}^{\infty}c_{n}\psi_{n}(q)e^{iE_{n}t/\hbar}=\sum\limits_{n=1}^{\infty}c_{n}\Psi_{n}(q,t); \quad \Psi(\vec{r},t)=\sum\limits_{n=1}^{\infty}c_{n}\Psi_{n}(\vec{r},t)$$
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
Se $|\psi\rangle$ è un autostato di $H$ con autovalore $E$
$$|\psi_{t}\rangle=\hat{U}_{t}|\psi\rangle=e^{-iEt/\hbar}|\psi\rangle$$
### Commutatori
$$[r_{i},p_{j}]=-[p_{i},r_{j}]=i\hbar\delta_{ij}, \quad [r_{i},r_{j}]=[p_{i},p_{j}]=0$$
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
$$\sum\limits_{i=1}^{n}\hat{P}_{\psi_{i}}=\hat{\mathbb{1}} \quad ; \quad \int_{-\infty}^{+\infty}|e_{z}\rangle\langle e_{z}|dz=\hat{\mathbb{1}}$$
Idempotenza
$$\hat{P}^{2}=\hat{P}$$
Tutti gli operatori idempotenti hanno come unici autovalori 0 e 1. Infatti
$$T |\psi\rangle=t |\psi\rangle , \quad T^{2}=T$$
implica
$$t |\psi\rangle=T |\psi\rangle=TT |\psi\rangle=Tt |\psi\rangle=tT |\psi\rangle=t^{2}|\psi\rangle \quad \Rightarrow \quad t=t^{2} \quad \Rightarrow \quad t=0,1$$
### Matrici di Pauli
Forma standard:
$$\hat{\sigma}_{x}=\pmatrix{0 & 1 \\ 1 & 0},\;\hat{\sigma}_{y}=\pmatrix{0 & -i \\ i & 0},\;\hat{\sigma}_{z}=\pmatrix{1 & 0 \\ 0 & -1}$$
tutte con autovalori $\pm1$. Sono autoaggiunte: $\hat{\sigma}_{i}^{\dagger}=\hat{\sigma}_{i}$. I quadrati sono unitari: $\hat{\sigma}_{i}^{2}=\hat{\mathbb{1}}$. Gli autovettori sono
$$x_{+}: \frac{1}{\sqrt{2}}\pmatrix{1 \\ 1}, \quad x_{-}: \frac{1}{\sqrt{2}}\pmatrix{1 \\ -1}$$
$$y_{+}: \frac{1}{\sqrt{2}}\pmatrix{1 \\ i}, \quad y_{-}: \frac{1}{\sqrt{2}}\pmatrix{1 \\ -i}$$
$$z_{+}: \pmatrix{1 \\ 0}, \quad z_{-}: \pmatrix{0 \\ 1}$$
Vale
$$\sigma_{x}|\uparrow\,\rangle=|\downarrow\;\rangle, \quad \sigma_{x}|\downarrow\;\rangle=|\uparrow\;\rangle$$
### Matrice di Hadamard
$$U= \frac{1}{\sqrt{2}}\pmatrix{1 & 1 \\ 1 & -1}=(|\uparrow x\;\rangle |\downarrow x\;\rangle)$$
### Matrice di densità
$$\hat{\rho}=\pmatrix{\rho & \sigma \\ \sigma^{*} & 1-\rho}$$
dove $\rho\in[0,1]$ e $\sigma\in\mathbb{C}$. Ha traccia unitaria, è autoaggiunta.
### Prodotto tensoriale
$$v\otimes w=\pmatrix{v_{1}\\ v_{2}}\otimes\pmatrix{w_{1} \\ w_{2}}=\pmatrix{v_{1} & \pmatrix{w_{1} \\ w_{2}} \\ v_{2} & \pmatrix{w_{1} \\ w_{2}}}=\pmatrix{v_{1}w_{1} \\ v_{1}w_{2} \\ v_{2}w_{1} \\ v_{2}w_{2}}$$
### Momento angolare
$$\hat{L}_{x}=\frac{\hbar y}{i}\frac{\partial }{\partial z}- \frac{\hbar z}{i}\frac{\partial }{\partial y}, \quad \hat{L}_{y}=\frac{\hbar z}{i}\frac{\partial }{\partial x}- \frac{\hbar x}{i}\frac{\partial }{\partial z}, \quad \hat{L}_{z}=\frac{\hbar x}{i}\frac{\partial }{\partial y}- \frac{\hbar y}{i}\frac{\partial }{\partial x}$$
$$[L_{x},L_{y}]=i\hbar L_{z}, \quad [L_{y},L_{z}]=i\hbar L_{x}, \quad [L_{z},L_{x}]=i\hbar L_{y}$$
$$[L^{2},L_{z}]=0; \quad L^{2}=\hbar^{2}l(l+1)$$
$$L^{2}Y_{lm}=\hbar^{2}l(l+1)Y_{lm}, \quad L_{z}Y_{lm}=\hbar mY_{lm}$$
$$l=0,\;1/2,\;1,\;3/2,\;2,\ldots\quad; \quad m=-l,-l+1,\ldots,0,\ldots,l-1,l$$
Operatori di creazione e distruzione
$$L_{\pm}\equiv L_{x}\pm iL_{y}$$
$$L_{\pm}|sm\rangle=\hbar\sqrt{l(l+1)-m(m\pm1)}|l(m\pm1)\rangle$$
$$L^{2}=L_{\pm}L_{\mp}+L^{2}_{z}\mp\hbar L_{z}$$
Gli autovalori sono gli stessi per tutte le componenti $L_{x}$, $L_{y}$ e $L_{z}$.
### Spin
$$[S^{2},S_{z}]=0$$
$$\hat{\mathbf{S}}=\frac{\hbar}{2}\hat{\sigma}$$
con $\hat{\sigma}$ le matrici di Pauli.
 
Equazioni agli autovalori
$$S^{2}|sm_{s}\rangle=\hbar^{2}s(s+1)|sm_{s}\rangle, \quad S_{z}|sm_{s}\rangle=\hbar m_{s} |sm_{s}\rangle$$
$$s=0,\frac{1}{2},1,\frac{3}{2},\ldots; \quad m_{s}=-s,-s+1,\ldots,0,\ldots,s-1,s$$
Operatori di creazione e distruzione
$$S_{\pm}=S_{x}\pm iS_{y}$$
$$S_{\pm}|sm\rangle=\hbar\sqrt{s(s+1)-m(m\pm1)}|s(m\pm1)\rangle$$
Per spin 1/2
$$\mathbf{S}_{+}|\downarrow\;\rangle=\hbar |\uparrow\;\rangle, \quad \mathbf{S}_{-}|\uparrow\;\rangle=\hbar |\downarrow\;\rangle, \quad \mathbf{S}_{+}|\uparrow\;\rangle=\mathbf{S}_{-}|\downarrow\;\rangle=0$$

La somma di spin in un sistema a due particelle con spin $s_{1}$ e $s_{2}$ è tra $|s_{1}-s_{2}|$ e $s_{1}+s_{2}$, a passi interi. Per una coppia di due particelle con $s=1/2$ è 0 o 1.

Gli autovalori sono gli stessi per tutte le componenti $S_{x}$, $S_{y}$ e $S_{z}$.
### Momento angolare totale
$$\vec{J}=\vec{L}+\vec{S}, \quad [\vec{J},\vec{L}], \quad [\vec{J},\vec{S}]$$
$$J^{2}|jm_{j}\rangle=\hbar^{2}j(j+1)|jm_{j}\rangle,\quad J_{z}|jm_{j}\rangle=\hbar m_{j}|jm_{j}\rangle$$
### Rappresentazioni di stato
Posizione
$$\Psi(x,t)=\langle x|\psi(t)\rangle$$
Momento
$$\Phi(p,t)=\langle p|\psi(t)\rangle$$
Coefficienti dell'Hamiltoniana
$$c_{n}(t)=\langle n|\psi(t)\rangle$$
Decomposizione spettrale di un qualunque operatore in una base ortonormale $\{e_{n}\}$
$$T=\sum\limits_{n}t_{n} e_{n}^{*}\cdot e_{n}=\sum\limits_{n}t_{n}|e_{n}\rangle \langle e_{n}|=\sum\limits_{n}t_{n}\hat{P}_{e_{n}}$$
dove deve valere
$$Te_{n}=t_{n}e_{n}$$
Se l'operatore modifica l'autovettore (come quelli di creazione/distruzione) del tipo
$$T e_{n}^{(1)}=t_{n}e_{n}^{(2)}$$
allora
$$T=\sum\limits_{n}t_{n}|e_{n}^{(2)}\rangle \langle e_{n}^{(1)}|$$
### Rappresentazioni di evoluzione
Di Schrödinger (con equazione di Schrödinger)
$$|\psi_{t,S}\rangle=U_{t}|\psi\rangle$$
Di Heisenberg (con equazione di Heisenberg)
$$\hat{A}_{t,H}=U_{t}^{+}\hat{A}U_{t}$$
Di interazione
$$H_{I}=H_{0}+H_{1}; \quad i\hbar \frac{\partial }{\partial t}|\psi_{I}(t)\rangle=H_{I}(t)|\psi_{I}(t)\rangle$$
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
$$\text{operatore numero: }a_{+}a_{-}\psi_{n}=n\psi_{n},\quad a_{-}a_{+}\psi_{n}=(n+1)\psi_{n}$$
Autostati dell'operatore numero
$$|n\rangle= \frac{(a^{+})^{n}}{\sqrt{n!}}|0\rangle$$
Posizione e momento in termini di operatori di creazione e distruzione
$$q=\sqrt{\frac{\hbar}{2m\omega}}(a_{+}+a_{-})\quad;\quad p=i\sqrt{\frac{\hbar m\omega}{2}}(a_{+}-a_{-})$$
Caso classico
$$\ddot{q}=- \frac{k}{m}q=-\omega^{2}q \quad ; \quad q(t)=A\cos(\omega t)+B\sin(\omega t)=C\cos(\omega t+\varphi)$$
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
	- Decomposizione spettrale (vedi sopra)
	- Traccia: $\mbox{Tr}(\hat{A})=\sum\limits_{n}^{\infty}\langle\phi_{n}| \hat{A}|\phi_{n}\rangle$, con $\phi_{n}$ autovettori di $\hat{A}$.
- Conviene sempre controllare la forma delle equazioni prima di usare formule fatte e finite (ad es. sostituire la perturbazione nell'Hamiltoniana prima di cercare le correzioni).
- L'integrazione per parti è utile casomai si debba risolvere un integrale: $\int_{a}^{b} fg'=fg|_{a}^{b}-\int_{a}^{b}f'g$.
- Cambiare forma all'equazione è utile per vedere nuove relazioni (ad es. prendere la norma di qualcosa, specialmente un operatore su un vettore).
- Identificare i vettori su cui proiettano dei proiettori è estremamente laborioso, quindi dovrebbe è meglio cercare se è ovvio.
- La fase è arbitraria, ma la differenza di fase no! È importante soprattutto cercando i moduli quadri di coefficienti, tipo in $|\alpha|^{2}+|\beta|^{2}=1$. Se ad es. $\alpha=1/\sqrt{2}$, allora $\beta=e^{i\phi}/\sqrt{2}$, perché abbiamo deciso fase nulla in $\alpha$ e quindi la fase in $\beta$ non la possiamo più decidere.
- Quando Benatti dice hermitiano, intende dire autoaggiunto.