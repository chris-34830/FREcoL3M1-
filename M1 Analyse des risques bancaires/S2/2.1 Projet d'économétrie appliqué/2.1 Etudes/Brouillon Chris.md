### Etablissement base de donnée
#### Variable total voiture
- Source : https://www.acea.auto
- Période : 2020J-2023D
#### Variable BEV Voiture
- Source : https://www.acea.auto
- Période : 2022J-2023D
#### Variable Lerner BEV 1
- Source : https://www.acea.auto
- Période : 2022J-2023D
#### Variable Lerner BEV 2 
- Source : https://cleantechnica.com/
- Période 2020J-2021D
#### Variable voiture BEV
- Source : Croisée des deux sources
- Calcul : Quantité total vendus par le % de part de marchés de BEV
- Commentaire : Acea jugé plus fiable
#### Variable voiture thermique (non conservé)
- Source : Croisée des deux sources
- Calcul : Différence voiture total - voiture BEV
- Raison : On se concentre sur les voitures FULL ELECTRIQUES
- Commentaire : Perte de pertinence mais absence de données cohérentes sur les plug-in cars
#### Commentaire traitement de donnée
- Méthodologie de récolte changé entre 2021 & 2022
- Absence d'une donnée en Juin21 et Jui 21
- Utilisation de l'indice de Lerner & du nombre de voiture vendus pour calculer les autres variables
> Permet de conserver une cohérence, les données étant sorties de plusieurs sources, on préfère conserver le nombre de voiture vendus comme donnée fiable de référence et calculer dessus en utilisant les parts de marchés trouvés sur des sites annexes
- 48 Observations mensuelles, déterminer le nombre optimal à utiliser
- Disclaimer sur les données :
> Acea corrige ses données à l'année T+1, les données finales de 2022 se trouvent sur les graph comparaison à 2023 etc. 
> Les données 2023 ne sont pas "corrigés" donc on travaille sur les données brutes des années respectives
> Les données sur la période varie légèrement (une dizaine de véhicule de différences par mois) entre les sources.
> La quantité de voiture vendue n'a qu'une seule et unique source pour des raisons de cohérences / lissage
> Pour les données antérieur à 2022J, arbitrage fait de cette façon :
> 1- Récupération du % de part de marché des BEV & Plug-ins sur le site cleantechnica
> 2- Récupération du nombre total de véhicules vendus (toute énergie confondu)
> 3- Calcul du nombre de BEV / Plug-in en multipliant les deux statistiques
- Les données traitent des ventes européenne au sens large ; UE + EFTA + UK

