Il **flusso energetico** $\Phi$, o semplicemente **flusso**, è la quantità di energia $E$ che passa attraverso una superficie $S$ per unità di tempo $t$:
$$\Phi=\frac{1}{S} \frac{dE}{dt} \quad \left[\frac{W}{m^{2}}\right]$$
Il flusso energetico trova applicazione in diversi ambiti della fisica e solitamente prende nomi diversi in ciascuno di essi.
### In astrofisica
Nel contesto di telescopi e misurazioni celesti, è comune usare due tipi di flusso: il flusso in una generica banda è la quantità di energia raccolta da un [[rivelatore]] per unità di tempo sulla sua superficie:
$$f_{banda}=\frac{1}{S_{rivelatore}} \frac{dE}{dt} \quad \left[\frac{erg}{s\cdot cm^{2}}\right]$$
Alternativamente, si può anche definire il **flusso monocromatico**, che è il flusso in un piccolo intervallo di lunghezze d'onda $d\lambda$:
$$f_{\lambda}=\frac{1}{S_{rivelatore}} \frac{dE}{dt\,d\lambda} \quad \left[\frac{erg}{s\cdot cm^{2}\cdot Å}\right]$$
che si riferisce al flusso che avrebbe uno strumento efficiente al 100% in quella banda. Questo non è un vero e proprio flusso in termini di unità di misura. È comune misurare le lunghezze d'onda in Angstrom (Å, 1 Å = 0.1 nm), anche se sono comuni anche in nanometri.

L'esatta risposta di un rivelatore dipende dalla lunghezza d'onda dell'onda incidente. I rivelatori non sono uniformemente efficienti in tutte le lunghezze: chiamiamo $s_{banda}(\lambda)$ la *funzione di risposta* di un rivelatore. Nel caso ideale, sarebbe una sorta di onda quadra, dove vale 1 in un certo intervallo e 0 altrove. Ciò permetterebbe misure perfette in un certo intervallo di lunghezze d'onda. Le funzioni d'onda reali sono invece distribuzioni continue con picco ad una certa lunghezza.

![[Assorbimento Filtri Telescopi|80%|center]]

Si può usare questa funzione per legare flusso monocromatico e flusso di banda:
$$f_{banda}=\int_{0}^{\infty}f_{\lambda}s_{banda}(\lambda)d\lambda$$
La funzione in sé è difficile da calcolare e dipende da fenomeni fuori dal controllo degli osservatori, meteo in primis. Si compie dunque una calibrazione ogni notte su stelle standard il cui [[Spettro elettromagnetico]] è noto.

Nell'ottico, le bande più usate sono UBVRI, dalle iniziali della luce che assorbono: (vicino) ultravioletto, blu, visibile, rosso, (vicino) infrarosso. Poi, al di là dell'ottico vi sono continua nell'infrarosso con JHKLMNQ, che sono semplicemente in (quasi) ordine alfabetico.