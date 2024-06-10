---
aliases:
  - decadimento
---
Il **decadimento di particelle** è il processo per il quale una [[Particella]] si divide spontaneamente in una o più particelle più piccole. Si tratta di un processo simile, ma distinto dal [[decadimento nucleare]], che invece accade in [[Nucleo atomico|nuclei]] e usa processi diversi.

In generale, il totale delle masse delle particelle figlie deve essere minore o uguale alla particella originale.
### Tipi
#### Particella a riposo
Consideriamo un decadimento in due corpi di una particella a riposo $a \rightarrow b+c$:

![[Schema Decadimento back-to-back|center]]

Per conservazione dell'energia e dell'impulso, si ha
$$\begin{cases}
|\vec{p}_{b}|=|\vec{p}_{c}|=p \\
M_{a}=E_{b}+E_{c}=\sqrt{s}
\end{cases}$$
Vale
$$M_{a}=\sqrt{p^{2}+m_{b}^{2}}+\sqrt{p^{2}+m_{c}^{2}} \quad \Rightarrow \quad (M_{a}-\sqrt{p^{2}+m_{b}^{2}})^{2}=p^{2}+m_{c}^{2} \quad \Rightarrow$$
$$\Rightarrow \quad M_{a}^{2}+p^{2}+m_{b}^{2}-2M_{a}\sqrt{p^{2}+m_{b}^{2}}=p^{2}+m_{c}^{2} \quad \Rightarrow$$
$$\Rightarrow \quad (M_{a}^{2}+m_{b}^{2}-m_{c}^{2})^{2}=2M_{a}\sqrt{p^{2}+m_{b}^{2}}) \quad \Rightarrow$$
$$\Rightarrow \quad M_{a}^{4}+(m_{b}^{2}-m_{c}^{2})-2M_{a}^{2}(m_{b}^{2}+m_{c}^{2})=4M_{a}^{2}(p^{2}+m_{b}^{2})$$
da cui
$$p=\frac{1}{2M_{a}}\sqrt{M_{a}^{4}+(m_{b}^{2}-m_{c}^{2})^{2}-2M_{a}^{2}(m_{b}^{2}+m_{c}^{2})}$$
che significa che l'impulso delle particelle emesse dipende solo dalle masse. D'altro canto, le energie
$$\begin{cases}
E^{2}_{b}=p^{2}+m_{b}^{2}=\frac{M_{a}^{2}+(m_{b}^{2}-m_{c}^{2})}{2M_{a}}=\frac{s+(m_{b}^{2}-m_{c}^{2})}{2\sqrt{s}} \\
E^{2}_{c}=p^{2}+m_{c}^{2}=\frac{M_{a}^{2}-(m_{b}^{2}-m_{c}^{2})}{2M_{a}}=\frac{s-(m_{b}^{2}-m_{c}^{2})}{2\sqrt{s}}
\end{cases}$$
quindi una volta fissata $s$, anche le energie dipendono solo dalle masse.
#### Particella in volo
Consideriamo una particella in volo nel sistema di riferimento del laboratorio. Per esempio, un [[pione]] che decade in due [[fotone|fotoni]]: $\pi^{0} \rightarrow \gamma\gamma$. In questo caso, le particelle figlie vengono emesse ad un angolo.

![[Schema Decadimento ad un angolo|80%|center]]

Si ha
$$\begin{cases}
\theta_{1}+\theta_{2}=\theta \\
(E_{\gamma,1}, \vec{p}_{\gamma,1})=(|\vec{p}_{\gamma,1}|^{2},\vec{p}_{\gamma,1}) \\
(E_{\gamma,2}, \vec{p}_{\gamma,2})=(|\vec{p}_{\gamma,2}|^{2},\vec{p}_{\gamma,2})
\end{cases}$$
dato che $M_{\gamma}=0$.

Se il decadimento viene visto nel sistema di riferimento del centro di massa, si tratta invece di un decadimento back-to-back come quello sopra. In questo caso si ha
$$\begin{cases}
M_{\pi^{0}}=\sqrt{s}=E_{\gamma,1}+E_{\gamma,2}=2E_{\gamma} \\
p_{\gamma,1}=-p_{\gamma,2} \Rightarrow E_{\gamma,1}=E_{\gamma,2}=E_{\gamma} \\
\end{cases}$$

Mettendo insieme le due cose, possiamo trovare l'energia nel centro di massa
$$\sqrt{s}=M_{\pi^{0}}=\sqrt{(p_{\gamma,1}+p_{\gamma,2})^{2}}=\ldots=\sqrt{4E_{\gamma,1}E_{\gamma,2}\sin^{2}\frac{\theta}{2}}$$
che significa che la massa invariante dipende dall'angolo a cui sono emessi i fotoni nel laboratorio. A questo punto ci chiediamo quale possa essere questo angolo. Invertendo la formula sopra
$$\sin\frac{\theta}{2}= \frac{M_{\pi^{0}}}{2\sqrt{E_{1}E_{2}}} \quad \Rightarrow \quad \begin{cases}
E_{1}=\frac{E_{\pi}}{2} \\
E_{2}=\frac{E_{\pi}}{2}
\end{cases}$$
quindi l'energia è equipartita fra le particelle figlie.

L'energia differisce tra sistemi di riferimento. È quindi utile vedere come cambia l'energia nel laboratorio rispetto al centro di massa. Chiamiamo la direzione di moto del pione $x$ e compiamo una [[Trasformazioni di Lorentz|trasformazioni di Lorentz]] su quell'asse:
$$\begin{cases}
E_{\gamma,1}&=\gamma(E_{\gamma,1}^{*}+\beta)=\gamma(E_{\gamma,1}^{*}-\beta p^{*}\cos\theta^{*}) \\
p_{1,x}&=\gamma(p_{1,x}^{*}+\beta E_{\gamma,1}^{*})=\gamma(p^{*}\cos\theta^{*}+\beta E_{\gamma,1}^{*}) \\
p_{1,y}&=p_{1,y}^{*}=p^{*}\sin\theta \\
p_{1,z}&=p_{1,z}
\end{cases}$$
