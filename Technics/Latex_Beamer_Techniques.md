# Latex Beamer Techniques
---

## Basic frame
```tex
\begin{frame}[t]{Functions}\vspace{4pt}

\begin{block}{Definition of a Function}
\vspace{0.5em}
A \textbf{function} $f$ is a rule that assigns to each element $x$ in a set $D$ exactly one element, called $f(x)$, in a set $E$.
\vspace{0.5em}
\end{block}

\vspace{10pt}
Set $D$ is called the 
\only<1>{\line(1,0){50}}
\only<2>{\textcolor{magenta}{domain}}
\,of the function.\\[10pt]
Set $E$ is called the 
\only<1>{\line(1,0){50}}
\only<2>{\textcolor{magenta}{range}}
\,of the function.

\end{frame}
```

## Show by click
```tex
\begin{frame}[t]{Your Very First Card}\vspace{10pt}
$\sqrt{x^2}=$\\[10pt]
\begin{enumerate}[(A)]
\item $x$
\item $-x$
\item $|x|$
\item undefined
\end{enumerate}
\end{frame}

\begin{frame}{Your Very First Card}\vspace{10pt}
\begin{columns}[onlytextwidth]
\column{0.4\textwidth}
$\sqrt{x^2}=$\\[10pt]
\begin{enumerate}[(A)]
\item $x$
\item $-x$
\item $|x|$
\item undefined
\end{enumerate}
\column{0.6\textwidth}
\only<3>{
    $\sqrt{x^2}=\begin{cases}
    -x,&x<0\\
    x,&x \geq 0
    \end{cases}$\\[10pt]
}
\only<2->{
\includegraphics[scale=0.45]{1}
}
\end{columns}
\end{frame}
```

## Slide to show
```tex
\begin{frame}[t]{Parent Functions}\vspace{4pt}
You should be able to identify by name and sketch a graph of each of the following parent functions
\begin{enumerate}
\begin{multicols}{3}
\item $y=x$
\item $y=|x|$
\onslide<2->
{\item $y=x^2$}
\end{multicols}
\end{enumerate}
\end{frame}
```

## Final page
```tex
\begin{frame}[standout]
\flushleft
Homework:p.342\#7-21
\end{frame}
```
