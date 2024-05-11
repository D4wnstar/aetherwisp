---
aliases:
  - buca finita
---
Consideriamo una [[particella]] immersa nel [[potenziale]]
$$V(x)=\begin{cases}
- V_{0} & \text{se }-a<x<a \\
0 & \text{altrove}
\end{cases}$$
con $a$ e $V_{0}$ costanti reali positive. Come per il [[Potenziale delta di Dirac]], sono possibili sia stati legati ($E<0$) e stati liberi ($E>0$).

![[Grafico Buca finita|70%|center]]
### Stati legati
In $x<-a$ il potenziale è zero, quindi l'[[Equazione di Schrödinger]] diventa
$$\frac{d^{2}\psi}{dx^{2}}=- \frac{2mE}{\hbar^{2}}\psi=\kappa^{2}\psi$$
con $\kappa\equiv \sqrt{-2mE}/\hbar$. Come per gli altri casi di questo genere, la soluzione generale è $\psi(x)=Ae^{-\kappa x}+Be^{\kappa x}$, ma il primo termine esplode a $-\infty$, quindi non è normalizzabile, quindi non è fisicamente ammissibile. Allora abbiamo la [[Funzione d'onda]]
$$\psi(x)=Be^{\kappa x}\quad \text{per }x<-a$$
In $-a<x<a$, $V(x)=-V_{0}$, quindi vale
$$- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}} -V_{0}\psi=E\psi \quad \rightarrow \quad \frac{d^{2}\psi}{dx^{2}}=- l^{2}\psi \quad \text{con}\quad l\equiv \frac{\sqrt{2m(E+V_{0})}}{\hbar}$$
$E$ è negativa, ma deve anche essere maggiore di $V_{min}=V_{0}$, quindi $l$ è reale positiva. La soluzione è
$$\psi(x)=C\sin(lx)+D\cos(lx) \quad \text{per }-a<x<a$$
In $x>a$, vale la stessa equazione del primo caso e quindi la soluzione è
$$\psi(x)=Fe^{-\kappa x}\quad \text{per }x>a$$
dato che il termine $Ge^{\kappa x}$ va all'infinito.

Il passo successivo è imporre le condizioni al contorno, ma possiamo risparmiare tempo notando che, dato che il potenziale è pari, allora anche le soluzioni sono o pari o dispari. Ciò ci permette di controllare le condizioni al contorno solo ad un lato. Per il casi pari, cerchiamo una soluzione del tipo
$$\psi(x)=\begin{cases}
Fe^{-\kappa x} & \text{se }x>a \\
D\cos(lx) & \text{se }0<x<a \\
\psi(-x) & \text{se }x<0
\end{cases}$$
La continuità di $\psi(x)$ in $a$ ci dà
$$Fe^{-\kappa a}=D\cos(la)$$
e la continuità della derivata
$$-\kappa Fe^{-\kappa x}=-lD\sin(la)$$
Dividendo la scorsa equazione per quella precedente si ha
$$\kappa=l\tan(la)\tag{1}$$
Dato che sia $\kappa$ che $l$ sono funzioni di $E$, possiamo trovare gli stati permessi dell'energia. Usiamo il cambio di variabile
$$z\equiv l a, \quad z_{0}\equiv \frac{a}{\hbar}\sqrt{2mV_{0}}$$
Usando le definizioni di $\kappa$ ed $l$ troviamo
$$\kappa^{2}+l^{2}=\frac{2mV_{0}}{\hbar^{2}}\quad \rightarrow \quad \kappa a=\sqrt{z_{0}^{2}-z^{2}}$$
che sostituendo nella $(1)$ ci dà
$$\tan(z)=\sqrt{\left(\frac{z_{0}}{z}\right)^{2}-1}$$
Questa è un'equazione trascendentale e quindi non può essere risolta analiticamente. Si tratta di una relazione tra $z$ (e quindi $E$) in funzione di $z_{0}$, che può essere interpretato come la grandezza della buca. Ci sono due casi specifici di particolare interesse.
#### Buca profonda e larga
Se $z_{0}$ è molto grande, le soluzioni si trovano appena sotto $z_{n}=n\pi/2$ con $n$ dispari. Vale allora
$$E_{n}+V_{0}\simeq \frac{n^{2}\pi^{2}\hbar^{2}}{2m(2a)^{2}}$$
Le energie a destra dell'equazione non sono altro che le energie della [[Buca infinita quantistica|buca infinita]] per una buca larga $2a$ (tecnicamente metà, dato che gli $n$ sono solo dispari; le altre provengono dalla funzione d'onda pari). Ma $E+V_{0}$ è l'energia della al di sopra del fondo della buca, quindi per un $V_{0}$ che tende ad infinito la buca finita tende correttamente alla buca infinita. Per ogni $V_{0}$ finito, tuttavia, esistono solo un numero *finito* di stati legati permessi.
#### Buca poco profonda e stretta
Se $z_{0}$ decresce, il numero di stati legati decresce fino a che, quando $z_{0}<\pi/2$, dove lo stato dispari più basso svanisce, non rimane che uno stato. È interessante notare come esiste sempre almeno uno stato, indipendentemente dal potenziale.
### Stati liberi
Troviamo ora gli stati liberi. A sinistra, con $V(x)=0$, si ha
$$\psi(x)=Ae^{ikx}+Be^{-ikx}\quad\text{con}\quad k\equiv \frac{\sqrt{2mE}}{\hbar}$$
Dentro la buca
$$\psi(x)=C\sin(lx)+D\cos(lx)\quad\text{con}\quad l\equiv \frac{\sqrt{2m(E+V_{0})}}{\hbar}$$
e a destra
$$\psi(x)=Fe^{ikx}$$
Qui $A$ è l'ampiezza dell'onda incidente, $B$ è l'ampiezza riflessa e $F$ l'ampiezza trasmessa.

Le condizioni al contorno sono: continuità di $\psi(x)$ in $-a$
$$Ae^{-ika}+Be^{ika}=-C\sin(la)+D\cos(la)$$
continuità della derivata $d\psi/dx$ in $-a$
$$ik[Ae^{-ika}+Be^{ika}]=l[C\cos(la)+D\sin(la)]$$
continuità di $\psi(x)$ in $+a$
$$C\sin(la)+D\cos(la)=Fe^{ika}$$
e continuità di $d\psi/dx$ in $+a$
$$l[C\cos(la)-D\sin(la)]=ikFe^{ika}$$
Come per il potenziale delta di Dirac, possiamo usare due di queste per eliminare $C$ e $D$ e le altre due per determinare $B$ ed $F$:
$$B=i \frac{\sin(2la)}{2kl}(l^{2}-k^{2})F$$
$$F= \frac{e^{-2ika}A}{\cos(2la)-i\frac{k^{2}+l^{2}}{2kl}\sin(2la)}$$
Il coefficiente di trasmissione $T=|F|^{2}/|A|^{2}$, espresso con le variabili originarie, viene da
$$T^{-1}=1 + \frac{V_{0}^{2}}{4E(E+V_{0})}\sin^{2}\left(\frac{2a}{\hbar}\sqrt{2m(E+V_{0})}\right)$$
È notevole il fatto che il coefficiente di trasmissione possa diventare 1 (e lo fa periodicamente). Ciò significa che, per certi valori di energia, una particella passa "sopra" la buca senza caderci dentro. Le energie a cui accade sono quelle per cui $\sin^{2}(\ldots)=0$, ossia
$$\frac{2a}{\hbar}\sqrt{2m(E_{n}+V_{0})}=n\pi$$
con $n$ un intero. Girando l'equazione, le energie di perfetta trasmissione si ottengono da
$$E_{n}+V_{0}=\frac{n^{2}\pi^{2}\hbar^{2}}{2m(2a)^{2}}$$
che, di nuovo, non sono altro che le energie della buca infinita di larghezza $2a$. Questo fenomeno è stato osservato sperimentalmente sotto forma dell'**effetto Ramsauer-Townsend**.