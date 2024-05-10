Lo **spin** è l'equivalente quantistico del momento angolare. Esso è rappresentato come un vettore in tre dimensioni.
$$\hat{\bar{S}}=(\hat{S}_{x},\hat{S}_{y},\hat{S}_{z})$$
Vale
$$\frac{\hat{S}}{\frac{\hbar}{2}}|\sigma\rangle=\sigma |\sigma\rangle;\quad\sigma=\pm 1$$
Considero
$$\hat{I}=\sum\limits_{x}|x\rangle\langle x|\sum\limits_{\sigma}|\sigma\rangle\langle \sigma|$$
$$\hat{I}|\psi\rangle=\sum\limits_{x,\sigma}(|x\rangle\otimes |\sigma\rangle)(\langle x|\otimes \langle \sigma|)|\psi\rangle$$
Allora
$$\psi(x,\sigma)=(\langle x|\otimes \langle \sigma|)|\psi\rangle$$
che ci dà la generalizzazione della [[Funzione d'onda]] che tiene conto anche dello spin per una singola particella. Nel caso di tante particelle, diventa
$$\psi(x_{1},\sigma_{1};x_{2},\sigma_{2};\ldots;x_{N},\sigma_{N})=\langle \bar{r}_{i},\sigma_{i}|\equiv x_{i}$$
Si hanno casi diversi in base alla particella che si considera. Per i bosoni si ha
$$\psi(x_{1},x_{2},\ldots,x_{i},\ldots,x_{j},\ldots,x_{N})=\psi(x_{1},x_{2},\ldots,x_{j},x_{i},\ldots,x_{N})$$
Nel caso di fermioni si ha
$$\psi(x_{1},x_{2},\ldots,x_{i},\ldots,x_{j},\ldots,x_{N})=-\psi(x_{1},x_{2},\ldots,x_{j},x_{i},\ldots,x_{N})$$
dove c'è un segno meno rispetto a quella dei bosoni.

Consideriamo un momento di dipolo magnetico $\hat{\vec{\mu}}$: esso dipende dallo spin con $\hat{\vec{\mu}}=-\mu_{B}g\hat{\vec{S}}$ con $\mu_{B}= \frac{e\hbar}{2mc}$ il *magnetone di Bohr*. $g$ è una costante che vale $g=2.0023$ e si chiama *fattore g*. Dunque invertendo la formula è possibile studiare lo spin in funzione del momento magnetico.
### Commutazioni
Applicando il [[commutatore]] alle componenti si ottiene
$$\begin{cases}
[S_{x},S_{y}]=i\hbar S_{z} \\
[S_{y},S_{z}]=i\hbar S_{x} \\
[S_{z},S_{x}]=i\hbar S_{y}
\end{cases}$$
che sono tutti non nulli. Non è quindi possibile costruire autostati simultanei per le componenti dello spin e quindi non è possibile misurarle simultaneamente. Si prova invece che $[S^{2},S_{z}]=0$.