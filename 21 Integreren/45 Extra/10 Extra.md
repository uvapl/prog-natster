# Fractals - Mandelbrot set

Jullie kennen vast wel die prachtige en veelkleurige plaatjes waarin patronen zich tot een oneindige diepte patronen herhalen. Deze zeer complexe patronen, **fractals** genaamd, komen gek genoeg voort uit een kleine set simpele (wiskundige) regels, iets dat we ook in de natuur regelmatig zien. In deze opgave gaan we iets meer in op de wiskunde achter de fractals en gaan we proberen daarmee zelf de meest beroemde fractal te reconstrueren en op het scherm te tekenen die hieronder ook te zien is: de [Mandelbrot set](https://en.wikipedia.org/wiki/Mandelbrot_set)

Mandelbrot set.

<p align="center">
![](mandelbrot.png){: style="width:50%"}
</p>

De opdracht van deze extra opdracht is dan ook: schrijf een programma `fractal.py` dat de Mandelbrot set op het scherm tekent.

### Stukje wiskunde: complexe getallen

Om iets te begrijpen van de wiskunde achter de fractals moeten we eerst een nieuw wiskundig concept introduceren: **complexe getallen**. Deze getallen hebben een speciale plek in wiskunde en ze komen overal in de natuurkunde terug. Jullie zullen de geheimen ervan later dan ook in verschillende colleges tegenkomen. Hier het absolute minimum.

   - we definiëren $$ i = \sqrt{-1}$$
   
Een complex getal (c) bestaat uit twee componenten: een reëel deel ($$\alpha$$) en een extra imaginair deel ($$\beta * i$$).

   - c = $$\alpha + \beta i$$

Een gebruikelijke manier om deze getallen voor te stellen is in een 2-dimensionaal vlak zoals hieronder weergegeven is. Twee voorbeelden van complexe getallen zijn bijvoorbeeld c = -5 + 3i en c=-2-4i. Deze zijn in blauw weergegeven. Er zijn ook getallen in rood weergegeven; daar komen we later op terug in de uitleg over fractals.

<p align="center">
![](ComplexeGetallen.png){: style="width:70%"}
</p>

Het optellen van complexe getallen is simpelweg het optellen van de reële en de complexe componenten en bij het vermenigvuldigen is het even opletten dat je de rekening houdt met het feit dat $$i^2 = -1$$.

   - $$(\alpha + \beta*i)^2 = (\alpha^2 - \beta^2) + (2 \alpha beta)*i$$

Zo is $$(2+i)^2 = 3+4i$$. Zowel $$2+i$$  als $$3+4i$$ zijn als rood punt weergegeven.

Dit is alle wiskundige achtergrond die je nodig hebt in deze opgave. Als je nog vragen hebt stel die dan aan de assistent.

### Zelf de Mandelbrot et tekenen

DIY

## Checkpy

Er is voor deze opdracht geen checkpy oplossing aanwezig. You're on your own.
