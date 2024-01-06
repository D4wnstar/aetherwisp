Una **singolarità isolata** per una funzione ad argomento complesso $f(z)$ è un punto isolato di [[funzione olomorfa|non-olomorfia]] entro il dominio della funzione. Si distinguono tre tipi.
### Singolarità removibili
Sono singolarità "finte", nel senso che è sempre possibile prolungare la funzione per continuità sulla singolarità in modo da renderla olomorfa anche in quel punto. Un esempio è $f(z)=\frac{\sin(z)}{z}$ in $z=0$, dove è prolungabile dichiarando $f(0)=1$.

Una singolarità in $z_{0}$ è removibile se esiste finito il limite della funzione in quel punto, ovvero esiste $l$ finito tale che
$$\lim\limits_{z \rightarrow z_{0}}f(z)=l$$
Allora definendo $f(z_{0})=l$ si è prolungata la funzione per continuità e la funzione è olomorfa anche in $z_{0}$. Più in generale, è vero che se la funzione $f(z)$ è limitata in un intorno di $z_{0}$, allora si tratta di una singolarità removibile. In simboli, se esiste $M$ costante tale che, per ogni punto di un intorno $I$ di $z_{0}$ escluso $z_{0}$, vale
$$|f(z)|\leq M$$
allora si può definire $f(z_{0})$ in modo che la funzione sia olomorfa in $z_{0}$.
### Poli
Un **polo** in $z_{0}$ è una singolarità isolata determinata dalla presenza di un numero *finito* di potenze negative nell'espansione in [[serie di Laurent]] della funzione in un intorno di $z_{0}$. Si dice **ordine** del polo tale numero di potenze negative. Ad esempio,  la funzione
$$f(z)=\frac{z^{2}}{1+z^{4}}$$
ha quattro poli di primo ordine nelle radici di $1+z^{4}$. Ogni funzione razionale della forma $f(z)=P(z)/Q(z)$ dove $P(z),Q(z)$ sono polinomi presenta poli nei punti in cui $Q(z)=0$ con ordine pari alla molteplicità degli zeri.

Vi sono tre possibili condizioni necessarie e sufficienti per l'esistenza di un polo di ordine $n$ in $z_{0}$ per una funzione $f(z)$:
1. esiste finito il limite
$$\lim\limits_{z \rightarrow z_{0}}(z-z_{0})^{n}f(z)=l\neq0$$
2. $z_{0}$ è uno zero di $n$-esimo ordine per la funzione $1/f(z)$
3. il seguente limite diverge positivamente $$\lim\limits_{z \rightarrow z_{0}}|f(z)|=+\infty$$ Questa condizione non dà informazioni sull'ordine del polo.
### Singolarità essenziali
Una **singolarità essenziale** in $z_{0}$ è una singolarità isolata determinata dalla presenza di un numero *infinito* di potenze negative nell'espansione in [[serie di Laurent]] della funzione in un intorno di $z_{0}$. Ad esempio, $e^{-1/z^{2}}$ ha una singolarità essenziale in $z_{0}=0$.

In una singolarità essenziale, il limite $\lim\limits_{z \rightarrow z_{0}}f(z)$ non può esistere, né finito, né infinito. Inoltre, vale il [[teorema di Picard]].