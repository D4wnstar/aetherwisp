La **fusione nucleare** è il processo per il quale i [[Nucleo atomico|nuclei]] di due [[atomo|atomi]] si fondono fra loro, creando un nuovo atomo combinato. Per accadere richiede temperature e pressioni estremamente alte. Il nucleo delle [[Stella|stelle]], ad esempio, ha le condizioni adatte per far avvenire la reazione, sebbene siano poco efficienti.

La fusione nucleare non produce sempre un surplus di energia. Il processo è energeticamente vantaggioso finché l'[[energia di legame]] per [[nucleone]] del nucleo figlia è superiore a quello dei nuclei madri. Questo è vero fino al ferro ($A=56$). Oltre ad esso, è un deficit netto di energia e dunque non è auto-sostenibile. Ciò significa che la fusione nucleare può produrre elementi solo fino al ferro, mentre per tutti gli elementi più pesanti c'è bisogno di qualche altro processo che produce quantità di energia considerevolmente più grandi.
## Processi
La fusione nucleare può avvenire in diversi modi, in base alla materia prima con cui viene attivata. In quanto segue, si assume che la fusione stia accadendo in una nube di gas a temperatura $T$, come una stella
### Ciclo protone-protone
Il processo più semplice è il **ciclo protone-protone** (o **ciclo PP**) ed avviene a temperature e pressioni relativamente basse. Consiste nel fondere quattro atomi [[protone|protoni]] in un atomo di elio, mediante la catena di reazioni nucleari
$$_{1}^{1}H+\ _{1}^{1}H \rightarrow\ ^{2}_{1}H + e^{+}+\nu_{e}$$
$$_{1}^{2}H+\ _{1}^{1}H \rightarrow\ ^{3}_{2}He+\gamma$$
$$^{3}_{2}He+\ _{2}^{3}He \rightarrow\ ^{4}_{2}He + \ _{1}^{1}H +\ _{1}^{1}H$$
dove $e^{+}$ è un [[Elettrone|positrone]] e $\nu_{e}$ è un [[neutrino]] elettronico. La catena coinvolge neutrini, che hanno [[Sezione d'urto|sezioni d'urto]] estremamente piccole e quindi smorzano l'efficienza di tutto il resto del ciclo.

Questo è il tipo di processo che usano le stelle per la maggior parte della loro vita, come anche le stelle primordiali create poco dopo il [[Big Bang]]. L'efficienza di conversione massa-energia questo processo è $\epsilon\propto \rho T^{4}$[^1] ed è pari a circa 0.7%.
### Ciclo CNO
Un altro processo è il **ciclo CNO**, che usa anche altri elementi, come azoto, ossigeno o carbonio, ma solo come catalizzatori. Infatti, la quantità netta di questi elementi prima e dopo il ciclo è la stessa. Il ciclo CNO richiede pressione e temperature più alte, ma è molti ordini di grandezza più efficiente della catena protone-protone. L'efficienza di questo processo è $\epsilon\propto \rho T^{17}$.

Entrambi i processi coesistono in quasi tutte le stelle, a patto che la loro [[metallicità]] sia abbastanza, alta, ma di solito uno domina sull'altro. Per stelle con temperature centrali $<2\times10^{7}K$ di solito domina il ciclo PP, al di sopra domina il ciclo CNO.
### Ciclo $3\alpha$
Un processo molto più energetico è il **ciclo** $3\alpha$, che coinvolge tre nuclei di $^{4}He$ e una reazione intermedia con il $^{8}Be$ per formare un nucleo di $^{12}C$. Questo è un ciclo a tre corpi e dunque dipende dal cubo della densità, non dal quadrato. Vale $\epsilon\propto \rho^{2}T^{40}$.
### Altri cicli
Esistono cicli ulteriori per atomi più pesanti, che si innescano se la temperatura della stella è sufficientemente alta. In ordine
$$\text{idrogeno} \rightarrow \text{elio} \rightarrow \text{carbonio} \rightarrow \text{neon} \rightarrow \text{ossigeno} \rightarrow \text{silicio}$$
Bruciare il silicio produce nichel, che [[Decadimento nucleare|decade]] in ferro ed è quindi una reazione inefficiente che consuma più energia di quanto ne produce, motivo per cui la catena si ferma lì.
## Condizioni minime
Consideriamo due [[particella|particelle]] cariche $q_{1}$ e $q_{2}$ e massa $m$ che collidono l'un l'altra a velocità $v$. La distanza minima che possono raggiungere a causa delle barriere di [[potenziale]] è data dalla [[Interazione elettromagnetica|legge di Coulomb]]
$$r=\frac{2q_{1}q_{2}}{mv^{2}}$$
(in cgs il termine $4\pi\epsilon_{0}$ non compare). Per portare questa distanza ad essere minore del raggio del nucleo ($\sim10^{-15}$ m), le velocità dovrebbero essere enormi. Talmente alte, infatti, che non si trovano nemmeno nel centro di una stella come il Sole.

Fortunatamente, la meccanica quantistica permette un modo per bypassare la barriera di potenziale: il [[tunnelling quantistico]]. Per una barriera elettromagnetica di questo genere, si trova che la probabilità di trasmissione è
$$P_{tunnel}\propto\exp\left(- \frac{2\pi^{2}r}{\lambda}\right)$$
con $\lambda$ la [[Formula di de Broglie|lunghezza d'onda di De Broglie]]. Dato che $\lambda$ diminuisce con $p$ e quindi con $v$, questa probabilità aumenta all'aumentare della velocità.

Nel contesto di stelle, o comunque gas ad una certa temperatura $T$, possiamo assumere che le velocità delle particelle del nucleo stellare siano distribuite secondo una [[distribuzione di Maxwell]]. La probabilità di avere una velocità sufficientemente alta si dimostra avere la forma
$$P_{maxwell}\propto\exp\left(- \frac{mv^{2}}{2k_{B}T}\right)$$
con $k_{B}$ la [[costante di Boltzmann]]. La probabilità di fusione totale è dunque il prodotto $P_{tunnel}P_{maxwell}$. Si dimostra che la probabilità è massimizzata per velocità
$$v=\left(\frac{2\pi q_{1}q_{2}k_{B}T}{\hbar m}\right)^{1/3}$$
con $\hbar$ la [[Costante di Planck|costante di Planck ridotta]]. Le condizioni minime per accendere il reattore a fusione nel nucleo allora sono
$$\boxed{P_{reaz}\propto \exp\left(- \left( \frac{T}{T_{0}} \right)^{-1/3}\right)}$$
$$ T_{0} = \left( \frac{3}{2} \right)^{3}\left( \frac{4\pi^{2}q_{1}q_{2}}{h} \right)^{2}\left( \frac{m}{k_{B}} \right)$$
dove $T_{0}$ è una temperatura di scala. $m$ in questo caso è la massa ridotta $m=m_{1}m_{2}/m_{1}+m_{2}$, dato che il nucleo è composto da particelle diverse (idrogeno, elio, etc...).
### Considerazioni
Da questa equazione si possono fare alcune considerazioni:
- $T_{0}$ cresce come $m(q_{1}q_{2})^{2}$, il che vale a dire che il cresce come $AZ^{4}$ in termini di [[Atomo|numero di massa atomica]] e [[Atomo|numero atomico]]. La temperatura minima cresce molto rapidamente usando atomi più pesanti dell'idrogeno.
- Anche per l'idrogeno $T_{0}$ è molto alta: con $q_{1}=q_{2}=e$ e $m=m_{p}/2$ si ha $T_{0}=3.8\times10^{10}$ K. Poche stelle hanno temperature interne così alte. Il Sole, ad esempio, ha temperatura intera di $1.5\times10^{7}$ K. La fusione nucleare accade quindi con probabilità molto bassa e, dunque, molto lentamente.
- L'efficienza della reazione cresce molto rapidamente con la temperatura. Reattori a temperatura più alta produrranno esponenzialmente più energia che reattori a temperatura più bassa.
## Creazione di elementi
Nel contesto dell'astrofisica e della cosmologia, è comodo classificare gli elementi della tavola periodica in base alla loro origine. Gli elementi molto leggeri, $H$, $^{2}H$, $^{3}He$, $He$ e $Li$ hanno tutti **origine cosmologica** e quindi esistono sin dal Big Bang. Questi sono gli elementi che danno inizio alla fusione nucleare delle stelle.

Si definiscono successivamente **elementi primari** quegli elementi che sono creati dalla fusione nucleare direttamente dagli elementi di origine cosmologica, mentre **elementi secondari** quelli creati da elementi pesanti già esistenti (come gli elementi primari prodotti da cicli meno energetici). Ad esempio, il $He$ è un elemento primario (oltre che cosmologico) perché prodotto dal $H$ nel ciclo PP, mentre il $N$ è un elemento secondario perché prodotto dal $C$ nel ciclo CNO.

Gli elementi secondari si spingono fino al $Fe$, oltre il quale la fusione nucleare spontanea non avviene. Di conseguenza, gli elementi più pesanti si devono formare tramite processi più energetici ed efficienti, come il [[processo s]] o il [[processo r]], o più rapidi e violenti, come una [[supernova]].

[^1]: Se la generazione di energia *totale* dipende da $\rho^{2}$, come accade in genere, la generazione di energia *per unità di massa* $\epsilon$ dipende solo da $\rho$.