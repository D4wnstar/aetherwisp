In meccanica quantistica, uno [[Stato]] si dice **determinato** se misure compiute su sistemi identicamente preparati conduce sempre allo stesso risultato. Un esempio sono gli stati stazionari di un'[[Hamiltoniana]], che danno sempre l'esatto valore di energia $E_{n}$ di quello stato.

Chiamiamo $q$ il risultato della misura di un'[[Osservabile]] $Q$. Uno stato indeterminato si costruisce cercando uno stato in cui la varianza è nulla. Ciò significa
$$\sigma^{2}_{Q}=\langle (\hat{Q}- \hat{q})^{2} \rangle=\langle \Psi| (\hat{Q}-\hat{q})^{2}|\Psi\rangle=\langle (\hat{Q}-\hat{q})\Psi \;|\;(\hat{Q}-\hat{q})\Psi\rangle=0$$
dove l'ultimo passaggio proviene dal fatto che $\hat{Q}$ è [[Operatore autoaggiunto|hermitiano]]. Dato che l'unico valore misurato e $q$, la media di $Q$ deve essere appunto $q$
$$\left\langle Q \right\rangle=q$$
L'unica funzione il cui [[prodotto scalare]] con sé stessa è nullo è 0, dunque vale
$$\hat{Q}\Psi=q\Psi$$
che è un'[[equazione agli autovalori]] per l'[[operatore]] $\hat{Q}$ di autovalore $q$ e autofunzione $\Psi$.

Allora, **gli stati determinati di un'osservabile sono autofunzioni dell'operatore associato a quell'osservabile**. Inoltre, se lo [[spettro]] di $\hat{Q}$ è discreto, le autofunzioni esistono in [[Spazi Lp#Spazio $L {2}$|L^2]] e corrispondono a stati fisicamente realizzabili. Se lo spettro è continuo, le autofunzioni non sono normalizzabili e non rappresentano alcuna [[Funzione d'onda]], anche se una loro combinazione lineare forse sì.