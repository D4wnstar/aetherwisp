Si dice **operatore unitario** $U:H \rightarrow H$ un [[operatore]] con la caratteristica di conservare il [[prodotto scalare]], ovvero
$$(Ux,Uy)=(x,y)$$
o equivalentemente (grazie alla linearità)
$$||Ux||=||x||$$
Valgono anche
$$U^{+}U=I\quad;\quad||U||=1$$
con $I$ la matrice identica. In dimensione finita, l'unitarietà è sufficiente a garantire l'invertibilità dell'operatore, ma ciò in dimensione infinita garantisce solo l'iniettività, dato che
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
2. se $T$ è [[operatore autoaggiunto|simmetrico]] in dominio $D_{0}$, allora $T'$ è simmetrico nel dominio $UD_{0}$ dei vettori trasformati $Ux\;\forall x\in D_{0}$
3. se $T$ è un [[proiettore]] che proietta su un sottospazio $H_{1}$, anche $T'$ è un proiettore e proietta sul sottospazio $UH_{1}$ dei vettori trasformati $Ux\;\forall x\in H_{1}$
4. se $S$ è un operatore invertibile, si può considerare la trasformazione $T \rightarrow T''=STS^{-1}$. Se $T$ ammette un autovettore $x$ con autovalore $\lambda$, allora $T''$ ammette l'autovettore $Sx$ con autovalore $\lambda$. Se $T$ soddisfa un'equazione algebrica $a_{n}T^{n}+\ldots+a_{0}I=0$, anche $T''$ la soddisfa. Va notato che questa trasformazione non conserva l'ortonormalità dei sistemi né le proprietà di autoaggiunzione degli operatori.