L'**operatore di parità** è l'[[operatore]] $\hat{\pi}:L^{2}([-a,a],dx)\to L^{2}([-a,a],dx)$ che inverte il segno dell'argomento di una funzione:
$$(\hat{\pi}\psi)(x)=\psi(-x)$$
### Proprietà
- $\hat{\pi}$ è [[Operatore autoaggiunto|autoaggiunto]], infatti prese due funzioni generiche $\psi$ e $\phi$ su $L^{2}([-a,a])$ si ha $$\braket{ \psi | \hat{\pi}\phi } =\int_{-a}^{a}\overline{\psi(x)}(\hat{\pi}\phi)(x)\ dx=\int_{-a}^{a}\overline{\psi(x)}\phi(\underbrace{ -x }_{ -y })\ dx=\int_{-a}^{a}\overline{\psi(-y)}\phi(y)\ dy=\braket{ \hat{\pi}\psi | \phi } $$e anche $\hat{\pi}=\hat{\pi}^{+}$.
- È anche [[Operatore unitario|unitario]]: $\hat{\pi}^{+}\hat{\pi}=\hat{\pi}^{2}=\hat{\mathbf{1}}$.
### Oscillatore armonico quantistico
L'[[Hamiltoniana]] dell'[[oscillatore armonico quantistico]] (in particolare il [[Potential]]) è invariante rispetto a trasformazioni di parità. Questo perché il potenziale dipende dal quadrato della posizione, quindi il segno svanisce. Infatti
$$\hat{H}=\frac{\hat{p}^{2}}{2m}+ \frac{m\omega ^{2}}{2}\hat{q}^{2}\quad\to \quad \hat{\pi}^{+}\hat{H}\hat{\pi}=\hat{H}_{\pi}$$
Usando l'unitarietà e l'autoaggiuntezza
$$\hat{\pi}\left( \frac{\hat{p}^{2}}{2m}+ \frac{m\omega ^{2}}{2}\hat{q}^{2} \right)\hat{\pi}=\frac{(\hat{\pi}\hat{p}\hat{\pi})^{2}}{2m}+ \frac{m\omega ^{2}}{2}(\hat{\pi}\hat{q}\hat{\pi})^{2}$$
Calcolando gli operatori separatamente in [[Rappresentazioni dello stato|rappresentazione della posizione]]
$$(\hat{\pi}\hat{q}\hat{\pi}\psi)(x)=(\hat{q}\hat{\pi}\psi)(-x)=-x(\hat{\pi}\psi)(-x)=-x\psi(x)\quad \forall \psi \in L^{2}(\mathbb{R})$$ossia
$$\hat{\pi}\hat{q}\hat{\pi}=-\hat{q}$$
e sfruttando l'[[Oscillatore armonico quantistico#Evoluzione temporale|evoluzione temporale]] degli operatori $\hat{q}$ e $\hat{p}$ nell'oscillatore abbiamo immediatamente
$$\hat{\pi}\hat{p}\hat{\pi}=-\hat{p}$$
Sostituendo nell'equazione di prima
$$\frac{(\hat{\pi}\hat{p}\hat{\pi})^{2}}{2m}+ \frac{m\omega ^{2}}{2}(\hat{\pi}\hat{q}\hat{\pi})^{2}=\frac{\hat{p}^{2}}{2m}+ \frac{m\omega ^{2}}{2}\hat{q}^{2}=\hat{H}$$
La conseguenza è che gli [[Equazione agli autovalori|autostati]] di $\hat{H}$ sono invariati per parità. Partendo da $\hat{H}\ket{\psi_{E}}=E\ket{\psi_{E}}$ abbiamo, usando l'unitarietà
$$\hat{H}\hat{\pi}\ket{\psi_{E}}=\hat{\pi}(\hat{\pi}\hat{H}\hat{\pi})\ket{\psi_{E}} =\hat{\pi}\hat{H}\ket{\psi} =E \hat{\pi}\ket{\psi_{E}}  $$
quindi vediamo che anche $\hat{\pi}\ket{\psi_{E}}$ è autovettore di $\hat{H}$ con autovalore $E$. A prima vista sembra che questo causi [[degenerazione]], ma in una dimensione non è possibile avere degenerazione, quindi deve essere che $\hat{\pi}\ket{\psi_{E}}$ deve essere proporzionale a $\ket{\psi_{E}}$.

Dato che le soluzione inverse per parità sono anche soluzioni dell'oscillatore armonico, questo implica che le soluzioni abbiano una parità intrinseca, nel senso che le autofunzioni che risolvono l'oscillatore sono o pari, o dispari. Questo si trova anche risolvendo l'oscillatore senza usare gli [[operatori di creazione e distruzione]].

Sebbene $\hat{\pi}$ sia una simmetria di $\hat{H}$, il [[teorema di Noether]] qui non si applica, perché $\hat{\pi}$ non è derivabile (in senso classico) e quindi non è un generatore di trasformazioni (nel senso che non ha la forma $\hat{\pi}=e^{a \hat{G}}$). Questo deriva dal fatto che la trasformazione di $\hat{\pi}$ non è continua, ma discreta.