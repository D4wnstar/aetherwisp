---
aliases:
  - operatori scaletta
  - operatore di creazione
  - operatore di distruzione
  - operatore numero
---
Gli **operatori di creazione e distruzione** $\hat{a}^{+}$ e $\hat{a}$ sono una coppia di [[operatore|operatori]] utilizzati in meccanica quantistica che modificano lo [[stato]] di un sistema aumentando o diminuendo un [[numero quantico]] (in meccanica quantistica) o creando o distruggendo una [[particella]] (in QFT). Sono particolarmente importanti nello studio dell'[[oscillatore armonico quantistico]], dove sono anche chiamati **operatori scaletta** e l'operatore $\hat{a}^{+}\hat{a}$ è detto **operatore numero**.
### Proprietà
- Sono uno l'[[Operatore aggiunto|aggiunto]] dell'altro.
- Non sono [[Operatore autoaggiunto|autoaggiunti]].
- Non [[commutatore|commutano]]: $[\hat{a},\hat{a}^{+}]=1$. Si può usare la [[Commutatore|formula di Baker-Campbell-Hausdorff]]: $e^{\alpha \hat{a}^{+}-\alpha^{*}\hat{a}}=e^{-\lvert \alpha \rvert^{2}/2}e^{\alpha \hat{a}^{+}}e^{-\alpha^{+}\hat{a}}$.
### Evoluzione temporale
Possiamo cercare l'evoluzione temporale nella [[Rappresentazioni della meccanica quantistica|rappresentazione di Heisenberg]] $\hat{a}\to \hat{U}_{t}^{+}\hat{a}\hat{U}_{t}$. Per risolvere questa equazione, possiamo notare che è la soluzione dell'[[equazione di Heisenberg]]. Infatti, presa l'[[Hamiltoniana]] dell'oscillatore armonico quantistico $\hat{H}=\hbar \omega\left( \hat{a}^{+}\hat{a}+ \frac{1}{2} \right)$
$$\frac{d}{dt}\hat{a}_{t}=\frac{i}{\hbar}[\hat{H},\hat{a}_{t}]=\frac{i}{\hbar}\left[ \hbar \omega\left( \hat{a}^{+}\hat{a}+ \frac{1}{2} \right), \hat{a}_{t} \right]=i\omega[\hat{a}^{+}\hat{a},\hat{a}_{t}]=\ldots$$
Naturalmente noi non sappiamo cos'è $\hat{a}_{t}$, quindi sembra che questo risultato sia inutile. Tuttavia, sappiamo cos'è $\hat{U}_{t}$ dato che conosciamo $\hat{H}$:
$$\hat{U}_{t}=e^{-i\omega t(\hat{a}^{+}\hat{a}+1/2)}$$
Allora possiamo esprimere $\hat{a}_{t}$ come
$$\begin{align}
[\hat{a}^{+}\hat{a},\hat{a}_{t}]&=[\hat{a}^{+}\hat{a},\hat{U}_{t}^{+}\hat{a}\hat{U}_{t}]=\hat{a}^{+}\hat{a}\hat{U}_{t}^{+}\hat{a}\hat{U}_{t}-\hat{U}_{t}^{+}\hat{a}\hat{U}_{t}\hat{a}^{+}\hat{a}=\hat{U}_{t}^{+}(\hat{a}^{+}\hat{a}\hat{a}-\hat{a}\hat{a}\hat{a}^{+})\hat{U}_{t}= \\
&=\hat{U}_{t}^{+}[\hat{a}^{+}\hat{a},\hat{a}]\hat{U}_{t}
\end{align}$$
allora tornando indietro abbiamo
$$\ldots=i\omega \hat{U}_{t}^{+}\underbrace{ [\hat{a}^{+}\hat{a},\hat{a}] }_{ -\hat{a} }\hat{U}_{t}=-i\omega \hat{a}_{t}$$
Questo ci lascia con un'[[equazione differenziale ordinaria]]:
$$\frac{d}{dt}\hat{a}_{t}=-i\omega \hat{a}_{t}$$
con condizione al contorno $\hat{a}_{t=0}=\hat{a}$. Questa è immediatamente risolvibile come
$$\boxed{\hat{a}_{t}=e^{-i\omega t}\hat{a}}$$
L'operatore di distruzione si trova in modo analogo e vale
$$\boxed{\hat{a}^{+}_{t}=e^{i\omega t}\hat{a}^{+}}$$
L'operatore numero è invece costante nel tempo
$$\boxed{(\hat{a}^{+}\hat{a})_{t}=\hat{a}^{+}\hat{a}}$$
Infatti, la dimostrazione sopra si può semplificare notando che
$$[\hat{a}^{+}\hat{a},\hat{a}_{t}]=[(\hat{a}^{+}\hat{a})_{t},\hat{a}_{t}]=\hat{U}_{t}^{+}[\hat{a}^{+}\hat{a},\hat{a}]\hat{U}_{t}$$
