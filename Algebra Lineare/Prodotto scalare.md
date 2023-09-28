Si denota $\langle\cdot|\cdot\rangle$ il **prodotto scalare** tra due variabili (usando la [[notazione Braket]]), che ha le seguenti proprietà:
1. è lineare nel membro di destra (convenzione, i matematici usano a sinistra)
2. è antilineare nel membro di sinistra (convenzione, i matematici usano a destra)
3. $\langle v|v\rangle\geq0\;\forall\;|v\rangle\in\mathbb{C}^{n}$
4. $\langle v|v\rangle=0\Leftrightarrow|v\rangle=0$
5. $|\langle w|v\rangle\leq||w||\;||v||$ (**disuguaglianza di Cauchy-Schwartz**)
6. $\langle v|w\rangle=\overline{\langle w|v\rangle}$

Si può definire anche su spazi di funzioni come $L^{2}(\mathbb{R},dx)$. Allora presi due vettori $|\psi\rangle,|\phi\rangle$ in questo spazio vale
$$\langle\phi|\psi\rangle=\int_{\mathbb{R}}\overline{\phi(x)}\psi(x)$$
$$\langle\psi|\psi\rangle=\int_{\mathbb{R}}|\psi(x)|^{2}$$
Il prodotto scalare può anche essere applicato su matrici. Prendiamo $\hat{A},\hat{B}\in M_{2}(\mathbb{C})$ matrici $2\times2$. Considero la *traccia* della matrice $Tr(\hat{A})=\sum\limits_{i=1}^{n}A_{ii}$. E' importante notare che la traccia è *unica* e non cambia *in base alla rappresentazione* della matrice (ossia la base rispetto al quale è espressa):
$$Tr\hat{A}=\sum\limits_{i=1}^{n}\langle\psi_{i}|\hat{A}\psi_{i}\rangle\;\forall\;\mbox{base o.n.}\{|\psi_{i}\rangle\}_{i=1}^{n}\in\mathbb{C}^{n}$$
