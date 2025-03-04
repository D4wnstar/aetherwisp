---
aliases:
  - prodotto hermitiano
---
Si denota $(v,w)$, $v\cdot w$ o $\langle v|w \rangle$ (in [[notazione braket]]) il **prodotto scalare** tra due variabili $v$ e $w$ appartenenti ad uno [[Vector space]]. Se le variabili $v$ e $w$ sono complesse, si dice anche **prodotto hermitiano**.

In spazi vettoriali a dimensione finita, come $\mathbb{R}^{N}$ o $\mathbb{C}^{N}$, il prodotto scalare è definito come una somma di prodotti delle componenti dei vettori. Siano $v,w$ due vettori dello spazio, allora il prodotto scalare tra i due è
$$\langle v|w\rangle=\sum\limits_{i=0}^{N}v_{i}w_{i}$$
che può anche essere espresso come
$$\langle v|w\rangle=vw\cos\theta$$
dove $\theta$ è l'angolo tra i due vettori.

Si può definire anche su spazi a dimensione infinita, come gli [[spazio di Hilbert|spazi di Hilbert]] o gli [[Spazi Lp]] come $L^{2}(\mathbb{R},dx)$. Allora presi due vettori $|\psi\rangle,|\phi\rangle$ in questo spazio vale
$$\langle\phi|\psi\rangle=\int_{\mathbb{R}}\overline{\phi(x)}\psi(x)$$
$$\langle\psi|\psi\rangle=\int_{\mathbb{R}}|\psi(x)|^{2}$$
### Proprietà
Ha le seguenti proprietà:
1. è lineare nel membro di destra (convenzione, i matematici usano a sinistra), ossia $\langle v|\alpha w + \beta z\rangle=\alpha \langle v|w\rangle+\beta \langle v|z\rangle$. 
2. è antilineare nel membro di sinistra (convenzione, i matematici usano a destra), ossia $\langle \alpha v + \beta w|z\rangle=\alpha^{\ast} \langle v|w\rangle+\beta^{\ast} \langle v|z\rangle$
3. è distributivo, ossia $\langle v|w+u\rangle=\langle v|w\rangle+\langle v|z\rangle$
4. $\langle v|v\rangle\geq0\;\forall\;|v\rangle\in\mathbb{C}^{n}$
5. $\langle v|v\rangle=0\Leftrightarrow|v\rangle=0$
6. $\langle w|v\rangle\leq||w||\;||v||$ (detta [[disuguaglianza di Cauchy-Schwarz]])
7. $\langle v|w\rangle=\overline{\langle w|v\rangle}$
8. è continuo, ossia presa una successione $\{x_{n}\}$ convergente a $x\in \mathcal{H}$ con $\mathcal{H}$ uno [[Spazio di Hilbert]], vale che per ogni $y\in \mathcal{H}$ si ha $\lim\limits_{n \rightarrow \infty}(y,x_{n})=(y,x)$
### In basis expression
Consider the vectors $\mathbf{v}_{1}$ and $\mathbf{v}_{2}$ in some vector space $V$ equipped with a [[basis]] $\{ \mathbf{e}_{1},\ldots,\mathbf{e}_{n} \}$. They can be expressed as a [[linear combination]] of basis vectors as $\mathbf{v}_{1}=\sum_{i=1}^{n}\alpha_{i}\mathbf{e}_{i}$ and $\mathbf{v}_{2}=\sum_{j=1}^{n}\beta_{j}\mathbf{e}_{j}$, using suitable values $\alpha_{i}$ and $\beta_{i}$. The scalar product between these two is
$$\begin{align}
\mathbf{v}_{1}\cdot \mathbf{v}_{2}&=\left( \sum_{i=1}^{n} \alpha_{i}\mathbf{e}_{i} \right)\cdot\left( \sum_{j=1}^{n} \beta_{j}\mathbf{e}_{j} \right)=\sum_{i=1}^{n} \alpha_{i}\mathbf{e}_{i}\cdot\left( \sum_{j=1}^{n} \beta_{j}\mathbf{e}_{j} \right)= \\
&=\sum_{i=1}^{n} \alpha_{i}\sum_{j=1}^{n} \beta_{j}(\mathbf{e}_{i}\cdot \mathbf{e}_{j})=\sum_{i=1}^{n}\sum_{j=1}^{n} \alpha_{i}\beta_{j}\delta_{ij}= \\
&=\sum_{i=1}^{n} \alpha_{i}\underbrace{ (\beta_{1}\delta_{i1}+\ldots+\beta_{n}\delta_{in}) }_{ \beta_{i}\delta_{ii} }=\sum_{i=1}^{n} \alpha_{i}\beta_{i}
\end{align}$$
using the [[Delta di Kronecker]].
### Su matrici
Il prodotto scalare può anche essere applicato su matrici. Prendiamo $\hat{A},\hat{B}\in M_{2}(\mathbb{C})$ matrici $2\times2$. Considero la *traccia* della matrice $Tr(\hat{A})=\sum\limits_{i=1}^{n}A_{ii}$. E' importante notare che la traccia è *unica* e non cambia *in base alla rappresentazione* della matrice (ossia la base rispetto al quale è espressa):
$$Tr\hat{A}=\sum\limits_{i=1}^{n}\langle\psi_{i}|\hat{A}\psi_{i}\rangle\;\forall\;\mbox{base o.n.}\{|\psi_{i}\rangle\}_{i=1}^{n}\in\mathbb{C}^{n}$$
La matrice $\hat{U}=[\langle \psi_{k}|\phi_{i}\rangle]$ è unitaria, ossia $\hat{U}\hat{U}^{\dagger}=\hat{\mathbb{1}}=\hat{U}^{\dagger}\hat{U}$.

Prendendo $|\psi\rangle,|\phi\rangle\in\mathbb{C}^{N}$. Il prodotto scalare possiamo scriverlo come
$$\langle \psi|\phi\rangle=\sum\limits_{i=1}^{n}\psi^{\ast}_{i}\phi_{i}=\sum\limits_{i=1}^{n}\langle \psi|\chi_{i}\rangle\langle \chi_{i}|\phi\rangle=\ldots$$usando una base ortonormale $\{|\chi_{i}\rangle\}^{n}_{i=1}\in\mathbb{C}^{N}$ da cui, usando la completezza dei [[Proiettore|proiettori]]
$$\ldots=\langle \psi|\underbrace{\left( \sum\limits_{i=i}^{n}\hat{P}_{\chi_{i}}\right)}\limits_{\hat{\mathbb{1}}}|\phi\rangle$$
Possiamo generalizzare a $|\psi\rangle,|\phi\rangle\in L^{2}(\mathbb{R},dx)$, ricordando che $\psi^{\ast}_{i}=\overline{\langle \chi_{i}|\psi\rangle}$,
$$\langle \psi|\phi\rangle=\int_{\mathbb{R}}\psi^{\ast}(x)\phi(x)dx=\int_{\mathbb{R}}\langle \psi|x\rangle \langle x|\phi\rangle=\ldots$$
ma possiamo descrivere $\phi(x)$ come
$$\phi(x)=\int \delta(\bar{x}-x)\phi(\bar{x})d\bar{x}$$
Si ha inoltre
$$\int_{\mathbb{R}}|x\rangle\langle x|dx=\hat{\mathbb{1}}$$
dove $|x\rangle\langle x|$ è uno *pseudoproiettore* di una base di pseudovettori. Allora tornando indietro
$$\ldots=\langle \psi|\left( \int_{\mathbb{R}}|x\rangle\langle x| dx\right)|\phi\rangle$$
