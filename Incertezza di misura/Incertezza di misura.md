 >[!note]
>Sappiamo che misure ripetute dello stesso parametro fisico non forniscono lo stesso valore. L'incertezza di misura è la stima della dispersione dei valori attribuibili al misurando.

Le misure sono sempre affette da "fluttuazioni" o errori (almeno potenziali), mai perfettamente conoscibili, che si traducono in una naturale "indeterminazione" o incertezza sul risultato di misura. Occorre quindi lasciare un approccio deterministico in favore di un approccio statistico grazie al quale è possibile stimare le fluttuazioni.

La variabilità del risultato di una misure è analizzata grazie ai metodi consolidati della statistica. Il risultato di misura dunque non è mai un unico numero deterministico ma un intervallo di valori possibili entro il quale il misurando può trovarsi con una data probabilità.

La semiampiezza di un particolare intervallo di valori (l'intervallo a $\pm1$ deviazione standard dal valore centrale) è l'incertezza di misura.

### Teoria degli errori
>[!note]
>La teoria degli errori di misura prevedeva che un misurando non potesse mai essere perfettamente conosciuto a causa degli inevitabili errori di misura.

>[!tip] Errori sistematici
>Si presentano nella stessa entità ogni volta che si ripete la misura.

>[!tip] Errori accidentali
>Si presentano in maniera diversa e "impredicibile" ogni volta che si ripete la misura.

Gli errori sistematici e accidentali non sono della stessa natura.

### Incertezza
>[!note]
>Una corretta analisi statistica della variabilità di una misura consente di risolvere in maniera soddisfacente il problema di esprimere l'incertezza standard di misura. Esistono due categorie di stima dell'incertezza: stimata con metodi statistici e stimata in un altro modo.

### Incertezza standard
>[!note]
>Per qualsiasi misura si definisce l'incertezza standard o scarto tipo, con simbolo $u$, una stima della deviazione standard $\sigma$, radice quadrata della varianza $\sigma^{2}$, prevista per il valore di misura. A seconda del metodo impiegato per la stima classificheremo questa incertezza come di categoria $A$ o $B$.

Definiamo la media campionaria di $n$ misure $x_{k}$ come: $$\overline{x}=\overline{x}_{k}\triangleq \frac{1}{n}\sum\limits_{k=1}^{n} x_{k}$$
La distribuzione della media campionaria $\overline{x}$ ha media $\mu(x)$ pari a quella della media della popolazione da cui è estratto il campione.

>[!example] Dimostrazione
>$$\begin{align*}
E\set{\overline{x}}&= E\left\{\frac{1}{n} \sum\limits_{k=1}^{n}x_{k}\right\}=  \frac{1}{n}E\left\{\sum\limits_{k=1}^{n}x_{k}\right\}\\
&=\frac{1}{n}\sum\limits_{k=1}^{n}E\set{x_{k}}=
\frac{1}{n}\sum\limits_{k=1}^{n}E\set{x}\\
&= \frac{1}{n}\sum\limits^{n}_{k=1}\mu(x)= \frac{1}{n}n\mu(x)=\mu(x)
\end{align*}$$

### Varianza campionaria
>[!note]
>La varianza campionaria è una stima della varianza dell'intera popolazione $\sigma^{2}(x)$, attraverso lo stimatore: $$s^{2}(x)=s^{2}(x_{k})\triangleq \frac{1}{n-1}\sum\limits_{k=1}^{n}(x_{k}-\overline{x})^{2}= \frac{1}{n-1}\left[\left(\sum\limits_{k=1}^{n}x_{k}^{2}\right)-n\overline{x}^{2}\right]$$

Il denominatore $n-1=\nu$ è il numero di gradi di libertà.

### Incertezza composta
>[!note]
>Definiamo l'incertezza composta come: $$u_{C}^{2}=u_{A}^{2}+u_{B}^{2}$$