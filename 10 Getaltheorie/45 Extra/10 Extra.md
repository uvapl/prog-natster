# Onderling priem

Schrijf een programma `priemparen.py` dat de waarschijnlijkheid berekent dat twee willekeurig gehele getallen geen gemeenschappelijke deler hebben. Zo'n paar wordt
'onderling-priem' genoemd. De Engelse term is 'coprime'.

    #python priemparen.py
    De kans dat twee random getallen geen onderlinge deler hebben is:
        - voorspelling (wiskunde): x.xx %
	    - empirisch (Python): x.xx %

Hoewel we in deze opdrachten jullie zoveel mogelijk vrij willen laten (er is ook geen `checkpy`) zullen we voor deze eerste extra opdracht nog een aantal tussenstappen aangeven. 

### Definitie van onderling-priem en voorspelling vanuit getaltheorie
	    
In de informatie over de definitie van deze [wikipedia co-primes](https://en.wikipedia.org/wiki/Coprime_integers) lezen we ook terug wat de kans is dat *n* willekeurige getallen géén gemeenschappelijke deler hebben. 

Deze kans is: $$\frac{1}{\zeta(n)}$$. 

, waarbij $$\zeta(n)$$ de beroemde [Riemann zeta functie](https://en.wikipedia.org/wiki/Riemann_zeta_function) is.

**Let op:** in het geval van drie (of meer) of meer getallen betekent `gemeenschappelijke deler` dat er een getal is dat een deler is van *alle* drie (of meer) getallen *tegelijk*.

**Specifiek geval: tewee getallen (n=2)**:

De kans dat twee willekeurige getallen géén gemeenschappelijke deler hebben is: 

$$\frac{1}/{\zeta(2)} = \frac{6}{\pi^2} \approx 0,608$$.


In deze opdracht gaan we zelf van twee willekeurige getallen bekijken of ze een gemeenschappelijke deler hebben. Door dit een groot aantal keer doen kunnen we de kans bepalen dat twee van zulke getallen onderling-priem zullen zijn. En of de voorspelling uit de getaltheorie klopt.

### Zelf de oplossing vinden

Er zijn verschillende manieren om dit problem aan te pakken. Volg voor deze opdracht de onderstaande oplossingsmethode en tussenstappen, omdat we daarbij bij het nakijken hoe ver je bent gekomen.

#### stap 1: lijst met priemfactoren

Elk getal is op een unieke manier te schrijven als het product van priemgetallen:

        34 = 2 x 17
        88 = 2 x 2 x 2 x 11
     79220 = 2 x 2 x 5 x 17 x 233

Schrijf een functie `PriemFactoren(getal)` die voor een bepaald getal de lijst met de priemfactoren (de delers) vindt en op het scherm kan printen.

    python> Priemfactoren(79220) 
            Priemfactoren  79220  =  [2, 2, 5, 17, 233]

Zorg ook dat de functie de lijst met priemgetallen als output teruggeeft (als return). Later in het programma zullen we deze functie meer gaan gebruiken
 
#### stap 2: op zoek naar gemeenschappelijke delers van twee getallen

Schrijf een functie `AantalDelers(n1, n2)` die voor twee getallen aangeeft of er een gemeenschappelijke deler is of niet. Gebruik hierbij de functie `Priemfactoren()` om voor elk van de getallen eerst de priemfactor-lijst te vinden en ga vervolgens op zoek naar getallen die in beide lijsten voorkomen.

Op dit moment is het niet van belang om het precieze aantal gemeenschappelijke delers te bepalen. Voor deze opgave is het vooral belangrijk om te weten of er *géén* gemeenschappelijke delers zijn. De functie moet dan als return argument 0 teruggeven.

#### stap 3: Hypothese testen voor groot aantal paren

Om de fractie van paren te bepalen waarin er geen gemeenschappelijke deler is moeten we:
   1. een groot aantal paren getallen maken
   2. voor elk paar kijken of er wel/niet een gemeenschappelijke deler is
   3. aan het eind bekijken welke fractie paren geen gemeenschappelijke deler had  

Maak een functie `Experiment()` die deze stappen implementeert en die de fractie als aan het eind de fractie op het scherm print en ook teruggeeft als return argument.

Specificaties:
    - gebruik getallen (n1 en n2) tussen de 10.000 en 100.000
    - gebruik 10.000 paren
    
**Python tip:**

Een van de dingen die we nodig hebben, het trekken van een willekeurig getal, is iets waar we pas in module 2 mee gaan werken. In dit geval is het nog specifieker, namelijk een willekeurig *geheel* getal. 

Plaats bovenaan je programma de volgende regel die je in staat stelt de `random-bibliotheek` te gebruiken in je programma. Deze bibliotheek bevat allerlei functies die random getallen maken.
 
        from random import *
        
De functie die wij nodig hebben is `randint(Nmin,Nmax)` die een random geheel getal teruggeeft tussen `Nmin` en `Nmax`. In onze opgave gebruiken we Nmin=10000 en Nmax = 100000. Om in je code een random geheel getal `n1` te krijgen gebruik je de volgende regel: 

         n1 = randint(Nmin, Nmax)        
        

Aan het eind van deze functie weet je dus de fractie paren die *géén* gemeenschappelijke deler hebben.

#### stap 4: Theoretische voorspelling

Schrijf een functie `Voorspelling(n)` die de kans uitrekent dat er geen gemeenschappelijke deler is voor `n` getallen. Dit is niet veel meer dan zelf de zeta functie uitrekenen en daarmee de kans bepalen. Geef deze kans terug als returnwaarde.

#### stap 5: Gooi alles bij elkaar

Door nou de twee functies `Experiment()` en `Voorspelling()` aan te roepen valt alles samen. Print beide getallen op het scherm.


## Extra extra opgave

Probeer bovenstaande ook eens voor triplets: n=3.


## Checkpy

Er is voor deze opdracht geen checkpy oplossing aanwezig. You're on your own.
