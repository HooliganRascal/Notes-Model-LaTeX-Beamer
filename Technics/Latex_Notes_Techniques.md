# Latex Notes Techniques

## Three-Line-Chart
```tex
\begin{tabular}{ccc}
\Xhline{2pt}
IV & \multicolumn{2}{c}{DV} \\
\Xcline{2-3}{0.4pt}
Radius & Length & Area \\
\Xhline{1pt}
1.00 & 6.28 & 6.28 \\
2.00 & 12.57 & 12.57 \\
3.00 & 18.85 & 28.37 \\
\Xhline{2pt}
\end{tabular}
```

## Normal Chart
```tex
\begin{center}
\textbf{Chart}\\
\vspace{0.7em}
\begin{tabular}{|c|c|c|c|c|}
\hline
&&&&
\hline\\
\end{tabular}
\end{center}
```

## Complement of the union: shade outside both circles
```tex
\begin{tikzpicture}[scale=1]
	\fill[violet!30, even odd rule] (-2.4,-1.6) rectangle (2.4,1.6)
		(-0.55,0) circle (0.9)
		(0.75,0) circle (0.9);
	\draw[thick] (-2.4,-1.6) rectangle (2.4,1.6);
	\fill[darkgray] (-0.55,0) circle (0.9);
	\fill[darkgray] (0.75,0) circle (0.9);
	\draw[thick] (-0.55,0) circle (0.9);
	\draw[thick] (0.75,0) circle (0.9);
	\node[above left] at (-2.4,1.6) {$M$};
	\node at (-0.95,0) {$A$};
	\node at (1.15,0) {$B$};
\end{tikzpicture}
```

## Hyper Link Jumping
```tex
\section{\protect\hyperlink{:}{your section}}
\addtocontents{toc}{\protect\hypertarget{:}{your section}} 
\subsection{\protect\hyperlink{:}{your subsection}}
\addtocontents{toc}{\protect\hypertarget{:}{your subsection}}

%\section{\protect\hyperlink{:}{your section}}
%\addtocontents{toc}{\protect\hypertarget{:}{your section}} 
%\subsection{\protect\hyperlink{:}{your subsection}}
%\addtocontents{toc}{\protect\hypertarget{:}{your subsection}}

\href{URL}{Text}
```

## Number of Page
```tex
\usepackage{fancyhdr}

\pagenumbering{Alph}
\pagestyle{fancy}
\fancyhead[L]{Left-Margin}
\fancyhead[R]{Right-Margin}
\fancyhead[L]{Center-Margin}
\fancyfoot[L]{Left-Footnote}
\fancyfoot[C]{\thepage}
\fancyfoot[R]{Right-Footnote}
\renewcommand{\headrulewidth}{4pt}
\renewcommand{\footrulewidth}{4pt}

\thispagestyle{empty}
\setcounter{page}{1}
\addtocounter{framenumber}{-1}
```

## Roman-Number
```tex
\usepackage{times}
\uppercase\expandafter{\romannumeral1}
\romannumeral1
```
