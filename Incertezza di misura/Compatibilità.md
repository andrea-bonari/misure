>[!note]
>La compatibilità tra due misure $x_{1}$ e $x_{2}$ è l'area in comune tra due PDF.
>![[Pasted image 20241010151623.png]]
>La distanza tra le due misure $x_{1}$ e $x_{2}$ è data da: $$d=|x_{1}-x_{2}|\leq k\sqrt{u^{2}(x_{1})+u^{2}(x_{2})-2r_{12}u(x_{1})u(x_{2})}$$

### Media pesata tra due misure compatibili
>[!note]
>Nel caso di $N$ risultati di misura compatibili, indipendenti e normalmente distribuiti, la miglior stima della misura è: $$x=\overline{x}_{MP}=\frac{\sum\limits^{N}_{i=1} \frac{x_{i}}{u^{2}(x_{i})}}{\sum\limits^{N}_{i=1} \frac{1}{u^{2}(x_{i})}}=\frac{\sum\limits^{N}_{i=1} w_{i}x_{i}}{\sum\limits^{N}_{i=1} w_{i}}$$
>I pesi $w_{i}= \frac{1}{u^{2}(x_{i})}$ sono i reciproci delle varianze stimate e dunque indicano il grado di confidenza che abbiamo sugli $x_{i}$.
>L'incertezza della media pesata è: $$u^{2}(\overline{x}_{MP})= \frac{1}{\sum\limits^{N}_{i=1}\frac{1}{u^{2}(x_{i})}}= \frac{1}{\sum\limits^{n}_{x=1}w_{i}}$$

