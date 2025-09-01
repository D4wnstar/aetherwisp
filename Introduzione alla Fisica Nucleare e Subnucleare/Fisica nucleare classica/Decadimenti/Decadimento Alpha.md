---
wiki-publish: true
aliases:
  - particella alpha
---
Il **decadimento $\alpha$** è un tipo di [[Decadimento nucleare|decadimento]] nel quale un [[Nuclide]] emette una *particella $\alpha$*, ossia un [[Atomic nucleus|nucleo]] di elio $_{2}^{4}\text{He}_{2}$. Il nucleo rilasciato è molto legato (infatti è [[Magic number|doppiamente magico]]), quindi l'energia cinetica rilasciata è massimizzata. Il processo di decadimento è
$$_{Z}^{A}X_{N} \rightarrow\ _{Z-2}^{A-4}X'_{N-2}+\alpha$$
dove $X$ e $X'$ sono simboli chimici di specie nucleari diverse nello stato iniziale e finale. Il numero di protoni e neutroni deve conservarsi separatamente. L'energia cinetica tipica della particella $\alpha$ emessa è nell'ordine dei [[Electronvolt|MeV]].

Il decadimento $\alpha$ è mediato dall'[[Strong interaction]].

Una reazione tipo è
$$_{88}^{226}\text{Ra}_{138}\rightarrow\, _{86}^{222}\text{Rn}_{136}+\,_{2}^{4}\text{He}_{2}$$
che ha un [[Legge di decadimento radioattivo|tempo di dimezzamento]] di 1600 anni e la particella $\alpha$ ha un'energia cinetica di $4.8$ MeV.
## Meccanismo
Protoni e neutroni hanno [[Binding energy]] attorno agli 8 MeV, quindi non possono scappare dal nucleo se non in condizioni particolare. Può però succedere che l'emissione di un gruppo di nucleoni sotto forma di un sistema legato $^{4}\text{He}$ sia energeticamente favorita.

Studiamo l'energia [[Potential]] $V(r)$ di una particella $\alpha$ in funzione della distanza $r$ dal nucleo

![[Grafico Decadimento Alpha|80%|center]]
A piccole distanze, l'interazione forte domina e si forma una buca di potenziale profonda $-V_{0}$.

A grandi distanze, la particella $\alpha$ è soggetta a [[Electromagnetism|repulsione Coulombiana]] dei protoni, come si vede in $V_{C}$. $Z$ è il [[Atom|numero atomico]] del nucleo, $Z-2$ è il numero dopo il decadimento $\alpha$.
- $Q$ è l'energia di disintegrazione.
- In $r<a$ si ha una buca di potenziale dovuta all'interazione forte. L'unico modo che la particella $\alpha$ ha per uscirne (o entrarne, nel caso della [[fissione spontanea]]) è mediante [[tunnelling quantistico]].
- In $a<r<b$ si forma una seconda barriera di potenziale perché l'energia potenziale supera quella disponibile $Q$. $\alpha$ non può entrare in questa regione.
- La regione $r>b$ è quella normale fuori dalla barriera.

Chiamiamo **costante di disintegrazione** $\lambda$ di un emettitore $\alpha$
$$\lambda=fP\text{ con }f\sim \frac{v}{a}$$
dove $f$ è la frequenza con cui $\alpha$ si presenta alla barriera, $P$ è la probabilità di trasmissione oltre la barriera e $v$ è la velocità della particella $\alpha$ sulla barriera.

La barriera di potenziale Coulombiano ha altezza $C$ per $r=a$ data da
$$C=\frac{1}{4\pi\epsilon_{0}} \frac{2(Z-2)e^{2}}{a}$$
per $\alpha$ con carica $2e$ e nucleo figlia con carica $(Z-2)e$. L'altezza della barriera varia da $C-Q$ in $r=a$ a 0 in $r=b$, quindi consideriamo il valor medio $\frac{1}{2}(C-Q)$. Considero anche la larghezza media $d=\frac{1}{2}(b-a)$.

Per comprendere il fenomeno, si può guardare la trattazione della [[Buca infinita quantistica]]. Dobbiamo risolvere l'[[equazione di Schrödinger]] in una dimensione per una particella sottoposta ad una barriera di potenziale $V(x)$. Consideriamo l'[[Equazione agli autovalori|autostato]] $\psi$. Allora
$$\frac{\hbar^{2}}{2m} \frac{d^{2}\psi(x)}{dx^{2}}+V(x)\psi(x)=E\psi(x)$$
A causa della barriera di potenziale, abbiamo tre soluzione per tre regioni dello spazio, determinate dalle condizione al contorno:
- $V(x)=0$ per $x<0$ ci dà $\psi_{1}(x)=Ae^{ik_{1}x}+Be^{-ik_{1}x}$
- $V(x)=V_{0}$ per $0\leq x\leq a$ ci dà $\psi_{2}(x)=Ce^{k_{2}x}+De^{-k_{2}x}$
- $V(x)=0$ per $x>a$ ci dà $\psi_{3}(x)=Ee^{ik_{3}x}+Fe^{-ik_{3}x}$
dove
$$k_{1}=k_{3}=\sqrt{\frac{2mE}{\hbar^{2}}}\quad;\quad k_{2}=\sqrt{\frac{2m(V_{0}-E)}{\hbar^{2}}}$$
Possiamo chiamare $P$ la probabilità di trasmissione
$$P=\frac{j_{trasmesso}}{j_{incidente}}$$
con $j_{trasmesso}$ la corrente di probabilità nell'onda trasmessa e $j_{incidente}$ la corrente nell'onda incidente. Quindi $P$ è la frazione della corrente incidente e trasmessa oltre la barriera. Si ha
$$P=\frac{1}{1+ \frac{1}{4} \frac{V_{0}^{2}}{E(V_{0}-E)}\sinh^{2}(k_{2}a)}$$
Con un nucleo possiamo scrivere
$$k_{2}=\sqrt{\frac{2m}{\hbar^{2}} \frac{1}{2}(C-Q)}$$
Per un nucleo pesante si ha $Z=90$, $a=7.5$ fm, $C\simeq34$ MeV e usando
$$b=\frac{1}{4\pi\epsilon_{0}} \frac{zZ'e^{2}}{Q}$$
possiamo ricavare il raggio a cui lascio la barriera. Per $Q\sim6$ MeV, si ha $b\sim42$ fm. Il valore di $b$ e di $P$ è molto sensibile a quello di $Q$, quindi anche piccole variazioni in questo possono causare cambiamenti di diversi ordini di grandezza del [[Legge di decadimento radioattivo|tempo di dimezzamento]] dei nuclidi che decadono $\alpha$.
## Conservazione dell'energia
Se assumo che il nucleo originario $X$ sia a riposo, allora l'energia iniziale del sistema è $m_{X}c^{2}$. Lo stato finale è costituito da $X'$ e $\alpha$, entrambi in moto in modo da conservare l'impulso lineare. L'energia finale è dunque
$$m_{X'}c^{2}+T_{X'}+m_{\alpha}c^{2}+T_{\alpha}$$
con $T$ l'energia cinetica. Per conservazione dell'energia
$$m_{X}c^{2}=m_{X'}c^{2}+T_{X'}+m_{\alpha}c^{2}+T_{\alpha}$$
$$\Rightarrow (m_{X}-m_{X'}-m_{\alpha})c^{2}=T_{X'}+T_{\alpha}$$
Il [[Q-valore]] questo caso vale
$$Q=(m_{X}-m_{X'}-m_{\alpha})c^{2}$$
dato che la particella $\alpha$ ha massa nota, le altre due masse sono calcolabili direttamente da tabelle contenenti le masse atomiche (le masse degli elettroni si annullano). Ricordando che la [[velocità della luce]] vale $931.5$ MeV/u e che le masse atomiche non vanno oltre le centinaia, si vede che $Q$ è nell'ordine dei MeV.

Il Q-valore può anche essere espresso come
$$Q=T_{X'}+T_{\alpha}$$
e dalla conservazione dell'impulso ho $p_{\alpha}=p_{X'}$. Sapendo che $\alpha$ tipicamente rilascia 5 MeV, sia $T_{X'}$ che $T_{\alpha}$ sono $\ll mc^{2}$, quindi posso usare la cinematica classica senza grande errore. Ho $T=p^{2}/2m$ e
$$T_{\alpha}=\frac{Q}{1+ \frac{m_{\alpha}}{m_{X'}}} \quad \text{con} \quad \frac{m_{\alpha}}{m_{X'}}\ll1$$
nel caso di un nucleo pesante. Semplificando, si ottiene
$$T_{\alpha}=\frac{Q}{1 + \frac{4}{A}} \quad \text{per} \quad A\gg 4\left(\frac{m_{\alpha}}{m_{X'}}\sim \frac{4}{A-4}\right)$$