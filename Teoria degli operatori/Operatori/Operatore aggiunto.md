---
aliases:
  - aggiunto
---
Presi due [[Spazio di Hilbert|spazi di Hilbert]] $H$ e $H'$, si dice **operatore aggiunto** $T^{+}$ (anche solo **aggiunto**, anche scritto $T^{\dagger}$) di un [[Operatore lineare]] $T:H \rightarrow H'$ un operatore per il quale vale
$$T^{+}:H'\rightarrow H\quad;\quad(y,Tx)=(T^{+}y,x)\quad\forall\;x,y\in H$$
Se l'operatore $T$ è limitato, allora ha sempre un aggiunto $T^{+}$ ed è anch'esso limitato e vale $||T||=||T^{+}||$. Inoltre, il dominio di $T^{+}$ coincide con tutto $H'$.
### Proprietà
Valgono le seguenti proprietà per due operatori limitati $T$ ed $S$
1. $(T^{+})^{+}=T$
2. $(TS)^{+}=S^{+}T^{+}$
### Forma matriciale
Dato che gli operatori aggiunti sono lineari, possono essere espressi in forma matriciale. In particolare, calcolando esplicitamente gli elementi si trova
$$(T^{+})_{ij}=(e_{i},T^{+}e_{j})=(Te_{i},e_{j})=(e_{j},Te_{i})^{*}=T_{ji}^{*}$$
ossia la matrice associata ad un operatore aggiunto è [[Matrice hermitiana|hermitiana]].