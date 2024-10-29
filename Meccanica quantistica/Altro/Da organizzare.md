La probabilità di trovare $|\phi\rangle$ quanto siamo nello [[Stato]] $|\psi\rangle$ è il modulo quadrato della rappresentazione di $\psi$ in $\phi$:
$$Prob(|\phi\rangle\; |\; |\psi\rangle)=|\langle \phi|\psi\rangle|^{2}=\langle \psi|\hat{P}_{\phi} |\psi\rangle$$
In questo caso, l'[[Osservabile]] è $\hat{A}=|\phi\rangle\langle \phi|=\hat{P}_{\phi}$. La probabilità è simmetrica.
$$\langle \psi| \langle \phi|\psi\rangle |\phi\rangle= \langle \psi|\phi\rangle \langle \phi|\psi\rangle=^{\ast}\langle \psi|\phi\rangle\overline{\langle \psi|\phi\rangle}=|\langle \psi|\phi\rangle|^{2}=$$
$$=Prob(|\psi\rangle\;|\; |\phi\rangle)$$
$$=^{\ast}\;\overline{\langle \phi|\psi\rangle} \langle \phi|\psi\rangle=|\langle \phi|\psi\rangle|^{2}=Prob(|\phi\rangle\;|\;|\psi\rangle)$$
$$\hat{P}_{\psi}=|\psi\rangle\langle \psi| \rightarrow \hat{P}_{\psi_{t}}=\hat{U}_{t}\hat{P}_{\psi_{t}}\hat{U}_{t}^{\dagger}$$

$$\begin{cases}
\partial_{t}\hat{P}_{\psi_{t}}=- \frac{i}{\hbar}[A,\hat{P}_{\psi_{t}}]& \mbox{ equazione di Heisenberg} \\
\partial_{t}\hat{\rho}_{t}=- \frac{i}{\hbar}[\hat{H}, \hat{\rho}_{t}]& \mbox{ equazione di Liouville-Von Neumann}
\end{cases}$$
dove $[A,B]$ è il [[Commutatore]].

---
$$\hat{H}=\hbar\omega(\hat{a}^{\dagger}\hat{a}+ \frac{1}{2})$$
$$\hat{H}|n\rangle=\hbar\omega\left(n+ \frac{1}{2}\right)|n\rangle\quad\forall n\in \mathbb{N}$$
$$\psi_{n}=\langle n|x\rangle$$
$$P_{t}(\psi_{n}|\psi)=|\langle n|\hat{U}_{t}\psi\rangle|^{2}=|\langle \hat{U}_{t}^{\dagger}n|\psi\rangle|^{2}=|\langle n|\psi\rangle|^{2}$$
Cerco qual è la probabilità stato coerente
$$|z\rangle=e^{- \frac{|z|^{2}}{2}}\sum\limits_{n=0}^{\infty} \frac{z^{n}}{\sqrt{n!}}|n\rangle$$
$$\{P(n|z)=|\langle n|z\rangle|^{2}\}_{n=0}^{\infty}$$
La probabilità somma a 1 perché $|\langle n|z\rangle|^{2}=\langle n|z\rangle \langle z|n\rangle=\langle z|n\rangle \langle n|z\rangle=\langle z|z\rangle=1$. Per trovare la distribuzione di probabilità possiamo sviluppare il modulo quadro
$$|\langle n|z\rangle|^{2}= e^{-|z|^{2}} \frac{(|z|^{2})^{n}}{n!}$$
che è una distribuzione Poissoniana.
Verificare l'indeterminazione di un qualsiasi stato coerente.
$$\Delta_{\psi}\hat{q}\Delta_{\psi}\hat{p}\geq \frac{\hbar^{2}}{4}$$
$$\hat{q}=\sqrt{\frac{\hbar}{2m\omega}}(\hat{q}+\hat{a}^{\dagger})$$
$$\hat{p}=i(-\hat{a}+\hat{a}^{\dagger})\sqrt{\frac{\hbar m\omega}{2}}$$
$$\Delta_{|z\rangle}\hat{q}=\langle z|\hat{q}^{2}|z\rangle-(\langle z|\hat{q}|z\rangle)^{2}$$
Calcolo i due termini separatamente
$$\langle z|\hat{q}|z\rangle=\sqrt{\frac{\hbar}{2m\omega}}\langle z|(\hat{a}+\hat{a}^{\dagger})|z\rangle=^{\ast}(z+z^{\ast})\sqrt{\frac{\hbar}{2m\omega}}=\sqrt{\frac{\hbar}{2m\omega}}\Re(z)$$
risolto usando che $z$ è un autostato di $\hat{a}$. Altrimenti si può fare i calcoli per esteso
$$\ldots=^{\ast}\sqrt{\frac{\hbar}{2m\omega}}e^{-|z|^{2}}\sum\limits_{l=0}^{\infty}\sum\limits_{k=0}^{\infty} \frac{(z^{\ast})^{l}}{\sqrt{l!}} \frac{z^{k}}{\sqrt{k!}}\langle l|(\hat{a}+\hat{a}^{\dagger})|k\rangle=\ldots$$
$$\langle l|(\hat{a}+\hat{a}^{\dagger})|k\rangle=\langle l|(\sqrt{k}|k-1\rangle)+\sqrt{k+1}|k+1\rangle)=\sqrt{k}\delta_{l,k-1}+\sqrt{k+1}\delta_{l,k+1}$$
$$\ldots=\sqrt{\frac{\hbar}{2m\omega}}e^{-|z|^{2}}\left(\sum\limits_{k=1}^{\infty} \frac{(z^{\ast})^{k-1}z^{k}}{\sqrt{k!(k-1)!}}+\sum\limits_{k=0}^{\infty} \frac{(z^{\ast})^{k+1}z^{k}}{\sqrt{k!(k+1)!}}\right)=$$
$$=\sqrt{\frac{\hbar}{2m\omega}}e^{-|z|^{2}}\sum\limits_{l=0}^{\infty}\frac{(z^{\ast})^{l}z^{l+1}+(z^{\ast})^{l+1}z^{l}}{\sqrt{l!(l+1)!}}=\sqrt{\frac{\hbar}{2m\omega}}e^{-|z|^{2}}\sum\limits_{l=0}^{\infty}|z|^{2l} \frac{z+z^{\ast}}{\sqrt{l!(l+1)!}}=$$
$$=\sqrt{\frac{\hbar}{2m\omega}}(z+z^{\ast})e^{-|z|^{2}}\sum\limits_{l=0}^{\infty} \frac{|z|^{2l}}{l!\sqrt{l+1}}$$
(calcoli sbagliati)
Calcolo anche il secondo termine
$$\langle z|\hat{q}^{2}|z\rangle=\frac{\hbar}{2m\omega}\langle z|(\hat{a}^{2}+\hat{a}^{\dagger^{2}}+\hat{a}\hat{a}^{\dagger}+\hat{a}^{\dagger}\hat{a})|z\rangle=$$
$$=\frac{\hbar}{2m\omega}\langle z|(z^{2}+(z^{\ast})^{2}+1+|z|^{2}+|z|^{2})|z\rangle=\ldots$$
usando che $\hat{a}\hat{a}^{\dagger}=1+\hat{a}^{\dagger}\hat{a}$ 
$$=\frac{\hbar}{2m\omega}(z^{2}+|z^{\ast}|^{2}+1+2|z|^{2})$$
Tornando alla varianza
$$\Delta_{|z\rangle}\hat{q}=\frac{\hbar}{2m\omega}$$
Ripetendo i calcoli per $\Delta_{t}\hat{p}$ si trova
$$\Delta_{t}\hat{p}=\frac{\hbar m\omega}{2}$$
Allora l'indeterminazione di uno stato coerente è
$$\boxed{\Delta_{|z\rangle}\hat{q}\Delta_{t}\hat{p}=\frac{\hbar^{2}}{4}}$$

---

$$e^{\hat{A}}\hat{B}e^{-\hat{A}}=\sum\limits_{k=0}^{\infty} \underbrace{\frac{1}{k!}[\hat{A},[\hat{A},[\hat{A},\ldots,[\hat{A},\hat{B}]]]]}\limits_{\mbox{k parentesi}}=$$
$$=\hat{B}+[\hat{A}+\hat{B}]+\ \frac{1}{2}[\hat{A},[\hat{A},\hat{B}]]+\ldots\left(1+\hat{A}+ \frac{1}{2}\hat{A}^{2}+\ldots\right)\hat{B}\left(1-\hat{A}+ \frac{\hat{A}^{2}}{2}+\ldots\right)=$$
$$=\hat{B}+\hat{A}\hat{B}-\hat{B}\hat{A}+ \frac{ \hat{A}\hat{A}\hat{B}+\hat{B}\hat{A}\hat{A}-\hat{A}\hat{B}\hat{A}-\hat{A}\hat{B}\hat{A}+\ldots}{2}=$$
$$=\hat{B}+[\hat{A},\hat{B}]+ \frac{1}{2}(\hat{A}[\hat{A},\hat{B}]-[\hat{A},\hat{B}])+\ldots$$

$$e^{\frac{i}{\hbar}q\hat{p}}\hat{q}e^{- \frac{i}{\hbar}q\hat{p}}=\hat{q}+q$$
$$e^{\frac{i}{\hbar}p\hat{q}}\hat{p}e^{- \frac{i}{\hbar}p\hat{q}}=\hat{p}-p$$
Prendo l'*operatore di spostamento* 
$$\hat{D}(\alpha)=e^{\alpha\hat{a}^{\dagger}-\alpha^{\ast}\hat{a}}$$
Si vuole quale segno è corretto in
$$\hat{D}^{\dagger}(\alpha)\hat{a}\hat{D}(\alpha)=\hat{a}\overbrace{\pm}^{?}\alpha$$
usando la *formula di Baker-Campbell-Hausdorff*: se $[\hat{A},\hat{B}]=c\hat{\mathbb{1}}$ allora $e^{\hat{A}+\hat{B}}=e^{- \frac{1}{2}[\hat{A},\hat{B}]}e^{\hat{A}}e^{\hat{B}}$.