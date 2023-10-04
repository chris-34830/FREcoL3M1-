#### Chapitre 1 : L'estimation par moindres carrés ordinaires (MCO)

##### QCM
- L'élément $\epsilon$ dans un modèle économétrique est habituellement appelé **le terme d'erreur**. C'est une variable qui traduit les perturbations qui affectent la variable dépendante sans être causées par la variable indépendante.
- L'élément $\beta$ dans un modèle économétrique est habituellement appelé **paramètre**. Ils permettent de quantifier les influences des autres autres facteurs sur y. 
- Les paramètres d'un modèle économétrique **décrivent la force de la relation entre la variable étudiée et les facteurs qui l'affectent**. 
- Les paramètres d'un modèle économétrique sont fixes. 
- Le modèle de régression linéaire multiple est **linéaire dans les paramètres**
- L'erreur d'un modèle économétrique **incorpore les effets des variables explicatives inobservables sur la variable dépendante**
- Dans le modèle de régression multiple $y=\beta_{0} + x_{1}\beta_{1}+x_{2}\beta_{2}+e$, $\beta_{0}$ est **l'ordonnée à l'origine**
- Une variable dépendante est également connue sous le nom de **variable de réponse**
- On a absence de multicolinéarité parfaite si **rang(X) = K**.
- On a une stricte exogénéité des variables explicatives si $E(\epsilon_{t}|X) =0$
- Le critère des moindres carrés **minimise la somme des carrés des erreurs**
- Dans l'estimation par moindres carrés, la matrice X'X est de rang-plein
- La matrice $M = I - X(X^tX)^{-1}X^t$  est **symétrique et idempotente**. La matrice M est une matrice de projection, par définition elle est réelle, symétrique et idempotente.
- Le levier d’une observation mesure **l’influence d’une observation dans une régression**
- La somme des leviers dans une régression est égale **au nombre de variables explicatives**


###### Vrai ou faux
- Le critère des moindres carrés consiste à minimiser la somme des carrés des résidus
**Vrai**
- L’estimation d’une constante est nécessaire pour que la moyenne des résidus soit nulle.
**Vrai**? Il semble que $E[\epsilon]=0$ définit la constante?
- La covariance de l'échantillon entre un régresseur et les résidus des moindres carrés ordinaires (MCO) dépend du signe du paramètre estimé pour ce régresseur
?
- Les résidus sont distribués symétriquement autour de zéro.
?
- Dans une régression multiple, il y a 𝑁 − 𝐾 degrés de liberté dans les résidus de moindres carrés ordinaires.
**Faux**. Dans une régression multiple, il y a N - K - 1 avec K le nombre de variables et 1 l'ordonnée à l'origine.
- Le $R^2$ est le rapport de la variation expliquée par rapport à la variation totale.
**Vrai**. Le $R^2$ représente la fraction de la variation de $y$ qui est expliquée par $x$ au sein de l'échantillon. 
- Le $\bar{𝑅}^2$ est toujours supérieur au $R^2$.
**Faux**. Le  $\bar{𝑅}^2$ ne peut pas être supérieur à $R^2$. Le $\bar{𝑅}^2$ peut-être au mieux égal à $R^2$ quand le modèle ne comprend qu'une unique variable prédictive, cependant en ajoutant des variables prédictives on ajoute une pénalité qui ajuste l'estimation de la variance de l'erreur en fonction du nombre de degré de liberté. (Augmentant avant le nombre de variable prédictive)
- Le  $\bar{𝑅}^2$ peut être négatif.
**Vrai**
- Le $R^2$ est le coefficient de corrélation entre la variable dépendante et la variable dépendante calculée sur le plan de régression.
**Faux**
- La matrice de projection 𝑴 est orthogonale à la matrice de projection 𝑷.
Par construction

##### Exercices théoriques
- En supposant deux matrices carrées A et B de même dimension, démontrez la propriété de circularité de la trace : tr(AB) = tr(BA)
Soit $A = [a_{ij}]$ et $B =[b_{ij}]$ des matrices carré de taille n
Le produit matriciel donne $(AB)_{ij} =\sum^n_{k=1}a_{ik}b_{kj}$ et  $(BA)_{ij} =\sum^n_{k=1}b_{ik}a_{kj}$ ainsi, $tr(AB)=\sum^n_{i=1}(AB)_{ii}$
$=\sum^n_{i=1}\sum^n_{k=1}a_{ik}b_{ki}$
$= \sum^n_{i=1}\sum^n_{k=1}b_{ik}a_{ki}$
$=\sum^n_{k=1}(AB)_{kk} = tr(BA)$ cqfd
- Soit A une matrice de dimension $r \times c$ , démontre que la trace de $A^tA$ est la somme des carrés de tous les éléments de A  :$(A^tA)= \sum^c_{i=1}\sum^r_{k=1}a_{ik}^2$$ 
La transposé ne modifie la matrice qu'en effectuant une symétrie axiale des coefficients tout en conservant sa diagonale principale, ainsi la démonstration de  $Tr(A^tA) = Tr(AA) =\sum^c_{i=1}\sum^r_{k=1}a_{ik}^2$ se fait facilement : 
$(A^tA)_{ij} = \sum^r_{k=1}(A^t)_{ik}\times(A)_{kj}$
$= \sum^r_{k=1}(A)_{ik}\times(A)$
$=\sum^r_{k=1}a_{ik}\times a_{jk}$
par conséquent, $(A^tA)_{ii}=\sum^r_{k=1}a^2_{ik} \implies tr(A^tA) \sum^c_{i=1}\sum^r_{k=1}a_{ik}^2=\sum_{1\le i,j \le n}a^2_{ij}$ cqfd
- Expliquez pourquoi chacune des propositions suivantes est vraie
-$(A+A^t)B = AB+ A^tB$
pour simplifier la notation notons $A^t = C$ ainsi 
$(A+C)B = \sum^n_{k=1}(a+c)_{kj}b_{ik}$
$=\sum^n_{k=1}a_{kj}b_{ik}+c_{kj}b_{ik}$ 
$=(AB)_{ij}+(CB)_{ij}=(AB+CB)_{ij}$ 
Le produit matriciel est distributif.
- $tr(B^tB)=tr(BB^t)$ 
Même démonstration que pour la question 1 cependant dans notre cas $A=B^t$ 

- Traquenard sur Obsidian, faites à l'écrit, démonstration trop longue pour l'écrire ici
-Vérifiez chaque proposition avec : A = $\begin{pmatrix} -1 & 2\\ 7 & 3  \end{pmatrix}$, B = $\begin{pmatrix} 6 & 8 &-1 &0 \\ 2 & 3&1&4 \end{pmatrix}$ et $x^t=\begin{pmatrix} 1 &1&2&3\end{pmatrix}$
