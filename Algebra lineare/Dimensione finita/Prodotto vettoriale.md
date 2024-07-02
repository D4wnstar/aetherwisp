Il **prodotto vettoriale** è un operazione tra due vettori che produce un terzo vettore [[Ortogonalità|ortogonale]] a entrambi. Presi due vettori $\vec{a}$ a $\vec{b}$ in $\mathbb{R}^{3}$, il prodotto vettoriale si denota
$$\vec{c}=\vec{a}\times\vec{b}=|\vec{a}|\ |\vec{b}|\sin\theta\ \hat{n}$$
dove $\theta$ è l'angolo tra i due vettori e $\hat{n}$ è il versore perpendicolare a $\vec{a}$ e $\vec{b}$. La direzione di $\vec{c}$ può essere intuita usano la regola della mano destra.
### Proprietà
Il prodotto vettoriale ha le seguenti proprietà:
1. è distributivo, ossia $\vec{a}\times(\vec{b}+\vec{c})=\vec{a}\times\vec{b}+\vec{a}\times\vec{c}$
2. è antisimmetrico, ossia $\vec{a}\times\vec{b}=-\vec{b}\times\vec{a}$
3. il prodotto vettoriale di un vettore per sé stesso è sempre nullo, ossia $\vec{a}\times\vec{a}=0$
### Rappresentazione matriciale
Nel caso tridimensionale, dati due vettori $\vec{a}$ e $\vec{b}$, il prodotto scalare $\vec{a}\times\vec{b}$ può essere rappresentato mediante la [[Matrice simmetrica|matrice antisimmetrica]] di $\vec{a}$
$$C(\vec{a})=\begin{pmatrix}0 & -a_{3} & a_{2} \\ a_{3} & 0 & -a_{1} \\ -a_{2} & a_{1} & 0\end{pmatrix}$$
e quindi il prodotto scalare è l'applicazione della matrice su $\vec{b}$:
$$\vec{a}\times\vec{b}=C(\vec{a})\vec{b}=\begin{pmatrix}0 & -a_{3} & a_{2} \\ a_{3} & 0 & -a_{1} \\ -a_{2} & a_{1} & 0\end{pmatrix}\begin{pmatrix}b_{1} \\ b_{2} \\ b_{3}\end{pmatrix}=\begin{pmatrix}a_{2}b_{3}-a_{3}b_{2} \\ a_{3}b_{1}-a_{1}b_{3} \\ a_{1}b_{2}-a_{2}b_{1}\end{pmatrix}$$

I [[Cartesian coordinates|coordinate cartesiane]] in particolare, è possibile un'ulteriore rappresentazione in forma di una pseudomatrice. Chiamati $\hat{i}$, $\hat{j}$ e $\hat{k}$ i versori della terna cartesiana, il prodotto scalare può essere calcolato come il [[determinante]] della pseudomatrice
$$\vec{a}\times\vec{b}=\begin{vmatrix}\hat{i} & \hat{j} & \hat{k} \\ a_{1} & a_{2} & a_{3} \\ b_{1} & b_{2} & b_{3}\end{vmatrix}$$
che può essere risolto, ad esempio, con la [[regola di Sarrus]]:
$$\vec{a}\times\vec{b}=(a_{2}b_{3}-a_{3}b_{2})\hat{i}+(a_{3}b_{1}-a_{1}b_{3})\hat{j}+(a_{1}b_{2}-a_{2}b_{1})\hat{k}$$
che dà lo stesso risultato di sopra.
### Interazione con rotazioni
Il prodotto vettoriale è distributivo rispetto ad una [[Rotation|rotazione]] $R$:
$$(R\vec{a})\times(R\vec{b})=R(\vec{a}\times\vec{b})$$
