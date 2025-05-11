---
wiki-publish: true
---
The **variational method** is a method of finding approximate solution to quantum problems, typically finding [[Equazione agli autovalori|eigenvalues]] and [[Equazione agli autovalori|eigenfunctions]] of a time-independent [[Hamiltonian]].
### Method
Consider some time-independent Hamiltonian $H$ of a function $\phi$ which can vary freely, called a **trial function**. We define the [[Functional]]:
$$E(\phi)=\frac{\braket{ \phi | H|\phi }}{\braket{ \phi | \phi } } $$
This is the [[mean]] value of $E$ in the state $\ket{\phi}$. As usual, if $\ket{\phi}$ is an eigenstate, then $E(\phi)$ is an [[Stato stazionario|energy eigenvalue]]. The heart of the method is this:

> [!info] Variational principle
> Every function for which $E(\phi)$ is stationary, that is, $dE(\phi)/d\phi=0$, is an eigenfunction of $H$.

To prove this, let's consider a small variation $\delta \phi$ of $\phi$. We now look for the eigenvalues of $E$ for the varied function:
$$E(\phi+\delta \phi)\braket{ \phi+\delta \phi | \phi+\delta \phi } =\braket{ \phi+\delta \phi | H|\phi+\delta \phi } $$
$$\begin{align}
\delta E\int \phi^{*}\phi d\tau&=-E\int \delta\phi^{*}\phi d\tau-E\int  \phi^{*}\delta\phi d\tau+\int \delta \phi^{*}H\phi d\tau +\int \phi^{*}H\delta \phi d\tau \\
&=\int \delta \phi^{*}(H-E)\phi d\tau+\int \phi^{*}(H-E)\delta \phi d\tau
\end{align}$$
But we want $E$ to be stationary, in which case $\delta E=0$ always. Thus, the left hand side must be zero. This is our condition to find $\phi$; the rest is "just" a matter of solving the equation.

For example, consider the [[Equazione di Schrödinger|Schrödinger equation]] $H\psi_{n}=E_{n}\psi_{n}$, indexed by a [[Numero quantico|quantum number]] $n\geq0$. The ground state is $n=0$ with $E_{0}$. We now consider a generic function $\phi$. This can be expressed in [[Serie di Fourier|Fourier series]] in the $\{ \psi_{n} \}_{n}$ [[Sistema ortonormale completo|basis]] as
$$\phi=\sum_{n}a_{n}\psi_{n}$$
The [[expected value]] of $E(\phi)$ for this function is
$$E(\phi)=\frac{\sum_{n}\lvert a_{n} \rvert ^{2}E_{n}}{\sum_{n}\lvert a_{n} \rvert ^{2}}=E_{0}+ \frac{\sum_{n}\lvert a_{n} \rvert ^{2}(E_{n}-E_{0})}{\sum_{n}\lvert a_{n} \rvert ^{2}}\geq E_{0}$$
We hit on a lower bound. In fact, while this doesn't give us a solution, it does gives a bound to restrict what $E(\phi)$ can be:
$$\boxed{E(\phi)=\frac{\braket{ \phi | H|\phi }}{\braket{ \phi | \phi } }\geq E_{0}}$$
The variational method consists in minimizing this functional.