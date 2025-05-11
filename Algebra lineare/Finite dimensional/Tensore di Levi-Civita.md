---
wiki-publish: true
aliases:
  - tensore antisimmetrico
---
Il **tensore di Levi-Civita** o **tensore antisimmetrico** $\epsilon_{i_{1}i_{2}\ldots i_{n}}$ è un oggetto definito dal segno di una [[permutazione]] di numeri naturali. Dato che vi sono $n^{n}$ possibili permutazioni di $n$ numeri interi, può essere rappresentato come un tensore quadrato $n\times n\times\ldots \times n$.
### Proprietà
Il tensore di Levi-Civita è [[Matrice simmetrica|antisimmetrico]], ossia scambiati due indici, si inverte il segno:
$$\epsilon_{\ldots i\ldots j\ldots} = -\epsilon_{\ldots j\ldots i\ldots}$$
Se due indici sono uguali, vale zero:
$$\epsilon_{\ldots i \ldots i \ldots}=0$$
Se invece gli indici sono tutti diversi vale
$$\epsilon_{i_{1}i_{2}\ldots i_{n}}=(-1)^{p}\epsilon_{12\ldots n}$$
dove $p$ è la **parità** di una permutazione, ossia il minimo numero di scambi necessari per riordinare gli indici a 1, 2, ..., $n$. $(-1)^{p}$ è detto **segno** di una permutazione.

Il valore di $\epsilon_{12\ldots n}$ è arbitrario e di solito si sceglie $\epsilon_{12\ldots n}=1$ a modo che sia sempre uguale al segno della permutazione.

In due dimensioni può essere rappresentato come
$$\pmatrix{\epsilon_{11} & \epsilon_{12} \\ \epsilon_{21} & \epsilon_{22}}=\pmatrix{0 & 1 \\ -1 & 0}$$
