# Je supprime la vault le jeudi 13 juin

## Initialisation d'un support Markdown sur un document LaTeX
Template pour LaTeX via Overleaf - vIM sans plugins : 

\documentclass{article}  
\usepackage{lmodern} %Permet d'avoir une police vectorielle qui, autrement, n'est pas conservé lors du chargement de fontenc.  
\usepackage[francais]{babel} %Pour écrire en français
\usepackage[utf8]{inputenc} %inputenc car utilisation d'accent et encodage automatique  
\usepackage[T1]{fontenc} %Permet de régler le problème de césure lié à l'utilisation d'accent et du package inputenc  
\usepackage{amsmath,amsfonts,amssymb} %maths  %Permet l'utilisation de diverses commandes
\usepackage{ragged2e} %Si utilisation de Overleaf : le texte est répartie uniformément entre les marges en tout temps ce qui empêche d'aligner avec la marge de gauche.
\usepackage{diffcoeff}  %équation différentielle
\usepackage{xcolor} %Permet de passer outre les couleurs utilisés dans le plaintext
\usepackage[hybrid]{markdown} %permet l'utilisation conjointe du Markdown et du LaTeX  
  
\begin{document}  
\begin{markdown}  
^Cours copié collé  
\end{markdown}  
\end{document}  

