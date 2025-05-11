---
wiki-publish: true
---
Il **teorema di Bayes** per la stima dei parametri afferma che la *distribuzione a posteriori*, o semplicemente *posteriore*, vale
$$P(p|dM)=\frac{P(d|pM)P(p|M)}{P(d|M)}$$
dove $d$ si riferisce ai dati misurati, $M$ al modello in uso (una distribuzione statistica) e $p$ sono i parametri di quel modello (della distribuzione, come valor medio e varianza). 

$P(d|pM)$ è la *funzione di verosimiglianza*, o [[Likelihood]].

$P(p|M)$ è la conoscenza *a priori* o [[Prior]], che quantifica quanto sappiamo del modello prima ancora di misurare i dati.

$P(d|M)$ è l'*evidenza* (*evidence*), o *likelihood marginalizzata*, ed è la likelihood calcolata su tutti i possibili parametri che il posteriore può avere.

La distribuzione a posteriori $P(p|dM)$, o [[Posterior]], rappresenta la probabilità che i parametri del modello abbiano un certo valore. In altre parole, il posteriore contiene l'informazione che sappiamo da prima (a priori) più le cose che scopriamo misurando (la likelihood).