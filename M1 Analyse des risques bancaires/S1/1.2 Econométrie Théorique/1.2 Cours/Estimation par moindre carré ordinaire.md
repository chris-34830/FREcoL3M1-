### Le modèle de régression linéaire classique
#### Le modèle de régression simple
	L'analyse de la régression
- Modélisation d'une relation pour expliquer une variable dépendante, notée y.
- Par des variables explicatives (régresseurs), notées x.

| X                   | Y                     |
| ------------------- | --------------------- |
| Variable dépendante | Variable indépendante |
| Variable expliquée  | Variable explicative  |
| Variable de réponse | Variable de contrôle  |
| Variable prédite    | Variable prédictive   |
| Variable endogène   | Variable exogène      |

	L'échantillon ou les données
- C'est un ensemble d'observations sur plusieurs variables ou caractéristiques
- Echantillon de N observations indicées : i = 1,2,3,..., N;
	Une coupe instantanée (données longitudinales) est observée sur différentes unités statistiques à une même période
	Elle est e général non ordonnée !
- Echantillon de T observations sur séries temporelles : t=1,2,3,...,T
	Une série temporelle (ou chronologique) est observée sur une même unité statistique pour plusieurs périodes de temps (année, trimestres, jours, ...)
	Une série temporelle a un ordre naturel : passé -> présent -> futur

	Les observations 
- Ici, une seule variable dépendante ($y_{i}$)
	- et plusieurs variables explicatives ($x_{k,i}$) : k = 1,2,3,...,K :
$$x_{i}=(x_{1,i},x_{2,i},\dots,x_{k,i},\dots,x_{K,i})$$
- En général, la première variable explicative est constante : $x_{1,i}=1$
- Dans la régression simple : $K=2 \rightarrow x_{i}=(1,x_{2,i})'$
- Dans la régression multiple : $K>2 \rightarrow x_{i}=(1,x_{2,i},\dots,x_{k,i},\dots,x_{K,i})'$
- Régression* de y sur les variables explicatives (régresseurs) $x_{k}$

	Le modèle
- La variable dépendante$(y_{i})$ et les variables explicatives $(x_{k,i})$ sont considérées comme des **variables aléatoires**
- Les observations sont considérées comme des **réalisations** d'un tirage aléatoire !
- Ici les régresseurs sont aussi des variables aléatoires parce que : 
	On ne contrôle pas les variables explicatives
	En sciences sociales et plus particulièrement en économie, on est rarement dans le cadre d'expérience contrôlées (randomisée), mais plutôt avec des **données observationnelles**
	Le cas des régresseurs "fixes" est un cas particulier du cas des régresseurs aléatoires
- Un **modèle économétrique** est un ensemble de restrictions sur la distribution conjointe des variables dépendante et explicatives
- C'est un ensemble de distributions conjointes qui satisfont un ensemble d'hypothèses
- Comme la relation n'est pas parfaite, on introduit une variable supplémentaire pour tenir compte d'autres éléments $\rightarrow$**l'erreur** : $\epsilon$
	Commentaire sur l'erreur
	- L'erreur est aussi appelée aléas ou perturbation
	- Elle correspond à des éléments imprédictibles des aléas, des comportements économiques, humains ou sociaux...
	- Elle mesure les incertitudes du modèle
	- Elle incorpore des effets inobservables
	- Elle capture les effets d'un grand nombre de variables omises (* Voir hypothèse, MISE EN PAGE NECESSAIRE)
	- Elle prend en compte les erreurs de mesure sur la variable dépendante.
	- L'erreur est une variable aléatoire avec des moments (espérance, variance,...) et une distribution à déterminer

**Hypothèse 1 : Linéarité du modèle**
	$y_{i}=\beta_{1}+\beta_{2}x_{2,i}+\beta_{3}x_{3,i}+\dots+\beta_{K}x_{K,i}+\epsilon_{i}$ pour i=1,2,...,N
	La relation entre les variables explicatives et la variable dépendante est **linéaire**
	L'erreur est **additive**
	Il n'y a pas d'erreurs de mesure sur les variables explicatives x.
	-> Le modèle est correctement spécifié
	$y_{i}=\beta_{1}+\beta_{2}x_{2,i}+\beta_{3}x_{3,i}+\dots+\beta_{K}x_{K,i}+\epsilon_{i} = \sum_{k=1}^K\beta_{k}x_{K,i}+\epsilon_{i}$
	$\beta_{1}+\beta_{2}x_{2,i}+\beta_{3}x_{3,i}+\dots+\beta_{K}x_{K,i}$ est la **fonction de régression**
	Les paramètres (ou coefficients) $\beta_{k}$ sont les coefficients de régression.
	Ils représentent l'effet marginal, toutes choses égales par ailleurs, d'une variation de la variable $x_{k,i}$ sur la variable dépendante $y_{i}$ : $\beta_{k}=\frac{\nabla y_{i}}{\nabla x_{k,i}}$
	La linéarité implique que les effets marginaux sont constants pour toutes les observations (individus)
	__Commentaire sur la forme linéaire__
	$y_{i}=\beta_{1}+\beta_{2}x_{2,i}+\beta_{3}x_{3,i}+\dots+\beta_{K}x_{K,i}$ 
	Forme linéaire comme approximation locale d'une forme non-linéaire inconnue, ou comme projection linéaire
	Modèle linéaire dans les paramètres, pas nécessairement dans les variables.

**Hypothèse 2 : Stricte exogénéité des régresseurs**
	L'erreur doit être exogène par rapport à toutes les observations de toutes les variables explicatives.
	$E(\epsilon i|X)=0$ pour tout i = 1,2,..,N
	$E(\epsilon i|x_{1},x_{2},\dots,x_{N})=0$ pour tout i = 1,2,..,N
	$E(\epsilon i|x_{j})=0$ pour tout i,j= 1,2,..,N
	Si nous considérons la distribution des (NK+N) variables aléatoires (cf ; la matrice des variables explicatives + le vecteurs des erreurs), la distribution conditionnelle pour chaque observation $i : f(\epsilon_{1},\epsilon_{2},\dots,\epsilon_{n},x_{1},x_{2},\dots,x_{n})$ aura une espérance nulle $E(\epsilon_{i}|x_{j})=E(\epsilon_{i}|X)=0$ pour l'ensemble de l'échantillon.
	Cette hypothèse est fondamentale pour qu'on puisse trouver un estimateur des paramètres $\beta$ possédant les bonnes propriétés statistiques
	__Implications de l'hypothèse d'exogénéité stricte__
	- L'espérance inconditionnelle de l'erreur est nulle
	$E(\epsilon_{i})=E_{X}[E(\epsilon i|X)]=0$ pour tout i = 1,2,..,N
	- Les régresseurs sont orthogonaux aux termes d'erreurs pour toutes les observations
	$E(x_{j}e_{i})=0_{k}$ => Espérance de leur produit scalaire = 0
	C'est la condition d'orthogonalité. $E(X'\epsilon)=0_{k}$
	Par construction, si la condition d'orthogonalité est validé, la corrélation est nulle. 

Hypothèse 3 : Absence de multicolinéarité parfaite
	Le rang de la matrice X de dimension $N \times K$ est K avec une probabilité 1, se traduit comme : $rang(X)=K$ 
	Ainsi, aucune colonne de X n'est une combinaison linéaire parfaite des autres colonnes de X. 
	Cette hypothèse rend possible l'utilisation des MCO et permet l'identification des paramètres du modèle. 
	Cependant, pour que cette hypothèse soit vraie, il faut au moins que $N \geq K$
	Si H3 n'est pas validé, alors les régresseurs sont parfaitement colinéaires.

Hypothèse 4 : Les erreurs ont une matrice de variance-covariance sphérique
	Homoscédasticité conditionnelle : Les termes d'erreur $\epsilon_{i}$ de toutes les observations ont la même variance conditionelle

 Hypothèse 5 : Normalité des erreurs
	 Cette hypothèse n'est pas fondamentale pour l'obtention d'un bon estimateur, mais elle est nécessaire pour obtenir des propriétés en petits échantillons.
	 Si on suppose les observations indépendantes, la fonction de densité conjointe des erreurs est le produit des fonctions de densité marginale de chaque erreur : $f(\epsilon | X) = f(\epsilon_1 | X) \cdot f(\epsilon_2 | X) \cdots f(\epsilon_n | X) = \prod_{i=1}^n f(\epsilon_i | X)$
	Avec $f(.)$ la fonction de densité de la loi normale univariée : $\epsilon_i \sim \mathcal{N}(0, \sigma^2) \rightarrow f(\epsilon_i | X) = \frac{1}{\sqrt{2 \pi \sigma^2}} \exp \left( - \frac{\epsilon_i^2}{2 \sigma^2} \right)$
	Dans ce cas, les erreurs suivent une loi normale multivariée de dimension N : $\epsilon \sim \mathcal{N}(0, \sigma^2 I_N) \rightarrow f(\epsilon | X) = \frac{1}{(2 \pi \sigma^2)^{N/2}} \exp \left( - \frac{\epsilon_{1}^2}{2 \sigma^2} \right)$