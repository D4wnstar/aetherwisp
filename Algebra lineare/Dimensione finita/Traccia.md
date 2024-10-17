La **traccia** è un numero e operazione definita su una matrice o un [[operatore]].
- Nel caso di una matrice $A$, la traccia è la somma dei valori sulla sua diagonale. Vale $\mbox{Tr}(A)=\sum\limits_{i=1}^{n}a_{ii}$.
- Nel caso di un operatore $\hat{A}$, la traccia è vale $\mbox{Tr}(\hat{A})=\sum\limits_{i=1}^{n}\langle \phi_{i}|\hat{A}\phi_{i}\rangle$ dove $\phi_{i}$ sono i vettori di un [[sistema ortonormale completo]] $\{ \phi_{i} \}_{i=1}^{n}$ dello [[spazio di Hilbert]] $\mathcal{H}$ in cui risiede $\hat{A}$. (In realtà questa formula vale anche per le matrici sulla loro [[base]], ma è più facile sommare la diagonale.)
### Proprietà
Ha le seguenti proprietà:
1. La traccia è indipendente dalla rappresentazione. Ciò significa che il valore della traccia è uguale in qualunque base la matrice o operatore sia espresso.
2. È lineare: $\lambda\text{Tr}(\hat{A})=\text{Tr}(\lambda \hat{A})$.
3. È ciclica: $\mbox{Tr}(\hat{A}\hat{B})=\mbox{Tr}(\hat{B}\hat{A})$.