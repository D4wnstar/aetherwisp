---
aliases:
  - L^2
  - L^1
  - L^p
---
Si chiamano **spazi** $L^{p}$ gli spazi di funzioni [[Integrale secondo Lebesgue|integrabili secondo Lebesgue]]. Sono tutti [[Spazio di Banach|spazi di Banach]] e $L^{2}$ in particolare è uno [[Spazio di Hilbert]]. Più formalmente, sono rappresentati con la notazione $L^{p}(\mathcal{H},dx)$ dove $\mathcal{H}$ è lo spazio su cui sono definite le funzioni (in genere $\mathbb{R}$ o $\mathbb{C}$) e $dx$ rappresenta la [[measure|misura]] di Lebesgue. È comune abbreviare a solo $L^{p}(\mathcal{H})$ o solo $L^{p}$.
### Spazio $L^1$
Si definisce **spazio** $L^{1}(I)$ l'insieme di tutte le funzioni **sommabili** o **integrabili** su un intervallo $I$, ovvero le funzioni $f$ tali per cui vale
$$\int_{I}|f(x)|dx<+\infty$$
Lo spazio $L^{1}$ è [[Spazio metrico completo|completo]] rispetto alla [[Norma#Norme canoniche|norma]] $L^{1}$ in dimensione infinita (**teorema di Riesz**). In particolare, è la chiusura dello spazio $C^{0}(I)$ delle funzioni continue su $I$ rispetto a tale norma.
### Spazio $L^{2}$
Si definisce **spazio** $L^{2}(I)$ l'insieme di tutte le funzioni **a quadrato sommabile** o **a quadrato integrabile** su un intervallo $I$, ovvero le funzioni $f$ tali per cui vale
$$\int_{I}|f(x)|^{2}dx<+\infty$$
Lo spazio $L^{2}(I)$ è anche uno [[Vector space]] con uno [[Prodotto scalare]] definito come
$$(f,g)=\int_{I}f^{*}(x)g(x)dx$$
e l'integrale esiste finito per qualunque coppia di funzione $L^{2}(I)$. Solo nel caso in cui $I$ è un intervallo finito, vale che se $f\in L^{2}(I)$ allora vale anche $f\in L^{1}(I)$, ma non vale il viceversa. Lo spazio $L^{2}(I)$ è anche completo rispetto alla [[Norma#Norme canoniche|norma]] $L^{2}$ in dimensione infinita (**teorema di Riesz-Fischer**). In particolare, è la chiusura dello spazio $C^{\infty}(I)$ delle funzioni regolari su $I$ rispetto a tale norma.

Tutti gli spazi $L^{2}$ sono separabili. Inoltre, il sottospazio $C^{\infty}$ è denso in tutti gli spazi $L^{2}$. In particolare negli spazi $L^{2}(\mathbb{R})$ e $L^{2}(0,+\infty)$ è anche denso il sottospazio $C^{\infty}$ delle funzioni che "decrescono esponenzialmente" all'infinito.
### Spazi $L^{p}$
In generale, preso un sottoinsieme misurabile $I$ di $\mathbb{R}^{N}$, si definisce **spazio** $L^{p}$ lo spazio di tutte le funzioni tali per esiste finito l'integrale
$$\int_{I}|f(x)|^{p}dx$$
