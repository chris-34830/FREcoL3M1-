 

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
L'objectif de l'opération est d'identifier une corrélation entre plusieurs variables afin de réduire nos axes a étudier. Dans l'exercice, nous observons très clairement une dépendance entre $\large{\vec{x_1}}$ et $\large{\vec{x_3}}$. Les deux vecteurs sont linéairement dépendantes au sens opposé. Nous pourrons donc en supprimer l'un des deux pour notre étude en ACP.

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

##### Que représentent-elles dans le contexte de l'ACP ? Quelles propriétés doivent-elles vérifier ?
Dans le cadre d'une ACP, les valeurs propres mesurent la part d'inertie d'une variance. 
Ainsi, $\frac{2.02*100}{3} = 67$% le premier axe factorielle permet d'extraire 67% des informations contenues dans le tableau de données initiales.
Il est nécessaire d'avoir toujours une nombre de valeur propre égal au nombre de variables p. Ici, nous avons 3 variables et 3 valeurs propres donc c'est bien vérifié.

#### Déterminer les vecteurs propres normés associés aux différentes valeurs propres. Que représentent-ils ?

Pour rappel,la matrice $R = \begin{pmatrix} 1    & -0,1 & -1  \\ -0,1 & 1    & 0,1 \\ -1   & 0,1  & 1   \end{pmatrix}$
Ainsi ; $R = \begin{pmatrix} 1    & -0,1 & -1  \\ -0,1 & 1    & 0,1 \\ -1   & 0,1  & 1   \end{pmatrix} \times \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \lambda_i \times \begin{pmatrix} x \\ y \\ z \end{pmatrix}$
Pour $\lambda_i = \lambda_1 = 2.02$ on a : 
$R = \begin{pmatrix} 1    & -0,1 & -1  \\ -0,1 & 1    & 0,1 \\ -1   & 0,1  & 1   \end{pmatrix} \times \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 2,02x \\ 2,02y \\ 2,02z \end{pmatrix}$
On peut voir que $x = -z$, chose déjà dite plus haut lorsque l'on a montré que dépendance linéaire au sens opposé lors de la question 3.
On transforme donc $R = \begin{pmatrix} 1    & -0,1 & -1  \\ -0,1 & 1    & 0,1 \\ -1   & 0,1  & 1   \end{pmatrix} \times \begin{pmatrix} x \\ y \\ -x \end{pmatrix} = \begin{pmatrix} 2x-0.1y \\ y-0.2x \\ 0.1y-2x \end{pmatrix}$ on se rend compte que $y=-0.2x$ donc on trouve le vecteur suivant $\vec{v_1} = \begin{pmatrix} 1x \\ 0.2x \\ -1x \end{pmatrix}$
Le calcul de la norme se fait comme suit $\left\lVert v_1 \right\rVert = \frac{1}{\sqrt(1^2+0.2^2+(-1)^2)} = \frac{1}{\sqrt{2.04}}$ donc le vecteur normé est $\left\lVert \vec{v_1} \right\rVert =  \begin{pmatrix} 0.7 \\ -0.14 \\ -0.7 \end{pmatrix}$
Pour finir, l'espace normé est ainsi $\begin{pmatrix} 0.7 & 0.097 & 0.707\\ -0.14 & 0.989 & 0 \\ -0.7 &-0.097 & 0.707 \end{pmatrix}$
Ils représentent les vecteurs directeurs des axes factoriels et doivent être orthogonaux deux à deux (Le produit **scalaire** des deux vecteurs issue de l'espace normée doit être égal à 0)




## Question 5 :
#### Calculer la matrice de dispersion des individus V
-

#### A quoi correspond-elle ? Quelles sont ses propriétés ?
Propriété : 
- Symétrique (donc carrée)
Correspond :
- Dispersion des individus




#### A quoi correspond-elle ? Quelles sont ses propriétés ?
$\lambda_{Ri} = \lambda_{Vi}$


## Question 6 :
#### Déterminer les coordonnées des individus dans le nouvel espace constitué par les deux premiers axes factoriels (F1 et F2).
La matrice des coordonnés des individus n'est autre que le produit de la matrice des données centrées-réduites Z et l'espace normé du changement de base.
$C = \begin{pmatrix} \sqrt(2) & \frac{\sqrt(2)}{2} & -\sqrt(2) \\ \frac{\sqrt(2)}{2} & \frac{- \sqrt(2)}{2} & \frac{-\sqrt(2)}{2} \\ 0 & -\sqrt(2) & 0 \\ \frac{-\sqrt(2)}{2} & \sqrt(2) & \frac{\sqrt(2)}{2} \\ -\sqrt(2) & 0 & \sqrt(2)\\ \end{pmatrix} \times \begin{pmatrix} 0.7 & 0.097 & 0.707\\ -0.14 & 0.989 & 0 \\ -0.7 &-0.097 & 0.707 \end{pmatrix} = \begin{pmatrix} 1.88 & 0.97  \\ 1.09 & -0.56 \\ 0.2 & -1.4 \\ -1.19 & 1.26 \\ -1.98 & -0.27 \end{pmatrix}$

#### Calculer les contributions absolues et contributions relatives des individus (CTA et CTR). Que représentent-elles ? En quoi sont-elles utiles ?
Les contributions absolues (CTA) mesurent l'importance des individus dans l'apparition de l'axe factoriel considéré. Plus le CTA est élevée, plus il contribue à faire apparaitre l'axe. Elle se calcul comme suit : CTA$_{i,r}\frac{(c_i^r)^2}{n\lambda_r}$. 
