---
wiki-publish: true
tags:
  - integrali
  - integrali-fisica
---
# Prima specie
Data una [[Surface]] regolare $\Phi : \Omega ⊂ \mathbb{R}^{2} → \mathbb{R}^{3}$ e una funzione continua $f : A → \mathbb{R}$ definita su un aperto $A ⊂ \mathbb{R}^{3}$ . Supponiamo che il sostegno di $\Phi$ sia contenuto in $A$, allora l’**integrale di superficie di prima specie di $f$ su $\Phi$** risulta
$$\int_{\Phi}fdS:=\int_{\Omega} f(\Phi(u,v))||(\Phi_{u}\times \Phi_v)(u,v)||dudv$$
Se $f(t)=1$ allora si ha la misura (cioè l'area) di $\Phi$. Questo integrale è *invariante* per superfici equivalenti. Per provarlo, basti trovare un $C^1$-diffeomorfismo $\varphi$ tale che $\Psi(u,v)=\varphi(\Phi(u,v))$, con $\Phi(u,v)$ e $\Psi(u,v)$ le due superfici e calcolare l'integrale.
# Seconda specie
Siano $\Phi:\Omega\subset\mathbb{R}^{2} \rightarrow\mathbb{R}^3$ una superficie regolare e $F:A\subset\mathbb{R}^N\rightarrow\mathbb{R}^N$ una funzione continua con $A$ aperto. Supponiamo che il sostegno di $\Phi$ sia contenuto in $A$, allora l'**integrale di seconda specie di $F$ lungo $\Phi$** risulta
$$\int_{\Phi}F\cdot\hat{\nu}dS:=\int_{\Omega}\langle F(\Phi(u,v)),(\Phi_{u}\times \Phi_{v})(u,v)\rangle dudv$$
dove $\langle a, b \rangle$ è il prodotto scalare. Questo integrale è invariante se le due curve hanno la stessa orientazione. Altrimenti l'integrale inverte segno.