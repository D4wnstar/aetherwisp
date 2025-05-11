---
wiki-publish: true
aliases:
  - materia degenere
---
In una [[stella]], due processi principali determinano il suo stato: l'[[irradiazione]] termica verso lo spazio vuoto attorno e il collasso [[Interazione gravitazionale|gravitazionale]] che fa comprimere la stella in risposta. Il [[teorema del viriale]] ci dice che queste due azioni si equilibrano, nel senso che ad ogni perdita di energia per irradiazione segue una contrazione della stella che aumenta l'energia interna. Questo porta ad un progressivo rimpicciolimento della stella.

Questo processo, tuttavia, non può andare avanti all'infinito. Eventualmente, la massa di una stella sufficientemente massiva ($>0.5M_{\odot}$) sarà così compressa dalla sua gravità da non poter esistere in uno stato plasmatico. In queste condizioni estreme, interviene un effetto quantistico detto **pressione degenere**, in genere da parte dagli [[elettrone|elettroni]].
### Derivazione
Prendiamo la [[disuguaglianza di Heisenberg]] in tre dimensioni[^1]:
$$\Delta x\Delta p_{x}>h$$
allora quando il nucleo viene compresso, l'errore sulla posizione naturalmente diminuisce (ci sono meno luoghi possibili in cui gli atomi possono trovarsi). Ma allora deve crescere l'errore sulla quantità di moto. Allora la distribuzione di quantità di moto si allarga. Definiamo un volumetto tridimensionale di volume $h^{3}$ nello [[Phase space]] che rappresenta uno [[stato]] quantistico. Il [[Pauli exclusion principle]] ci dice che in questo volumetto possono esistere in contemporanea al massimo due [[Elettrone|elettroni]], e solo se hanno [[spin]] opposto.

Consideriamo un gas di $n_{e}$ elettroni liberi. Lo spazio delle fasi è tra loro equipartito e ciascuno di essi occupa uno un volume $\Delta x^{3}\simeq1/n_{e}$. Allora, l'incertezza sulla loro posizione è isotropica, dato che il volume è cubico, e vale
$$\Delta x\simeq \frac{1}{n_{e}^{1/3}}=n_{e}^{- 1/3}$$
Quindi l'incertezza su $\Delta p_{x}$ è
$$\Delta p_{x}= \frac{h}{\Delta x}\simeq h n_{e}^{1/3}$$
il che vale a dire che gli elettroni hanno una quantità di moto minima "innata" che tende a respingere gli elettroni circostanti, una sorta di pressione che tende a respingere altri elettroni e che non dipende dalla pressione termica e quindi dalla temperatura. Questo fenomeno si dice **pressione degenere** e la materia che è soggetta a questa pressione è detta **materia degenere**.
#### Temperatura minima
Sebbene non sia dipendente dalla temperatura, la pressione degenere può accadere solo all'interno di materia a temperature sufficientemente basse. Questo deriva dal fatto che, se la materia fosse molto calda, le [[particella|particelle]] costituenti avrebbero energia mediamente più alta, in particolare abbastanza alta da compiere [[Transizione di stato|transizioni di stato]] a stati eccitati. Questo permette alla materia di avere più stati a disposizione per distribuire le particelle e quindi evitare lo stato di pressione degenere.

Cerchiamo allora in che temperature un gas può essere degenere. Definiamo la *densità di stati quantici* come
$$n_{Q}=\left( \frac{2\pi m_{e}k_{B}T}{h^{2}} \right)^{3/2}$$
dove $k_{B}$ è la [[Boltzmann constant]]. Questa è la quantità di stati a disposizione menzionata prima. Più bassa è la temperatura, meno stati si ha. La degenerazione diventa importante quando $n_{Q}$ diventa minore del numero di particelle libere. Nel centro del Sole, ad esempio, vale $n_{Q}\sim3n_{e}$, con $n_{e}$ il numero di elettroni liberi, quindi sebbene la maggior parte degli elettroni non sia degenere, l'effetto non è proprio trascurabile.

Da qui si trova che la temperatura sotto il quale il gas può essere degenere dipende dalla densità
$$\boxed{T_{deg}\propto n_{Q}^{2/3}\propto \rho^{2/3}}$$
#### Caso non relativistico
Ora che abbiamo una stima del momento, possiamo giungere ad una stima della pressione. Nel caso non [[Lorentz transformation|relativistico]], possiamo usare la teoria cinetica dei gas, che ci dice che la pressione è $P=nv_{x}p_{x}$. Usando le stime di indeterminatezza come valori in sé abbiamo
$$P_{deg}\simeq \frac{h^{2}n_{e}^{5/3}}{m_{e}}$$
con $m_{e}$ la massa dell'elettrone.
#### Caso generale
Nel caso generale, possiamo sfruttare il seguente integrale
$$P=\frac{1}{3}\int_{0}^{\infty}n(p)pv\ dp$$
dove $n(p)dp$ è la distribuzione di densità di momento, cioè la quantità di elettroni che hanno momento contenuto in un certo intervallo $[p,p+dp]$. Dato che il momento è quantizzato, si integra su tutti gli stati quantistici.

Dobbiamo trovare che distribuzione usare. Se usassimo la distribuzione di Maxwell-Boltzmann per $n(p)$, troveremmo la ben nota [[equazione di stato dei gas perfetti]]. Purtroppo le condizioni sono troppo estreme per usarla. Sfruttiamo quindi la fisica statistica: gli elettroni sono [[Fermion|fermioni]] e quindi siamo legittimati ad usare la [[Distribuzione di Fermi-Dirac]].

Risolvere l'integrale analiticamente con questa distribuzione è impossibile. Per semplificare, a temperature basse possiamo usare la *condizione di degenerazione*. Si dice che un gas è *degenere* se la sua energia termica $k_{B}T\ll E_{F}$ con $E_{F}$ l'*energia di Fermi*. In questa condizione, tutti gli stati quantistici con energia minore di quella di Fermi sono occupati, mentre nessuno di quelli con energia superiore lo è[^2].

A ciascuno stato di energia è associato un momento. Il momento dello stato all'energia di Fermi si dice *momento di Fermi* $p_{F}$. Questo è quindi il momento massimo che una particella del gas può avere. Allora possiamo usare $p_{F}$ come limite superiore nell'integrale precedente. Il momento di Fermi si calcola come
$$p_{F}=\left( \frac{3n_{e}}{8\pi} \right)^{\frac{1}{3}}h$$
allora considerando due spin per ogni stato ho
$$n_{e}(p)dp=2\cdot4\pi p^{2} \frac{dp}{h^{3}}\quad,\quad p<p_{F}$$
e ricordando $v=p/m_{e}$, l'integrale sarà
$$P_{deg}= \frac{1}{3}\int_{0}^{p_{F}} \frac{2\cdot4\pi p^{2}}{h^{3}}pv\ dp=\frac{1}{3}\int_{0}^{p_{F}} \frac{8\pi p^{4}}{m_{e}h^{3}}dp=\left[ \frac{8}{3}\pi \frac{1}{5} \frac{p^{5}}{m_{e}h^{3}} \right]_{0}^{p_{F}}=$$
$$=\boxed{\frac{1}{5}\left( \frac{3}{8\pi} \right)^{\frac{2}{3}} \frac{h^{2}n_{e}^{\frac{5}{3}}}{m_{e}}}$$
che è l'espressione della pressione degenere per un gas di elettroni. Quindi il nucleo di elio inerte, sostenuto solo dalla pressione degenere, non è affetto in alcun modo dalla temperatura.
#### Caso ultrarelativistico
Può capitare che se la densità di elettroni è altissima, il momento $\Delta p_{x}$ possa diventare ultrarelativistico. Calcolando l'integrale del punto precedente ponendo $v_{x}=c$ si ha
$$P_{ultra}=\frac{1}{4}\left(\frac{3}{8\pi}\right)^{1/3}hcn_{e}^{4/3}$$
che, oltre ad essere meno dipendente dalla densità di stati (4/3 contro 5/3), ha anche la curiosa proprietà di essere completamente indipendente dalla massa della particella in sé.
### Risultati
Raccogliendo i risultati sulla temperatura minima e la pressione in sé, possiamo trarre tre conclusioni:
1. La pressione degenere è inversamente proporzionale alla massa della particella di cui è composto il gas. Più leggera è la particella, più forte è la pressione che produce.
2. È completamente indipendente dalla temperatura, se non per il limite minimo di temperatura degenere.
3. La pressione dipende dalla densità come $P_{deg}\propto n^{5/3}\propto\rho^{5/3}$.

La non-dipendenza dalla temperatura pone una fine al ciclo del teorema del viriale che impone che la stella debba rimpicciolirsi indefinitamente. Una stella degenere, infatti, può teoricamente raffreddarsi fino ad arrivare all'equilibrio termico, come accade nelle [[Nana bianca|nane bianche]].

Questo spesso non accade però. Dato che la pressione non aumenta più all'aumentare della temperatura, non si instaura più il meccanismo di controllo che mantiene la [[fusione nucleare]] ad una certa efficienza. La fusione è quindi instabile nelle stelle degeneri e se si riaccende, essa porta ad un aumento enorme di temperatura, che va avanti fino alla temperatura minima di degenerazione. A quel punto, la stella cessa di essere degenere e torna a bilanciare la propria pressione in funzione dell'energia termica. Ma l'energia accumulata nella fase degenere è talmente alta che viene espulsa tutta in pochissimo tempo in un processo esplosivo. Questo processo non è sufficientemente energetico da essere classificato come [[supernova]], ma può in qualche caso distruggere la stella.

È possibile mostrare l'andamento della densità e della temperatura in un grafico log-log:

![[Grafico Gas degenere|100%|center]]

L'area colorata in azzurro è la fase degenere. Si può vedere che il centro del Sole sia molto vicino ad uno stato degenere. La massa di una stella è (perlopiù) costante, ma la sua densità dipende da quanto gravitazionalmente contratta è. La linea tratteggiata verde rappresenta l'evoluzione di una stella in equilibrio idrostatico per una certa massa $M$, con pendenza $1/3$ ottenuta dalla relazione
$$T_{gas\ perf.}\propto M^{2/3}\rho^{1/3}$$
ottenuta dall'equilibrio idrostatico $P\propto M^{2}/R^{4}$, dal gas perfetto $P\propto \rho T$ e dalla densità $\rho\propto M/R^{3}$. Man mano che la densità cambia, e quindi la temperatura, una stella media salta avanti e indietro tra stati di degeneri e di gas perfetto quando $T_{gas\ perf.}=T_{deg}$, mediante l'innesco della fusione e le esplosioni menzionate prima. Se la fusione non innesca, allora la stella rimane permanentemente in stato degenere a raffreddarsi.
#### Nane brune
La temperatura di transizione da gas perfetto a degenere $T_{gas\ perf.}=T_{deg}$ dipende dalla massa della stella ai 2/3. Per certi oggetti molto leggeri, questa temperatura non è sufficiente per innescare la fusione nucleare dell'idrogeno e non diventeranno mai stelle. Questo limite si trova valere
$$M_{min}=0.08M_{\odot}$$
sotto il quale la temperatura è troppo bassa. La linea tratteggiata verde più bassa è un esempio di tale oggetto: diventa degenere prima ancora di accendersi. Questo oggetti sono detti [[Nana bruna|nane brune]].
#### Limite relativistico
Considerando l'[[Equazioni della struttura stellare#Equilibrio idrostatico|approssimazione di pressione idrostatica]], possiamo esprimerla in funzione della densità
$$P_{idro}\sim M^{2/3}\rho^{4/3}$$
ma questa pressione ha lo stesso andamento in densità della pressione degenere ultrarelativistica. Questo è importante: il rapporto tra pressione idrostatica (necessaria per mantenere una stella) e pressione degenere ultrarelativistica dipende solo e soltanto dalla massa della stella, quindi è possibile che per stelle molto massive nemmeno la pressione degenere ultrarelativistica sia in grado di mantenere la stella. In questo caso, la stella collassa gravitazionalmente. Questo limite, detto [[limite di Chandrasekhar]][^3], vale
$$M_{Ch}=1.44M_{\odot}$$


Il grafico ha un limite destro *relativistico*. Ad una certa massa, la pressione degenere necessaria per evitare che il nucleo collassi richiederebbe particelle con velocità superluminali, cosa impossibile. Dunque, se la massa sale oltre questo limite, la stella collassa *di nuovo*. Questo si chiama **limite di Chandrasekhar**, che è di circa 1.44 masse solari *per il solo nucleo*, non tutta la stella. La linea tratteggiata blu più alta rappresenta questa massa.
#### Pressione di radiazione
Un'ulteriore forma di pressione verso l'esterno è data dalla [[pressione di radiazione]], che vale
$$P_{rad}=\frac{1}{3}\sigma T^{4}$$
con $\sigma$ la [[Stefan-Boltzmann constant]]. L'effetto di questa pressione è quello di destabilizzare la stella, espellendo gli strati esterni (i più leggeri) e quindi rimuovendo massa dalla stella. A sua volta, questo porta ad una diminuzione della pressione.

Rispetto ad un gas perfetto, il rapporto di pressioni vale
$$\frac{P_{rad}}{P_{gas\ perf.}}\propto M^{2}$$
Come per il limite di Chandrasekhar, questo impone un limite: se la pressione di radiazione alta porta ad una diminuzione di massa, ma la diminuzione di massa porta a diminuire la pressione di radiazione, deve esistere un limite di massa superiore oltre il quale la radiazione è troppo forte per permettere ad una stella di crescere oltre. Questo limite è circa
$$M_{max}\sim100M_{\odot}$$

[^1]: Non ho idea del perché Monaco usi questa forma ovviamente sbagliata della disuguaglianza di Heisenberg. Usando la costante non ridotta dovrebbe essere $\hbar/2=h/4\pi$ e quindi $\Delta x\Delta p_{x}>h/4\pi$.
[^2]: Questa condizione vale solo per fermioni.
[^3]: Il limite di Chandrasekhar vale solo per stelle degeneri del tutto prive di idrogeno.