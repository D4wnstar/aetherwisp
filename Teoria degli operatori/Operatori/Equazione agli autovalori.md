---
aliases:
  - autovalore
  - autovettore
  - autofunzione
---
Sia $T:H \rightarrow H$ un [[Operatore lineare]] su uno [[Spazio di Hilbert]]. L'**equazione agli autovalori** associata all'operatore $T$ di dominio $D$ è
$$Tx=\lambda x;\quad \lambda\in\mathbb{C},\quad x\neq0\in D$$
dove $\lambda$ è l'**autovalore** e $x$ è l'**autovettore**. Nel caso di spazi di funzioni, si ha $Tf=\lambda f$ e $f$ si dice **autofunzione**.
### Dimensione infinita
In dimensione infinita è impossibile fare una constatazione generale sull'esistenza degli autovettori. Ciò non dipende nemmeno dalla limitatezza dell'operatore. Vale comunque il seguente teorema: se $T$ è [[Operatore autoaggiunto|simmetrico]] e possiede qualche autovalore, allora
1. gli autovalori sono reali
2. gli autovettori relativi ad autovalori diversi sono ortogonali
In dimensione finita, è anche vero che gli autovettori formano una [[base]] dello spazio.
### Risultati utili
Se un operatore $T$ soddisfa un equazione algebrica
$$\mathcal{P}(T)=a_{n}T^{n}+\ldots+a_{0}I=0$$
con $I$ la matrice identica, allora i suoi autovalori $\lambda$ sono le soluzioni $\mathcal{P}(\lambda)=0$. Inoltre, $T$ possiede effettivamente autovettori: infatti, chiamata $\lambda_{1}$ una soluzione di $\mathcal{P}(\lambda)=0$ si ha $\mathcal{P}(T)=(T-\lambda_{1})\mathcal{Q}(T)=0$ e dunque, per qualsiasi $v\in H$, si ha $(T-\lambda_{1})\mathcal{Q}(T)v=0$. Allora se $v$ è tale che $\mathcal{Q}(T)v\neq0$ si deduce che $w:=\mathcal{Q}(T)v$ è un autovettore di $T$ con autovalore $\lambda_{1}$. Se invece $\mathcal{Q}(T)v=0$, il problema si riconduce ad un'equazione di grado $n-1$.

Se $T$ ed $S$ sono due operatori tali che $TS=ST$ e $T$ ha un autovalore $\lambda$, allora il sottospazio $V_{\lambda}$ dei corrispondenti autovettori è un sottospazio *invariante* sotto $S$, cioè $S|_{V_{\lambda}}:V_{\lambda}\rightarrow V_{\lambda}$. Infatti, per ogni $v_{\lambda}\in V_{\lambda}$ si ha $TSv_{\lambda}=STv_{\lambda}=\lambda Sv_{\lambda}$. Se $\lambda$ è *non degenere*, $v_{\lambda}$ è anche autovettore di $S$. Se inoltre $V_{\lambda}$ è di dimensione finita, valgono tutti i teoremi per le matrici (a dimensione finita).