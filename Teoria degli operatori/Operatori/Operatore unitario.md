---
wiki-publish: true
aliases:
  - unitario
---
Si dice **operatore unitario** $U:H \rightarrow H$ un [[Operatore]] con la caratteristica di conservare il [[Scalar product]], ovvero
$$(Ux,Uy)=(x,y)$$
o equivalentemente (grazie alla linearità)
$$||Ux||=||x||$$
Valgono anche
$$U^{+}U=I\quad;\quad||U||=1$$
con $I$ l'operatore identico. In dimensione finita, l'unitarietà è sufficiente a garantire l'invertibilità dell'operatore, ma in dimensione infinita garantisce solo l'iniettività, dato che
$$Ux=Uy \quad \Rightarrow \quad 0=||U(x-y)||=||x-y|| \quad \Rightarrow \quad x=y$$
Per ottenere la suriettività anche in dimensione infinita, bisogna porre la condizione
$$\text{Imm}U=H$$
cioè che l'immagine sia uguale al dominio. In tal caso (sempre vero per operatori finiti), si ha
$$U^{-1}=U^{+}$$
### Cambi di sistema
Una proprietà importante degli operatori unitari è trasformare [[Sistema ortonormale completo|sistemi ortonormali completi]] in altri sistemi ortonormali completi. Con un tale cambio di sistema, gli operatori cambiano rappresentazione con legge
$$T'=UTU^{+}$$
Valgono in tal caso
1. chiamato $A$ è l'aggiunto di $T$, $A'=UAU^{+}$ è l'aggiunto di $T'$
2. se $T$ è [[Operatore autoaggiunto|simmetrico]] in dominio $D_{0}$, allora $T'$ è simmetrico nel dominio $UD_{0}$ dei vettori trasformati $Ux\;\forall x\in D_{0}$
3. se $T$ è un [[proiettore]] che proietta su un sottospazio $H_{1}$, anche $T'$ è un proiettore e proietta sul sottospazio $UH_{1}$ dei vettori trasformati $Ux\;\forall x\in H_{1}$
4. se $S$ è un operatore invertibile, si può considerare la trasformazione $T \rightarrow T''=STS^{-1}$. Se $T$ ammette un autovettore $x$ con autovalore $\lambda$, allora $T''$ ammette l'autovettore $Sx$ con autovalore $\lambda$. Se $T$ soddisfa un'equazione algebrica $a_{n}T^{n}+\ldots+a_{0}I=0$, anche $T''$ la soddisfa. Va notato che questa trasformazione non conserva l'ortonormalità dei sistemi né le proprietà di autoaggiuntezza degli operatori.
### Parentesi di commutazione
Gli operatori unitari non cambiano il [[commutatore]]. Infatti, presi due operatori $X$ e $Y$ e un operatore unitario $U$ che applichiamo ad essi, vale
$$\begin{align}
[X_{U},Y_{U}]&=[U^{+}XU,U^{+}YU] \\
&=U^{+}XUU^{+}YU-U^{+}YUU^{+}XU \\
&=U^{+}XYU-U^{+}YXU \\
&=U^{+}[X,Y]U
\end{align}$$
Questo genere di trasformazioni $X_{U}=U^{+}XU$, dette unitarie, sono l'equivalente quantistico delle [[canonical transformation|trasformazioni canoniche]] che preservano l'[[Hamiltoniana]] in meccanica classica. Per esse vale dunque il [[teorema di Noether]].

Più in generale, questo fatto è importante perché la traslazione per operatori unitari non varia gli [[Equazione agli autovalori|autovalori]]. Infatti, consideriamo un'equazione agli autovalori
$$H\ket{\psi_{a}} =E_{a}\ket{\psi_{a}} $$
Ora trasliamo $\ket{\psi_{a}}$ come $\ket{\psi^{U}_{a}}=U\ket{\psi_{a}}$. Ora abbiamo
$$H^{U}\ket{\psi_{a}^{U}} =E_{a}^{U}\ket{\psi_{a}^{U}} $$
Ma vale
$$U^{+}H \underbrace{ UU^{+} }_{ \hat{\mathbf{1}} }\ket{\psi_{a}} =E_{a}U^{+}\ket{\psi_{a}} $$
Quindi gli autovalori rimangono gli stessi sotto trasformazione unitaria (???).

> [!example] Oscillatore armonico quantistico
> L'Hamiltoniana dell'[[oscillatore armonico quantistico]] traslata per $q$ è
> $$\hat{H}_{q}=\frac{\hat{p}^{2}}{2m}+ \frac{m\omega ^{2}}{2}(\hat{q}-q)^{2}=e^{-iq\hat{p}/\hbar}\hat{H}e^{-iq\hat{p}/\hbar}$$
> dove $e^{-iq \hat{p}/\hbar}$ è l'[[Operatori di traslazione e boost|operatore di traslazione]]. L'energia invece è
> $$E_{n}^{q}=\hbar \omega\left( n+ \frac{1}{2} \right)=E_{n}$$
> L'evoluzione dell $n$-esimo autostato è $\ket{\psi_{n}^{q}}=e^{-iq\hat{p}/\hbar}\ket{\psi_{n}}$. Vogliamo trovarne l'autofunzione associata. In [[Rappresentazioni dello stato|rappresentazione del momento]] l'operatore $\hat{p}$ diventa semplicemente $p$ e abbiamo
> $$\braket{ p | \psi_{n}^{q} } =e^{-iqp/\hbar}\braket{ p | \psi_{n} } $$
> ma a noi interessa la [[Rappresentazioni dello stato|rappresentazione della posizione]] e per convertire dovremmo fare l'[[Trasformata di Fourier|antitrasformata di Fourier]] dell'autostato (e quindi dei [[polinomi di Hermite]], buona fortuna). Partiamo dunque direttamente dalla posizione
> $$\braket{ x | \psi_{n}^{q} } =\braket{ x | e^{-iq\hat{p}/\hbar}\psi_{n}^{q} } $$
> Risolviamo prima
> $$\hat{q}e^{iq\hat{p}/\hbar}\ket{x} =e^{iq\hat{p}/\hbar}\underbrace{ e^{-iq\hat{p}/\hbar}\hat{q}e^{iq\hat{p}/\hbar} }_{ \hat{q}-q }\ket{x} =\ldots$$
> dove abbiamo fatto comparire l'evoluzione in $q$ per unitarietà. Allora continuando
> $$\ldots=e^{iq\hat{p}/\hbar}(\hat{q}-q)\ket{x} =e^{iq\hat{p}/\hbar}(x-q)\ket{x} =(x-q)e^{iq\hat{p}/\hbar}\ket{x} $$
> $e^{iq\hat{p}/\hbar}\ket{x}$ deve essere proporzionale a $\ket{x-q}$:
> $$e^{iq\hat{p}/\hbar}\ket{x}=c\ket{x-q} $$
> Possiamo sfruttare l'[[Orthonormality|ortonormalità di Dirac]] degli autostati
> $$\delta(y-x)=\braket{ e^{iq\hat{p}/\hbar}y |e^{iq\hat{p}/\hbar}x  }=\braket{ c(y-q) | c(x-q) } =\lvert c \rvert ^{2}\braket{ y-q | x-q } =\lvert c \rvert ^{2}\delta (y-x) $$
> e quindi $\lvert c \rvert^{2}=1$, da cui $c=1$. Allora vale $e^{iq\hat{p}/\hbar}\ket{x}=\ket{x-q}$. Tornando quindi indietro si ha
> $$\braket{ x | \psi_{n}^{q} }=\braket{ x | e^{-iq\hat{p}/\hbar}\psi_{n} }  =\braket{ e^{iq\hat{p}/\hbar}x | \psi_{n} } =\braket{ x-q | \psi_{n} } $$
> Le autofunzioni in posizione sono quindi uguali in tutto tranne che sono traslate di $-q$:
> $$\psi_{0}^{q}(x)=\psi_{0}(x-q)=\sqrt[4]{ \frac{m\omega}{\hbar \pi} }e^{-(m\omega/2\hbar)(x-q)^{2}}$$
