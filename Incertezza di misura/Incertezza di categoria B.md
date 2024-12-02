>[!note]
>L'incertezza di categoria B definisce a priori un opportuno intervallo di valori entro il quale si suppone debbano cadere i valori del misurando. L'intervallo è fissato attorno al valor medio: $$\overline{x}=a_{0}=\frac{(a_{0}+a)+(a_{0}-a)}{2}$$
>E l'incertezza di misura sarà la larghezza: $$\Delta x=(a_{0}+a)-(a_{0}-a)=2a$$
>![[Pasted image 20241003090542.png]]

Per trovare una stima dell'incertezza di categoria B, si esegue in sequenza:
1. Stima dell'intervallo
2. Associamo una densità di probabilità (PDF)
3. Si calcolano media, varianza e deviazione standard

>[!example] Esempi di PDF comuni
>![[Pasted image 20241003090909.png]]

I criteri per scegliere la PDF:
- Esperienza sul comportamento del misurando.
- Specifiche dei costruttori di materiali e strumenti coinvolti della misura.
- Dati di calibrazioni
- Informazioni da articoli scientifici/tecnici
- Incertezza sui parametri di riferimento

Per calcolare il valor medio e deviazione standard: $$x=x_\text{MIS}=\mu(x)$$
$$u_{B}(x)=\text{INC}_{B}(x)=\sigma(x)$$

>[!tip] Altri metodi di stima di $\mu_{B}$
>- Si calcola $\mu_{B}$ partendo dalla conoscenza di un intervallo di confidenza con probabilità $P$.
>- Si calcola $\mu_{B}$ partendo da conoscenza di una incertezza estesa $U_{B}=k u_{B}$
