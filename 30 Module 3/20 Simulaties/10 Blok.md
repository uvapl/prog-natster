# Simulaties

Als je al weet dat je vier om elkaar heen draaiende ballen niet analytisch uit
kan rekenen dan is het duidelijk dat er enorm veel (bijna alle) problemen
uiteindelijk met een computersimulatie doorgerekend worden. Met een computer
kan je kleine stapjes in de tijd nemen en op elk tijdstip alle krachten
berekenen die er op een voorwerp werken en zo per deeljte kan kijken welke kant
hij op zal bewegen en met welke snelheid.

We starten nu met een probleem waarbij je de antwoorden zelf nog kunt
controleren en uitrekenen, maar daarna ben je op je programmeer-skills en je
natuurkundige intuitie aangewezen om uiteindelijk tot het het antwoord te komen.

# Opgave 1: appel valt van de Dom

Schrijf een programma **appel.py** dat de beweging van de appel beschrijft als
die op een hoogte van 100 meter wordt losgelaten.

![](GravityOverzicht.png)

Zorg dat je programma kleine stapjes in de tijd maakt ($$\Delta t=0.01$$
seconden) en hou steeds bij op welke hoogte de appel zich bevindt ($$x$$) en met
welke snelheid hij beweegt ($$v$$).

Bereken voor elke nieuw stapje in de tijd en in deze volgorde:

1. de kracht die op de appel werkt (F)
2. de versnelling die de appel daardoor krijgt (a)
3. de nieuwe snelheid die de appel daardoor krijgt (v)
    gebruik: $$v_{\rm nieuw} = v + a \Delta t$$
4. de nieuwe positie van de appel (x). 
    gebruik: $$x_{\rm nieuw} = x + v \Delta t$$

Je hebt dan een nieuwe positie en snelheid gekregen en je kan vervolgens een stapje in de tijd maken en deze cyclus herhalen.

Zorg dat de volgende grootheden bepaald worden en op het scherm weergegeven worden aan het eind van je programma:

1. Na hoeveel seconden raakt de appel de grond?

2. Met welke snelheid (km/uur) raakt de appel de grond?

3. Na hoeveel seconden heeft de appel een snelheid van 100 km/uur bereikt? Is
    een vallende appel daarmee sneller dan Bugatti Veyron (2.46 seconden) of niet?

Tip:

- Gebruik bovenstaande formule en start de appel dus op x = $${\rm R_{earth}}$$ + 100 meter. Als je wilt weten hoe hoog de appel is, de grootheid die je iets zegt en die je ook in de plots gebruikt, gebruik dan h = x - $${\rm R_{earth}}$$.
- Let goed op het teken van de krachten en snelheden. je begint bij positieve $$x$$ en beweegt dan naar $$x=0$$ toe.
- In dit voorbeeld kan je de antwoorden ook zelf uitrekenen met behulp van pen en papier.
- Bereken alles eerst in m/s en reken dan voor punt 2 de snelheid om naar km/uur.



# Opgave 2: vrije val van base jumpers

In de vorige opgave is de luchtwrijving verwaarloosd waardoor je ook met behulp van de natuurkunde 
van de middelbare school de antwoorden kon controleren. We gaan nu een stuk realisme toevoegen: luchtwrijving. 

De luchtweerstand die een vallend voorwerp ondervindt is evenredig met het kwadraat van de snelheid. 

$$F = \xi v^2$$, met $$ \xi = 0.24$$

Hoewel de luchtweerstand ook afhankelijkheid is van de oppervlakte en massa van
het object en de dichtheid van de lucht zullen we in deze opdracht alleen het
effect van de snelheid bestuderen. De wrijving betekent dat er een snelheid is
waarbij de zwaartekracht en de wrijving elkaar in evenwicht houden. Deze
maximum snelheid die een parachutespringer kan bereiken, ongeveer 196 km/uur
wordt [terminal velocity](https://en.wikipedia.org/wiki/Terminal_velocity) genoemd.

![](Freefall.png)

Schrijf een programma **basejump.py** dat de val beschrijft van een base jumper
die van de top van de Burj Khalifa in Dubai (828 m) naar beneden springt. Volg
dezelfde strategie als in de eerste, maar neem nu ook de luchtweerstand mee
zoals gegeven in bovenstaande formule. Nee hierbij aan dat de basejumper 72 kilo weegt.

1. Maak een grafiek van de snelheid als functie van de tijd.

    Tip: test je programma door net te doen of de toren 2000 meter hoog is en te kijken of je inderdaad vindt dat de terminal velocity ongeveer 196 km/uur is.

2. Maak een grafiek van de hoogte als functie van de tijd. 

    Teken 2 lijnen in dezelfde figuur: in het groen/blauw de situatie als we luchtweerstand wel/niet verwaarlozen.
    
3. De base jumper is eerst in vrije val, maar op 100 meter van het oppervlak moet deze de parachute opengooien. Hoeveel tijd heeft de jumper vanaf de afsprong tot dat moment, als we de luchtweerstand buiten beschouwing laten? Hoeveel langer heeft de base-jumper om te genieten van de vrije val dankzij de luchtweerstand?

    Zoals altijd heb je ook hier mensen die het [randje opzoeken](https://en.wikipedia.org/wiki/Speed_skydiving).

    Omdat hij zijn sprong maakte in een gebied waar de luchtdruk enorm laag was is het record met 1342 km/uur veilig in handen van Felix Baumgartner.


## Sanity check

Je kunt deze opgaven allemaal maken met de Python-onderdelen die je kent uit modules 1 en 2!
