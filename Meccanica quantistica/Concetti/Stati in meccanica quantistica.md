---
aliases:
  - stato legato
  - stato libero
---
In meccanica classica, preso un [[physical system|sistema]] composto da una [[particella]] ad [[energy|energia]] totale $E$ immersa in un [[Potential]] unidimensionale indipendente dal tempo $V(x)$, si distinguono due tipi di [[stato|stati]] (assumendo la conservazione dell'energia nel sistema, quindi niente motori o attrito):
1. Gli **stati legati** sono quegli stati nei quali la particella è "bloccata" tra due barriere di potenziale insormontabili ed è quindi destinata a "rimbalzare" tra le barriere senza poter mai uscire. Questo accade quando il potenziale cresce al di sopra dell'energia totale della particella, ossia $V(x)>E$ per qualche $x$.
2. Gli **stati liberi** sono quegli stati nei quali la particella si muove da un infinito ad un altro, o rimbalza su una barriera e torna all'infinito di partenza. Questo accade quando il potenziale non sale sopra l'energia della particella o lo fa solo una volta, a modo che non crei una "trappola".

![[Schema Stati legati e liberi|80%|center]]

Anche in meccanica quantistica esistono questi stati, e hanno un particolare significato matematico. Come si può vedere dal caso della [[Buca infinita quantistica|buca infinita]] e della [[Particella libera (quantistica)|particella libera]], ci sono due possibili soluzioni dell'[[equazione di Schrödinger]]: normalizzabili e non-normalizzabili. Le soluzioni normalizzabili possono essere viste come una collezione infinita numerabile di stati indipendenti, mentre quelle non-normalizzabili non corrispondono ad alcuno stato fisico. Tuttavia, in entrambi i casi la loro combinazione lineare ci dà una [[funzione d'onda]] fisica.

Si ha che *le soluzioni normalizzabili corrispondono a stati legati, mentre le soluzioni non-normalizzabili a stati liberi*. Infatti, a causa del [[tunnelling quantistico]], la divisione è ancora più chiara perché è possibile che una particella "salti" una qualunque barriera di potenziale finita, dunque l'unica cosa che conta è il potenziale all'infinito. Vale dunque
$$\begin{cases}
E < [V(-\infty) & \text{e} & V(+\infty)] & \Rightarrow & \text{stato legato} \\
E > [V(-\infty) & \text{o} & V(+\infty)] & \Rightarrow & \text{stato libero}
\end{cases}$$
Nei (moltissimi) casi in cui il potenziale tende a zero all'infinito, la regola è molto semplice:
$$\begin{cases}
E < 0 & \Rightarrow & \text{stato legato} \\
E > 0 & \Rightarrow & \text{stato libero}
\end{cases}$$
I casi comuni ricadono in queste regole: la buca infinita e l'[[oscillatore armonico quantistico]] hanno potenziale che tendono a infinito all'infinito, quindi ammettono solo stati legati. La particella libera ha un potenziale che sempre zero e energia cinetica sempre maggiore di zero, quindi ammette solo stati liberi.