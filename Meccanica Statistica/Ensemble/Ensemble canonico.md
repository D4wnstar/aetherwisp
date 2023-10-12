L'**[[ensemble]] canonico** è un insieme statistico che descrive i possibili stati di un sistema chiuso in equilibrio termico con una grande fonte di calore, solitamente chiamata *termostato*. Esso dipende dal numero di particelle $N$ e il volume $V$ e la temperatura $T$, tutte fissate. Si tratta di una generalizzazione dell'[[ensemble microcanonico]] che invece richiede che il sistema sia [[Sistema isolato|isolato]]. Il canonico permette gli scambi di calore (ma non di particelle).

Prendiamo due sistemi.
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
$$\boxed{Q_{N}(V,T)=\int d\Gamma e^{-\beta H}\equiv e^{-\beta H(N,V,P)}}$$
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
## Fluttuazioni di energia
L'energia nel ensemble canonico è
$$E=\langle H \rangle= \frac{1}{Q_{N}(V,T)}\int d\Gamma e^{-\beta H}H$$
Derivando per $\beta$ troviamo la scarto quadratico medio
$$-\frac{\partial E}{\partial \beta}=\frac{1}{Q_{N}(V,T)}\int d\Gamma e^{-\beta H}H^{2}- \frac{1}{Q^{2}_{N}(V,T)}\left( \int d\Gamma e^{-\beta H} H\right)^{2}=\langle H^{2} \rangle-\langle H \rangle^{2}$$
Ma vale anche che
$$-\frac{\partial E}{\partial \beta}=-\frac{\partial T}{\partial \beta}\frac{\partial E}{\partial T}=- \frac{1}{\frac{\partial \beta}{\partial T}}\frac{\partial E}{\partial T}=\frac{T}{\beta}C_{V}=k_{B}T^{2}C_{V}$$
con $C_{V}$ la **capacità termica**. Il **calore specifico** è $c_{V}=\frac{C_{V}}{V}$. Allora abbiamo che
$$\langle H^{2} \rangle-\langle H \rangle^{2}=k_{B}T^{2}C_{V}$$
Troviamo ora le fluttuazioni di energia del sistema
$$\sqrt{\frac{\langle H^{2} \rangle - \langle H \rangle^{2}}{E^{2}}}=\sqrt{\frac{k_{B}T^{2}C_{V}}{E^{2}}}=\sqrt{\frac{k_{B}T^{2}c_{V}V}{E^{2}}}\sim \frac{\sqrt{c_{V}}}{\sqrt{V}}$$
da cui si vede che le fluttuazioni sono *soppresse* per $c_{V}$ finiti, ma possono diventare grandi quando $c_{V}$ è grande, cioè vicino alle transizioni di fase.
Le **condizioni di stabilità del sistema** sono
$$\frac{1}{c_{V}}\geq0\quad\quad \frac{1}{k_{p}}=-V \frac{\partial P}{\partial V}\geq0$$
con $k_{P}= - \frac{\Delta V}{V} \frac{1}{\Delta P}=- \frac{1}{V}\frac{\partial V}{\partial P}$ la *compressibilità* del gas.
$$Q_{N}(V,T)=e^{-\beta A}=\int d\Gamma e^{-\beta H}=\int_{0}^{\infty}dE\omega(E)E^{-\beta E}=\int_{0}^{\infty}dE e^{-\beta[E-TS(E,N,V)]}$$
usando che $S=k_{B}\ln\omega(E)\rightarrow\omega(E)=E^{S/k_{B}}=e^{-[-\beta TS]}$. Sappiamo che $E-TS(E)$ offre un estremo, che si trova con
$$\frac{\partial }{\partial E}[E-TS(E)]=1-T \frac{\partial S}{\partial E}=0$$
Usando il [[Principi della termodinamica#Primo principio|primo principio della termodinamica]] troviamo
$$1- \frac{T}{T_{MC}(E)}=0 \Rightarrow T_{MC}(E)=T$$
dove $T_{MC}$ è la temperatura data dall'[[ensemble microcanonico]] ($T$ è quella dell'ensemble canonico).

$$E-TS(E,N,V)=\bar{E}-TS(\bar{E})+0+ \frac{1}{2} \frac{1}{TC_{V}(\bar{E})}(E-\bar{E})^{2}$$
trovato usando
$$\frac{\partial^{2}}{\partial E^{2}}[E-TS(E)]{\big|}_{E}=0-T \frac{\partial ^{2}}{\partial E^{2}}{\big|}_{\bar{E}}=-T\frac{\partial }{\partial E} \frac{1}{T_{MC}(E)}{\big|}_{\bar{E}}=T \left( \frac{1}{T_{MC}^{2}(E)} \frac{\partial T_{MC}}{\partial E} \right)=$$
$$=\frac{T}{T^{2}_{MC}} \frac{1}{\frac{\partial E}{\partial T_{MC}}}{\big|}_{\bar{E}}=\frac{T}{T^{2}_{MC}} \frac{1}{C_{V}(\bar{E})}$$
Tornando a $Q_{N}$ 
$$Q_{N}(V,T)=\int dE e^{-\beta(E-TS(E))}=e^{-\beta(\bar{E}-TS(\bar{E}))}\int_{0}^{\infty}dE e^{\frac{-\beta}{2} \frac{1}{TC_{V}}(E-\bar{E})^{2}}$$
$$\ln Q_{N}=-\beta A(N,V,T)=-\beta(\bar{E}-TS(\bar{E}))+\ln\int_{0}^{\infty}dE e^{- \frac{1}{2k_{B}T^{2}C_{V}}(E-\bar{E})^{2}}$$
Cerchiamo di approssimare l'integrale
$$\simeq\int_{-\infty}^{\infty}dE e^{- \frac{1}{2k_{B}T^{2}C}(E-\bar{E})^{2}}=\int_{-\infty}^{\infty}dx e^{- \frac{1}{2k_{B}T^{2}C_{V}}x^{2}}=\sqrt{2\pi k_{B}T^{2}C_{V}}$$
Allora abbiamo
$$\ln Q_{N}=-\beta(\bar{E}-TS(\bar{E}))+ \frac{1}{2}\ln(2\pi k_{B}T^{2}C_{V})$$
Nel [[limite termodinamico]]
$$\boxed{A(N,V,T)=\bar{E}-TS_{MC}(\bar{E})}$$
con $S_{MC}$ l'entropia dell'ensemble microcanonico, da cui si ritrova $T_{MC}(\bar{E})=T$, stavolta per una generica [[Hamiltoniana]].