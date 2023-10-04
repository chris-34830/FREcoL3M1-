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
- 