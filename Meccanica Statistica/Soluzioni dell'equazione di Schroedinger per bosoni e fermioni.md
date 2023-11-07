Nel caso di $N$ particelle, la soluzione dell'[[equazione di Schroedinger]] ha la forma
$$\psi(x_{1},\ldots,x_{N})=\varphi(x_{1})\varphi(x_{2})\ldots\varphi(x_{N})$$
Usando le [[Hamiltoniana|Hamiltoniane]] 
$$\hat{H}_{i}= \frac{\hat{p}^{2}_{i}}{2m};\quad \hat{H}=\sum\limits_{i=1}^{N} \frac{\hat{p}^{2}_{i}}{2m}$$
si ha
$$\hat{H}_{i}\varphi_{\alpha}(x_{i})=\mathcal{E}_{\alpha}\varphi_{\alpha}(x_{i})$$
e quindi
$$H\psi=E\psi$$
con $E=\sum\limits_{i=1}^{N}\mathcal{E}_{\alpha,i}$. Queste soluzioni non valgono nel caso di fermioni o bosoni, tuttavia. Cerchiamo delle buone funzioni risolutive per entrambi i casi.
## Fermioni
Per i fermioni parto da
$$\frac{1}{\sqrt{N!}}\sum\limits_{P}(-1)^{P}\varphi_{\alpha,i}(x_{P(1)})\varphi_{\alpha,2}(x_{P(2)})\ldots\varphi_{\alpha,N}(x_{P(N)})= \frac{1}{\sqrt{N!}}\det[\varphi_{\alpha,i}(x_{i})]$$
Il determinante è
$$\det\begin{pmatrix}\varphi_{\alpha,1}(x_{1}) & \varphi_{\alpha,1}(x_{2}) & \cdots & \varphi_{\alpha,1}(x_{N})  \\ \varphi_{\alpha,2}(x_{1}) & \varphi_{\alpha,2}(x_{2}) & \cdots & \varphi_{\alpha,2}(x_{N}) \\ \vdots & \vdots & & \vdots \\ \varphi_{\alpha,N}(x_{1}) & \varphi_{\alpha,N}(x_{2}) & \cdots & \varphi_{\alpha,N}(x_{N})\end{pmatrix}$$
## Bosoni
Nel caso di bosoni parto da
$$\psi(x_{1},\ldots,x_{N})\propto \sum\limits_{P}\varphi_{\alpha,1}(x_{P(1)})\ldots\varphi_{\alpha,N}(x_{P(N)})$$
Qui invece di uscire il determinante esce un'altra proprietà della matrice chiamata *permanente*.