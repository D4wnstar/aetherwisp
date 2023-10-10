Uso i risultati dell'[[ensemble canonico]]. Ho che
$$Q_{N}=\frac{1}{N!}\prod\limits_{i=1}^{N}q_{i}\quad;\quad q_{i}=\frac{1}{h^{3}}\int\limits_{V}d\bar{r}_{i}\int\limits_{\mathbb{R}^{3}}d\bar{p}_{i}e^{-\beta \frac{\bar{p}^{2}}{2m}}$$
$$\int\limits_{V}d\bar{r}_{i}=V$$
$$\int d\bar{p}_{i}e^{-\beta \frac{\bar{p}_{i}^{2}}{2m}}=\prod\limits_{\alpha=x,y,z}\int\limits_{\mathbb{R}}d\bar{p}_{i}e^{-\beta \frac{\bar{p}_{i,\alpha}^{2}}{2m}}$$
$$\int_{-\infty}^{\infty} d\bar{p}_{i}e^{-\beta \frac{\bar{p}^{2}}{2m}}=\sqrt{2m k_{B} T}\int_{-\infty}^{\infty}dx e^{-{x^{2}}}=\sqrt{2m\pi k_{B}T}$$
$$q_{\alpha}=\frac{V(2m\pi k_{B}T)^{\frac{3}{2}}}{h^{3}}=V\left(\frac{2m\pi k_{B}T}{h^{2}}\right)^{\frac{3}{2}}\equiv \frac{V}{\lambda^{3}_{\Gamma}}$$
con $\lambda_{\Gamma}=\frac{\sqrt{2m\pi k_{B}T}}{h}$. Tornando alla funzione $Q_{N}$ 
$$Q_{N}(V,T)= \frac{V^{N}}{N!} \frac{1}{\lambda^{3}_{\Gamma}}=\frac{1}{N!}\left(\frac{V}{\lambda^{3}_{\Gamma}}\right)^{N}=\ldots$$
ora usiamo l'[[approssimazione di Stirling]] 
$$\ldots\simeq \left(\frac{e}{N}\frac{V}{\lambda^{3}_{\Gamma}}\right)^{N}$$
Ora troviamo l'[[entropia]] 
$$S=-\frac{\partial }{\partial T}(-k_{B}T\ln Q_{N})=-\frac{\partial }{\partial T}\left[-k_{B}T\ln\left(\frac{eV}{N\lambda^{3}_{\Gamma}}\right)^{N}\right]=$$
$$=k_{B}\frac{\partial }{\partial T}\left[NT\ln\left(\frac{eV}{N\lambda^{3}_{\Gamma}}\right)\right]=k_{B}\left[N\ln\left( \frac{eV}{N\lambda^{3}_{\Gamma}}\right)\right]+ \frac{N\pi3}{2\pi}=$$
$$=Nk_{B}\left[\ln\left( \frac{eV}{N\lambda^{3}_{\Gamma}}+\ln e^{\frac{3}{2}}\right)\right]=Nk_{B}\ln \left( \frac{e^{\frac{5}{2}}V}{N\lambda^{3}_{\Gamma}} \right)$$
Allora, usando la densità $\rho=N/V$, l'entropia è
$$\boxed{S=Nk_{B}\ln\left( \frac{e^{\frac{5}{2}}}{\rho\lambda^{3}_{\Gamma}} \right)}$$
Ora cerco la pressione partendo dall'[[Potenziali termodinamici#Energia libera di Helmholtz|energia libera di Helmholtz]] 
$$A=-k_{B}TN\ln\left( \frac{eV}{N\lambda^{3}_{\Gamma}} \right)$$
$$\boxed{P=-\frac{\partial A}{\partial V}=-\left[ -k_{B}TN \frac{1}{V} \right]= \frac{Nk_{B}T}{V}}$$
Il potenziale chimico $\mu$ è
$$\mu=\frac{\partial A}{\partial N}=-k_{B}T\ln\left( \frac{eV}{N\lambda^{3}_{\Gamma}} \right)-Nk_{B}T \frac{\partial }{\partial N}\ln\left( \frac{1}{N} \right)=$$
$$=-k_{B}T\left[ \ln\left( \frac{V}{N\lambda^{3}_{\Gamma}}\right) +1+N \left( - \frac{1}{N} \right) \right]$$
$$\boxed{\mu=k_{B}T\ln(\lambda^{3}_{\Gamma}\rho)}$$
