Consideriamo un integrale della media di posizione o quantità di moto per una data [[funzione d'onda]] $\psi_{n}$ per l'[[oscillatore armonico quantistico]]. Si ha un'espressione della forma
$$\int_{-\infty}^{+\infty}\psi_{n}^{*}x^{i}\psi_{n}\; dx=\langle \psi|x^{i}|\psi\rangle\quad\text{ o }\quad \int_{-\infty}^{+\infty}\psi^{*}_{n}p^{i}\psi_{n}\;dx=\langle \psi|p^{i}|\psi\rangle$$
Possiamo esprimere $x$ e $p$ in funzione degli [[operatori di creazione e distruzione]] come
$$x=\sqrt{\frac{\hbar}{2m\omega}}(a_{+}+a_{-})\quad\text{o}\quad p=i\sqrt{\frac{\hbar m\omega}{2}}(a_{+}-a_{-})$$
Possiamo sfruttare il fatto che $(a_{+})^{i}\psi_{n}=\psi_{n+i}$, che è ortogonale a $\psi_{n}$ dato che le $\psi_{n}$ formano un [[Sistema ortonormale completo]] e quindi $\langle \psi_{n}|\psi_{n+i}\rangle=0$. Allora, molti termini si annullano per ortogonalità, mentre per gli altri possiamo sfruttare che
$$a_{+}a_{-}\psi_{n}=n\psi_{n},\quad a_{-}a_{+}\psi_{n}=(n+1)\psi_{n}$$
e di nuovo l'ortonormalità con $\psi_{n}^{*}\psi_{n}=1$.

Per un esempio, calcoliamo $\left\langle x^{2} \right\rangle$:
$$\int_{-\infty}^{+\infty}\psi_{n}^{*}x^{2}\psi_{n}\;dx=\int_{-\infty}^{+\infty}\psi_{n}^{*}\frac{\hbar}{2m\omega}[(a_{+})^{2}+(a_{+}a_{-})+(a_{-}a_{+})+(a_{-})^{2}]\psi_{n}\;dx=$$
$$=\frac{\hbar}{2m\omega}\left[\int\psi_{n+2}^{*}\psi_{n}dx+\int\psi_{n}^{*}(a_{+}a_{-})\psi_{n}dx+\psi_{n}^{*}(a_{-}a_{+})\psi_{n}dx+\int\psi_{n-2}^{*}\psi_{n}dx\right]=$$
$$=\frac{\hbar}{2m\omega}\left[0 + \int_{-\infty}^{+\infty}\psi_{n}^{*} n\psi_{n}dx + \int_{-\infty}^{+\infty}\psi_{n}^{*}(n+1)\psi_{n}dx + 0 \right]=$$
$$=\frac{\hbar}{2m\omega}[n+n+1]=\frac{\hbar}{m\omega}\left(n+ \frac{1}{2}\right)$$
