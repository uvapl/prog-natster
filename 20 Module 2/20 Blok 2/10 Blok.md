# Numeriek integreren [Riemann sommatie]

Een van de manieren om een integraal te evalueren is door het te schrijven als de som van kleine rechthoekjes, de Riemannsom.

### het probleem:
Gegeven $$f(x)$$ op $$a \leq x \leq b$$, bereken $$\int_a^b f(x)~dx$$

### de oplossingsstrategie
Schrijf de integraal als een Riemannsom

Verdeel het interval $$(a,b)$$ in $$N$$ intervallen van gelijke lengte $$\Delta x$$. Je hebt dan dus $$N+1$$ x-waardes $$x_i_$$ die elk $$Delta
 x = \frac{b-a}{N}$$ uit elkaar liggen. 

Je kan de totale integraal dan schrijven als de som van de intregraal op elk van de subsecties:

$$ \int_a^b f(x)~dx = \sum_{i=0}^{N-1} \int_{x_i}^{x_{i+1}} f(x)~dx$$

### specifieke implementatie

In elk van de subsecties gaan we de deelintegraal benaderen door het voor te stellen als een rechthoek. De breedte van de rechthoek is natuurlijk 
$$\Delta x$$ (x_{i+1}- x_{i}). De hoogte van de rechthoek zou de gemiddelde hoogte moeten zijn op het interval. De simpelste schatting is om gewoon het gemiddelde te nemen van de functie $$f(x)$$ op de linkerkant van het interval ($$f_{i}$$) en de waarde van de  de functie $$f(x)$$ op de rechterkant van het interval ($$f_{i+1}$$). In deze lineaire benadering op het interval $(x_i,x_{i+1})$ is $f(x)$ dan te schrijven als:

$$f(x) = \frac{f_{i+1}+f_i}{2}~+~\mathcal{O}(\Delta x)$$

De sommatie voor de integraal is dan te schrijven als:

$$
   \int_a^b f(x)~dx &\approx& \frac{\Delta x}{2} (f_0 + 2 f_1 + 2 f_2 + ... +  2 f_{N-1} + f_N)~+~\mathcal{O}((\Delta x)^2)\\
                       ~~ &\approx& \Delta x(f_1 + f_2 + ... +  f_{N-1}) +\frac{\Delta x}{2}(f_0+f_N)                         
$$

### Extra: hogere orde (meer precieze) benaderingen}
Het is mogelijk de evaluatie van de integraal te verbeteren door niet te uit te gaan van de (te simpele) lineaire benadering. De *Simpsonregel* bijvoorbeeld is een parabolische benadering (let op, N=even) waarbij $$f(x)$$ op het interval $$(x_{i-1},x_{i+1})$$ wordt benaderd door een parabool door de 3 punten $$(f_{i-1},f_{i},f_{i+1})$$. Zoek op of werk zelf uit als je deze wilt gebruiken.

