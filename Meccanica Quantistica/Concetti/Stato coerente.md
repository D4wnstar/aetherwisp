Uno **stato coerente** è un qualunque [[Equazione agli autovalori|autostato]] dell'[[Operatori di creazione e distruzione|operatore di distruzione]] $\hat{a}$ e ha la forma
$$|z\rangle=e^{-|z|^{2}/2} \sum\limits_{n=0}^{\infty} \frac{z^{n}}{\sqrt{n!}}|n\rangle$$
### Proprietà
Gli stati coerenti, sebbene siano [[Normalizzazione|normalizzati]], non sono [[Ortogonalità|ortogonali]] fra loro:
$$\langle z_{1}|z_{2}\rangle=\exp\left(- \frac{1}{2}(|z_{1}|^{2}+|z|^{2})+ z_{1}^{*}z_{2}\right)$$
Sono *ipercompleti*, ossia vale
$$\int_{\mathbb{C}}\hat{P}_{z}dz=\int_{\mathbb{C}}|z\rangle\langle z|dz=\mathbb{1}$$
La loro [[norma]] vale
$$|\langle z_{1}|z_{2}\rangle|^{2}=e^{-|z_{1}-z_{2}|^{2}}$$
### Formulazione
Consideriamo gli [[Operatori di creazione e distruzione|operatore di distruzione]] $\hat{a}$ e la sua [[equazione agli autovalori]]:
$$\hat{a}|z\rangle=z |z\rangle$$
Dato che $\hat{a}$ non è [[Operatore autoaggiunto|autoaggiunto]], $z$ in generale è complesso. Consideriamo il [[sistema ortonormale completo]] costituito dagli autostati $|p\rangle$ dell'operatore numero $\hat{a}^{+}\hat{a}$. Dato che $|z\rangle$ e i $|p\rangle$ risiedono nello stesso [[spazio di Hilbert]], possiamo esprimere $|z\rangle$ come combinazione lineare dei $|p\rangle$ come
$$|z\rangle=\sum\limits_{p=1}^{\infty}c_{p}(z)|p\rangle$$
da cui
$$\begin{cases}
\hat{a}|z\rangle=\sum\limits_{p=1}^{\infty}c_{p}(z)\sqrt{p}|p-1\rangle=\sum\limits_{k=0}^{\infty}c_{k+1}(z)\sqrt{k+1}|k\rangle \\
z |z\rangle=\sum\limits_{k=0}^{\infty}c_{k}(z)z |k\rangle
\end{cases}$$
e quindi
$$\sum\limits_{k=0}^{\infty}c_{k+1}(z)\sqrt{k+1}|k\rangle=\sum\limits_{k=0}^{\infty}c_{k}(z)z |k\rangle$$
e allora
$$c_{k+1}(z)= \frac{z}{\sqrt{k+1}}c_{k}(z)=\frac{z^{2}}{\sqrt{(k+1)k}}c_{k-1}(z)= \frac{z^{k+1}}{\sqrt{(k+1)!}}c_{0}(z)$$
quindi l'autostato è
$$|z\rangle=c_{0}(z)\sum\limits_{k=0}^{\infty} \frac{z^{k}}{\sqrt{k!}}|k\rangle$$
Gli autostati dell'operatore di distruzione sono [[Normalizzazione|normalizzati]], quindi vale
$$1=||\,|z\rangle\,||^{2}=|c_{0}(z)|^{2}\sum\limits_{k,p=0}^{\infty} \frac{z^{k+p}}{\sqrt{k!p!}}\langle k|p\rangle=|c_{0}(z)|^{2}\sum\limits_{k,p=0}^{\infty} \frac{z^{k+p}}{\sqrt{k!p!}}\delta_{kp}=|c_{0}(z)|^{2}\sum\limits_{j=0}^{\infty} \frac{|z|^{2j}}{\sqrt{j!}}=$$
$$=|c_{0}(z)|^{2}e^{|z|^{2}} \Rightarrow |c_{0}(z)|^{2}=e^{-|z|^{2}}$$
Dato che il termine di fase è arbitrario lo poniamo a zero, quindi abbiamo
$$c_{0}(z)=e^{-|z|^{2}/2}$$
Ora che sappiamo i coefficienti, possiamo esprimere lo stato coerente come
$$|z\rangle=e^{-|z|^{2}/2} \sum\limits_{n=0}^{\infty} \frac{z^{n}}{\sqrt{n!}}|n\rangle$$
### Evoluzione temporale
È interessante studiare in ulteriore dettaglio come gli stati coerenti evolvono nel tempo. Nella [[Rappresentazioni della meccanica quantistica|rappresentazione di Schrödinger]], lo stato coerente $|z\rangle$ evolve nel tempo con l'[[evolutore]] come
$$|z_{t}\rangle=\hat{U}_{t}|z\rangle=e^{-|z|^{2}/2}\sum\limits_{k=0}^{\infty} \frac{z^{k}}{\sqrt{k!}}\hat{U}_{t}|k\rangle$$
Dato che
$$|k\rangle= \frac{(\hat{a}^{+})^{k}}{\sqrt{k!}}|0\rangle$$
abbiamo
$$|z_{t}\rangle=e^{-|z|^{2}/2}\sum\limits_{k=0}^{\infty} \frac{z^{k}}{k!}\hat{U}_{t}(\hat{a}^{+})^{k}|0\rangle=\ldots$$
usando l'[[Operatore unitario|unitarietà]] dell'evolutore
$$\ldots=e^{-|z|^{2}/2}\sum\limits_{k=0}^{\infty} \frac{z^{k}}{k!}\hat{U}_{t}(\hat{a}^{+})^{k}\hat{U}^{+}_{t}\hat{U}_{t}|0\rangle=e^{-|z|^{2}/2}\sum\limits_{k=0}^{\infty} \frac{z^{k}}{k!}(\hat{a}^{+}_{-t})^{k}\hat{U}_{t}|0\rangle=$$
$$=\ldots=e^{-|z|^{2}/2}\sum\limits_{k=0}^{\infty} \frac{z^{k}}{k!}e^{-i\omega tk}(\hat{a}^{+})^{k}e^{- (i/\omega)t(\hat{n}+1/2)}|0\rangle=e^{-|z|^{2}/2}\sum\limits_{k=0}^{\infty} \left(\frac{ze^{-i\omega t}}{k!}\right)^{k}e^{-i\omega t/2}\sqrt{k!}|k\rangle=$$
$$=e^{-i\omega t/2}e^{-|z\exp(-i\omega t)|^{2}/2}\sum\limits_{k=0}^{\infty}\frac{(ze^{-i\omega t})^{k}}{\sqrt{k!}}|k\rangle$$
e quindi
$$\boxed{|z_{t}\rangle=e^{-i\omega t/2}|e^{-i\omega t}z\rangle}$$
### Probabilità
A ciascuno stato coerente è associata una distribuzione di probabilità
$$P(n|z)=|\langle n|z\rangle|^{2}=\frac{e^{-|z|^{2}/2}}{\sqrt{n!}}z^{-n}\frac{e^{-|z|^{2}/2}}{\sqrt{n!}}z^{n}=e^{-|z|^{2}} \frac{|z|^{2n}}{n!}$$
che è una [[distribuzione di Poisson]]. Il suo valor medio è $|z^{2}|$, che è il valor medio dell'operatore numero.

Vale una proprietà importante riguardo alle fluttuazioni di uno stato coerente: presi $\hat{q}$ e $\hat{p}$ operatori di posizione e momento in uno stato coerente, la [[disuguaglianza di Heisenberg]] è satura:
$$\sigma^{2}_{\hat{q}}\sigma^{2}_{\hat{p}}=\frac{\hbar^{2}}{4}$$