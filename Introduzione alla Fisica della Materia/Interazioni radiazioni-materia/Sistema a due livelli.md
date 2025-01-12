Consideriamo un sistema con due livelli di energia 1 e 2; l'esatta natura del sistema non è importante. Questo sistema è immerso in un bagno di fotoni, quindi interagisce continuamente con questi. Accadono due processi fondamentali mediati da fotoni.
1. Il fotone può essere **assorbito**, aumentando il livello di energia da 1 a 2.
2. Un fotone può essere **spontaneamente emesso**, diminuendo il livello da 2 a 1.
In entrambi i casi, l'energia del fotone è $h\nu=E_{2}-E_{1}=\Delta E$, con $h$ la [[costante di Planck]] e $\nu$ la frequenza.

Chiamiamo $N_{2}(t)$ il numero di atomi nello stato eccitato. La derivata temporale è
$$\frac{dN_{2}(t)}{dt}=-A_{21}N_{2}(t)$$
con $A_{21}$ la probabilità di emissione spontanea. È un'equazione differenziale che viene risolta da
$$N_{2}(t)=N_{2}(0)e^{-A_{21}t}=N_{2}(0)e^{-t/\tau}\text{ con }\tau=\frac{1}{A_{21}}$$
Possiamo fare il processo inverso. Chiamiamo $N_{1}(t)$ il numero di atomi nello stato fondamentale. La derivata temporale è
$$\frac{dN_{1}(t)}{dt}=-B_{12}N_{1}(t)u(\omega)$$
con $B_{12}$ la probabilità di assorbimento e $u(\omega)$ la densità di energia di illuminazione (ossia quella immagazzinata nel campo in cui è immerso il sistema). La presenza della densità di energia denota che abbiamo bisogno di immettere energia per causare l'aumento di livello; nel caso dell'emissione non serve perché il decadimento è spontaneo.

Nella sua formulazione originale di questo sistema, Einstein postulò la presenza di un terzo processo, detto di **emissione stimolata**, oltre a quella spontanea, dove un fotone esterno presente nel sistema causa l'emissione di un fotone dal sistema. Il fotone esterno *non* viene assorbito. Per questo si ha
$$\frac{dN_{2}(t)}{dt}=-B_{21}N_{2}(t)u(\omega)$$
che, come l'assorbimento, dipende dalla densità di energia $u(\omega)$, oltre che dalla probabilità di emissione stimolata $B_{21}$.

![[Schema processi sistema a due livelli|80%|center]]

Possiamo imporre una condizione di stazionarietà: vale a dire che per ogni fotone che assorbito, statisticamente parlando uno ne viene emesso.
$$B_{12}N_{1}u(\omega)=B_{21}N_{2}u(\omega)+A_{21}N_{2}$$
Posso chiedermi qual è il rapporto tra $N_{1}$ e $N_{2}$.
$$\frac{N_{2}}{N_{1}}=\frac{B_{12}u(\omega)}{B_{21}u(\omega)+A_{21}}\equiv e^{-\hbar\omega/k_{B}T}$$
assumendo che gli stati hanno la stessa [[degenerazione]] e seguano una statistica di un sistema termodinamico. Con un po' di algebra si trova
$$u(\omega)= \frac{A_{21}/B_{21}}{(B_{12}/B_{21})e^{\frac{\hbar\omega}{k_{B}T}}}$$
Se vogliamo prendere il [[Limite termodinamico]] e far tendere $T \rightarrow \infty$, vogliamo che l'energia diverga. Tuttavia, la quantità di energia nel sistema a due livelli è finita: una volta che tutti gli elementi del sistema sono allo stato eccitato, non si può più aumentare l'energia. Dunque, se l'energia deve andare all'infinito, bisogna che l'energia in eccesso vada tutta nel campo. Matematicamente, se $u(\omega) \rightarrow \infty$ bisogna che $B_{12}=B_{21}$, a modo che il denominatore tenda a $0$. Quindi i tassi di emissione devono essere uguali.

Usando termini più generici $A_{21}=A$ e $B_{12}=B_{21}=B$ si calcola
$$u(\omega)=\frac{A}{B}\left(\frac{1}{e^{\hbar\omega/k_{B}T}-1}\right)$$
per $\omega$ piccole possiamo prendere il primo ordine dell'espansione di Taylor
$$u(\omega)\simeq\frac{A}{B}\left(\frac{1}{\frac{\hbar\omega}{k_{B}T}}\right)$$
$$\frac{A}{B}=\frac{\omega^{2}k_{B}T}{\pi^{2}c^{3}} \frac{\hbar\omega}{k_{B}T}=\frac{\hbar\omega^{3}}{\pi^{2}c^{3}}$$
allora
$$u(\omega)\simeq\frac{\hbar\omega^{3}}{\pi^{2}c^{3}}\left(\frac{1}{e^{\hbar\omega/k_{B}T}-1}\right)$$
che è la [[legge di Planck]].
### Oscillazione di un corpo nero
Consideriamo i modi di oscillazione di un [[corpo nero]]
$$k_{x,y,z}=\frac{\pi n_{x,y,z}}{L}$$
ottenuti da un [[Oscillatore armonico]] tridimensionale per un oggetto cubico di lato $L$.

![[Schema modi di oscillazione corpo nero|90%|center]]

Prendiamo il volume occupato da un modo (un cubo di lato $\pi/L$)
$$\frac{1}{8}\underbrace{4\pi k^{2}dk}\limits_{*}\underbrace{\left(\frac{\pi}{L}\right)^{-3}}\limits_{**}2$$
con $*$ l'elemento di volume e $**$ il volume occupato da un modo. Allora la densità di modi è
$$\rho_{k}dk=\frac{k^{2}dk}{\pi^{2}}$$
da cui l'energia dei [[Photon|fotoni]] in funzione della frequenza $\nu$
$$U(\nu)d\nu=\frac{8\pi}{c^{3}}\nu^{2}d\nu k_{B}T$$
con $c$ la [[velocità della luce]] e $k_{B}$ la [[Boltzmann constant]]. Questa si chiama **legge di Riley-Jeans** ed è la spiegazione classica dell'emissione di fotoni in funzione della lunghezza d'onda. Tuttavia, aumenta quadraticamente con la frequenza, il che significa che diverge per frequenze alte, fatto sperimentalmente falso conosciuto come **catastrofe ultravioletta**. Per correggere la legge si è dovuto ricorrere alla fisica quantistica, specificamente alla quantizzazione dell'energia. Allora prendendo
$$E_{n}=nh\nu$$
abbiamo la probabilità che il fotone sia eccitato allo stato $n$-esimo
$$P_{n}=\frac{e^{-E_{n}/k_{B}T}}{\sum\limits_{n}e^{-E_{n}/kt}}=\frac{U^{n}}{\sum\limits_{n}U^{n}}=(1-U)U^{n}\text{ con }U=e^{-h\nu/kT}$$
da cui troviamo il numero medio di fotoni per modo
$$\left\langle n \right\rangle=\sum\limits_{n}nP_{n}=(1-U)\sum\limits_{n}U^{n}=(1-U)U\frac{\partial }{\partial n}\sum\limits_{n}U^{n}=\frac{U}{1+U}=$$
$$=\frac{e^{-h\nu/kT}}{1-e^{-h\nu/kT}}=\frac{1}{e^{-h\nu/kT}-1}$$
e anche l'energia media
$$\left\langle E \right\rangle=h\nu \left\langle n \right\rangle= \frac{h\nu}{e^{-h\nu/kT}-1}$$
quindi ritroviamo l'energia totale immagazzinata in un corpo nero moltiplicando il numero di modi per l'energia per modo
$$U(\nu)=\frac{8\pi}{c^{3}}\nu^{2}\frac{h\nu}{e^{-h\nu/kT}-1}$$
Quindi l'energia ad alte frequenze non tende più a infinito perché diventa dominata dal termine esponenziale. Questa forma quantizzata è sperimentalmente provata.