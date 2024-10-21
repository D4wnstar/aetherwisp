> [!info] Teorema
> In una dimensione, lo [[spettro]] discreto di una [[Hamiltoniana]] (ossia un insieme di [[Equazione agli autovalori|autostati]] [[Normalizzazione|normalizzati]], o funzioni [[Spazi Lp|L^2]]) è non-[[Degenerazione|degenere]].
#### Dimostrazione
Considero una Hamiltoniana $\hat{H}$ e una [[funzione d'onda]] $\psi$. Per l'[[Equazione di Schrödinger]] vale
$$(\hat{H}\psi)(x)=- \frac{\hbar^{2}}{2m}\psi''(x)+V(x)\psi(x)$$
Ma anche
$$(\hat{H}\psi)(x)=E\psi(x)$$
Per due stati $\psi_{1}$ e $\psi_{2}$ assumiamo $\psi_{1}(x)\neq \psi_{2}(x)$. Allora vogliamo vedere se c'è degenerazione:
$$\begin{align}
(\hat{H}\psi_{1})(x)=E\psi_{1}(x) = - \frac{\hbar^{2}}{2m}\psi_{1}''(x)+V(x)\psi_{1}(x) \\
(\hat{H}\psi_{2})(x)=E\psi_{2}(x) = - \frac{\hbar^{2}}{2m}\psi_{2}''(x)+V(x)\psi_{2}(x)
\end{align}$$
Non sapendo cos'è $V(x)$, non possiamo risolvere le equazioni direttamente, quindi bisogna trovare un modo per bypassare il termine. Posso moltiplicare la 1 per $\psi_{2}$ e la 2 per $\psi_{1}$:
$$\begin{align}
E\psi_{1}(x)\psi_{2}(x)&=- \frac{\hbar^{2}}{2m}\psi_{1}''(x)\psi_{2}(x)+V(x)\psi_{1}(x)\psi_{2}(x) \\
E\psi_{2}(x)\psi_{1}(x)&=- \frac{\hbar^{2}}{2m}\psi_{2}''(x)\psi_{1}(x)+V(x)\psi_{2}(x)\psi_{1}(x)
\end{align}$$
ma adesso posso eguagliare le due equazioni per trovare
$$0=\psi_{1}''(x)\psi_{2}(x)-\psi_{2}''(x)\psi_{1}(x)=\frac{d}{dx}(\psi_{1}'(x)\psi_{2}(x)-\psi_{1}(x)\psi_{2}'(x))$$
da cui si evince che $\psi_{1}'(x)\psi_{2}-\psi_{1}(x)\psi_{2}'(x)$ è pari ad una costante $c$. Ma le autofunzioni devono essere a quadrato sommabile e quindi andare a zero all'infinito. Ma l'unica costante che va a zero a infinito e lo zero stesso, quindi $c=0$. In altre parole,
$$\psi_{1}'(x)\psi_{2}(x)=\psi_{1}(x)\psi_{2}'(x)\quad\Rightarrow \quad \frac{\psi_{1}'(x)}{\psi_{1}(x)}=\frac{\psi_{2}'(x)}{\psi_{2}(x)}\quad\Rightarrow \quad \frac{d}{dx}\ln \psi_{1}(x)=\frac{d}{dx}\ln \psi_{2}(x)\quad\Rightarrow$$
$$\Rightarrow \quad \ln \psi_{1}(x)=\ln \psi_{2}(x)+a\quad\Rightarrow \quad \psi_{1}(x)=\psi_{2}(x)e^{a}$$

