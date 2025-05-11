---
wiki-publish: true
aliases:
  - autoaggiunto
  - simmetrico
  - hermitiano
  - operatore hermitiano
  - operatore simmetrico
---
Un **operatore autoaggiunto** $T:H \rightarrow H'$ è un [[operatore lineare]] che è pari al suo [[Operatore aggiunto|aggiunto]]. In simboli, vale
$$T^{+}=T\tag{1}$$
e il dominio di $T$ coincide con il dominio di $T^{+}$. Presi due vettori qualunque $x,y$ appartenenti al dominio di $T$, si ha dunque
$$(x,Ty)=(Tx,y)\quad;\quad \braket{ \psi | T\phi } =\braket{ T\psi |\phi  } \tag{2}$$
mostrato anche in [[notazione braket]] per convenienza. È possibile che valga la $(2)$ in un sotto-dominio $D_{0}$ denso nello spazio contenente $T$, contenuto nel dominio $D$ di $T$, ma il dominio non coincida con quello dell'aggiunto. In tal caso, vale solo la $(2)$ e non la $(1)$ e si dice che l'operatore è **hermitiano** (se complesso) o **simmetrico** (se reale) in $D_{0}$. Se $T$ è continuo, allora la $(1)$ e la $(2)$ sono equivalenti, in quanto $D=H$.

Si definisce operatore **antiautoaggiunto** l'operatore che è uguale all'opposto del suo aggiunto
$$T^{+}=-T$$
### Proprietà
- Un operatore hermitiano il cui dominio è l'intero [[spazio di Hilbert]] è [[Operatore lineare|limitato]].
- Per il [[spectral theorem|teorema spettrale]], ogni operatore autoaggiunto in $\mathbb{C}^{n}$ ha $n$ autovettori [[Orthonormality|ortonormali]] e $n$ autovalori reali, che formano una [[base]] di $H$.
- Gli autovalori di un operatore autoaggiunto sono tutti positivi.
- La somma di operatori hermitiani è hermitiana.