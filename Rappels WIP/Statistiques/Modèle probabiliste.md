## Espace probabilisable

### Expérience aléatoire et événements
Une expérience est aléatoire si son résultat n'est **pas prévisible** en avance et malgré **une répétition dans des conditions identiques**, les **résultats peuvent variés**.
Le résultat de cette expérience est un élément $\omega$ de l'ensemble $\Omega$. L'ensemble $\Omega$ représente l'ensemble des résultats possible de l'expérience aléatoire, c'est l'**ensemble fondamental**
Un **évènement** est une **proposition logique relative au résultat de l'expérience**, il est réalisé - ou non - suivant que l'assertion est vraie est fausse une fois l'expérience effectuée.

*Exemple*
Soit jeu de 52cartes. Si une personne tire une carte aléatoirement et la remet dans le jeu de carte, alors :
- L'**expérience aléatoire** est le tirage d'une carte **avec remise**.
- Le **résultat** de cette expérience est l'élément $\omega$ correspondant au numéro et au symbole de la carte
- L'**ensemble fondamental** est l'ensemble des cartes qui composent mon jeu de carte initialement
- L'**événement** est une proposition établie au préalable, ainsi nous pouvons poser comme événement "La carte tiré est une carte trèfle"
- Si mon évènement est "La carte tiré est un as de trèfle" alors nous parlons d'**événement élémentaire** : Mon ensemble $\Omega$ ne comprend qu'un seul as de trèfle. Ainsi, si mon ensemble $\Omega$ est égal au singleton $(\omega)$ alors, c'est un ensemble élémentaire. *On reviendra à cet partie dans la partie qui suit

### Algèbre des événements
Soit deux événements $A,B \in \mathcal{C}$ (Propriété de $\mathcal{C}$ avec $\mathcal{C} \in \Omega$ mais $\mathcal{C} \notin \mathcal{C}$) : 
- il existe l'événement $\bar{A}$ qui représente son contraire. L'implication logique empêche la réalisation de A et $\bar{A}$ en même temps. Ainsi, $\bar{A}$ se veut être la partie complémentaire de A dans mon ensemble fondamentale $\Omega$ . 
*Rappel : Un événement est une assertion logique, sur mon ensemble fondamentale, se réalisant ou non. Lorsqu'elle se réalise alors la complémentarité n'est rien d'autre que l'ensemble d'éventualité qui n'est pas $A$ : $\bar{A} = \{ \omega \in \Omega \mid \omega \notin A \}$*
**Implication logique** : Si $A \in \mathcal{C}$ alors $\bar{A} \in \mathcal{C}$
- On détermine que l'ensemble fondamental, désormais appelé univers, $\Omega$ est l'**événement certain** qui possède pour complémentaire l'**événement vide** $\emptyset$ qui est un **événement logiquement impossible** Exemple : Jeu de 52cartes, tirer 2 As de pique
- $A \cup B$ est réalisé si $A \cup B = \{ \omega \in \Omega \mid (\omega \in A) \vee (\omega \in B)\}$ => Au moins un événement est réalisé
- $A \cap B$ est réalisé si $A \cap B = \{ \omega \in \Omega \mid (\omega \in A) \wedge (\omega \in B)\}$
Ainsi, un espace probabilisable est le couple $(\Omega;\mathcal{C})$ ou le second est un sigma-algèbre de boole.