Partiamo in modo analogo al caso tridimensionale. Prendiamo [[Boson]] con [[spin]] 0. Immagino una griglia suddivisa in quadratini di dimensione $\frac{h}{L}$ dove $h$ è la [[costante di Planck]]. La quantità di moto è
$$\vec{p}=\frac{h}{L}(n_{x},n_{y})$$
La densità è
$$\rho= \frac{1}{V} \frac{z}{1-z}+ \frac{1}{V}\sum\limits_{|\vec{p}|>0} \frac{z}{e^{\beta \frac{p^{2}}{2m}}-z}$$
Si ha che $p>0$ e $p^{2}=\left(\frac{h}{L}\right)^{2}(n^{2}_{x}+n^{2}_{y})>0$. L'energia per quadratino è
$$\epsilon_{m}=\frac{p^{2}}{2m}= \frac{1}{2m}\left(\frac{h}{L}\right)^{2}$$
Ora calcolo
$$g(E)=\frac{1}{A}\sum\limits_{\vec{p}}\delta\left(E- \frac{p^{2}}{2m}\right)=\frac{2\pi}{A}\int dp\; \frac{p}{\left(\frac{h}{L}\right)^{2}}\delta\left(E- \frac{p^{2}}{2m}\right)=\ldots$$
Vogliamo calcolare l'integrale con la [[Delta di Dirac]] 
$$\int dx f(x)\delta(g(x)-c)=\sum\limits_{i=1}^{M}f(x_{i}) \frac{1}{|g'(x_{i})|}$$
$$\int_{0}^{\infty}dp\;p \delta\left(E- \frac{p^{2}}{2m}\right)=\sqrt{2mE} \frac{1}{\frac{\sqrt{2mE}}{m}}=m$$
Quindi tornando al calcolo di $g$ 
$$g(E)=\frac{2\pi m}{h^{2}}\theta(E)$$
La densità per quadratino è
$$\rho_{m}=\int dE\;g(E) \frac{z}{e^{\beta E}-z}=\frac{2\pi m}{h^{2}}\int_{\epsilon_{m}}^{\infty}dE\; \frac{z}{e^{\beta E}-z}$$
Risolviamo l'integrale separatamente
$$\int_{\epsilon_{m}}^{\infty}dE\; \frac{2e^{-\beta E}}{1-ze^{-\beta E}}==\int_{\epsilon_{m}}^{\infty}dE\; \frac{1}{\beta} \frac{d}{dE}\ln(1-ze^{-\beta E})=\frac{1}{\beta}\ln(1-ze^{-\beta E})\Big|_{\epsilon_{m}}^{\infty}=$$
$$=-k_{B}T\ln(1-ze^{-\beta \epsilon_{m}})$$
usando che
$$\frac{d}{dE}\ln(1-ze^{-\beta E})= \frac{ze^{-\beta E}}{(1-ze^{-\beta E})}\beta$$
Tornando alla densità
$$\rho_{m}=\frac{-2\pi m}{h^{2}}k_{B}T\ln(1-ze^{\beta \epsilon_{m}})$$
Nel [[Limite termodinamico]] si ha
$$\rho_{m}=- \frac{1}{\lambda^{2}_{T}}\ln(1-z)$$
