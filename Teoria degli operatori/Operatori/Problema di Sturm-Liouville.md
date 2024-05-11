Un **problema di Sturm-Liouville** è un'[[Equazione agli autovalori]] associata all'equazione
$$\frac{1}{\rho(x)}\left[\frac{d}{dx}\left(p(x) \frac{d}{dx}\right)-q(x)\right]u(x)+\lambda u(x)=0\tag{1}$$
per la funzione $u(x)$, dove $p(x),q(x)$ e $\rho(x)$ sono funzioni "abbastanza regolari" in un intervallo finito $[\alpha,\beta]$. La $u(x)$ deve anche soddisfare una condizione agli estremi, come l'annullamento agli estremi
$$u(\alpha)=u(\beta)=0\tag{2}$$
Altre condizioni agli estremi, come l'annullamento della derivata o periodicità, sono comunque valide.
### Soluzioni
Ci si aspetta che la $u(x)$ soddisfi la $(1)$ solo per certi $\lambda$ nelle condizioni $(2)$. Stiamo studiando l'[[Operatore]]
$$T=- \frac{1}{\rho(x)}\left[\frac{d}{dx}\left(p(x) \frac{d}{dx}\right)-q(x)\right]$$
che è non limitato nello [[Spazi Lp#Spazio $L {2}$|spazio]] $L^{2}(\alpha,\beta)$ e generalizza l'operatore derivata seconda $-d^{2}/dx^{2}$, che si ottiene ponendo $\rho(x)=p(x)=1$ e $q(x)=0$.

Supponiamo che le funzioni $p,q,\rho$ verifichino le seguenti condizioni
$$p(x)>0\text{, classe }C^{1}$$
$$q(x)\geq0,\;\rho(x)>0\text{ entrambe continue}$$
Grazie alla positività di $\rho(x)$ possiamo definire il [[Prodotto scalare]] pesato
$$(f,g)_{\rho}=\int_{\alpha}^{\beta}\rho(x)f^{*}(x)g(x)dx\tag{3}$$
Si trova che $T$ è [[Operatore autoaggiunto|simmetrico]] rispetto a questo prodotto scalare nel sottoinsieme [[Spazio denso|denso]] in $L^{2}(\alpha,\beta)$ delle funzioni due volte derivabili in $L^{2}$ e soddisfacenti la $(2)$. Allora se $u_{1}(x)$ e $u_{2}(x)$ sono autofunzioni di $T$, e dunque soluzioni della $(1)$, sono ortogonali a $\rho(x)$
$$(u_{1},u_{2})_{\rho}=\int_{\alpha}^{\beta}u_{1}^{*}(x)u_{2}(x)\rho(x)dx$$
Allora si hanno i seguenti risultati
1. Gli autovalori del problema di Sturm-Liouville sono tutti reali e maggiori di zero
2. Le corrispondenti autofunzioni $\{u_{n}(x)\}_{n\geq1}$, che sono ortogonali fra loro nel prodotto scalare $(3)$, formano un [[Sistema ortonormale completo|sistema completo]] nello spazio, relativo alla [[Norma]] indotta dal prodotto scalare.
Ciò significa che una funzione $f$ tale che
$$\int_{\alpha}^{\beta}|f|^{2}\rho\;dx<+\infty$$
può essere sviluppata in [[Serie di Fourier]] di tali autofunzioni $u_{n}$
$$f=\sum\limits_{n=1}^{\infty}a_{n}u_{n}$$
e per $N \rightarrow\infty$ si ha
$$\int_{\alpha}^{\beta}\left|f-\sum\limits_{n=1 }^{N}a_{n}u_{n}\right|^{2}\rho\;dx \rightarrow0$$
cioè la serie di Fourier converge in *media del secondo ordine rispetto alla densità $\rho$*. I coefficienti $a_{n}$ possono essere calcolati come
$$(u_{m},f)_{\rho}=\sum\limits_{n}a_{n}(u_{m},u_{n})\rho=a_{m}(u_{m},u_{m})_\rho=a_{m}||u_{m}||^{2}_{\rho}$$
Valgono anche altri risultati
1. Gli autovalori sono crescenti e $\lambda_{n}\rightarrow\infty$.
2. Se $\lambda_{1}$ è il più piccolo degli autovalori, la corrispondente autofunzione $u_{1}(x)$ si annulla solo nei punti $x=\alpha$ e $x=\beta$.
3. Vale il **teorema di monotonia**: mantenendo inalterate le $p,q,\rho$ ma riducendo l'intervallo $[\alpha,\beta]$ a $[\alpha',\beta']$ con $\alpha<\alpha'<\beta'<\beta$, aumentano tutti gli autovalori. Lo stesso accade aumentando $p$ e/o $q$ o diminuendo $\rho$.
4. Vale il **teorema di separazione**: dette $u_{n},u_{m}$ due autosoluzioni con autovalori $\lambda_{n},\lambda_{m}$ rispettivamente, se $\lambda_{n}>\lambda_{m}$ allora fra due zeri consecutivi di $u_{m}$ cade almeno uno zero di $u_{n}$.
5. Vale il **teorema di oscillazione**: supponendo di aver ordinato gli autovalori $\lambda_{n}$ in ordine crescente, la $n$-esima autosoluzione $u_{n}$ ha $n-1$ zeri nell'intervallo aperto $\alpha,\beta$, ossia $n+1$ includendo gli estremi $x=\alpha$ e $x=\beta$.
### Esempi
L'[[Equazione di Schrödinger]] indipendente dal tempo, unidimensionale, per una particella quantistica soggetta a potenziale $V(x)$ è del tipo $(1)$
$$\left[- \frac{d^{2}}{dx^{2}}+V(x)\right]u(x)=\lambda u(x)$$
Le corrispondenti autofunzioni formano un sistema completo, che garantisce che uno stato può essere espresso come sovrapposizione (cioè serie di Fourier) degli autostati dell'operatore energia.

L'[[Equazione di d'Alembert]] in due dimensioni
$$\left(\frac{\partial ^{2}}{\partial x^{2}}+\frac{\partial ^{2}}{\partial y^{2}}\right)u(x,y;t)=\frac{1}{v^{2}}\frac{\partial^{2} u}{\partial t^{2}}(x,y;t)$$
può rappresentare un problema di Sturm-Liouville.