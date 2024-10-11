L'**ensemble microcanonico** è un insieme statistico che descrive i possibili stati di un [[Sistema isolato]]. In esso valgono il [[Teorema di equipartizione dell'energia]] e l'[[Ipotesi ergodica]].
Prendo una funzione di densità dei punti rappresentativi $\rho(q;p)=\rho(H(q;p)) \Rightarrow \rho(E)$ nello spazio delle fasi con $H$ [[Hamiltoniana]] del sistema. Prendiamo un sistema isolato, quindi con energia $E$ costante. Decido che $\rho = cost$, allora valgono alcune scelte per $H$:
1. $H=E$ con $E$ l'energia del sistema
2. $E\leq H \leq E+\Delta$ con $\Delta$ finito
3. $0\leq H\leq E$
Queste tre scelte ci danno la stessa identica dinamica del sistema. Da esse posso calcolare l'*estensione dello spazio delle fasi* $\Gamma$. La 2. è la convenzione di Boltzmann, mentre la 3. è quella di Gibbs. La 3. smette di funzionare con temperature negative.

Nel caso della 1. si ha
$$\int\delta(E-H(q;p))d^{3N}qd^{3N}p$$
con $\delta(x)$ la [[Delta di Dirac]].
Nella 2. si ha
$$\Gamma=\int\limits_{E<H\leq E+\Delta}\rho(H(q;p))d^{3N}qd^{3N}p=\ldots$$
ma la $\rho$ non è univoca. Allora introduco un'[[Azione]] e definisco $\rho$ come l'inversa dell'azione
$$\ldots=\int\limits_{E\leq H<E+\Delta}  \frac{d^{3N}qd^{3N}p}{h^{3N}}= \frac{1}{h^{3N}}\int\limits_{E\leq H<E+\Delta}  d^{3N}qd^{3N}p\quad\quad\mbox{con }\rho(q;p)= \frac{1}{h^{3N}}$$
da cui si trova si trova
$$S=k_{B}\ln(\Gamma(E,N,V,\Delta))$$
quindi dall'estensione dello spazio delle fasi possiamo trovare l'[[entropia]].
Vediamo se vale l'*additività* di $S$. Considero un contenitore diviso in due sotto-contenitori
![[Additività di S|center]]
con volumi $V=V_{1}+V_{2}$. Valgono anche $E=E_{1}+E_{2}$ e $N=N_{1}+N_{2}$ Considero le quantità $\Gamma(E_{1},N_{1},V_{1})$ e $\Gamma(E_{2},N_{2},V_{2})$. Definisco $0\leq i\leq\frac{E}{\Delta}$, che ci dà una divisione in quanti di energia, cioè all'aumentare di $i$ aumento l'energia di una quantità $\Delta$.
$$\Gamma(E,N,V)=\sum\limits_{N_{1}=\Delta}^{N}\sum\limits_{E_{1}=i\Delta} \Gamma(E_{1},N_{1},N_{1})\Gamma(E-E_{1},N-N_{1},V-V_{1}) \frac{N!}{N_{1}!(N-N_{1})!}$$
dove il termine fattoriale rappresenta tutti i modi possibili per partizionare lo spazio.

Consideriamo il caso in cui le particelle interagiscano tra loro (ossia smettiamo di considerare un gas ideale) e prendiamo l'Hamiltoniana come
$$H = H_{1}+H_{2}+V_{12}$$
con $V_{12}$ il termine di interazione reciproca. Inoltre vale
$$H=\sum\limits_{i=1}^{N} \frac{\bar{p}^{2}_{i}}{2m}+\sum\limits_{i<j}\phi(|\bar{r}_{1}-\bar{r}_{2}|)$$
dove la prima somma è quella dei gas ideali non interagenti, mentre la seconda ha una funzione $\phi$ che rappresenta l'interazione tra due particelle. La somma va in $i<j$ per evitare di raddoppiare gli effetti.

Consideriamo un'interazione a lungo raggio $\phi\sim\frac{1}{r_{ij}}$ e inoltre $\phi_{ij}(r)=\varepsilon\left[\left( \frac{\sigma}{r}\right)^{12}- \left( \frac{\sigma}{r}\right)^{6} \right]$. Stiamo considerando l'approssimazione delle **sticky hard spheres (SHS)**. In questo caso, $V_{12}$ è trascurabile rispetto a $H_{1}+H_{2}$ *solo* nel [[Limite termodinamico]]. Allora troviamo che l'entropia del sistema è
$$S_{\alpha}=k_{b}\ln(\Gamma_{\alpha}(E_{\alpha},N_{\alpha},V_{\alpha}))$$
Abbiamo che
$$\begin{align}\underbrace{\Gamma_{1}(E_{1}^{\ast},N_{1}^{\ast},N_{1})\Gamma_{2}(E_{2}^{\ast},N_{2}^{\ast},V_{2}) \frac{N!}{N_{1}^{\ast}!N_{2}^{\ast}!}}\limits_{A_{1}}
\leq\underbrace{\Gamma(E,N,V)}\limits_{A}\leq\\
\leq
\underbrace{(N+1)\left(\frac{E}{\Delta}+1\right)\Gamma_{1}(E_{1}^{\ast},N_{1}^{\ast},N_{1})\Gamma_{2}(E_{2}^{\ast},N_{2}^{\ast},V_{2}) \frac{N!}{N_{1}^{\ast}!N_{2}^{\ast}!}}\limits_{A_{2}}\end{align}$$
$$\frac{k_{b}\ln A_{1}}{N}\leq\frac{k_{b}\ln A}{N}\leq\frac{k_{b}\ln A_{2}}{N}$$
$$A_{2}=(N+1)\left( \frac{E}{\Delta}+1\right)\tilde{A}_{2}\quad,\quad\tilde{A}_{2}=A_{1}$$
$$\hat{S}=\frac{k_{b}\ln[(N+1)(\frac{E}{\Delta}+1)]}{N}=k_{b}\left[\frac{\ln(N+1)}{N}+\frac{\ln(\frac{E}{\Delta}+1)}{N} \right] \Rightarrow_{N \rightarrow\infty} 0$$
$$k_{b}\ln\left( \frac{\Gamma_{1}}{N_{1}!}\right)+k_{b}\ln\left( \frac{\Gamma_{2}}{N_{2}!}\right)\leq k_{b}\ln\left( \frac{\Gamma}{N!}\right)\leq k_{b}\ln\left( \frac{\Gamma_{1}}{N_{1}!}\right)+k_{b}\ln\left( \frac{\Gamma_{2}}{N_{2}!}\right)$$
Allora chiamo $\tilde{\Gamma}$ il **fattore di conteggio corretto** e vale
$$\tilde{\Gamma}=\frac{\Gamma}{N_{\alpha}!}$$
Allora possiamo riscrivere l'integrale $\Gamma$ nell'azione con il conteggio corretto
$$\Gamma(E,N,V)=\frac{1}{N!}\int\limits_{E\leq H<E+\Delta}  \frac{d^{3N}qd^{3N}p}{h^{3N}}$$
Questa vale anche per *diversi* tipi di particelle.

Ora considero la scelta di Gibbs 3. Si ha
$$\Sigma(E,N,V)=\frac{1}{N!}\int\limits_{0\leq H<E}  \frac{d^{3N}qd^{3N}p}{h^{3N}}=\frac{1}{N!}\int\frac{d^{3N}qd^{3N}p}{h^{3N}}\Theta(E-H)$$
dove $\Theta(x)$ è la [[funzione di Heaviside]].

La scelta di Boltzmann 2. diventa
$$\Gamma(E,N,V,\Delta)=\Sigma(E+\Delta,N,V)-\Sigma(E,N,V)$$
La 1. invece è
$$\omega(E,N,V)=\frac{1}{N!}\int\frac{d^{3N}qd^{3N}p}{h^{3N}}\delta(E-H)=\frac{\partial \Sigma}{\partial E}$$
con $\delta(x)$ la delta di Dirac. L'ultima uguaglianza si nota dal fatto che la derivata di $\Theta(x)$ è $\delta(x)$.

Calcoliamo ora l'entropia delle tre scelte. Partendo da Boltzmann
$$S=k_{B}\ln(\Gamma(E,N,V,\Delta)) \overbrace{\Rightarrow}\limits^{L.T.} k_{b}\ln[\omega(E,N,V)\cdot\Delta]=k_{B}\ln[\omega(E,N,V)]+k_{B}\ln(\Delta)$$
$$\frac{S}{N}=\frac{1}{N}k_{B}\ln(\omega(E,N,V))+k_{B} \ln\frac{\Delta}{N} \overbrace{\Rightarrow}\limits^{L.T.} \frac{k_{B}}{N}\ln(\omega(E,N,V))$$
Quindi troviamo che l'entropia della scelta di Boltzmann è uguale a quella della scelta 1. Nel caso di Gibbs, si trova l'equivalenza delle entropie se e solo se $\omega(E)>0$.

Possiamo ritrovare la densità dei punti rappresentativi dall'estensione dello spazio delle fasi
$$\mbox{Scelta 1: }\rho(H)= \frac{1}{N!h^{3N}}\delta(E-H)$$
$$\mbox{Boltzmann: }\rho_{B}(H)= \frac{1}{N!h^{3N}}[\Theta(E+\Delta-H)-\Theta(E-H)]$$
$$\mbox{Gibbs: }\rho_{G}(H)= \frac{1}{N!h^{3N}}\Theta(E-H(q;p))$$
## Microcanonico quantistico
Parto da due postulati sulla distribuzione $\rho$ dell'energia
1. **Equipartizione dell'energia a priori.** $\rho_{nn}$ indipendente da $n$
2. **Ipotesi delle fasi casuali.** $\rho_{nn'}=0$
