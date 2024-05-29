Il **decadimento $\alpha$** è un tipo di [[Decadimento]] nel quale un [[nuclide]] emette una *particella $\alpha$*, ossia un [[Nucleo atomico|nucleo]] di elio $_{2}^{4}\text{He}_{2}$. Il nucleo rilasciato è molto legato, quindi l'energia cinetica rilasciata è massimizzata. Il processo di decadimento è
$$_{Z}^{A}X_{N} \rightarrow _{Z-2}^{A-4}X'_{N-2}+\alpha$$
dove $X$ e $X'$ sono simboli chimici di specie nucleari diverse nello stato iniziale e finale. Il numero di protoni e neutroni deve conservarsi. L'energia cinetica tipica di una tale reazione è nell'ordine dei [[Elettronvolt|MeV]].

Una reazione tipo è
$$_{88}^{226}Ra_{138}\rightarrow _{86}^{222}Rn_{136}+_{2}^{4}He_{2}$$
che ha un tempo di dimezzamento di 1600 anni e la particella $\alpha$ ha un'energia cinetica di $4.8$ MeV.
## Meccanismo
Protoni e neutroni hanno [[energia di legame]] attorno agli 8 MeV, quindi non possono scappare dal nucleo. Può però succedere che l'emissione di un gruppo di nucleoni sotto forma di un sistema legato sia energeticamente favorita.

Studiamo l'energia potenziale $V(r)$ di una particella $\alpha$ in funzione della distanza $r$ dal nucleo

![[Grafico Decadimento Alpha|80%|center]]
A grandi distanze, $\alpha$ è soggetta a repulsione Coulombiana dei protoni, come si vede in $V_{C}$. $Z$ è il numero atomico del nucleo, $Z-2$ è il numero dopo il decadimento $\alpha$.
- $Q$ è l'energia di disintegrazione.
- In $r<a$ si ha una buca di potenziale che rappresenta l'interno del nucleo. La barriera di potenziale è alta $-V_{0}$. In meccanica classica, il nucleone può muoversi dentro questa buca, ma non può uscirne.
- In $a<r<b$ si forma una seconda barriera di potenziale perché l'energia potenziale supera quella disponibile $Q$. $\alpha$ non può entrare in questa regione.
- La regione $r>b$ è quella normale fuori dalla barriera.
L'unico modo che la particella $\alpha$ ha per entrare o uscire dal nucleo è tramite il [[tunneling quantistico]].

Chiamiamo *costante di disintegrazione* $\lambda$ di un emettitore $\alpha$
$$\lambda=fp\text{ con }f\sim \frac{v}{a}$$
dove $f$ è la frequenza con cui $\alpha$ si presenta alla barriera, $p$ è la probabilità di trasmissione oltre la barriera e $v$ è la velocità della particella $\alpha$ sulla barriera.

Per comprendere il fenomeno, dobbiamo risolvere l'[[equazione di Schrödinger]] in una dimensione per una particella sottoposta ad una barriera di potenziale $V(x)$. Consideriamo l'[[autostato]] $\psi$. Allora
$$\frac{\hbar^{2}}{2m} \frac{d^{2}\psi(x)}{dx^{2}}+V(x)\psi(x)=E\psi(x)$$
A causa della barriera di potenziale, abbiamo tre soluzione per tre regioni dello spazio, determinate dalle condizione al contorno:
- $V(x)=0$ per $x<0$ ci dà $\psi_{1}(x)=Ae^{ik_{1}x}+Be^{-ik_{1}x}$
- $V(x)=V_{0}$ per $0\leq x\leq a$ ci dà $\psi_{2}(x)=Ce^{k_{2}x}+De^{-k_{2}x}$
- $V(x)=0$ per $x>a$ ci dà $\psi_{3}(x)=Ee^{ik_{3}x}+Fe^{-ik_{3}x}$
dove
$$k_{1}=k_{3}=\sqrt{\frac{2mE}{\hbar^{2}}}\quad;\quad k_{2}=\sqrt{\frac{2m(V_{0}-E)}{\hbar^{2}}}$$
Possiamo chiamare $P$ la probabilità di trasmissione
$$P=\frac{j_{trasmesso}}{j_{incidente}}$$
con $j_{trasmesso}$ la corrente nell'onda trasmessa e $j_{incidente}$ la corrente nell'onda incidente. Quindi $P$ è la frazione della corrente incidente e trasmessa oltre la barriera. Si ha
$$P=\frac{1}{1+ \frac{1}{4} \frac{V_{0}^{2}}{E(V_{0}-E)}\sinh^{2}(k_{2}a)}$$
In meccanica classica, $P=0$, quindi penetrare la barriera è impossibile. L'onda quantistica invece può penetrare la barriera con probabilità $P$, fenomeno detto *tunnelling quantistico*.
## Conservazione dell'energia
non so, farò prima o poi
