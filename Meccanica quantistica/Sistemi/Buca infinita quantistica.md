---
aliases:
  - buca infinita
  - particella in una scatola
---
Consideriamo un potenziale della forma
$$V=\begin{cases}
0,&\text{ se }0\leq x \leq a \\
\infty,& \text{ altrimenti}
\end{cases}$$
Una [[Particella]] in questo potenziale è perfettamente libera entro $0$ e $a$, ma non può in alcun modo uscire da questi due limiti, ai quali vi è una forza infinita che le impedisce di fuggire. Sebbene sia un potenziale chiaramente artificioso, è molto utile per testare la teoria.
![[Grafico Buca infinita|center]]
Al di fuori della buca, la [[Funzione d'onda]] $\psi(x)$ è identicamente zero, dato che la probabilità di trovare la particella lì è nulla. Dentro la buca, con potenziale $V=0$, l'[[Equazione di Schrödinger#Potenziale indipendente dal tempo|equazione di Schrödinger]] indipendente dal tempo è
$$- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}}=E\psi$$
o anche
$$\frac{d^{2}\psi}{dx^{2}}=-k^{2}\psi,\quad\text{con }k\equiv \frac{\sqrt{2mE}}{\hbar}$$
dove abbiamo assunto che $E\geq0$, che è sempre vero dato che $E\geq V_{min}=0$. Ma questa non è altro che l'[[oscillatore armonico]] classico, la cui soluzione generale è
$$\psi(x)=A\sin(kx)+B\cos(kx)$$
con $A$ e $B$ costanti arbitrarie, determinate dalle condizioni al contorno del problema. Sappiano infatti che per la continuità di $\psi$ deve valere $\psi(0)=\psi(a)=0$. Allora abbiamo
$$\psi(0)=A\sin(0)+B\cos(0)=B=0$$
e allora la soluzione generale diventa
$$\psi(x)=A\sin(kx)$$
Usando l'altra condizione $\psi(a)=0$ otteniamo
$$\psi(a)=A\sin(ka)=0$$
Abbiamo due possibilità: $A=0$, in qual caso abbiamo la soluzione banale, ma non normalizzabile (quindi la scartiamo), o $\sin(ka)=0$. Quest'ultimo caso implica
$$ka=0,\pm\pi,\pm2\pi,\pm3\pi,\ldots$$
Non può essere $k=0$ dato che renderebbe $\psi(x)$ identicamente nulla anche nella buca. Inoltre, le soluzioni negative non danno informazioni aggiuntive, dato che il segno meno può essere incluso nella costante e riottenere quella positiva in ogni caso. Le uniche soluzioni possibili e significative che ci rimangono sono dunque
$$k_{n}=\frac{n\pi}{a},\quad\text{con }n=1,2,3,\ldots$$
Ma sappiamo qual è l'espressione di $k$, da cui possiamo ottenere i valori permessi[^1] dell'energia $E$:
$$\boxed{E_{n}=\frac{\hbar^{2}k_{n}^{2}}{2m}=\frac{n^{2}\pi^{2}\hbar^{2}}{2ma^{2}}}$$
La condizione al contorno ci ha definito $k$, *non* $A$, che è quello che stavamo cercando. Fortunatamente, essa non è altro che la costante di normalizzazione della funzione d'onda:
$$\int_{0}^{a}|A|^{2}\sin^{2}(kx)dx=|A|^{2} \frac{a}{2}=1 \quad \rightarrow \quad |A|^{2}=\frac{2}{a}$$
$A$ può essere ottenuta semplicemente prendendo la radice reale positiva, tanto la fase di $A$ non fa differenza. Sapendo tutte le costanti, possiamo scrivere esplicitamente la soluzione generale
$$\boxed{\psi_{n}=\sqrt{\frac{2}{a}}\sin\left(\frac{n\pi}{a}x\right)}$$
che, come atteso, è un insieme infinito e numerabile di soluzioni. $\psi_{1}$ è la soluzione ad energia più bassa ed è detta **stato fondamentale**. $\psi_{2},\psi_{3},\ldots$ sono a energia più alta e sono dette **stati eccitati**. Queste soluzioni hanno anche proprietà interessanti:
1. sono una pari e l'altra dispari rispetto al centro della buca. $\psi_{1}$ è pari, $\psi_{2}$ è dispari, e via avanti.
2. hanno $n-1$ nodi.
3. sono ortonormali fra loro, ossia $\int_{-\infty}^{+\infty}\psi_{m}^{*}(x)\psi_{n}(x)dx=\delta_{mn}$ per ogni $m, n\in\mathbb{N}$.
4. sono [[Sistema completo|complete]], quindi ogni altra funzione può essere espressa come combinazione lineare di esse.

Dunque le soluzioni formano un [[Sistema ortonormale completo]] e una qualunque funzione può essere espressa in [[Serie di Fourier]] in questa base:
$$f(x)=\sum\limits_{n=1}^{\infty}c_{n}\psi_{n}(x)=\sqrt{\frac{2}{a}}\sum\limits_{n=1}^{\infty}c_{n}\sin\left(\frac{n\pi}{a}x\right)$$
Queste proprietà valgono *spesso*, ma non *sempre*.
1. vale solo se $V$ è simmetrico
2. vale sempre
3. vale quasi sempre
4. vale per quasi tutti i potenziali effettivamente incontrati in fisica

Aggiungendo la dipendenza temporale alle soluzioni e sommandole tutte, troviamo la soluzione all'equazione di Schrödinger dipendente dal tempo:
$$\boxed{\Psi(x,t)=\sum\limits_{n=1}^{\infty}c_{n}\psi(x)\varphi(t)=\sum\limits_{n=1}^{\infty}c_{n}\sqrt{\frac{2}{a}}\sin\left(\frac{n\pi}{a}x\right)e^{-i(n^{2}\pi^{2}\hbar/2ma^{2})t}}$$
e anche la condizione iniziale può essere trovata allo stesso modo:
$$\boxed{\Psi(x,0)=\sum\limits_{n=1}^{\infty}c_{n}\psi(x)=\sum\limits_{n=1}^{\infty}c_{n}\sqrt{\frac{2}{a}}\sin\left(\frac{n\pi}{a}x\right)}$$
I coefficienti per $\Psi(x,t)$ o $\Psi(x,0)$ possono essere calcolati come di norma
$$c_{n}=(\psi_{n},\Psi(x,t))\quad\text{ oppure }\quad c_{n}=(\psi_{n},\Psi(x,0))$$
dove la notazione intende il [[Prodotto scalare]]. La [[Norma]] di questi coefficienti, $|c_{n}|^{2}$, rappresentano la probabilità che la misura dell'energia della particella dia come risultato un certo $E_{n}$ più che un altro. La misura, inoltre, può *solo* ritornare uno degli $E_{n}$ e *mai* un valore al di fuori, al di là di errori di misura o strumentali.

---
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
Cerco l'[[Rappresentazioni dello stato#Autoaggiuntezza di $ hat{x}$, $ hat{p}$|autoaggiuntezza]] di $\hat{x}$ e $\hat{p}$:
$$\langle \phi|\hat{p}\psi\rangle=-i\hbar\int_{0}^{a}dx \phi^{\ast}(x)\psi'(x)=-i\hbar \phi^{\ast}(x)\psi(x)|^{a}_{0}+i\hbar\int_{0}^{a}dx (\phi'(x))^{\ast}\psi(x)=$$
$$=\underbrace{-i\hbar \phi^{\ast}(x)\psi(x)|_{0}^{a}}\limits_{0}+\int_{0}^{a}dx(-i\hbar\partial_{x}\phi(x))^{\ast}\psi(x)=^{?}\langle \hat{p}^{\dagger}\phi|\psi\rangle$$
dove il termine calcolato agli estremi si annulla. Per essere vero, oltre che soddisfare l'equazione agli autovalori di $\hat{p}$ deve anche soddisfare le condizioni al contorno. Si trova che non vengono soddisfatte, quindi $\hat{p}$ non è autoaggiunto. Il suo quadrato, $\hat{p}^{2}$, invece si.



Per una buca infinita simmetrica tra $[-a,a]$ abbiamo
$$p_{n}=\frac{\hbar \pi}{2a},\qquad E_{n}=\frac{\hbar^{2}\pi^{2}n^{2}}{8a^{2}m}$$
e gli autostati
$$\psi_{n}(x)=A_{n}(e^{ip_{n}x/\hbar}-e^{-ip_{n}x/\hbar}e^{-2ip_{n}a/\hbar})$$
con $\psi_{n}\in L^{2}([-a,a],dx)$. Sviluppiamo $\psi_{n}$:
$$\psi_{n}(x)=A_{n}e^{-ip_{n}a/\hbar}(\ldots)$$
Divido per autostati pari e dispari:
$$\begin{align}
\psi_{n=2l}(x)&=\tilde{A}_{2l}\sin\left( \frac{\pi}{2a}2lx+\pi l \right)=\tilde{A}_{2l}(-1)^{l}\sin\left( \frac{\pi}{la}x \right)=\tilde{\tilde{A}}_{2l}\sin\left( \frac{l\pi}{a}x \right) \\
\psi_{n=2l+1}(x)&=\tilde{A}_{2l+1}\sin\left( \frac{\pi}{2a}(2l+1)x+\pi l+ \frac{\pi}{2} \right)=\tilde{\tilde{A}}_{2l+1}\cos\left( \frac{\pi}{2a}(2l+1)x \right)
\end{align}$$
e combinandole
$$\psi_{n}(x)=2A_{n}\sin\left( \frac{\psi n}{2a}x+ \frac{\pi}{2}n \right)$$
Troviamo la costante di normalizzazione
$$1=\int_{-a}^{a}\lvert \psi_{n}(x) \rvert ^{2}\ dx=4\lvert A_{n} \rvert ^{2}=\int_{-a}^{a}\sin ^{2}\left( \frac{\pi n}{2a}x+ \frac{\pi}{2}n \right)\ dx=\ldots$$
Posso fare la sostituzione
$$y=\frac{\pi n}{2a}+ \frac{\pi}{2}n,\qquad y(+a)=\frac{\pi n}{2}+ \frac{\pi}{2}n=\pi n,\qquad dy=\frac{\pi n}{2a}dx$$
per trovare l'integrale
$$\ldots=4\lvert A_{n} \rvert ^{2}\int_{0}^{\pi n} \frac{2a}{\pi n}\sin ^{2}y\ dy=4a\lvert A_{n} \rvert ^{2}\quad\Rightarrow \quad \lvert A_{n} \rvert ^{2}=\frac{1}{2\sqrt{ a }}$$
e quindi
$$\psi_{n}(x)=\frac{1}{\sqrt{ a }}\sin\left( \frac{\psi n}{2a}x+ \frac{\pi}{2}n \right)$$

Consideriamo l'[[operatore di parità]] e applichiamolo alla funzione d'onda dell'[[Hamiltoniana]]:
$$(\hat{H}\hat{\pi}\psi)(x)=- \frac{\hbar^{2}}{2m}(\hat{\pi}\psi)''(x)=- \frac{\hbar^{2}}{2m}\psi''(-x)$$
Dato che Hamiltoniana e parità sono operatori, è utile sapere se commutano:
$$(\hat{\pi}\hat{H}\psi)(x)=(\hat{H}\psi)(-x)=- \frac{\hbar^{2}}{2m}\psi''(-x)$$
quindi commutano: $[\hat{\pi},\hat{H}]=0$. So per il [[teorema di Noether]] che la commutatività con $\hat{H}$ può comportare una degenerazione. Per vedere cosa succede, considero l'$n$-esimo autostato
$$(\hat{\pi}\psi_{n})(x)=\psi_{n}(-x)=\sin\left( - \frac{\pi}{2a}x+ \frac{\pi}{2}n \right)$$
Per gli autostati pari
$$(\hat{\pi}\psi_{2l})(x)=\frac{1}{\sqrt{ a }}(-1)^{l+1}\sin\left( \frac{l\pi}{a}x \right)$$
Dato che cambia solo per una fase rispetto a $\ket{\psi_{2l}}$, gli stati rappresentano la stessa situazione e quindi non c'è degenerazione. Per gli autostati dispari vale lo stesso, quindi $\ket{\psi_{n}}$ in generale non è degenere a causa di $\hat{\pi}$.


[^1]: È interessante notare come la quantizzazione dell'energia è nata da un obbligo matematico (le condizioni al contorno), non uno fisico.