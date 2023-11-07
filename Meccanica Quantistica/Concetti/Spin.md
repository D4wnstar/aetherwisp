Lo **spin** è un concetto necessario per la corretta descrizione di una particella elementare, come l'elettrone. Esso è rappresentato come un vettore in tre dimensioni.
$$\hat{\bar{S}}=(\hat{S}_{x},\hat{S}_{y},\hat{S}_{z})$$
Vale
$$\frac{\hat{S}}{\frac{\hbar}{2}}|\sigma\rangle=\sigma |\sigma\rangle;\quad\sigma=\pm 1$$
Considero
$$\hat{I}=\sum\limits_{x}|x\rangle\langle x|\sum\limits_{\sigma}|\sigma\rangle\langle \sigma|$$
$$\hat{I}|\psi\rangle=\sum\limits_{x,\sigma}(|x\rangle\otimes |\sigma\rangle)(\langle x|\otimes \langle \sigma|)|\psi\rangle$$
Allora
$$\psi(x,\sigma)=(\langle x|\otimes \langle \sigma|)|\psi\rangle$$
che ci dà la generalizzazione della [[funzione d'onda]] che tiene conto anche dello spin per una singola particella. Nel caso di tante particelle, diventa
$$\psi(x_{1},\sigma_{1};x_{2},\sigma_{2};\ldots;x_{N},\sigma_{N})=\langle \bar{r}_{i},\sigma_{i}|\equiv x_{i}$$
Si hanno casi diversi in base alla particella che si considera. Per i bosoni si ha
$$\psi(x_{1},x_{2},\ldots,x_{i},\ldots,x_{j},\ldots,x_{N})=\psi(x_{1},x_{2},\ldots,x_{j},x_{i},\ldots,x_{N})$$
Nel caso di fermioni si ha
$$\psi(x_{1},x_{2},\ldots,x_{i},\ldots,x_{j},\ldots,x_{N})=-\psi(x_{1},x_{2},\ldots,x_{j},x_{i},\ldots,x_{N})$$
dove c'è un segno meno rispetto a quella dei bosoni.