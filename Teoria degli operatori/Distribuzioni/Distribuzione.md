Una **distribuzione** o **funzione generalizzata** è un oggetto matematico che generalizza il concetto di funzione. Una distribuzione agisce non su un punto del suo dominio, come una funzione, bensì per integrazione su una **funzione di test**. Una distribuzione $T$ agisce su una funzione di test $\varphi$ con
$$\int_{I}T\varphi(x) dx$$
### Esempi
Tutte le funzioni localmente [[Spazi Lp|sommabili]] $u(x)\in L^{1}_{loc}(\mathbb{R})$, cioè sommabili su ogni sottoinsieme compatto del dominio, e limitate sono distribuzioni. Le costanti, l'onda quadra, seno e coseno e la [[theta di Heaviside]] sono tutte di questo tipo. L'integrale
$$\int_{-\infty}^{+\infty}u(x)\varphi(x)dx$$
esiste per ogni $\varphi\in\mathcal{S}$ ed è un funzionale lineare di $\mathcal{S}$ in $\mathbb{C}$. Inoltre, se $\varphi_{n}\rightarrow\varphi$, l'integrale converge, le $\varphi_{n}$ convergono a $\varphi$ anche in senso $L^{1}(\mathbb{R})$ e $u(x)$ individua una [[Distribuzione temperata]] $T_{u}\in\mathcal{S}'$:
$$T_{u}(\varphi)=\int_{-\infty}^{+\infty}u(x)\varphi(x)dx=\langle T_{u},\varphi\rangle\tag{1}$$
e chiamiamo $T_u$ la distribuzione *associata alla funzione $u(x)$* o distribuzione con *densità $u(x)$*. Una distribuzione che non è associata a nessuna funzione si dice *singolare*.

Ogni funzione $L^{1}(\mathbb{R})$ individua una distribuzione tramite la (1). Lo stesso vale per $L^{2}(\mathbb{R})$, dove la (1) è proprio il [[Prodotto scalare]] in $L^{2}$ (più correttamente sarebbe $(u^{*},\varphi)$).