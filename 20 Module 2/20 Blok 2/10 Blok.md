# Numeriek integreren [Riemann sommatie]

Een van de manieren om een integraal te evalueren is door het te schrijven als de som van kleine rechthoekjes, de Riemannsom.

### a) Het probleem: 
Gegeven $$f(x)$$ op $$a \leq x \leq b$$, bereken $$\int_a^b f(x)~dx$$

### b) De oplossingsstrategie
Algemeen: verdeel het interval $$(a,b)$$ in $$N$$ intervallen van gelijke lengte $$\Delta x$$ en schrijf de integraal als de som van de deel-integralen op elk van deze intervallen:

$$ \int_a^b f(x)~dx = \sum_{i=0}^{N-1} \int_{x_i}^{x_{i+1}} f(x)~dx$$

Hierbij is $$x_i$$ het hoekpunt van een van de intervallen. Er zijn $$N+1$$ hoekpunten die lopen van $$x_0$$ tot $$x_{N+1}$$.

### c) Benadering hoogte elk rechthoek mbv de trapeziumregel en uitwerking integraal

Benader nu de deel-integralen in elk van de subsecties door het voor te stellen als een rechthoek. De breedte van de rechthoek is natuurlijk 
$$\Delta x = (x_{i+1} - x_{i})$$. Een (simpele) schatting van de hoogte van het rechthoek dat het best de integraal op dit kleine interval weergeeft is simpelweg het gemiddelde te nemen van de waarde van $$f(x)$$ op de linkerkant en de rechterkant van het interval. De integraal op het deelinterval is dan te schrijven als:

$$\int_{x_i}^{x_{i+1}} f(x)~dx = \frac{f_{i+1}+f_i}{2}~\Delta x$$

De volledige integraal is dan te schrijven als (werk dit ook zelf uit op papier):

$$\int_a^b f(x)~dx \approx \frac{\Delta x}{2} (f_0 + 2 f_1 + 2 f_2 + ... +  2 f_{N-1} + f_N)~+~\mathcal{O}((\Delta x)^2)\\
                       ~~ \approx \Delta~x(f_1 + f_2 + ... +  f_{N-1}) ~+~ \frac{\Delta x}{2}(f_0+f_N) $$

### d) Implementatie in Python 
Zoals je ziet het je 'alleen' de waarde van de functie nodig op de $$N+1$$ hoekpunten van de intervallen. Zorg dat je het aantal intervallen $$(N)$$ in je programma vrij kan veranderen en bepaal aan de hand daarvan de hoekpunten $$x_i$$ en de waarde van de grafiek op elk van die hoekpunten $$f(x_i)$$. Bereken aan het eind van het programma de integraal en print het op het scherm.


## Tips:

  - Maak altijd een plaatje van je grafiek zodat je duidelijk ziet welk gebied je aan het integreren bent.

  - test je programma altijd op een (vergelijkbare) integraal die je wel analytisch kan uitrekenen. 

  - specifiek voor Riemannnsom: Als je het interval in $$N$$ stukjes verdeeld zijn er $$N+1$$ hoekpunten.


### Extra: hogere orde (meer precieze) benaderingen}
Het is mogelijk de evaluatie van de integraal te verbeteren door niet te uit te gaan van de (te simpele) lineaire benadering. De *Simpsonregel* bijvoorbeeld is een parabolische benadering (let op, N=even) waarbij $$f(x)$$ op het interval $$(x_{i-1},x_{i+1})$$ wordt benaderd door een parabool door de 3 punten $$(f_{i-1},f_{i},f_{i+1})$$. Zoek op of werk zelf uit als je deze wilt gebruiken.


# Opgaves

## opgave 1: $$\int_{0}^{1}x^x dx$$
Hint: test je functie door te testen of je programma de integraal $$\int_{0}^{1}x^2 dx$$ goed voorspelt

## opgave 2: $$\int_{0.1}^{2} sin(x) dx$$
Hint: test je functie door te testen of je programma de integraal $$\int_{0}^{\pi]}sin(x) dx$$ goed voorspelt

## opgave 3: $$\int_{0}^{\pi} sin(x^2) dx$$
Hint: teken de functie en let op de integratiegebieden onder de y-as.










