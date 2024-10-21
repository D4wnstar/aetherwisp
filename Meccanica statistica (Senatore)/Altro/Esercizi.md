Abbiamo un cilindro di base $A_{b}$ e altezza $L_{z}$. Abbiamo $l=\frac{k_{B}T}{mg}$, con $k_{B}$ la [[Boltzmann constant]]. Il cilindro è pieno di gas ideale di densità
$$\rho(\bar{r})=N \langle \delta(\bar{r}-\bar{r}_{i}) \rangle$$
dove $\delta$ è la [[Delta di Dirac]] tridimensionale. Dobbiamo trovare un espressione per la densità, la pressione e il potenziale chimico.
$$\rho(\bar{r})=\sum\limits_{i=1}^{N}\langle \delta(\bar{r}-\bar{r}_{i}) \rangle$$
Rendendo la somma continua
$$\int_{\mathcal{D}}d\bar{r}\rho(\bar{r})=\sum\limits_{i=1}^{N}\left\langle \int_\mathcal{D}\delta(\bar{r}-\bar{r}_{i}) \right\rangle=N_{\mathcal{D}}\;\forall\mathcal{D}$$
dove $\mathcal{D}$ è un insieme arbitrariamente piccolo e $N_{\mathcal{D}}$ è il numero di particelle nell'insieme. Allora abbiamo
$$\langle\delta(\bar{r}-\bar{r}_{i})\rangle= \frac{\int d\bar{r}\;\delta(\bar{r}-\bar{r}_{i})e^{- z/l}}{\int d\bar{r}\;e^{- z/l}}=\frac{e^{- z/l}}{\int_{A_{b}}dA\int_{0}^{?}dz\;e^{- z/l}}=\frac{e^{- z/l}}{A_{b}l(1-e^{- L_{z}/l})}$$
dove abbiamo usato l'espressione della $\delta$ in coordinate cartesiane
$$\int dx_{i}\int dy_{i}\int dz_{i} \delta(x-x_{i})\delta(y-y_{1})\delta(z-z_{1})$$
Potrebbe tornare utile avere un'espressione in coordinate sferiche
$$\delta(\bar{r}-\bar{r}_{0})= \frac{\delta(r-r_{0})\delta(\phi-\phi_{0})\delta(\cos\theta-\cos\theta_{0})}{r_{0}^{2}}$$
allora l'integrale diventa
$$\int dr\;r^{2}\int_{0}^{2\pi}d\phi\int_{-1}^{1}d\cos\theta\;\delta(\bar{r}-\bar{r}_{0})$$
Tornando alle proprietà termodinamiche abbiamo
$$\rho(\bar{r})=\frac{e^{- z/l}}{1-e^{- z/l}}$$
$$P= \frac{Nk_{B}T}{A_{b}l} \frac{-e^{- L_{z}/l}}{1-e^{- L_{z}/l}}=k_{B}T\rho(L_{z})$$
$$\mu=k_{B}T\ln\left( \frac{\lambda^{3}N}{A_{b}l} \frac{1}{1-e^{L_{z}/l}} \right)$$
