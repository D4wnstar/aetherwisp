Considero una trasformazione reversibile di un gas da $V_{1}$ a $V_{2}$ all'interno di un termostato. L'energia interna del sistema è $E=\frac{3}{2}Nk_{b}T$, dove $k_{b}$ è la [[costante di Boltzmann]]. La variazione di energia (con il pedice $g$ che sta per gas):
$$dE_{g}=0=TdS_{g}-PdV_{g}$$
$$TdS_{g}=PdV_{g}\quad \Rightarrow\quad dS_{g}= \frac{P}{T}dV_{g}$$
Dato che siamo in una trasformazione reversibile, possiamo fare l'integrale con l'uguaglianza per il [[Principi della termodinamica#Primo principio|primo principio della termodinamica]]
$$\Delta S= S(V_{2})-S(V_{1})=\int_{V_{1}}^{V_{2}}\frac{P}{T}dV_{g}=\int_{V_{1}}^{V_{2}}\frac{Nk_{b}}{V_{g}}dV_{g}=Nk_{b}\ln\left(\frac{V_{2}}{V_{1}}\right)$$
Allora la variazione di entropia del termostato e del gas è
$$\Delta S_{t} = - \Delta S_{g}\quad \Rightarrow \quad \Delta S_{t}+\Delta S_{g}=0$$

Consideriamo ora l'espansione libera di un gas da $V_{1}$ a $V_{2}$ in un sistema isolato a temperatura $T$ fissa. In questo caso valgono gli stessi risultati appena trovati.

Nel caso ci sia un contenitore chiuso di volume $V$ diviso in due parti, ciascuna con una certa quantità di gas $V_{1}$ e $V_{2}$ si ha $P_{1}= \frac{Nk_{b}T}{V_{1}}$ e $P_{2}= \frac{Nk_{b}T}{V_{2}}$. Prendo come sistema di riferimento iniziale $V_{1}=V_{2}=\frac{V}{2}$
$$\Delta S_{1}=Nk_{b}\ln\left(\frac{V_{1}}{\frac{V}{2}}\right),\quad \Delta S_{2}=Nk_{b}\ln\left(\frac{V_{2}}{\frac{V}{2}}\right)$$
$$\Delta S = \Delta S_{1}+\Delta S_{2}=Nk_{b}\ln\left(\frac{V_{1}V_{2}}{\left(\frac{V}{2}\right)^{2}}\right)$$
Chiamando $\phi = V_{1}/\frac{V}{2}$, che varia in $0\leq\phi\leq2$ e usando $V_{2} =V-V_{1}$
$$\Delta S=Nk_{b}\ln[\phi(2-\phi)]$$
Considero la funzione $f(\phi)=\phi(2-\phi)$. Questa è una funzione parabolica con un massimo.

![[Forma Phi MS|center]]