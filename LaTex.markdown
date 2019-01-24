# LaTeX


### LaTex font sizes
\tiny
\scriptsize
\footnotesize
\small
\normalsize
\large
\Large
\LARGE
\huge
\Huge

### Beamer presentation special effect:
\transblindshorizontal    % Horizontal blinds pulled away
\transblindsvertical % Vertical blinds pulled away
\transboxin % Move to center from all sides
\transboxout % Move to all sides from center
\transdissolve % Slowly dissolve what was shown before
\transglitter % Glitter sweeps in specified direction
\transslipverticalin % Sweeps two vertical lines in
\transslipverticalout % Sweeps two vertical lines out
\transhorizontalin % Sweeps two horizontal lines in
\transhorizontalout % Sweeps two horizontal lines out
\transwipe % Sweeps single line in specified direction
\transduration{2}    % Show slide specified number of seconds

### Indicator variable style equations

\[
x_i = \left\{
\begin{array}{l l}
1 & \quad \text{if the ith person is female}\\
0 & \quad \text{if the ith person is male}\\
\end{array} \right.
\]

### Figure example

\begin{figure}[!h]
\begin{center}
\includegraphics[width=15.0cm]{figures/fig1.png}
\end{center}
\caption
 [Short caption.]    
{Long caption.}
\label{fig:fig1}
\end{figure}

or 

\begin{figure}
\centering
\includegraphics[height=0.32\textheight]{RecursionTree}
\caption{A caption.}
\label{fig:recursiontree}
\end{figure}

### use numbers instead of letters in the appendix

\appendix
\renewcommand{\thesection}{\arabic{section}}

### footnotes

\footnote{text, blah, blah}

### urls

\usepackage{hyperref}

Then:

\url{www.example.com}

### enumerations

Use `\setcounter{enumi}{<value>}` before an `item` to change the value of an
enumeration counter.

To get different markers,

```
\usepackage{enumitem}

%Roman numbers
\begin{enumerate}[label=\roman*)]
%...

% Arabic numbers
\begin{enumerate}[label=\arabic*)]
%...

% Alphabetical
\begin{enumerate}[label=\alph*)]
%...
```

Also,

```
\begin{itemize}
\item[--] Dash
\item[$-$] Dash
\item[$\ast$] Asterisk
\end{itemize}
```

### matrices

We can use `bmatrix`, `pmatrix`, etc.

\begin{pmatrix}
\Sigma_x & \Sigma_{xy} \\
Sigma_{xy}^T & \Sigma_y
\end{pmatrix}

### nice limits

\lim\limits_{x \to y}
