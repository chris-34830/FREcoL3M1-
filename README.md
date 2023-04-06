# FacS6
Pré-requis :
Pour les cours de [6.1 Analyse Financière] un support : 
- MultiMarkdown
- LaTeX
- HTML
Pour les cours de [6.2 Analyse de Donnée] un support :
- LaTeX
- Markdown
Pour les cours de [6.3 Base de Donnée] un support :
- Markdown
Pour les cours de [6.4 Politique économique et sociale] un support : 
- Markdown
Pour les cours de [6.5 Microéconomie appliquée] un support :
- Markdown
- LaTeX
Pour les cours de [6.6 Anglais] un support :
- Markdown 

Logiciel conseillé qui permet le support (natif ou par traduction) :
- Vim (Le mieux mais absence d'interface graphique)
- Obsidian (Le plus simple, le repo github étant ma vault obsidian)
- Notion 

## Initialisation d'un support Markdown sur un document LaTeX
Exemple expliqué d'initialisation d'un document LaTeX pour le support complet du Markdown :  
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

