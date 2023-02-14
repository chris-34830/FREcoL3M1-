# FacS6
Nécessite l'utilisation de obsidian.md (ou tout autre logiciel supportant le LaTeX & le Markdown) https://obsidian.md/, sinon allez copier le cours dont vous avez besoin et coller le sur google doc ou Word tout en activant le support Markodwn (référer internet), ne fonctionne pas pour les cours d'analyse de donnée & du S5 ces éditeurs de texte supportent mal le LaTeX.

## Support overleaf / LaTeX   
Exemple initialisation document LaTeX :  
\documentclass{article}  
\usepackage{lmodern} %Permet d'avoir une police vectorielle qui, autrement, n'est pas conservé lors du chargement de fontenc.  
\usepackage[francais]{babel} 
\usepackage[utf8]{inputenc} %inputenc car utilisation d'accent et l'encodage se fait automatiquement    
\usepackage[T1]{fontenc} %Permet de régler le problème de césure lié à l'utilisation d'accent et du package inputenc  
\usepackage{amsmath,amsfonts,amssymb} %maths  
\usepackage{ragged2e} %Sur overleaf, le texte est répartie uniformément entre les marges en tout temps ce qui empêche d'aligner avec la marge de gauche.   
\usepackage{diffcoeff}  %equation différentielle  
\usepackage{xcolor} %permet de passer outre les couleurs utilisés dans le plaintext  
\usepackage[hybrid]{markdown} %permet l'utilisation conjointe du Markdown et du LaTeX  
  
\begin{document}  
\begin{markdown}  
^Cours copié collé
\end{markdown}  
\end{document  
 
## Utilisation avec Obsidian.md  
Créer une vault   
Télécharger le git   
Mettre la gib à la place de votre vault  
Relancer Obsidian  
Accepter les plug-ins  
Normalement vous devez voir ceci :   

![image](https://user-images.githubusercontent.com/115942285/218623173-2ded9c5a-4d94-46a9-b9bf-8f0309c26977.png)


