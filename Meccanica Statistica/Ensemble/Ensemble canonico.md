L'**[[ensemble]] canonico** dipende dal numero di particelle $N$ e il volume $V$. La temperatura $T$ è fissata. Prendiamo due sistemi.
1. Termostato
2. Contenitore rigido, permeabile al calore, impermeabile alle particelle

![[Sistemi Annidati|center]]
Quindi ci sono solo scambi di energia fra i due sistemi, non scambi di particelle.
$$d\Gamma=\frac{d^{3N}qd^{3N}p}{N!h^{3N}}\quad;\quad\Gamma(q_{1},\ldots,q_{3N},p_{1},\ldots,p_{3N})$$
D'ora in poi consideriamo $\Gamma$, oltre che come estensione dello [[spazio delle fasi]], anche come punto nello spazio delle fasi, solo come notazione conveniente.
Dalla teoria degli ensemble in generale si trova
$$\langle f(\Gamma)\rangle=\frac{\int\rho(q,p,t)f(q,p)dp^{3N}dq^{3N}}{\int\rho(q,p,t)dp^{3N}dq^{3N}}$$
Come nell'[[ensemble microcanonico]] dobbiamo scegliere $\rho$. Qui lo scegliamo come
$$\boxed{\rho(\Gamma)=\delta(E-H)}$$
Cerco la media nel sistema 1. Consideriamo interazioni a lungo raggio
$$\langle f_{1}(\Gamma_{1}) \rangle=\frac{\int d\Gamma_{1}\int d \Gamma _{2}f(\Gamma_{1})\delta(E-H_{1}-H_{2})}{\int d\Gamma_{1}\int d \Gamma _{2} \delta(E-H_{1}-H_{2})}=$$
$$=\frac{\int_{0}^{E} dE_{1}\int d\Gamma_{1}\int d \Gamma _{2}f(\Gamma_{1})\delta(E_{1}-H_{1})\delta(E-E_{1}-H_{2})}{\int_{0}^{E} dE_{1}\int d\Gamma_{1}\int d \Gamma _{2} \delta(E_{1}-H_{1})\delta(E-E_{1}-H_{2})}=\ldots$$
in pratica sto considerando tutte le possibili energie del sistema. (Nelle note del prof. al posto di $E$ come limite superiore dell'integrale c'è $\min[E, \tilde{E}_{1}]$ con $\tilde{E}_{1}=\max H_{1}$ che è valido anche con temperature negative.) Ora riordinando i contenuti degli integrali
$$\ldots=\frac{\int_{0}^{E} dE_{1}\int d\Gamma_{1}f(\Gamma_{1})\delta(E_{1}-H_{1})\int d \Gamma _{2}\delta(E-E_{1}-H_{2})}{\int_{0}^{E} dE_{1}\int d\Gamma_{1}\delta(E_{1}-H_{1})\int d \Gamma _{2} \delta(E-E_{1}-H_{2})}=\ldots$$
Si ha
$$e^{\frac{1}{k_{B}}S_{2}(E-E_{1},N_{2},V_{2})}=\int d \Gamma_{2}\delta(E-E_{1}-H_{2})=\omega_{1}(E-E_{1},N_{2},V_{2})$$
Se si fanno i logaritmi naturali di entrambi i lati si trova qualcosa, credo. Tornando agli integrali
$$\ldots=\frac{\int_{0}^{E} dE_{1}\int d\Gamma_{1}f(\Gamma_{1})\delta(E_{1}-H_{1})e^{\frac{S_{2}}{k_{B}}- \frac{E_{1}}{k_{B}T}}}{\int_{0}^{E} dE_{1}\int d\Gamma_{1}\delta(E_{1}-H_{1})e^{\frac{S_{2}}{k_{B}}- \frac{E_{1}}{k_{B}T}}}=\frac{\int\limits_{H_{1}\leq E} d\Gamma_{1} f_{1}(\Gamma_{1})e^{-\frac{E_{1}}{k_{B}T}}}{\int\limits_{H_{1}\leq E} d\Gamma_{1}e^{-\frac{E_{1}}{k_{B}T}}}$$
semplificando $e^{\frac{S_{2}}{k_{B}}}$. Chiamando $\beta= \frac{1}{k_{B}T}$ e togliendo i pedici si ha
$$\boxed{\langle f(\Gamma) \rangle_{C}= \frac{\int d\Gamma f(\Gamma)e^{-\beta E}}{\int d\Gamma e^{-\beta E}}}$$
che chiamiamo **media canonica**. Chiamo
$$Q_{N}(V,T)=\int d\Gamma e^{-\beta H}\equiv e^{-\beta H(N,V,P)}$$
$$\beta H=-\ln[Q_{N}(V,T)]\quad;\; \frac{\partial \beta H(N,V,T)}{\partial \beta}= \frac{1}{Q_{N}(V,T))}\int d\Gamma He^{-\beta H}=\langle H \rangle=E$$
Ricordando l'[[Potenziali termodinamici#Energia libera di Helmholtz|energia libera di Helmholtz]] 
$$E=A+TS=A+T\left(-\frac{\partial A}{\partial T}\right)=A+\beta \frac{\partial A}{\partial \beta}=\frac{\partial \beta A}{\partial \beta}$$
usando
$$\frac{\partial \beta}{\partial T}=\frac{-\beta}{T}\quad;\quad T \frac{\partial f}{\partial T}=T\frac{\partial \beta}{\partial T}\frac{\partial f}{\partial \beta}=-\beta \frac{\partial f}{\partial \beta}$$
Mi chiedo se $\beta H=\beta A$. Si trova di si.
Suddivido $H$ in $p$ parti *disgiunte*, cioè che le variabili di una parte sono indipendenti da quelle delle altre.
$$H=\sum\limits_{\alpha=1}^{p}H_{\alpha}$$
Allora si ha
$$Q_{N}=\int d \Gamma e^{-\beta\sum\limits_{\alpha=1}^{o}H_{\alpha}}=\frac{\prod\limits_{\alpha}\int d\tilde{\Gamma}_{\alpha}e^{-\beta H_{\alpha}}}{N!}$$
quindi c'è un prodotto di esponenziali e possiamo calcolare una somma di integrali semplici. Per la media si ha
$$\langle H_{\gamma} \rangle=\frac{\int d\Gamma e^{-\beta H}H_{\gamma}}{\int d\Gamma e^{-\beta H}}=\frac{\prod\limits_{\alpha\neq\gamma}\int d\tilde{\Gamma}_{\alpha}e^{-\beta H_{\alpha}}\int d\tilde{\Gamma}_{\gamma}e^{-\beta H_{\gamma}}H_{\gamma}}{\prod\limits_{\alpha\neq\gamma}e\int d\tilde{\Gamma}_{\alpha}e^{-\beta H_{\alpha}}\int d\tilde{\Gamma}_{\gamma}e^{-\beta H_{\gamma}}}=\ldots$$
Semplifico rimuovendo il primo integrale sia sopra che sotto
$$\ldots=\frac{\prod\limits_{\alpha\neq\gamma}\int d\tilde{\Gamma}_{\gamma}e^{-\beta H_{\gamma}}H_{\gamma}}{\prod\limits_{\alpha\neq\gamma}e\int d\tilde{\Gamma}_{\gamma}e^{-\beta H_{\gamma}}}$$
Allora la $Q_{N}$ sarà
$$Q_{N}=\frac{1}{N!}\prod\limits_{\alpha}q_{\alpha}$$
