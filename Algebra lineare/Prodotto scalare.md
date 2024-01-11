Si denota $\langle v|w \rangle$ il **prodotto scalare** tra due variabili (usando la [[notazione Braket]], altrimenti $(v,w)$ o $v\cdot w$), che ha le seguenti proprietà:
1. è lineare nel membro di destra (convenzione, i matematici usano a sinistra), ossia $\langle v|\alpha w + \beta z\rangle=\alpha \langle v|w\rangle+\beta \langle v|z\rangle$. 
2. è antilineare nel membro di sinistra (convenzione, i matematici usano a destra), ossia $\langle \alpha v + \beta w|z\rangle=\alpha^{\ast} \langle v|w\rangle+\beta^{\ast} \langle v|z\rangle$
3. $\langle v|v\rangle\geq0\;\forall\;|v\rangle\in\mathbb{C}^{n}$
4. $\langle v|v\rangle=0\Leftrightarrow|v\rangle=0$
5. $\langle w|v\rangle\leq||w||\;||v||$ (detta **disuguaglianza di Cauchy-Schwarz**)
6. $\langle v|w\rangle=\overline{\langle w|v\rangle}$

Si può definire anche su spazi di funzioni come $L^{2}(\mathbb{R},dx)$. Allora presi due vettori $|\psi\rangle,|\phi\rangle$ in questo spazio vale
$$\langle\phi|\psi\rangle=\int_{\mathbb{R}}\overline{\phi(x)}\psi(x)$$
$$\langle\psi|\psi\rangle=\int_{\mathbb{R}}|\psi(x)|^{2}$$
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
