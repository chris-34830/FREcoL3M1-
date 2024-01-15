## **Notions de convergence de variables aléatoires**
### **La convergence de variable aléatoires**
- Utilisation de règles de convergence spécifique pour des variables aléatoires...
- Comportement à la limite d'une séquence de variables aléatoires : $(Z_{1},Z_{2},\dots,Z_{N}) \implies {Z_{N}}$
- Quand $N \rightarrow \infty$, est-ce que cette séquence converge ?
	Vers une valeur fixe ? $\rightarrow$ convergence
	Vers une variable aléatoire ? $\rightarrow$ convergence
	Vers une distribution connue ? $\rightarrow$ théorème central limite
##### **Définition 1: Convergence en probabilité**
> Une séquence de variables aléatoires $\{Z_N\}$ converge en probabilité vers une constante (non-aléatoire) $\alpha$ si, pour tout $\epsilon > 0$ : $$\begin{align*} \lim_{N \to \infty} \Pr(|Z_N - \alpha| > \epsilon) &= 0 \end{align*}$$
La définition stipule qu'une séquence de variables aléatoires $\{Z_N\}$ converge en probabilité vers une constante (non-aléatoire) $\alpha$ si, pour tout $\epsilon > 0$, la probabilité que la valeur de $Z_N$ soit supérieure à $\alpha + \epsilon$ tend vers $0$ lorsque le nombre de termes de la séquence, $n$, tend vers l'infini.
- La constante $a$ est appelée la limite en probabilité de $Z_n$.
- On note : $Z_N \overset{p}\to \alpha$ ou $\text{p}\lim Z_n = \alpha$ =>  $\text{p}\lim Z_n = \alpha$ indique que $Z_n$ converge en probabilité vers $\alpha$.
	La définition est généralisée à un vecteur ou une matrice de variables aléatoires en stipulant que chacun de leurs éléments converge en probabilité vers une constante propre.

##### **Définition 2: Convergence presque sûre**
>Une séquence de variables aléatoires $\{Z_n\}$ converge presque sûrement vers une constante (non-aléatoire) $\alpha$ si :
$\Pr(\lim_{N \to \infty} Z_N = \alpha) = 1$
La définition stipule qu'une séquence de variables aléatoires $\{Z_N\}$ converge presque sûrement vers une constante (non-aléatoire) $\alpha$ si, pour tout événement $\mathrm{A}$ tel que la probabilité que $\mathrm{A}$ se produise soit nulle, la probabilité que $Z_N$ appartienne à $\mathrm{A}$ pour un nombre infini de valeurs de $N$ est également nulle.
En d'autres termes, la convergence presque sûre signifie que la valeur de $Z_N$ est égale à $\alpha$ pour presque tous les $N$
- La constante $\alpha$ est appelée la limite presque sûre de $Z_n$.
	On note :
	$Z_N \overset{a.s}\to \alpha$
- La convergence presque sûre est souvent utilisée pour montrer que les estimations sont convergentes.
- La convergence presque sûre est une notion de convergence plus "forte" que la convergence en probabilité si : $Z_N \overset{a.s}\to \alpha \implies Z_N \overset{p}\to \alpha$
- Le corollaire n'est pas toujours vrai*
> Exemple :
> Soit $Z_n = \frac{1}{n}$. La suite $\{Z_n\}$ converge en probabilité vers 0. Cependant, la suite $\{Z_n\}$ ne converge pas presque sûrement vers 0, car la probabilité que $Z_n = 1$ est non nulle pour tout $n$.

##### **Définition 3: Convergence en moyenne quadratique**
>Une suite de variables aléatoires $\{Z_{N​}\}$ converge en moyenne quadratique vers une constante (non-aléatoire) $\alpha$ si :
$\lim_{N \to \infty} \mathbb{E}[Z_{N}]=\alpha$ et $\lim_{N \to \infty} \mathbb{E}[(Z_N - \alpha)^2] = 0$
La définition stipule qu'une suite de variables aléatoires $\{Z_{N​}\}$ converge en moyenne quadratique vers une constante (non aléatoire) $\alpha$ si, pour tout $\epsilon > 0$, la variance de $Z_N - \alpha$ tend vers 0 lorsque le nombre de termes de la suite, $N$, tend vers l'infini.

- La constante $\alpha$ est appelée la limite en moyenne quadratique de $Z_n$.
	On note :
	$Z_N \overset{m.s}\to \alpha$
- Ainsi, si : $\lim_{N \to \infty} \mathbb{E}[Z_{N}]=\alpha$ et $\lim_{N \to \infty} \mathbb{V}[(Z_N)] = 0$, alors $Z_N \overset{m.s}\to \alpha$	
- La convergence en moyenne quadratique est une notion de convergence plus "forte" que la convergence en probabilité si : $Z_N \overset{m.s}\to \alpha \implies Z_N \overset{p}\to \alpha$
- Le corollaire n'est pas toujours vrai*
>**Rajout personnel**
La notation $\lim_{N \to \infty} \mathbb{V}[(Z_N)] = 0$ est équivalente à la notation $\lim_{N \to \infty} \mathbb{E}[(Z_N - \alpha)^2] = 0$. 
Pour être précis ; $\lim_{N \to \infty} \mathbb{E}[(Z_N - \alpha)^2] = 0 \implies \lim_{N \to \infty} \mathbb{V}[(Z_N)] = 0$ car
$\text{Var}(Z_N - \alpha) = \mathbb{E}[(Z_N - \alpha - \mu)^2]$
$\equiv \text{Var}(Z_N - \alpha) = \mathbb{E}[Z_N^2 - 2Z_N \alpha + \alpha^2]$
$\equiv \text{Var}(Z_N - \alpha) = \mathbb{E}[Z_N^2] - 2 \alpha \mathbb{E}[Z_N] + \alpha^2$
$\equiv \lim_{N \to \infty} \mathbb{E}[Z_N^2] - 2 \alpha \mathbb{E}[Z_N] + \alpha^2 = 0$
En effet, si la variance de la suite est égale à 0, alors la moyenne des carrés des écarts à la moyenne est égale à 0. Par conséquent, les notations sont équivalentes

##### **Définition 4: Convergence en probabilité vers une variable aléatoire**
> Une séquence de variables aléatoires $\{Z_N\}$ converge en probabilité vers une variable aléatoire $Z$ si :
> $Z_{N}-Z\overset{p}\to 0$ alors $Z_{N}\overset{p}\to Z$
> (ou $\lim_{N \to \infty} \mathbb{P}(Z_N \in \mathcal{A}) = \mathbb{P}(Z \in \mathcal{A})$)
> La définition stipule qu'une suite de variables aléatoires $\{Z_{N}\}$ converge en probabilité vers une variable aléatoire $Z$ si, pour tout événement $\mathcal{A}$ tel que la probabilité que $Z$ appartienne à $\mathcal{A}$ soit non nulle, la probabilité que $\{Z_{N}\}$​ appartienne à $\mathcal{A}$ tend vers la probabilité que $Z$ appartienne à $\mathcal{A}$ lorsque le nombre de termes de la suite, $N$, tend vers l'infini.
- Ainsi :
	$Z_N - Z \overset{a.s}\to 0$ alors $Z_N \overset{a.s}\to Z$
	$Z_N - Z \overset{m.s}\to 0$ alors $Z_N \overset{m.s}\to Z$
- La convergence en probabilité vers une variable aléatoire implique une convergence en probabilité vers une constante : $\lim_{n \to \infty} \mathbb{P}(Z_n = c) = \mathbb{P}(Z = c)$
- La convergence en probabilité est une notion de convergence plus "forte" que la convergence en distribution si : $Z_N \overset{p}\to Z \implies Z_N \overset{d}\to Z$ 

##### **Définition 5: Convergence en distribution**
> Soit une suite de variables aléatoires $\{Z_n\}$ avec une fonction de distribution $F_N(Z_{N})$, on dira que $\{Z_N\}$ converge en distribution vers une variable aléatoire $Z$ si la limite de la fonction de distribution de $Z_n$ est égale à la fonction de distribution de $Z$ : $\lim_{n \to \infty} F_n(z) = F(z)$.

- On note :
	$Z_N \overset{d}\to Z$ ou $Z_N \overset{L}\to Z$ ou $Z_N \overset{d}\to F$
 - La convergence en distribution implique une convergence en probabilité si la séquence converge vers une constante, on note alors : $Z_N \overset{p}\to \alpha \implies Z_N \overset{d}\to \alpha$

##### **Définition 6 :  
> $F$ est appelé la distribution asymptotique ou la distribution limite de $Z_{N}$

Se référer définition 5

##### **Lemme 2.3. : Préservation de la convergence avec une transformation continue**
>Soit $\{Z_N​\}$ une suite de variables aléatoires convergeant en distribution vers une variable aléatoire $Z$. Soit $g$ une fonction continue. Alors, la suite ${g(Z_{N})}$ (ne dépendant pas de N) converge en distribution vers la variable aléatoire $g(Z)$.
>Si $Z_{N}\overset{p}\to a \implies g(Z_n) \overset{p}\to g(a)$ ou si $p\lim g (Z_{N})=g(p\lim Z_{N})$
Si : $Z_{N}\overset{d}\to Z \implies g(Z_n) \overset{d}\to g(Z)$

Conséquences du Lemme :
- $X_{N}\overset{p}\to \beta \text{ et } Y_{N}\overset{p}\to \alpha \implies X_{N}+Y_{N}\overset{p} \to \beta+\alpha$
- $X_{N}\overset{P}\to \beta \text{ et } Y_{N}\overset{p}\to \alpha \implies X_{N}Y_{N}\overset{p} \to \beta\alpha$
- $X_{N}\overset{p}\to \beta \text{ et } Y_{N}\overset{p}\to \alpha \implies \frac{X_{N}}{Y_{N}}\overset{p} \to \frac{\beta}{\alpha}$ tant que $a \ne 0$
- ${Y_{N}}\overset{p} \to \gamma \implies{Y_{N}}^{-1}\overset{p} \to \gamma^{-1}$ si $\gamma$ inversible

##### **Lemme 2.4. : Préservation de la convergence avec une transformation continue**
> Si les opérations matricielles sont possibles alors :
>$X_{N}\overset{d}\to X \text{ et } Y_{N}\overset{p}\to A \implies X_{N}+Y_{N}\overset{d} \to X+A$
 $X_{N}\overset{d}\to X \text{ et } Y_{N}\overset{p}\to 0 \implies Y_{N}^{'}X_{N}\overset{P} \to 0$
 $X_{N}\overset{d}\to X \text{ et } A_{N}\overset{p}\to A \implies A_{N}X_{N}\overset{d} \to AX$
 $X_{N}\overset{d}\to X \text{ et } A_{N}\overset{p}\to A \implies X_{N}^{'}A_{N}^{-1}X_{N}\overset{d} \to X^{'}A^{-1}X$

##### **Définition 7 : Equivalence asymptotique**
> Deux séquences $\{Z_{N}\}$ et $\{X_{N}\}$ sont asymptotiquement équivalentes si :
> $Z_{N}-X_{N}\overset{p}\to 0$
- On note :
	$Z_N \asymp X_N$ ou $Z_{N}=X_{N}+o_{p}$, avec $o_p$ une variable aléatoire adéquate qui converge en probabilité vers zéros.

##### **Lemme 2.5. : Méthode du Delta**
> Si $\{X_{N}\}$ est une séquence de vecteurs aléatoires de dimension K qui converge en probabilité vers un vecteur constant $\beta$ : $X_{N}\overset{p}\to\beta$ et $\sqrt{ N }(X_{N}-\beta)\overset{d}\to Z$
> On suppose une fonction $f(X_N)$ ou $\mathbb{R}^K \to \mathbb{P}^K$ continûment différentiable telle que $G(\beta) = \frac{df}{d\beta}(\beta)$ est la matrice $P \times K$ des dérivées premières évaluée en $\beta$
> alors $\sqrt{ N }[f(X_{N}-f(\beta))]\overset{d}\to G(\beta)Z$
> Ainsi, si nous avons une séquence de vecteurs aléatoires qui sont asymptotiquement normaux, et si nous appliquons une fonction continuellement différentiable à ces vecteurs, alors la séquence résultante de vecteurs aléatoires sera également asymptotiquement normale.


### **Les estimateurs sont des séquences de variables aléatoires**
On considère $\hat{\theta_{N}}$ un estimateur d'un vecteur de paramètres $\theta$ à partir d'un échantillon de taille $N$.
En augmentant la taille de l'échantillon, on a une séquence de variables aléatoires : $\{\hat{\theta_{N}}\}$.
##### **Définition 8 : Convergence d'un estimateur**
>Un estimateur d'un vecteur de paramètres est convergent (consistent) si et seulement si $\lim_{N\to\infty} \mathbb{E_\theta}[\|\hat\theta_N - \theta\|] = 0$ qui est la notation de $\hat{\theta_{N}}\overset{p}\to\theta$
- On parle parfois de «convergence faible» par opposition à la «< convergence forte » lorsque le concept de convergence presque sûre est utilisée...
##### **Définition 9 : Biais asymptotique**
> Le biais asymptotique d'un estimateur d'un vecteur de paramètres $θ$ est défini par :
> $As.Biais(\hat{\theta_N}) = \lim_{N \to \infty} \mathbb{E}(\hat{\theta_N}) - \theta$

Donc un estimateur est convergent si son biais asymptotique est nul.
##### **Définition 10 : Estimateur convergent et asymptotiquement normal**
>Un estimateur $\hat\theta_N$​ d'un vecteur de paramètres $θ$ est dit convergent et asymptotiquement normal si 
>  $\hat\theta_N$​ est convergent (consistent) donc $\hat\theta_N \xrightarrow{p} \theta$,
> $\hat\theta_N$ est asymptotiquement normal donc  $\sqrt{N}(\hat\theta_N-\theta) \xrightarrow{d} N(0, \Sigma).$ 
> La seconde partie signifie que la séquence de variables aléatoires $\sqrt{N}(\hat\theta_N-\theta)$ converge vers une distribution normale de moyenne $0$ et de variance $Σ$, lorsque la taille de l'échantillon $N$ augmente à l'infini. Se référer à la définition 5

### **Loi des grands nombres**
> Soit $Z_1, Z_2, ..., Z_N$ une suite de variables aléatoires indépendantes et identiquement distribuées (i.i.d.) de moyenne $\mu$ et de variance $\sigma^2$. Alors, $\frac{1}{N} \sum_{i=1}^N Z_i \xrightarrow{a.s.} \mu$. On parle de **forme forte**.
>Soit $X_1, X_2, ..., X_N$ une suite de variables aléatoires indépendantes et identiquement distribuées (i.i.d.) de moyenne $\mu$ et de variance $\sigma^2$. Alors, $\frac{1}{N} \sum_{i=1}^N X_i \xrightarrow{p} \mu$. On parle de **forme faible**.

##### **Loi faible des grands nombres de Khintchine**
>Soit une suite de variables aléatoires ${Z_N​}$ i.i.d. (indépendantes et identiquement distribuées) avec espérance $μ$ et variance finie. Alors, la moyenne empirique $\bar{Z_n​}=\frac{1}{n}​∑_{i=1}^{n}Z_i​$ converge en probabilité vers $μ$, c'est-à-dire que pour tout $ϵ>0$, $P\left(\left|\overline{Z}_n - \mu\right| \geq \epsilon\right) \to 0 \text{ lorsque } n \to \infty.$

Preuve (différente du cours pour que ma notation soit constante):
	En utilisant l'inégalité de Tchebychev-Bienaymé, on obtient que pour tout $\epsilon > 0$, $P\left(\left|\overline{Z}_n - \mu\right| \geq \epsilon\right) \leq \frac{\text{Var}(Z_1)}{n \epsilon^2}.$
	En prenant la limite supérieure lorsque $n \to \infty$, on obtient que $\lim_{n \to \infty} P\left(\left|\overline{Z}_n - \mu\right| \geq \epsilon\right) \leq \frac{\text{Var}(Z_1)}{\epsilon^2}.$
	Puisque $\text{Var}(Z_1)$ est fini, on a que $\lim_{n \to \infty} P\left(\left|\overline{Z}_n - \mu\right| \geq \epsilon\right) = 0$

##### **Loi faibles des grands nombre de Tchebychev**
>Soit une suite de variables aléatoires $\{Z_n\}$ i.i.d. (indépendantes et identiquement distribuées) avec espérance $\mu$ et variance $\sigma^2$. Alors, pour tout $\epsilon > 0$, $P\left(\left|\frac{1}{n} \sum_{i=1}^n Z_i - \mu\right| \geq \epsilon\right) \leq \frac{\sigma^2}{\epsilon^2 n}.$ qui n'est rien d'autre que $P(|\overline{Z}_n - \mu| \geq \epsilon) \leq \frac{\sigma^2}{\epsilon^2 n}$ 
La loi faible des grands nombres de Tchebychev nous dit que la moyenne d'échantillon $Z_{N}$​ **converge en probabilité** vers la moyenne de la population $μ$ lorsque la taille de l'échantillon $N$ tend vers l'infini.

### **Théorèmes central limite**
##### **Théorème central-limite de Lindeberg-Lévy**
>Si univariée : Soit une séquences de variables aléatoires {Zn​} i.i.d. (indépendantes et identiquement distribuées) avec espérance $μ$ et variance $σ^2$. Alors, $\sqrt{N} \left( \frac{1}{N} \sum_{i=1}^N \frac{Z_i - \mu}{\sigma} \right) \xrightarrow{d} \mathcal{N}(0, \sigma^2)$
> Si multivarié alors :
> Soit une suite de variables aléatoires ${Z_n​}$ i.i.d. (indépendantes et identiquement distribuées) avec espérance $μ$ et variance $V(Z_{i})=\Sigma>0$. Alors, $\sqrt{n} \left( \frac{1}{n} \sum_{i=1}^n Z_i - \mu \right) \xrightarrow{d} \mathcal{N}(0, \Sigma)$
##### **Théorème central-limite de Lindeberg-Feller**
>Soit une suite de variables aléatoires {Zn​} i.i.d. (indépendantes et identiquement distribuées) avec espérance $μ$ et variance $σ^2$. 
>Soit les moyennes des espérances et variances : $\overline{\mu_{N}}=\frac{1}{n} \sum_{i=1}^n \mu_i$ et ^$\overline{\sigma_{N}^2}=\frac{1}{n} \sum_{i=1}^n \sigma_i^{2}$.
>Supposons la moyenne des variances convergente vers une limite finie et définie positive, avec aucune variance d'une observation ne dominant la somme des variances : $\lim_{N \to \infty}(N\overline{\sigma_{N}^2})^{-1}\sigma^{2}=\lim_{N \to \infty}(\sum_{i=1}^n\sigma^{2}_{i})^{-1}\sigma^{2}_{i}=0$
>Alors,$\sqrt{n} \left( \frac{1}{n} \sum_{i=1}^n Z_i - \mu \right) \xrightarrow{d} \mathcal{N}(0, \sigma^2)$

## **Concepts fondamentaux avec des séries temporelles.**
### **Les processus stochastiques**
En étudiant les séries temporelles, il est nécessaire d'utiliser de nouvelle propriété asymptotiques. Les variables aléatoires sont désormais dépendantes de leur passés.
	Dans cette partie, nous ne parlerons plus de suites de variables (séquences) mais d'un processus stochastique.
- Une réalisation de ce processus stochastique est l'assignation à chaque période $t \in T$ d'une valeur possible de $Z_{T}$
- Cette realisation sera appelée une trajectoire
- Il n'est possible d'observer qu'une seule réalisation du processus stochastique
- Le processus stochastique va être supposé stable pour permettre à chaque observation temporelle d'être considéré comme une réalisation.
	Sera définie par la stationnarité, l'ergodicité, le martingale.

##### **Définition 11 : Processus stationnaire**
> Un processus stochastique ${X_T​}$ est dit stationnaire si sa distribution jointe est invariante par translation dans le temps. Cela signifie que la distribution de la réalisation $(X_t​,X_{t+}​,X_{t+2}​,\dots,X_{t_p})$ est la même que la distribution de la réalisation $(X_{t+h​},X_{t+h+1}​,X_{t+h+2}​,…,X_{t_{p}+h})$ pour tout $h∈Z$.
- Si on définit la fonction de distribution par $F$, on aura pour un processus strictement stationnaire : $F(X_t​,X_{t+}​,X_{t+2},\dots,X_{t_p})=𝐹(X_{𝑡_1+ℎ},X_{𝑡_2+ℎ}, ,X_{𝑡_𝑝+ℎ}$ pour tout ℎ ∈ ℤ et fini. 
	Ce qui importe pour la distribution est sa **position relative** dans la séquence, et non sa **position absolue** dans le temps. 
	La moyenne, la variance, des moments d’ordre supérieur (s’ils existent) restent identiques quelle que soit la valeur du décalage $ℎ$ .
- Toute fonction continue d'un processus stationnaire est aussi stationnaire
- Une série temporelle présentant une trend n'est pas stationnaire.
	Dans ce cas, on peut enlever la tendance (fonction de $t$), on aura alors un **processus stationnaire autour de sa tendance**
	- Si une série temporelle n'est pas stationnaire mais que sa différence première l'est ($\Delta X_{t}=X_{t}-X_{t-1}$) est stationnaire, on parlera de processus stochastique $\{X_t\}$ **stationnaire en différence**
- Certaines séries sont non stationnaires car leur variance augmente au cours du temps

##### **Définition 12 : Processus stationnaire en covariance**
> Un processus stochastique $\{X_T\}$ est stationnaire en covariance ou faiblement stationnaire si :
> $\mathbb{E}[X_t] = \mu$ pour tout $t = 1, 2, \dots, T$
$\mathrm{Var}[X_t] = \sigma^2 < \infty$ pour tout $t = 1, 2, \dots, T$
$\operatorname{Cov}(X_t, X_{t + s}) = f(s) = P_s$ pour tout $t = 1, 2, \dots, T$ et pour tout $s$
- $\mathbb{E}[X_t] = \mu$ signifie que l'espérance du processus est constante dans le temps.
- $\mathrm{Var}[X_t] = \sigma^2 < \infty$ signifie que la variance du processus est constante dans le temps.
- $\operatorname{Cov}(X_t, X_{t + s}) = f(s) = P_s$ (suffisante) signifie que **la covariance** entre deux réalisations du processus ne **dépend que de la différence entre les deux temps de réalisation**.
	A noter : **si la variance n'est pas constante dans le temps, alors la covariance entre deux réalisations du processus dépendra du temps, violant la troisième condition.**
- Si processus stochastique strictement stationnaire et si la variance et les covariances sont finies, alors le processus est aussi stationnaire en covariance.
	Corollaire faux.

##### **Définition 13 : Processus de bruit blanc**
>Un processus stochastique $\{X_t\}$ est un bruit blanc si :
$\mathbb{E}[X_t] = 0$ pour tout $t$
$\mathrm{Var}[X_t] = \sigma^2 < \infty$ pour tout $t$
$\operatorname{Cov}(X_t, X_{t + s}) = 0$ pour tout $t$ et pour tout $s$
Une séquence de variables aléatoires indépendantes et identiquement distribuées avec une moyenne nulle est un **bruit blanc**.

##### **Définition 14 : Ergodicité d'un processus stochastique**
> Un processus stochastique $\{X_T\}$ est dit **ergodique** si, pour deux fonctions bornées quelconques $f: R^K → R$ et $g:R^L → R$,
> $\lim_{T\to\infty} E[f(x_t,...,x_{t+k})g(x_{t+n},...,x_{t+n+L})] = E[f(x_t,...,x_{t+k})]E[g(x_{t+n},...,x_{t+n+L})]$
> Un **processus ergodique** est un processus stochastique dont les statistiques peuvent être approximées par l’étude d’une **seule réalisation du processus suffisamment longue dans le temps** (les valeurs du processus à des moments éloignés sont statistiquement indépendantes)

##### **Théorème ergodique**
> Soit un processus stochastique stationnaire et ergodique $\{X_T\}$ avec $\mathbb{E}[X_t] = \mu$, alors $\overline{x_{t}}=\frac{1}{T}\sum^T_{t=1}x_{t}\overset{a.s}\to \mu$
> Implique que  la moyenne temporelle du processus convergera vers la valeur attendue du processus lorsque la période de temps sur laquelle la moyenne est calculée tend vers l'infini. 
- Généralisation de la loi forte des grands nombres de Kolmogorov quand variables aléatoires plus dépendantes 
- Si $\{X_T\}$ est ergodique et stationnaire, toute fonction mesurable (ou continue) donne également un processus stationnaire et ergodique.

##### **Définition 15 : Martingale**
> Soit $x_t$ un élément de $z_t$, le processus stochastique $\{X_T\}$ est appelé une martingale par rapport au processus stochastique de $\{Z_T\}$ si : $E(X_t|Z_{t-1}, Z_{t-2}, ..., Z_1) = X_{t-1} \quad \text{pour tout } t \ge 2$
> La définition stipule que l'espérance conditionnelle est égale à sa valeur actuelle, compte tenu de toutes les observations passées. Cela signifie que, connaissant les informations disponibles à un moment donné, nous ne pouvons pas prédire avec certitude la valeur future du processus.

- Les variables conditionnantes $Z_{t-1}, Z_{t-2}, ..., Z_1$ sont appelées l'**ensemble d'information à la date $t-1$**.
- Le processus $\{X_t\}$ est appelé simplement une **martingale** si l'ensemble d'information comprend uniquement les valeurs passées de $X_t$ : $X_{t-1}, X_{t-2}, ..., X_1$.
- On généralise immédiatement la notion de martingale pour un vecteur.
- La marche au hasard (ou marche aléatoire) est une martingale.

##### **Définition 16 : Marche aléatoire**
>Soit $\{X_t\}$ un processus stochastique vectoriel bruit blanc (i.i.d. d'espérance nulle et de matrice de variance-covariance finie).
Une marche aléatoire $\{Z_t\}$ est la séquence de somme cumulée : $Z_1 = X_1, Z_2 = X_1 + X_2, Z_t = \sum_{s=1}^t X_s, \text{ pour } t = 1,2,..., T.$
On a : $E(Z_t|Z_{t-1}, Z_{t-2}, ..., Z_1) =E(Z_t|X_{t-1}, X_{t-2}, ..., X_1)=Z_{t-1}$
$\{X_t\}$ est un processus stochastique vectoriel bruit blanc, c'est-à-dire qu'il est constitué d'une suite de variables aléatoires indépendantes et identiquement distribuées d'espérance nulle et de matrice de variance-covariance finie.
La marche aléatoire $\{Z_t\}$ est définie comme la somme cumulée des pas aléatoires $\{X_t\}$. En d'autres termes, $Z_t$ est la valeur cumulée du processus stochastique $\{X_t\}$ jusqu'à l'instant $t$.

##### **Définition 17 : Martingale en différence**
> Un processus stochastique vectoriel $\{X_t\}$ est une martingale en différence si et seulement si son espérance conditionnelle par rapport à ses valeurs passées est nulle : $E(X_t - X_{t-1} | X_{t-1}, X_{t-2}, ..., X_1) = 0 \quad \text{pour tout } t \ge 2$
> Si l'espérance de $X_t - X_{t-1}$ est nulle, alors, connaissant les valeurs passées de $X_t$, on ne peut pas prédire avec certitude la valeur future de $X_t$.
- Le processus $\{Z_T\}$ provenant de la somme cumulée d'une martingale en différence $\{X_T\}$, est une martingale.
- L'inverse est aussi vrai !
- Une martingale en différence à une auto-corrélation nulle : $\operatorname{Cov}(X_t, X_{t -s}) = 0$ 

