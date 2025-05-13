---
wiki-publish: true
---
Si dice **spettro** di un [[operatore]] $T$ l'insieme di tutti i numeri $\sigma$ tali per cui l'operatore $T-\sigma I$ non ammette inverso limitato, cioè se non è invertibile o se ammette un inverso non limitato. Gli [[Equazione agli autovalori|autovalori]] sono automaticamente parte dello spettro. In particolare, in dimensione finita lo spettro *è* l'insieme degli autovalori.

Uno spettro si dice **degenere** se due o più autovettori (o autofunzioni) [[lineare indipendenza|linearmente indipendenti]] hanno lo stesso autovalore.

Si dice **risolvente** di $T$ l'insieme complementare dello spettro, ovvero se $\lambda\in\mathbb{C}$ è nel risolvente, l'equazione $(T-\lambda)x=v$, dove $v\in H$ è assegnato e $x$ il vettore incognito, ha un'unica soluzione $x=(T-\lambda)^{-1}v$. Se invece $\lambda$ è nello spettro, l'equazione ha soluzione solo se $v\in\text{Imm}(T-\lambda I)$ e in questo caso la soluzione è unica se $\lambda$ non è autovalore di $T$.

Si dimostra anche che lo spettro è un insieme chiuso e quindi il risolvente è aperto.
### Proprietà
- Presi due operatori $T_{1}$ e $T_{2}$, lo spettro della somma $\text{Sp}(T_{1}+T_{2})$ è pari alla somma degli spettri $\text{Sp}(T_{1})+\text{Sp}(T_{2})$ se e solo se $T_{1}$ e $T_{2}$ [[Commutator|commutano]].