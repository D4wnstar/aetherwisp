---
tags:
  - integrali
  - integrali-fisica
---
*Nota:* si usa $\Phi_u$ per significare $\frac{\partial \Phi}{\partial u}$.

Si dice **superficie** una funzione continua $\Phi : \Omega\subset \mathbb{R}^2 → \mathbb{R}^3$ con $\Phi(u,v)=(x(u,v),y(u,v),z(u,v))$. L’immagine $\Sigma=\Phi(\Omega)$ si dice **sostegno della superficie**.
Una superficie si dice *regolare* se è di classe $C^1$ e vale $(\Phi_u\times \Phi_v)(u,v)\neq(0,0,0),\;\forall(u,v)\in\Omega$.

Posso considerare i vettori normali alla superficie $\widehat{N}_\Phi:\Omega\rightarrow \mathbb{R}^3$ come
$$\widehat{N}_\Phi(u,v)= \frac{\Phi_u\times\Phi_v}{||\Phi_u\times\Phi_v||}$$

Due curve regolari $\Phi_1:\Omega_1\rightarrow\mathbb{R}^3$ e $\Phi_2:\Omega_2\rightarrow\mathbb{R}^3$ si dicono *equivalenti* se hanno lo stesso sostegno ed esiste un $C^1$-diffeomorfismo $\varphi:\Omega_1\rightarrow \Omega_2$ tale che $\Phi_1=\Phi_2\circ\varphi$. Si dirà che le due curve hanno la stessa orientazione se $\det J_\varphi(u,v)>0\;\forall (u,v)\in \Omega_1$.

Si definisce *insieme riflesso* l'insieme $\tilde{\Omega}=\{(v,u)|(u,v)\in\Omega\}$. e definire la superficie $\Psi:\tilde{\Omega}\subset \mathbb{R}^{2}\rightarrow \mathbb{R}^{3}$ come $\Psi(v,u)=\Phi(u,v)$ in cui abbiamo scambiato le variabili. I vettori normali sono invertiti di segno.