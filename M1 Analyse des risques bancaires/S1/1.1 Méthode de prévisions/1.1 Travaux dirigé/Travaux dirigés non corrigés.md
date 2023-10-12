
## Prévision d'une série chronologique avec les méthodes de prévision traditionnelles

#### Exercice 1
Série : 22,13,10,29,22,14,12,31,23,15,13,33,25,16,15,34
Par trimestre
##### Donner la représentation graphique de la chronique. Analyser.
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

##### Constituer les tableaux de Buys-Ballot et Buys-Ballot classé.

- Tableau de buys-Ballot : 

| Date                | T1    | T2    | T3    | T4    | $x_{i.}$ | $\hat{\sigma}_{i.}$ |
| ------------------- | ----- | ----- | ----- | ----- | -------- | ------------------- |
| Année 1      | 22    | 13    | 10    | 29    | 18,5     | 8,66          |
| Année 2      | 22    | 14    | 12    | 31    | 19,75    | 8,653         |
| Année 3      | 23    | 15    | 13    | 33    | 21       | 9,092         |
| Année 4      | 25    | 15    | 16    | 34    | 22,5     | 8,888         |
| $x_{.j}$            | 23    | 14,5  | 12,75 | 31,75 | $x_{..}$ | $\hat{\sigma}_{..}$ |
| $\hat{\sigma}_{.j}$ | 1,414 | 1,291 | 2n082 | 2,217 | 20,4375  | 8,0412              |
Attention, l'écart-type est à exprimer sans biais autrement, le test de buys-ballot ne sera pas juste.
Ainsi, $\hat{\sigma}=\frac{n}{n-1}\sigma^{2}$

- Tableau de Buys-Ballot classé : 

|      |     |     |     |     |
| ---- | --- | --- | --- | --- |
| 2018 | T4  | T1  | T2  | T3  |
| 2019 | T4  | T1  | T2  | T3  |
| 2020 | T4  | T1  | T2  | T3  |
| 2021 | T4  | T1  | T2  | T3  |

##### Effectuer l'analyse de la variance.
Rappel des formules :
$S_{p}=N\times \sum(x_{.i}-x_{..})^2$
$S_{A}=P\times \sum(x_{i.}-x_{..})^2$
$S_{R}=\sum_{i} \sum_{j}(x_{ij}-x_{i.}-x_{.j}+x_{..})^2$
$S_{T}=\sum_{i} \sum_{j}(x_{ij}-x_{..})$
