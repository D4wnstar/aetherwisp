Si chiama **proiettore** $\hat{P}_{\psi}$ l'[[operatore lineare]] che, applicato ad un elemento di uno [[spazio vettoriale]], risulta nella componente di quell'elemento che giace su $\psi$. Usando la [[notazione braket]], si scrive
$$\hat{P}_\psi=|\psi\rangle\langle\psi|$$
e applicato ad un vettore $|\phi\rangle$ si scrive
$$\hat{P}_{\psi}|\phi\rangle=\langle\psi|\phi\rangle|\psi\rangle$$
Il numero risultante (se si proietta su uno spazio 1D) appartiene al sottospazio unidimensionale generato da $|\psi\rangle$.
### Proiettore su base ortonormale
Presa una [[base]] [[Ortonormalità|ortonormale]] discreta $|\psi\rangle$ costituita da $\{|\psi_{i}\rangle\}^{n}_{i=1}$, si può definire l'operatore
$$\hat{P}_{i}=|i\rangle\langle i|$$
che proietta l'argomento sull'$i$-esimo vettore della base ortonormale. Se applicato ad un vettore, ci dà i componenti dell'espansione in [[Serie di Fourier]] nella base:
$$\hat{P}_{i}|\phi\rangle=|i\rangle\langle i|\phi\rangle=|\phi_{i}\rangle$$
dato che $\langle i|\phi\rangle$ le componenti $\phi_{i}$. Per questo operatore vale la **relazione di completezza**
$$\sum\limits_{i=1}^{n}\hat{P}_{\psi_{i}}=\hat{\mathbb{1}}$$
Questo risultato si estende immediatamente anche al caso a dimensione infinita discreta, prendendo un [[Sistema ortonormale completo]]. Nel caso di un sistema a dimensione infinita continua, c'è bisogno che sia [[Ortonormalità|Dirac-ortonormale]], in qual caso la relazione di completezza diventa
$$\int_{-\infty}^{+\infty}|e_{z}\rangle\langle e_{z}|dz=\hat{\mathbb{1}}$$
### Proprietà
Il proiettore è un operatore [[idempotenza|idempotente]]
$$\hat{P}_{\psi}^{2}=\hat{P}_{\psi}\hat{P}_{\psi}=(|\psi\rangle\langle \psi|)(|\psi\rangle\langle \psi|)=\langle \psi|\psi\rangle|\psi\rangle\langle \psi|=\hat{P}_{\psi}$$
e vale $\hat{P}_{\psi}^{0}=0$.

Il proiettore è [[Operatore autoaggiunto|autoaggiunto]], infatti
$$\langle \phi|\hat{P}_{x}\psi\rangle=\langle \hat{P}_{x}\phi+\phi-\tilde{\phi}|\hat{P}_{x}\psi\rangle=\langle \hat{P}_{x}\phi|\hat{P}_{x}\psi\rangle=\langle \hat{P}_{x}\phi|\hat{P}_{x}\psi+\psi-\tilde{\psi}\rangle=\langle \hat{P}_{x}\phi|\psi\rangle$$

Per dimostrare che un operatore è un proiettore bisogna dimostrare
- l'autoaggiuntezza
- l'idempotenza
### Risultati utili
La somma di tutte le proiezioni su una base ortonormale è il vettore stesso, grazie alla completezza:
$$|\psi\rangle=\sum\limits_{i=1}^{n}\langle i|\psi\rangle|i\rangle=\sum\limits_{i=1}^{n}|i\rangle\langle i|\psi\rangle=\left(\sum\limits_{i=1}^{n}\hat{P}_{i}\right)|\psi\rangle$$
che è una serie di Fourier.

Un vettore proiettato su sé stesso dà sé stesso:
$$\hat{P}_{\psi}|\psi\rangle=\langle \psi|\psi\rangle|\psi\rangle=|\psi\rangle$$

Un vettore proiettato su un altro vettore ortogonale ad esso dà sempre 0:
$$\hat{P}_{\psi}|\phi\rangle=\langle \psi|\phi\rangle|\psi\rangle=0\quad\text{con}\quad|\phi\rangle\in\{|\psi\rangle\}^{\perp} \Rightarrow\langle \phi|\psi\rangle=0$$

Considero l'esponenziale
$$e^{\hat{P}_{\psi}}=\sum\limits_{n=0}^{\infty} \frac{1}{n!}(\hat{P}_{\psi})^{n}=\hat{\mathbb{1}}+\left(\sum\limits_{n=1}^{\infty} \frac{1}{n!}\right)\hat{P}_{\psi}=\hat{\mathbb{1}}+(e-1)\hat{P}_{\psi}$$
ricordando l'idempotenza.