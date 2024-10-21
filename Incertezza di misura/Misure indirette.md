>[!note]
>Una misura $Y$ è detta indiretta quando è calcolata genericamente come $$Y=f(X_{1},X_{2},\cdots,X_{N})$$
>Dalla conoscenza di $N$ grandezze. La funzione $f$ prende il nome di relazione funzionale. Saranno le incertezza degli ingressi, opportunamente "combinate", a fornire l'incertezza dell'uscita: $$u_{C}(y)=\Phi[u(x_{i});f(\cdot)]$$

### Incertezza composta
>[!note]
>Sviluppiamo $f$ come serie di Taylor al primo ordine. Per farlo definiamo i coefficienti di sensibilità, che sono costanti: $$c_{i}\triangleq \left(\frac{\partial f}{\partial x_{i}}\right)_{\overline{y}}$$
>Il coefficiente di sensibilità indica come varia il misurando $Y$ in corrispondenza di una variazione del parametro $X_{i}$ di dipendenza. Quindi l'incertezza di composta di una misura indiretta: $$u_{C}(y)=\sqrt{\sum\limits^{N}_{i=1}c_{i}^{2} u^{2}(x_{i})+2\sum\limits^{N-1}_{i=1}\sum\limits^{N}_{j=i+1}c_{i}c_{j} u(x_{i},x_{j})}$$
>In generale per ciascuna incertezza $u(x_{i})$: $$u_{C}(x_{i})=\sqrt{u^{2}_{A}(x_{i})+u^{2}_{B}(x_{i})}=\sqrt{s^{2}(\overline{x}_{i})+u^{2}_{B}(x_{i})}=\sqrt{ \frac{s^{2}(x_{i})}{n}+u^{2}_{B}(x_{i})}$$

>[!tip] Casi particolari
>Se la relazione funzionale è: $$\overline{y}=n_{1}\overline{x}_{1}\pm\cdots\pm n_{i}\overline{x}_{i}\pm\cdots\pm n_{N}\overline{x}_{N}$$
>Allora: $$u_{C}^{2}(y)=\sum\limits^{N}_{i=1}n_{i}^{2}u^{2}(x_{i})$$
>Se invece la relazione funzionale è: $$\overline{y}=\overline{x}_{1}^{n_{1}}\times \cdots\times \overline{x}_{i}^{n_{i}}\times\cdots\times\overline{x}_{N}^{n_{N}}$$
>Allora: $$u_{r,C}(y)=\sqrt{\sum\limits^{N}_{i=1}n_{i}^{2}u_{r}^{2}(x_{i})}$$

