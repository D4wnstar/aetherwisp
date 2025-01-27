Sia $(p,q)$ un insieme di punti rappresentativi e $\rho$ la loro densità nello [[Phase space]]. Chiamando $x$ la funzione che descrive il loro moto nello spazio delle fasi, vale
$$\frac{d\rho}{dt}=\frac{\partial\rho}{\partial t}+\sum\limits_{i=1}^{2N}\left[\frac{\partial \rho}{\partial q_{i}}\frac{\partial q_{i}}{\partial t}+\frac{\partial \rho}{\partial p_{i}}\frac{\partial p_{i}}{\partial t} \right]=\frac{\partial \rho}{\partial t}+\{\rho,x\}$$
dove $\{\cdot,\cdot\}$ sono le [[Poisson bracket]].

Prendiamo uno spazio $\omega$ arbitrario che non ha né pozzi né sorgenti di punti.
![[Teorema di Lioville|30%|center]]
Chiamo $\vec{v}=(\dot{q}_{1},\ldots,\dot{q}_{3N},\dot{p}_{1},\ldots,\dot{p}_{3N})$. Descrivo il flusso dei punti attraverso il bordo come
$$\begin{align}-\frac{d}{dt}\int_{\omega}\rho(q,p,t)dp^{3N}dq^{3N}&=- \frac{d}{dt}\int_{\omega}\rho d\omega\\
&=\int_{S}\rho\vec{v}^{2}\cdot d\vec{S}\\
&=\int_{\omega}\nabla\cdot(\rho\vec{v})d\omega\\
&=\int_{\omega}\left[\nabla\cdot(\rho\vec{v})+\frac{\partial \rho }{\partial t} \right]\\
&=0
\end{align}$$
definendo $\int_{\omega}\rho d\omega$ l'integrale sullo spazio delle fasi e usando il [[Teorema della divergenza]].

Prendo ora un $\omega$ arbitrario infinitesimo.
$$\begin{align}0&=\left[\nabla\cdot(\rho\vec{v})+\frac{\partial \rho }{\partial t}\right]=\sum\limits_{i=1}^{3N}\left[\frac{\partial }{\partial q_{i}}(\rho\dot{q}_{i})+\frac{\partial }{\partial p_{i}}(\rho\dot{p}_{i}) \right]\\
&=\sum\limits_{i=1}^{3N}\left[\frac{\partial \rho}{\partial q_{i}}\dot{q}_{i}+\frac{\partial \rho}{\partial p_{i}}\dot{p}_{i} \right] + \rho\underbrace{\left[\frac{\partial }{\partial q_{i}}\frac{\partial x}{\partial p_{i}}+\frac{\partial }{\partial p_{i}}\frac{\partial x}{\partial q_{i}} \right]}\limits_{0}
\end{align}$$
sapendo che $\frac{\partial \rho}{\partial t}+\nabla\cdot(\rho\vec{v})=\frac{\partial \rho}{\partial t}+\{\rho,x\}=0$.