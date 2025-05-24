---
wiki-publish: true
---
L'**oscillatore armonico quantistico** è l'analogo quantistico dell'[[Harmonic oscillator]] classico, ossia un sistema quantistico con un [[punto di equilibrio]] soggetto ad una forza di ritorno $F$ una volta perturbato.
### Soluzione
Il caso dell'oscillatore armonico consiste nel risolvere l'[[equazione di Schrödinger]] per una [[particella]] immersa nel [[Potential]]
$$V(x)=\frac{1}{2}m\omega^{2}x^{2}$$
Partiamo dunque dall'equazione indipendente dal tempo, che prende la forma
$$- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}}+ \frac{1}{2}m\omega^{2}x^{2}\psi=E\psi\tag{1}$$
Esistono due modi comuni per risolvere questa equazione: un modo semplice e "di forza bruta" che sfrutta le [[serie di potenze]] e un metodo algebrico che sfrutta gli operatori di creazione e distruzione.
#### Metodo algebrico
Riscriviamo la $(1)$ in un modo più comodo, usando l'[[operatore]] di quantità di moto $p\equiv (\hbar/i)d/dx$:
$$\frac{1}{2m}[p^{2}+(m\omega x)^{2}]\psi=E\psi$$
da cui otteniamo la nota [[Hamiltoniana]] dell'oscillatore armonico
$$H=\frac{1}{2m}[p^{2}+(m\omega x)^{2}]$$
L'idea è fattorizzare l'Hamiltoniana usando
$$z^{2}+w^{2}=(iz+w)(-iz+w)$$
ma bisogna fare particolare attenzione, dato che $x$ e $p$ *non* sono numeri, bensì operatori, e perché la precedente equazione sia vera bisogna che valga la commutatività. Per il prodotto tra scalari è garantita, ma per due operatori in genere no, nel senso che non sempre $xp\neq px$. Detto ciò, possiamo comunque analizzare le seguenti quantità
$$a_{\pm}\equiv \frac{1}{\sqrt{2\hbar m\omega}}(\mp ip+m\omega x)$$
Il fattore di scala iniziale è solo per comodità. Controlliamo il prodotto $a_{-}a_{+}$:
$$a_{-}a_{+}=\frac{1}{2\hbar m \omega}(-ip+m\omega x)(ip+m\omega x)=\frac{1}{2\hbar m\omega}[p^{2}+(m\omega x)^{2}-im\omega(xp-px)]$$
dove ritroviamo il [[Commutator]] di $x$ e $p$ al terzo termine nelle parentesi. Estraendo l'ultimo termine e esplicitando il commutatore otteniamo
$$a_{-}a_{+}=\frac{1}{2\hbar m\omega}[p^{2}+(m\omega x)^{2}] - \frac{i}{2\hbar}[x,p]\tag{2}$$
Calcoliamo allora il commutatore tra $x$ e $p$, aggiungendo una funzione di test dato che sono operatori:
$$[x,p]\varphi(x)=\left[x \frac{\hbar}{i} \frac{d\varphi}{dx}- \frac{\hbar}{i} \frac{d}{dx} (x\varphi)\right]=\frac{\hbar}{i}\left(x \frac{d\varphi}{dx}-x \frac{d\varphi}{dx}-\varphi\right)=i\hbar\varphi$$
da cui si trova la relazione commutativa canonica
$$\boxed{[x,p]=i\hbar}$$
Tornando alla $(2)$, abbiamo
$$a_{-}a_{+}=\frac{1}{\hbar \omega}H+ \frac{1}{2}$$
Riconoscendo che $[a_{-},a_{+}]=1$, possiamo esprimere l'Hamiltoniana come
$$H=\hbar\omega\left(a_{-}a_{+}- \frac{1}{2}\right)$$
Possiamo rifare lo stesso percorso usando $a_{+}a_{-}$ anziché $a_{-}a_{+}$ e troviamo
$$a_{+}a_{-}=\frac{1}{\hbar \omega}H- \frac{1}{2}$$
Riconoscendo che $[a_{+},a_{-}]=1$, possiamo esprimere l'Hamiltoniana come
$$\boxed{H=\hbar\omega\left(a_{+}a_{-}+ \frac{1}{2}\right)}$$
che possiamo sostituire nell'equazione di Schrödinger
$$\hbar\omega\left(a_{\pm}a_{\mp}\pm \frac{1}{2}\right)\psi=E\psi\tag{3}$$
Si dimostra[^1] che se $\psi$ soddisfa l'equazione di Schrödinger per l'energia $E$, allora $(a_{+}\psi)$ soddisfa l'equazione per energia $E+\hbar\omega$. Allo stesso modo, $(a_{-}\psi)$ soddisfa l'equazione per $E-\hbar\omega$. Gli operatori $a_{\pm}$ sono detti [[operatori di creazione e distruzione|operatori scaletta]] e permettono di aumentare e diminuire lo stato di energia.

Applicando a catena l'operatore di discesa si arriva eventualmente ad una soluzione non normalizzabile: questa non è altro che lo stato fondamentale del sistema. Per questa, vale $a_{-}\psi_{0}=0$. Da qui in poi, l'operatore di discesa smette di darci nuove soluzioni, dato che $a_{-}(0)=0$. Possiamo così determinare la funzione d'onda (spaziale) dello stato fondamentale:
$$\frac{1}{\sqrt{2\hbar m\omega}}\left(\hbar \frac{d}{dx}+m\omega x\right)\psi_{0}=0\quad \rightarrow \quad \frac{d\psi_{0}}{dx}=- \frac{m\omega}{\hbar} x\psi_{0}$$
L'equazione differenziale è facilmente risolvibile per quadratura:
$$\int \frac{d\psi_{0}}{\psi_{0}}=- \frac{m\omega}{\hbar}\int xdx \quad\rightarrow \quad\ln\psi_{0}=- \frac{m\omega}{2\hbar} x^{2}+K$$
con $K$ una costante. Allora
$$\psi_{0}(x)=Ae^{-(m\omega/2\hbar) x^{2}}$$
con $A$ la costante di normalizzazione (che ha assorbito $K$). Possiamo trovare $A$ velocemente
$$1=|A|^{2}\int_{-\infty}^{+\infty} e^{-m\omega x^{2}/\hbar}dx=|A|^{2}\sqrt{\frac{\pi\hbar}{m\omega}} \quad\rightarrow\quad A=\left(\frac{m\omega}{\pi\hbar}\right)^{1/4}$$
quindi la funzione d'onda spaziale dello stato fondamentale è
$$\boxed{\psi_{0}(x)=\left(\frac{m\omega}{2\hbar}\right)^{1/4}e^{-(m\omega/2\hbar)x^{2}}}$$
Possiamo determinarne l'energia sostituendola nell'equazione di Schrödinger $(3)$:
$$\hbar\omega\left(a_{\pm}a_{\mp}\pm \frac{1}{2}\right)\psi_{0}=E_{0}\psi_{0} \quad \rightarrow \quad E_{0}=\frac{1}{2}\hbar \omega$$
(sfruttando che $a_{-}\psi_{0}=0$). Ora che abbiamo una base, trovare gli altri stati è banale: basta applicare l'operatore di salita a catena per trovare l'$n$-esimo stato eccitato, aumentando l'energia di $\hbar\omega$ ogni salto. Abbiamo quindi trovato due cose: l'equazione d'onda spaziale di tutti gli stati dell'oscillatore armonico quantistico e tutte le energie permesse a loro associate:
$$\psi_{n}(x)=A_{n}(a_{+})^{n}\psi_{0}(x)\quad\text{con}\quad E_{n}=\left(n+ \frac{1}{2}\right)\hbar\omega$$
con $A_{n}$ la costante di normalizzazione dell'$n$-esimo stato.

In realtà è anche possibile derivare le costanti $A_{n}$ algebricamente, usando gli operatori scaletta. Consideriamo il fatto che i due operatori scaletta sono l'[[Operatore aggiunto|aggiunto]] l'un dell'altro, quindi $(\psi,a_{\pm}\varphi,a_{\mp}\psi,\varphi)$, usando il [[Scalar product|prodotto hermitiano]] $\langle \cdot|\cdot\rangle$. Sappiamo che $a_{\pm}\psi_{n}$ è proporzionale a $\psi_{n+1}$ tramite le relazioni
$$a_{+}\psi_{n}=c_{n}\psi_{n+1}, \quad a_{-}\psi_{n}=d_{n}\psi_{n-1}\tag{4}$$
Vogliamo conoscere le costanti $c_{n}$ e $d_{n}$. Vale
$$\langle a_{\pm}\psi_{n}|a_{\pm}\psi_{n}\rangle=\langle a_{\mp}a_{\pm}\psi_{n}|\psi_{n}\rangle$$
Ma sappiamo che $a_{+}a_{-}\psi_{n}=n\psi_{n}$ e $a_{-}a_{+}\psi_{n}=(n+1)\psi_{n}$, da cui
$$\langle a_{+}a_{-}\psi_{n}|\psi_{n}\rangle=\langle n\psi_{n}|\psi_{n}\rangle=n\int_{-\infty}^{+\infty}|\psi_{n}|^{2}dx$$
$$\langle a_{-}a_{+}\psi_{n}|\psi_{n}\rangle=\langle(n+1)\psi_{n}|\psi_{n}\rangle=(n+1)\int_{-\infty}^{+\infty}|\psi_{n}|^{2}dx$$
Ma le $\psi_{n}$ sono normalizzate, quindi $n+1=|c_{n}|^{2}$ e $n=|d_{n}|^{2}$. Mettendole nella $(4)$, si ha
$$\boxed{a_{+}\psi_{n}=\sqrt{n+1}\psi_{n+1},\quad a_{-}\psi_{n}=\sqrt{n}\psi_{n-1}}$$
da cui la forma definitiva del $n$-esimo stato dell'oscillatore armonico quantistico:
$$\boxed{\psi_{n}=\frac{1}{\sqrt{n!}}(a_{+})^{n}\psi_{0}=\frac{1}{\sqrt{n!}}(a_{+})^{n}\left(\frac{m\omega}{\pi\hbar}\right)^{1/4}e^{-(m\omega/2\hbar)x^{2}}\quad\text{con}\quad E_{n}=\left(n+ \frac{1}{2}\right)\hbar\omega}$$

L'energia potenziale media è[^2]
$$\left\langle V \right\rangle=\left\langle \frac{1}{2}m\omega^{2}x^{2} \right\rangle=\frac{1}{2}m\omega^{2} \left\langle x^{2} \right\rangle=\ldots=\frac{1}{2}\hbar\omega\left(n+ \frac{1}{2}\right)$$
cioè esattamente metà dell'energia totale, come nel caso classico.
#### Risultati
Le $\psi_{n}$ così trovate sono curiosamente diverse dalle soluzioni del moto classico: da una parte, abbiamo che l'energia è quantizzata; dall'altra, notiamo fenomeni che né si osservano né si spiegano in meccanica classica, come il fatto che la probabilità che la particella si trovi al di fuori dell'ampiezza (classica) dell'oscillatore *non* è zero e che la probabilità di trovarsi al centro dell'oscillatore negli stati dispari è *sempre* 0.

Si può inoltre definire uno [[stato coerente]] come l'unico autostato $|\alpha\rangle$ dell'operatore di distruzione
$$a_{-}|z\rangle=\alpha |z\rangle$$
con il suo autovalore associato $\alpha$. Questo stato è quello con la dinamica più simile a quella dell'oscillatore armonico classico ed è un esempio del principio di corrispondenza.

Si nota anche che per stati di energia sufficientemente alti ($n\gg1$), la probabilità di osservare la particella in una data posizione è approssimativamente uguale quella classica, se si prende la media.

:::image
![[Stati stazionari oscillatore armonico quantistico.png]]
*Fonte: Introduction to Quantum Mechanics di Griffiths*
:::
### Soluzione alternativa
L'[[Hamiltoniana]] di un oscillatore armonico quantistico è
$$\hat{H}=\frac{\hat{p}^{2}}{2m}+ \frac{m\omega ^{2}}{2}\hat{q}^{2}$$
L'equazione che vogliamo risolvere, indipendente dal tempo è
$$\hat{H}\ket{\psi_{E}} =E\ket{\psi_{E}} $$
dove gli stati $\ket{\psi_{E}}$ sono [[Stati in meccanica quantistica|stati legati]] ad [[energy|energia]] $E$. L'[[equazione di Schrödinger]] completa in [[Rappresentazioni dello stato|rappresentazione della posizione]] allora è
$$- \frac{\hbar^{2}}{2m}\psi''_{E}(x)+ \frac{m\omega ^{2}}{2}x^{2}\psi_{E}(x)=E\psi_{E}(x)$$
Risolvere questa equazione diventa molto più gestibile introducendo gli [[operatori di creazione e distruzione]] $\hat{a}$ e $\hat{a}^{+}$. Usando l'algebra degli [[Operatore|operatori]] ed in particolare quella dei [[Commutator|commutatori]], è possibile trovare $\psi_{E}$ senza nemmeno risolvere un'equazione differenziale. Per definizione, gli operatori sono
$$\hat{a}=\alpha \hat{q}+i\beta \hat{p},\qquad \alpha,\beta \in \mathbb{R}$$
Le due costanti sono
$$\alpha=\sqrt{ \frac{m\omega}{2\hbar} },\qquad \beta=\frac{1}{\sqrt{ 2m\omega \hbar }}$$
quindi l'operatore di distruzione $\hat{a}$ e il suo [[Operatore aggiunto|aggiunto]] l'operatore di creazione sono
$$\boxed{\hat{a}=\sqrt{ \frac{m\omega}{2\hbar} }\hat{q}+i \frac{1}{\sqrt{ 2m\omega \hbar }}\hat{p},\qquad \hat{a}^{+}=\sqrt{ \frac{m\omega}{2\hbar} }\hat{q}-i \frac{1}{\sqrt{ 2m\omega \hbar }}\hat{p}}$$
I due non commutano:
$$[\hat{a},\hat{a}^{+}]=\left[ \sqrt{ \frac{m\omega}{2\hbar} }\hat{q}+ \frac{i}{\sqrt{ 2m\omega \hbar }}\hat{p},\sqrt{ \frac{m\omega}{2\hbar} }- \frac{i}{\sqrt{ 2m\omega \hbar }}\hat{p} \right]=\ldots$$
Sfruttiamo le proprietà dei commutatori $[\hat{A}+\hat{B},\hat{C}]=[\hat{A},\hat{C}]+[\hat{B},\hat{C}]$ e $[\hat{A}\hat{B},\hat{C}]=\hat{A}\hat{B}\hat{C}-\hat{C}\hat{A}\hat{B}$:
$$\ldots=\sqrt{ \frac{m\omega}{2\hbar} } \frac{\sqrt{ \hbar }}{\sqrt{ 2m\omega \hbar }}+ \frac{\sqrt{ \hbar }}{\sqrt{ 2m\omega \hbar }}\sqrt{ \frac{m\omega}{2\hbar} }=\frac{1}{2}+ \frac{1}{2}=1$$
Quindi
$$[\hat{a},\hat{a}^{+}]=1$$
In particolare, possiamo chiamare $\hat{a}^{+}\hat{a}$ operatore numero, e notare che è un [[operatore semidefinito positivo]] dato che
$$\braket{ \psi |\hat{a}^{+}\hat{a}\psi  }=\braket{ \hat{a}\psi | \hat{a}\psi } =\lvert \hat{a}\psi \rvert ^{2} \geq0$$
Ciò significa che tutti gli autovalori di $\hat{a}^{+}\hat{a}$ sono positivi. L'espressione dell'operatore numero è
$$\hat{a}^{+}\hat{a}=\frac{m\omega}{2\hbar}\hat{q}^{2}+ \frac{1}{\sqrt{ 2m\omega \hbar }}\hat{p}^{2}- \frac{i}{2\hbar}\hat{q}\hat{p}+ \frac{i}{2\hbar}\hat{p}\hat{q}=\frac{\hat{p}^{2}}{2m\omega \hbar}+ \frac{m\omega}{2\hbar}\hat{q}^{2}- \frac{i}{2\hbar}[\hat{q},\hat{p}]$$
Sappiamo $[\hat{q},\hat{p}]=i\hbar$ quindi
$$\boxed{\hat{a}^{+}\hat{a}=\frac{\hat{p}^{2}}{2m\omega \hbar}+ \frac{m\omega}{2\hbar}\hat{q}^{2}- \frac{1}{2}}$$
Ma questa espressione è molto simile a quella dell'Hamiltoniana. Infatti, se la sostituiamo in essa troviamo
$$\boxed{\hat{H}=\hbar\omega\left(\hat{a}^{+}\hat{a}+ \frac{1}{2}\right)}$$
L'operatore numero agisce su un autostato $\ket{\lambda}$ di autovalore $\lambda$ come
$$\hat{a}^{+}\hat{a}\ket{\lambda} =\lambda \ket{\lambda} $$
quindi l'Hamiltoniana su un autostato è
$$\hat{H}\ket{\lambda} =\hbar \omega \hat{a}^{+}\hat{a}\ket{\lambda} + \frac{\hbar \omega}{2}\ket{\lambda} =\hbar \omega \left( \lambda+ \frac{1}{2} \right)\ket{\lambda}  $$
La cosa comoda è che ora per trovare gli autostati di $\hat{H}$, ossia il suo [[Spettro]], basta trovare lo spettro dell'operatore numero. Ora bisogna capire cosa sono $\lambda$ e $\ket{\lambda}$. Intanto, vediamo un po' di algebra di commutatori. Naturalmente vale
$$[\hat{a},\hat{a}^{n}]=0,\qquad [\hat{a}^{+},(\hat{a}^{+})^{n}]=0$$
Ma è interessante
$$[\hat{a},(\hat{a}^{+})^{n}]=[\hat{a},\hat{a}^{+}(\hat{a}^+)^{n-1}]=\ldots$$
Usiamo la proprietà
$$[\hat{A},\hat{B}\hat{C}]=\hat{C}\hat{A}\hat{B}-\hat{A}\hat{B}\hat{C}$$
Quindi
$$\ldots=\hat{a}^{+}[\hat{a},(\hat{a}^{+})^{n-1}]+(\hat{a}^{+})^{n-1}\underbrace{ [\hat{a},\hat{a}^{+}] }_{ 1 }=\hat{a}^{+}[\hat{a},\hat{a}^{+}(\hat{a}^{+})^{n-2}]+(\hat{a}^{+})^{n-1}=\ldots$$
Adesso posso iterare questo procedimento $n$ volte per ottenere
$$\boxed{[\hat{a},(\hat{a}^{+})^{n}]=n(\hat{a}^{+})^{n-1}}$$
Non per altro, $\hat{a}$ si chiama operatore di distruzione perché diminuisce la potenza di uno. Per l'inverso possiamo sfruttare quello che abbiamo già trovato prendendo l'aggiunto del commutatore
$$[\hat{a}^{+},(\hat{a})^{n}]=-[\hat{a},(\hat{a}^{+})^{n}]^{+}=-n((\hat{a}^{+})^{n-1})^{+}$$
Qui possiamo sfruttare le proprietà dell'aggiunto per ottenere
$$\boxed{[\hat{a}^{+},(\hat{a})^{n}]=-n \hat{a}^{n-1}}$$
Queste sono valide per ogni $n$ naturale. Altri commutatori utili sono
$$\boxed{[\hat{a}^{+}\hat{a},\hat{a}]=-\hat{a},\qquad[\hat{a}^{+}\hat{a},\hat{a}^{+}]=\hat{a}^{+}}$$
che legano l'operatore numero con gli operatori di creazione e distruzione.

Vediamo dunque qualche azione dell'operatore numero su autostati, sfruttando quanto appena trovato. Partiamo da
$$\hat{a}^{+}\hat{a}\hat{a}\ket{\lambda} =[\hat{a}^{+}\hat{a},\hat{a}]\ket{\lambda} +\hat{a}\underbrace{ \hat{a}^{+}\hat{a}\ket{\lambda} }_{ \lambda \ket{\lambda}  } =-\hat{a}\ket{\lambda} +\lambda\hat{a}\ket{\lambda} =(\lambda-1)\hat{a}\ket{\lambda} $$
Vediamo anche
$$\hat{a}^{+}\hat{a}\hat{a}^{n}\ket{\lambda} =\hat{a}^{n}\underbrace{ \hat{a}^{+}\hat{a}\ket{\lambda} }_{ \lambda \ket{\lambda}  } +[\hat{a}^{+}\hat{a},\hat{a}^{n}]\ket{\lambda} =\lambda \hat{a}^{n}\ket{\lambda} -n \hat{a}^{n}\ket{\lambda} =(\lambda-n)\hat{a}^{n}\ket{\lambda} $$
Qui però sorge un problema. Sappiamo per definizione di semi-positività che tutti gli autovalori di $\hat{a}^{+}\hat{a}$ sono positivi. Ma per $n$ sufficientemente grandi l'autovalore $\lambda-n$ diventerà eventualmente negativo, quindi deve esistere una condizione su $\lambda-n$ tale per cui è sempre maggiore di zero. Questa condizione è che $\lambda \in \mathbb{N}$ (e quindi anche $\lambda-n\in \mathbb{N}$) e che $\hat{a}^{+}\hat{a}\ket{0}=0$, ossia ci sia un limite inferiore all'azione dell'operatore numero. Sapendo questo, possiamo riscrivere l'azione di $\hat{a}^{+}\hat{a}$ come
$$\boxed{\hat{a}^{+}\hat{a}\ket{n} =n\ket{n} }$$
da cui si può vedere che l'operatore numero si chiama così perché i suoi autovalori sono tutti i numeri naturali. Ora vorremo anche capire l'azione di $\hat{a}$ e $\hat{a}^{+}$ sugli autostati. Intanto sappiamo
$$\hat{a}^{+}\hat{a}\hat{a}\ket{n} =(n-1)\hat{a}\ket{n} $$
Vogliamo vedere se $\hat{a}\ket{n}\propto \ket{n-1}$. Se questo è vero, allora posso applicare $\hat{a}$ a catena fino a che non raggiungo $\ket{0}$, pesato per qualche costante. (TODO: Rivedi lezione 07/11/2024 circa 15-20 minuti seconda parte).

$$\hat{a}^{+}\hat{a}\hat{a}^{+}\ket{n}=\hat{a}^{+}\hat{a}^{+}\hat{a}\ket{n}+[\hat{a}^{+}\hat{a},\hat{a}]\ket{n} =n \hat{a}^{+}\ket{n} +\hat{a}^{+}\ket{n} =(n+1)\hat{a}^{+}\ket{n} $$
Abbiamo/vogliamo che $\hat{a}^{+}\ket{n}\propto \ket{n+1}$. Quindi con consecutive applicazione di $\hat{a}^{+}$ su $\ket{0}$ possiamo alzare l'autostato a qualunque $\ket{n}$. Controlliamo dunque la [[Norma]] di questo valore
$$\lvert \ket{(\hat{a}^{+})^{n}0}  \rvert ^{2}=\braket{ (\hat{a}^{+})^{n}0 | (\hat{a}^{+})^{n}0 } =\braket{ 0 | \hat{a}^{n}(\hat{a}^{+})^{n}0 }=\ldots$$
Per districare questa equazione vogliamo sfruttare il fatto che $\ket{0}$ è annichilito da $\hat{a}$, quindi idealmente vogliamo trovare un modo per spostare almeno un $\hat{a}$ da sinistra dei $(\hat{a}^{+})^{n}$ a destra, in modo che possa essere applicato a $\ket{0}$ e che quindi cancelli tutto. Allora
$$\ldots=\braket{ 0 | \hat{a}^{n-1}\hat{a}(\hat{a}^{+})^{n}0 }=\cancel{ \braket{ 0 | \hat{a}^{n-1}(\hat{a}^{+})^{n}\hat{a} |0 } } +\braket{ 0 | \hat{a}^{n-1}[\hat{a},(\hat{a}^{+})^{n}]|0 } = n\braket{ 0 | \hat{a}^{n-1}(\hat{a}^{+})^{n-1}|0 } =\ldots$$
Posso ripetere la cancellazione $n$ volte per ottenere
$$\ldots=n!$$
Quindi da questo possiamo concludere che l'$n$-esima azione di $\hat{a}^{+}$ su $\ket{0}$ è
$$(\hat{a}^{+})^{n}\ket{0} =\sqrt{ n! }\ket{n}$$
Possiamo invertire questa forma per trovare una formula per gli autostati dell'oscillatore armonico in funzione di $\ket{0}$:
$$\boxed{\ket{n} =\frac{(\hat{a}^{+})^{n}\ket{0}}{\sqrt{ n! }}}\tag{1}$$
per ogni $n\in \mathbb{N}$. Dobbiamo però dimostrare che siano tutti [[Orthonormality|ortonormali]]. Allora presi $n\neq m\in \mathbb{N}$ vogliamo l'ortogonalità
$$\braket{ n | m } =\frac{\braket{ 0 | \hat{a}^{n}(\hat{a}^{+})^{m}|0 }}{\sqrt{ n!m! }} =0$$
Questo è vero, infatti per iterazione abbiamo
$$\braket{ 0 | \hat{a}^{n-1} \hat{a}(\hat{a}^{+})^{m}|0}=\braket{ 0 | \hat{a}^{n-1}[\hat{a},(\hat{a}^{+})^{m}]|0 } =m\braket{ 0 | \hat{a}^{n-1}(\hat{a}^{+})^{m-1}|0 }  $$
Ora, supponiamo che $n>m$. Dato che $n$ e $m$ diminuiscono in unisono, quando $m$ arriva a zero, sarà rimasto almeno un $\hat{a}$ davanti al $\ket{0}$, quindi va tutto a zero. Se invece $n<m$ rimarrà almeno un $\hat{a}^{+}$, che possiamo spostare dall'altra parte del prodotto scalare per comunque trovare un $\hat{a}$ che agisce su $\ket{0}$, di nuovo annullando tutto. L'unico caso con risultato non nullo è quello in cui $n=m$, in qual caso rimane $\braket{ 0 | 0 }=1$. Ma questa non è altro che una [[Kronecker delta]], quindi $\braket{ n | m }=\delta_{nm}$, che prova l'ortonormalità. Questo prova definitivamente che $\{ \ket{n} \}_{n\in \mathbb{N}}$ è la [[base]] ortonormale degli autostati dell'oscillatore armonico, ed è equivalente all'insieme dei modi di oscillazione normale del [[Harmonic oscillator|caso classico]].

Ora che sappiamo la statica del sistema, vogliamo trovarne l'evoluzione temporale. Preso l'[[evolutore]] $\hat{U}_{t}=e^{-i \hat{H}t/\hbar}$. Avendo la base degli autostati, un generico stato $\ket{\psi_{t}}$ è rappresentato in [[Serie di Fourier]] da
$$\ket{\psi_{t}} =\hat{U}_{t}\ket{\psi} =\sum_{n=0}^{\infty} \braket{ n | \psi } \hat{U}_{t}\ket{n} =\sum_{n=0}^{\infty} \braket{ n | \psi } e^{-it\hbar \omega(n+ 1/2)/\hbar}\ket{n} $$
Ci interessa la [[Rappresentazioni dello stato|rappresentazione della posizione]] $\psi_{n}(x)=\braket{ x | n }$. (TODO: Rivedi lezione 07/11/24 verso la fine). Lo stato fondamentale è
$$\boxed{\psi_{0}(x)=\sqrt[4]{ \frac{m\omega}{\hbar \pi} }e^{-(m\omega/2\hbar)x^{2}}}$$
La forma degli autostati in posizione può essere derivata in alcuni modo. In unità naturali di lunghezza ed energia, sono dati dai [[polinomi di Hermite]]. Si possono derivare dalla soluzione in serie dell'oscillatore armonico. Si possono anche ottenere dagli operatori di creazione e distruzione. Il primo stato eccitato si trova essere
$$\boxed{\psi_{1}(x)=\sqrt[4]{ \frac{m\omega}{\hbar \pi} }\sqrt{ \frac{2m\omega}{\hbar} }xe^{-(m\omega/2\hbar)x^{2}}}$$

> [!example] Con operatori di creazione e distruzione
> Ci interessa $\psi_{1}(x)=\braket{ x | 1 }$. Allora
> $$\begin{align}
> \braket{ x | 1 }&=\braket{ x | \hat{a}^{+} | 0 } \\
> &=\bra{x} \left( \sqrt{ \frac{m\omega}{2\hbar} }\hat{q}-i \frac{\hat{p}}{\sqrt{ 2m\omega \hbar }} \right)\ket{0} \\
> &=\sqrt{ \frac{m\omega}{2\hbar} }x\psi_{0}(x)-\sqrt{ \frac{\hbar}{2m\omega} } \partial_{x}  \psi_{0}(x) \\
> &=\sqrt{ \frac{m\omega}{2\hbar} }x\sqrt[4]{ \frac{m\omega}{\hbar \pi } }e^{-(m\omega/2\hbar)x^{2}}+\sqrt{ \frac{m\omega}{2\hbar} }\sqrt[4]{ \frac{m\omega}{\hbar \pi} }xe^{-(m\omega/2\hbar)x^{2}}= \\
> &=\sqrt{ \frac{2m\omega}{\hbar} }\sqrt[4]{ \frac{m\omega}{\hbar \pi} }xe^{-(m\omega/2\hbar)x^{2}}
> \end{align} $$

#### Azione di $\hat{a}$ e $\hat{a}^{+}$
Ora che sappiamo la forma degli autostati $(1)$, possiamo vedere quale sia l'azione di $\hat{a}$ e $\hat{a}^{+}$ su di loro. Partiamo da $\hat{a}$:
$$\hat{a}\ket{n} =\hat{a} \frac{(\hat{a}^{+})^{n}}{\sqrt{ n! }}\ket{0} =\frac{(\hat{a}^{+})^{n}\hat{a}\ket{0}}{\sqrt{ n! }}+ \frac{1}{\sqrt{ n! }}\underbrace{ [\hat{a},(\hat{a}^{+})^{n}] }_{ n(\hat{a}^{+})^{n-1} }\ket{0}=\ldots $$
usando che $\hat{a}$ e $\hat{a}^{+}$ non commutano. Ora
$$\ldots=\frac{n}{\sqrt{ n! }}(\hat{a}^{+})^{n-1}\ket{0} =\sqrt{ n } \frac{(\hat{a}^{+})^{n-1}}{\sqrt{ (n-1)! }}\ket{0}=\sqrt{ n }\ket{n-1}  $$
Ora guardiamo $\hat{a}^{+}$:
$$\hat{a}^{+}\ket{n} =\hat{a}^{+} \frac{(\hat{a}^{+})^{n}}{\sqrt{ n! }}\ket{0} =\frac{(\hat{a}^{+})^{n+1}}{\sqrt{ n! }}\ket{0} =\sqrt{ n+1 }\ket{n+1} $$
Quindi in conclusione abbiamo
$$\boxed{\hat{a}\ket{n} =\sqrt{ n }\ket{n-1} ,\qquad \hat{a}^{+}\ket{n} =\sqrt{ n+1 }\ket{n+1}}$$
Troviamo anche i valori medi negli autostati:
$$\braket{ m | \hat{a} | n } =\sqrt{ n }\braket{ m | n-1 } =\sqrt{ n }\delta_{m,n-1},\qquad \braket{ m | \hat{a}^{+} | n } =\sqrt{ n+1 }\braket{ m | n+1 } =\sqrt{ n+1 }\delta_{m,n+1}$$
con $\delta$ la [[Kronecker delta]].
#### Evoluzione temporale
Dato che conosciamo l'evoluzione temporale di $\hat{a}$ e $\hat{a}^{+}$ e che possiamo esprimere posizione e momento dell'oscillatore rispetto a questi due, possiamo anche trovare la loro evoluzione temporale. Infatti, dato che
$$\hat{q}=\sqrt{\frac{\hbar}{2m\omega}}(\hat{a}^{+}+\hat{a}),\quad \hat{p}=i\sqrt{\frac{\hbar m\omega}{2}}(\hat{a}^{+}-\hat{a})$$
Abbiamo dunque
$$\hat{q}_{t}=\hat{U}_{t}^{+}\hat{q}\hat{U}_{t}=\sqrt{ \frac{\hbar}{2m\omega} }(e^{-i\omega t}\hat{a}+e^{i\omega t}\hat{a}^{+})$$
$$\hat{p}_{t}=\hat{U}_{t}\hat{p}\hat{U}_{t}=-i\sqrt{ \frac{m\omega \hbar}{2} }(e^{-i\omega t}\hat{a}-e^{i\omega t}\hat{a}^{+})$$
Idealmente vorremmo togliere completamente $\hat{a}$ e $\hat{a}^{+}$ e esprimere tutto in funzione di $\hat{q}$ e $\hat{p}$. Ma sappiamo esprimere $\hat{a}$ e $\hat{a}^{+}$ in termini di $\hat{q}$ e $\hat{p}$ quindi sostituiamo
$$\begin{align}
\hat{q}_{t}&=\sqrt{ \frac{\hbar}{2m\omega} }\left[ \left( \sqrt{ \frac{m\omega}{2\hbar} } \hat{q}+ \frac{i}{\sqrt{ 2m\omega \hbar }}\hat{p} \right) e^{-i\omega t}+\left( \sqrt{ \frac{m\omega}{2\hbar} }- \frac{i}{\sqrt{ 2m\omega \hbar }} \right)e^{i\omega t} \right] \\
&=\frac{1}{2}\hat{q}e^{-i\omega t}+ \frac{i}{2m\omega}\hat{p}e^{-i\omega t}+ \frac{1}{2}\hat{q}e^{i\omega t}- \frac{i}{2m\omega}\hat{p}e^{i\omega t} \\
&=\hat{q}\cos(\omega t)+ \frac{\hat{p}}{m\omega}\sin(\omega t)
\end{align}$$
e $\hat{p}$ analogamente (intuibile dal fatto che questo sono identiche alle soluzioni classiche)
$$\begin{align}
\hat{p}_{t}&=\hat{p}\cos(\omega t)-m\omega \hat{q}\sin(\omega t)
\end{align}$$
Allora in un oscillatore armonico quantistico, posizione e momento evolvono come
$$\boxed{\hat{q}_{t}=\hat{q}\cos(\omega t)+ \frac{\hat{p}}{m\omega}\sin(\omega t),\qquad \hat{p}_{t}=\hat{p}\cos(\omega t)-m\omega \hat{q}\sin(\omega t)}$$
Ora possiamo anche risolvere l'[[equazione di Heisenberg]] per entrambe
$$\frac{d}{dt}\hat{q}_{t}=\frac{i}{\hbar}[\hat{H},\hat{q}_{t}]=\ldots=\frac{\hat{p}_{t}}{m}$$
$$\frac{d}{dt}\hat{p}_{t}=\frac{i}{\hbar}[\hat{H},\hat{p}_{t}]=\frac{i}{\hbar}\hat{U}_{t}^{+}[\hat{H},\hat{p}]\hat{U}_{t}=\left[ \frac{\hat{p}^{2}}{2m}+ \frac{m\omega ^{2}}{2}\hat{q}^{2},\hat{p} \right]=\frac{m\omega ^{2}}{2}[\hat{p}^{2},\hat{q}]=m\omega ^{2}i\hbar \hat{q}$$
Allora abbiamo il sistema di equazioni differenziali operatoriali
$$\begin{cases}
\frac{d}{dt}\hat{q}_{t}=\frac{\hat{p}_{t}}{m} \\
\frac{d}{dt}\hat{p}_{t}=-m\omega ^{2}\hat{q}_{t}
\end{cases}$$
che sono identiche alle [[Hamilton equation|equazioni di Hamilton]] classiche. Questo è dovuto al fatto che $\hat{H}$ qui è quadratica sia in $\hat{q}$ che $\hat{p}$.
### Forza di Lorentz
Un'applicazione diretta dell'oscillatore armonico quantistico è per descrivere una [[particella]] [[Electric charge|elettricamente carica]] soggetta alla [[Lorentz force|forza di Lorentz]]. Questa può essere espressa come
$$m \frac{d\mathbf{v}}{dt}=\frac{q}{c}\mathbf{v}\times \mathbf{B}(\mathbf{r},t)+q\mathbf{E}(\mathbf{r},t)$$
Sfruttiamo l'[[Lagrange equation|equazione di Lagrange-Eulero]]
$$\frac{d}{dt}\frac{ \partial \mathcal{L} }{ \partial \mathbf{v} } =\frac{ \partial \mathcal{L} }{ \partial \mathbf{r} } $$
con $\mathcal{L}$ la [[Lagrangiana]] della particella. Ricordiamo le [[Maxwell's equations|equazioni di Maxwell]]:
$$\nabla\cdot\mathbf{B}=0,\qquad \nabla\times\mathbf{E}=- \frac{1}{c}\frac{ \partial \mathbf{B} }{ \partial t } $$
Usando il [[Magnetic vector potential|potenziale vettore]] $\mathbf{A}$ abbiamo anche $\nabla\times\mathbf{B}=\mathbf{A}$. Il [[Curl|rotore]] di $\mathbf{E}$ mediante il potenziale vettore è
$$\nabla\times\mathbf{E}=- \frac{1}{c}\frac{ \partial  }{ \partial t } \nabla\times\mathbf{A}=-\nabla\times\mathbf{\left( \frac{1}{c}\frac{ \partial \mathbf{A} }{ \partial t } \right) }$$
Dunque
$$\nabla\times\mathbf{\left( \mathbf{E}+ \frac{1}{c}\frac{ \partial \mathbf{A} }{ \partial t }  \right)}=0\quad\Rightarrow \quad \mathbf{E}+ \frac{1}{c}\frac{ \partial \mathbf{A} }{ \partial t } =-\nabla \Phi$$
dove $\Phi$ è un [[Electric potential|potenziale elettrico]]. Ricordando che, essendo potenziali, possiamo traslare $\Phi$ e $\mathbf{A}$ di una costante senza cambiare la fisica, possiamo esprimere la [[gauge freedom|libertà di gauge]] come
$$\begin{align}
\mathbf{A}\to \mathbf{A}+\nabla f,\quad &\mathbf{B}\to \mathbf{B} \\
\Phi\to \Phi- \frac{1}{c}\frac{ \partial f }{ \partial t } ,\quad &\mathbf{E}\to \mathbf{E}
\end{align}$$
dove $f$ è la funzione di gauge. Nel caso $\mathbf{E}=0$ e
$$\mathbf{B}=(0,0,B)=\nabla\times\mathbf{A}=(\partial_{y}A_{z}-\partial_{z}A_{y},\partial_{z} A_{x}-\partial_{x} A_{z},\partial_{x} A_{y}-\partial_{y} A_{x})$$
Allora $\mathbf{A}'=(0,B_{x},0)$ e $\mathbf{A}=\left( - \frac{B}{2}y, \frac{B}{2}x,0 \right)$. La funzione di gauge viene da
$$\begin{cases}
0=- \frac{B}{2}y+\partial_{x} f \\
B_{x}=\frac{B}{2}x+\partial_{y} f \\
0=0+\partial_{z} f
\end{cases}$$
Da cui $f(x,y)=\frac{B}{2}xy$.

Una volta ottenuta la Lagrangiana, possiamo trovare l'Hamiltoniana tramite una [[trasformata di Legendre]] secondo
$$H(\mathbf{r},\mathbf{p})=\mathbf{v}\cdot \mathbf{p}-\mathcal{L}(\mathbf{r},\mathbf{v})$$
Cerchiamo quindi la Lagrangiana. Sostituendo quanto trovato nella forza di Lorentz abbiamo
$$m \frac{d\mathbf{v}}{dt}=\frac{q}{c} \mathbf{v}\times\mathbf{A}- \frac{q}{c}\partial_{t} \mathbf{A}-q\nabla \Phi$$
Il primo termine è
$$m \frac{d\mathbf{v}}{dt}=\frac{d}{dt}\frac{ \partial  }{ \partial \mathbf{v} } \left( \frac{m\mathbf{v}^{2}}{2} \right)$$
quindi
$$\begin{align}
\frac{d}{dt}\frac{ \partial  }{ \partial \mathbf{v} } \left( \frac{m\mathbf{v}^{2}}{2} \right)&=\frac{q}{c}(v_{y}(\nabla\times\mathbf{A})_{z}-v_{z}(\nabla\times\mathbf{A})_{y})- \frac{q}{c}\partial_{t} A_{x}-q\partial_{x} \Phi \\
&=\frac{q}{c}(v_{y}\partial_{x} A_{y}-v_{y}\partial_{y}A_{x}-v_{z}\partial_{z}A_{x} +v_{z}\partial_{x} A_{z}-v_{x}\partial_{x}A_{x}+v_{x}\partial_{x} A_{x})- \frac{q}{c}\partial_{t} A_{x}-q \partial_{x} \Phi \\
&=\ldots
\end{align}$$
Il termine $v_{x}\partial_{x}A_{x}$ è stato aggiunto e rimosso per poter semplificare l'equazione
$$\begin{align}
\ldots&=\frac{q}{c}\mathbf{v}\cdot \partial_{x} \mathbf{A}-\left( \frac{q}{c}\mathbf{v}\cdot \nabla A_{x}+ \frac{q}{c}\partial_{t} A_{x} \right)-q\partial_{x} \Phi \\
&=\frac{q}{c}\partial_{x} (\mathbf{v}\cdot \mathbf{A})- \frac{q}{c} \frac{d}{dt}(\partial_{v_{x}}\mathbf{v} \cdot A)-q\partial_{x} \Phi
\end{align}$$
Allora
$$\frac{d}{dt}\partial_{v_{x}} \left( \frac{m\mathbf{v}^{2}}{2} + \frac{q}{c}\mathbf{v}\cdot \mathbf{A}-q\Phi \right)=\partial_{x} \left( \frac{q}{c}\mathbf{v}\cdot A- q\Phi + \frac{m\mathbf{v}^{2}}{2} \right)$$
e quindi
$$\boxed{\mathcal{L}(\mathbf{r,\mathbf{v},t})=\frac{m\mathbf{v}^{2}}{2}+ \frac{q}{c}\mathbf{v}\cdot \mathbf{A}(\mathbf{r},t)-q\Phi(\mathbf{r},t)}$$
Allora il momento è
$$\mathbf{p}=\frac{ \partial \mathcal{L} }{ \partial \mathbf{v} } =m\mathbf{v}+ \frac{q}{c}\mathbf{A}(\mathbf{r},t)$$

[^1]: Soddisfare l'equazione di Schrödinger significa che vale $H\psi=E\psi$, quindi vogliamo trovare $H(a_{+}\psi)=(E+\hbar\omega)\psi$. Difatti, si ha$$H(a_{+}\psi)=\hbar\omega\left(a_{+}a_{-}+ \frac{1}{2}\right)(a_{+}\psi)=\hbar\omega\left(a_{+}a_{-}a_{+}+ \frac{1}{2}a_{+}\right)\psi=\hbar\omega a_{+}\left(a_{-}a_{+}+ \frac{1}{2}\right)\psi=$$$$=a_{+}\left[\hbar\omega\left(\underbrace{a_{+}a_{-}+1}\limits_{*}+ \frac{1}{2}\right)\psi\right]=a_{+}(H+\hbar\omega)\psi=a_{+}(E+\hbar\omega)\psi=(E+\hbar\omega)(a_{+}\psi)$$dove in $*$ abbiamo usato il commutatore $[a_{+},a_{-}]=1$ per affermare $a_{-}a_{+}=a_{+}a_{-}+1$.

[^2]: L'integrale che compare da $\left\langle x^{2} \right\rangle=\int_{-\infty}^{+\infty}\psi_{0}^{*}x^{2}\psi_{0}\;dx$ può essere risolto usando tecniche per [[Integrali di posizione e quantità di moto]].