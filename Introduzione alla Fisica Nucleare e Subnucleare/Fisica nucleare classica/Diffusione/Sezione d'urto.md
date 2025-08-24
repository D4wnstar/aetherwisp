---
wiki-publish: true
---
La **sezione d'urto** $\sigma$ è definita come la probabilità che avvenga una reazione tra due [[Particella|particelle]], come per esempio una particella che impatta su un bersaglio in un acceleratore. È una misura di superficie e generalmente si misura in *barn* (b). 1 b  = $10^{-28}$ m$^{2}$. La sezione d'urto varia in funzione dell'energia delle particelle incidenti.
### Valori tipici
La sezione d'urto varia di sistema in sistema e in base all'energia delle particelle interagenti, ma gli ordini di grandezza sono grosso modo determinati dal tipo di [[Fundamental interaction]] che si va considerando:
- [[Strong interaction]]: $\sigma\sim10^{-24}$ cm$^{2}$.

In casi di particelle comuni si ha
- $\sigma_{pp}(10\text{ GeV})\sim40\text{ mb }=4\times10^{-26}\text{ cm}^{2}$ per la [[Diffusione di particelle|diffusione]] [[protone]] protone (interazione forte)
- $\sigma_{pp}(13\text{ TeV})\sim110\text{ mb}=1.1\times10^{-25}\text{ cm}^{2}$ per quella protone protone a energie più alte (interazione forte), di cui 30 mb è elastica e 80 mb è anelastica.
- $\sigma_{\nu p}(10\text{ GeV})\sim70\text{ fb}=7\times10^{-38}\text{ cm}^{2}$ per quella [[neutrino]] protone (interazione debole)

Per un fascio di particelle tipico con flusso di particelle incidenti
$$I\sim10^{14}\frac{\text{particelle}}{\text{s}\times\text{cm}^{2}}$$
che interagiscono forte ($\sigma\sim10^{-24}$ cm$^{2}$), il tasso di conversione di particelle stabili in una reattiva è $\sim10^{-10}s^{-1}$: un tasso estremamente piccolo.
## Sezione d'urto geometrica
Consideriamo una targhetta rettangolare di spessore $d$ e superficie $A$

![[Schema Sezione d'urto geometrica|center]]

su cui si scontra un fascio di particelle $a$ puntiformi a velocità $\vec{v}_{a}$. Ogni particella del bersaglio ha una sezione geometrica $\sigma_{b}$ (in unità di area) che si può determinare sperimentalmente. Quando una particella del fascio urta con una particella della targhetta, esse reagiscono. Si assume che dopo la reazione, la particella incidente sia rimossa dal fascio.

Sulla targhetta vi sono dei *centri diffusori* (che non si sovrappongono) che rappresentano le aree dove i proiettili devono entrare per urtare una particella del bersaglio. Chiamo $\dot{N}$ il numero di conteggi totali, ossia il numero di reazioni per unità di tempo, che è una misura diretta della sezione d'urto $\sigma_{b}$ dei centri diffusori. Chiamata $A$ la sezione trasversale e la densità di proiettili è $n_{a}$, il flusso incidente è
$$\Phi_{a}=n_{a}v_{a}=\frac{\dot{N}_{a}}{A}$$
che è il numero di proiettili che colpiscono il bersaglio per unità di tempo e di area. Allora la frequenza di collisione è
$$\dot{N}=\Phi_{a}N_{b}\sigma_{b}$$

Il numero totale di particelle nel bersaglio è $N_{b}=n_{b}Ad$ con $n_{b}$ è la densità di ???.

L'area che ogni centro diffusore ha a disposizione per la reazione con $a$ è la sezione d'urto geometrica
$$\sigma_{b}=\frac{\dot{N}}{\Phi_{a}N_{b}}=\frac{\text{numero di reazioni / tempo}}{\text{numero di proiettili / tempo e area }\times\text{ numero di centri diffusori }}$$
La sezione d'urto geometrica è divisibile in sezione d'urto elastica e anelastica in base al tipo di diffusione
$$\sigma_{tot}=\sigma_{el}+\sigma_{anel}$$
## Sezione d'urto differenziale
Immagino di avere un fascio che va ad incidere su un bersaglio.

![[Schema Sezione d'urto differenziale|center]]
$A_{R}$ è l'area del [[rivelatore]] posto ad una distanza $r$ e ad un angolo $\theta$ dal bersaglio. Il rivelatore copre un angolo solido $\Delta\Omega=A_{R}/r^{2}$. Il numero di conteggi totali $\dot{N}$ è dipendente dall'energia, ma anche dagli angoli:
$$\dot{N}(E,\theta,\Delta\Omega)=\mathscr{L} \frac{d\sigma(E,\theta)}{d\Omega}\Delta\Omega$$
Se posso misurare l'energia delle particelle prodotte $E'$ ho
$$\frac{d^{2}\sigma(E,E',\theta)}{d\Omega dE'}$$
e la sezione d'urto totale è
$$\sigma_{tot}(E)=\int_{0}^{E'_{mox}}\int_{4\pi} \frac{d^{2}\sigma(E,E',\theta)}{d\Omega dE'}d\Omega dE'$$
## Predizione teorica
La sezione d'urto può essere predetta dalla teoria usando la *seconda regola d'oro di Fermi*. Partiamo dal fatto che $\dot{N}$ dipende dal potenziale d'interazione, le cui caratteristiche sono contenute nell'operatore di Hamilton $\mathcal{H}_{int}$, che trasforma una [[Funzione d'onda]] iniziale $\Psi_{i}$ in una finale $\Psi_{f}$.

L'elemento di matrice della transizione è
$$\mathcal{M}_{fi}=\langle \Psi_{f}|\mathcal{H}_{int}|\Psi_{i}\rangle=\int\Psi_{f}^{*}\mathcal{H}_{int}\Psi_{i}dV$$
che ci dà l'ampiezza di probabilità. Prendiamo una particella in volume $V$ nello [[Phase space]]. Considero l'intervallo tra impulsi da $p'$ a $p'+dp$. Creo una calotta sferica $4\pi p'^{2}dp$ con volume $h^{3}=(2\pi\hbar)^{3}$. Il numero di stati finali è
$$dn(p')=\frac{4\pi p'^{2}dp'}{2\pi\hbar^{3}}V$$
L'energia differenziale è $dE'=v'dp'$, da cui posso trovare la densità di stati finali
$$\rho(E')=\frac{dn(E')}{dE'}= \frac{V4\pi p'^{2}}{v'2\pi\hbar^{3}}$$
La seconda regola d'oro di Fermi dice che il tasso di reazioni $W$, normalizzato per una particella del fascio e una del bersaglio, è pari a
$$W=\frac{2\pi}{\hbar}|\mathcal{M}_{fi}|\rho(E')$$
quindi lega il tasso di reazioni con la probabilità e la densità. Vale anche
$$W=\frac{\dot{N}(E)}{N_{b}N_{a}}=\frac{\sigma v_{a}}{V}$$
con $V=N_{a}/n_{a}$. Allora eguagliando le due formule per $W$ possiamo trovare $\sigma$ come
$$\sigma=\frac{2\pi}{\hbar v_{a}}|\mathcal{M}_{fi}|^{2}\rho(E')V$$
## Sezione d'urto di Mott
La sezione d'urto di Mott tiene conto degli [[spin]] dell'elettrone e del nucleo e di come influenzano la sezione d'urto. Vale
$$\left(\frac{d\sigma}{d\Omega}\right)_{\text{Mott}}=\left(\frac{d\sigma}{d\Omega}\right)_{\text{Rutherford}}\left[1-\beta^{2}\sin^{2}\left(\frac{\theta}{2}\right)\right]$$
con $\beta=v/c$. Con rinculo del nucleo trascurabile nel regime $\beta \rightarrow 1$ vale
$$\left(\frac{d\sigma}{d\Omega}\right)_{\text{Mott}}=\left(\frac{d\sigma}{d\Omega}\right)_{\text{Rutherford}}\cos^{2}\left(\frac{\theta}{2}\right)$$
La sezione d'urto di Mott diminuisce più rapidamente di Rutherford al crescere di $\theta$.