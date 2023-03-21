

## Question 1 :
##### Justifier le choix de réaliser une analyse en composantes principales sur le tableau des données brutes.
L'analyse en composante principale permet de révéler des interrelations entre caractères quantitatifs. Dans le tableau de l'exercice, les variables sont quantitatives et multidimensionnels rendant le traitement opportun à l'ACP.
##### Présenter les différentes étapes de réalisation de l'ACP
Se référer au cours de CM







## Question 2 :
##### Transformer la matrice des donnes brutes X en matrice des données centrées-réduites Z
La matrice des données brutes $X = \begin{pmatrix} 50 & 4 & 15 \\ 40 & 2 & 25 \\ 30 & 1 & 35 \\ 20 & 5 & 45 \\ 10 & 3 & 55 \\ \end{pmatrix}$
se transforme en matrice des données centrées réduites Z tel que : $z^j_i = \frac{x^j_i-\bar{x}^j}{s_j}$
Avec pour j = 1,2,3 : $\bar{x}^j = \begin{aligned}\begin{cases} \bar{x}^1&=30 \\ \bar{x}^2&=3\\ \bar{x}^3 &= 35 \end{cases} \end{aligned}$ et $\bar{s}_j = \begin{aligned}\begin{cases} \bar{s}_1&=10\sqrt(2) \\ \bar{s}_2&=\sqrt(2)\\ \bar{s}_3 &= 10\sqrt(2) \end{cases} \end{aligned}$

Ainsi, on trouve $Z = \begin{pmatrix} \frac{50-30}{10\sqrt(2)} = \sqrt(2) & \frac{\sqrt(2)}{2} & -\sqrt(2) \\ \frac{\sqrt(2)}{2} & \frac{- \sqrt(2)}{2} & \frac{-\sqrt(2)}{2} \\ 0 & -\sqrt(2) & 0 \\ \frac{-\sqrt(2)}{2} & \sqrt(2) & \frac{\sqrt(2)}{2} \\ -\sqrt(2) & 0 & \sqrt(2)\\ \end{pmatrix}$
##### Quel est l'objectif de cette opération de centrage et réduction ?
Cette opération permet de standardiser les variables, soit :
- Rend les distances entre individus invariantes (par transformations linéaires séparée de chaque variables)
- Faire fi des unités de mesures
##### En quoi consiste-t-elle au plan géométrique ?
Graphiquement, c'est un changement d'origine dans notre espace euclidien à n-dimensions. L'origine n'est plus 0 mais devient le centre du nuage de point lui-même.

## Question 3 :
##### Calculer la matrice R des coefficients de corrélation linéaire entre les variables.
Soit la matrice des coefficients de corrélation linéaire donnée par $R = \frac{1}{n}Z^TZ$.
Il faut commencer par calculer $Z^T = \begin{pmatrix} \sqrt(2) & \frac{\sqrt(2)}{2} & 0 & \frac{-\sqrt(2)}{2} & -\sqrt(2)\\ \frac{\sqrt(2)}{2} & \frac{-\sqrt(2)}{2} & -\sqrt(2) & \sqrt(2) & 0 \\ -\sqrt(2) & \frac{-\sqrt(2)}{2} & 0 & \frac{\sqrt(2)}{2} & \sqrt(2) \\ \end{pmatrix}$ 

Rappel produit matriciel : $c_{i,j} = \sum_{k} a_{i,k} b_{k,j}$
##### Que contient-elle ? Quelles propriétés en découlent ?
La matrice R contient les variances-covariances, permettant ainsi de résumer la structure de dépendance linéaire.
Les propriétés en découlant est la présence unique de 1 sur la diagonale. La covariance d'une variable envers elle-même étant égale à sa variance. La variance étant cependant standardisé, elle est égal à 1


Ainsi, $R = \begin{pmatrix} 1    & -0,1 & -1  \\ -0,1 & 1    & 0,1 \\ -1   & 0,1  & 1   \end{pmatrix}$. On observe très clairement une relation linéaire entre $\large{\vec{x_1}}$ et $\large{\vec{x_2}}$, l'un étant simplement l'inverse de l'autre.


