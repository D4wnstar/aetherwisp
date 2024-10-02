---
aliases:
  - rappresentazione di Schrödinger
  - rappresentazione di Heisenberg
  - rappresentazione di interazione
  - rappresentazione di Dirac
---
La meccanica quantistica possiede un certo "grado di libertà" nella sua rappresentazione. È possibile formulare i risultati della teoria quantistica, in particolare dell'evoluzione temporale, in più modi equivalenti, detti **rappresentazioni** o ***picture***. Esistono tre rappresentazioni: la **rappresentazione di Schrödinger**, quella **di Heisenberg** e quella **di interazione**.
### Rappresentazione di Schrödinger
La rappresentazione di Schrödinger è definita ponendo la dipendenza temporale nello [[stato]] del sistema, lasciando invece gli [[Operatore|operatori]] costanti nel tempo. In simboli, preso uno stato $|\psi\rangle$, esso evolve nel tempo mediante l'applicazione dell'[[evolutore]] $U_{t}$ come
$$|\psi_{t}\rangle=U_{t}|\psi\rangle$$
dove $|\psi_{t}\rangle$ rappresenta lo stato al tempo $t$. La dinamica del sistema è determinata dall'[[equazione di Schrödinger]]:
$$i\hbar \frac{\partial }{\partial t}|\psi_{t}\rangle=\hat{H}|\psi_{t}\rangle$$
Il valor medio di un'[[osservabile]] $Q$ al tempo $t$ è quindi definito semplicemente come
$$\left\langle Q \right\rangle_{t}=\langle \psi_{t}|\hat{Q}|\psi_{t}\rangle$$
La [[Matrice di densità]] $\rho$ varia nel tempo come
$$\rho_{t}=U_{t}\rho U_{t}^{+}$$
### Rappresentazione di Heisenberg
La rappresentazione di Heisenberg è definita ponendo la dipendenza temporale negli operatori associati alle [[Osservabile|osservabili]], lasciando invece lo stato costante nel tempo. Preso un'operatore $\hat{A}$, esso evolve nel tempo come
$$\hat{A}(t)=U_{t}^{+}\hat{A}U_{t}$$
e la dinamica è determinata dall'[[equazione di Heisenberg]]:
$$\frac{d}{dt}\hat{A}_{H}(t)=\frac{i}{\hbar}[\hat{H},\hat{A}_{H}(t)]+\left(\frac{\partial }{\partial t}\hat{A}_{S}(t)\right)_{H}$$
Il valor medio di un'osservabile $Q$ al tempo $t$ è allora
$$\left\langle Q \right\rangle_{t}=\langle \psi|\hat{Q}(t)|\psi\rangle$$
La matrice densità $\rho$ è invece costante nel tempo.
### Rappresentazione di interazione
La rappresentazione di interazione, anche detta rappresentazione di Dirac, è una via di mezzo tra le due rappresentazioni precedenti, dove la dipendenza temporale e suddivisa tra stato e operatori. È particolarmente utile per descrivere l'effetto di perturbazioni al sistema (ossia interazioni, da cui il nome) nel tempo nella [[teoria delle perturbazione dipendente dal tempo]].

Presa un'[[Hamiltoniana]] $H$ descritta dalla rappresentazione di Schrödinger, essa può essere divisa in due pezzi:
$$H=H_{0}+H_{1}$$
$H_{0}$ e $H_{1}$ possono essere una qualunque suddivisione e la rappresentazione di interazione funzionerà per tutte quante, ma per avere utilità pratica, $H_{0}$ si assume risolvibile facilmente, mentre $H_{1}$ è un'interazione difficile da risolvere. Questa non è altro che la suddivisione usata in [[Meccanica statistica/Teoria delle perturbazioni]], a meno di una costante. In genere, $H_{0}$ dovrebbe essere indipendente dal tempo.

Definiamo $U_{t}=e^{-iHt/\hbar}$, $U_{t,0}=e^{-iH_{0}t/\hbar}$ e $U_{t,1}=e^{-iH_{1}t/\hbar}$ gli evolutori associati alle Hamiltoniane. Preso uno stato $|\psi_{S}(t)\rangle=U_{t}|\psi(0)\rangle$ descritto dalla rappresentazione di Schrödinger, la rappresentazione di interazione è
$$|\psi_{I}(t)\rangle=U_{t,0}^{+}|\psi_{S}(t)\rangle$$
e preso un operatore $\hat{A}_{S}$, esso diventa
$$\hat{A}_{I}(t)=U_{t,0}^{+}\hat{A}_{S}(t)U_{t,0}$$
La matrice densità $\rho_{S}$ in S diventa
$$\rho_{I}(t)=U_{t,0}^{+}\rho_{S}(t)U_{t,0}$$
### Equivalenza
Le tre rappresentazioni spiegano gli stessi fenomeni e sono completamente equivalenti l'una dall'altra. Il [[teorema di Stone]] dà la dimostrazione formale dell'equivalenza tra S e H.