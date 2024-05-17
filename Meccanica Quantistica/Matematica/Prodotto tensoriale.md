Presi due sistemi $S_{1}:|\psi_{1}\rangle\in\mathbb{H}$ e $S_{2}:|\psi_{2}\rangle\in\mathbb{H}$, la somma dei due sistemi è
$$S_{1}+S_{2}:|\psi_{1}\otimes\psi_{2}\rangle\equiv |\psi_{1}\rangle\otimes |\psi_{2}\rangle$$
con $\otimes$ il **prodotto tensoriale**. Valgono le seguenti proprietà
1. E' lineare: $$\alpha |\psi_{1}\otimes\psi_{2}\rangle+\beta |\phi_{1}\otimes\phi_{2}\rangle\;\forall\alpha,\beta\in\mathbb{C}$$
2. Per definizione: $$\langle \psi_{1}\otimes\psi_{2}|\phi_{1}\otimes\phi_{2}\rangle=\langle \psi_{1}|\phi_{1}\rangle \langle \psi_{2}|\phi_{2}\rangle$$
3. La norma quadra è: $$||\;|\phi_{1}\otimes\phi_{2}\rangle\;||^{2}=||\phi_{1}||^{2}\;||\phi_{2}||^{2}$$
4. Presi due [[operatori locali]] $\hat{A}_{1}:\mathbb{H}_{1} \rightarrow \mathbb{H}_{1}$ e $\hat{A}_{2}:\mathbb{H}_{2} \rightarrow \mathbb{H}_{2}$ si ha $$\hat{A}_{1}\otimes\hat{A}_{2}\;|\psi_{1}\otimes\psi_{2}\rangle=\hat{A}_{1}|\psi_{1}\rangle\otimes\hat{A}_{2}|\psi_{2}\rangle$$
5. La media di un prodotto tensoriale di due operatori è la sua traccia: $$\langle \hat{A}_{1}\otimes \hat{A}_{2} \rangle=\mbox{Tr}(\hat{A}_{1}\otimes\hat{A}_{2})=\sum\limits_{mn}(\langle \phi_{m}|\otimes \langle \varphi_{n}|)(\hat{A}_{1}\otimes\hat{A}_{2})(|\phi_{n}\rangle\otimes |\varphi_{n}\rangle)=$$$$=\sum\limits_{mn}\langle \phi_{m}|\hat{A}_{1}|\phi_{n}\rangle \langle \varphi_{n}|\hat{A}_{2}|\varphi_{n}\rangle=\sum\limits_{m}\langle \phi_{m}|\hat{A}_{1}|\phi_{m}\rangle \sum\limits_{n}\langle \varphi_{n}|\hat{A}_{2}|\varphi_{n}\rangle=\mbox{Tr}^{(1)}\hat{A}_{1}\mbox{Tr}^{(2)}\hat{A}_{2}$$
