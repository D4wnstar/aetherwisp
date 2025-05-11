---
wiki-publish: true
---
La **traccia** è un numero e operazione definita su una matrice o un [[operatore]].
- Nel caso di una matrice $A$, la traccia è la somma dei valori sulla sua diagonale. Vale $\mbox{Tr}(A)=\sum\limits_{i=1}^{n}a_{ii}$.
- Nel caso di un operatore $\hat{A}$, la traccia è vale $\mbox{Tr}(\hat{A})=\sum\limits_{i=1}^{n}\langle \phi_{i}|\hat{A}\phi_{i}\rangle$ dove $\phi_{i}$ sono i vettori di un [[sistema ortonormale completo]] $\{ \phi_{i} \}_{i=1}^{n}$ dello [[spazio di Hilbert]] $\mathcal{H}$ in cui risiede $\hat{A}$. (In realtà questa formula vale anche per le matrici sulla loro [[base]], ma è più facile sommare la diagonale.)
### Proprietà
Ha le seguenti proprietà:
1. È ciclica: $\mbox{Tr}(\hat{A}\hat{B})=\mbox{Tr}(\hat{B}\hat{A})$.
2. È lineare: $\lambda\text{Tr}(\hat{A})=\text{Tr}(\lambda \hat{A})$.
3. La traccia è indipendente dalla rappresentazione. Ciò significa che il valore della traccia è uguale in qualunque base la matrice o operatore sia espresso.
#### Dimostrazione indipendenza dalla base
Consideriamo una base $\{ \psi_{i} \}_{i}^{d}$ e un operatore $\hat{A}: \mathbb{C}^{d}\to \mathbb{C}^{d}$. Assumiamo per assurdo che la traccia dipenda dalla base. Allora troviamo la traccia in $\{ \psi_{i} \}_{i}^{d}$:
$$\mathrm{Tr}_{\{ \psi_{i} \}}\hat{A}=\sum_{i=1}^{d} \braket{ \psi_{i} | \hat{A}\psi_{i}  } $$
e anche in un'altra base $\{ \phi_{j} \}_{j}^{d}$:
$$\text{Tr}_{\{ \phi_{j} \}}\hat{A}=\sum_{j=1}^{d} \braket{ \phi_{j} | \hat{A}\phi_{j} } $$
Sfruttiamo la relazione di completezza dei [[Proiettore|proiettori]] su una base:
$$\mathrm{Tr}_{\{ \psi_{i} \}}\hat{A}=\sum_{i=1}^{d} \braket{ \psi_{i} | \left( \sum_{j=1}^{d} \hat{P}_{\phi_{j}} \right)\hat{A}\left( \sum_{k=1}^{d} \hat{P}_{\phi_{k}} \right)\psi_{i} } =\ldots$$
Le somme possono essere tirate fuori dal prodotto scalare per linearità:
$$\ldots=\sum_{i=1}^{d} \sum_{j=1}^{d} \sum_{k=1}^{d} \braket{ \psi_{i} |\hat{P}_{\phi_{j}}\hat{A}\hat{P}_{\phi_{k}}\psi_{i}  }=\sum_{i=1}^{d} \sum_{j=1}^{d} \sum_{k=1}^{d} \braket{ \psi_{i} |\phi_{j}  }\braket{ \phi_{j} | \hat{A}\phi_{k} } \braket{ \phi_{k} | \psi_{i} } =\ldots$$
Posso riordinare i termini per costruire il proiettore su $\psi_{i}$:
$$\ldots=\sum_{i=1}^{d} \sum_{j=1}^{d} \sum_{k=1}^{d} \braket{ \phi_{j} | \hat{A}\phi_{k} } \braket{ \phi _{k}|\psi_{i} } \braket{ \psi_{i} | \phi_{j} } =\sum_{j=1}^{d} \sum_{k=1}^{d} \braket{ \phi_{j} | \hat{A}\phi_{k} }\sum_{i=1}^{d} \bra{\phi_{k}}\hat{P}_{\psi_{i}}\ket{\phi_{j}}=\ldots $$
Possiamo portare la somma in $i$ dentro il prodotto scalere e con la relazione di completezza vale $\sum_{i=1}^{d}\hat{P}_{\psi_{i}}=\hat{\mathbf{1}}$ troviamo $\braket{ \phi_{k} | \phi_{j} }$, ma questi sono [[Orthonormality|ortonormali]] l'un l'altro, quindi diventano la [[Kronecker delta]] $\delta_{kj}$. Ma questa delta "assorbe" una delle somme (o in $j$ o in $k$) e quindi ci rimane
$$\ldots=\sum_{j=1}^{d} \braket{ \phi_{j} | \hat{A}\phi_{j} } =\text{Tr}_{\{ \phi_{j} \}}\hat{A}$$
quindi la traccia è indipendente dalla base.

Può anche essere derivata in una linea sfruttando la ciclicità. Preso un operatore $\hat{A}$ e una sua rappresentazione in un'altra base $\hat{B}=\hat{S}\hat{A}\hat{S}^{-1}$, allora vale
$$\text{Tr}(\hat{B})=\text{Tr}(\hat{S}\hat{A}\hat{S}^{-1})=\text{Tr}(\hat{S}\hat{S}^{-1}\hat{A})=\text{Tr}(\hat{A})$$
