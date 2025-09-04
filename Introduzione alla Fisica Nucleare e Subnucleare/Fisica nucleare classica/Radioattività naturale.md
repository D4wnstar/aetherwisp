---
wiki-publish: true
---
Alcuni elementi radioattivi prodotti dopo il [[Big Bang]] sono già decaduti, ma altri con tempi di dimezzamento sufficientemente lunghi sono ancora presenti sulla terra e costituiscono la **radioattività naturale**.

I [[Nuclide|nuclidi]] radioattivi decadono [[Decadimento Alpha|alpha]] e [[Decadimento Beta|beta]]. Esistono quattro catene di [[Nuclear decay|decadimento]] indipendenti.

|              | Tipo   | Elementi con $t_{1/2}$ più lungo               |
| ------------ | ------ | ---------------------------------------------- |
| **Torio**    | $4n$   | $^{232}\text{Th}$ con $1.41\times10^{10}$ anni |
| **Nettunio** | $4n+1$ | $^{237}\text{Np}$ con $\sim10^{6}$ anni        |
| **Uranio**   | $4n+2$ | $^{238}\text{U}$ con $\sim10^{10}$ anni        |
| **Attinio**  | $4n+3$ | $^{235}\text{U}$ con $\sim10^{9}$ anni         |
Dato che l'uranio ha un $t_{1/2}$ più basso dell'età della Terra, oggi non si vedono effetti della catena di decadimento. Le altre catene producono tutte gas radon che è quindi presente nelle pietre e può costituire un rischio per la salute.

L'uranio oggi in natura è un mix di $^{238}\text{U}$ al 99.28% e $^{235}\text{U}$ al 0.72%. Assumiamo che all'origine del [[Sistema Solare]] i 2 [[Isotope|isotopi]] avessero la stessa abbondanza. Calcoliamo allora l'età della Terra a partire dal rapporto odierno.

Uso la legge esponenziale del decadimento
$$N(t)=N_{0}e^{-\lambda t}$$
allora
$$\frac{99.28}{0.72}=\frac{e^{-\lambda_{238}t}}{e^{-\lambda_{235}t}}$$
Conosco i tempi di dimezzamento
$$t_{1/2,238}=4.468\times10^{9}\text{ anni}\quad;\quad t_{1/2,235}=7.038\times10^{8}\text{ anni}$$
Allora le costanti di decadimento sono
$$\lambda_{238}=\frac{\ln2}{t_{1/2,238}}=0.155\times10^{-9}\text{ anno}^{-1}$$
$$\lambda_{235}=0.0985\times10^{-8}\text{ anno}^{-1}$$
allora
$$t=\frac{\ln(e^{-\lambda_{238}-\lambda_{235}})t}{\lambda_{238}-\lambda_{235}}=5.94\times10^{9}\text{ anni}$$
