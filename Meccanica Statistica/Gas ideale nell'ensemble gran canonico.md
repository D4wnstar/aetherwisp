Si dimostra che l'[[ensemble canonico]] e l'[[ensemble gran canonico]] danno risultati equivalenti nel calcolo delle proprietà di un gas ideale.

<!-- Lezione del 19/10/23 da recuperare va qui -->

<!-- Lezione del 24/10/23 -->
$$a)\quad a'(\rho_{B})-a'(\rho_{a})=v_{B}P(v_{B})-v_{A}P(v_{A})-\int_{v_{A}}^{v_{B}}P(v)dv$$
$$b)\quad P(v_{B})-P(v_{A})=\int_{\rho_{B}}^{\rho_{A}}d\rho a'(\rho)-[\rho_{A}a'(\rho_{A})-\rho_{B}a'(\rho_{B})]$$
$$\rho_{A}=\frac{1}{v_{A}}\quad;\quad\rho_{B}=\frac{1}{v_{B}}$$
Condizioni per l'estremo: $a'(\rho)=\mu$ 

![[Drawing 2023-10-24 09.11.00.excalidraw|100%|center]]
$$S_{1}=S_{2}\quad;\quad A_{c}-A_{r}=S_{1}-S_{2} \Rightarrow A_{c}=A_{r} \Rightarrow P(v_{1})=P(v_{2})=P^{\ast}$$
Usando la b)
$$P(v_{2})-P(v_{1})=\int_{\rho_{2}}^{\rho_{1}}d\rho a'(\rho)-[\rho_{1}a'(\rho_{1})-\rho_{2}a'(\rho_{2})]$$
$$0=a'(\rho_{2})-a'(\rho_{1})=(v_{2}-v_{1})P'-\int_{v_{1}}^{v_{2}}P(v)dv=0$$
$$A_{r}-A_{c}=\tilde{S}_{1}-\tilde{S}_{2}\Rightarrow \tilde{S}_{1}-\tilde{S}_{2}$$
Se aumenti il potenziale chimico $\mu^{\ast}$ nel grafico di sinistra, aumenta $S_{1}$ e diminuisce $S_{2}$ quindi $S_{1}>S_{2}\rightarrow P(v_{2}')>P(v_{1}')$ con $v_{1}',v_{2}'$ le velocità associate al nuovo $\mu^{\ast}$.

$$Z(\mu,V,T)=\exp\left(\frac{e^{\beta\mu} V}{\lambda^{3}}\right)=\exp\left(\frac{zV}{\lambda^{3}}\right)$$
$$d\Omega=-SdT-PdV-Nd\mu$$
$$\langle N \rangle=- \frac{\partial \Omega}{\partial \mu}{\big|}_{T,V}= $$
$$\Omega=-PV \rightarrow P=- \frac{\Omega}{V} \rightarrow Z=e^{\beta P V}=e^{-\beta\Omega}$$
$$S=- \frac{\partial \Omega}{\partial T}{\big|}_{V,\mu}= \frac{\partial }{\partial T}\left( k_{B}T \frac{e^{\beta\Omega}}{\lambda^{3}}V \right)=k_{B} \frac{5}{2} \frac{1}{\lambda^{3}}e^{\beta\mu}V+ \frac{k_{B}T}{\lambda^{3}}Ve^{\beta\mu}\left( - \frac{\beta\mu}{T} \right)=$$
$$=\frac{5}{2}k_{B} \frac{e^{\beta\mu}V}{\lambda^{3}}- k_{B} \frac{Ve^{\beta\mu}}{\lambda^{3}} \beta\mu=\ldots$$
Voglio scrivere $\beta\mu$ in termini di pressione e temperatura. Allora uso che
$$\frac{\langle N \rangle}{V}=\rho=\frac{z}{\lambda^{3}}= \frac{e^{\beta\mu}}{\lambda^{3}}$$
allora
$$\ldots=\frac{5}{2}k_{B}\langle N \rangle-k_{B}\langle N \rangle\ln(\rho\lambda^{3})=k_{B}\langle N \rangle \left( \frac{5}{2}+\ln\left(\frac{1}{\lambda^{3}\rho}\right) \right)=$$
$$=k_{B}\langle N \rangle \left( \ln e^{\frac{5}{2}} + \ln\left(\frac{1}{\lambda^{3}\rho}\right) \right)$$
da cui troviamo che
$$\boxed{S=k_{B}\langle N \rangle\ln\left( \frac{e^{\frac{5}{2}}}{\lambda^{3}\rho} \right)}$$
che è lo stesso risultato che abbiamo trovato nel [[gas ideale nell'ensemble canonico]].