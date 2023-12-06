## Résumé d'étude (A faire à la fin)
-> Le but de notre étude est d'explorer la relation entre émission et facteurs socio-économiques => Re-écrire le sujet (cf expliquer le titre)
-> Ce qui a été fait dans l'étude

## Introduction
# Fini, ne pas oublier de rename les variables sur le document LaTeX et insérer les footnotes

###### Variable indicatrices
-> Région géographique 
	genr SAS = (Region =="South Asia")
	genr ECS = (Region =="Europe & Central Asia")
	genr MEA = (Region =="Middle East & North Africa")
	genr AFE = (Region =="Africa Eastern and Southern")	
	genr LCN = (Region =="Latin America & Caribbean")
	genr AFW = (Region =="Africa Western and Central")
	genr AFE = (Region =="Africa Eastern and Southern")
	genr NAC= (Region =="North America")
## Modèle test 1  (Ajouter GNI en variable explicative)
-  Nuages de points
$Y_t =\beta_{0}+\beta_{1}x_{1}\dots$
### Présentation

#### Test explication
- Test linéarité (Non linéaire, transformation non-linéaire augmente la fiabilité du modèle) B
- Significativité ( 4 valeurs non significatives (income etc) B 
- Colinéarité (Non colinéarité, VIF>10 pour HDI & Income) G
- Homoscédasticité (hétéroscédasticité) B
- Normalité (Pas nécessaire pour BLUE) B-G
#### Conclusion
- Le modèle n'est pas satisfaisant. Parmi les 4 hypothèses nécessaires à la création d'un BLUE, seulement une est validé. 
- Il aurait été possible de s'arrêter dès lors que nous avions vu que notre modèle ne présentait pas de linéarité pour le changer. 
- Cependant, en continuant de tester les autres hypothèses, il a été possible de déterminer la cause du problème. 
- La forme "$\ln(\text{CO2globalC}) =const+\beta_{1}\text{}dots$" ne s'adapte à notre modèle 1 car l'hypothèse de linéarité n'est pas respectée. Ainsi, il est nécessaire de trouver un modèle alternative.
## Modèle test 2 
- Nuages de points
- Le modèle test 2 va avoir la variable Yt transformé en Yt/capita, CO2_emission => CO2_emission_capita
- L'income sera changé en PIB pour limiter les problèmes liés à l'utilisation du GNI comme variable indicatrice
- Ajout des variables indicatrices
## Modèle correctif 2.1
### Présentation
- Même modèle que le second modèle, composé des mêmes variables
- Correction des erreurs du modèle test 2 (cf, significativité, colinéarité)

![[Pasted image 20231118230435.png]]
![[Pasted image 20231118234054.png]]
#### Test
- Test linéarité (Test complètement linéaire) G
- Significativité ( Tous les paramètres sont significatifs) G
- Colinéarité (Absence de colinéarité) G
- Homoscédasticité (Homoscédasticité) G
- Normalité des résidus (Validé, même si pas nécessaire pour BLUE) G
#### Conclusion
- Notre modèle est bien spécifié.
- 
#### Observations
- 
- 
- 
## Modèle FINAL correctif transformation non linéaire (sq, ln) 2.2
![[Pasted image 20231119000224.png]]
#### Test
- Test linéarité (Test complètement linéaire) G
- Significativité ( Tous les paramètres sont significatifs) G
- Colinéarité (Absence de colinéarité) G
- Homoscédasticité (Homoscédasticité) G
- Normalité des résidus ( Validé, même si pas nécessaire pour BLUE) G
#### Conclusion
- Une transformation non linéaire de la variable dépendante à l'aide d'un logarithme ainsi que l'ajout de transformation non linéaire sur les paramètres Energy Intensy & Density personne (respectivement, square & ln) augmente drastiquement la valeur du R².
- Nous pouvons retirer le paramètre GDP du modèle, cela n'a aucun impact sur les résultats dudit modèle.
#### Observations
- Plus un pays a une energy intensité élévé plus il va polluer
- Plus un pays à un GNI élevé (cf, est développé) plus sa population va être pollueur (variable expliquée co2 / hab)
- A l'inverse, moins il a un GNI élevé, moins il va polluer
> Le niveau de développement d'un pays a un impact sur sa génération de CO2 / habitant
- De la même manière, plus un pays a une densité population élevé, plus il va être émetteur de CO2.
### Conclusion final
- Notre modèle s'inscrit dans la théorie économique moderne : 
	- Les pays développés sont parmi les plus gros pollueur respectivement à leur population
	- Les pays non développés sont parmi les moins émetteur respectivement à leur population
	- Les pays a forte densité humaine sont quant à eux des forts pays émetteurs
### Pensée finale
- Il serait intéressant de prolonger le modèle en observant si le niveau d'urbanisme et les pays a forte densité urbaine sont synonyme d'impact positif ou négatif sur l'émission de CO2
- La relation entre les impacts sociologiques (éducations, E(Life), etc.) et émissions de CO2 n'a pas pu être mise en lumière par notre modèle. Un nouveau modèle se concentrant principalement sur ses variables pourraient montrer leur impact sur les émissions de CO2. 

$\ln(\text{CO2globalC})=const+\beta_{1}\text{Density}+\beta_{2}\ln(\text{Income})+\beta_{3}\ln(\text{Ener\_Intens})+\beta_{3}\text{Ener\_GDP}+\epsilon$
![[Pasted image 20231123181005.png]]
https://www.eia.gov/international/data/world
https://doi.org/10.5281/zenodo.7215364
https://blogs.worldbank.org/opendata/2016-edition-world-development-indicators-out-three-features-you-won-t-want-miss
https://databank.worldbank.org/source/world-development-indicators/Series/EN.POP.DNST


$\ln(\text{CO2globalC})=const+\beta_{1}\text{Density}+\beta_{2}\ln(\text{Income})+\beta_{3}\ln(\text{Income})^2+\beta_{4}\ln(\text{Ener\_Intens})+\beta_{5}\text{Ener\_GDP}+\epsilon$