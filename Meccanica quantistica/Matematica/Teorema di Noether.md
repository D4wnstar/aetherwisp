Il **teorema di Noether** è un risultato fondamentale che associa trasformazioni della dinamica di un sistema con leggi di conservazione.

Consideriamo un'Hamiltoniana $\hat{H}$ definita nell'[[algebra]] dei [[operatore|operatori]] unitari $\mathcal{B}(\mathcal{H})$, con $\mathcal{H}$ uno [[spazio di Hilbert]]. Consideriamo anche un operatore $\hat{G}:\mathcal{H}\to \mathcal{H}$ definita nella stessa algebra che genera una trasformazione di $\hat{H}$ in $\alpha$. Allora, l'evoluzione temporale di $\hat{G}$ e $\hat{H}$ sono
$$\frac{d}{dt}\hat{G}_{t}=\frac{i}{\hbar}[\hat{H},\hat{G}_{t}],\qquad \frac{d}{d\alpha}\hat{H}_{\alpha}=i[\hat{G},\hat{H}]$$
L'Hamiltoniana trasforma altri operatori nel tempo, gli altri operatori trasformano l'Hamiltoniana in altri parametri. Se $\hat{G}_{t}=\hat{G}$ commuta con $\hat{H}$, quindi $[\hat{G}_{\alpha},\hat{H}]=0$, allora è una [[costante del moto]]. Detto questo, possiamo enunciare il teorema di Noether

> [!info] Teorema di Noether
> Presa un'Hamiltoniana $\hat{H}$ e un operatore $\hat{G}_{\alpha}$, se $\hat{G}_{\alpha}$ genera una [[Trasformazione di simmetria|simmetria]] di $\hat{H}$ in un parametro $\alpha$, allora è una costante del moto. In simboli,
> $$\hat{G}_{\alpha}^{+}\hat{H}\hat{G}_{\alpha}=\hat{H}_{\alpha}=\hat{H}\quad \Leftrightarrow \quad [\hat{G}_{\alpha},\hat{H}]=0$$


> [!info] Teorema di Noether
> Il generatore di una [[Trasformazione di simmetria|trasformazione continua di simmetria]] è una quantità conservata (cioè una [[costante del moto]]). Ogni costante del moto genera una trasformazione continua di simmetria.
### In meccanica quantistica
Consideriamo due [[operatore|operatori]], l'[[Hamiltoniana]] $\hat{H}$ e $\hat{\pi}$, che [[Commutatore|commutano]]: $[\hat{H},\hat{\pi}]=0$, e l'[[equazione di Schrödinger]] indipendente dal tempo
$$\hat{H}\ket{\psi_{E}} =E\ket{\psi_{E}} $$
ma se i due operatori commutano possiamo scrivere
$$\hat{H}\hat{\pi}\ket{\psi_{E} }=\hat{\pi}\hat{H}\ket{\psi_{E}} =\hat{\pi}(E\ket{\psi_{E}} )=E \hat{\pi}\ket{\psi_{E}}$$
$$\hat{H}\hat{\pi}\ket{\psi_{E}} =E\hat{\pi}\ket{\psi_{E}} \quad\Rightarrow \quad \hat{H}\ket{\psi_{E}^{\pi}}=E\ket{\psi_{E}^{\pi}}  $$
quindi la commutatività con l'Hamiltoniana può comportare una [[degenerazione]] degli [[Equazione agli autovalori|autostati]] se $\ket{\psi_{E}}\neq \ket{\psi_{E}^{\pi}}$.

---

Usando gli operatori $\hat{H}$ e $\hat{F}$ si ha, per estensione
$$\hat{H}'=\frac{d\hat{H}_{\alpha}}{d\alpha}=\frac{i}{\hbar}[\hat{F},\hat{H}_{\alpha}]=\frac{i}{\hbar}\hat{V}_{\alpha}^{\dagger}[\hat{F},\hat{H}]\hat{V}_{\alpha}$$
$$\dot{\hat{F}}=\frac{d\hat{F}_{t}}{dt}=\frac{i}{\hbar}[\hat{H},\hat{F}_{t}]=\frac{i}{\hbar}\hat{U}_{t}^{\dagger}[\hat{H},\hat{F}]\hat{U}_{t}$$
usando che $\hat{F}_{t}=\hat{U}_{t}^{\dagger}\hat{F}\hat{U}_{t}$ e $\hat{H}_{\alpha}=\hat{V}_{\alpha}^{\dagger}\hat{H}\hat{V}_{\alpha}$, con $\hat{U}_{t}=e^{- \frac{i}{\hbar}t \hat{H}}$ e $\hat{V}_{\alpha}=e^{- \frac{i}{\hbar}\alpha\hat{F}}$.
### Forma generale
Il teorema di Noether può essere generalizzato. La sua forma più generale è
$$\text{simmetria} \Leftrightarrow \text{legge di conservazione}$$
Quindi per ogni simmetria esiste una legge di conservazione associata ad essa, e per ogni legge di conservazione esiste una simmetria.