>[!note]
>L'oscilloscopio è uno strumento di misura che consente la visualizzazione grafica dell'evoluzione di un segnale di tensione in funzione del tempo. Permette di effettuare misure quantitative e qualitative.

### Oscilloscopio analogico
>[!note]
>L'oscilloscopio analogico si basa sulla tecnologia del CRT (Tubo Catodico). È estremamente limitato da:
>- banda passante limitata a poche centinaia di $\text{MHz}$
>- Impossibilità di acquisire e salvare il segnale
>- Impossibilità di elaborare il segnale
>- Interfaccia molto limitata
>- Il costo non può scalare troppo con la tecnologia

### Oscilloscopio digitale
>[!note]
>L'oscilloscopio digitale è l'evoluzione dell'oscilloscopio analogico, mitigando le sue debolezze. 
>![[Pasted image 20241202162917.png]]
>A differenza di un oscilloscopio analogico l'oscillogramma non è in tempo reale con il segnale. Inoltre il segnale è visualizzato tramite un display raster. Infine permette di usare dispositivi I/O per il trasferimento dati (interfacce RS-232, GPIB, USB, TCP-IP).

>[!tip] Front-end analogico
>![[Pasted image 20241202163630.png]]
>Il commutatore varia il coefficiente di deflessione secondo i passi tarati con la sequenza 1/2/5, tipicamente da $1\text{ mV/DIV}$ fino a $5\text{ V/DIV}$. Il grado di incertezza che il costruttore assegna alla taratura di questa sezione è dell'ordine dell'1%.

>[!tip] ADC
>![[Pasted image 20241202164225.png]]
>Al fine di massimizzare la frequenza di campionamento, si usa interlacciare più ADC.

Affinché l'occhio possa riconoscere distintamente la forma d'onda, il numero di campioni acquisiti deve essere sufficientemente elevato da non generare ambiguità di percezione. Il valore convenzionale è di almeno 25 punti per periodo, tuttavia usando un interpolatore a $\sin(x)/x$ questi si riducono a $2.5$.

>[!tip] Trigger
>In base ad una pendenza o un valore può essere generato un segnale di sincronismo: 
>![[Pasted image 20241202193038.png]]

