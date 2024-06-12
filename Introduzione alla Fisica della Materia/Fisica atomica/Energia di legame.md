L'**energia di legame** $B$ è l'energia necessaria per rimuovere una [[Particella]] da un sistema legato, come per esempio un [[atomo]] e i suoi [[Elettrone|elettroni]]. In fisica nucleare, si preferisce il termine **energia di separazione** quando si parla di rimuovere [[Nucleone|nucleoni]] dal [[Nucleo atomico|nucleo]].

È definita come la differenza tra la massa dei singoli costituenti del sistema e la massa del sistema, moltiplicata per $c^{2}$. La differenza tra la massa del sistema legato e i suoi costituenti viene anche detta **difetto di massa**. Per un nucleo, è la differenza in massa tra il nucleo $^{A}_{Z}X_{N}$ e i suoi costituenti $Z$ [[protone|protoni]] e [[neutrone|neutroni]].

È conveniente esprimere l'energia di legame in funzione delle masse atomiche, in quanto sono misurabili sperimentalmente con grande precisione ($\sim10^{-6}$) usando la [[spettroscopia di massa]]. Allora abbiamo
$$B(Z,A)=[Zm(^{1}H)+Nm_{n}-m(A,Z)]c^{2}$$
dove
- $m_{n}$ è la massa del [[neutrone]].
- $m(^{1}H)=m_{e}+m_{p}$, con $m_{e}$ e $m_{p}$ le masse dell'[[Elettrone]] e del [[protone]].
- $A$, $N$ e $Z$ [[Atomo|numero di massa atomica]], [[Atomo|numero di neutroni]] e [[Atomo|numero atomico]].
- $c$ è la [[velocità della luce]].
In sostanza, questa formula misura la differenza tra le masse dell'atomo e la massa che avrebbe il sistema se fosse composto da atomi di idrogeno e neutroni separatamente.

![[Schema Energia di legame elio|100%]]

### Parametrizzazione
Per un nucleo atomico, l'energia di legame è la differenza tra la massa dei suoi protoni e neutroni e l'energia che li tiene legati assieme. È più comodo scrivere $B$ come
$$B(Z,A)=[Zm_{p}+Nm_{n}-(M(^{A}X)-Zm_{e})]c^{2}=\ldots$$
Raggruppando le $Z$ masse di protoni e elettroni in $Z$ atomi di idrogeno ho
$$\ldots=[ZM(^{1}H)+Nm_{n}-m(^{A}X)]c^{2}$$
dove ci rimane la massa del nucleo $m(^{A}X)$. Sapendo il difetto di massa $\Delta = (m-A)c^{2}$ posso invertire questa relazione per trovare la massa atomica.

L'*energia di separazione di un neutrone* $S_{n}$ è l'energia necessaria per rimuovere un neutrone da un nucleo, cioè la differenza di energia di legame tra $_{Z}^{A}X_{N}$ e $_{Z}^{A-1}X_{N-1}$:
$$S_{n}=B(_{Z}^{A}X_{N})-B(_{Z}^{A-1}X_{N-1})=[m(_{Z}^{A-1}X_{N-1})-m(_{Z}^{A}X_{N})+m_{n}]c^{2}$$
L'*energia di separazione di un protone* $S_{p}$ è definita analogamente:
$$S_{p}=B(_{Z}^{A}X_{N})-B(_{Z-1}^{A-1}X_{N})=[m(_{Z-1}^{A-1}X_{N})-m(_{Z}^{A}X_{N})+m(^{1}H)]c^{2}$$

L'energia di legame di un nucleo dipende dal suo numero di massa atomica $A$. Ci si potrebbe aspettare che il rapporto tra energia di legame e numero di nucleoni sia costante, ma non è così:

![[Grafico Energia di legame|80%|center]]

$B$ cresce moltissimo nei primi atomi (fino a $A\simeq20$) dopodiché comincia ad appiattirsi e a scendere con una lieve pendenza. La stragrande maggioranza dei nuclei risiede in una fascia relativamente stretta, compresa tra 7.2 e 8.8 MeV/nucleone ($8.0\pm0.8$ MeV/nucleone). Gli unici elementi non inclusi in questa banda sono quelli molto leggeri, con $A<10$, come idrogeno ed elio. Il picco di energia per nucleone si trova a $A\sim60$, dove gli nuclei evidentemente sono particolarmente legati.

Questo grafico ci dà informazioni su quale processo è energeticamente viabile per rilasciare energia:
1. per $A<60$ è più efficiente combinare nuclei assieme mediante la [[fusione nucleare]].
2. per $A>60$ è più efficiente spezzare nuclei per crearne di più piccoli mediante la [[Fissione spontanea]].

Il "capolinea" di questi processi è in ogni caso gli elementi ad $A\sim60$. Per esempio, la fusione nucleare non può creare atomi più pesanti del ferro ($A=56$) senza avere aggiunte di energia dall'esterno.