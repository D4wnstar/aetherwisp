La **magnitudine** (apparente) $m$ è una misura di luminosità relativa definita originariamente da Ipparco nell'antica Grecia per descrivere quanto appariva luminosa una stella all'occhio umano. Nel 1856, il concetto è stato formalizzato matematicamente da Norman Pogson. Si tratta di una misura relativa, che paragona la magnitudine di due stelle e ci dà una misura della differenza tra le due. Conoscendo i flussi dei due astri $f_{1}$ e $f_{2}$, vale
$$m_{2}-m_{1}=2.5\times\log_{10}\left(\frac{f_{2}}{f_{1}}\right)$$
Più bassa è, più luminoso è l'oggetto, con valori molto negativi corrispondenti a corpi molto brillanti come il Sole (circa -27) o la Luna (circa -13 a luna piena).

Essendo una misura relativa, bisogna avere un punto di riferimento:
- Una possibilità è il **sistema Vega**. Vega è la stella più luminosa del cielo estivo, la cui magnitudine è definita 0 in tutte le lunghezze d'onda. Il problema è misurare il flusso (complesso) di Vega.
- Alternativamente si usa il **sistema AB**, dove ci si basa su un oggetto immaginario che ha flusso costante in tutte le lunghezze d'onda. Diventa facile calcolare il flusso, senza integrali, usando $f_{banda}=\frac{L_{banda}}{4\pi d^{2}}$, con $L_{banda}$ la luminosità della banda.
![[Sistemi di magnitudine|center|100%]]

La magnitudine dipende dal flusso di un oggetto e quindi dalla sua distanza. Dunque, per "normalizzare" le magnitudini in funzione della distanza, si usa la **magnitudine assoluta**
$$M=m-5\log(d)+5\equiv m-\mu$$
dove $m$ è la magnitudine apparente in una certa banda e $d$ è la distanza dell'oggetto. $\mu$ si dice *modulo di distanza*. Questa misura rappresenta la luminosità che la stella avrebbe se fosse posta a 10 [[parsec]] di distanza.