## Particelle non interagenti
Sia $\vec{H}$ un campo magnetico. Le particelle hanno un momento magnetico $\vec{\mu}$ e sono distinguibili. "Non interagenti" significa che nella [[Hamiltoniana]] di una particella non ci sono termini che la legano ad altre e le Hamiltoniane sono *separabili*.

Prendo come Hamiltoniana $H_{i}=-\vec{\mu}_{i}\cdot\vec{H}=-\mu_{i} H\cos\theta_{i}$, dove $\theta$ è l'angolo tra il campo magnetico e l'asse del dipolo magnetico. Ho come variabili $\phi$ e $\theta$. Grazie alla separabilità delle Hamiltoniane, possiamo affermare che
$$H=\sum\limits_{i=1}^{N}H_{i}(i)=-\sum\limits_{i=1}^{N}\vec{\mu}_{i}\cdot\vec{H}=\sum\limits_{i=1}^{N}\mu_{i} H\cos\theta$$
Cerco $Q_{N}=q^{N}$ 
$$q=\int_{0}^{\pi}d \phi_{i}\int_{0}^{\pi}d \theta_{i}\sin\theta_{i}e^{\beta\mu H\cos\theta_{i}}$$
Riscrivo come un integrale nella variabile $\cos\theta_{i} = y$ con $d\theta_{i}\sin\theta_{i}=-d\cos\theta_{i}$. Allora l'integrale diventa
$$q=2\pi\int_{-1}^{1}dy e^{\beta\mu Hy}=2\pi \frac{e^{\beta\mu H y}}{\beta\mu H}{\big|}_{-1}^{1}=4\pi \frac{e^{-\beta\mu H}-e^{-\beta\mu H}}{2\beta\mu H}=\ldots$$
dove abbiamo trovato un seno iperbolico
$$\ldots=4\pi \frac{\sinh(\beta\mu H)}{\beta\mu H}$$
Allora abbiamo
$$Q_{N}=\left[ 4\pi \frac{\sinh(\beta\mu H)}{\beta\mu H} \right]^{N}$$
Cerchiamo l'[[Potenziali termodinamici#Energia libera di Helmholtz|energia libera di Helmholtz]] $A=-k_{B}T\ln Q_{N}$ e l'[[Potenziali termodinamici#Energia del sistema|energia libera]] $E=\frac{\partial \beta A}{\partial \beta}$
$$A=-Nk_{B}T\ln\left[ 4\pi \frac{\sinh(\beta\mu H)}{\beta\mu H} \right]$$
$$E=\frac{\partial \beta A}{\partial \beta}=\frac{\partial }{\partial \beta}\left[ -N\ln\left( 4\pi \frac{\sinh(\beta\mu H)}{\beta\mu H} \right) \right]=$$
$$=-N \frac{\partial }{\partial \beta}\left[ \ln(\sinh(\beta\mu H))-\ln(\beta\mu H) -\ln(4\pi)\right]=-N\left[ \frac{\cosh(\beta\mu H)}{\sinh(\beta\mu H)}\mu H- \frac{1}{\beta\mu H}\mu H \right]=$$
$$=-N\mu H\left[ \cosh(\beta\mu H)- \frac{1}{\beta\mu H} \right]$$
dove $\ln(4\pi)$ svanisce per le proprietà dei logaritmi.
Cerco ora la magnetizzazione $M=\frac{\partial A}{\partial H}$ 
$$M=Nk_{B}T\frac{\partial }{\partial H}\left[ \ln(\sinh(\beta\mu H)) -\ln(\beta\mu H) \right]=Nk_{B}T\left[ \coth(\beta\mu H)\beta\mu- \frac{1}{\beta\mu H}\beta\mu \right]=$$
$$=N\mu\left[ \coth(\beta\mu H) - \frac{1}{\beta\mu H} \right]=N\mu f(H)$$
che è il termine nelle parentesi dell'energia libera $E=-N\mu H M$.
Cerco ora la suscettibilità magnetica $\chi=\frac{\partial M}{\partial H}$. Uso lo sviluppo in serie della $\coth$ e di $\frac{1}{x}$ 
$$\coth(x)= \frac{\cosh(x)}{\sinh(x)}\simeq \frac{1 + \frac{x^{2}}{2}}{x + \frac{x^{3}}{6}}= \frac{1}{x} \frac{1+ \frac{x^{2}}{2}}{1+\frac{x^{2}}{6}}\simeq\frac{1}{x} \left( 1 + \frac{x^{2}}{2} \right) \left( 1 - \frac{x^{2}}{6} \right)=$$
$$=\frac{1}{x} \left( 1 + \frac{x^{2}}{2} - \frac{x^{2}}{6} \right)=\frac{1}{x}\left( 1+ \frac{x^{2}}{3} \right)=\frac{1}{x} + \frac{x}{3}$$
Allora la magnetizzazione diventa
$$M=N\mu \left( \frac{1}{\beta\mu H} + \frac{\beta\mu H}{3} - \frac{1}{\beta\mu H}\right)= \frac{N\mu^{2}}{3k_{B}T}H$$
Provo che la magnetizzazione è davvero $\frac{\partial A}{\partial H}$ 
$$- \frac{\partial A}{\partial H_{\alpha}}= \frac{\partial }{\partial H_{\alpha}}(k_{B}T\ln Q_{N})=k_{B}T \frac{1}{Q_{N}}\frac{\partial Q_{N}}{\partial H_{\alpha}}$$
$$\frac{\partial Q_{N}}{\partial H_{\alpha}}=\int\ldots\int \beta\left(\sum\limits_{i=1}^{N}\mu_{i,\alpha}\right)e^{\beta \vec{H}\sum\limits_{i=1}^{N}\mu_{i}}$$
$$- \frac{\partial A}{\partial H_{\alpha}}= \frac{1}{Q_{N}}\int\ldots\left(\sum\limits_{i=1}^{N}\mu_{i,\alpha}\right)e^{\beta \vec{H}\sum\limits_{i=1}^{N}\mu_{i}}$$
Prendo $H=A_{1}+A_{2}+A_{3}$ 
$$-\beta H=-\beta[\alpha A_{1}+A_{2}+A_{3}]$$
$$- \frac{1}{\beta} \frac{\partial F}{\partial \alpha}{\big|}_{a=1}=\langle A_{1} \rangle$$
## Particelle cariche con accoppiamento minimale
Provo il **teorema di Bohr-Von Neumann**, che ci dice che il diamagnetismo è un fenomeno puramente quantistico. Chiamo $q$ la carica.
$$\vec{p}_{i}\Rightarrow\vec{p}_{i}-q \frac{\vec{A}(\vec{r}_{i})}{c}$$
$$H=\sum\limits_{i=1}^{N} \frac{\left( \vec{p}_{i}-q \frac{\vec{A}(\bar{r}_{i})}{c} \right)^{2}}{2m}+v(\bar{r}_{1},\bar{r}_{2},\ldots,\bar{r}_{N})$$
$$Q_{N}(V,T)=\frac{1}{N!h^{3N}}\int d\bar{r}_{i}\ldots d\bar{r}_{N}\;e^{-\beta v(\bar{r}_{1},\ldots,\bar{r}_{N})}\int dp_{1}\ldots dp_{N}\; e^{-\beta \sum\limits_{i=1}^{N}\left(\vec{p}_{i}-q\frac{\vec{A}(\bar{r}_{i})}{c}\right) \frac{1}{2m}}$$
