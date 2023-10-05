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
	_Commentaire sur la forme linéaire_ 
	$y_{i}=\beta_{1}+\beta_{2}x_{2,i}+\beta_{3}x_{3,i}+\dots+\beta_{K}x_{K,i}$ 
	Forme linéaire comme approximation locale d'une forme non-linéaire inconnue, ou comme projection linéaire
	Modèle linéaire dans les paramètres, pas nécessairement dans les variables.

Hypothèse 2 : Stricte exogénéité des régresseurs
	L'erreur doit être exogène par rapport à toutes les observations de toutes les variables explicatives.
	$E(\epsilon i|X)=0$ pour tout i = 1,2,..,N
	$E(\epsilon i|x_{1},x_{2},\dots,x_{N})=0$ pour tout i = 1,2,..,N
	$E(\epsilon i|x_{j})=0$ pour tout i,j= 1,2,..,N
