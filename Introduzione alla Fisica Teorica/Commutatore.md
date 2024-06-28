---
aliases:
  - anticommutatore
---
Il **commutatore** è un valore che indica quanto due elementi legati da un'operazione binaria non soddisfano la proprietà commutativa. Nel caso della moltiplicazione, presi due elementi $A$ e $B$, il loro commutatore è
$$[A,B]=AB-BA$$
che è pari a 0 se e solo se vale la proprietà commutativa tra $A$ e $B$ (e dunque $AB=BA$).

Si dice **anticommutatore** l'operazione con segno opposto
$$\{A,B\}=AB+BA$$
### Proprietà
Valgono numerose proprietà del commutatore. Le principali sono:
1. $[A+B,C]=[A,C]+[B,C]$
2. $[A,A]=0$, quindi un elemento commuta sempre con se stesso.
3. $[A,B]=-[B,A]$, detta *anticommutatività*.
4. $[A,[B,C]]+[B,[C,A]]+[C,[A,B]]=0$, detta *identità di Jacobi*.

Nel caso specifico di [[Operatore|operatori]], tutti gli operatori commutano con qualunque costante. Un'operatore commuta anche con qualunque sua funzione, nel senso che l'operatore $A$ e una sua funzione $f(A)=e^{cA}$ commutano: $[A,f(A)]=0$.
### In meccanica quantistica
Il commutatore è di importanza primaria nella meccanica quantistica, dove permette di esprimere numerosi concetti relativi al [[Disuguaglianza di Heisenberg|principio di indeterminazione]]. La relazione commutativa più importante della materia è la cosiddetta **relazione commutativa canonica**, che dimostra che l'operatore posizione e l'operatore quantità di moto non commutano:
$$[\hat{x},\hat{p}]=i\hbar$$
con $\hbar$ la [[Costante di Planck|costante di Planck ridotta]].

In tre dimensioni si hanno, per le variabili $\vec{r}$ e $\vec{p}$,
$$[r_{i},p_{j}]=-[p_{i},r_{j}]=i\hbar\delta_{ij}, \quad [r_{i},r_{j}]=[p_{i},p_{j}]=0$$
con gli indici che si riferiscono alle tre dimensioni spaziali. In altre parole, la posizione commuta sempre con la posizione; la quantità di moto commuta sempre con la quantità di moto; tra di loro commutano solo in coordinate diverse, altrimenti si ha $i\hbar$.

Per il [[momento angolare quantistico]] sull'asse $z$ $L_{z}$ valgono
$$[L_{z},x]=i\hbar y, \quad [L_{z},y]=-i\hbar x, \quad [L_{z},z]=0$$
$$[L_{z},p_{x}]=i\hbar p_{y}, \quad [L_{z},p_{y}]=-i\hbar p_{x}, \quad [L_{z},p_{z}]=0$$
