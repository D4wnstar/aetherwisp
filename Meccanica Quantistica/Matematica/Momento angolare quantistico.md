Classicamente, il momento angolare è dato dalla formula vettoriale
$$\vec{L}=\vec{r}\times\vec{p}$$
che suddiviso nelle sue componenti dà
$$L_{x}=yp_{z}-zp_{y}, \quad L_{y}=zp_{x}-xp_{z}, \quad L_{z}=xp_{y}-yp_{x}$$
Quantizzando queste quantità con l'[[operatore]] quantità di moto si trova
$$\hat{L}_{x}=\frac{\hbar y}{i}\frac{\partial }{\partial z}- \frac{\hbar z}{i}\frac{\partial }{\partial y}, \quad \hat{L}_{y}=\frac{\hbar z}{i}\frac{\partial }{\partial x}- \frac{\hbar x}{i}\frac{\partial }{\partial z}, \quad \hat{L}_{z}=\frac{\hbar x}{i}\frac{\partial }{\partial y}- \frac{\hbar y}{i}\frac{\partial }{\partial x}$$
### Commutatività
Per trovare gli [[Equazione agli autovalori|autovalori]] di questi operatori, anzitutto calcoliamo il loro [[commutatore]]:
$$[L_{x},L_{y}]=[yp_{z}-zp_{y}, zp_{x}-xp_{z}]=[yp_{z},zp_{x}]-[yp_{z},xp_{z}]-[zp_{y},zp_{x}]+[zp_{y},xp_{z}]=\ldots$$
Gli unici commutatori che non commutano sono $x$ con $p_{x}$, $y$ con $p_{y}$ e $z$ con $p_{z}$, quindi
$$\ldots=[yp_{z},zp_{x}]-[zp_{y},xp_{z}]=yp_{x}[p_{z},z]+xp_{y}[z,p_{z}]=i\hbar(xp_{yu}-yp_{x})=i\hbar L_{z}$$
Quindi il commutatore di $L_{x}$ e $L_{y}$ dipende da $L_{z}$. Invero, per ottenere tutti i commutatori è sufficiente compiere una permutazione ciclica nell'indice delle variabili:
$$[L_{x},L_{y}]=i\hbar L_{z}, \quad [L_{y},L_{z}]=i\hbar L_{x}, \quad [L_{z},L_{x}]=i\hbar L_{y}$$
Ciò significa le coppie di momenti angolari sono [[Disuguaglianza di Heisenberg|osservabili incompatibili]]. Secondo il principio di indeterminazione generalizzato si ha
$$\sigma_{L_{x}}^{2}\sigma_{L_{y}}^{2}\geq \frac{\hbar^{2}}{4}\left\langle L_{z} \right\rangle^{2} \quad\Rightarrow\quad \sigma_{L_{x}}\sigma_{L_{y}}\geq \frac{\hbar}{2}|\left\langle L_{z} \right\rangle|$$

Se però prendiamo il quadrato del momento angolare *totale*
$$L^{2}\equiv L_{x}^{2}+L_{y}^{2}+L_{z}^{2}$$
si trova che commuta con tutte le componenti
$$\begin{align}
[L^{2},L_{x}]&=[L^{2}_{x},L_{x}]+[L^{2}_{y},L_{x}]+[L^{2}_{z},L_{x}] \\
&=L_{y}[L_{y},L_{x}]+[L_{y},L_{x}]L_{y}+L_{z}[L_{z},L_{x}]+[L_{z},L_{x}]L_{z} \\
&=L_{y}(-i\hbar L_{z}) + (-i\hbar L_{z})L_{y} + (-i\hbar L_{z})L_{y} + (i\hbar L_{y})L_{z} \\
&=0
\end{align}$$
(per le altre componenti basta compiere una permutazione ciclica come sopra). In una forma più compatta, si ha
$$[L^{2},\vec{L}]=0$$
Ciò significa che è possibile trovare [[Stato stazionario|autostati]] simultanei di $L^{2}$ e (per esempio) $L_{z}$.
### Autovalori
Per trovare gli autovalori, usiamo un approccio simile a quello dell'[[oscillatore armonico quantistico]], usando degli [[operatori di creazione e distruzione]]. Definiamo
$$L_{\pm}\equiv L_{x}\pm iL_{y}$$
Il commutatore con $L_{z}$ è
$$[L_{z},L_{\pm}]=[L_{z},L_{x}]\pm i[L_{z},L_{y}]=i\hbar L_{y}\pm i(-i\hbar L_{x})=\pm\hbar(L_{x}\pm iL_{y})=\pm\hbar L_{\pm}$$
e anche
$$[L^{2},L_{\pm}]=0$$
Voglio dimostrare che se $f$ è un'autofunzione di $L^{2}$ e $L_{z}$, lo è anche $L_{\pm}f$. Dalla commutatività qui sopra
$$L^{2}(L_{\pm}f)=L_{\pm}(L^{2}f)=L_{\pm}(\lambda f)=\lambda(L_{\pm}f)$$
che è un'equazione agli autovalori con autofunzione appunto $L_{\pm}f$. Controlliamo anche $L_{z}$ con la sua commutatività:
$$L_{z}(L_{\pm}f)=[L_{z},L_{\pm}]f+L_{\pm}L_{z}f=\pm\hbar L_{\pm}f+L_{\pm}(\mu f)=(\mu\pm\hbar)(L_{\pm}f)$$
che è un'altra equazione agli autovalori, ma con un nuovo autovalore $\mu\pm\hbar$. Chiamiamo $L_{+}$ l'operatore di creazione (o di salita) perché *aumenta* l'autovalore di $\hbar$, mentre $L_{-}$ l'operatore di distruzione (o di discesa) perché lo *diminuisce* di $\hbar$. Questi operatori ci permettono di costruire una "scaletta" di autovalori a partire da qualunque valore $\lambda$, con passi di $\hbar$.

Questa scaletta deve avere un termine, dato che il momento angolare totale è finito e quindi nessuna sua componente può essere più grande di essa. Formalmente vale  $\left\langle L^{2} \right\rangle=\left\langle L_{x}^{2} \right\rangle+\left\langle L_{y}^{2} \right\rangle+\left\langle L_{z}^{2} \right\rangle$, ma $\left\langle L_{x}^{2} \right\rangle=\langle f|L_{x}^{2}f\rangle=\langle L_{x}f|L_{x}f\rangle\geq0$ (lo stesso per $L_{y}$), dunque $\lambda=\left\langle L_{x}^{2} \right\rangle+\left\langle L_{y}^{2} \right\rangle+\mu^{2}\geq\mu^{2}$.