
![[Buca infinita|center]]

$$\begin{cases}
i\hbar\partial_{t}|\psi_{t}\rangle=\hat{H}|\psi_{t}\rangle \\
\psi_{t}(0)=0 \\
\psi_{t}(a)=0
\end{cases}$$
$$\begin{cases}
- \frac{\hbar^{2}}{2m}\psi''(x)=E \psi(x) \\
\psi(0)=0 \\
\psi(a)=0
\end{cases}$$
$$\begin{cases}
\frac{\hat{p}^{2}}{2m}|\psi\rangle=E |\psi\rangle \\
\psi(0)=0 \\
\psi(a)=0
\end{cases}$$
Cerco l'[[Equazioni di Schrödinger#Autoaggiuntezza di $ hat{x}$, $ hat{p}$|autoaggiuntezza]] di $\hat{x}$ e $\hat{p}$:
$$\langle \phi|\hat{p}\psi\rangle=-i\hbar\int_{0}^{a}dx \phi^{\ast}(x)\psi'(x)=-i\hbar \phi^{\ast}(x)\psi(x)|^{a}_{0}+i\hbar\int_{0}^{a}dx (\phi'(x))^{\ast}\psi(x)=$$
$$=\underbrace{-i\hbar \phi^{\ast}(x)\psi(x)|_{0}^{a}}\limits_{0}+\int_{0}^{a}dx(-i\hbar\partial_{x}\phi(x))^{\ast}\psi(x)=^{?}\langle \hat{p}^{\dagger}\phi|\psi\rangle$$
dove il termine calcolato agli estremi si annulla. Per essere vero, oltre che soddisfare l'equazione agli autovalori di $\hat{p}$ deve anche soddisfare le condizioni al contorno. Si trova che non vengono soddisfatte, quindi $\hat{p}$ non è autoaggiunto. Il suo quadrato, $\hat{p}^{2}$, invece si.