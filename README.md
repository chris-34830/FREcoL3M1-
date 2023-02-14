# FacS6
Nécessite l'utilisation de obsidian.md (ou tout autre logiciel supportant le LaTeX & le Markdown) https://obsidian.md/, sinon allez copier le cours dont vous avez besoin et coller le sur google doc ou Word tout en activant le support Markodwn (référer internet), ne fonctionne pas pour les cours d'analyse de donnée & du S5 ces éditeurs de texte supportent mal le LaTeX.

## Si problème de lecture / faute dans le cours
M'envoyer un message whatsapp

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
\end{document}  
 
## Utilisation avec Obsidian.md  
Créer une vault   
Télécharger le git   
Mettre la git à la place de votre vault  
Relancer Obsidian  
Accepter les plug-ins  
Normalement vous devez voir ceci :   
![image](https://user-images.githubusercontent.com/115942285/218880631-6af1a44e-3e93-4492-8984-b8280f8873f9.png)



## Mise à jour automatique
Se référer à la documentation lié au plugin déjà installé dans le .git "Obsidian Git".
(Si problème malgré avoir suivi la documentation, changer la clef HTTPS en SSH)

