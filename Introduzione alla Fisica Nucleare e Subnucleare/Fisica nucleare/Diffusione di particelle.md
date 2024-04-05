La **diffusione** è un urto, o collisione, tra [[Particella|particelle]]. È utile per studiare la struttura interna dell'oggetto, detto *bersaglio* o *targhetta*, in questione. Questo può essere una targhetta *fissa* (solida, liquida o gassosa) o una *in movimento*, che viene bombardata da un *proiettile* che può essere una qualunque particella: [[elettrone]], [[protone]], ecc.
## Diffusione elastica
La diffusione elastica è un tipo di diffusione nel quale l'energia cinetica viene conservata, ma viene redistribuita tra le particelle prodotte. Inoltre, le particelle prodotte sono le stesse di quelle incidenti.
![[Schema Diffusione elastica|60%|center]]
La diffusione si scrive
$$a+b \rightarrow a'+b'$$

Prendiamo la [[lunghezza d'onda di Compton]]
$$\lambda_{C}=\frac{\lambda}{2\pi}=\frac{\hbar}{p}=\frac{\hbar c}{\sqrt{2mc^{2}E_{cin}+E_{cin}^{2}}}$$
Ora ho due casi, a dipendenza di quanto relativistica sia l'energia
$$\lambda_{C}=\begin{cases}
\frac{\hbar}{\sqrt{2mE_{cin}}} \text{ se }E_{cin}\ll mc^{2} \\
\sim \frac{\hbar c}{E_{cin}} \text{ se }E_{cin}\gg mc^{2}
\end{cases}$$
A causa del [[Disuguaglianza di Heisenberg|principio di indeterminazione]], se voglio studiare una risoluzione spaziale $\Delta x$, devo utilizzare $\lambda_{C}\leq\Delta x$, ossia
$$p\geq \frac{\hbar}{\Delta x} \rightarrow pc\geq \frac{\hbar c}{\Delta x}\sim \frac{200 \text{ MeV fm}}{\Delta x}$$
Se il raggio del [[nucleo atomico]] è circa 1 fm, allora ho $p\sim$ 10 - 1000 MeV/c. Se è attorno ai 0.8 fm, si ha $p\sim$ 1000 MeV/c, quindi l'energia deve essere nell'ordine dei GeV.
## Diffusione anelastica
La diffusione anelastica è un tipo di diffusione dove :)
![[Schema Diffusione anelastica|60%|center]]
La diffusione si scrive
$$a+b \rightarrow a'+b^{*} \rightarrow a'+c+d$$
dove $b^{*}$ può tornare allo stato fondamentale emettendo [[Decadimento Gamma#Radiazione elettromagnetica|radiazione]] $\gamma$ o può [[Decadimento|decadere]] in $c$ e $d$.
## Diffusione di Rutherford
La diffusione di Rutherford è lo scattering (urto) di particelle $\alpha$ sul nucleo. Le particelle $\alpha$ non sono puntiformi e useremo l'elettrone. La forza tra elettrone e nucleo è l'[[Interazioni fondamentali#Interazione elettromagnetica|interazione elettromagnetica]].
### Cinematica della diffusione di $e^{-}$ sul nucleo
La collisione avviene a regime relativistico, quindi usiamo la notazione [[quadrivettore|quadrivettoriale]]. Il quadrivettore spaziotemporale e il quadrivettore energia-impulso sono
$$x=(x_{0},x_{1},x_{2},x_{3}),\quad p=(p_{0},p_{1},p_{2},p_{3})=\left( \frac{E}{c}, \vec{p}\right)$$
Sappiamo che $p^{2}$ è una [[invariante relativistica]] e quindi
$$p^{2}=pp=\frac{E}{c} \frac{E}{c}-p_{1}p_{1}-p_{2}p_{2}-p_{3}p_{3}=\frac{E^{2}}{c^{2}}-\vec{p}^{2}$$
ma anche $p^{2}=m^{2}c^{4}$ nel sistema di riferimento a riposo con $\vec{p}=0$ e $E=mc^{2}$. Allora definisco **massa invariante** $m=|\vec{p}|/c$. A riposo ho $E^{2}-\vec{p}^{2}c^{2}=m^{2}c^{4}$, ma per energie relativistiche posso fare l'approssimazione
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

Consideriamo un urto di un elettrone su un nucleo con carica $Ze$. Trovo la [[sezione d'urto]] di Rutherford.

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