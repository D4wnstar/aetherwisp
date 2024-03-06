Si chiama **rapidità** $y$ il valore per il quale valgono le relazioni
$$\begin{cases}
e^{y}=\gamma(1+\beta)=\gamma\left(1+ \frac{v}{c}\right)=\sqrt{\frac{1+ \frac{v}{c}}{1- \frac{v}{c}}}=\sqrt{\frac{1+\beta}{1-\beta}} \\
e^{-y}=\ldots=\sqrt{\frac{1-\beta}{1+\beta}}
\end{cases}$$
Allora $y=\ln(\gamma(1+\beta))$ e
$$\begin{cases}
ct-x=e^{-y}(ct'-x') \\
ct+x=e^{y}(ct'+x')
\end{cases}$$
$$\frac{e^{y}+e^{-y}}{2}=\gamma\quad;\quad \frac{e^{y}-e^{-y}}{2}=\beta\gamma$$
da cui si trova
$$\begin{cases}
\gamma=\cosh(y) \\
\beta\gamma=\sinh(y)
\end{cases}$$
e mettendole insieme
$$\beta=\tanh(y)$$
Allora possiamo interpretare le trasformazioni di Lorentz come rotazioni iperboliche nello spaziotempo, con la rapidità che rappresenta l'angolo di rotazione:
$$\pmatrix{ct' \\ x' \\ y' \\ z'}=\pmatrix{\cosh y & -\sinh y & 0 & 0 \\ -\sinh y & \cosh y & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1}\pmatrix{ct \\ x \\ y \\ z}$$
Possiamo invertire la relazione sopra per definire $y$
$$y=\text{arctanh}\left(\frac{|\vec{p}|c}{E}\right)=\frac{1}{2}\ln\left(\frac{E-|\vec{p}|c}{E+|\vec{p}|c}\right)$$
La rapidità, per costruzione, è un'[[invariante relativistica]].