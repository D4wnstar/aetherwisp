Le simulazioni $N$-body sono usate per simulare fluidi non-collisionali, quali la materia oscura in un ammasso di galassie o le stelle in una galassia.
## Formulazione
La descrizione viene fatta mediante fisica statistica. Si parte dalla **funzione di distribuzione esatta** delle particelle nello spazio delle fasi:
$$F(\mathbf{r},\mathbf{v},t)=\sum_{i=1}^{N} \delta(\mathbf{r}-\mathbf{r}_{i}(t))\delta(\mathbf{v}-\mathbf{v}_{i}(t))$$
per $N$ particelle in posizioni $\mathbf{r}_{i}$ e velocità $\mathbf{v}_{i}$. Questa funzione dà la densità di numero delle particelle nel punto $(\mathbf{r},\mathbf{v})$ dello spazio delle fasi al tempo $t$. Assumiamo che tutte le particelle siano identiche. Chiamo
$$p(\mathbf{r}_{1},\ldots,\mathbf{r}_{N},\mathbf{v}_{1},\ldots,\mathbf{v}_{N})d\mathbf{r}_{1}\ldots d\mathbf{r}_{N}d\mathbf{v}_{1}\ldots d\mathbf{v}_{N}$$
la probabilità che il sistema sia nel microstato $\mathbf{w}\equiv(\mathbf{r}_{1},\ldots,\mathbf{r}_{N},\mathbf{v}_{1},\ldots,\mathbf{v}_{N})$ al tempo $t$. $p(\mathbf{w})$ è la densità di probabilità degli stati. Di questa probabilità si trova dunque l'[[Ensemble average]]:
$$f_{1}(\mathbf{r},\mathbf{v},t)\equiv \langle F(\mathbf{r},\mathbf{v},t) \rangle =\int F(\mathbf{r},\mathbf{v},t)p(\mathbf{w})d\mathbf{r}_{1}\ldots d\mathbf{r}_{N}d\mathbf{v}_{1}\ldots d\mathbf{v}_{N}$$
Questo è il valor medio della densità di numero in $(\mathbf{r},\mathbf{v},t)$ al tempo $t$.

Riprendendo la definizione di $F$, dato che è fatta di delta di Dirac, possiamo dire che
$$\begin{align}
f_{1}(\mathbf{r},\mathbf{v},t)&=\sum_{i=1}^{N} \int \delta(\mathbf{r}-\mathbf{r}_{i})\delta(\mathbf{v}-\mathbf{v}_{i})p(\mathbf{r}_{1},\ldots,\mathbf{r}_{N},\mathbf{v}_{1},\ldots,\mathbf{v}_{N})\ d\mathbf{r}_{1}\ldots d\mathbf{r}_{N}d\mathbf{v}_{1}\ldots d\mathbf{v}_{N} \\
&=N\int p(\mathbf{r},\mathbf{r}_{2},\ldots,\mathbf{r}_{N},\mathbf{v},\mathbf{v}_{2},\ldots,\mathbf{v}_{N})\ d\mathbf{r}_{2}\ldots d\mathbf{r}_{N}d\mathbf{v}_{2}\ldots d\mathbf{v}_{N}
\end{align}$$
Questo è perché per ogni indice, la delta di Dirac dà
$$\begin{align}
&\int p(\mathbf{r}_{1},\ldots,\mathbf{r}_{i},\ldots,\mathbf{r}_{N},\mathbf{v}_{1},\ldots,\mathbf{v}_{i},\ldots,\mathbf{v}_{N})\delta(\mathbf{r}-\mathbf{r}_{i})\delta(\mathbf{v}-\mathbf{v}_{i})d^{3N}r\ d^{3N}v \\
=&\int p(\mathbf{r}_{1},\ldots,\mathbf{r},\ldots,\mathbf{r}_{N},\mathbf{v}_{1},\ldots,\mathbf{v},\ldots,\mathbf{v}_{N})d^{3N-3}r\ d^{3N-3}v
\end{align}$$
In pratica, l'$i$-esimo argomento viene sostituito con il generico punto $(\mathbf{r},\mathbf{v})$. Dato che le particelle sono identiche, possiamo permutare questo risultato a modo che l'argomento sostituito sia sempre quelli di indice $i=1$, dandoci dunque $N$ risultati uguali, che si sommano dando $N$ copie dello stesso integrale.

Similmente, possiamo definire $f_{2}(\mathbf{r},\mathbf{r}',\mathbf{v},\mathbf{v}',t)$ come l'ensemble average del prodotto di $F$ in due punti $(\mathbf{r},\mathbf{v})$ e $(\mathbf{r}',\mathbf{v}')$ al tempo $t$:
$$\begin{align}
f_{2}(\mathbf{r},\mathbf{r}',\mathbf{v},\mathbf{v}',t)&\equiv \langle F(\mathbf{r},\mathbf{v},t)F(\mathbf{r}',\mathbf{v}',t) \rangle  \\
&=N(N-1)\int p(\mathbf{r},\mathbf{r}',\mathbf{r}_{3},\ldots,\mathbf{r}_{N},\mathbf{v},\mathbf{v}',\mathbf{v}_{3},\ldots,\mathbf{v}_{N})d\mathbf{r}_{3}\ldots d\mathbf{r}_{N}d\mathbf{v}_{3}\ldots d\mathbf{v}_{N}
\end{align}$$
Possiamo poi definire $f_{3}$, $f_{4}$, ecc., analogamente. Questo dà vita alla **catena BBGKY** (o **catena Bogoliubov-Born-Green-Kirkwood-Yvon**). Risolverla non è semplice, ma in un sistema dove ogni particella è scorrelata da ogni altra, essa si semplifica ad un semplice prodotto:
$$f_{2}(\mathbf{r},\mathbf{r}',\mathbf{v},\mathbf{v}',t)=f_{1}(\mathbf{r},\mathbf{v},t)f_{1}(\mathbf{r}',\mathbf{v}',t)$$
e via avanti. In altre parole, ogni distribuzione è "lasciata a se stessa" e non è affetta in alcun modo dalle altre. In pratica, è il limite di [[Independent variables]].

Tornando alla distribuzione degli stati $p(\mathbf{w})$, la conservazione della probabilità nello spazio degli stati implica la presenza di un'equazione di continuità:
$$\frac{ \partial p }{ \partial t } +\nabla(p \dot{\mathbf{w}})=0$$
che può essere riscritta come
$$\frac{ \partial p }{ \partial t } +\sum_{i} \left( p \frac{ \partial \dot{\mathbf{r}}_{i} }{ \partial \mathbf{r}_{i} } +\frac{ \partial p }{ \partial \mathbf{r}_{i} } \dot{\mathbf{r}}_{i}+p \frac{ \partial \dot{\mathbf{v}}_{i} }{ \partial \mathbf{v}_{i} } +\frac{ \partial p }{ \partial \mathbf{v}_{i} } \dot{\mathbf{v}}_{i} \right)=0$$
Dato che nel nostro caso stiamo trattando sistemi puramente gravitazionali e quindi conservativi, possiamo descrivere il sistema con una Hamiltoniana e quindi le leggi del moto di Hamilton. Applicando
$$\dot{\mathbf{r}}=\frac{ \partial H }{ \partial \mathbf{p} } ,\quad \dot{\mathbf{p}}=- \frac{ \partial H }{ \partial \mathbf{r} } $$
ritroviamo il [[Liouville's theorem]]:
$$\frac{ \partial p }{ \partial t } +\sum_{i} \left( \mathbf{v}_{i}\frac{ \partial p }{ \partial \mathbf{r}_{i} } +\mathbf{a}_{i}\frac{ \partial p }{ \partial \mathbf{v}_{i} }  \right)=0$$
dove $\mathbf{a}_{i}=\dot{\mathbf{v}}_{i}=\mathbf{F}_{i}/m_{i}$. Nel limite scorrelato/non-collisionale, questo risultato si applica anche alla distribuzione ad un punto $f_{1}\equiv f$ (che dipende da $p$) fintanto che integriamo tutte le coordinate tranne una. In tal caso, la somma di fatto svanisce e otteniamo l'**equazione di Vlasov**:
$$\boxed{\frac{ \partial f }{ \partial t } +\mathbf{v}\frac{ \partial f }{ \partial \mathbf{r} } +\mathbf{a}\frac{ \partial f }{ \partial \mathbf{v} } =0}$$
Nel limite non-collisionale, l'accelerazione/forza su una particella non può essere causata da una singola altra particella. Se lo fosse, le due particelle non sarebbero scorrelate e dunque non varrebbe più l'approssimazione. Deve essere solo dovuta a effetti collettivi. Nel caso cosmologico, ciascuna particella massiva ha un campo gravitazionale proprio e ciascuna particella percepisce *solo* l'effetto del campo collettivo. Il campo collettivo si determina dalla densità di massa
$$\rho(\mathbf{r},t)=m\int f(\mathbf{r},\mathbf{v},t)d\mathbf{v}$$
che produce un campo il cui potenziale soddisfa la [[Poisson's equation]]
$$\nabla ^{2}\Phi(\mathbf{r},t)=4\pi G\rho(\mathbf{r},t)$$
L'accelerazione dunque è data da
$$\mathbf{a}=-\frac{ \partial \Phi }{ \partial \mathbf{r} } $$
Piazzando questa equazione in quella di Vlasov si ottiene un **sistema Poisson-Vlasov**:
$$\boxed{\begin{align}
\frac{ \partial f }{ \partial t } +\mathbf{v}\frac{ \partial f }{ \partial \mathbf{r} } -\frac{ \partial \Phi }{ \partial \mathbf{r} } \frac{ \partial f }{ \partial \mathbf{v} } =0 \\
\nabla ^{2}\Phi =4\pi Gm \int f(\mathbf{r},\mathbf{v},t)d\mathbf{v}
\end{align}}$$
Lo scopo di una simulazione $N$-body è risolvere queste due equazioni simultaneamente.

Queste equazioni però descrivono un sistema fluido e continuo, dato che le particelle sono andate a perdersi nel fare l'ensemble average. Per tornare ad un sistema di corpi discreti, reintroduciamo le particelle come macro-particelle fiduciali che comprendono numerose particelle vere. Questo è necessario per mantenere realisticamente piccolo il numero di particelle che dovranno essere simulate. Le equazioni del modo delle macro-particelle sono
$$\boxed{\begin{align}
\ddot{\mathbf{x}}_{i}&=-\nabla_{i}\Phi(\mathbf{r}_{i}) \\
\Phi(\mathbf{r})&=-G\sum_{j=1}^{N}  \frac{m_{j}}{\sqrt{ (\mathbf{r}-\mathbf{r}_{j})^{2}+\boldsymbol{\epsilon}^{2} }}
\end{align}}\tag{1}$$
Alcuni commenti:
- La massa di una macro-particella non compare nella propria equazione del moto, solo quella delle altre. Non c'è una auto-forza. Questo è importante perché l'unica cosa che rimane è la forma di $\Phi$. Dunque, le orbite delle macro-particelle sono tanto valide quanto quelle delle particelle originali finché il loro numero è sufficiente da descrivere $\Phi$ bene.
- Questo modello a $N$ corpi dà una singola realizzazione (approssimata) della distribuzione ad un punto $f_{1}$. Non dà direttamente l'ensemble average.
- $\boldsymbol{\epsilon}$ è una **lunghezza di attenuazione**. Lo scopo è evitare grossi angoli di scattering dovuti alle singolarità di singole macro-particelle (che sono fittizie). Vogliamo anche evitare che alcune particelle si leghino ad altre in sistemi legati (e.g. due particelle che si orbitano a vicenda). Questa sarebbe una grave violazione della non-correlazione/collisionalità. Le particelle non si legano in coppie finché
  $$\langle v^{2} \rangle \gg \frac{Gm}{\epsilon}$$
  che è un buon punto d'inizio (necessario ma non sufficiente) per scegliere il valore di $\epsilon$. La presenza di un'attenuazione implica l'introduzione di una risoluzione spaziale minima: ogni cosa al di sotto viene sfumata.

In linea di principio, il sistema Poisson-Vlasov sopra è sufficiente. Di fatto, in cosmologia dobbiamo affrontare il problema di uno spaziotempo in espansione e dunque un concetto di spazio che cambia nel tempo della simulazione. Le coordinate a tempo zero sono diverse da quelle al tempo finale semplicemente perché lo spazio si è espanso nel frattempo. Questo problema è risolto esprimendo tutto in [[comoving coordinates]] $\mathbf{x}$ anziché coordinate regolari $\mathbf{r}$. Le due sono legate da
$$\mathbf{x}=a(z)\mathbf{r}$$
dove $a(z)=1/(1+z)$ è il fattore scala cosmologico al [[redshift]] $z$. L'evoluzione di $a$ è governata da quella del parametro di Hubble:
$$\begin{align}
\frac{\dot{a}}{a}=H(z)&= \sqrt{ (1+z)^{3}\Omega_{m}+ (1+z)^{2}(1-\Omega_{m}-\Omega_{\Lambda})+\Omega_{\Lambda} }  \\
&=\sqrt{ \frac{\Omega_{m}}{a^{3}}+ \frac{1-\Omega_{m}-\Omega_{\Lambda}}{a^{2}}+\Omega_{\Lambda} }
\end{align}$$
nel modello di FLRW.

In un universo in espansione infinito, modellato attraverso condizioni al contorno periodiche in una regione simulazione cubica di spigolo $L$, si può dimostrare (Springer et al. 2001) che il sistema Poisson-Vlasov può essere riscritto come
$$\boxed{\begin{align}
\frac{d}{dt} (a^{2}\dot{\mathbf{x}}_{i})&=- \frac{1}{a}\nabla_{i}\phi(\mathbf{x}_{i}) \\
\nabla ^{2}\phi(\mathbf{x}) & =4\pi G\sum_{i=1}^{N} m_{i}\left[\sum_{\mathbf{n}}\delta(\mathbf{x}-\mathbf{x}_{i}-\mathbf{n}L) - \frac{1}{L^{3}} \right]
\end{align}}$$
- Qui $\phi$ è il **potenziale gravitazionale peculiare**, che corrisponde al potenziale Newtoniano delle deviazioni di densità rispetto ad una densità costante di sfondo, qui calcolato in forma discreta come differenza tra il potenziale delle particelle e la media di fondo.
- Da notare che la somma per il potenziale nelle parentesi quadre è compiuta su tutte le copie periodiche di una particella, identificata dal vettore $\mathbf{n}=(n_{1},n_{2},n_{3})\in \mathbb{Z}^{3}$ che identifica una copia periodica dell'universo.
- Il termine $-1/L^{3}$ serve a far svanire la densità media, altrimenti non esisterebbe una soluzione per spazio infinito. Infatti, quando portato fuori dalla parentesi si riduce a $-4\pi G/L^{3}\sum_{i=1}^{N}m_{i}=-4\pi GM/L^{3}$, dove $M$ è la massa totale della simulazione.

In pratica:
1. La prima equazione contiene tutte le equazioni del moto da risolvere. Queste sono le ODE che vanno integrate nel modo standard in qualunque metodo.
2. La seconda equazione dà il potenziale gravitazionale e dunque le forze necessarie per risolvere le equazioni del moto. Il metodo di simulazione determina come viene risolta questa.

In metodi efficienti come quelli ad albero o PM, l'equazione di Poisson è risolta numericamente per ottenere i valori di $\phi(\mathbf{x})$ in modo efficiente. Nella somma diretta, in realtà non abbiamo bisogno dell'equazione di Poisson o del potenziale peculiare, dato che possiamo sommare direttamente i contributi gravitazionali secondo la legge di gravità di Newton.
### Somma diretta
Estraendo $\ddot{\mathbf{x}}$ otteniamo:
$$\ddot{\mathbf{x}}_{i}=\underbrace{ - \frac{1}{a^{3}}\nabla\Phi(\mathbf{x}_{i}) }_{ \ddot{\mathbf{x}}_{\text{grav},i} }\underbrace{ - 2 H(z)\dot{\mathbf{x}}_{i} }_{ \ddot{\mathbf{x}}_{\text{Hubble},i} }\tag{2}$$
dove $H(z)=\dot{a}/a$ è il parametro di Hubble. Queste sono le nostre equazioni del moto. Il primo termine è quello gravitazionale, il secondo è detto **Hubble drag** e rappresenta una decelerazione dovuta all'espansione dell'universo. Difatti, dipende solo dalla cosmologia scelta e non dalla gravità. Di conseguenza, ha costo computazionale pressoché nullo.

Le forze sono calcolate mediante somma diretta. Con condizioni al contorno chiuse, la forza è quella della legge della gravitazione universale di Newton, ossia partendo da $(1)$ cerchiamo $-\nabla \Phi(\mathbf{x}_{i})$. Il potenziale gravitazionale prodotto dalla $j$-esima particella e sentito dalla $i$-esima particella è
$$\Phi_{j}(\mathbf{x}_{i})=-G m_{j} \frac{1}{\sqrt{ (\mathbf{x}_{i}-\mathbf{x}_{j})^{2}+\boldsymbol{\epsilon}^{2} }}$$
Il cui gradiente è (usando $\mathbf{x}_{i}-\mathbf{x}_{j}\equiv \boldsymbol{\mathfrak{r}}$ per brevità):
$$\begin{align}
\nabla \Phi_{j}(\mathbf{x}_{i})&=\nabla\left[ -Gm_{j} \frac{1}{\sqrt{ \mathfrak{r}^{2}+\epsilon ^{2} }} \right] \\
&=-Gm_{j}\nabla\left[ \frac{1}{\sqrt{ \mathfrak{r}^{2}+\epsilon ^{2} }} \right] \\
&=-Gm_{j}\left[ - \frac{1/2}{[\mathfrak{r}^{2}+\epsilon ^{2}]^{3/2}}\nabla(\mathfrak{r}^{2}+\epsilon ^{2}) \right] \\
&=-Gm_{j}\left[ - \frac{1}{2[\mathfrak{r}^{2}+\epsilon ^{2}]^{3/2}}\nabla \mathfrak{r}^{2} \right] \\
&=-Gm_{j}\left[ - \frac{1}{2[\mathfrak{r}^{2}+\epsilon ^{2}]^{3/2}} 2\boldsymbol{\mathfrak{r}} \right] \\
&=Gm_{j} \frac{\boldsymbol{\mathfrak{r}}}{[\mathfrak{r}^{2}+\epsilon ^{2}]^{3/2}}
\end{align}$$
e dunque
$$-\nabla \Phi_{j}(\mathbf{x}_{i})=-Gm_{j} \frac{\mathbf{x}_{i}-\mathbf{x}_{j}}{[(\mathbf{x}_{i}-\mathbf{x}_{j})^{2}+\epsilon ^{2}]^{3/2}}$$
Per trovare il potenziale totale su $i$ sommiamo su tutte le particelle[^1]:
$$\boxed{-\nabla \Phi(\mathbf{x}_{i})=-G\sum_{j=1}^{N}m_{j} \frac{\mathbf{x}_{i}-\mathbf{x}_{j}}{[(\mathbf{x}_{i}-\mathbf{x}_{j})^{2}+\epsilon ^{2}]^{3/2}}}$$
Questo è esatto in condizioni al contorno chiuse. In condizioni periodiche, dobbiamo considerare anche tutte le (infinite) copie periodiche di ciascuna particella. Ciascuna copia della $j$-esima particella è situata a coordinate $\mathbf{x}_{j}+\mathbf{n}L\equiv \mathbf{x}_{j,\mathbf{n}}$ di distanza, con $\mathbf{n}$ che identifica quale copia periodica si ha. Il gradiente va dunque esteso a
$$\boxed{-\nabla \Phi(\mathbf{x}_{i})=-G\sum_{j=1}^{N} m_{j}\sum_{\mathbf{n}} \frac{\mathbf{x}_{i}-\mathbf{x}_{j,\mathbf{n}}}{[(\mathbf{x}_{i}-\mathbf{x}_{j,\mathbf{n}})^{2}+\epsilon ^{2}]^{3/2}}}\tag{3}$$
La somma su $\mathbf{n}$ è infinita dato che le condizioni periodiche servono per simulare un universo infinito. Di conseguenza, non è risolvibile analiticamente. Per renderla trattabile, si può ad esempio limitarsi alle $k$ copie più vicine.

Con questo abbiamo tutti i pezzi necessari per integrare numericamente. Ad ogni timestep, si calcola il gradiente del potenziale $(3)$, poi lo si usa per integrare $(2)$ numericamente.

Con il metodo leapfrog, l'integrazione numerica è
$$\begin{align}
\dot{x}_{n+1/2}&=\dot{x}_{n}+f(x_{n}) \frac{\Delta t}{2} \\
x_{n+1}&=x_{n}+\dot{x}_{n+1/2} \Delta t \\
\dot{x}_{n+1}&=\dot{x}_{n+1/2}+f(x_{n+1}) \frac{\Delta t}{2}
\end{align}$$
dove $f(x)$ è il lato destro di $(2)$.
### Fonti
- Springel, 2014, High performance computing and numerical modelling

[^1]: Ricordiamo che stiamo cercando il potenziale collettivo, quindi serve contare anche la particella stessa nella somma.
