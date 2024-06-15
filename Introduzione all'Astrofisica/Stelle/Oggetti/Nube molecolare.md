Le **nubi molecolari** sono luoghi dell'universo in cui c'è una densità di massa molto più alta che nel resto dell'universo. Come suggerisce il nome, ci si trovano solo molecole libere, principalmente di idrogeno. La densità è nell'ordine delle 1000 molecole per centimetro cubo, mentre la temperatura si aggira attorno ai 10 K. Se l'energia gravitazionale della nube è abbastanza forte, la nube può collassare su se stessa e cominciare la formazione di una [[Stella|stella]]. Solo il 2/3% delle nubi molecolari si trasforma in stelle.
## Massa di Jeans
Prendiamo un volume sferico di raggio $R$, $V=4\pi R^{3}/3$ e $\rho=M/V$. Le energie che ci interessano sono quella termica $K$ e quella gravitazionale $\Omega$
$$K=\frac{3}{2}k_{B} \frac{TM}{\mu m_{p}}\quad;\quad \Omega=-\frac{GM^{2}}{R}$$
con $k_B$ la [[costante di Boltzmann]] e $m_{p}$ la massa del protone. Se l'energia gravitazionale è maggiore a quella termica, la nube comincia a collassare su sé stessa e comincia la formazione di una stella. Dunque la condizione per l'inizio della formazione stellare è
$$\boxed{K+\Omega<0}$$
sostituendo le formule precedenti
$$\frac{3}{2}k_{B} \frac{TM}{\mu m_{p}}- \frac{GM^{2}}{R}<0$$
Il raggio è
$$R=\left( \frac{3V}{4\pi} \right)^\frac{1}{3}=\left( \frac{3M}{4\pi \rho } \right)^{\frac{1}{3}}$$
dunque
$$M \left( \frac{3}{2}k_{B} \frac{T}{\mu m_{p}}- \frac{GM}{R} \right)<0$$
togliendo la $M$ dato che è positiva
$$\left( \frac{3}{2} \frac{k_{B}T}{\mu m_{p}}- GM \left( \frac{3M}{4\pi\rho} \right)^{- \frac{1}{3}} \right)<0$$
$$\frac{3}{2} \frac{k_{B}T}{\mu m_{p}}-G \left( \frac{3}{4\pi\rho} \right)^{- \frac{1}{3}}M^\frac{2}{3}<0$$
$$\boxed{M_{J}> \left( \frac{3}{2} \frac{k_{B}T}{G\mu m_{p}} \right)^{\frac{3}{2}} \left( \frac{3}{4\pi\rho} \right)^{\frac{1}{2}}}$$
che è la **massa di Jeans**. Mettendo le costanti numeriche
$$M_{J}=15.4M_{\odot} \left( \frac{T}{1K} \right)^{\frac{3}{2}}\mu^{-2} \left( \frac{n}{cm^{-3}} \right)^{-\frac{1}{2}}$$
con $M_{\odot}$ la massa solare.

## Frammentazione gerarchica
Generalmente, quando una nube collassa, l'aumento della densità fa si che sezioni più piccole *interne* alla nube comincio esse stesse a collassare, più in fretta della nube totale. Di conseguenza, invece di collassare in una singola stella con la massa di tutta la nube, si creano molte stelle più piccoli che hanno solo la massa di una piccola parte della nube. Questo fenomeno si chiama **frammentazione gerarchica**.

![[Frammentazione gerarchica|center]]
Una stella che ha cominciato il collasso e che ha cominciato ad aumentare la sua temperatura si chiama **protostella**, e non è ancora una stella vera e propria in quanto non ha ancora processi interni. Attorno ad esse vi sono **dischi di accrescimento** da cui accumulano massa. Le protostelle sono un tipo di **Young Stellar Object** (**YSO**). La stella diventa tale solo quando comincia la [[Fusione nucleare]] all'interno del suo nucleo.
## Dissipare momento angolare
Per far sì che il collasso avvenga correttamente c'è bisogno di dissipare molto del momento angolare che agisce sul gas, altrimenti non è verificata la condizione per l'inizio di formazione stellare. Un modo in cui un *plasma* in particolare dissipa il momento angolare è il caso in cui è immerso in un campo magnetico. Il plasma, essendo elettricamente carico, nel girare attorno ad un campo magnetico, *piega* le linee magnetiche in una direzione. Per fare ciò, consuma energia che viene tolta dall'energia cinetica, agendo praticamente come *attrito magnetico*. Questo fenomeno si chiama **magnetic braking**.

![[Rallentamento magnetico|100%|center]]

