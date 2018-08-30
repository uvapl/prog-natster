# Fractals - Mandelbrot set

Jullie kennen vast wel die prachtige en veelkleurige plaatjes waarin patronen zich tot een oneindige diepte patronen herhalen. Deze zeer complexe patronen, **fractals** genaamd, komen gek genoeg voort uit een kleine set simpele (wiskundige) regels, iets dat we ook in de natuur regelmatig zien. In deze opgave gaan we iets meer in op de wiskunde achter de fractals en gaan we proberen daarmee zelf de meest bekende fractal te reconstrueren en te tekenen: de [Mandelbrot set](https://en.wikipedia.org/wiki/Mandelbrot_set)

<p align="center">
![](mandelbrot.png){: style="width:50%"}
</p>

De opdracht van deze extra opdracht is dan ook: schrijf een programma `fractal.py` dat de Mandelbrot set op het scherm tekent.

### Stukje wiskunde: complexe getallen

Om iets te begrijpen van de wiskunde achter de fractals moeten we eerst een nieuw wiskundig concept introduceren: **complexe getallen**. Deze getallen hebben een speciale plek in wiskunde en ze komen overal in de natuurkunde terug. Jullie zullen de geheimen ervan later dan ook in verschillende colleges tegenkomen. Hier het absolute minimum.

   - definitie: we definiëren $$ i = \sqrt{-1}$$
   
Een complex getal (c) bestaat uit twee componenten: een reëel deel ($$\alpha$$) en een extra imaginair deel ($$\beta i$$):

   - complex getal: c = $$\alpha + \beta i$$

Een gebruikelijke manier om deze getallen voor te stellen is in het zogenaamde **complexe vlak**, een 2-dimensionaal vlak zoals hieronder weergegeven is met een reële-as en een imaginaire-as die het complexe deel van het getal weergeeft. Twee voorbeelden van complexe getallen zijn bijvoorbeeld $$c = -5 + 3i$$ en $$c=-2-4i$$. Deze zijn beide in blauw weergegeven. Er zijn ook getallen in rood weergegeven; daar komen we verderop nog op terug.

<p align="center">
![](ComplexeGetallen.png){: style="width:70%"}
</p>

Het optellen van complexe getallen is simpelweg het optellen van de reële en de complexe componenten, maar bij het vermenigvuldigen is het even opletten dat je de rekening houdt met het feit dat $$i^2 = -1$$. Een getal kwadrateren bijvoorbeeld:

   - kwadrateren (vermenigvuldigen): $$(\alpha + \beta i)^2 = (\alpha^2 - \beta^2) + (2 \alpha \beta)i$$

Als voorbeeld: $$(2+i)^2 = 3+4i$$. Als je hierbij het oorspronkelijke getal $$(2+i)$$ weer bij optelt kom je uit op $$5+5i$$. Deze getallen zijn alledrie in rood weergegeven in het hierboven getekende complexe vlak.

Dit is alle wiskundige achtergrond over complexe getallen die je nodig hebt in deze opgave. Daar gaan we.


### Zelf de Mandelbrot tekenen

Voor elk punt in het complexe vlak ($$z_0 = x_0 + y_0i)$$ kunnen we functie (in dit geval een een polynoom) definiëren die
aangeeft naar welke punt (weer een complex getal) het punt zich verplaatst. Een belangrijke set polynomen wordt gegeven door:

   $$f(z) = z^2 + c$$

Elk punt $$z_0$$ dat je kiest eert geeft een nieuw punt z1 = f(z0) = z2
0 + c. Het is zo
steeds mogelijk om het volgende punt te berekenen, immers z2 = f(z1) = z2
1 + c en
meer algemeen zn = f(n)(z0). Er zijn nu 2 mogelijkheden:
De reeks convergeert ! z0 is wel onderdeel van de set
De reeks divergeert ! z0 is geen onderdeel van de set
Elke keuze van c geeft een uniek patroon. De Mandelbrotset is speciaal omdat in
dat geval geldt dat c het startpunt zelf is, dus c = z0. Als je een punt een kleur
geeft als het in de set zit krijg je de karakteristieke plaatjes zoals beneden.




## Checkpy

Er is voor deze opdracht geen checkpy oplossing aanwezig. You're on your own.
