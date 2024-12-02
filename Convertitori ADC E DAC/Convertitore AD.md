>[!note]
>Un convertitore AD (o voltmetro) è uno strumento che riceve in ingresso una tensione analogica e la digitalizza discretizzando il dominio del tempo e dell'ampiezza. In particolare, la quantizzazione nel dominio del tempo avviene con risoluzione $T_{\text{Sa}}= \frac{1}{f_{\text{Sa}}}$.

La discretizzazione nel tempo avviene campionando la tensione (segnale) in istanti di tempo regolarmente spaziati di una distanza $T_{c}$ periodo di campionamento ($f_{c}= \frac{1}{T_{c}}$ frequenza di campionamento).
![[Pasted image 20241104185622.png]]

La quantizzazione in ampiezza avviene suddividendo la dinamica $D$ di misura in $N$ sotto-intervalli di larghezza costante $\Delta V= \frac{D}{N}$ risoluzione. A tutte le tensione analogiche che cadono nell'intervallo $i$-esimo si associa un unico valore numerico: l'intero $i-1$ che identifica l'intervallo in questione.
![[Pasted image 20241104190151.png]]
