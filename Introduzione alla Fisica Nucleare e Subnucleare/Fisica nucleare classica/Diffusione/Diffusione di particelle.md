---
wiki-publish: true
---
La **diffusione** è un urto, o collisione, tra [[Particella|particelle]]. Quando si usano strutture macroscopiche, come in un collisore, si dice **bersaglio** o **targhetta** l'oggetto colpito da un **fascio di particelle** con una certa energia. Le particelle del fascio sono dette **proiettili**.

La diffusione è utile per studiare la struttura interna dell'oggetto colpito, che può essere una targhetta *fissa* (solida, liquida o gassosa) o una *in movimento*, come un altro fascio di particelle che viaggia in direzione opposta. Questo è quello che accade, per esempio, al LHC del CERN, dove si fanno collidere due fasci di particelle opposti.
## Diffusione elastica
La **diffusione elastica** è un tipo di diffusione nel quale l'energia cinetica viene conservata e viene redistribuita tra le particelle prodotte. Inoltre, le particelle prodotte sono le stesse di quelle incidenti e il bersaglio rimane nello [[stato]] fondamentale. In pratica, le particelle *rimbalzano* e si scambiano energia cinetica.

![[Schema Diffusione elastica|60%|center]]

La diffusione si scrive
$$a+b \rightarrow a'+b'$$

Prendiamo la [[Formula di de Broglie|lunghezza d'onda di De Broglie ridotta]]
$$\newcommand\lambdabar{
\raise1.5pt{\moveright2.0pt\unicode{0x0335}}\moveleft1pt\lambda
}
\lambdabar=\frac{\lambda}{2\pi}=\frac{\hbar}{p}=\frac{\hbar c}{\sqrt{2mc^{2}E_{cin}+E_{cin}^{2}}}$$
Ora ho due casi, a dipendenza di quanto relativistica sia l'energia
$$\lambdabar\simeq\begin{cases}
\frac{\hbar}{\sqrt{2mc^{2}E_{cin}}} \text{ se }E_{cin}\ll mc^{2} \\
\frac{\hbar c}{E_{cin}} \text{ se }E_{cin}\gg mc^{2}
\end{cases}$$
A causa del [[Disuguaglianza di Heisenberg|principio di indeterminazione]], se voglio studiare una risoluzione spaziale $\Delta x$, devo utilizzare $\lambdabar\leq\Delta x$, ossia
$$p\geq \frac{\hbar}{\Delta x} \quad\rightarrow\quad E= pc\geq \frac{\hbar c}{\Delta x}\sim \frac{200 \text{ MeV fm}}{\Delta x}$$
Se il raggio del [[nucleo atomico]] è circa 1 fm, allora ho $p\sim$ 10 - 1000 MeV/c. Se è attorno ai 0.8 fm, si ha $p\sim$ 1000 MeV/c, quindi l'energia deve essere nell'ordine dei GeV.
## Diffusione anelastica
La **diffusione anelastica** è un tipo di diffusione dove parte dell'energia cinetica viene trasferita dal proiettile $a$ al bersaglio $b$, che lo porta ad uno stato eccitato $b^{*}$. Questo poi [[Decadimento nucleare|decade]] allo stato fondamentale, emettendo una o più particelle.
![[Schema Diffusione anelastica|60%|center]]
La diffusione si scrive
$$a+b \rightarrow a'+b^{*} \rightarrow a'+c+d$$
dove $b^{*}$ può tornare allo stato fondamentale emettendo [[Decadimento Gamma#Radiazione elettromagnetica|radiazione]] $\gamma$ o può [[Decadimento nucleare|decadere]] in $c$ e $d$.

Se da una diffusione anelastica rivelo solo $a'$, si dice **inclusiva**, mentre se rivelo tutti i prodotti di reazione, si dice **esclusiva**. In realtà, il proiettile $a$ può anche scomparire in una diffusione anelastica, emettendo solo nuove particelle o trasferendo l'energia per alzare di stato il bersaglio.
## Diffusione di Rutherford
La diffusione di Rutherford è lo scattering (urto) di particelle $\alpha$ sul nucleo. Le particelle $\alpha$ non sono puntiformi e useremo l'elettrone. La forza tra elettrone e nucleo è l'[[Fundamental interaction#Interazione elettromagnetica|interazione elettromagnetica]].
### Cinematica della diffusione di $e^{-}$ sul nucleo
La collisione avviene a regime relativistico, quindi usiamo la notazione [[Four-vector|quadrivettoriale]]. Il quadrivettore spaziotemporale e il quadrivettore energia-impulso sono
$$x=(x_{0},x_{1},x_{2},x_{3}),\quad p=(p_{0},p_{1},p_{2},p_{3})=\left( \frac{E}{c}, \vec{p}\right)$$
Sappiamo che $p^{2}$ è una [[Relativistic invariant]] e quindi
$$p^{2}=pp=\frac{E}{c} \frac{E}{c}-p_{1}p_{1}-p_{2}p_{2}-p_{3}p_{3}=\frac{E^{2}}{c^{2}}-\vec{p}^{2}$$
ma anche $p^{2}=m^{2}c^{4}$ nel sistema di riferimento a riposo con $\vec{p}=0$ e $E=mc^{2}$. Allora definisco [[Invariant mass]] $m=|\vec{p}|/c$. A riposo ho $E^{2}-\vec{p}^{2}c^{2}=m^{2}c^{4}$, ma per energie relativistiche posso fare l'approssimazione
$$\text{se }E\gg mc^{2} \Rightarrow E\sim|\vec{p}|c$$
![[Schema Diffusione di Rutherford|80%|center]]
I quadrivettori impulso-energia iniziali sono $p=(E/c, \vec{p})$ e $P=(Mc^{2}/c,0)$ per elettrone e nucleo rispettivamente. Conservo energia ed impulso
$$p+P=p'+P'=\left(\frac{E'}{c},\vec{p}'\right)+\left(\frac{E'_{n}}{c},\vec{P}'\right)\tag{*}$$
Assumiamo di avere una diffusione elastica. Allora, $m_{e}$ e $M$ sono invariate dopo l'urto. Vale
$$p^{2}=p'^{2}=m_{e}^{2}c^{2},\quad P^{2}=P'^{2}=M^{2}c^{2}\quad \rightarrow \quad p\cdot P=p'\cdot P'$$
$$p\cdot P=p'(p+P-p')=p'\cdot p+p P-m_{e}^{2}c^{2}\tag{1}$$
Nel sistema di riferimento $(*)$ e la $(1)$
$$(p\cdot P)c^{2}=(p'\cdot P')c^{2}=(p'\cdot p+p'\cdot P-m_{e}c^{2})c^{2}=E'E+\vec{p}\cdot\vec{p}'+E'Mc^{2}-m_{e}^{2}c^{4}$$
Ad energie relativistiche $E\sim|\vec{p}|c$ trascuro $m_{e}^{2}c^{4}$. Mi rimane
$$EMc^{2}=E'E(1-\cos\theta)+E'Mc^{2}$$
Nel sistema $(*)$ del laboratorio vale
$$E'=\frac{E}{\frac{E}{Mc^{2}}(1-\cos\theta)}$$
con $\theta$ l'angolo di diffusione. Questa quantità è molto importante perché è molto facile da misurare.

Consideriamo un urto di un elettrone su un nucleo con carica $Ze$. Trovo la [[Sezione d'urto]] di Rutherford.

*grafico dell'urto di Rutherford qui*
#### Metodo classico
L'elettrone subisce una traiettoria di tipo iperbolico ($\propto 1/r^{2}$). Quando l'elettrone è lontano dal nucleo, non subisce repulsione Coulombiana. Il potenziale è $V=0$ e l'energia cinetica è $T=\frac{1}{2}mv_{0}^{2}$. Il momento angolare è $l=|\vec{r}\times m\vec{v}|=mv_{0}b$.

Ho $b$ il parametro d'impatto e $r_{min}$ la distanza minima tra elettrone e nucleo. Se ho $b=0$ ho una collisione frontale e $r_{min}$ è il più piccolo possibile
$$\frac{1}{2}mv_{0}^{2}=\frac{1}{4\pi\epsilon_{0}} \frac{zZe^{2}}{d}$$
Conservo l'energia in un punto generico della traiettoria:
$$\frac{1}{2}mv_{0}^{2}=\frac{1}{2}mv^{2}+ \frac{1}{4\pi\epsilon_{0}} \frac{zZe^{2}}{r}$$
*grafico simmetrica cilindrica qui*
Ho simmetria cilindrica. Le particelle incidono nell'anello $b+db$ e sono distribuite in un anello $d\theta$ in un rivelatore posto a distanza $r$. Chiamo $df$ la frazione di particelle incidenti che attraversano l'anello di area $2\pi bdb$:
$$df=nx(2\pi dbd)\tag{2}$$
con $n$ il numero di nuclei e $x$ lo spessore della pellicola

Con parametri $<b$ ho $f=nx\pi b^{2}$. Il momento lineare $\vec{p}_{i}$ e $\vec{p}_{f}$ cambiano direzione. Lontano dal nucleo vale $mv_{0}$. Assumendo un atomo massivo, non ho rinculo.

*ancora un altro grafico qui*
Uso come coordinate istantanee $\vec{r}$ e $\beta$, dove $\beta$ è la coordinata tra la bisettrice e $\vec{r}$, dove $\vec{r}$ localizza la particella. Vale
$$|\Delta\vec{p}|=2mv_{0}\sin\left(\frac{\theta}{2}\right)=2\pi v_{0}\cos\left(\frac{\pi-\theta}{2}\right)\tag{3}$$
Ho considerato $|\vec{p}_{i}|=|\vec{p}_{f}|$. Ora considero la seconda legge di Newton $F=dp/dt$. Allora
$$\Delta p =\int dp=\int Fdt=\frac{zZe^{2}}{4\pi\epsilon_{0}}\int \frac{\cos(\beta)}{r^{2}}dt\tag{4}$$
A $t=0$ ho $\beta=- \frac{\pi-\theta}{2}$ e a $t=\infty$ ho $\beta= \frac{\pi-\theta}{2}$.

Calcolo la velocità istantanea $\vec{v}$
$$\vec{v}=\frac{dr}{dt}\hat{r}+r \frac{d\beta}{dt}\hat{\beta}$$
Solo la componente tangenziale contribuisce a $\vec{v}$ vicino al nucleo.
$$l(\text{vicino al nucleo})=|m\vec{r}\times\vec{v}|=mr^{2} \frac{d\beta}{dt}$$
$$l(\text{lontano dal nucleo})=mv_{0}\beta$$
Vale la conservazione del momento angolare, quindi ho
$$mr^{2} \frac{d\beta}{dt}=mv_{0}\beta \quad\rightarrow \quad \frac{dt}{r^{2}}=\frac{d\beta}{v_{0}b}$$
Sostituendo in $(4)$ trovo
$$\Delta p = \frac{zZe^{2}}{4\pi\epsilon_{0}}\int_{-(\pi-\theta)/2}^{(\pi-\theta)/2} \cos\beta d\beta= \frac{zZe^{2}}{4\pi\epsilon_{0}v_{0}\beta} \cos\left(\frac{\theta}{2}\right)$$
Combino con $(3)$ per ottenere
$$b=\frac{d}{2}\cot\left(\frac{\theta}{2}\right)$$
e infine combino con $(2)$ per ottenere
$$|df|=\pi nx \frac{d^{2}}{4}\cot\left(\frac{\pi}{2}\right)\csc^{2}\left(\frac{\theta}{2}\right)d\theta=\pi nx \frac{d^{2}}{4}\cot\left(\frac{\pi}{2}\right) \frac{1}{\sin^{2}\left(\frac{\theta}{2}\right)}d\theta\tag{5}$$
Ora cerco la sezione d'urto
$$\frac{d\sigma}{d\Omega}=\frac{1}{nx} \frac{df}{d\Omega}$$
con $nx$ il numero di nuclei su un area e $df/d\Omega$ le particelle incidenti su un angolo solido. Nella geometria anulare ho $\sin\theta d\theta d\phi$ ed integro su tutto l'angolo azimutale, quindi ho $d\Omega=2\pi\sin\theta d\theta$.

Utilizzo $(1)$ e $(5)$
$$\frac{d\sigma}{d\Omega}=\left(\frac{zZe^{2}}{8\pi\epsilon_{0}T}\right)^{2} \frac{\cot\left(\frac{\theta}{2}\right)}{2\sin\theta \sin^{2}\left(\frac{\theta}{2}\right)}=\left(\frac{zZe^{2}}{8\pi\epsilon_{0}T}\right)^{2} \frac{\cos\left(\frac{\theta}{2}\right)}{2\sin^{3}\left(\frac{\theta}{2}\right)2\sin\left(\frac{\theta}{2}\right)\cos(\frac{\theta}{2})}=$$
$$=\left(\frac{zZe^{2}}{16\pi\epsilon_{0}T}\right)^{2} \frac{1}{\sin^{4}\left(\frac{\theta}{2}\right)}$$
Quindi, ricapitolando, ho che la sezione d'urto di Rutherford è
$$\frac{d\sigma}{d\Omega}=\left(\frac{zZe^{2}}{4\pi\epsilon_{0}}\right)^{2} \left(\frac{1}{4T}\right)^{2} \frac{1}{\sin^{4}\left(\frac{\theta}{2}\right)}$$
quindi dipende da $\propto z^{2}T^{-2}\sin^{-4}(\theta/2)$. Queste dipendenze sono state tutte dimostrare sperimentalmente da Geiger e Madsen.
#### Metodo quantistico
In regime quantistico vale il [[Disuguaglianza di Heisenberg|principio di indeterminazione]]. L'incertezza $\Delta b$ su $b$ implica $\Delta p\sim \hbar/\Delta b$. La dimostrazione classica ha senso se $\Delta b\ll b$ e $\Delta p\ll p$. Si ha
$$b\Delta p\gg \Delta b \Delta p \geq \hbar \quad \rightarrow\quad \frac{b\Delta p}{\hbar}\gg 1$$
Se $b\sim0$ e l'energia del proiettile è molto elevata, risento della forza forte. Allora, la sezione d'urto di Rutherford perde validità. A questo punto mi aiuta a stimare il raggio del nucleo.

Per trovare la sezione d'urto di Rutherford tramite la meccanica quantistica, consideriamo
- il rinculo del nucleo come trascurabile.
- inizialmente si ha una carica puntiforme che incide sul nucleo atomico.
- l'*approssimazione di Born*: $Z\alpha\ll1$, dove $\alpha=1/137$ è la [[Fine-structure constant]].
Le [[Funzione d'onda|funzioni d'onda]] entranti e uscenti dall'elettrone sono [[onda piana|onde piane]] e valgono
$$\psi_{i}=\frac{1}{\sqrt{V}}e^{i \vec{p}\cdot\vec{r}/\hbar},\quad \psi_{f}=\frac{1}{\sqrt{V}}e^{i \vec{p}'\cdot\vec{r}'/\hbar}$$
con $V$ il volume del nucleo. Gli elettroni sono liberi a 0 e a $+\infty$.

Considero le strutture discrete degli elettroni come un continuo.
$$V=\frac{N}{n}$$
dove $N$ è il numero di centri diffusori (di fatto il numero di [[Nucleone|nucleoni]]) e $n$ è la densità. Per un volume grande, considero una normalizzazione del tipo
$$\int_{V}|\psi_{i}|^{2}dV=nV$$
La regola d'oro di Fermi afferma che il tasso di reazioni $W$ è messo in relazione con la velocità delle particelle del fascio, la sezione d'urto ed il volume nel seguente modo:
$$W=\frac{\sigma v_{e}}{V}=\frac{2\pi}{\hbar}|\langle \psi_{f}|\mathcal{M}_{int}|\psi_{i}\rangle|^{2} \frac{dn}{dE_{f}}$$
L'energia dello stato finale è $E_{f}$ e vale $dE_{f}=dE'=dE$.

La densità nello [[Phase space]] è
$$dn(|\vec{p'}|)=\frac{4\pi |\vec{p'}|d |\vec{p'}|}{(2\pi\hbar)^{3}}V$$
quindi scrivo la sezione d'urto per l'elettrone nell'elemento di angolo solido $d\Omega$ come
$$d\sigma \frac{N}{V}=\frac{2\pi}{\hbar}|\langle \psi_{f}|\mathcal{H}_{int}|\psi_{i}\rangle|^{2} \frac{V |\vec{p'}|^{2}d |\vec{p'}|}{(2\pi\hbar)^{3}dE_{f}}d\Omega$$
Sostituisco $v$ con $c$ per il caso relativistico, nel quale $|\vec{p'}|\sim E'/c$. Allora
$$\frac{d\sigma}{d\Omega}=\frac{V^{2}}{(2\pi)^{2}} \frac{E'^{2}}{(\hbar c)^{4}} |\langle \psi_{f}|\mathcal{H}_{int}|\psi_{i}\rangle|^{2}$$
L'Hamiltoniana è
$$\mathcal{H}_{int}=\phi(\vec{r})$$
con $\phi(\vec{r})$ il potenziale del campo elettrico. La matrice di transizione è
$$\mathcal{M}_{fi}=\langle \psi_{f}|\mathcal{H}_{int}|\psi_{f}\rangle=\frac{1}{V}\int e^{-i \vec{p}'\cdot \vec{r}'/\hbar}V(\vec{r})e^{i\vec{p}\cdot \vec{r}/\hbar}d\vec{r}$$
Definiamo l'*impulso trasferito* $\vec{q}\equiv\vec{p}-\vec{p}'$. Allora la matrice diventa
$$\mathcal{M}_{fi}=\frac{1}{V}\int V(\vec{r}) e^{-i\vec{q}\cdot\vec{r}/\hbar}d\vec{r}$$
e vale anche
$$|\vec{q}|=2 |\vec{p}|\sin\left(\frac{\theta}{2}\right)$$
con $|\vec{p'}|=|\vec{p}|$ e $(1-\cos\theta)=2\sin^{2}(\theta/2)$. Il quadrato è
$$|\vec{q}|^{2}=|\vec{p}|^{2}+|\vec{p'}|^{2}-2 |\vec{p}| |\vec{p'}|\cos\theta=2 |\vec{p}|^{2}(1-cos\theta)=4 |\vec{p}|^{2}\sin^{2}\left(\frac{\theta}{2}\right)$$

Consideriamo una carica puntiforme. In un sistema a simmetria sferica, il potenziale è
$$V(\vec{r})= \frac{zZe^{2}}{4\pi\epsilon_{0}}\int \frac{\rho(\vec{r'})}{|\vec{r}-\vec{r'}|}d\vec{r'}$$
Tornando alla matrice di transizione, si ha
$$\mathcal{M}_{fi}=\frac{zZe^{2}}{4\pi\epsilon_{0}V}\int e^{i\vec{q}\cdot\vec{r}/\hbar}d\vec{r}\int \frac{\rho(\vec{r})}{|\vec{r}-\vec{r'}|}d\vec{r}=\ldots$$
e definendo $\vec{D}=\vec{r}-\vec{r'}$
$$\ldots=\frac{zZe^{2}}{4\pi\epsilon_{0}V}\int e^{i\vec{q}\cdot\vec{r}/\hbar}\frac{1}{D}d\vec{D}\int \rho(\vec{r}) e^{i\vec{q}\cdot\vec{r}/\hbar}d\vec{r'}$$
Passiamo in coordinate polari sferiche, usando $\alpha$ angolo polare e $\phi$ angolo azimutale.
$$\int \frac{\rho^{i\vec{q}\cdot\vec{r}/\hbar}}{r}d\vec{r}=\int_{0}^{2\pi}d\phi\int_{0}^{\pi}\sin\alpha d\alpha \int_{0}^{\pi} \frac{r^{2}}{r}e^{iqr\cos\alpha/\hbar}dr=2\pi\int_{-1}^{1}d(\cos\alpha)\int_{0}^{\infty} \frac{r^{2}}{r}e^{iqr\cos\alpha/\hbar}dr$$
$$=2\pi\int_{0}^{\infty}r \frac{\hbar}{iqr}(e^{iqr/\hbar}-e^{-iqr/\hbar})dr=2\pi\int_{0}^{\infty}\sin x dx$$
definendo $x=qr/\hbar$. Il problema è questo integrale diverge. Per sistemarlo, aggiungiamo un termine esponenziale $e^{-\lambda x}$ come
$$\int_{0}^{\infty}e^{-\lambda x}\sin xdx=\frac{1}{2i}\int_{0}^{\infty}[e^{(i-\lambda)x}-e^{-(i+\lambda x)}] dx=-\frac{1}{2i}\left(\frac{1}{i-\lambda}+ \frac{1}{i+\lambda}\right)=\frac{1}{1+\lambda^{2}}$$
Agli estremi si ha
$$\lim\limits_{\lambda \rightarrow 0} \frac{1}{1+\lambda^{2}}=1,\quad\lim\limits_{\lambda \rightarrow \infty} \frac{1}{1+\lambda^{2}}=0$$
Allora l'aggiunta del termine $e^{-\lambda x}$ tramite moltiplicazione non cambia il risultato fisico. Sostituisco
$$\int e^{iqD/\hbar} \frac{1}{D}dD=4\pi \left(\frac{\hbar}{q}\right)^{2}$$
e la matrice diventa
$$\mathcal{M}_{fi}=\langle \psi_{f}|\mathcal{H}_{int}|\psi_{i}\rangle=\frac{zZe^{2}}{\epsilon_{0}V} \frac{\hbar^{2}}{|\vec{q}|^{2}}\int \rho(\vec{r'}) e^{i\vec{q}\cdot\vec{r}/\hbar}d\vec{r'}$$
Il termine integrale è il [[Fattore di forma]] $F(\vec{q})$.

Nel caso in cui la carica sia puntiforme, si ha
$$\mathcal{M}_{fi}=\frac{zZe^{2}}{\epsilon_{0}V} \frac{\hbar^{2}}{|\vec{q}|^{2}}$$
e la sezione d'urto di Rutherford è
$$\frac{d\sigma}{d\Omega}=\frac{V^{2}E'^{2}}{(2\pi)^{2}(\hbar c)^{4}}|M_{fi}|^{2}=\left(\frac{zZe^{2}}{16\pi\epsilon_{0}}\right) \frac{4E'^{2}}{p^{4}c^{4}} \frac{1}{\sin^{4}(\frac{\theta}{2})}$$
Nel limite relativistico $E'=|\vec{p'}|c$ e $|\vec{p'}|=|\vec{p}|$ si ha
$$\frac{d\sigma}{d\Omega}=\left(\frac{zZe^{2}}{8\pi\epsilon_{0}E'}\right)^{2} \frac{1}{\sin^{4}(\frac{\theta}{2})}$$
Se consideriamo il caso non relativistico della particella di carica $Ze$ che si muove liberamente con $p=mv$ e $E_{cin}=1/2mv^{2}$ e se $E'=mc^{2}\gamma\sim1$, con $\gamma$ il [[coefficiente di Lorentz]], si ha
$$\frac{d\sigma}{d\Omega}=\left(\frac{zZe^{2}}{4\pi\epsilon_{0}}\right)^{2} \frac{1}{(4E_{cin})^{2}} \frac{1}{\sin^{4}(\frac{\theta}{2})}$$
che è esattamente il risultato del caso classico.