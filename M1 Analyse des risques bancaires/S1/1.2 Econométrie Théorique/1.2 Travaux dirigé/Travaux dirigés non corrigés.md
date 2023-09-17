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
- La matrice 

###### Vrai ou faux
- Le critère des moindres carrés consiste à minimiser la somme des carrés des résidus

##### Exercices théoriques
- En supposant deux matrices carrées A et B de même dimension, démontrez la propriété de circularité de la trace : tr(AB) = tr(BA)
Soit $A = [a_{ij}]$ et $B =[b_{ij}]$ des matrices carré de taille n
Le produit matriciel donne $(AB)_{ij} =\sum^n_{k=1}a_{ik}b_{kj}$ et  $(BA)_{nn} =\sum^n_{k=1}b_{ik}a_{kj}$ ainsi, $tr(AB)=\sum^n_{i=1}(AB)_{ii}= \sum^n_{i=1}\sum^n_{k=1}a_{ik}b_{ki}= \sum^n_{i=1}\sum^n_{k=1}b_{ik}a_{ki}=\sum^n_{k=1}(AB)_{kk} = tr(BA)$ 
- Soit A une matrice de dimension $r \times c$ , démontre que la trace de $A^tA$ est la somme des carrés de tous les éléments de A  :$(A^tA)= \sum^c_{i=1}\sum^r_{k=1}a_{ik}^2$ 
La transposé n'affecte pas la diagonale principale d'une matrice ainsi, $Tr(A^tA) = Tr(AA) =\sum^c_{i=1}\sum^r_{k=1}a_{ik}^2$ * Démontrable de la même façon que $tr(AB) = tr(BA)$
- Expliquez pourquoi chacune des propositions suivantes est vraie
-$(A+A^t)B = AB+ A^tB$
pour simplifier la notation notons $A^t = C$ ainsi $(A+C)B = \sum^n_{k=1}(a+c)_{kj}b_{ik} =\sum^n_{k=1}a_{kj}b_{ik}+c_{kj}b_{ik}=(AB)_{ij}+(CB)_{ij}=(AB+CB)_{ij}$ 
Le produit matriciel est distributif.
-$tr(B^tB)=tr(BB^t)$ 
Même démonstration que pour la question 1 cependant dans notre cas $A=B^t$ 
-?
-Vérifiez chaque proposition avec : A = $\begin{pmatrix} -1 & 2\\ 7 & 3  \end{pmatrix}$, B = $\begin{pmatrix} 6 & 8 &-1 &0 \\ 2 & 3&1&4 \end{pmatrix}$ et $x^t=\begin{pmatrix} 1 &1&2&3\end{pmatrix}$
