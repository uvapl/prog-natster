# Numeriek integreren [Monte Carlo methode]

Benader de integraal door gebruik te maken van random getallen. Gooi in een gebied (van bekende grootte) rond de integratie regio random punten en kijk welke fractie binnen het integratiegebied valt.

### a) Het probleem: 
Gegeven $$f(x)$$ op $$a \leq x \leq b$$, bereken $$\int_a^b f(x)~dx$$

### b) De oplossingsstrategie

Stap 1) Definieer een gebied (vaak een rechthoek) dat het de integraalregio omsluit. Definieer dus een $$x_{min}$$, $$x_{max}$$, $$y_{min}$$ en $$y_{max}$$ zodanig dat geldt: $$x_{min} \leq a$$ en $$x_{max} \geq b$$ en dat ook geldt:
$$
   \mbox{ voor } a \leq x \leq b \mbox{ : } y_{min} \leq f(x)  \leq y_{max}
$$

Note: in de meeste toepassingen wordt gekozen voor $x_{min} = a$ en $x_{max} = b$.

Stap 2) Gooi een groot aantal random punten $$(x_i, y_i)$$ in het rechthoek dat het integratiegebied om sluit en bekijk voor elk punt of het binnen het integratiegebied valt ('goed') of erbuiten ('fout'). Hou bij welke fratie van de punten in het integratiegebied vald: $$f_{goed}_$$.

De integraal is vervlogens te schrijven als:

$$\int_a^b f(x)~dx = f_{goed}$$ x oppervlakte rechthoek

### d) Implementatie in Python 

Gooi een groot aantal random punten $$(x_i, y_i)$$ in het rechthoek

$$
   x_i: \mbox{ random getal tussen } x_{min} \mbox{ en } x_{max}
   y_i: \mbox{ random getal tussen } y_{min} \mbox{ en } y_{max}$$

Bepaald voor elk punt of het 'goed' (binnen het integratiegebied) of 'fout' is (buiten het integratiegebied):

$$
   \mbox{'goed':  } y_i < f(x_i) \mbox{  of   'fout':  } y_i > f(x_i)
$$

Let op: bij negatieve $$f(x)$$ draait definitie om. Visualiseer altijd je functie.










{\bf Implementatie: Gooi random punten in de box:}\\

~~\\
{\bf Bepaal de integraal:}\\
De integraal is de fractie punten die binnen de grafiek vallen keer de oppervlakte van de totale box. 
In ons geval (rechthoek als box) geldt dan:
\[
    \int_a^b f(x)~dx = \frac{N_{\rm goed}} {N_{\rm goed} + N_{\rm fout} }  (x_{max}-x_{min})(y_{max}-y_{min})
\]

{\bf Extra:}\\
In 'echte' toepassingen wordt voor effici\"{e}ntie maximalisatie de box zo gekozen dat hij de 
integraal zo nauw mogelijk omsluit: grootste fractie 'goede' worpen.\\

{\bf computing hints:}
\begin{itemize}
\item Een random getal tussen 0 en 1 krijg je door: {\tt  xi = random()}
\end{itemize}


