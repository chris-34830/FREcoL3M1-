[[Econométrie]][[Modèle des moindres carrés ordinaires]]
[[Beta]][[Variable endogène]][[Variance Beta]][[Variance du résidu]]
Hypothèses : 
$H_0 : \beta=0$
$H_1 : \beta \neq 0$
Règle de décision : 
Si $\frac{\hat{\beta}}{\hat{\sigma_{\hat{\beta}}}} < T^{(n-2)}, H_0$ est acceptée au risque de première espece p = 5%, la variable est non-significative.
Si $\frac{\hat{\beta}}{\hat{\sigma_{\hat{\beta}}}} \geqslant T^{(n-2)}, H_0$ est rejetée au risque de première espece p = 5%, la variable est significative. (Si rejeté, modèle valide)
Calcul :
$1-p = Prob\[t_{p/2}<T^{(n-2)}<t_{1-p/2}]$ 
$= Prob\[t_{p/2}<\frac{\hat{\beta}}{\hat{\sigma}_{\hat{\epsilon}}/\sqrt{\Sigma x_t^2}}<t_{1-p/2}]$ 
$= Prob\[\frac{\hat{\beta}}{\hat{\sigma}_{\hat{\beta}}}<t_{1-p/2}]$ 








