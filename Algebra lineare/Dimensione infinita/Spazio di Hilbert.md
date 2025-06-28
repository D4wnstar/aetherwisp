---
wiki-publish: true
---
Uno **spazio di Hilbert**, in genere denotato $\mathrm{H}$ o $\mathcal{H}$, è uno [[Vector space]] [[Spazio metrico completo|completo]] rispetto alla [[Norma]] indotta da un [[Scalar product]] definito su di esso. Se sullo spazio è inoltre presente un [[Sistema completo]] (non necessariamente ortonormale), si dice che lo spazio è **separabile**.

Un esempio di spazio di Hilbert è lo [[Spazi di successioni lp#Spazio $L {2}$|spazio L^2]], ma lo so anche tutti gli spazi $\mathbb{R}^{N}$ e $\mathbb{C}^{N}$, sebbene di norma si usi parlare di spazi di Hilbert solo in dimensione infinita.

Sia $H$ un generico spazio di Hilbert che assumiamo di dimensione infinita. Allora è possibile trovare un insieme infinito di vettori $v_{1},v_{2},\ldots,v_{n}$ [[lineare indipendenza|linearmente indipendenti]], ossia un insieme infinito numerabile tale per cui, preso un qualunque $n$ naturale, i primi $x_{1},\ldots,x_{n}$ vettori sono linearmente indipendenti fra loro. Se si riesce a trovare un tale insieme, è sempre possibile trovare un altro insieme di vettori ortonormali fra loro tramite l'[[Ortonormalizzazione di Gram-Schmidt]].
### Relazione con le probabilità
Gli spazi di Hilbert sono particolarmente utili per lavorare con le probabilità. Fondamentalmente, ogni numero reale compreso fra zero e uno può essere interpretato come probabilità (di *cosa* sia probabilità è un altro discorso). Consideriamo a titolo di esempio $\mathbb{C}^{2}$, uno spazio di Hilbert molto semplice. Consideriamo due vettori $\ket{\psi}$ e $\ket{ \phi}$ su questo spazio (usando la [[notazione braket]]). Questi sono
$$\ket{\psi} =\begin{pmatrix}
\alpha \\
\beta
\end{pmatrix},\quad
\ket{\phi} =\begin{pmatrix}
\gamma \\
\delta
\end{pmatrix} $$
allora il loro [[Scalar product]] è
$$\braket{ \psi | \phi } =\alpha^{*}\gamma+\beta^{*}\delta$$
Se cerchiamo invece la [[Norma]] di $\ket{\psi}$ si ha
$$\braket{ \psi | \psi } =\lvert \psi \rvert^{2}= \lvert \alpha \rvert^{2}+\lvert \beta \rvert ^{2} $$
Se $\ket{\psi}$ è normalizzato, deve valere
$$\lvert \psi \rvert ^{2}=\lvert \alpha \rvert ^{2}+\lvert \beta \rvert ^{2}=1$$
e quindi $\lvert  \alpha \rvert^{2}$ e $\lvert  \beta \rvert^{2}$ devono essere compresi fra 0 e 1, ossia possono essere interpretati come probabilità.

> [!success] Probabilità e spazi di Hilbert
> Le norme quadre dei componenti di un vettore normalizzato su un spazio di Hilbert possono essere interpretate come probabilità.
