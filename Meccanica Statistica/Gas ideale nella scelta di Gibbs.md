Consideriamo l'estensione dello spazio delle fasi di Gibbs dell'[[ensemble microcanonico]]. Un gas ideale ha [[Hamiltoniana]]
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
$$S=k_{B}\ln\Sigma=Nk_{B}\ln\left[ \frac{V}{N}e\left(\frac{4\pi meE}{3Nh^{2}}\right)^\frac{3}{2}\right]$$
Si vede che l'entropia è [[Proprietà intensive e estensive|estensiva]].
Prendo il [[Principi della termodinamica#Primo principio|primo principio della termodinamica]] in funzione del numero di elementi
$$dE=TdS-PdV+\mu dN$$
$$\frac{1}{T}=\frac{\partial }{\partial E}Nk_{B}\ln\left[ \frac{V}{N}e\left(\frac{4\pi meE}{3Nh^{2}}\right)^\frac{3}{2}\right]=\ldots$$
possiamo usare le proprietà dei logaritmi
$$\ldots=\frac{\partial }{\partial E}Nk_{B}(\ln X+\ln E^{\frac{3}{2}})=\frac{\partial }{\partial E}Nk_{B} \frac{3}{2}\ln E$$
da cui troviamo
$$\frac{1}{T}=\frac{3}{2}Nk_{B} \frac{1}{E} \Rightarrow \boxed{E= \frac{3}{2}Nk_{B}T}$$
quindi l'energia è funzione della temperatura. L'entropia inoltre è
$$S=Nk_{B}\ln\left[ \frac{V}{N}e^{\frac{5}{2}}\left(\frac{2\pi mE}{h^{2}}\right)^\frac{3}{2}\right]$$
