L'**operatore di parità** è l'[[operatore]] $\hat{\pi}:L^{2}([-a,a],dx)\to L^{2}([-a,a],dx)$ che inverte il segno dell'argomento di una funzione:
$$(\hat{\pi}\psi)(x)=\psi(-x)$$
$\hat{\pi}$ è [[Operatore autoaggiunto|autoaggiunto]], infatti prese due funzioni generiche $\psi$ e $\phi$ su $L^{2}([-a,a])$ si ha
$$\braket{ \psi | \hat{\pi}\phi } =\int_{-a}^{a}\overline{\psi(x)}(\hat{\pi}\phi)(x)\ dx=\int_{-a}^{a}\overline{\psi(x)}\phi(\underbrace{ -x }_{ -y })\ dx=\int_{-a}^{a}\overline{\psi(-y)}\phi(y)\ dy=\braket{ \hat{\pi}\psi | \phi } $$
