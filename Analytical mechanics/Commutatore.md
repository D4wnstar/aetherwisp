---
aliases:
  - anticommutatore
  - formula di Baker-Campbell-Hausdorff
---
Il **commutatore** è un valore che indica quanto due elementi legati da un'operazione binaria non soddisfano la proprietà commutativa. Nel caso della moltiplicazione, presi due elementi $A$ e $B$, il loro commutatore è
$$[A,B]=AB-BA$$
che è pari a 0 se e solo se vale la proprietà commutativa tra $A$ e $B$ (e dunque $AB=BA$).

Si dice **anticommutatore** l'operazione con segno opposto
$$\{A,B\}=AB+BA$$
### Proprietà
Valgono numerose proprietà del commutatore. Le principali sono:
1. $[A+B,C]=[A,C]+[B,C]$
2. $[AB,C]=ABC-CAB$
3. $[A,A]=0$, quindi un elemento commuta sempre con se stesso.
4. $[A,B]=-[B,A]$, detta *anticommutatività*.
5. $[A,[B,C]]+[B,[C,A]]+[C,[A,B]]=0$, detta *identità di Jacobi*.
6. $[A,B]^{+}=-[A,B]$, con $^{+}$ l'[[Operatore aggiunto|aggiunto]].

Nel caso specifico di [[Operatore|operatori]], tutti gli operatori commutano con qualunque costante. Un'operatore commuta anche con qualunque sua funzione, nel senso che l'operatore $A$ e una sua funzione $f(A)$ commutano: $[A,f(A)]=0$.

Se due operatori non commutano per una costante, ossia $[A,B]=c \hat{\mathbf{1}}$, allora vale la **formula di Baker-Campbell-Hausdorff**:
$$e^{A+B}=e^{-[A,B]/2}e^{A}e^{B}$$
quindi compare un termine correttivo $e^{-[A,B]/2}$ nel suddividere una somma di operatori all'esponente.

Nel caso di due funzioni operatori $e^{-A}$  e $e^{A}$ applicate su un altro operatore $B$, si possono usare gli **commutatori annidati**:
$$\begin{align}
e^{A}Be^{-A}&=\sum_{k=0}^{\infty} \frac{1}{k!}\underbrace{ [A,[A, \ldots[A,B] }_{ k \text{ volte} }\ldots]] \\
&=B+[A,B]+ \frac{1}{2}[A,[A,B]]+ \frac{1}{3!}[A,[A,[A,B]]]+\ldots
\end{align}$$

> [!example] Dimostrazione
>Possiamo espandere in serie le funzioni separatamente:
> $$\begin{align}
> &\quad\left( 1+A+ \frac{A^{2}}{2}+\ldots \right)B\left( 1-A+ \frac{A^{2}}{2} +\ldots\right)= \\
> &=\left( 1+A+ \frac{A^{2}}{2}+\ldots \right)\left( B-BA+ B \frac{A^{2}}{2}+\ldots \right)= \\
> &=B-BA+ \frac{BA^{2}}{2}+ AB-ABA- \frac{A^{2}}{2}B+\ldots= \\
> &=B+[A,B]+ \left( \frac{1}{2}BA^{2}- ABA + \frac{1}{2}A^{2}B \right)+\ldots \\
> &=B+[A,B]+[A,[A,B]]+\ldots
> \end{align}$$

Vale anche per $e^{A}f(B)e^{-A}$ dato che $e^{A}f(B)e^{-A}=f(e^{A}Be^{-A})$.
### In meccanica quantistica
Il commutatore è di importanza primaria nella meccanica quantistica, dove permette di esprimere numerosi concetti relativi al [[Disuguaglianza di Heisenberg|principio di indeterminazione]]. La relazione commutativa più importante della materia è la cosiddetta **relazione commutativa canonica**, che dimostra che l'operatore posizione e l'operatore quantità di moto non commutano:
$$[\hat{q},\hat{p}]=i\hbar$$
con $\hbar$ la [[Costante di Planck|costante di Planck ridotta]]. Più correttamente si ha
$$[\hat{q},\hat{p}]=i\hbar \mathbf{\hat{1}}$$
dove $\mathbf{\hat{1}}$ è l'operatore identità, di solito omesso per comodità ma necessario perché un operatore deve essere pari ad un altro operatore, non uno scalare.

> [!example] Dimostrazione
> Consideriamo lo [[spazio di Hilbert]] [[Spazi Lp|L^2]] su $\mathbb{R}$ e ci interessiamo al commutatore $[\hat{q},\hat{p}]$ entro di esso. Il commutatore qui è definito $[\hat{q},\hat{p}]:L^{2}(\mathbb{R})=\mathcal{H}\to \mathcal{H}$. Allora per una [[funzione d'onda]] generica $\psi(x)$ (gli operatori devono agire su *qualcosa*) si ha
> $$([\hat{q},\hat{p}]\psi)(x)=(\hat{q}\hat{p}\psi)(x)-(\hat{p}\hat{q}\psi)(x)=x(\hat{p}\psi)(x)+i\hbar \partial_{x}(\hat{q}\psi)(x)=\ldots$$
> ricordando che gli operatori agiscono sempre su quello che hanno alla loro destra. Continuando
> $$\ldots=-i\hbar x\partial _{x}\psi(x)+i\hbar\partial_{x}(x\psi(x))=-\cancel{ i\hbar x\partial_{x}\psi(x) }+i\hbar \psi(x)+\cancel{ i\hbar x\partial_{x}(x) }$$
> e quindi
> $$([\hat{q},\hat{p}]\psi(x))=i\hbar \psi(x)$$
> che, essendo vero per ogni $\psi(x)\in L^{2}(\mathbb{R})$, ci permette di dire
> $$[\hat{q},\hat{p}]=i\hbar$$

In tre dimensioni si hanno, per le variabili $\vec{r}$ e $\vec{p}$,
$$[r_{i},p_{j}]=-[p_{i},r_{j}]=i\hbar\delta_{ij}, \quad [r_{i},r_{j}]=[p_{i},p_{j}]=0$$
con gli indici che si riferiscono alle tre dimensioni spaziali. In altre parole, la posizione commuta sempre con la posizione; la quantità di moto commuta sempre con la quantità di moto; tra di loro commutano solo in coordinate diverse, altrimenti si ha $i\hbar$.

Per il [[momento angolare quantistico]] sull'asse $z$ $L_{z}$ valgono
$$[L_{z},x]=i\hbar y, \quad [L_{z},y]=-i\hbar x, \quad [L_{z},z]=0$$
$$[L_{z},p_{x}]=i\hbar p_{y}, \quad [L_{z},p_{y}]=-i\hbar p_{x}, \quad [L_{z},p_{z}]=0$$
