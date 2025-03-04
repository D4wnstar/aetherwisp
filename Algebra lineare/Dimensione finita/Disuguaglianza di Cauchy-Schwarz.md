Preso uno [[prodotto scalare]] $(v,w)$ in uno [[Vector space]] $V$, si chiama **disuguaglianza di Cauchy-Schwarz** la seguente espressione
$$|(v,w)|\leq||v||\;||w||$$
con $||\cdot||$ la [[norma]] derivata dal prodotto scalare, valida per qualunque $v,w\in V$. La disuguaglianza è satura se un vettore è multiplo dell'altro, ossia $w=\gamma v$ con $\gamma \in \mathbb{R}$. In altre parole, devono essere paralleli, $v\parallel w$.

> [!example] Dimostrazione
> Vogliamo
> $$\lvert \braket{ \psi | \phi }  \rvert ^{2}=||\psi||^{2}\, ||\phi||^{2}\quad\Leftrightarrow\quad \ket{\phi} =\gamma \ket{\psi} $$
> Allora dimostriamolo per assurdo. Diciamo che $\ket{\phi}$ non sia parallelo a $\ket{\psi}$ e che quindi ci sia una componente perpendicolare $\ket{\psi_{\perp}}$,
> $$\ket{\phi} =\gamma \ket{\psi} +\delta \ket{\psi_{\perp}} $$
> Allora
> $$||\phi||^{2}=\lvert \gamma \rvert ^{2}||\psi||^{2}+\lvert \gamma \rvert ^{2}||\psi_{\perp}||^{2}$$
> Troviamo il prodotto scalare
> $$\lvert \braket{ \phi | \psi }  \rvert ^{2}=\lvert \gamma \rvert ^{2}||\psi||^{4}=||\psi||^{2}(\lvert \gamma \rvert ^{2}||\psi||^{2}+\lvert \delta \rvert ^{2}||\psi_{\perp}||^{2})=\lvert \gamma \rvert ^{2}||\psi||^{4}+\lvert \delta \rvert ^{2}||\psi||^{2}||\psi_{\perp}||^{2}$$
> Il termine $\lvert \gamma \rvert^{2}||\psi||^{4}$ si cancella nel secondo e nell'ultimo passaggio, quindi ci rimane
> $$0=\lvert \delta \rvert ^{2}||\psi||^{2}||\psi_{\perp}||^{2}$$
> Quindi, al di là del caso banale $\psi=0$, può solo essere $\lvert \delta \rvert^{2}=0$, ossia $\delta=0$. Quindi la componente perpendicolare è sempre zero.
