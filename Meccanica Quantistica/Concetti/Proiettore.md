Si chiama **proiettore**
$$\hat{P}_\psi=|\psi\rangle\langle\psi|$$
e vale che
$$\hat{P}_{\psi}|\phi\rangle=\langle\psi|\phi\rangle|\psi\rangle$$
Un importante proiettore è, presa una base ortonormale $|\psi\rangle\in\mathbb{C}^{N}$ con $\{|\psi_{i}\rangle\}^{n}_{i=1}$,
$$\hat{P}_{i}=|i\rangle\langle i|$$
che proietta sull'$i$-esimo vettore della base ortonormale.
Vale la **relazione di completezza**
$$\sum\limits_{i=1}^{n}\hat{P}_{\psi_{i}}=\hat{\mathbb{1}}$$
che si può estendere anche al caso $n \rightarrow\infty$. Valgono anche
$$\langle j|\psi\rangle=\sum\limits_{i=1}^{n}\psi_{i}\underbrace{\langle j|i\rangle}\limits_{\delta_{ij}}=\psi_{j}$$
$$|\psi\rangle=\sum\limits_{i=1}^{n}\langle i|\psi\rangle|i\rangle=\sum\limits_{i=1}^{n}|i\rangle\langle i|\psi\rangle=\left(\sum\limits_{i=1}^{n}\hat{P}_{i}\right)|\psi\rangle$$
$$\hat{P}_{i}|\psi\rangle=\langle \psi|\psi\rangle|\psi\rangle=|\psi\rangle$$ $$\hat{P}_{\psi}|\phi\rangle=\langle \psi|\phi\rangle|\psi\rangle=0\quad|\phi\rangle\in\{|\psi\rangle\}^{\perp} \Rightarrow\langle \phi|\psi\rangle=0$$
Possiamo prendere il quadrato di un proiettore
$$\hat{P}_{\psi}^{2}=\hat{P}_{\psi}\hat{P}_{\psi}=(|\psi\rangle\langle \psi|)(|\psi\rangle\langle \psi|)=\langle \psi|\psi\rangle|\psi\rangle\langle \psi|=\hat{P}_{\psi}$$
quindi la potenza di un proiettore è il proiettore stesso, ossia è **idempotente**.
Considero l'esponenziale
$$e^{\hat{P}_{\psi}}=\sum\limits_{n=0}^{\infty} \frac{1}{n!}(\hat{P}_{\psi})^{n}=\hat{\mathbb{1}}+\left(\sum\limits_{n=1}^{\infty} \frac{1}{n!}\right)\hat{P}_{\psi}=\hat{\mathbb{1}}+(e-1)\hat{P}_{\psi}$$
ricordando che $\hat{P}_{\psi}^{0}=0$.