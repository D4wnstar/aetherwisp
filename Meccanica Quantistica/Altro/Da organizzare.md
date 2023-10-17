La probabilità di trovare $|\phi\rangle$ quanto siamo nello [[stato]] $|\psi\rangle$ è il modulo quadrato della rappresentazione di $\psi$ in $\phi$:
$$Prob(|\phi\rangle\; |\; |\psi\rangle)=|\langle \phi|\psi\rangle|^{2}=\langle \psi|\hat{P}_{\phi} |\psi\rangle$$
In questo caso, l'[[osservabile]] è $\hat{A}=|\phi\rangle\langle \phi|=\hat{P}_{\phi}$. La probabilità è simmetrica.
$$\langle \psi| \langle \phi|\psi\rangle |\phi\rangle= \langle \psi|\phi\rangle \langle \phi|\psi\rangle=^{\ast}\langle \psi|\phi\rangle\overline{\langle \psi|\phi\rangle}=|\langle \psi|\phi\rangle|^{2}=$$
$$=Prob(|\psi\rangle\;|\; |\phi\rangle)$$
$$=^{\ast}\;\overline{\langle \phi|\psi\rangle} \langle \phi|\psi\rangle=|\langle \phi|\psi\rangle|^{2}=Prob(|\phi\rangle\;|\;|\psi\rangle)$$
$$\hat{P}_{\psi}=|\psi\rangle\langle \psi| \rightarrow \hat{P}_{\psi_{t}}=\hat{U}_{t}\hat{P}_{\psi_{t}}\hat{U}_{t}^{\dagger}$$

$$\begin{cases}
\partial_{t}\hat{P}_{\psi_{t}}=- \frac{i}{\hbar}[A,\hat{P}_{\psi_{t}}]& \mbox{ equazione di Heisenberg} \\
\partial_{t}\hat{\rho}_{t}=- \frac{i}{\hbar}[\hat{H}, \hat{\rho}_{t}]& \mbox{ equazione di Liouville-Von Neumann}
\end{cases}$$
dove $[A,B]$ è il [[commutatore]].