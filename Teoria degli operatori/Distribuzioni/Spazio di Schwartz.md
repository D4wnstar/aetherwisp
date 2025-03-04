Si dice **spazio di Schwartz**, indicato con $\mathcal{S}$, lo [[Vector space]] costituito dalle funzioni $\varphi$ infinitamente derivabili e a *decrescenza rapida* in tutte le derivate, ovvero tali che, per ogni $h,k\in\mathbb{N}$ si ha
$$\sup\limits_{x\in\mathbb{R}}\left|x^{h} \frac{d^{k}\varphi}{dx^{k}}\right|<+\infty$$
In altre parole, la funzione e tutte le sue derivate decrescono *più velocemente* di qualunque potenza. Le funzioni $\varphi$ si dicono **funzioni test** o **funzioni di Schwartz**.

Si introduce il seguente concetto di convergenza in questo spazio: presa $\{\varphi_{n}\}$ una successione di funzioni in $\mathcal{S}$, si dice che $\{\varphi_{n}\}\rightarrow0$ in $\mathcal{S}$ se, per ogni $h,k\in\mathbb{N}$ fissati, si ha
$$x^{h} \frac{d^{k}\varphi_{n}}{dx^{k}}\rightarrow0\quad\text{ per }\quad n \rightarrow \infty$$
con [[Convergenza uniforme]]. Ovviamente vale anche $\varphi_{n} \rightarrow \varphi$ se $(\varphi_{n}-\varphi)\rightarrow 0$. Usando questa definizione di convergenza, lo spazio di Schwartz è [[Spazio metrico completo|completo]] in quanto ogni successione $\{\varphi_{n}\}\in\mathcal{S}$ converge ad una $\varphi\in\mathcal{S}$.