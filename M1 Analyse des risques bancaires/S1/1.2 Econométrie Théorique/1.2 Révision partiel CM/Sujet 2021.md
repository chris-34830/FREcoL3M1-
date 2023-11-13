Sachant que $\hat{\beta}$ est un estimateur sans biais de $\beta$,  on cherche à démontrer la variance totale : Var$(\hat{\beta}) = \mathbb{E}[\text{Var}(\hat{\beta}|X)] + \text{Var}(\mathbb{E}[\hat{\beta}|X]$
Définition de la variance :
$\text{Var}(\hat{\beta}) = \mathbb{E}[(\hat{\beta} - \mathbb{E}[\hat{\beta}])^2]$
1. On développe les termes au carrés:
$\text{Var}(\hat{\beta}) = \mathbb{E}[\hat{\beta}^2 - 2\hat{\beta}\mathbb{E}[\hat{\beta}] + (\mathbb{E}[\hat{\beta}])^2]$
2. Sachant que  $\hat{\beta}$ est sans biais alors on sait que $\mathbb{E}[\hat{\beta}] = \beta$, donc:
$\text{Var}(\hat{\beta}) = \mathbb{E}[\hat{\beta}^2] - \beta^2$
3. On cherche à modifier la forme de l'expression pour isoler le terme $\text{Var}(\mathbb{E}[\hat{\beta}|X])$ alors on ajoute $\mathbb{E}[\mathbb{E}[\hat{\beta}|X]]^2$ en s'assurant de garder l'égalité (On l'additionne et le soustrait dans la même partie de l'équation):
$\text{Var}(\hat{\beta}) = \mathbb{E}[\hat{\beta}^2] - \mathbb{E}[\mathbb{E}[\hat{\beta}|X]]^2 + \mathbb{E}[\mathbb{E}[\hat{\beta}|X]]^2 - \beta^2$
4. On peut alors trouver que $\mathbb{E}[\mathbb{E}[\hat{\beta}|X]] = \mathbb{E}[\hat{\beta}]$, car $\mathbb{E}[\mathbb{E}[\hat{\beta}|X]]$ est l'espérance prise sur toutes les valeurs possibles de X. Ainsi, on ne parle plus de valeurs conditionnelles, alors on retrouve  $\mathbb{E}[\hat{\beta}]$
$\text{Var}(\hat{\beta}) = (\mathbb{E}[\hat{\beta}^2] - \mathbb{E}[\mathbb{E}[\hat{\beta}|X]]^2) + (\mathbb{E}[\mathbb{E}[\hat{\beta}|X]]^2 - \beta^2)$. 
5. Le premier terme est l'espérance de la variance conditionné à X:
$\mathbb{E}[\text{Var}(\hat{\beta}|X)] = \mathbb{E}[\mathbb{E}[\hat{\beta}^2|X] - (\mathbb{E}[\hat{\beta}|X])^2]$
>(ou $\mathbb{E}[\hat{\beta}^2] - (\mathbb{E}[\hat{\beta}|X])^2]$ car $\mathbb{E}[\text{Var}(\hat{\beta}|X)] = \mathbb{E}[\mathbb{E}[\hat{\beta}|X] - (\mathbb{E}[\hat{\beta}|X])]^2$ = $\mathbb{E}[\mathbb{E}[\hat{\beta}^2|X]] - \mathbb{E}[(\mathbb{E}[\hat{\beta}|X])^2]$ = $\mathbb{E}[\hat{\beta}^2] - (\mathbb{E}[\hat{\beta}|X])^2$ sachant que  $(\mathbb{E}[\hat{\beta}|X])^2] \neq(\mathbb{E}[\hat{\beta]})^2$ sinon ça supposerait que $\hat{\beta}$ soit une constante )
6. Le second terme est la variance de l'espérance conditionnée à X 
$\text{Var}(\mathbb{E}[\hat{\beta}|X]) = \mathbb{E}[(\mathbb{E}[\hat{\beta}|X]] - (\mathbb{E}[\hat{\beta}]))^2]$ 
>(car $\text{Var}(\mathbb{E}[{X}|Y]) =\mathbb{E}[\mathbb{E}[{X}|Y]^2]-\mathbb{E}[\mathbb{E}[{X}|Y]]^2\equiv \mathbb{E}[(\mathbb{E}[{X}|Y]- \mathbb{E}[X])^2$)
7. En combinant les deux, on se retrouve avec :
$\text{Var}(\hat{\beta}) = \mathbb{E}[\text{Var}(\hat{\beta}|X)] + \text{Var}(\mathbb{E}[\hat{\beta}|X])$
CQFD

