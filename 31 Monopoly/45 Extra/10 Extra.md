# Deeltjes in een doos

In een doos (afmeting $$0 \leq x \leq 1$$ en $$0 \leq y \leq 1$$) worden op een bepaalde plek ($$x_{bron}, y_{bron}$$) = (0,25;0,75) een aantal deeltjes weggeschoten in een willekeurige richting en snelheid. Voor elk deeltje $$i$$ geldt:

   - snelheid $$(v_{i}): 0 < v_{i} < 0.10$$
   - hoek $$(\alpha_{i}): 0 < \alpha_{i} < 2\pi$$
   
<p align="center">
![](ParticlesInABox_box.png){: style="width:50%"}
</p>

We gaan in deze opdracht de positie van een groot aantal deeltjes volgen. In deel 1 zullen we aannemen dat de deeltjes niet botsen (dat maakt de simulatie veel  makkelijker). Deel twee van deze opgave bevat de echte botsingsdynamiek, maar daarmee wordt het wel gelijk een stuk lastiger. 


## Deel 1: niet-botsende deeltjes

Onze aannames in dit deel van de opdracht:

   1.  Er worden 1000 deeltjes geproduceerd
   
   2.  De deeltjes ketsen elastisch tegen de wanden en kunnen de doos niet uit

   3.  De deeltjes hebben geen afmeting en kunnen niet botsen

   4.  De doos is gesloten
   
Het is handig om de volgende stappen te volgen:

##### stap 1: genereer een beginsituatie
  
  Elk deeltje wordt gekarakteriseerd door vier getallen: de x-positie (x), de y-positie (y) en de snelheid in de x-richting (vx) en de y-richting (vy). Maak daarom in het begin van je programma vier lijsten aan die de posities en snelheden van alle deeltjes bevatten.
  
**Tips:**

   - Als je in het begin (t=0) de random snelheid en richting hebt gekozen voor het deeltje kan je die gelijk omschrijven in termen van vx en vy. Deze snelheden zullen niet meer veranderen van grootte (bedenk waarom niet), tenzij het deeltje tegen de wand botst natuurlijk.
   
   - begin niet gelijk met 1000 deeltjes, maar volg eerst een enkel deeltje om te kijken of het deeltje zich wel gedraagt zoals je denkt dat je het geprogrammeerd hebt: ketst het bijvoorbeeld wel (goed) af van de wanden etc.

   - Hoewel het helemaal in het begin van het programma handig is om het pad van een deeltje te volgen (botst hij wel netjes terug van de wanden) is het **niet** handig om in je programma voor elk deeltje de positie en snelheid bij als functie van de tijd bij te houden. Je programma bevat op elk moment in de tijd alleen de vier lijsten met de posities en snelheden die de deeltjes op dat moment hebben.
   
##### stap 2: maak stapjes in de tijd

Omdat elk deeltje een snelheid heeft zal zijn positie veranderen in de tijd. Maak kleine stapjes in de tijd ($$\Delta t$$) en bereken op welke nieuwe positie het deeltje terecht zal komen. Gebruik hiervoor, als voorbeeld voor de positie in de x-richting): 

  $$x_i(t+\Delta_t) = x_i(t) + v_x,i(t)\Delta t$$ 

De snelheid in de x-richting zal onveranderd blijven, tenzij het deeltje tegen de wand botst natuurlijk. Bedenk zelf wat er moet gebeuren als het deeltje op een positie buiten de doos terechtkomt. De deeltjes mogen de doos immers niet uit.


##### Opdracht 1: gesloten doos

Schrijf een programma `deeltjes_in_doos.py` dat 100 deeltjes produceert en de simulatie in de tijd laat lopen gedurende een groot aantal stappen. Het programma moet twee grafieken produceren:
 
   - Een grafiek van het aantal deeltjes aan de rechterkant van de doos ($$x_i > 0,5$$) als functie van de tijd.

##### Opdracht 2: doos met een gat

Stel nou dat er een gat in de doos zit ($$y_{gat} = 0$$ en $$0,8 \leq x_{gat} \leq 0,9$$). Het is dan mogelijk dat deeltjes uit de doos ontsnappen. Het tijdstip waarop (meer dan) de helft (of meer) van de deeltjes noemen we $$t_{50}$$.

Gebruik je programma uit opdracht 1 als basis en breid die zodanig uit dat het als input een variabele `Igat` meeneemt als argument. Igat=0(1) betekent dat er niet (wel) een gat in de doos zit. Als je optie Igat=0 meegeeft dan produceert het programma de grafieken van opdracht 1. 

Breid het programma uit opdracht 1 zo uit dat (optie Igat=1) deeltjes die door het gat verdwijnen uit de lijsten verwijderd worden. Hou op elk moment bij hoeveel deeltjes er nog in de doos zitten en bepaal de tijd waarop voor het eerst (meer dan) de helft van de deeltjes uit de doos zijn verdwenen. 

Start ook hier in het begin met 1000 deeltjes. Je programma moet de volgende output op het scherm printen:

    "Op t = xxx zijn voor het eerst meer dan 50% van de deeltjes verdwenen."


**Nadenkertje:** Zou je ook zonder een computerprogramma een schatting voor $$t_{50}$$ kunnen geven? Hoe zou je dat aanpakken? Dit hoef je niet in te leveren.


## Deel 2: botsende deeltjes

Er zijn verschillende mogelijkheden om deze simulatie uit te breiden met meer realisme. Het visualiseren van een simulatie is erg leuk en interessant omdat het je meer
inzicht geeft in mogelijke programmeerfouten en fenomenen die soms niet gelijk opvallen als je naar de vergelijkingen zelf kijkt. We zullen de deeltjes ook een 'echte'
afmeting geven en de deeltjes te laten botsen.

![](collidingballs_4.gif){: style="width:50%"}{:.inline}

Je mag in deze opdracht zelf weten waar je de deeltjes neerzet in de doos op het startmoment. Omdat de animatie (nu met circels i.p.v puntjes zoals eerder in de opgave) net even lastiger is hebben we een voorbeeld template aangeleverd dat jullie zelf aan kunnen passen: [animation_template_circles.py](https://www.nikhef.nl/~ivov/Python/DeeltjesInDoos/animation_template_circles.py)

##### Opdracht 4: deeltjes: met afmeting en met botsen

Schrijf een programma `deeltjes_in_doos_animatie_realistisch.py` om een paar deeltjes door de doos te zien bewegen als functie van de tijd. Gebruik hierbij als basis de bovenstaande template. Geef de deeltjes een afmeting en laat ze netjes van de wand ketsen als de rand van het deeltje de wand raakt. En dus niet het centrum van het deeltje. 

Laat vervolgens ook de deeltjes onderling botsen. De botsingsdynamica (in twee dimensies) die je daarbij nodig hebt staat hier netjes opgeschreven:
[2-dimensional elastic collisions without trigonometry](http://www.vobarian.com/collisions/2dcollisions2.pdf).



## Checkpy

Er is voor deze opdracht geen checkpy oplossing aanwezig. You're on your own.
