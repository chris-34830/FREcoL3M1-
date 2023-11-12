Sachant que $\hat{\beta}$ est un estimateur sans biais de $\beta$,  on cherche à démontrer la variance totale : Var$(\hat{\beta}) = \mathbb{E}[\text{Var}(\hat{\beta}|X)] + \text{Var}(\mathbb{E}[\hat{\beta}|X]$
Définition de la variance :
$\text{Var}(\hat{\beta}) = \mathbb{E}[(\hat{\beta} - \mathbb{E}[\hat{\beta}])^2]$


2. Expand the squared term:
$text{Var}(hat{beta}) = mathbb{E}[hat{beta}^2 - 2hat{beta}mathbb{E}[\hat{\beta}] + (mathbb{E}[\hat{\beta}])^2]$

3. Since \(\hat{\beta}\) is an unbiased estimator, \(\mathbb{E}[\hat{\beta}] = \beta\), thus:
$\text{Var}(\hat{\beta}) = \mathbb{E}[\hat{\beta}^2] - \beta^2$


4. Add and subtract \(\mathbb{E}[\mathbb{E}[\hat{\beta}|X]]^2\):
$\text{Var}(\hat{\beta}) = \mathbb{E}[\hat{\beta}^2] - \mathbb{E}[\mathbb{E}[\hat{\beta}|X]]^2 + \mathbb{E}[\mathbb{E}[\hat{\beta}|X]]^2 - \beta^2$


5. Recognize that \(\mathbb{E}[\mathbb{E}[\hat{\beta}|X]] = \mathbb{E}[\hat{\beta}]\) and rearrange:
$\text{Var}(\hat{\beta}) = (\mathbb{E}[\hat{\beta}^2] - \mathbb{E}[\mathbb{E}[\hat{\beta}|X]]^2) + (\mathbb{E}[\mathbb{E}[\hat{\beta}|X]]^2 - \beta^2)$


6. The first term is the expected value of the conditional variance:
$\mathbb{E}[\text{Var}(\hat{\beta}|X)] = \mathbb{E}[\mathbb{E}[\hat{\beta}^2|X] - (\mathbb{E}[\hat{\beta}|X])^2]$

7. The second term is the variance of the conditional mean:
$\text{Var}(\mathbb{E}[\hat{\beta}|X]) = \mathbb{E}[\mathbb{E}[\hat{\beta}|X]]^2 - (\mathbb{E}[\hat{\beta}])^2$
8. Thus, combining these two gives us the law of total variance:
$\text{Var}(\hat{\beta}) = \mathbb{E}[\text{Var}(\hat{\beta}|X)] + \text{Var}(\mathbb{E}[\hat{\beta}|X])


\end{document}
