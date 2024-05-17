Prendo un'[[Hamiltoniana]] nello spazio delle fasi $PS$, $H:PS \rightarrow \mathbb{R}$.
$$\phi=(q,p)\quad;\quad\dot{\phi}=\{\phi,H\}$$
Prendo una funzione qualunque dallo spazio delle fasi, $F:PS \rightarrow \mathbb{R}$ 
$$\frac{d\phi}{d\alpha}=\phi'=\{\phi_{\alpha},F\}$$
Questo sono trasformazioni nello *spazio delle fasi in meccanica classica*.

Usando un operatore quantistico $\hat{x}$ ho
$$\frac{d\hat{x}_{t}}{dt}=\frac{i}{\hbar}[\hat{H},\hat{x}_{t}]$$
e
$$\frac{d\hat{x}_{t}}{d\alpha} =\frac{i}{\hbar}[\hat{F},\hat{x}_{\alpha}]$$
Queste sono trasformazioni *di operatori in meccanica quantistica*.

La derivata della funzione $F$ è
$$\dot{F}=\dot{q}\partial_{q}F+\dot{p}\partial_{p}F=\ldots$$
ma usando
$$\begin{cases}
\dot{q}=\frac{\partial H}{\partial p} \\
\dot{p}=-\frac{\partial H}{\partial q}
\end{cases}$$
$$\ldots=\partial_{p}H\partial_{q}F-\partial_{q}H\partial_{p}F=\{F,H\}$$
Trovo la derivata per $\alpha$ dell'Hamiltoniana
$$H'=\frac{dH}{d\alpha}=q'\partial_{q}H+q'\partial_{p}H=\{H,F\}$$
Allora posso enunciare il **teorema di Noether**:
> Il generatore di una [[trasformazione di simmetria|trasformazione continua di simmetria]] è una quantità conservata (cioè una [[costante del moto]]). Ogni costante del moto genera una trasformazione continua di simmetria.

Usando gli operatori $\hat{H}$ e $\hat{F}$ si ha, per estensione
$$\hat{H}'=\frac{d\hat{H}_{\alpha}}{d\alpha}=\frac{i}{\hbar}[\hat{F},\hat{H}_{\alpha}]=\frac{i}{\hbar}\hat{V}_{\alpha}^{\dagger}[\hat{F},\hat{H}]\hat{V}_{\alpha}$$
$$\dot{\hat{F}}=\frac{d\hat{F}_{t}}{dt}=\frac{i}{\hbar}[\hat{H},\hat{F}_{t}]=\frac{i}{\hbar}\hat{U}_{t}^{\dagger}[\hat{H},\hat{F}]\hat{U}_{t}$$
usando che $\hat{F}_{t}=\hat{U}_{t}^{\dagger}\hat{F}\hat{U}_{t}$ e $\hat{H}_{\alpha}=\hat{V}_{\alpha}^{\dagger}\hat{H}\hat{V}_{\alpha}$, con $\hat{U}_{t}=e^{- \frac{i}{\hbar}t \hat{H}}$ e $\hat{V}_{\alpha}=e^{- \frac{i}{\hbar}\alpha\hat{F}}$.
### Forma generale
Il teorema di Noether può essere generalizzato. La sua forma più generale è
$$\text{simmetria} \Leftrightarrow \text{legge di conservazione}$$
Quindi per ogni simmetria esiste una legge di conservazione associata ad essa, e per ogni legge di conservazione esiste una simmetria.