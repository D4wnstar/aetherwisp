# Convezione di Gibbs
Consideriamo l'estensione dello spazio delle fasi di Gibbs dell'[[Ensemble microcanonico]]. Un gas ideale ha [[Hamiltoniana]]
$$H=\sum\limits_{i=1}^{N} \frac{\bar{p}_{i}^{2}}{2m}\quad;\quad H=\sum\limits_{\alpha=1}^{3N} \frac{\bar{p}_{\alpha}^{2}}{2m}$$
la prima è in una dimensione, la seconda in tre. In $N$ dimensione l'estensione sarà
$$\Sigma=\frac{V^{N}}{N!h^{3N}}\int\limits_{\sum\limits_{\alpha=1}^{3N} \frac{\bar{p}_{\alpha}^{2}}{2m}\leq E}d^{3N}p=\frac{V^{N}}{N!h^{3N}}\int\limits_{\sum\limits_{\alpha=1}^{3N} \bar{p}_{\alpha}^{2}\leq2mE\equiv R^{2}}d^{3N}p$$
che è un integrale su una *ipersfera* di $p$. Quindi noi vogliamo il volume dell'ipersfera.
$$\phi_{n}=c_{n}R^{n}\quad;\quad c_{n}= \frac{\pi^{\frac{n}{2}}}{\Gamma(\frac{n}{2}+1)}$$
con $n=3N$. Usando $R^{n}=[(2mE)^\frac{1}{2}]^{3N}$, l'estensione diventa
$$\Sigma=\frac{V^{N}}{N!h^{3N}} \frac{\pi^{\frac{3N}{2}}}{\Gamma(\frac{3N}{2}+1)}(2mE)^{\frac{3N}{2}}$$
Per procedere dobbiamo approssimare qualcosa: usiamo l'*approssimazione di Stirling* per il fattoriale
$$N!\simeq\left( \frac{N}{e}\right)^{N}\quad;\quad\ln N!\simeq N[\ln (N)-1]\quad;\quad \frac{1}{N!}\simeq\left( \frac{e}{N}\right)^{N}$$
applicandola a $\Sigma$ si trova
$$\Sigma\simeq\left[ \frac{V}{h^{3}} \left(\frac{2\pi mE2e}{3N}\right)^{\frac{3}{2}} \frac{e}{N}\right]^{N}$$
e l'[[entropia]] è
$$\boxed{S=k_{B}\ln\Sigma=Nk_{B}\ln\left[ \frac{V}{N}e^{\frac{5}{2}}\left(\frac{4\pi mE}{3Nh^{2}}\right)^\frac{3}{2}\right]}$$
con $k_{B}$ la [[Boltzmann constant]]. Si vede che l'entropia è [[Proprietà intensive e estensive|estensiva]].
Prendo il [[Principi della termodinamica#Primo principio|primo principio della termodinamica]] in funzione del numero di elementi
$$dE=TdS-PdV+\mu dN$$
$$\frac{1}{T}=\frac{\partial }{\partial E}Nk_{B}\ln\left[ \frac{V}{N}e\left(\frac{4\pi meE}{3Nh^{2}}\right)^\frac{3}{2}\right]=\ldots$$
possiamo usare le proprietà dei logaritmi
$$\ldots=\frac{\partial }{\partial E}Nk_{B}(\ln X+\ln E^{\frac{3}{2}})=\frac{\partial }{\partial E}Nk_{B} \frac{3}{2}\ln E$$
da cui troviamo
$$\frac{1}{T}=\frac{3}{2}Nk_{B} \frac{1}{E} \Rightarrow \boxed{E= \frac{3}{2}Nk_{B}T}$$
quindi l'energia è funzione della temperatura. L'entropia inoltre è
$$\boxed{S=Nk_{B}\ln\left[ \frac{V}{N}e^{\frac{5}{2}}\left(\frac{2\pi mE}{h^{2}}\right)^\frac{3}{2}\right]}$$
Da qui, partendo dal primo principio, possiamo trovare le espressioni per le variabili di stato. Partiamo dalla pressione
$$P=T \frac{\partial S}{\partial V}{\big|}_{E,N}=T \frac{\partial }{\partial V}Nk_{B}[\ln V+\ln(\ldots)]$$
la seconda parte del logaritmo non dipende da $V$, quindi scompare nella derivata
$$\boxed{P=\frac{N}{V}Tk_{B}}$$
Ora troviamo il potenziale chimico
$$\begin{align}\mu&=-T \frac{\partial S}{\partial N}{\big|}_{V,E}=-T \left\{ k_{B}\ln[\ldots]+Nk_{B} \frac{\partial }{\partial N}\left(\ln\left(\frac{1}{N^{\frac{5}{2}}}\right)+\ln x \right)\right\}=\\
&=-T\left\{ k_{B}\ln\left[ \frac{V}{N}e^{\frac{5}{2}}\left(\frac{4\pi mE}{3Nh^{2}}\right)^\frac{3}{2}\right]+Nk_{B} \left(- \frac{5}{2} \frac{1}{N}\right)\right\}=\\
&=-k_{B}T\left\{\ln\left[ \frac{V}{N}e^{\frac{5}{2}}\left(\frac{4\pi mE}{3Nh^{2}}\right)^\frac{3}{2}\right]+\ln\left( \frac{1}{e^{\frac{5}{2}}}\right)\right\}=\ldots
\end{align}$$
poi usiamo le proprietà dei logaritmi per combinarli e semplificare $e^{\frac{5}{2}}$, oltre a definire $\rho=\frac{N}{V}$
$$\boxed{\mu=k_{B}T\ln\left[\rho \left(\frac{3Nh^{2}}{4\pi mE}\right)^\frac{3}{2}\right]}$$
Chiamo la quantità interna alle parentesi tonde $\lambda^{3}_{T}$
$$\lambda^{3}_{T}=\left(\frac{3Nh^{2}}{4\pi mE}\right)^{\frac{3}{2}}$$
sostituendo l'energia in funzione della temperatura
$$\lambda_{T}^{3}=\left(\frac{3Nh^{2}}{4\pi m} \frac{2}{3Nk_{B}T}\right)^\frac{3}{2}=\left(\frac{h^{2}}{2\pi mk_{B}T}\right)^{\frac{3}{2}}=\frac{h^{3}}{(\sqrt{2\pi mk_{B}T})^{3}}$$
Allora possiamo scrivere
$$\mu=k_{B}T\ln(\lambda^{3}_{T}\rho)$$
# Convenzione $\omega$
Considero ora la convenzione $\omega$ per l'estensione dello spazio delle fasi
$$\omega(E)=\frac{\partial \Sigma(E,N,V)}{\partial E}=\frac{3}{2}NCE^{\frac{3N}{2}-1}=\frac{\frac{3}{2}NCE^{\frac{3N}{2}}}{E}=\Sigma(E) \frac{3}{2} \frac{N}{E}$$
che quindi è in funzione della convenzione di Gibbs.
$$\frac{\ln\omega(E)}{E}= \frac{\ln\Sigma(E)}{E}+\frac{\ln\left( \frac{3}{2} \frac{N}{E}\right)}{E} \rightarrow 0$$
che tende a zero nel [[Limite termodinamico]]. Quindi i risultati della convenzione $\omega$ coincidono con quelli della convenzioni di Gibbs nel limite. Ciò accade anche per la convenzione di Boltzmann. I problemi sorgono quando si considerano sistemi con temperature negative.
$$\Sigma(E)=\sum\limits_{i=1}^{\frac{E}{\Delta}}\Gamma(E_{i},N,V)$$
con $E_{i}=i\Delta$, cioè stiamo considerando l'energia in pacchetti discreti di grandezza $\Delta$. Trovo il termine massimo della somma $E^{\ast}=\max\limits_{i}\Gamma(E_{i},N,V)$. Allora si ha
$$\Gamma(E^{\ast},N,V)\leq\Sigma\leq\left( \frac{E}{\Delta}+1\right)\Gamma(E^{\ast},N,V)$$
$$\frac{\ln\Gamma(E^{\ast})}{E}\leq\frac{\ln\Sigma}{E}\leq\frac{\left( \frac{E}{D}+1\right)}{E}+\frac{\ln\Gamma(E^{\ast})}{E}$$
dove $\frac{E}{D}+1$ svanisce nel limite termodinamico. Allora in quel caso
$$\ln\Sigma(E)=\ln\Gamma(E^{\ast})=\ln(\omega(E^{\ast}))\mbox{ con }\omega'(E)>0$$
Nel caso $\omega'(E)$ non crescente l'uguaglianza non vale.

