Si parla di potenziali termodinamici **estensivi** se sono *[[Funzioni omogenee di primo grado]] nelle [[Proprietà intensive e estensive|variabili estensive]]*. 
## Energia del sistema

Si tratta di quella trovata nel [[Principi della termodinamica#Primo principio|primo principio della termodinamica]], ossia $E = Q - W$ con differenziale $dE = TdS - PdV$.

## Energia libera di Helmholtz

Chiamo l'**energia libera di Helmholtz** $A = TS$ con differenziale $dA = dE - d(TS) = TdS - PdV - TdS - SdT$ da cui si ottiene $dA = -SdT - PdV$. Ora il potenziale è dipendente da $T$ e da $V$. L'atto di cambiare le variabili da cui dipende una quantità si chiama [[trasformata di Legendre]]. Si nota che la temperatura è di nuovo associata all'entropia e la pressione con il volume.

## Energia libera di Gibbs

Chiamo l'**energia libera di Gibbs** $G=A+PV$ e trovo il differenziale $dG=-SdT+VdP$. Ora è dipendente da $T$ e $P$. L'energia libera di Gibbs ha *solo* dipendenze [[Proprietà intensive e estensive|intensive]].

### Potenziali dipendenti dal numero di particelle

L'energia del sistema diventa $E(T,S,N)=TdS-PdV+\mu dN$, con $\mu = \frac{\partial E}{\partial N}$ tenendo costanti a $S,V$.
L'energia di Helmholtz diventa $A(V,T,N) = -SdT - PdV + \mu dV$, con $\mu=\frac{\partial A}{\partial N}$ tenendo $T,V$ costanti.
L'energia di Gibbs diventa $G(T,P,N)=-SdT+VdP+\mu dN$, con $\mu = \frac{\partial G}{\partial N}$ tenendo $T,P$ costanti.

Vale $\frac{\partial G}{\partial N}{\big|}_{T,P} N=G=N\mu$, da cui $dG=\mu dN+VdP-SdT=Nd\mu+\mu dN$ quindi eliminando $\mu dN$ trovo
$$Nd\mu=VdP-SdT$$
Quindi dividendo per $V$ e chiamando $\rho=\frac{N}{V}$ la densità
$$\rho d\mu=dP- \frac{S}{V}dT$$
O dividendo per $N$
$$d\mu = VdP - \frac{S}{N}dT$$

Quindi la derivata parziale del potenziale nel numero di particelle è il **potenziale chimico** $\mu$ di quelle particelle. Questa formula è generalizzata dalla [[Relazione di Gibbs-Duhem]].

Nel caso dell'energia di sistema si ha $A(N,V,T)=\frac{\partial A}{\partial N}N+\frac{\partial A}{\partial V}V=A=N\mu-PV$, da cui $dA=-SdT-PdV+\mu dN=Nd\mu+\mu dV-PdV-VdP$, quindi semplificando $Nd\mu=-SdT+VdP$, quindi torniamo alla stessa relazione trovata dall'energia di Gibbs. Se dividiamo per il volume $V$: $\frac{A(N,V,T)}{V}\equiv a=\rho\mu-P$, ossia il *potenziale per unità di volume*.
Differenziando: $da=\rho d\mu+\mu d\rho-dP=dP- \frac{S}{V}dT+\mu d\rho-dP = -\frac{S}{V}dT+\mu d\rho$, quindi $a$ è dipendente solo da $T$ e $\rho$. In simboli
$$a= \frac{A(N,T,P)}{V}=a(\rho,T)\quad\quad \frac{\partial a}{\partial \rho}{\big|}_{T}= \mu$$
