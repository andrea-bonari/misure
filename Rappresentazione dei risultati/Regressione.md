>[!note]
>La regressione è la procedura usata per stimare la relazione tra dei dati in un insieme di dati discreto.

### Regressione lineare LS
>[!note]
>Consideriamo la dipendenza lineare $y=mx+q$ di cui si vogliono ricavare i due parametri $m$ e $q$. Per il punto $i$-esimo di misura lo scarto $\delta_{i}$ tra il valore empirico $y_{i}$ e quello della curva di regressione $f(x_{i})$ vale: $$\delta_{i}=y_{i}-[mx_{i}+q]$$
>Dobbiamo trovare i valori dei parametri per i quali è minima la distanza: $$\Phi(m,q)=\sum\limits_{i=1}^{n}\delta_{i}^{2}=\sum\limits_{i=1}^{n}[y_{i}-(mx_{i}+q)]^{2}$$
>Deriviamo quindi rispetto a $m$ e $q$ e le annulliamo. $$\begin{align*}
>\frac{\partial \Phi}{\partial m}&=0\Longrightarrow \left(m\sum\limits x_{i}^{2}\right)+q\sum\limits x_{i}=\sum\limits x_{i}y_{i}\\
>\frac{\partial\Phi}{\partial q}&=0\Longrightarrow \left(m\sum\limits x_{i}\right)+nq=\sum\limits y_{i}
>\end{align*}$$
>Otteniamo quindi un sistema risolvibile per sostituzione che si risolve come: 
>$$m=\frac{n\sum\limits x_{i}y_{i}-\sum\limits x_{i}\sum\limits y_{i}}{n\sum\limits x_{i}^{2}-(\sum\limits x_{i})^{2}}$$
>$$q=\overline{y}-m\overline{x}=\frac{\sum\limits y_{i}-m\sum\limits x_{i}}{n}$$
