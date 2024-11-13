L'**operatore di traslazione** o di **displacement** $\hat{D}(\alpha)$ è un [[operatore]] che tipicamente compare in ottica quantistica che trasforma lo [[stato]] fondamentale $\ket{0}$ di un [[oscillatore armonico quantistico]] in uno [[stato coerente]] $\ket{\alpha}$ di [[Equazione agli autovalori|autovalore]] $\alpha \in \mathbb{C}$. In simboli
$$\hat{D}(\alpha)\ket{0} =\ket{\alpha} $$
Ha una forma chiusa data da
$$\hat{D}(\alpha)=e^{\alpha \hat{a}^{+}-\alpha^{*}\hat{a}}$$
### Proprietà
- È [[Operatore unitario|unitario]], infatti $D^{+}(\alpha)=e^{-\alpha \hat{a}^{+}+\alpha^{*}\hat{a}}=\hat{D}(-\alpha)=\hat{D}^{-1}(\alpha)$.

Se applicato all'[[Operatori di creazione e distruzione|operatore di distruzione]] $\hat{a}$ vale
$$\begin{align}
\hat{a}_{\alpha}&=D^{+}(\alpha)\hat{a}D(\alpha)=e^{\alpha^{*}\hat{a}-\alpha \hat{+}}\hat{a}e^{\alpha \hat{a}-\alpha \hat{a}^{+}}=\sum_{k=0}^{\infty} \frac{1}{k!}\underbrace{ [\alpha^{*}\hat{a}-\alpha  \hat{a}^{+},[\alpha^{*}\hat{a}-\alpha \hat{a}^{+},\ldots] }_{ k\text{ volte} }]= \\
&=\hat{a}+ \underbrace{ [\alpha^{*}\hat{a}-\alpha \hat{a},\hat{a}] }_{ \alpha }+ \frac{1}{2}\underbrace{ [\alpha^{*}\hat{a}-\alpha \hat{a}^{+},\underbrace{ [\alpha^{*}\hat{a}-\alpha \hat{a}^{+},\hat{a}] }_{ \alpha }] }_{ 0 }+ 0=\hat{a}+\alpha
\end{align}$$
quindi aggiunge una traslazione $\alpha$ all'operatore di distruzione. Vediamo anche l'operatore di creazione $\hat{a}^{+}$ e notiamo che $(\hat{a}^{+})_{\alpha}=(\hat{a}_{\alpha})^{+}$ grazie alle proprietà dell'[[Operatore aggiunto|aggiunto]]. Ma allora
$$(\hat{a}^{+})_{\alpha}=(\hat{a}_{\alpha})^{+}=(\hat{a}+\alpha)^{+}=\hat{a}^{+}+\alpha^{*}$$
### Dimostrazione
Partendo da
$$e^{\alpha \hat{a}^{+}-\alpha^{*}\hat{a}}\ket{0} =e^{-\lvert \alpha \rvert^{2}/2}e^{\alpha \hat{a}^{+}}e^{-\alpha^{+}\hat{a}}\ket{0} =\ldots$$
Possiamo scoprire l'azione dell'esponenziale espandendolo in [[serie esponenziale]]:
$$e^{-\alpha^{*}\hat{a}}\ket{0} =\sum_{k=0}^{\infty} \frac{(-\alpha^{*})^{k}}{k!} \hat{a}^{k}\ket{0} =\ket{0} $$
Dato che $\hat{a}^{k}\ket{0}=0$, rimane solo il primo termine con $k=0$. Allora
$$\ldots=e^{-\lvert \alpha \rvert ^{2}/2}e^{\alpha \hat{a}^{+}}\ket{0} =\ldots$$
e ancora in serie esponenziale
$$e^{\alpha \hat{a}^{+}}\ket{0} =\sum_{k=0}^{\infty} \frac{\alpha^{k}}{k!}(\hat{a}^{+})^{k}\ket{0} =\sum_{k=0}^{\infty} \frac{\alpha^{k}}{\sqrt{ k! }}\ket{k} $$
$$\ldots=e^{-\lvert \alpha \rvert ^{2}/2}\sum_{k=0}^{\infty} \frac{\alpha^{k}}{\sqrt{ k! }}\ket{k} =\ket{\alpha} $$
