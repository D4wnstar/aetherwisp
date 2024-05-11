Si chiama $\hat{\rho}$ la **densità statistica**, **matrice densità** o altri nomi l'operatore:
$$\hat{\rho}=\sum\limits_{i=1}^{\infty}P_{\psi}^{A}(a_{i})|a_{i}\rangle\langle a_{i}|=\sum\limits_{i=1}^{\infty}|\langle a_{i}|\psi\rangle|^{2}|a_{i}\rangle\langle a_{i}|=\sum\limits_{i=1}^{\infty}\langle a_{i}|\psi\rangle \langle \psi|a_{i}\rangle |a_{i}\rangle\langle a_{i}|$$
$$=\sum\limits_{i=1}^{\infty}|a_{i}\rangle\langle a_{i}|\hat{P}_{\psi}|a_{i}\rangle\langle a_{i}|=\sum\limits_{i=1}^{\infty}\hat{P}^{A}_{a_{i}}\hat{P}_{\psi}^{A}\hat{P}^{A}_{a_{i}}$$
$\hat{\rho}$ è *[[Operatore positivo|definito positivo]]*, dunque si ha
$$\langle \psi|\hat{\rho}\psi\rangle=\sum\limits_{\alpha}\lambda_{\alpha}\langle \psi|\hat{P}_{\alpha}\psi\rangle\geq0$$
$$\langle \psi|\psi_\alpha\rangle \langle \psi_{\alpha}|\psi\rangle=|\langle \psi_{\alpha}|\psi\rangle|^{2}\geq 0$$
In [[Rappresentazione spettrale]] è
$$\hat{\rho}=\sum\limits_{\alpha}\lambda_{\alpha}\hat{P}_{\alpha}=\sum\limits_{\alpha}\lambda_{\alpha} |\psi_{\alpha}\rangle\langle \psi_{\alpha}|$$
Cerco la traccia di $\hat{\rho}$ 
$$\mbox{Tr}\hat{\rho}=\sum\limits_{\alpha}\lambda_{\alpha}=1$$
$$\hat{P}_{\alpha}=|\psi_{\alpha}\rangle\langle \psi_{\alpha}||\psi\rangle\langle \psi|=1$$
$$\hat{P}=|\psi_{i}\rangle\langle \psi_\alpha||\psi\rangle\langle \psi|=0$$
con $\psi_{i}$ ket della base e sapendo che $\psi_{i} \perp \psi_{\alpha}$ sono ortogonali.