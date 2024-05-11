Il **metodo variazionale** è un metodo usato spesso per trovare le energie e autofunzioni di un'[[Hamiltoniana]] $H$ indipendente dal tempo. Consideriamo una funzione $\phi$ che può variare liberamente. Allora definiamo il funzionale
$$E(\phi)=\frac{\langle \phi|E |\phi\rangle}{\langle \phi|\phi\rangle}$$
che è il valore di aspettazione di $E$ nello stato $\phi$ normalizzato per $\langle \phi|\phi\rangle=|\phi|^{2}$. Se $\phi$ è un [[autostato]], $E(\phi)$ è un autovalore di energia. Ogni funzione per cui $E(\phi)$ è stazionaria, ossia $dE(\phi)/d\phi=0$, è un'autofunzione di $H$.

Calcoliamo il valor medio di $H$:
$$\left\langle H \right\rangle= \frac{\langle \phi|H |\phi\rangle}{\langle \phi|\phi\rangle}=\frac{\int_{-\infty}^{+\infty}\phi^{*}H\phi d\tau}{\int_{-\infty}^{+\infty}\phi^{*}\phi d\tau}$$

Considero una variazione infinitesima di $\tilde{\phi}=\phi+\delta \phi$. Quindi anche l'Hamiltoniana varia:
$$\left\langle H \right\rangle+ \delta \left\langle H \right\rangle=\frac{\int_{-\infty}^{+\infty}(\phi^{*}+\delta \phi^{*})H(\phi+\delta\phi)d\tau}{\int_{-\infty}^{+\infty}(\phi^{*}+\delta\phi^{*})(\phi+\delta\phi)d\tau}=\ldots$$
Possiamo espandere l'integrale sopra, sopprimendo i limiti degli integrali per semplicità:
$$\ldots=\frac{\int \phi^{*}H\phi d\tau+\int\delta\phi^{*}H\phi d\tau+\int \phi^{*}H\delta\phi d\tau}{\int \phi^{*}\phi d\tau + \int \delta\phi^{*}\phi d\tau+ \int \phi^{*}\delta\phi d\tau}=\ldots$$

dove gli integrali con le sole variazioni vanno a zero. Usando l'approssimazione
$$\frac{1}{1+x} \rightarrow 1 -x \quad\text{per}\quad x \rightarrow 0$$
il termine variazionale della media diventa (per qualche motivo)
$$\delta \left\langle H \right\rangle=\underbrace{\int_{-\infty}^{+\infty}\delta\phi^{*} H \phi d\tau+\int_{-\infty}^{+\infty}\phi^{*}H\delta\phi d\tau}\limits_{\text{complesso coniugato 1 (cc1)}}- \left\langle H \right\rangle\left[\underbrace{\int_{-\infty}^{+\infty}\delta\phi^{*}\phi d\tau + \int_{-\infty}^{+\infty}\phi^{*}\delta\phi d\tau}\limits_{\text{complesso coniugato 2 (cc2)}}\right]$$
e il termine variazione non della media è
$$\delta H=\left[\int_{-\infty}^{+\infty}\delta \phi^{*}H \phi d\tau +\text{cc1}\right]- \left\langle H \right\rangle \left[\int_{-\infty}^{+\infty} \delta\phi^{*}\phi d\tau+ \text{cc2}\right]$$

e imponendo la condizione di stazionarietà $\delta H=0$ troviamo
$$\int_{-\infty}^{+\infty} \delta\phi^{*}[H - \left\langle H \right\rangle]\phi+\text{cc}=0$$
che è equivalente a chiedere l'[[Equazione di Schrödinger]]
$$H\phi=E\phi$$
Quindi aggiungere un termine variazionale e chiedere la stazionarietà è equivalente a risolvere l'equazione di Schrödinger.
### Utilizzo
Consideriamo le autofunzioni di $H$: $H\Psi_{n}=E_{n}\Psi_{n}$, con stato fondamentale $n=0$ con energia $E_{0}$. Una funzione $\phi$ può essere espansa nelle autofunzioni come $\phi=\sum\limits_{n}a_{n}\Psi_{n}$. Il valore di aspettazione dell'energia su $\phi$ è
$$E(\phi)=\frac{\sum\limits_{n}|a_{n}|^{2}E_{n}}{\sum\limits_{n}|a_{n}|^{2}}=E_{0}+\frac{\sum\limits_{n}|a_{n}|^{2}(E_{n}-E_{0})}{\sum\limits_{n}|a_{n}|^{2}}\geq E_{0}$$
e quindi qualunque sia $\phi$, vale
$$E(\phi)=\frac{\langle \phi|E |\phi\rangle}{\langle \phi|\phi\rangle}\ge E_{0}$$
Per ogni $\phi$, il valore di aspettazione dell'energia è maggiore dello stato fondamentale e posso cercare un'approssimazione dello stato fondamentale minimizzando questa funzione, che è appunto il metodo variazionale.