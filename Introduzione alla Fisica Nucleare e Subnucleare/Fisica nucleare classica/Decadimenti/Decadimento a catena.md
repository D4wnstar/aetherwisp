---
aliases:
  - catena di decadimento
---
È possibile che un [[Nuclide|radionuclide]] [[Decadimento|decada]] in [[Nucleo atomico|specie nucleari]] che al loro volta sono instabili, e quindi queste a loro volta decadranno in nuove specie. Questo fenomeno è detto **decadimento a catena** e la successione di nuclei che vengono prodotti dai decadimenti è detta **catena di decadimento**.
### Serie di decadimenti
Nel caso di una serie di decadimenti, e quindi di generazione di nuclei, ho
$$dN_{i}=\lambda_{i-1}N_{i-1}dt-\lambda_{i}N_{i}dt$$
dette le **equazioni di Bateman**, che danno una soluzione generale nel caso in cui $N_{0}$ sia costituito solo da nuclei madre. L'attività è
$$A_{n}=N_{0}\sum\limits_{i=0}^{n}c_{i}e^{-\lambda_{i}t}=N_{0}(c_{1}e^{-\lambda_{1}t}+c_{2}e^{-\lambda_{2}t}+\ldots+c_{n}e^{-\lambda_{n}t})$$
dove $c_{i}$ è
$$c_{m}=\frac{\prod_{i=1}^{n}\lambda_{i}}{\prod_{i=1}^{n}(\lambda_{i}-\lambda_{m})}=\frac{\lambda_{1}\lambda_{2}\lambda_{3}\ldots\lambda_{n}}{(\lambda_{1}-\lambda_{m})(\lambda_{2}-\lambda_{m})\ldots(\lambda_{n}-\lambda_{m})}$$
dove nei produttori ometto il termine $i=m$. Si ha equilibrio secolare nel caso
$$\lambda_{1}N_{1}=\lambda_{2}N_{2}=\ldots=\lambda_{n}N_{n}$$
