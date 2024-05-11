Il **potenziale di Woods-Saxon** è un potenziale di campo medio per i nucleoni del [[nucleo]] di un [[atomo]]. Usa una distribuzione di densità di carica di Fermi
$$\rho(r)=\frac{\rho(0)}{1+e^{(r-c)/a}}$$
dove $c$ è la distanza radiale alla quale $\rho(c)=\rho(0)/2$ e $a$ è lo spessore della superficie del nucleo. Sperimentalmente si trova $a\sim0.5$ fm. Il potenziale è
$$V(r)=- \frac{V_{0}}{1+e^{(r-R)/a}}$$
![[Grafico Potenziale di Wood-Saxon|center]]
con $R$ il raggio medio del nucleo. Vale $R=R_{0}A^{1/3}$ con $R_{0}$ la [[costante di Rydberg]] e $V_{0}$ si trova essere $\sim50$ MeV.
### Accoppiamento spin-orbita
$$V_{tot}(r)=V_{centr}(r)+V_{l,s}(r)\frac{\left\langle \vec{l}\cdot\vec{s} \right\rangle}{\hbar^{2}}$$
dove $\vec{l}$ è il momento angolare orbitale (rispetto al centro del nucleo) e $\vec{s}$ è lo [[Spin]] del nucleone.

Ogni nucleone ha spin $\frac{1}{2}$ e momento angolare totale $\vec{j}=\vec{l}+\vec{s}$. Vale $j=l\pm \frac{1}{2}$. Calcoliamo
$$j^{2}=(\vec{l}+\vec{s})^{2}=(\vec{l}^{2}+2\vec{l}\cdot\vec{s}+\vec{s}^{2}) \rightarrow \vec{l}\cdot\vec{s}=\frac{1}{2}(\vec{j}^{2}-\vec{l}^{2}-\vec{s}^{2})$$
risolvo l'equazione agli autovalori e inserisco i valori attesi
$$\left\langle \vec{l} \cdot\vec{s} \right\rangle=\frac{\hbar^{2}}{2}[j(j+1)-l(l+1)-s(s+1)]=$$
$$=\hbar^{2}\begin{cases}
j=l+ \frac{1}{2} \rightarrow \frac{l}{2} \\
j=l- \frac{1}{2} \rightarrow -l \frac{l+1}{2}
\end{cases}$$
La separazione energetica dei livelli è
$$\Delta E_{l,s}=\left[\left\langle \vec{l} \cdot \vec{s}_{j=l+1/2} \right\rangle - \left\langle \vec{l}\cdot\vec{s} \right\rangle_{j=l-1/2}\right]V_{l,s}(r)=\frac{2l+1}{2}V_{l,s}(r)$$
1. Se $l>0$, i livelli sono separati in 2 parti. 
2. Si usa il pedice $j=l\pm \frac{1}{2}$ con $j=0,1,2,3\ldots=s,p,d,f,\ldots$
3. La degenerazione è $2(2l+1)$
