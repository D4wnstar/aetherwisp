Nel caso di sistemi quantistici, è più facile calcolare l'ensemble gran canonico che quello canonico.

# Gran canonico quantistico
...

$$\beta P=\frac{1}{V}\ln Z=\frac{1}{V}\sum\limits_{\alpha}\sigma\ln(1+\sigma e^{-\beta \epsilon_{\alpha}}z)=\frac{1}{V}\sum\limits_{\alpha}\sigma\ln(1+\sigma e^{-\beta(\epsilon_{\alpha}-\mu)})$$
con $z=e^{\beta \mu}$ la *fugacità*. Si ha
$$Z=\sum\limits_{n=0}^{\infty}e^{\beta\mu n}\sum\limits_{\{n_{\alpha}\}}\delta\left(n-\sum\limits_{\alpha}n_{\alpha}\right)e^{-\beta E \{n_{\alpha}\}}$$
Cerco la media
$$\langle n_{\gamma} \rangle=- \frac{\partial \ln Z}{\beta\partial \epsilon_{\gamma}}= \frac{1}{Z}\left\{- \frac{1}{\beta} \frac{\partial Z}{\beta\partial \epsilon_{\gamma}}\right\}=$$
$$=\frac{1}{Z}\left\{\sum\limits_{N=0}^{\infty} e^{\beta\mu N} \sum\limits_{\{n_{\alpha}\}} \delta\left(N-\sum\limits_{\alpha}n_{\alpha}\right)e^{-\beta E \{n_{\alpha}\}} \left[- \frac{1}{\beta} \frac{\partial }{\beta\partial \epsilon_{\alpha} }(-\beta E \{n_{\alpha}\})\right]\right\}=$$
$$=\frac{1}{Z}\left\{ \sum\limits_{N=0}^{\infty}e^{\beta \mu N}\sum\limits_{\{n_{\alpha}\}} \delta(N-\sum\limits_{\alpha}n_{\alpha})e^{-\beta E_{\alpha}n_{\alpha}y}n_{\gamma} \right\}$$

Usando la formula per $\ln Z$ troviamo
$$\langle n_{\gamma} \rangle=- \frac{1}{\beta}\frac{\partial }{\partial \epsilon_{\gamma}}\sum\limits_{\sigma}\sigma\ln(1+\sigma e^{-\beta \epsilon_{\alpha}}z)=- \frac{1}{\beta} \frac{\partial }{\partial \epsilon_{\alpha}}[\sigma\ln(1+\sigma e^{-\beta \epsilon_{\gamma}})z]=$$
$$=\frac{\sigma}{1+\sigma e^{-\beta \epsilon_{\gamma}}z}\sigma e^{-\beta \epsilon_{\gamma}}z= \frac{z}{e^{\beta \epsilon_{\gamma}}+\sigma z}$$
che ci dà l'*occupazione media dello stato*.
Questa formula cambia per [[fermioni]] e [[bosoni]]
$$\mbox{Fermioni: }\frac{1}{e^{\beta(E_{\gamma}-\mu)}+1}\quad\mbox{Bosoni: }\frac{1}{e^{\beta(E_{\gamma}-\mu)}-1}$$
ossia si ha $z=1$ e cambia il segno al denominatore.

Esiste un terzo tipo (teorico) di particelle chiamate *boltzmannioni*. Se prendiamo le funzioni di occupazioni di stato $\varphi_{\alpha_{1}}(x_{1})\varphi_{\alpha_{2}}(x_{2})\ldots\varphi_{\alpha_{N}}(x_{N})$ abbiamo
$$g \{n_{\alpha}\}= \frac{N!}{\prod\limits_{\alpha}n_{\alpha}!} \Rightarrow \tilde{g}\{n_{\alpha}\}=\frac{1}{N!} \frac{N!}{\prod_{\alpha}n_{\alpha}!}= \frac{1}{\prod_{\alpha}n_{\alpha}!}$$
$$Z_{\alpha}=\sum\limits_{N=0}^{\infty}e^{\beta \mu N}\sum\limits_{\{n_{\alpha}\}}\delta\left(N-\sum\limits_{\alpha}n_{\alpha}\right) \frac{1}{\prod\limits_{\alpha}n_{\alpha}!}e^{- \beta\sum\limits_{\alpha}n_{\alpha}\epsilon_{\alpha}}=$$
$$=\sum\limits_{\{n_{\alpha}\}}e^{\beta \mu \sum\limits_{\alpha}n_{\alpha}}\sum\limits_{\{n_{\alpha}\}}\delta\left(N-\sum\limits_{\alpha}n_{\alpha}\right) \prod\limits_{\alpha} \frac{e^{-\beta n_{\alpha}\epsilon_{\alpha}}}{n_{\alpha}!}=\sum\limits_{\{n_{\alpha}\}}\prod\limits_{\alpha}\frac{e^{-\beta(\epsilon_{\alpha} -\mu)n_{\alpha}}}{n_{\alpha}!}$$
Calcolo
$$Z_{B}=\sum\limits_{n_{1}}\sum\limits_{n_{2}}\ldots\prod\limits_{\alpha} \frac{e^{-\beta (\epsilon_{\alpha}-\mu)n_{\alpha}}}{n_{\alpha}!}=\prod\limits_{\alpha}\exp(e^{-\beta(\epsilon_{\alpha}-\mu)})$$
$$\frac{1}{V} \ln Z_{B}= \frac{1}{V}\sum\limits_{\alpha}\ln[\exp(e^{-\beta (\epsilon_{\alpha}-\mu)})]=\frac{1}{V}\sum\limits_{\alpha}e^{-\beta(\epsilon_{\alpha}-\mu)}$$
Si trova analogamente a sopra
$$\langle n_{\gamma}^{B} \rangle=e^{-\beta(\epsilon_\alpha-\mu)}$$
In conclusione, per *temperature finite*, abbiamo
$$\beta P=\frac{1}{V}\ln Z=\frac{1}{V}\sum\limits_{\alpha}\sigma\ln(1+\sigma e^{-\beta \epsilon_{\alpha}}z)$$
$$\rho= \frac{\langle N \rangle}{V}=\sum\limits_{\alpha} \frac{\langle n_{\alpha} \rangle}{V} =\sum\limits_{\alpha} \frac{1}{V} \frac{1}{\frac{e^{\beta \epsilon_{\alpha}}}{z}+\sigma}=\frac{1}{V}z \frac{\partial \ln Z}{\partial z}$$
## Proprietà a temperature prossime a 0
Vogliamo trovare una relazione tra lo [[stato fondamentale]] del sistema e le proprietà di meccanica statistica nel caso di temperature che tendono allo zero. Ci aspettiamo che convergano. Partiamo dall'[[Potenziali termodinamici#Energia libera di Helmholtz|energia libera di Helmholzt]].
$$A(N,T,V)=E(N,T,V)-TS(N,T,V)\quad T \rightarrow 0$$
Consideriamo lo stato fondamentale per i [[bosoni]] con [[spin]] 0. Abbiamo $\alpha = \bar{p}$. Supponiamo di avere $N$ particelle. Descriviamo l'energia come
$$E=\sum\limits_{\bar{p}}n_{p}\epsilon_{p}$$
dove c'è il vincolo che $\sum n_{p}=n$. In questo caso, $e_{p}=p^{2}/2m$ e $\bar{p}=\frac{h}{L}(n_{x},n_{y},n_{z})$.
Cerchiamo la densità
$$\rho= \frac{1}{V}\sum\limits_{\bar{p}} \frac{1}{\frac{e^{\beta \frac{p^{2}}{2m}}}{z}-1}=\frac{1}{V} \frac{z}{1-z} + \frac{1}{V}\sum\limits_{|\bar{p}|>0} \frac{z}{e^{\beta \frac{p^{2}}{2m}}-z}$$
dove la fugacità $z<1$.
Ci aspettiamo che $\rho$ tenda a $\frac{1}{V} \frac{z}{1-z}$ per $T \rightarrow 0,\; V \rightarrow 0$. In altre parole vogliamo che
$$\rho= \frac{1}{V} \frac{z}{1-z} \Rightarrow \rho_{0}$$
con $\rho_{0}$ al densità di particelle ad impulso nullo.
Uguagliando i due membri
$$\rho_{0}=\frac{1}{V} \frac{z}{1-z}\Rightarrow N_{0}= \frac{z}{1-z} \Rightarrow z=(1-z)N_{0}$$
$$z(1+N_{0})=N_{0} \Rightarrow z= \frac{N_{0}}{1+N_{0}}$$
$$z= \frac{1}{1+\frac{1}{N_{0}}}\simeq 1- \frac{1}{N_{0}}$$
Quindi la fugacità è dipendente solo dal numero medio di particelle a impulso nullo.