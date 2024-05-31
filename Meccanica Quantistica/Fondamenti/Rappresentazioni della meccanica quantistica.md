---
aliases:
  - rappresentazione di Schrödinger
  - rappresentazione di Heisenberg
  - rappresentazione di interazione
---
La meccanica quantistica possiede un certo "grado di libertà" nella sua rappresentazione. È possibile formulare i risultati della teoria quantistica, in particolare dell'evoluzione temporale, in più modi equivalenti, detti **rappresentazioni** o ***picture***. Esistono tre rappresentazioni: la **rappresentazione di Schrödinger**, quella **di Heisenberg** e quella **di interazione**.
### Rappresentazione di Schrödinger
La rappresentazione di Schrödinger è definita ponendo la dipendenza temporale nello [[stato]] del sistema, lasciando invece gli [[Operatore|operatori]] costanti nel tempo. In simboli, preso uno stato $|\psi\rangle$, esso evolve nel tempo mediante l'applicazione dell'[[evolutore]] $U_{t}$ come
$$|\psi_{t}\rangle=U_{t}|\psi\rangle$$
dove $|\psi_{t}\rangle$ rappresenta lo stato al tempo $t$. La dinamica del sistema è determinata dall'[[equazione di Schrödinger]]:
$$i\hbar \frac{\partial }{\partial t}|\psi_{t}\rangle=\hat{H}|\psi_{t}\rangle$$
Il valor medio di un'[[osservabile]] $Q$ al tempo $t$ è quindi definito semplicemente come
$$\left\langle Q \right\rangle_{t}=\langle \psi_{t}|\hat{Q}|\psi_{t}\rangle$$
### Rappresentazione di Heisenberg
La rappresentazione di Heisenberg è definita ponendo la dipendenza temporale negli operatori associati alle [[Osservabile|osservabili]], lasciando invece lo stato costante nel tempo. Preso un'operatore $\hat{A}$, esso evolve nel tempo come
$$\hat{A}(t)=U_{t}^{+}\hat{A}U_{t}$$
e la dinamica è determinata dall'[[equazione di Heisenberg]]:
$$\frac{d}{dt}\hat{A}(t)=\frac{i}{\hbar}[H,A(t)]+ \frac{\partial A(t)}{\partial t}$$
Il valor medio di un'osservabile $Q$ al tempo $t$ è allora
$$\left\langle Q \right\rangle_{t}=\langle \psi|\hat{Q}(t)|\psi\rangle$$
### Equivalenza
Le due rappresentazioni spiegano gli stessi fenomeni e sono completamente equivalenti l'una dall'altra.