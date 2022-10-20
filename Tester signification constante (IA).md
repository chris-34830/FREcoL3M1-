[[Alpha]][[Variance alpha]][[Variables exogènes]][[Variance du résidu]][[Econométrie]][[Modèle des moindres carrés ordinaires]]
Hypothèses : 
$H_0 : \alpha=0$
$H_1 : \alpha \neq 0$
Règle de décision : 
Si $\hat{\alpha} \in IA, H_0$ est acceptée au risque de première espece p = 5%, la constante est non-significative.
Si  $\hat{\alpha} \notin IA, H_0$ est rejetée au risque de première espece p = 5%, la constante est significative.
Loi :
$T(n-2) \equiv \frac{(\hat{\alpha}-\alpha)\sqrt{n\Sigma x_t^2}}{\hat{\sigma}^2_{\hat{\epsilon}}/\sqrt{\Sigma x_t^2}}$ 

Calcul :
$1-p = Prob\[t_{p/2}<T^{(n-2)}<t_{1-p/2}]$ 
$= Prob\[t_{p/2}<\frac{(\hat{\alpha}-\alpha)\sqrt{n\Sigma x_t^2}}{\hat{\sigma}^2_{\hat{\epsilon}}/\sqrt{\Sigma x_t^2}}<t_{1-p/2}]$  
$= Prob\[\hat{\alpha}\in [\pm t_{p/2}\hat{\sigma_\epsilon}\frac{\sqrt{\Sigma X_t^2}}{\sqrt{n\Sigma x_t^2}}]]$   

