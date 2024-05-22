La **teoria delle perturbazioni non degenere** è una forma della [[teoria delle perturbazioni]] indipendente dal tempo nella quale gli [[Equazione agli autovalori|autovalori]] dell'[[Hamiltoniana]] imperturbata non sono [[degenerazione|degeneri]].

Consideriamo un'Hamiltoniana del tipo
$$\hat{H}=\hat{H}^{0}+\lambda \hat{H}'$$
con $\hat{H}'$ la perturbazione e $\lambda$ una costante. $\hat{H}^{0}$ è l'Hamiltoniana non perturbata, che risolve il sistema descritto dall'[[Equazione di Schrödinger#Potenziale indipendente dal tempo|equazione di Schrödinger indipendente dal tempo]]
$$\hat{H}^{0}\psi_{n}^{0}=E_{n}^{0}\psi_{n}^{0}$$
La dinamica del sistema perturbato invece è descritto da
$$\hat{H}\psi_{n}=E_{n}\psi_{n}\tag{1}$$
### $\lambda$ piccolo
Scriviamo $\psi_{n}$ e $E_{n}$ come [[serie di potenze]] in $\lambda$:
$$\psi_{n}=\psi_{n}^{0}+\lambda\psi_{n}^{1}+\lambda^{2}\psi_{n}^{2}+\ldots=\sum\limits_{i=0}^{\infty}\lambda^{i}\psi_{n}^{i}$$
$$E_{n}=E_{n}^{0}+\lambda E_{n}^{1}+\lambda^{2}E_{n}^{2}+\ldots=\sum\limits_{i=0}^{\infty}\lambda^{i}E_{n}^{i}$$
$\psi_{n}^{0}$ e $E_{n}^{0}$ sono i termini non perturbati, mentre quelli successivi sono le correzioni di $i$-esimo ordine. Sostituendo queste due nella $(1)$ e omettendo i cappucci si ha
$$(H^{0}+\lambda H')\left(\sum\limits_{i=0}^{\infty}\lambda^{i}\psi_{n}^{i}\right)=\left(\sum\limits_{i=0}^{\infty}\lambda^{i}E_{n}^{i}\right)\left(\sum\limits_{i=0}^{\infty}\lambda^{i}\psi_{n}^{i}\right)$$
E usando il prodotto di Cauchy
$$\sum\limits_{i=0}^{\infty}\lambda^{i}H^{0}\psi_{n}^{i}+\sum\limits_{i=0}^{\infty}\lambda^{i+1}H'\psi_{n}^{i}=\sum\limits_{i=0}^{\infty}\sum\limits_{j=0}^{i}\lambda^{j}\lambda^{i-j}E_{n}^{j}\psi_{n}^{i-j}=\sum\limits_{i=0}^{\infty}\lambda^{i}\sum\limits_{j=0}^{i}E_{n}^{j}\psi_{n}^{i-j}$$
Definiamo $k=i+1$ e Nella sommatoria con $H'$ e estraiamo i primi termini nelle altre due sommatorie
$$H^{0}\psi_{n}^{0}+\sum\limits_{k=1}^{\infty}\lambda^{k}(H^{0}\psi_{n}^{k}+H'\psi_{n}^{k-1})=E_{n}^{0}\psi_{n}^{0}+\sum\limits_{k=1}^{\infty}\lambda^{k}\sum\limits_{j=0}^{k}E_{n}^{j}\psi_{n}^{k-j}$$
Esplicitando i primi termini si ha
$$\begin{align}
H^{0}\psi_{n}^{0}+\lambda (H^{0}\psi_{n}^{1}+H'\psi_{n}^{0})+\lambda^{2}(H^{0}\psi_{n}^{2}+H'\psi_{n}^{1})+\ldots \\
=E^{0}_{n}\psi_{n}^{0}+\lambda(E_{n}^{0}\psi_{n}^{1}+H^{1}_{n}\psi_{n}^{0})+\lambda^{2}(E_{n}^{0}\psi_{n}^{2}+E_{n}^{1}\psi_{n}^{1}+E_{n}^{2}\psi_{n}^{0})+\ldots
\end{align}$$
Eguagliando i termini con $k$ uguale ritroviamo
$$H^{0}\psi_{n}^{0}=E_{n}^{0}\psi_{n}$$
che è il sistema non perturbato, ma anche
$$\sum\limits_{k=1}^{\infty}\lambda^{k}(H^{0}\psi_{n}^{k}+H'\psi_{n}^{k-1})=\sum\limits_{k=1}^{\infty}\lambda^{k}\sum\limits_{j=0}^{k}E_{n}^{j}\psi_{n}^{k-j}$$
che sono le correzioni di $k$-esimo ordine.