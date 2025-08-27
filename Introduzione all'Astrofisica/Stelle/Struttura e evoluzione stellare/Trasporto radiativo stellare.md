---
wiki-publish: true
---
Considero un elemento di volume cilindro pieno di [[Particle|particelle]] ad una temperatura $T$ all'interno di una [[stella]].

![[Schema Particelle in sezione di gas|center]]

$$\sigma ndx \rightarrow \sigma n dx=1$$
Definisco il [[cammino libero medio]] (*mean free path*) di una particella come
$$l= \frac{1}{\sigma n}$$
dove $\sigma$ è lo [[sezione d'urto]] di [[Diffusione di particelle|diffusione]] e $n$ è il numero di particelle. Se consideriamo tutti i possibili modi $\sigma_{i}$ in cui una particella può fare scattering si ha
$$l= \frac{1}{\sum\limits_{i}n_{i}\sigma_{i}}=\frac{1}{\rho \kappa}$$
dove $\rho$ è la densità della stella e $\kappa$ è l'**opacità**, che rappresenta quanto un gas sia "permissivo" al lasciar passare particelle al suo interno.

Nel caso del Sole, possiamo fare una grossa approssimazione per trovare un numero. Consideriamo solo lo solo gli [[elettrone|elettroni]] per la [[diffusione di Thompson]], la cui sezione d'urto è
$$\sigma_{T}= \frac{8\pi}{3} \frac{e^{2}}{m_{e}c^{2}}$$
e numero di elettroni
$$n_{e}= \frac{\rho}{m_{H}}$$
con $m_{H}$ la massa dell'idrogeno. Allora il cammino libero medio è
$$l= \frac{1}{\sigma n}= \frac{m_{H}}{\rho\sigma_{T}}\simeq 2cm$$
ossia un fotone viaggia approssimativamente per 2 cm all'interno del Sole. Il valore reale, ottenuto con un calcolo molto più preciso, è circa 1 mm.

Per via del numero di particelle e interazioni, il cammino di una particella all'interno del gas stellare è di fatto un cammino casuale (*random walk*). Se vuole andare da un punto A ad uno B, lontani $D$ l'uno dall'altro, lo farà in $N$ cammini liberi casuali
![[Grafico Cammino di una particella|40%|center]]
$$D=l_{1}+l_{2}+l_{3}+\ldots+l_{N}$$
$$D^{2}=|l_{1}|^{2}+|l_{2}|^{2}+\ldots+2(l_{1}\cdot l_{2}+l_{1}\cdot l_{3}+l_{1}\cdot l_{4}+\ldots)$$
Il cammino quadrato medio è
$$\langle D \rangle^{2}=Nl$$
Un cammino libero alla [[velocità della luce]] richiede tempo
$$\tau=\frac{l}{c}$$
Nel caso del Sole, $D=r_{\odot}$ e si ha tempi scala dell'ordine di 52.000 anni, ossia un elettrone ci impiega oltre 50.000 anni ad uscire dal Sole.

Consideriamo un guscio di gas stellare di spessore $\Delta r$ a distanza $L$ dal centro della stella. Se $\Delta r$ è abbastanza fine, possiamo considerarlo come un corpo nero (approssimando). L'energia in eccesso di quel guscio è
$$E_{ecc}=4\pi r^{2}\Delta r\Delta u$$
Il tempo che una particella impiega a attraversare questo guscio è
$$\tau= \frac{(\Delta r)^{2}}{lc}$$
La [[luminosità]] dovuta ai [[Photon|fotoni]] uscenti da quel guscio è
$$L(r)=-\frac{E_{ecc}}{\tau}= - \frac{4\pi r^{2}\Delta r \Delta u}{\frac{\Delta r^{2}}{lc}}=- 4\pi r^{2}lc \frac{\Delta u}{\Delta r}$$
che è un'approssimazione. Il valore reale ottenuto con calcoli più complessi è
$$L(r)=- \frac{4}{3}\pi r^{2}lc \frac{\Delta u}{\Delta r}$$
ossia ha un fattore $\frac{1}{3}$. Possiamo trovare il [[flusso energetico]] come luminosità per area
$$f=\frac{L(r)}{4\pi r^{2}}=\left( - \frac{cl}{3} \right) \frac{du}{dr}$$
dove il termine tra parentesi è il **coefficiente di diffusione** e la derivata è il **gradiente di densità energetica**. Usando la [[legge di Stefan-Boltzmann]] $u= (4\sigma/c) T^{4}=aT^{4}$ si può calcolare la derivata
$$\frac{du}{dr}=\frac{du}{dT} \frac{dT}{dr}=4a T^{3} \frac{dT}{dr}$$
$$\boxed{\frac{dT(r)}{dr}= \frac{3}{4c\pi} \frac{\kappa L(r)\rho(r)}{r^{2}4a T^{3}}}$$
che è la **legge di trasporto energetico radiativo**. Possiamo calcolare la luminosità per il Sole usando $T_{vir,\odot}=4\times10^{6}$ e $l=0.1cm$, che ci dà $L_{\odot}=2\times10^{33}erg/s$. Le misure effettive ci danno $L_{\odot}=3.8\times10^{33}erg/s\sim3.86\times10^{26}W$, un valore tutto sommato simile (ben dentro i margini delle deviazioni standard di queste misure). Per contesto, il consumo energetico globale è nell'ordine dei $10^{12}W$.

Possiamo calcolare la potenza prodotta per unità di massa $\epsilon(r)$ da cui si ha
$$dL=\epsilon(r)dm=\epsilon\rho4\pi r^{2}dr$$
che in forma diversa
$$\boxed{\frac{dL}{dr}=4\pi r^{2}\rho(r)\epsilon(r)}$$
che è la **conservazione di energia** all'interno di una stella.