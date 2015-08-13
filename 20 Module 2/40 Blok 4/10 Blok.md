# Fitten van data en foutenbepaling 

Om de onderliggende fenomenen van (natuurkundige) verschijnselen te achterhalen wordt data verzameld om afhankelijkheden te onderzoeken. Dat kan de massa van het Higgs boson zijn, de vervaltijd van uranium, maar ook het aantal kinderen in een gezin als functie van de gemiddelde lengte van de ouders. Je kan dan zoeken naar een (causaal) verband: lineair, exponentieel,etc. en daarbij ook de bijbehorende parameters bepalen met hun onzekerheid. Als je een goede beschrijving hebt gevonden kan je daarmee vervolgens ook voorspellingen doen.


Om de 'beste' waarde te vinden hebben we een maat (metriek) nodig die de *goedheid* van de fit beschrijft. We doen dat hier met de $$\chi^2$$-maat: de som van de gemiddelde afwijking van de meetpunten tot het model gewogen met hun fout. Voor elk punt bepalen we dus *hoeveel standaardafwijkingen ligt dit punt weg van mijn model/voorspelling ?*

$$\chi^2 = \sum_{i~ {\rm (datapunten)}}  \left(\frac{  y_i - f(x_i|\vec{\alpha}) }{\sigma_i}\right)^2$$

Hierbij is $$\vec{\alpha}$$ de vector met de parameters die je gebruikt in je model.

## Fit: bepalen van de beste waarde van je model ($$\alpha_{best}_$$)

In de fitprocedure zoeken we naar de waarde van de parameters in je model die de kleinste $$\Chi^2$$ opleveren. Dat zijn namelijk de 'beste' waardes van het model omdat met die waarde van de parameters je model de data het best beschrijft.

## Fit: bepalen van de onzekerheid op $$\alpha_{best}_$$ ($$\Delta_{alpha}$$)

Zodra de parameters

De fout in de positieve richting $(\Delta_c)^r$ en negatieve richting $(\Delta c)^l$ zijn die waardes van c waarbij de $\chi^2$ 1 hoger is dan $\chi_{\rm min}^2$. In de meeste gevallen geldt  $(\Delta c)^l$ = $(\Delta c)^r$ = $\Delta c$

### Voorbeeld: $$f(x) = c$$


{\bf Voorbeeld:} 1 dimensie/parameter (zie plot) $f(x|\vec{\alpha}) = c$. 

~\vspace{-2em}
\begin{figure}[!h]
\begin{minipage}{8.0cm}
\subsubsection*{a) de beste waarde van c: $c_{\rm best}$}
De waarde van $c$ waarbij de $\chi^2$  minimaal is.
\subsubsection*{b) de onzekerheid op $c_{\rm best} (\Delta_c)$ }
De fout in de positieve richting $(\Delta_c)^r$ en negatieve richting $(\Delta c)^l$ zijn die waardes van c waarbij de $\chi^2$ 1 hoger is dan $\chi_{\rm min}^2$. In de meeste gevallen geldt  $(\Delta c)^l$ = $(\Delta c)^r$ = $\Delta c$
\end{minipage}
~~
\begin{minipage}{8.5cm}
 \begin{center}
   \includegraphics[width=8.5cm]{chi2.pdf}
 \end{center}
\end{minipage}
\end{figure}

\framebox[\textwidth]{  \minibox{  
Het eindresultaat van je meting is dan: $c = c_{\rm best}~^{+(\Delta_c)^r}_{-(\Delta_c)^l}$
}}


%----------
\clearpage
%----------

%------------------------------------------------------
\begin{center}
{\Large \bf opgavenset week 4 (deel 2)}
\end{center}
%------------------------------------------------------
~~\\
{\bf opgave [2]: fitten van een model aan de data}\\
~~\\De onderstaande data-set geeft voor een specifieke voetballer het percentage goede passes ($y$) weer als functie van het aantal gespeelde wedstrijden in oranje ($x$). De onzekerheid op het aantal goede passes is weergegeven als $\sigma_y$.\\
\begin{center}
\begin{tabular}{|c||r|r|r|r|r|r|r|r|r|r|}
     \hline
     $x$            &   1  &   2  &    3  &   4  &   5  &   6   &   7   &  8   &   9   &10\\
     \hline
      $y$           & 55  & 50  &  39  & 58  & 54  & 57   & 78  & 66   & 62  & 82\\
     \hline
   $\sigma_y$ &   5  &   4  &    9  &   4  &   5  &   5   &   7   &  3   &   6  &   6\\
     \hline
\end{tabular}
\end{center}

\begin{tabbing}
a)~\=maak een plot van deze data met fouten\\ 
    \>Computing tip: gebruik de functie {\tt plt.errorbar(x,y, yerr=yerror)}\\
~~\\
b) \>bereken de beste waarde van c als $f(x)=$c en de bijbehorende onzekerheid $\Delta$c.\\
~~\\
c) \>Wat gebeurt er met $\Delta$c als de fout in elk meetpunt 2x kleiner wordt ?
\end{tabbing}

