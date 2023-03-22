

## Question 1 :
##### Justifier le choix de réaliser une analyse en composantes principales sur le tableau des données brutes.
L'analyse en composante principale permet de révéler des interrelations entre caractères quantitatifs. Dans le tableau de l'exercice, les variables sont quantitatives et multidimensionnels rendant le traitement opportun à l'ACP.
##### Présenter les différentes étapes de réalisation de l'ACP
Se référer au cours de CM







## Question 2 :
#### Transformer la matrice des donnes brutes X en matrice des données centrées-réduites Z
La matrice des données brutes $X = \begin{pmatrix} 50 & 4 & 15 \\ 40 & 2 & 25 \\ 30 & 1 & 35 \\ 20 & 5 & 45 \\ 10 & 3 & 55 \\ \end{pmatrix}$
se transforme en matrice des données centrées réduites Z tel que : $z^j_i = \frac{x^j_i-\bar{x}^j}{s_j}$
Avec pour j = 1,2,3 : $\bar{x}^j = \begin{aligned}\begin{cases} \bar{x}^1&=30 \\ \bar{x}^2&=3\\ \bar{x}^3 &= 35 \end{cases} \end{aligned}$ et $\bar{s}_j = \begin{aligned}\begin{cases} \bar{s}_1&=10\sqrt(2) \\ \bar{s}_2&=\sqrt(2)\\ \bar{s}_3 &= 10\sqrt(2) \end{cases} \end{aligned}$

Ainsi, on trouve $Z = \begin{pmatrix} \frac{50-30}{10\sqrt(2)} = \sqrt(2) & \frac{\sqrt(2)}{2} & -\sqrt(2) \\ \frac{\sqrt(2)}{2} & \frac{- \sqrt(2)}{2} & \frac{-\sqrt(2)}{2} \\ 0 & -\sqrt(2) & 0 \\ \frac{-\sqrt(2)}{2} & \sqrt(2) & \frac{\sqrt(2)}{2} \\ -\sqrt(2) & 0 & \sqrt(2)\\ \end{pmatrix}$
#### Quel est l'objectif de cette opération de centrage et réduction ?
Cette opération permet de standardiser les variables, soit :
- Rend les distances entre individus invariantes (par transformations linéaires séparée de chaque variables)
- Faire fi des unités de mesures
#### En quoi consiste-t-elle au plan géométrique ?
Graphiquement, c'est un changement d'origine dans notre espace euclidien à n-dimensions. L'origine n'est plus 0 mais devient le centre du nuage de point lui-même.

## Question 3 :
#### Calculer la matrice R des coefficients de corrélation linéaire entre les variables.
Soit la matrice des coefficients de corrélation linéaire donnée par $R = \frac{1}{n}Z^TZ$.
Il faut commencer par calculer $Z^T = \begin{pmatrix} \sqrt(2) & \frac{\sqrt(2)}{2} & 0 & \frac{-\sqrt(2)}{2} & -\sqrt(2)\\ \frac{\sqrt(2)}{2} & \frac{-\sqrt(2)}{2} & -\sqrt(2) & \sqrt(2) & 0 \\ -\sqrt(2) & \frac{-\sqrt(2)}{2} & 0 & \frac{\sqrt(2)}{2} & \sqrt(2) \\ \end{pmatrix}$ 

Rappel produit matriciel : $c_{i,j} = \sum_{k} a_{i,k} b_{k,j}$

Ainsi, $R = \begin{pmatrix} 1    & -0,1 & -1  \\ -0,1 & 1    & 0,1 \\ -1   & 0,1  & 1   \end{pmatrix}$. 
#### Que contient-elle ? Quelles propriétés en découlent ?
La matrice R contient les variances-covariances, permettant ainsi de résumer la structure de dépendance linéaire.
Les propriétés en découlant est :
- la présence unique de 1 sur la diagonale. La covariance d'une variable envers elle-même étant égale à sa variance. La variance étant cependant standardisé, elle est égal à 1
- Symétrie des valeurs, la covariance est commutatitve. Cov(A,B) = Cov(B,A)

 #### Quel est l'objectif de cette opération ? L'ACP est-elle réalisable ?
L'objectif de l'opération est d'identifier une corrélation entre plusieurs variables afin de réduire nos axes a étudier. Dans l'exercice, nous observons très clairement une dépendance entre $\large{\vec{x_1}}$ et $\large{\vec{x_2}}$. Les deux vecteurs sont linéairement dépendantes au sens opposé. Nous pourrons donc en supprimer l'un des deux pour notre étude en ACP.

## Question 4 :
#### Calculer les valeurs propres $\lambda_j$ associées à la matrice R. Que représentent-elles dans le contexte de l'ACP ? Quelles propriétés doivent-elles vérifier ?
##### Calcul valeur propre
Cherchons le polynôme caractéristique : $p_R(\lambda) det(R-\lambda) = \begin{pmatrix} 1-\lambda    & -0,1 & -1  \\ -0,1 & Cherchons le polynôme caractéristique : $p_R(\lambda) = 0 \equiv det(R-\lambda) = \begin{pmatrix} 1-\lambda    & -0,1 & -1  \\ -0,1 & 1-\lambda    & 0,1 \\ -1   & 0,1  & 1-\lambda   \end{pmatrix}$ = 0
Rappel de la règle de Sarrus :
Soit la matrice d'exemple $A = \begin{pmatrix} A & B & C & A & B \\ D & E & F & D & E \\ G & H & I & G & H \end{pmatrix}$ son déterminant est la somme des produits des diagonales. Les diagonales "descendantes" sont positives (en vert) tandis que les "ascendantes" sont négatives (en orange), ce qui donne : $det(A) = \textcolor{Green}{(+)AEI + BFG + CDH} \textcolor{Orange}{- GEC - HFA - IDB}$ 

En utilisant la règle de Sarrus on ré-écrit (au brouillon) R commé étant la matrice $R_s = \begin{pmatrix} 1-\lambda    & -0.1 & -1 & 1-\lambda  & -0.1 \\ -0.1 & 1-\lambda    & 0,1 & -0.1 & 1-\lambda \\ -1 & 0.1 & 1-\lambda & -1 & 0.1 \end{pmatrix}$ On s'intéresse aux diagonales de $R_s$ on trouve le polynome caractéristique de R $p_R(\lambda)= (1-\lambda)^3 + (-0.1)(0.1)(-1)+(-1)(-0.1)(0.1) - (-1)(1-\lambda)(-1) - (0.1)(0.1)(1-\lambda)-(1-\lambda)(-0.1)(-0.1)$ se simplifiant en : $\textcolor{Red}{(-\lambda)^3 -1.98\lambda+3\lambda^2 \Rightarrow \lambda(\lambda^2-1.98+3\lambda) \equiv -\lambda(\lambda^2-3\lambda+1.98)}$ (Les étapes de simplification disponible [[TD 1 Analyse en composante principale#^23e73c^|ici]])
On reconnait dans $(-\lambda)(\lambda^2-3\lambda+1.98)$ l'expression d'un polynome du second degré si on ne tient pas compte du monôme $(-\lambda)$ ainsi, on calcul le discriminant :
$\Delta = (3)^2 - 4(1)(1.98) = 1.08$. On observe que $\Delta > 0$ donc il existe deux solutions différentes qui permettent de résoudre l'équation $\lambda^2-3\lambda+1.98 = 0$. (On pouvait s'attendre à trouver au pire un discriminant égale à 0, la matrice étant symétrique ses valeurs propres sont des nombres réelles par définition)
Ainsi ; $\lambda_i = \frac{-b\pm\sqrt(\Delta)}{2a}$
$\lambda_1 = 2.02, \lambda_2 = 0.98$ sont les solutions de l'équation du polynome de second degré.
Ainsi, nous avons trois valeurs propres : $\lambda_1 = 2.02, \lambda_2 = 0.98, \lambda_3 =0$ 

###### Etape de simplification
Soit l'expression initiale : $(1-\lambda)^3 + (-0.1)(0.1)(-1)+(-1)(-0.1)(0.1) - (-1)(1-\lambda)(-1) - (0.1)(0.1)(1-\lambda)-(1-\lambda)(-0.1)(-0.1)$
Première partie ; Selon le *binome de Newton* $(1-\lambda)^3$ se développe comme suit :$1^3 - 3(1^2)(\lambda) + 3(1)(\lambda)^2- \lambda^2 \equiv 1-3\lambda+3\lambda^2 - \lambda^3$ ^23e73c

La seconde partie se simplifie comme suit ; $(-0.1)(0.1)(-1)+(-1)(-0.1)(0.1) - (-1)(1-\lambda)(-1) - (0.1)(0.1)(1-\lambda)-(1-\lambda)(-0.1)(-0.1)$ = $(0.01)+(0.01)-(1-\lambda)-(0.01-0.01\lambda)-(0.01-0.01\lambda)$ en retirant les parenthèses et en additionnant on se retrouve avec : $0.02-1+\lambda-0.01+0.01\lambda-0.01+0.01\lambda \\ \Rightarrow 0.02-0.02 -1+1.02\lambda\\ \Rightarrow 1.02\lambda-1$

En ajoutant la première partie à la seconde on trouve $1-3\lambda+3\lambda^2 + 1.02\lambda -1 =-1.98\lambda+3\lambda^2-\lambda^3$
En sortant un lambda on fini avec : $\lambda (\lambda^2+3\lambda-1.98) \equiv -\lambda(\lambda^2-3\lambda+1.98)$

#### Que représentent-elles dans le contexte de l'ACP ? Quelles propriétés doivent-elles vérifier ?