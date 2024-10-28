>[!note]
>![[Pasted image 20241024100035.png]]
>Una scheda di acquisizione dati è un dispositivo usato per acquisire dei dati analogici. È formata da:
>- Multiplexer: permette di selezionare i diversi ingressi disponibili
>- Amplificatore per strumentazione: consente di utilizzare la piena dinamica del convertitore ADC
>- Campionatore e ADC: converte la tensione in valore numerico
>- FIFO: consente di inviare sul bus dati del PC e/o direttamente in memoria RAM (DMA) del PC i dati acquisiti
>
>Solitamente le schede dispongono anche di uscite analogiche (DAC), di linee di I/O e di sincronizzazioni analogiche e digitali (timer e trigger).

### Multiplexer
>[!note]
>Il multiplexer ha $n$ ingressi (solitamente dagli $8$ agli $80$). La scheda può essere in modalità single-ended o differenziali. La scheda avrà $n$ ingressi single-ended e $\frac{n}{2}$ ingressi differenziali. L'acquisizione differenziale è più precisa perché ha minor disturbo.
>![[Pasted image 20241024101101.png]]

### Amplificatore di strumentazione
>[!note]
>Siccome la dinamica di un ADC è fissa, si massimizza la risoluzione sul segnale amplificandolo: $$G= \frac{D_\text{ADC}}{D_\text{Segnale}}$$

### ADC
>[!note]
>Un ADC trasforma un segnale analogico in digitale. Oltre la sua dinamica (range di ampiezza) ha una risoluzione, cioè il numero di bit che usa per rappresentare il segnale analogico in ingresso. La minima tensione rilevabile si calcola come: $$\Delta V=\frac{D_\text{ADC}}{G\cdot 2^{n}}\qquad\underbrace{\delta}_{\text{risoluzione dimensionale (}\Delta V\text{ ideale)}}= \frac{1}{N}= \frac{1}{2^{n}}$$

