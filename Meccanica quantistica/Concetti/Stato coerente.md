Uno **stato coerente** è un qualunque [[Equazione agli autovalori|autostato]] dell'[[Operatori di creazione e distruzione|operatore di distruzione]] $\hat{a}$ e ha la forma
$$\hat{a}\ket{\alpha} =\alpha \ket{\alpha} $$
con $\alpha \in \mathbb{C}$. Si trova che l'autostato è correlato allo stato fondamentale da
$$\ket{\alpha}=e^{-|\alpha|^{2}/2} \sum\limits_{n=0}^{\infty} \frac{\alpha^{n}}{\sqrt{n!}}|n\rangle$$
### Proprietà
Gli stati coerenti, sebbene siano [[Normalizzazione|normalizzati]], non sono [[Ortogonalità|ortogonali]] fra loro:
$$\braket{  \alpha_{1} | \alpha_{2} } =\exp\left(- \frac{1}{2}(|\alpha_{1}|^{2}+|\alpha_{2}|^{2})+ \alpha_{1}^{*}\alpha_{2}\right)$$
La loro [[norma]] vale
$$\braket{  \alpha_{1} | \alpha_{2} } ^{2}=e^{-|\alpha_{1}-\alpha_{2}|^{2}}$$
Può essere ottenuto dallo stato fondamentale di un [[oscillatore armonico quantistico]] mediante l'[[Operatore di displacement]]:
$$\ket{\alpha} =e^{\alpha \hat{a}^{+}-\alpha^{*}\hat{a}}\ket{0} =\hat{D}(\alpha)\ket{0} $$
### Probabilità
Gli stati coerenti esibiscono un comportamento interessante per quanto riguarda la loro [[probability|probabilità]]. Il [[Expected value|valor medio]] dell'operatore numero in uno stato coerente è
$$\braket{ \alpha | \hat{n}| \alpha } =\braket{ \alpha | \hat{a}^{+}\hat{a}| \alpha }=\braket{ \hat{a}\alpha | \hat{a}\alpha }  =\lvert \alpha \rvert^{2} $$
Per la [[Variance|varianza]] invece troviamo
$$\braket{ \alpha | \hat{n}^{2} | \alpha } =\braket{ \alpha | (\hat{a}^{+}\hat{a})^{2}| \alpha } =\braket{ \alpha | \hat{a}^{+}\hat{a}\hat{a}^{+}\hat{a}| \alpha } =\ldots$$
Qui basta rigirare l'equazione a modo che $\hat{a}$ agisca su $\ket{\alpha}$:
$$\ldots=\lvert \alpha \rvert ^{2}\braket{ \alpha | \hat{a}\hat{a}^{+}| \alpha } =\lvert \alpha \rvert ^{2}\braket{ \alpha | (\hat{\mathbf{1}}+\hat{a}^{+}\hat{a})| \alpha } =\lvert \alpha \rvert ^{2}(1+\lvert \alpha \rvert ^{2})=\lvert \alpha \rvert ^{2}+\lvert \alpha \rvert ^{4}$$
La varianza quindi è
$$\Delta_{\alpha}\hat{n}=\sigma_{\alpha}^{2}\hat{n}=\langle \hat{n}^{2} \rangle _{\alpha}-\langle \hat{n} \rangle_{\alpha}^{2}= \lvert \alpha \rvert ^{2}$$
che è uguale al valor medio. Ma questo è interessante, perché la [[Probability distribution|distribuzione di probabilità]] con valor medio uguale alla varianza è la [[Poisson distribution|distribuzione di Poisson]]. Deve quindi nascondersi una distribuzione di Poisson entro la descrizione degli stati coerenti. Cerchiamo dunque la probabilità che l'autovalore di $\hat{n}$ sia esattamente $m$ in uno stato $\ket{\alpha}$:
$$\text{Prob}(\hat{n}=m|\alpha)=\lvert \braket{ m | \alpha }  \rvert ^{2}=\left\lvert e^{-\lvert \alpha \rvert ^{2}/2}\sum_{n=0}^{\infty} \frac{\alpha^{n}}{\sqrt{ n! }}\underbrace{ \braket{ m | n } }_{ \delta_{mn} } \right\rvert^{2} =\left\lvert e^{-\lvert \alpha \rvert ^{2}/2} \frac{\alpha^{m}}{\sqrt{ m! }} \right\rvert^{2}=e^{-\lvert \alpha \rvert ^{2}} \frac{(\lvert \alpha \rvert^{2} )^{m}}{m!}  $$
che è una distribuzione di Poisson con $\nu=\lvert  \alpha \rvert^{2}$ e $k=m$.

Vale una proprietà importante riguardo alle fluttuazioni di uno stato coerente: presi $\hat{q}$ e $\hat{p}$ operatori di posizione e momento in uno stato coerente, la [[disuguaglianza di Heisenberg]] è satura:
$$\sigma^{2}_{\hat{q}}\sigma^{2}_{\hat{p}}=\frac{\hbar^{2}}{4}$$
### Derivazione
Consideriamo gli [[Operatori di creazione e distruzione|operatore di distruzione]] $\hat{a}$ e la sua [[equazione agli autovalori]]:
$$\hat{a}\ket{\alpha}=\alpha \ket{\alpha}$$
Dato che $\hat{a}$ non è [[Operatore autoaggiunto|autoaggiunto]], $\alpha$ in generale è complesso. Consideriamo il [[sistema ortonormale completo]] costituito dagli autostati $\ket{n}$ dell'operatore numero $\hat{a}^{+}\hat{a}$. Dato che $\ket{\alpha}$ e gli $\ket{n}$ risiedono nello stesso [[spazio di Hilbert]], possiamo esprimere $\ket{\alpha}$ come combinazione lineare degli $\ket{n}$ come
$$\ket{\alpha}=\sum\limits_{n=1}^{\infty}c_{n}\ket{n}$$
e quindi
$$\begin{align}
\hat{a}\ket{\alpha} =\sum_{n=0}^{\infty} c_{n}\hat{a}\ket{n} =\sum_{n=1}^{\infty} c_{n}\sqrt{ n }\ket{\underbrace{ n-1 }_{ p }} &=\alpha \sum_{p=0}^{\infty} c_{p}\ket{p} \\
&=\sum_{p=0}^{\infty} c_{p+1}\ket{p+1} \ket{p} 
\end{align} $$
ma quindi
$$c_{p+1}\sqrt{ p+1 }=\alpha c_{p}$$
e invertendo, per ricorsione
$$c_{p+1}=\frac{\alpha}{\sqrt{ p+1 }}c_{p}=\frac{\alpha ^{2}}{\sqrt{ (p+1)p }}c_{p-1}=\frac{\alpha^{p+1}}{\sqrt{ (p+1)! }}c_{0}$$
e sostituendo
$$\ket{\alpha} =c_{0}\sum_{n=0}^{\infty} \frac{\alpha^{n}}{\sqrt{ n! }}\ket{n} =c_{0}\sum_{n=0}^{\infty} \frac{\alpha^{n}}{\sqrt{ n! }} \frac{(\hat{a}^{+})^{n}}{\sqrt{ n! }}\ket{0} =c_{0}\sum_{n=0}^{\infty} \frac{\alpha^{n}}{n!}(\hat{a}^{+})^{n}\ket{0} $$
che è l'espressione per uno stato coerente. Va notato che non abbiamo posto alcuna condizione su $\alpha$: $\hat{a}$ non è autoaggiunto quindi $\alpha$ può essere qualunque numero complesso. Ci manca solo da determinare la costante di [[normalizzazione]] $c_{0}$. Allora troviamo la [[norma]] quadra di $\ket{\alpha}$:
$$1=\lvert \lvert \ket{\alpha}  \rvert  \rvert ^{2}=\braket{ \alpha | \alpha } =|c_{0}|^{2}\sum_{n,m=0}^{\infty} \frac{(\alpha^{*})^{n}}{\sqrt{ n! }} \frac{\alpha^{m}}{\sqrt{ m! }}\underbrace{ \braket{ n | m } }_{ \delta_{nm} }=|c_{0}|^{2} \sum_{n=0}^{\infty} \frac{(\lvert \alpha \rvert ^{2})^{n}}{n!}=\lvert c_{0} \rvert ^{2}e^{\lvert \alpha \rvert^{2} } $$
Allora
$$\lvert c_{0} \rvert =e^{-\lvert \alpha \rvert ^{2}/2}$$
Mettendo tutto insieme, abbiamo definitivamente l'espressione per gli stati coerenti di un [[oscillatore armonico quantistico]]:
$$\boxed{\ket{\alpha} =e^{-\lvert \alpha \rvert ^{2}/2}\sum_{n=0}^{\infty} \frac{\alpha^{n}}{\sqrt{ n! }}\ket{n}}$$
### Evoluzione temporale
È interessante studiare come gli stati coerenti evolvono nel tempo. Nella [[Rappresentazioni della meccanica quantistica|rappresentazione di Schrödinger]], lo stato coerente $\ket{\alpha}$ evolve nel tempo con l'[[evolutore]] come $\ket{\alpha}\to \hat{U}_{t}\ket{\alpha}$. Allora
$$\hat{U}_{t}\ket{\alpha} =e^{-\lvert \alpha \rvert ^{2}/2}\sum_{k=0}^{\infty} \frac{\alpha^{k}}{\sqrt{ k! }}\hat{U}_{t}\ket{k}=\ldots $$
L'evoluzione temporale di uno [[Stato stazionario|autostato di energia]] è $\hat{U}_{t}\ket{k}=e^{-iE_{k}t/k}\ket{k}$ e sappiamo che $E_{k}$ è quella dell'oscillatore armonico quantistico, ossia $E_{k}=\hbar \omega(k+1/2)$. Allora
$$\ldots=e^{-\lvert \alpha \rvert ^{2}/2}\sum_{k=0}^{\infty} \frac{\alpha^{k}}{\sqrt{ k! }}e^{-i\omega t(k+1/2)}\ket{k}=e^{-\lvert \alpha \rvert ^{2}/2t}\sum_{k=0}^{\infty} \frac{(\alpha e^{-i\omega t})^{k}}{\sqrt{ k! }}\ket{k}=$$




---

$$|z_{t}\rangle=\hat{U}_{t}\ket{\alpha}=e^{-|z|^{2}/2}\sum\limits_{k=0}^{\infty} \frac{z^{k}}{\sqrt{k!}}\hat{U}_{t}|k\rangle$$
Dato che
$$|k\rangle= \frac{(\hat{a}^{+})^{k}}{\sqrt{k!}}|0\rangle$$
abbiamo
$$|z_{t}\rangle=e^{-|z|^{2}/2}\sum\limits_{k=0}^{\infty} \frac{z^{k}}{k!}\hat{U}_{t}(\hat{a}^{+})^{k}|0\rangle=\ldots$$
usando l'[[Operatore unitario|unitarietà]] dell'evolutore
$$\ldots=e^{-|z|^{2}/2}\sum\limits_{k=0}^{\infty} \frac{z^{k}}{k!}\hat{U}_{t}(\hat{a}^{+})^{k}\hat{U}^{+}_{t}\hat{U}_{t}|0\rangle=e^{-|z|^{2}/2}\sum\limits_{k=0}^{\infty} \frac{z^{k}}{k!}(\hat{a}^{+}_{-t})^{k}\hat{U}_{t}|0\rangle=$$
$$=\ldots=e^{-|z|^{2}/2}\sum\limits_{k=0}^{\infty} \frac{z^{k}}{k!}e^{-i\omega tk}(\hat{a}^{+})^{k}e^{- (i/\omega)t(\hat{n}+1/2)}|0\rangle=e^{-|z|^{2}/2}\sum\limits_{k=0}^{\infty} \left(\frac{ze^{-i\omega t}}{k!}\right)^{k}e^{-i\omega t/2}\sqrt{k!}|k\rangle=$$
$$=e^{-i\omega t/2}e^{-|z\exp(-i\omega t)|^{2}/2}\sum\limits_{k=0}^{\infty}\frac{(ze^{-i\omega t})^{k}}{\sqrt{k!}}|k\rangle$$
e quindi
$$|z_{t}\rangle=e^{-i\omega t/2}|e^{-i\omega t}z\rangle$$
