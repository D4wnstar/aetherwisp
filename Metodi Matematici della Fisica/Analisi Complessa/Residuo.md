Il **residuo** di una [[singolarità isolata]] in $z_{0}$ di una [[funzione analitica]] $f(z)$ in un intorno di $z_{0}\;\backslash\;\{z_{0}\}$ è definito come
$$\text{Res}_{f}(z_{0})=\frac{1}{2\pi i}\oint_{\gamma}f(z)dz$$
dove $\gamma$ è una qualsiasi [[curva]] semplice chiusa percorsa in senso antiorario contenuta nel campo di analiticità di $f$ e contenente $z_{0}$ e nessun altra singolarità. Il residuo di $f(z)$ in $z_{0}$ è il coefficiente di $(z-z_{0})^{-1}$ nello sviluppo in [[serie di Laurent]] centrata in $z_{0}$. In particolare, se $z_{0}$ è un [[Singolarità isolata#Poli|polo]] di ordine $n$, si ha
$$\text{Res}_{f}(z_{0})=\frac{1}{(n-1)!} \lim\limits_{z \rightarrow z_{0}} \left(\frac{d}{dz}\right)^{n-1}(z-z_{0})^{n}f(z)$$
nel caso $n=1$ diventa
$$\text{Res}_{f}(z_{0})=\lim\limits_{z \rightarrow z_{0}}(z-z_{0})f(z)$$
 Se si ha una funzione della forma $1/g(z)$, come ad esempio $1/(1+z^{4})$, è possibile calcolare il residuo di un polo di ordine 1 in $z_{0}$ usando la formula
$$\text{Res}_{\frac{1}{g}}(z_{0})= \frac{1}{g'(z_{0})}$$

Il punto all'infinito si comporta in modo particolare: è possibile che il residuo all'infinito sia diverso da zero anche se non vi è presente alcuna singolarità isolata. Per calcolare questo residuo, si può considerare la funzione $g(z')=f(1/z)$. Si ha, usando la formula per i coefficienti della [[serie di Laurent]]
$$c'_{n}=\frac{1}{2\pi i}\oint_{\gamma'} \frac{g(z')}{(z')^{n+1}}dz'=- \frac{1}{2\pi i}\oint_{-\gamma} \frac{f(z)}{z^{-(n+1)}} \frac{dz}{z^{2}}=- \frac{1}{2\pi i}\oint_{-\gamma} \frac{f(z)}{z^{-n+1}}dz$$
dove si usa la sostituzione $z=1/z'$ nell'integrale. Allora, ponendo $n=1$, si ha $\text{Res}_{f}(\infty)=-c_{1}'$, cioè il primo componente dell'espansione in serie di $g(z)$ in 0.

Utilizzando le due forme del [[teorema dei residui]] si ottiene che la somma di tutti i residui di una funzione (incluso quello all'infinito) è sempre zero:
$$\sum\limits_{z_{i}}\text{Res}_{f}(z_{i})=0$$
