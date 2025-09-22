---
wiki-publish: true
aliases:
  - massa di Jeans
---
La **formazione stellare** è il processo per cui il [[Mezzo interstellare]] si aggrega per formare una [[Stella]]. Ad oggi, è il punto meno compreso dell'[[Evoluzione stellare]] e si basa principalmente sulla fisica dell'ISM e delle sue fasi.
## Fasi di formazione
### Inizio del collasso
La formazione stellare inizia in una [[Nube molecolare]], una nuvola di ISM in fase molecolare. Se il [[Gravity|potenziale gravitazionale]] $\Omega$ di questa nube è sufficiente da superare la sua energia termica $K$, la nube comincia a contrarsi. In altre parole, l'energia totale della nube deve essere negativa (dato che il [[Potential]] è convenzionalmente negativo):
$$K+\Omega<0$$

Consideriamo una nube di [[gas perfetto]], per semplicità uniforme, con un volume sferico di raggio $R$, $V=4\pi R^{3}/3$, densità $\rho=M/V$ e peso molecolare $\mu$. L'energia termica $K$ e quella gravitazionale $\Omega$ sono
$$K=\frac{3}{2}k_{B} \frac{TM}{\mu m_{p}}\quad;\quad \Omega=-\frac{GM^{2}}{R}$$
con $k_B$ la [[Boltzmann constant]], $m_{p}$ la massa del [[protone]] e $G$ la [[Gravitational constant]]. Dunque, per il collasso deve essere
$$\frac{3}{2}k_{B} \frac{TM}{\mu m_{p}}- \frac{GM^{2}}{R}<0$$
Il raggio è
$$R=\left( \frac{3V}{4\pi} \right)^\frac{1}{3}=\left( \frac{3M}{4\pi \rho } \right)^{\frac{1}{3}}$$
e raccogliendo $M$ e sostituendo $R$:
$$M \left( \frac{3}{2}k_{B} \frac{T}{\mu m_{p}}- GM \left(\frac{3M}{4\pi\rho}\right)^{-1/3} \right)<0$$
La $M$ è positiva quindi la possiamo trascurare
$$\frac{3}{2} \frac{k_{B}T}{\mu m_{p}}- GM \left( \frac{3M}{4\pi\rho} \right)^{- \frac{1}{3}}<0$$
$$\frac{3}{2} \frac{k_{B}T}{\mu m_{p}}-G \left( \frac{3}{4\pi\rho} \right)^{- \frac{1}{3}}M^\frac{2}{3}<0$$
$$\boxed{M> \left( \frac{3}{2} \frac{k_{B}T}{G\mu m_{p}} \right)^{\frac{3}{2}} \left( \frac{3}{4\pi\rho} \right)^{\frac{1}{2}}}$$
che è la massa minima necessaria per una nube per cominciare il collasso. Il valore che satura questa disequazione è detto **massa di Jeans**. Mettendo le costanti numeriche
$$M_{J}=15.4M_{\odot} \left( \frac{T}{1K} \right)^{\frac{3}{2}}\mu^{-2} \left( \frac{n}{cm^{-3}} \right)^{-\frac{1}{2}}$$
con $M_{\odot}$ la [[Massa solare]]. Come vediamo, la massa di Jeans aumenta con la temperatura.

> **Risultato.** Più calda è una nube molecolare, più massiva deve essere per iniziare la formazione stellare. Per questo, sono sempre le nubi più fredde a diventare zone di formazione stellare.
### Collasso
Generalmente, quando una nube collassa, l'aumento della densità diminuisce la massa di Jeans e ciò fa si che sezioni più piccole *interne* alla nube comincino esse stesse a collassare, più in fretta della nube totale. Di conseguenza, invece di collassare in una singola stella con la massa di tutta la nube, si creano molte stelle più piccoli che hanno solo la massa di una piccola parte della nube. Questo fenomeno si chiama **frammentazione gerarchica**.

![[Schema Frammentazione gerarchica|center]]

Una stella che ha cominciato il collasso e che ha cominciato ad aumentare la sua temperatura si chiama [[protostella]], e non è ancora una stella vera e propria in quanto non ha ancora processi interni. Attorno ad esse vi sono [[disco di accrescimento|dischi di accrescimento]] da cui accumulano massa. Le protostelle sono un tipo di [[Young Stellar Object]]. La stella diventa tale solo quando comincia la [[Nuclear fusion]] dell'idrogeno all'interno del suo nucleo.
#### Dissipazione del momento angolare
Non basta semplicemente collassare per far sì che una nube diventi una stella. Il momento angolare tipico di una stella è molto minore di quello di una nube ($\sim10^{17}$ contro $\sim10^{24}$) quindi c'è bisogno di dissipare una grande quantità di momento angolare per far sì che il gas non diventi un disco, come per esempio accade in una [[Galassia]].

Una parte del momento è perso nella frammentazione gerarchica, ma non abbastanza. Un'altra parte si trova nel [[Disco protoplanetario]] di alcune stelle, ma la massa del disco è trascurabile. Deve esserci quindi un altro modo importante di dissipazione.

Questo modo è mediante i campi magnetici. Il plasma della nube, essendo elettricamente carico, emette un tenue campo magnetico nell'ordine dei microgauss. In un plasma, il campo magnetico rimane congelato con il gas, quindi il campo si oppone alla rotazione e trasporta momento angolare dalla protostella verso l'esterno. Nel girare attorno ad un campo magnetico, *piega* le linee magnetiche in una direzione. Per fare ciò, consuma energia che viene tolta dall'energia cinetica, agendo praticamente come *attrito magnetico*. Questo fenomeno si chiama **magnetic braking**.

![[Schema Rallentamento magnetico|100%|center]]
### Contrazione
Nel perdere momento angolare, la protostella si contrae sempre di più. A differenza di una stella "viva", questo processo non è governato dal [[Teorema del viriale]]. Infatti, la nube è otticamente sottile e quasi tutta l'energia termica viene [[irradiazione|irradiata]] verso l'esterno, quindi può continuare a collassare e accumulare potenziale gravitazionale. La fase di contrazione dura circa un [[Tempo dinamico]], che è nell'ordine dei milioni di anni per ISM in fase molecolare.

La contrazione tende a formare un nucleo più denso. Ad un certo punto, il gas diventa abbastanza denso da diventare opaco. A questo punto, l'irradiazione di energia diventa inefficiente ed entra in gioco il teorema del viriale, ponendo la protostella in quasi-equilibrio idrostatico. A questo punto, il nucleo si contrae sul [[Tempo scala di Kelvin-Helmholtz]]. Nel frattempo, la nube attorno alla protostella diventa una [[Regione H II]] ed emette nell'infrarosso lontano, assorbendo nell'ottico e nell'UV. Ciò rende difficile individuare le protostelle finché queste non producono venti stellari abbastanza forti da dissipare la nube.

Le protostelle sono completamente [[convezione|convettive]], fredde, molto grandi e molto luminose. Cominciano tutte sul lato destro del [[Diagramma Hertzsprung-Russell|diagramma HR]], al [[Limite di Hayashi]], per poi avvicinarsi alla [[Sequenza principale]] a età zero (ZAMS). Questa fase si dice **fase di presequenza** e osservativamente sono simili alle [[gigante rossa|giganti]], ma a sono distinguibili perché occupano una parte molto precisa del diagramma, sono sempre circondate da spesse nubi di gas e polvere, hanno [[Spettro (astrofisica)|spettri]] peculiari con forti [[Riga spettrale|righe di emissione]] e allargamenti per venti stellari. Cambiano anche la loro [[Luminosità]] molto rapidamente. Presentano talvolta anche una grande quantità di litio, fatto strano dato che di solito viene consumato nella fusione.

![[Grafico Evoluzione protostelle|90%|center]]
