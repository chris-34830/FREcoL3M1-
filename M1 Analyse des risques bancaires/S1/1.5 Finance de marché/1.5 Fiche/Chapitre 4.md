- Le PRM est le portefeuille qui "domine" tout les portefeuilles sous-optimaux mais si on souhaite gagner plus que $\bar{R}_{PRM}$ il faut forcément supporter plus de risque
- Il existe une frontière efficiente qui détermine les allocations optimales en actifs qui respectent le critère rentabilité-risque
- Il est possible de généraliser à N actifs le raisonnement de Markowitz. Les formules seront plus complexes mais la logique sous-jacente à la diversification et la frontière efficiente restent identique.
  On peut donc déduire la rentabilité moyenne et le risque d'un portefeuille composé à N actifs risqués comme suit : 
  $\bar{R}_{pf} =w_{A}R_{A}+w_{B}R_{B}+\dots+w_{N}R_{N}$
  Et son niveau de risque comme suit : $\sqrt{\sigma^2_{P} }= \sqrt{w_{A}^2\sigma_{A}^2+w_{B}^2\sigma_{B}^2+ }$

Quelle est l'allocation optimale risqués qui forme PO?
	Cas le plus simple avec 2 actifs risqués A et B dont on connait par calcul $R_{A}$ et $R_{B}$ ainsi qu'une portefeuille $\sigma_{A}$et $\sigma_{B}$ (depuis un historique de prix passés).
		Ce portefeuille propose alors le meilleur couple Rentabilité-Risque si l'on souhaite investir dans les actifs risqués uniquement à savoir $R_{PO}-\sigma_{PO}$ (trouver à partir des formules de la diapo 8)
	Le théorème de séparation des fonds nous dit que tous les portefeuilles composes de $w$ investit dans le portefeuille optimal risque et de $1-w$ dans l'actif sans risques $rf$  sont efficient.
	Il existe deux façons de trouver le portefeuille efficient qui correspond à votre tolérance au risque.
		- En se fixant une rentabilité espérée / exégéré
		- En fixant un niveau de risque
	Le portefeuille efficient de rentabilité $R_{PE}$ et de risque $\sigma_{PE}$ se définit comme suit:
	En se fixant un seuil de risque souhaité $\bar{\sigma}_{PE}$ on peut aisément trouver $w=\frac{\bar{\sigma}_{PE}}{\sigma_{PO}}$
	En se fixant une rentabilité exigée/espérée $\bar{R}_{PE}$ on pose alors : $\bar{R}_{PE}=w(R_{PO}-rf)+rf \rightarrow$  




Cas pratique
	Soit les 3 actifs suivants :

| Annuel      | A    | B    | rf   |
| ----------- | ---- | ---- | ---- |
| Rendement   | 0.14 | 0.08 | 0.06 |
| Risque      | 0.20 | .15  | .00  |
| Correlation |      |      |      |
1 - Calculer le rendement et le risque d'un portefeuille 50-50 : 
	Rendement : 11%
	Risque : 12.5 (diapo 8)
2 - Quelle allocation permet d'atteindre le PRM ?
	36%
	64%
3 - Calculer le rendement du PRM et le risque du PRM et comparez avec le portefeuille 5050
	Rendement : 10,16%
	Risque : 12%
 