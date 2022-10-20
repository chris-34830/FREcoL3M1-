[[Test hypothèse résidu]][[Tester signification constante (IA)]][[Tester signification de la pente (pas IA)]][[Econométrie]][[Modèle des moindres carrés ordinaires]]

Hypothèses : 
$H_0 : \hat{\sigma^2_\epsilon} =K$
$H_1 : \hat{\sigma^2_\epsilon}  \neq K$
Règle de décision : 
Si $\hat{\sigma^2_\epsilon} \in IA, H_0$ est acceptée au risque de première espece p = 5%, le résultat est non-significatif. (Hypothèse du modèle)
Si  $\hat{\sigma^2_\epsilon}  \notin IA, H_0$ est rejetée au risque de première espece p = 5%, le résultat est non-significatif. 
Loi :
$(n-2)\frac{\hat{\sigma}^2_\epsilon}{\sigma^2_\epsilon} \equiv \chi^2 (n-2)$
Calcul :
$1-p = Prob\[\chi^2_{p/2}<(n-2)\frac{\hat{\sigma}^2_\epsilon}{\sigma^2_\epsilon}<t_{1-p/2}]$ 
$= Prob\[\hat{\alpha}\in [\chi^2_{p/2} \frac{\sigma^2_\epsilon}{n-2} ; \chi^2_{1-p/2} \frac{\sigma^2_\epsilon}{n-2}]$  
