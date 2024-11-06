La **disuguaglianza di Schwarz-Hölder** è una generalizzazione della [[Disuguaglianza di Cauchy-Schwarz]] agli spazi a dimensione infinita, in particolare gli [[Spazio di Hilbert|spazi di Hilbert]].

Siano $f\in L^{p}(I)$ e $g\in L^{q}(I)$ funzioni appartenenti agli spazi [[Spazi Lp|L^p]], dove $p$ e $q$ sono numeri tali che $1/p+1/q=1$. Allora il prodotto $fg$ è [[Spazi Lp#Spazio $L 1$|sommabile]] e vale la disuguaglianza
$$\int_{I}|fg|dx\leq\left[\int_{I}|f|^{p}dx\right]^{1/p}\left[\int_{I}|g|^{q}dx\right]^{1/q}$$

Nel caso importante per cui $f\in L^{2}(I)$ e $g\in L^{2}(I)$, la disuguaglianza prende la forma
$$\int_{I}|fg|dx\leq \sqrt{\int_{I}|f|^{2}dx \int_{I}|g|^{2}dx}$$
e scrivendolo usando la notazione della [[Norma]] è
$$||fg||_{L^{1}}^{2}\leq ||f||_{L^{2}}||g||_{L^{2}}$$

La disuguaglianza è saturata quando una funzione è multiplo dell'altra, ossia $g=cf$ con $c$ una costante.