---
tags:
  - equazioni-differenziali-ordinarie
---
Sia $I ⊆ \mathbb{R}$ intervallo aperto e $f : I × \mathbb{R}^n → \mathbb{R}^n$ che soddisfa le [[Condizioni di Lipschitz]]. Supponiamo che per ogni [[Spazio metrico compatto|compatto]] $J ⊆ I$ esistano due costanti $C_1, C_2 ≥ 0$ tali che
$$||f (t, x)|| ≤ C_1 + C_2 ||x||\quad∀t ∈ J , ∀x ∈ \mathbb{R}^n$$
allora la soluzione massimale di ogni problema di Cauchy è definita su tutto l’intervallo $I$.

Il **teorema di esistenza globale** ci dice che se la funzione cresce al massimo linearmente, la soluzione massimale esiste su tutto $I$.

*Dimostrazione.* Consideriamo gli intervalli dell'enunciato in questa forma: $I=]a,b[ \supseteq \tilde{I}=]\alpha,\beta[$, dove $\tilde{I}$ è l'intervallo su cui è definita la soluzione massimale. Supponiamo per assurdo che $\beta<b$ (e $\beta\in\mathbb{R}$) e prendiamo $\delta>0$ tale che $\beta-\delta>\alpha$. Consideriamo il compatto $[\beta-\delta,\beta]\subseteq I$. La soluzione $\tilde{x}$ è definita come
$$\tilde{x}(t)=\tilde{x}(\beta-\delta)+\int_{\beta-\delta}^{t}f(s, \tilde{x}(s))ds,\quad\forall t\in[\beta-\delta,\beta]$$
Segue che, con la [[Disuguaglianza di Cauchy-Schwarz]]:
$$\begin{align}||\tilde{x}(t)||&\leq||\tilde{x}(\beta-\delta)||+\int_{\beta-\delta}^{t}||f(s,\tilde{x}(s))||ds\\
&\leq||\tilde{x}(\beta-\delta)||+\int_{\beta-\delta}^{t}C_{1}+C_{2}||\tilde{x}(s)||ds
\end{align}
$$
Ponendo $A=||\tilde{x}(\beta-\delta)||+C_{1}\delta$, $B=C_{2}$ e $u(s)=||\tilde{x}(s)||$ vale
$$u(t)\leq A+B\int_{\beta-\delta}^{t}u(s)ds$$
Applicando il [[Lemma di Gronwall]] otteniamo
$$u(t)=||\tilde{x}(t)||\leq (||\tilde{x}(\beta-\delta)||+C_{1}\delta)e^{C_{2}[t-(\beta-\delta)]}=Ae^{B[t-(\beta-\delta)]}\leq Ae^{B\delta}$$
Posto $R:=Ae^{B\delta}$, troviamo che $||\tilde{x}(t)||\leq R$ per ogni $t\in[\beta-\delta,\beta[$ e quindi
$$(t,\tilde{x}(t))\in K:=[\beta-\delta,\beta]\times\bar{B}_{R}(0)$$
che è un compatto. Allora la soluzione massimale contraddice il [[Teorema di uscita dal compatto]]. Di conseguenza non possiamo avere $\beta\leq b$. Ipotizzare che valga $\alpha>a$ porta allo stesso assurdo. Dunque $\tilde{I}=I$.