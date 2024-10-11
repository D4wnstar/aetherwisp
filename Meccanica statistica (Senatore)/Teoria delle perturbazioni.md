Assumiamo di avere un'[[Hamiltoniana]] con la seguente espressione
$$H_{\lambda}=H_{0}+\lambda H_{1}$$
con $\lambda H_{1}$ un **termine di perturbazione**. Ipotizziamo che $\lambda\ll1,\lambda \rightarrow0$. Cerchiamo un'espressione con primo ordine dominante (l'ordine dominante è il primo ordine non nullo dopo la costante). Quindi vogliamo
$$f(x)\simeq f(0)+ \frac{df}{d\lambda}{\big|}_{\lambda=0}\lambda+\ldots$$
Usiamo
$$\int d\Gamma e^{-\beta H}= \frac{1}{N!h^{3N}}\int d^{3N}qd^{3N}p\;e^{-\beta H}\equiv\sum e^{-\beta H}$$
Definisco inoltre la media
$$\langle f \rangle_{0}= \frac{\sum e^{-\beta H_{0}}f}{\sum e^{-\beta H_{0}}}$$
Cerco $Q_{N}$, $A$ in termini di $Q_{N,0}$ o $A_{0}$, e $\langle H_{1} \rangle_{0}$ al primo ordine in $\lambda$. Parto con $Q_{N}$ 
$$Q_{N}=\sum e^{-\beta H}=\sum e^{-\beta(H_{0}+\lambda H_{1})}=\sum e^{-\beta H_{0}}e^{-\beta \lambda H_{1}} \frac{\sum e^{-\beta H_{0}}}{\sum e^{-\beta H_{0}}}=$$
$$=Q_{N,0}\langle e^{-\beta\lambda H_{1}} \rangle_{0}=Q_{N,0}\langle 1-\lambda\beta H_{1} \rangle_{0}$$

Ora trovo $A$ 
$$A=-k_{B}T\ln[Q_{N,0}\langle 1-\lambda\beta H_{1} \rangle_{0}]=A_{0}-k_{B}T\ln(1-\lambda\beta \langle H_{1} \rangle_{0})\simeq\ldots$$
che *non* è di dominata al primo ordine in quanto $\lambda$ è dentro un logaritmo, che contiene tutte le sue potenze. Dobbiamo usare l'approssimazione $\ln(1+x)\simeq x$ quando $x\ll1$, cioè il logaritmo dominato al primo ordine. Allora l'espressione diventa
$$\ldots\simeq A_{0}+\lambda\beta \langle H_{1} \rangle_{0}k_{B}T=A_{0}+\lambda\langle H_{1} \rangle_{0}$$
che è ciò che cerchiamo. Troviamo ora l'energia $E$ 
$$E=\frac{\partial \beta A}{\partial \beta}=\frac{\partial }{\partial \beta}[\beta A_{0}+\lambda \langle H_{1} \rangle_{0}\beta])=E_{0}+\lambda \frac{\partial }{\partial \beta}[\beta \langle H_{1} \rangle_{0}]=\ldots$$
$$\frac{\partial }{\partial \beta}[\beta \langle H_{1} \rangle_{0}]=\langle H_{1} \rangle_{0}+\beta \frac{\partial }{\partial \beta}\langle H_{1} \rangle_{0}$$
$$\frac{\partial }{\partial \beta}\langle H_{1} \rangle_{0}=\frac{\partial }{\partial \beta} \frac{\sum e^{-\beta H_{0}}H_{1}}{\sum e^{-\beta H_{0}}}=-\langle H_{0}H_{1} \rangle+\frac{\sum e^{-\beta H_{0}}+H_{0}}{(\sum e^{-\beta H_{0}})^{2}}\sum e^{-\beta H_{0}}H_{1}=$$
$$=-\langle H_{0}H_{1} \rangle+\langle H_{1} \rangle\langle H_{0} \rangle$$
Rimettendo tutto insieme troviamo
$$E=E_{0}+\lambda[\langle H_{1} \rangle_{0}+\beta(-\langle H_{1}H_{0} \rangle+\langle H_{1} \rangle\langle H_{0} \rangle)]$$
Troviamo infine l'[[entropia]] a partire dall'[[Potenziali termodinamici#Energia libera di Helmholtz|energia libera di Helmholtz]] $A=E-TS$ 
$$S= \frac{E-A}{T}= \frac{1}{T}(E_{0}-A_{0}+\lambda(\langle H_{1} \rangle_{0}+\beta(\langle H_{1}H_{0} \rangle+\langle H_{1} \rangle\langle H_{0} \rangle)-\langle H_{1} \rangle_{0}))$$
