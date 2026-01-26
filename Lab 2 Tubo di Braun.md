Tubo di Braun:
- Usare porta da 6.3 V
- Campo magnetico locale non importante perché tubo in verticale
- Direzione di osservazione non importante perché basta guardare sopra al tubo
- Campo magnetico generato da bobine esterne posizionate manualmente
- Punto luminoso molto fioco, lavorare al buio, attenti con i cavi!
- Usare un foglio trasparente per marcare le posizioni del punto con un pennarello
- Allineare l'asse di simmetria delle bobine con il centro delle piastre
- Una volta trovata la posizione giusta delle bobine, fissare tutto con scotch
- Almeno 4 diverse condizioni ($V_\text{blast}$ e $I_\text{coils}$; $V_\text{cap}$ rimane fisso)
- Data l'imperfetta collimazione del raggio di elettroni, con $B$ acceso il puntino diventa una rosa a causa di moto di ciclotrone. Lunghezza del "petalo" come misura di errore sistematico
- Infine, misurare i campi magnetici $B_\text{coils}$ con sonda Hall per ogni $I_\text{coils}$ usato
- In serie 250 V + 0-250 V per blaster

- $V_\text{blast}$ variabile ma circa $450\text{ V}$.
- $V_\text{cap}$ variable da $10\text{ V}$ a $50\text{ V}$.
- $B$ variabile da $0.08\text{ mT}$ a $0.22\text{ mT}$.
- $D=1.12\text{ cm}$.

Tutti i valori di $B$, nonostante empiricamente, sono sottostime. Questo è perché la formula di $e/m_{e}$ vuole che entrambi i campi siano confinati alla regione tra le piastre. Questo è tutto sommato vero per $E$, ma NON per $B$, che è ampiamente presente al di fuori. Di conseguenza, la deflessione dovuta a $B$ è superiore a quella che sarebbe, a pari intensità, se fosse confinato alle piastre, perché gli elettroni spendono più tempo entro il campo magnetico. Di conseguenza, abbiamo bisogno di intensità magnetiche inferiori per nullificare il campo elettrico, portando a valori di $B$ più bassi rispetto a quando dovrebbero. Ciò porta a sua volta ad una sovrastima sistematica del rapporto $e/m_{e}$.

Per quantificare l'errore sistematico, almeno in prima approssimazione, possiamo compiere il seguente ragionamento. Possiamo trovare il rapporto tra i rapporti sperimentali e quello "reale" consigliato dal CODATA, $e/m_{e}=1.758\text{ C/kg}$. Questo ci dà
$$\frac{(e/m_{e})_\text{exp}}{(e/m_{e})_\text{CODATA}}\equiv r=[0.822, 1.18, 2.1, 1.95, 2.02, 1.9, 2.23, 2.11, 2.6]$$

Le bobine usate per il campo magnetico avevano circa un diametro di $d_\text{bob}=5\text{ cm}$ e $N=10$ giri. La sezione di una bobina era dunque $A_\text{bob}=\pi (d_\text{bob}/2)^{2}=19.6\text{ cm}^{2}$. Come grossolana approssimazione, consideriamo le due bobine come fossero un singolo solenoide infinito con $2N$ giri. In questo caso, il campo magnetico è confinato alla sezione $A_\text{bob}$. Il condensatore, di piastre quadrate, aveva lato $D=1.12\text{ cm}$ e dunque sezione $A_\text{cond}=D^{2}=1.25\text{ cm}^{2}$. Il rapporto tra le due è circa $A_\text{bob}/A_\text{cond}=15.7$. La sezione del campo magnetico era dunque $\sim 15$ volte più grande del dovuto. Di questa sezione, l'elettrone esplora solo una parte minima. Dato che il centro delle bobine era allineato con il centro del condensatore, l'altezza della sezione di $B$ è $d_\text{bob}=5\text{ cm}$. Dunque il percorso medio compiuto da un elettrone all'interno di $B$ è circa $d_\text{bob}$ quando dovrebbe essere circa $D$. Assumendo una velocità costante, ciò implica che l'elettrone spende $d_\text{bob}/D=4.46$ volte più tempo nel campo magnetico di quanto dovrebbe.

![[Drawing 2026-01-08 18.36.52.excalidraw|30%]]






---

Come grossolana approssimazione, possiamo dire che lo sconfinamento del campo magnetico sia responsabile della maggior parte dell'errore; supponiamo il 90%. Allora, possiamo dire che i campi siano stati sottostimati di un fattore $f\equiv0.9s$ e che i campi che ci saremmo dovuti aspettare sarebbero


In assenza di altri errori, random o meno, questo è interpretabile come il rapporto tra il campo magnetico usato e quello che sarebbe dovuto essere usato fosse esso confinato alle piastre, assumendo che tutto l'errore nella misura sia dovuto solo allo sconfinamento del campo magnetico. Moltiplicando i campi usati per questi fattori ci dà
$$B_\text{proper}=[0.06, 0.11, 0.19, 0.23, 0.27, 0.31, 0.38, 0.42, 0.52]$$
rispetto a
$$B_\text{exp}=[0.08, 0.1, 0.1, 0.13, 0.15, 0.18, 0.19, 0.22, 0.22]$$
Fosse il campo stato confinato correttamente, i valori che ci saremmo dovuti aspettare sarebbero stati più simili a $B_\text{proper}$ che a $B_\text{exp}$.