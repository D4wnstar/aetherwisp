La **matrice di densità** o **densità statistica** $\hat{\rho}$ è una matrice $2\times2\in\mathbb{C}^{2\times2}$ che è la forma più generale di una matrice con [[traccia]] unitaria. È definita in forma matriciale come l'[[operatore]]
$$\hat{\rho}=\pmatrix{\rho & \sigma \\ \sigma^{*} & 1-\rho}$$
dove $\rho\in[0,1]$ e $\sigma\in\mathbb{C}$.
### Proprietà
La matrice di densità ha traccia unitaria, ossia
$$\text{Tr}(\hat{\rho})=1$$
Detti $\rho_{1}$ e $\rho_{2}$ gli [[Equazione agli autovalori|autovalori]] della matrice, il suo determinante e traccia sono
$$\det(\hat{\rho})=\rho_{1}\rho_{2}, \quad \text{Tr}(\hat{\rho})=\rho_{1}+\rho_{2}$$
La matrice di densità è [[Matrice hermitiana|autoaggiunta]]:
$$\hat{\rho}=\overline{\hat{\rho}^{T}}$$
### Rappresentazione di Bloch
È possibile rappresentare la matrice di densità in forma più compatta usando le [[matrici di Pauli]]. Chiamando $\vec{r}=(r_{1},r_{2},r_3)$ un vettore qualunque detto **vettore di Bloch**, si ha
$$\hat{\rho}= \frac{1+\vec{r}\cdot\vec{\sigma}}{2}$$
con $\vec{\sigma}=(\sigma_{1},\sigma_{2},\sigma_{3})$ il vettore contente le tre matrici di Pauli. Questa si chiama **rappresentazione di Bloch**.

Possiamo invertire la formula per trovare le componenti di $r$ in funzione di $\rho$ e $\sigma$:
$$r_{1}=2 \text{Re}(\sigma),\quad r_{2}=-2\text{Im}(\sigma), \quad r_{3}=2\rho-1$$
o anche esprimere $\rho$ e $\sigma$ in funzione di queste componenti
$$\rho=\frac{1+r_{3}}{2}, \quad \sigma=\frac{r_{1}-ir_{2}}{2}$$
e anche il determinante
$$\det(\hat{\rho})=\frac{1-||\vec{r}||^{2}}{4}$$
da cui si nota che il determinante è positivo solo se $||\vec{r}||^{2}\leq1$, ossia che il vettore sia racchiuso entro una sfera unitaria, detta **sfera di Bloch**.

Per avere un determinante nullo, $||\vec{r}||^{2}=1$, ossia il vettore deve essere proprio sulla sfera di Bloch. In questo caso, dato che $\hat{\rho}$ ha traccia nulla, deve avere autovalori 0 e 1. Ma questo implica che $\hat{\rho}$ non sia altro che un [[proiettore]]. Infatti, sapendo che è anche autoaggiunta, possiamo [[Operatore lineare|decomporla]] come
$$\hat{\rho}=\rho_{1}|\rho_{1}\rangle\langle \rho_{1}|+\rho_{2}|\rho_{2}\rangle\langle \rho_{2}|=\rho_{1}\hat{P}_{\rho_{1}}+\rho_{2}\hat{P}_{\rho_{2}}$$
e se diciamo che $\rho_{1}=1$ e $\rho_{2}=0$ questa si riduce a
$$\hat{\rho}=|\rho_{1}\rangle\langle \rho_{1}|$$
Più in generale, per ogni proiettore possiamo associare un vettore di Bloch tale per cui
$$\hat{\rho}=\hat{P}_{\rho_{1,2}}=\frac{1+\vec{r}_{1,2}\cdot\vec{\sigma}}{2}$$

Se non vale la $||\vec{r}||^{2}=1$, allora la scrittura precedente non è valida. Tuttavia, è possibile trovare un modo per ritrovare quella forma anche per $||\vec{r}||^{2}\leq1$. In questo caso, vale
$$\hat{\rho}=\frac{1+r}{2} \frac{1+\hat{r}\cdot\vec{\sigma}}{2}+ \frac{1-r}{2} \frac{1-\hat{r}\cdot\vec{\sigma}}{2}$$
che è la decomposizione spettrale di $\hat{\rho}$ se
$$P_{\rho_{1,2}}=\frac{1\pm\vec{r}\cdot\sigma}{2}$$
sono due proiettori ortogonali fra loro. Perché ciò sia vero, deve essere $P_{\rho_{1}}P_{\rho_{2}}=0$ e $P^{2}_{\rho_{1,2}}=P_{\rho_{1,2}}$. Dimostriamo l'[[ortogonalità]]:
$$P_{\rho_{1}}P_{\rho_{2}}=\frac{1+\hat{r}\cdot\vec{\sigma}}{2}\frac{1-\hat{r}\cdot\vec{\sigma}}{2}=\frac{1}{4}[1-(\hat{r}\cdot\vec{\sigma})(\hat{r}\cdot\vec{\sigma})]=\ldots$$
Si dimostra che $(\hat{r}\cdot\vec{\sigma})(\hat{r}\cdot\vec{\sigma})=(\hat{r}\cdot\hat{r}+i(\hat{r}\times\hat{r})\cdot\vec{\sigma})$, quindi
$$\ldots=\frac{1}{4}[1-(\hat{r}\cdot\hat{r}+i(\hat{r}\times\hat{r})\cdot\vec{\sigma})]=0$$
dato che $\hat{r}\cdot\hat{r}=1$ e $\hat{r}\times\hat{r}=0$. Per l'idempotenza si ha
$$P^{2}_{\rho_{1,2}}=\frac{1}{4}[1\pm2\hat{r}\cdot\vec{\sigma}+(\hat{r}\cdot\vec{\sigma})^{2}]=\frac{1}{4}(2\pm2\hat{r}\cdot\vec{\sigma})=\frac{1}{2}(1\pm\hat{r}\cdot\vec{\sigma})=P_{\rho_{1,2}}$$
dato che $(\hat{r}\cdot\vec{\sigma})^{2}=1$. Abbiamo quindi dimostrato che $\hat{\rho}$ è una combinazione di proiettori, in particolare una con coefficienti positivi la cui somma è unitaria. Questo particolare tipo di combinazione si dice [[combinazione convessa]].

Possiamo ora cercare i vettori associati a questi proiettori. Questi sono, in generale, del tipo
$$|\rho_{1},\rho_{2}\rangle=\pmatrix{a_{\pm} \\ b_{\pm}}$$
e quindi i proiettori in generale sono
$$P_{\rho_{1,2}}=|\rho_{1},\rho_{2}\rangle\langle \rho_{1},\rho_{2}|=\pmatrix{|a_{\pm}|^{2} & a_{\pm}b_{\pm} \\ a^{*}_{\pm}b_{\pm} & |b_{\pm}|^{2}}$$
ma questa matrice deve avere la forma
$$P_{\rho_{1,2}}=\frac{1\pm\vec{r}\cdot\vec{\sigma}}{2}=\pmatrix{1\pm \frac{r_{1}}{r} & \pm \frac{r_{1}-ir_{2}}{2r} \\ \pm \frac{r_{1}+ir_{2}}{2r} & 1\mp \frac{r_{3}}{r}}$$
Confrontando i termini della diagonale si trovano due condizioni sui moduli:
$$a_{\pm}=e^{i\phi_{\pm}}\sqrt{\frac{1}{2}\left(1\pm \frac{r_{3}}{r}\right)}, \quad b_{\pm}=e^{i\psi_{\pm}}\sqrt{\frac{1}{2}\left(1\mp \frac{r_{3}}{r}\right)}$$
e una differenza di fase confrontando i termini non diagonali:
$$a_{\pm}b_{\pm}^{*}=e^{i(\phi_{\pm}-\psi_{\pm})} \frac{1}{2}\sqrt{1- \frac{r_{3}^{2}}{r^{2}}}=\pm \frac{r_{1}-ir_{2}}{2r}=\pm e^{-i\arctan(r_{2}/r_{1})}\sqrt{\left(\frac{r_{1}}{r}\right)^{2}+ \left(\frac{r_{2}}{r}\right)^{2}}$$
e confrontando il secondo e quarto termine
$$e^{i(\phi_{\pm}-\psi_{\pm})} \frac{1}{2}\sqrt{1- \frac{r_{3}^{2}}{r^{2}}}=\pm e^{-i\arctan(r_{2}/r_{1})}\sqrt{\left(\frac{r_{1}}{r}\right)^{2}+ \left(\frac{r_{2}}{r}\right)^{2}}$$
I moduli devono essere uguali per costruzione, quindi rimangono solo le fasi
$$e^{i(\phi_{\pm}-\psi_{\pm})}=\pm e^{-i\arctan(r_{2}/r_{1})}$$
e allora
$$e^{i\psi_{\pm}}=\pm e^{i(\phi_{\pm}+\arctan(r_{2}/r_{1}))}$$
e infine, esplicitando i vettori generici, si ha
$$\pmatrix{a_{\pm} \\ b_{\pm}}=e^{i\phi_{\pm}}\pmatrix{\sqrt{\frac{1}{2}\left(1\pm \frac{r_{3}}{r}\right)} \\ \pm e^{i\arctan(r_{2}/r_{1})}\sqrt{\frac{1}{2}\left(1\mp \frac{r_{3}}{r}\right)}}$$
La fase totale $e^{i\arctan(r_{2}/r_{1})}$ non dà alcuna informazione, in quanto scompare nel calcolo della matrice del proiettore essendo moltiplicata per la sua coniugata, quindi è trascurabile. Questi due vettori sono effettivamente gli autovettori del proiettore.

---

$$\hat{\rho}=\sum\limits_{i=1}^{\infty}P_{\psi}^{A}(a_{i})|a_{i}\rangle\langle a_{i}|=\sum\limits_{i=1}^{\infty}|\langle a_{i}|\psi\rangle|^{2}|a_{i}\rangle\langle a_{i}|=\sum\limits_{i=1}^{\infty}\langle a_{i}|\psi\rangle \langle \psi|a_{i}\rangle |a_{i}\rangle\langle a_{i}|$$
$$=\sum\limits_{i=1}^{\infty}|a_{i}\rangle\langle a_{i}|\hat{P}_{\psi}|a_{i}\rangle\langle a_{i}|=\sum\limits_{i=1}^{\infty}\hat{P}^{A}_{a_{i}}\hat{P}_{\psi}^{A}\hat{P}^{A}_{a_{i}}$$
$\hat{\rho}$ è un *[[operatore semidefinito positivo]]*, dunque si ha
$$\langle \psi|\hat{\rho}\psi\rangle=\sum\limits_{\alpha}\lambda_{\alpha}\langle \psi|\hat{P}_{\alpha}\psi\rangle\geq0$$
$$\langle \psi|\psi_\alpha\rangle \langle \psi_{\alpha}|\psi\rangle=|\langle \psi_{\alpha}|\psi\rangle|^{2}\geq 0$$
In [[rappresentazione spettrale]] è
$$\hat{\rho}=\sum\limits_{\alpha}\lambda_{\alpha}\hat{P}_{\alpha}=\sum\limits_{\alpha}\lambda_{\alpha} |\psi_{\alpha}\rangle\langle \psi_{\alpha}|$$
Cerco la traccia di $\hat{\rho}$ 
$$\mbox{Tr}\hat{\rho}=\sum\limits_{\alpha}\lambda_{\alpha}=1$$
$$\hat{P}_{\alpha}=|\psi_{\alpha}\rangle\langle \psi_{\alpha}||\psi\rangle\langle \psi|=1$$
$$\hat{P}=|\psi_{i}\rangle\langle \psi_\alpha||\psi\rangle\langle \psi|=0$$
con $\psi_{i}$ ket della base e sapendo che $\psi_{i} \perp \psi_{\alpha}$ sono ortogonali.