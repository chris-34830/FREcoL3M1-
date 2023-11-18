## Résumé d'étude (A faire à la fin)
-> Le but de notre étude est d'explorer la relation entre émission et facteurs socio-économiques => Re-écrire le sujet (cf expliquer le titre)
-> Ce qui a été fait dans l'étude

## Introduction
##### Initialisation
-> Amorce (Accroche du choix du sujet) 
-> On reformule le titre en posant des questions 
-> Explication du problème de date (post 2020)
-> On dit sur quoi on a décidé de se concentrer comme variable -> L'arbitrage variable => Pourquoi certaines variables et pas d'autre (Ex : **Expliquer que le problème d'émission de CO2 est pluridisciplinaire et l'impossibilité de se contenter à une étude uniquement économique sur le sujet**)
-> On explique les résultats qu'on aurait attendu (On imaginait densité élevé = Emission CO2 élevé)

#### Définition des données (Expliquer les variables, leur échelle etc)  (3-4lignes max par variables)
###### Variable expliquée 
-> Listing des variables, leur nom, échelle
-> Les définir
-> La raison du choix
-> Essayer de les sourcer avec des études pour justifier nos choix
###### Variable explicative (Hors GNI)
-> Listing des variables, leur nom, échelle
-> Les définir
-> La raison du choix
-> Essayer de les sourcer avec des études pour justifier nos choix
###### Choix des observations
-> Création de la base de donnée, les sources des différentes bases
-> Justification date 2019
-> Arbitrage donnée ; comment ? Pourquoi certains pays n'y sont pas... (ex : Taiwan, Israël) **Israël => Problème !**
###### Statistique descriptive des variables explicatives
-> Min
-> Max
-> Ecart type
-> Moyenne
###### Variable indicatrices
-> GNI 
######  Matrice variance-cov

## Modèle test 1  (Ajouter GNI en variable explicative)
-  Nuages de points
### Présentation
![[Pasted image 20231116191757.png]]
#### Test explication
- Test linéarité (Non linéaire, transformation non-linéaire augmente la fiabilité du modèle) B EXPLICATION DU TEST RESET
- Significativité ( 4 valeurs non significatives (income etc) B 
- Colinéarité (Non colinéarité, VIF>10 pour HDI & Income) G
- Homoscédasticité (hétéroscédasticité) B
- Normalité (Pas nécessaire pour BLUE) B
#### Conclusion
- Le modèle n'est pas satisfaisant. Parmi les 4 hypothèses nécessaires à la création d'un BLUE, seulement une est validé. 
- Il aurait été possible de s'arrêter dès lors que nous avions vu que notre modèle ne présentait pas de linéarité pour le changer. 
- Cependant, en continuant de tester les autres hypothèses, il a été possible de déterminer la cause du problème. 
> En faisant la même transformation que le PIB a subit, alors le modèle prend son sens : Le modèle n'a du sens que lorsqu'il est rapporté à l'échelle d'un membre de la population d'un pays.
## Modèle test 2 
- Nuages de points
- Le modèle test 2 va avoir la variable Yt transformé en Yt/capita, CO2_emission => CO2_emission_capita
- L'income sera changé en PIB pour limiter les problèmes liés à l'utilisation du GNI comme variable indicatrice
## Modèle correctif 2.1
### Présentation
- Même modèle que le second modèle, composé des mêmes variables
- Correction des erreurs du modèle test 2 (cf, significativité, colinéarité)
- Ajout des variables indicatrices

![[Pasted image 20231118230435.png]]
![[Pasted image 20231118234054.png]]
#### Test
- Test linéarité (Test complètement linéaire) G
- Significativité ( Tous les paramètres sont significatifs) G
- Colinéarité (Absence de colinéarité) G
- Homoscédasticité (Homoscédasticité) G
- Normalité des résidus ( Validé, même si pas nécessaire pour BLUE) G
#### Conclusion
- 
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
- 