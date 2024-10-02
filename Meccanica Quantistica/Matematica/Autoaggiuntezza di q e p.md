Gli [[operatore|operatori]] $\hat{q}$ e $\hat{p}$ sono gli operatori più importanti della meccanica quantistica, rappresentando rispettivamente la posizione e il momento della [[particella]] considerata. Come per tutte le [[Osservabile|osservabili]] quantistiche, questi operatori sono [[Operatore autoaggiunto|autoaggiunti]].
### Autoaggiuntezza di $\hat{p}$
Consideriamo due funzioni generiche $\psi$ e $\phi$. Ricordiamo che vale
$$(\hat{p}\psi)(x)=-i\hbar \psi(x)\tag{1}$$
Allora partiamo dalla definizione di autoaggiuntezza e sviluppiamo il [[prodotto scalare]]
$$\begin{align}
\braket{ \psi | \hat{p}\phi }&=\int_{-\infty}^{\infty} \overline{\psi(x)}\left( -i\hbar \partial_{x}  \phi(x) \right) \, dx  \\
&=-i\hbar \overline{\psi(x)}\phi(x)|_{-\infty}^{\infty}+i\hbar \int_{-\infty}^{\infty} \overline{\partial_{x}  \psi (x)}\phi(x) \, dx \\
&=\int_{-\infty}^{\infty} \overline{-i\hbar \partial_{x}  \psi(x)}\phi(x) \, dx =\braket{ \hat{p}\psi | \phi } 
\end{align}$$
usando l'[[integrazione per parti]]. Quindi $\hat{p}$ è autoaggiunto: $\hat{p}=\hat{p}^{+}$.
### Autoaggiuntezza di $\hat{q}$
Consideriamo due funzioni generiche $\psi$ e $\phi$. Ricordiamo che vale
$$(\hat{q}\psi)(x)=x\psi(x)\tag{2}$$
Cerchiamo se anche $\hat{q}$ è autoaggiunto, sviluppando
$$\braket{ \psi |\hat{q}\phi  }=\int_{-\infty}^{\infty} \overline{\psi(x)}(\hat{q}\phi)(x) \, dx=\int_{-\infty}^{\infty} \overline{\psi(x)}x\phi(x) \, dx  =\int_{-\infty}^{\infty} \overline{x\psi(x)}\phi(x) \, dx =\braket{ \hat{q}\psi | \phi }  $$
usando che $x \in \mathbb{R}$ e quindi $\overline{x}=x$. $\hat{q}$ quindi è autoaggiunto.
### Relazioni costitutive della commutazione
Le relazioni $(1)$ e $(2)$ denotano le [[Rappresentazioni dello stato|rappresentazioni in posizione]] $\hat{q}$ e $\hat{p}$:
$$\boxed{\begin{align}
(\hat{q}\psi)(x)&=x\psi(x) \\
(\hat{p}\psi)(x)&=-i\hbar \partial_{x}  \psi(x)
\end{align}}$$
