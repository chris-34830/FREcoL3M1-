
## Prévision d'une série chronologique avec les méthodes de prévision traditionnelles

#### **Exercice 1**
Série : 22,13,10,29,22,14,12,31,23,15,13,33,25,16,15,34
Par trimestre
##### **Donner la représentation graphique de la chronique. Analyser**.
```chart
type: line
labels: [T1, T2, T3, T4, T1, T2, T3, T4,T1, T2, T3, T4,T1, T2, T3, T4]
series:
  - title: 
    data: [22, 13, 10, 29, 22,14,12,31,23,15,13,33,25,16,15,34]
tension: 0.2
width: 50%
labelColors: false
fill: false
beginAtZero: true
bestFit: true
bestFitTitle: undefined
bestFitNumber: 0
```
L'analyse graphique nous permet de voir :
- La série suit une tendance saisonnière, il existe une composante cyclique ; on remarque presque une représentation sinusoïdal. 
- La prévision est rigide.
- Le modèle est additive : l'amplitude est constante autour de la tendance.

##### **Constituer les tableaux de Buys-Ballot et Buys-Ballot classé**.

- Tableau de Buys-Ballot : 

| Date                | T1    | T2    | T3    | T4    | $x_{i.}$ | $s_{i.}$ |
| ------------------- | ----- | ----- | ----- | ----- | -------- | ------------------- |
| Année 1      | 22    | 13    | 10    | 29    | 18,5     | 8,66          |
| Année 2      | 22    | 14    | 12    | 31    | 19,75    | 8,653         |
| Année 3      | 23    | 15    | 13    | 33    | 21       | 9,092         |
| Année 4      | 25    | 15    | 16    | 34    | 22,5     | 8,888         |
| $x_{.j}$            | 23    | 14,5  | 12,75 | 31,75 | $x_{..}$ | $s_{..}$ |
| $s_{.j}$ | 1,414 | 1,291 | 2,082 | 2,217 | 20,4375  | 8,0412              |
Attention, l'écart type est à exprimer sans biais autrement, le test de Buys-Ballot ne sera pas juste.
Ainsi, ${s}^2=\frac{n}{n-1}\sigma^{2} = \frac{\left( \frac{\sum x_{i}^2}{n} \right)-\bar{x}^2}{n-1}$

- Tableau de Buys-Ballot classé : 

|      |     |     |     |     |
| ---- | --- | --- | --- | --- |
| 2018 | T4  | T1  | T2  | T3  |
| 2019 | T4  | T1  | T2  | T3  |
| 2020 | T4  | T1  | T2  | T3  |
| 2021 | T4  | T1  | T2  | T3  |

#### **Effectuer l'analyse de la variance.**
Rappel des formules :

| Somme des carrés                                        | Degré de liberté | Désignation         | Variance                                                                   |
| ------------------------------------------------------- | ---------------- | ------------------- | -------------------------------------------------------------------------- |
| $S_{P}=N\sum(x_{.j}-x..)^2$                             | $P-1$            | Variance période    | $V_{P}=\frac{N\sum(x_{.j}-x_{..})^2}{P-1}$                                 |
| $S_{N}=P\sum(x_{i.}-x_{..})^2$                          | $N-1$            | Variance année      | $V_{A}=\frac{P\sum(x_{i.}-x_{..})^2}{N-1}$                                 |
| $S_{R}=\sum_{i}\sum_{j}(x_{i.}-x_{.j}-x_{ij}+x_{..})^2$ | *$(P-1)(N-1)$*   | Variance résiduelle | $V_{R}=\frac{\sum_{i}\sum_{j}(x_{i.}-x_{.j}-x_{ij}+x_{..})^2}{(P-1)(N-1)}$ |
| $S_{T}=\sum(x_{ij}-x_{..})^2$                           | $NP-1$           | Variance totale     | $V_{T}=\sum$                                                               

#### **Test de Fisher**
- Influence du facteur colonne
$H_{0}$ : pas d'influence du facteur colonne (Pas saisonnalité)
$H_{1}$ : Influence du facteur colonne (saisonnalité):
RDD :
$F_{c} > F_{1-k}$ on rejette $H_{0}$
Loi : 
$F_{c}=\frac{V_{P}}{V_{R}} \equiv F((P-1);(N-1)(P-1))$
- Influence du facteur ligne :
$H_{0}$ : pas d'influence du facteur ligne (Pas de tendance)
$H_{1}$ : Influence du facteur ligne (Tendance)
RDD :
$F_{c} > F_{1-k}$ on rejette $H_{0}$
Loi : 
$F_{c}=\frac{V_{A}}{V_{R}} \equiv F((N-1);(N-1)(P-1))$

#### **Test de Buys-Ballot**
$H_{0}$ : B=0, schéma additif
$H_{1}$ : B!=0, schéma multiplicatif
RDD :
$T_{c} > T_{1-\frac{p}{2}}$ on rejette $H_{0}$
Loi : 
$t_{c}=\frac{\hat{\beta}}{s_{\beta}} \equiv T(n-2)$
Pour calculer $\hat{\beta}=\frac{\operatorname{Cov}(s_{i.},x_{i.})}{\mathbb{V}(x_{i.})} \equiv \frac{\sum s_{i}x_{i}-\bar{s_{i}}x_{..}}{\sum x_{i.}^2-x_{..}^2}$
Pour calculer $\hat{\alpha}=\bar{s}-\hat{\beta}x_{..}$, du coup on se retrouve avec désormais : $\hat{s_{i}}=\hat{\alpha}+\hat{\beta}x_{i}$
Pour calculer $\hat{s_{\beta}}=\sqrt{ \frac{1}{\sum(x_{i.}-x_{..})^2}}\hat{s_{\epsilon}}$, cependant on cherche $\hat{s_{\epsilon}}=\frac{\sum(e_{t}^2)}{n-2} \equiv \frac{\sum(\hat{s_{i}}-\hat{\bar{s_{i}}})}{n-2}$


# Suite tablette
