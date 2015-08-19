
# Simulaties


# Opgave 1: appel valt van de Dom in Utrecht

Schrijf een programma `VallendeAppel.py` dat de beweging van de appel beschrijft als die op een hoogte van 100 meter wordt losgelaten.

![](GravityOverzicht.png)

Zorg dat je programma kleine stapjes in de tijd maakt ($$\Delta t=$$0.01 seconden) en hou steeds bij op welke hoogte de appel zich bevindt (*x*) en met welke snelheid hij beweegt (*v*). 

Bereken voor elke nieuw stapje in de tijd en in deze volgorde:

  1. de kracht die er op de appel werkt (F)
  2. de versnelling die de appel daardoor krijgt (a)
  3. de nieuwe snelheid die de appel daardoor krijgt (v). 
       Gebruik: $$v_{\rm nieuw} = v + a \Delta t$$
  4. de nieuwe positie van de appel (v). 
       Gebruik: $$x_{\rm nieuw} = x + v \Delta t$$

Je hebt dan een nieuwe positie en snelheid gekregen en je kan vervolgens een stapje in de tijd maken en deze cyclus herhalen.

Zorg dat de volgende grootheden bepaald worden en op het scherm weergegeven worden aan het eind van je programma:

### a) Na hoeveel seconden raakt de appel de grond ?

### b) Met welke snelheid raakt de appel de grond ?

### c) Na hoeveel seconden heeft de appel een snelheid van 100 km/uur bereikt ?
bereikt een vallende appel sneller de 100 km/uur dan een Formule 1 auto of niet ?

# Opgave 2: vrije val van base jumpers

In de vorige opgave is de luchtwrijving verwaarloosd waardoor je ook met behulp van de natuurkunde van de middelbare school de antwoorden kon controleren. We gaan nu een stuk realisme toevoegen: luchtwrijving. 

De luchtweerstand die een vallend voorwerp ondervindt is evenredig met het kwadraat van de snelheid. 

$$ F = \xi v^2$$, met $$ \xi = 12$$

Schrijf een programma `BaseJump.py` die ook de luchtweerstand meeneemt. Volg dezelfde strategie als in vraag 1. We beschrijven de val van een parachute springer die van de top van de Burj Khalifa in Dubai (828 m) naar beneden springt.

### a) Maak een grafiek van de snelheid als functie van de tijd
       Print op het scherm de maximale snelheid die de base-jumper bereikt.

### b) Maak een grafiek van de hoogte als functie van de tijd. Teken 2 lijnen in dezelfde figuur: in het groen/blauw de situatie als we luchtweerstand wel/niet verwaarlozen.
    
### c) Op 100 meter moet de base jumper zijn parachute opengooien. Hoeveel langer heeft de base-jumper om te genieten van de vrije val dankzij de luchtweerstand ?


![](Freefall.png)

# Opgave 3: de ultieme free-fall
![](EarthHole.png)
