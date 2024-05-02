Il **teorema di Ehrenfest** afferma che i valori di aspettazione degli [[Operatore|operatori]] posizione $x$ e quantità di moto $p$ obbediscono leggi simili a quelle classiche.
$$m \frac{d \left\langle x \right\rangle}{dt}=m \left\langle v \right\rangle =\left\langle p \right\rangle\tag{1}$$
$$\frac{d \left\langle p \right\rangle}{dt}=-\left\langle \frac{\partial V(x)}{\partial x} \right\rangle=- \left\langle V'(x) \right\rangle\tag{2}$$
con $V'$ la derivata di $V$.

La $(1)$ è di fatto uguale alla legge $p=mv=m (\partial t/\partial x)$ della meccanica classica. La $(2)$, tuttavia, non è propriamente uguale alla controparte classica. Infatti, se $(1)$ e $(2)$ soddisfassero le leggi di Newton, si dovrebbe avere $-V'(\left\langle x \right\rangle)$ e *non* $-\left\langle V'(x) \right\rangle$. Queste due quantità sono uguali solo se il moto è lineare; in tal caso, $V$ è quadratico e $V'$ è lineare, il che fa tornare i calcoli. Se $V$ dipende da potenze maggiori di $x$, si trova che la forma classica dà $\left\langle x \right\rangle^{p}$, mentre quella di Ehrenfest dà $\left\langle x^{p} \right\rangle$, che non sono di solito uguali.

Il teorema vale anche in tre dimensioni:
$$m \frac{d\left\langle \vec{x} \right\rangle}{dt}=\left\langle \vec{p} \right\rangle$$
$$\frac{d \left\langle \vec{p} \right\rangle}{dt}=\left\langle -\nabla V \right\rangle$$
