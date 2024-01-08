## Template 
\documentclass[12pt,a4paper]{article}
\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}
\usepackage[french]{babel}
\usepackage{times}
\usepackage{amsmath, amssymb}
\usepackage{geometry}
\usepackage{graphicx}
\usepackage{biblatex} 
\usepackage{titlesec}
\usepackage{fancyhdr}
\usepackage{hyperref}
\usepackage{siunitx}
\usepackage{booktabs}
\usepackage{dcolumn}
\usepackage{float}
\usepackage{floatrow}

\addbibresource{references.bib}
\geometry{margin=2cm}
\sisetup{
  round-mode=places, % Arrondit les nombres
  round-precision=2, % Arrondit à 2 chiffres après la virgule
  table-align-text-post=false, % Assure que l'alignement tient compte des textes après les nombres
}
\setcounter{secnumdepth}{4}
% Ajouter le niveau de subsubsubsection, non numéroté
\titleclass{\subsubsubsection}{straight}[\subsection]
\newcounter{subsubsubsection}
\renewcommand\thesubsubsubsection{\thesubsubsection.\arabic{subsubsubsection}}
\titleformat{\subsubsubsection}
{\normalfont\normalsize\bfseries}{\thesubsubsubsection}{1em}{}
\titlespacing*{\subsubsubsection}
{0pt}{1.ex plus 1ex minus .2ex}{0,5ex plus .2ex}

% Vérifier que ces niveaux apparaissent dans la table des matières
\setcounter{tocdepth}{4}
\setcounter{secnumdepth}{4}

% Ajouter la prise en charge pour la table des matières
\makeatletter
\let\toclevel@subsubsubsection\toclevel@subsection
\let\l@subsubsubsection\l@subsection
\makeatother


\linespread{1.10}

% Personnalisation des titres de sections
\titleformat{\section}{\fontsize{15}{16}\selectfont\bfseries}{\thesection}{1em}{}
\titleformat{\subsection}{\fontsize{12}{14}\selectfont\bfseries}{\thesubsection}{1em}{}
\titlespacing*{\subsection}{0pt}{1.75ex plus 1ex minus .2ex}{0,75ex plus .2ex}
\titleformat{\subsubsection}{\fontsize{12}{13}\selectfont\bfseries}{\thesubsubsection}{1em}{}
\titlespacing*{\subsubsection}{0pt}{1.5ex plus 1ex minus .2ex}{0,5ex plus .2ex}

% Configuration de l'en-tête
\fancyhf{} % Vide l'en-tête et le pied de page
\fancyhead[L]{\nouppercase{\leftmark}} % Nom de la section à gauche
\fancyhead[R]{Les émissions de CO2} % Texte personnalisé à droite
\renewcommand{\headrulewidth}{0,4pt} % Ligne sous l'en-tête
\fancyfoot[C]{\thepage} % Numéro de page au centre du pied de page

% Applique le style fancy aux pages qui ne sont pas la première
\pagestyle{fancy} 

\title{Impact des facteurs socio-économiques sur l'émission de CO2}
\author{Auteur 1 \and Auteur 2}
\date{\today}

\begin{document}

\begin{titlepage}
\centering
\vspace*{\fill}
{\LARGE \bfseries Impact des facteurs socio-économiques sur l'émission de CO2}\\[10mm]
{\large ABUBAKER Mohamed}\\
M1 ARB\\[5mm]
{\large FRAYSSE Christopher}\\
M1 ARB \\
\vspace*{\fill}
\thispagestyle{empty} % S'assure que la page de titre n'a pas de numéro de page
\end{titlepage}

% Commencer la numérotation des pages à partir de la deuxième page
\setcounter{page}{1} % Réinitialiser le compteur de pages

% Résumé et le reste du document viennent ici
\begin{abstract}

## Template tableau
\begin{table}[H]
\centering
Variable dépendante: l\_CO2GlobalC\\
\begin{tabular}{lr@{,}lr@{,}lr@{,}lr@{,}l} %A changer selon besoin
\hline
  &
 \multicolumn{2}{c}{A} &%A changer selon besoin
  \multicolumn{2}{c}{B} &%A changer selon besoin
   \multicolumn{2}{c}{C} &%A changer selon besoin
    \multicolumn{2}{c}{D} \\%A changer selon besoin
     \hline
**CONTENU**
        \hline
\end{tabular}
\vspace{1ex}
\begin{tabular}{lrlr} %A changer selon besoin
**CONTENU**
\hline
\end{tabular}
\caption{Modèle 1}