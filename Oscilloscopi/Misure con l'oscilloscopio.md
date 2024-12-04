### Impostazione iniziale
>[!note]
>1. Si procede innanzitutto alla predisposizione del livello di riferimento dello zero sullo schermo. Per effettuare questa operazione si pone il selettore di ingresso sulla posizione GND e la modalità di trigger automatica. A questo punto sullo schermo appare una linea orizzontale, che può essere traslata in senso verticale, mediante il comando Vert. Pos. del canale di ingresso prescelto. Alla posizione scelta viene in questo modo assegnata la tensione di riferimento zero.
>2. Normalmente si predispone un accoppiamento di tipo DC, in modo da visualizzare il segnale inalterato, con la sua componente continua.
>3. Se utile/necessario è possibile utilizzare anche l’accoppiamento AC, per eliminare la componente continua sovrapposta alla componente variabile del segnale. In questo caso è però necessario assicurarsi che la frequenza del segnale sia convenientemente più elevata di quella del filtro passa alto dell’accoppiamento AC (5 Hz), in modo da evitare grossolane alterazione del segnale di misura.
>4. Nel caso di segnale continuo, è necessario predisporre il trigger nella modalità automatica e non è richiesta la regolazione del livello di trigger. Nel caso di segnale variabile, il livello del trigger va regolato in modo da sincronizzare la base dei tempi con il segnale di misura. E’ opportuno regolare il livello di trigger in modo che esso cada nel tratto a maggior pendenza del segnale, così da aumentare l’insensibilità dell’istante di scatto al rumore additivo di ampiezza. Sempre per limitare l’effetto del rumore è possibile utilizzare i filtri in ingresso del trigger, per limitare la bande passante di questa sezione allo stretto necessario. È possibile impostare la modalità normale, quando c’è un motivo per non visualizzare il segnale in assenza di impulsi di trigger.
>5. Vanno impostate le amplificazioni verticali e orizzontali, in modo da visualizzare "bene" il segnale (o la porzione di segnale di interesse)

### Misure comuni

>[!tip] Misura di ampiezza
>![[Pasted image 20241204155945.png]]
>$$V_{p}=MA_{Y}$$

>[!tip] Misura di tempo e frequenza
>![[Pasted image 20241204160016.png]]
>$$T=N A_{X}$$

>[!tip] Misura di sfasamento
>![[Pasted image 20241204160057.png]]
>$$\Delta \phi= -2\pi \frac{NA_{X}}{T}$$

>[!tip] Misura di tempo di salita
>![[Pasted image 20241204160153.png]]
>$$\begin{align*}
t_{sm}&= \sqrt{t^{2}_{ss}+t^{2}_{so}}\\
t_{ss}&= \sqrt{t^{2}_{sm}-t^{2}_{so}}
\end{align*}$$
Con $t_{so}\cong 0.35/B$

### Modalità X-Y
>[!note]
>La modalità di visualizzazione X-Y applica i due segnali presenti sugli ingressi CH1 e CH2 rispettivamente alle placche di deflessione orizzontale e verticale. Tale modalità permette di visualizzare un segnale in funzione di un altro segnale e quindi di osservare la caratteristica di una grandezza fisica in funzione dell'altra.

### Misure differenziali
>[!note]
>Gli ingressi dell'oscilloscopio sono di tipo sbilanciato o single-ended. Un singolo ingresso non può essere usato per misure di tipo differenziale.
