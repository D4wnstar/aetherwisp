---
aliases:
  - shell
---
Il **modello a shell** è un modello del [[nucleo atomico]]. Da non confondere con il modello a shell dell'[[atomo]] stesso, che tratta degli [[elettrone|elettroni]]. Ha i seguenti presupposti:
1. ogni [[nucleone]] occupa un livello di energia ben preciso all'interno di una *shell*.
2. i nucleoni si muovono nel nucleo sottoposti ad un [[potenziale]] *medio*.
3. il potenziale medio ha origine dagli altri nucleoni.

Lo stato di un nucleo ([[spin]] $\pm1/2$ e [[parità]] $(-1)^{l}$) è poi determinato unicamente dai nucleoni **spaiati**, ossia quelli disaccoppiati, un po' come sono gli elettroni di valenza a determinare lo stato di un atomo nella shell elettronica. Un nucleone mancante in una shell è detto **buco**.

Il modello a shell più preciso ([[Potenziale di Woods-Saxon]] con [[Struttura fine|accoppiamento spin-orbita]]) è molto accurato per $A<150$ e $190<A<220$. Al di là di questo intervallo bisogna adoperare altri stratagemmi, come considerare la deformazione dei nuclei (per $150<A<190$ e $A>230$).

Le predizioni compiute da questo modello sono corrette solo se nella shell più superiore (quella di valenza) è presente soltanto un nucleone spaiato. Shell non complete con più di un nucleone, come quelle del $^{23}_{11}Na_{12}$ non sono corrette.
### Potenziale gaussiano
Per nuclei piccoli ($A\leq7$), la distribuzione dei nucleoni nel nucleo è circa gaussiana, quindi possiamo approssimare il potenziale con distribuzione spaziale gaussiana. In altre parole, abbiamo un [[oscillatore armonico quantistico]] tridimensionale, che ha potenziale
$$V(r)=\frac{1}{2}kr^{2}$$
che dipende solo dalla coordinata radiale. La parte angolare dipende dagli angoli $\theta$ e $\phi$ e ha soluzione costante con le [[armoniche sferiche]] $Y_{l,m_{l}}(\theta,\phi)$ con $l=0,1,2,\ldots=s,p,d,f,\ldots$ [[numero quantico]] di momento angolare orbitale e $m_{l}=0,\pm1,\pm2,\ldots,\pm l$ numero quantico magnetico. Gli [[Equazione agli autovalori|autovalori]] di energia sono
$$E_{N}=\hbar \omega_{0}\left(N + \frac{3}{2}\right)$$
con $N=0,1,2,\ldots$ il numero di livelli energetici (*non è* il numero quantico principale!). Vale $l\leq N$. Introducendo $n$ il numero di nodi, possiamo scrivere i livelli come
$$N=2(n-1)+l$$
La [[degenerazione]] dei livelli di energia è pari a $2l+1$, o $2(2l+1)$ considerando lo [[spin]].

![[Grafico Modello a shell nucleare|80%|center]]

- Il livello $N=0$ ha $n=1$ e $l=0$, quindi corrisponde allo stato $1s$.
- Il livello $N=1$ ha $n=1$ e $l=1$, quindi corrisponde allo stato $1p$.
- Il livello $N=2$ ha $n=1$ e $l=2$ o $n=2$ e $l=0$, quindi corrisponde rispettivamente agli stati $1d$ e $2s$.

Calcolando il numero di nucleoni che compongono le shell chiuse, si trova che corrispondono ai [[Numero magico|numeri magici]] fino al 20, ma poi divergono.
### Potenziale di Woods-Saxon
Una descrizione più accurata richiede un potenziale più preciso. A questo scopo si può usare il [[Potenziale di Woods-Saxon]], per il quale si trovano numeri magici più accurati.

![[Shell complete Woods-Saxon.png|240]]

L'effetto di usare il potenziale di Woods-Saxon è quello di rimuovere la degenerazione di $l$ nelle shell, dato che gli stati con stesso $N$ ma diverso $nl$ hanno energie diverse sotto questo potenziale. Non replica comunque tutte i numeri magici, ma è più preciso del potenziale gaussiano.
### Accoppiamento spin-orbita
Migliorare ulteriormente il modello è complicato perché il potenziale di Woods-Saxon ha già la forma corretta dal punto di vista fisico e cambiarlo rovinerebbe l'interpretazione fisica del modello. Allora, ciò che possiamo fare è aggiungere correzioni a questo potenziale. Una tale correzione è l'**accoppiamento spin-orbita**, tra l'altro una delle correzioni di [[struttura fine]] dell'[[atomo di idrogeno]].

Chiamando il potenziale della correzione $V_{l,s}$, il potenziale corretto sarà
$$V_{tot}(r)=V_{centr}(r)+V_{l,s}(r)\frac{\left\langle \vec{l}\cdot\vec{s} \right\rangle}{\hbar^{2}}$$
dove $\vec{l}$ è il momento angolare orbitale (rispetto al centro del nucleo) e $\vec{s}$ è lo spin del nucleone.

I nucleoni sono [[fermione|fermioni]] e quindi hanno spin 1/2. Definiamo il **momento angolare totale** $\vec{j}$ come $\vec{j}=\vec{l}+\vec{s}$. Dato che lo spin può avere solo due valori, si ha
$$j=l\pm \frac{1}{2}$$
L'unica eccezione è il caso $l=0$, dove si ha sempre $j=1/2$. Calcoliamo
$$j^{2}=(\vec{l}+\vec{s})^{2}=(\vec{l}^{2}+2\vec{l}\cdot\vec{s}+\vec{s}^{2}) \quad\rightarrow\quad \vec{l}\cdot\vec{s}=\frac{1}{2}(\vec{j}^{2}-\vec{l}^{2}-\vec{s}^{2})$$
e risolvendo l'[[equazione agli autovalori]] e inserendo i valori attesi
$$\left\langle \vec{l} \cdot\vec{s} \right\rangle=\frac{\hbar^{2}}{2}[j(j+1)-l(l+1)-s(s+1)]=$$
$$=\hbar^{2}\begin{cases}
j=l+ \frac{1}{2} \rightarrow \frac{l}{2} \\
j=l- \frac{1}{2} \rightarrow -\frac{l+1}{2}
\end{cases}$$
quindi la separazione energetica dei livelli cresce linearmente con il momento angolare è
$$\Delta E_{l,s}=\left[\left\langle \vec{l} \cdot \vec{s}\right\rangle_{j=l+ \frac{1}{2}} - \left\langle \vec{l}\cdot\vec{s} \right\rangle_{j=l- \frac{1}{2}}\right]\langle V_{l,s}(r)\rangle=\frac{2l+1}{2}\langle V_{l,s}(r)\rangle$$
Sperimentalmente si trova che $V_{l,s}$ è negativo, quindi il livello $l+1/2$ è sempre sotto quello da $l-1/2$.

L'effetto di questa correzione è molto pronunciato e con questa, i numeri magici sono riprodotti alla perfezione.

![[Shell complete Spin-orbita.png|360]]

Ora i livelli con $l>0$ sono divisi in due nuovi livelli. Di solito il numero quantico $j$ è specificato mettendo un indice in più sotto la lettera associata ad $l$. Per esempio, per lo stato $n=1$ e $l=3$ ($1f$), che ha degenerazione 14, si scrive
$$\begin{cases}
j=\frac{5}{2} \rightarrow \text{ livello } 1f_{5/2} \\
j=\frac{7}{2} \rightarrow \text{ livello } 1f_{7/2}
\end{cases}$$
Ciascuno di questi livelli ha una cosiddetta **capacità**, ossia il numero di nucleoni che può ospitare. La somma progressiva delle capacità produce uno ad uno tutti i numeri magici.
### Applicazioni
Consideriamo due [[Isotopo|isotopi]] dell'ossigeno: $^{15}_{8}O$ e $^{17}_{8}O$. Entrambi hanno 8 protoni, ma uno ha 7 neutroni e l'altro 9. Nel primo caso vi è un protone spaiato; nel secondo un neutrone spaiato.

![[Shell ossigeno.png]]

Nel $^{15}_{8}O$, il protone spaiato è nella shell $1p_{1/2}$. Lo stato fondamentale del nucleo dovrebbe quindi avere spin 1/2 e parità $(-1)^{1}=-1$. È comune scrivere lo stato del nucleo nella forma $J^{P}$, dove $J$ è il momento angolare e $P$ è la parità, denotata con $+$ e $-$. In questa caso, si ha $J^{P}=\frac{1}{2}^{-}$.

Nel $^{17}_{8}O$, c'è un buco nel livello $1d_{5/2}$, quindi lo spin dovrebbe essere 5/2 e la parità $(-1)^{2}=1$, quindi un totale di $J^{P}=\frac{5}{2}^{+}$.
#### Nuclei pari-pari e dispari-dispari
Nel caso di [[nuclide|nuclidi]] con $Z$ e $N$ pari, indipendentemente da quali stati sono eccitati, lo stato fondamentale sarà $J^{P}=0^{+}$ e il primo eccitato sarà $J^{P}_{1}=2^{+}$. Siccome sono ordinati a coppie, avranno sempre parità positiva.

Per nuclidi con $Z$ e $N$ dispari, lo spin totale si ottiene come da norma per un sistema con due particelle con spin, ossia presi $j_{1}$ e $j_{2}$ gli spin, i valori possibili sono tra $|j_{1}-j_{2}|$ e $j_{1}+j_{2}$ in intervalli interi. La parità sarà $(-1)^{l_{1}+l_{2}}$, con $l_{1}$ e $l_{2}$ i momenti angolari orbitali del protone e neutrone spaiati.

Ad esempio, $^{6}_{3}Li_{3}$ ha sia un protone che un neutrone spaiato in $1p_{3/2}$, quindi ha $l_{1}=l_{2}=l=1$. Allora la parità sarà $(-1)^{1+1}=1$. Lo spin invece è tra $|3/2-3/2|=0$ e $3/2+3/2=3$, quindi può avere i valori di 0, 1, 2 o 3. In totale, gli stati possibili sono
$$J^{P}=0^{+},\,1^{+},\,2^{+},\,3^{+}$$
### Transizione di stato
Così come per gli elettroni, anche i nucleoni possono compiere una [[transizione di stato]] per salire o scendere di shell. Un nucleone può salire ad uno stato eccitato in due modi:
1. per eccitazione del nucleone spaiato nella sottoshell successiva.
2. per accoppiamento di questo nucleone con un altro che provenga da una sottoshell più interna.

Per esempio, nel caso del $^{7}_{3}Li_{4}$ ($J^{P}=\frac{3}{2}^{+}$), il neutrone spaiato è in $1p_{3/2}$ e può
1. salire di energia a $1p_{1/2}$. In questo caso diventa $J^{P}=\frac{1}{2}^{-}$.
2. accoppiarsi con il neutrone in $1s_{1/2}$. In questo caso diventa $J^{P}=\frac{1}{2}^{+}$.
Il caso 2 richiede molta più energia.