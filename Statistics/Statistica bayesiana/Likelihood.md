---
wiki-publish: true
---
La **funzione di verosimiglianza** o **likelihood** è la probabilità di osservare un dato condizionata dai parametri del modello utilizzato per stimarlo. Se consideriamo una variabile casuale $X$ e un modello con parametri $\theta$, la probabilità di una realizzazione $x$ di $X$ condizionata da tali parametri è
$$x \rightarrow P(x|\theta)$$
e la likelihood dei parametri condizionata da $x$ è
$$\theta \rightarrow P(\theta|x):= L(\theta|x)$$
che si può interpretare come il livello di fiducia che si ha nei parametri $\theta$ avendo osservato $x$.

La likelihood è una componente fondamentale del [[Teorema di Bayes per la stima dei parametri]], dove viene moltiplicato per il [[Prior]] per ottenere il [[Posterior]].