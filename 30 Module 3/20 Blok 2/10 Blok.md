
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

Tip:

  - Gebruik bovenstaande formule en start de appel dus op x = $${\rm R_{earth}}$$ + 100 meter. Als je wilt weten hoe hoog de appel is, de grootheid die je iets zegt en die je ook in de plots gebruikt, gebruik dan h = x - $${\rm R_{earth}}$$.
- Let goed op het teken van de krachten en snelheden. je begint bij positieve $$x$$ en beweegt dan naar $$x=0$$ toe.
- In dit voorbeeld kan je de antwoorden ook zelf uitrekenen met behulp van pen en papier.

Zorg dat de volgende grootheden bepaald worden en op het scherm weergegeven worden aan het eind van je programma:

### a) Na hoeveel seconden raakt de appel de grond ?

### b) Met welke snelheid (km/uur) raakt de appel de grond ?

### c) Na hoeveel seconden heeft de appel een snelheid van 100 km/uur bereikt ?
Is een vallende appel daarmee sneller dan Bugatti Veyron (2.46 seconden) of niet ?

# Opgave 2: vrije val van base jumpers

In de vorige opgave is de luchtwrijving verwaarloosd waardoor je ook met behulp van de natuurkunde van de middelbare school de antwoorden kon controleren. We gaan nu een stuk realisme toevoegen: luchtwrijving. 

De luchtweerstand die een vallend voorwerp ondervindt is evenredig met het kwadraat van de snelheid. 

$$ F = \xi v^2$$, met $$ \xi = 0.0033$$

Meer informatie kan je hier vinden:
https://en.wikipedia.org/wiki/Terminal_velocity

Schrijf een programma `BaseJump.py` die ook de luchtweerstand meeneemt. Volg dezelfde strategie als in vraag 1. We beschrijven de val van een parachute springer die van de top van de Burj Khalifa in Dubai (828 m) naar beneden springt.

### a) Maak een grafiek van de snelheid als functie van de tijd
Print op het scherm de maximale snelheid die de base-jumper bereikt.

### b) Maak een grafiek van de hoogte als functie van de tijd. 
Teken 2 lijnen in dezelfde figuur: in het groen/blauw de situatie als we luchtweerstand wel/niet verwaarlozen.
    
### c) Op 100 meter moet de base jumper zijn parachute opengooien. Hoeveel langer heeft de base-jumper om te genieten van de vrije val dankzij de luchtweerstand ?

![](Freefall.png)

Zoals altijd heb je ook hier mensen die het randje opzoeken:
https://en.wikipedia.org/wiki/Speed_skydiving

Omdat hij zijn sprong maakte in een gebied waar de luchtdruk enorm laag was is het record met 1342 km/uur veilig in handen van Felix Baumgartner.

# Opgave 3: de ultieme free-fall

De appel in vraag 1 bereikt na iets meer dan 4 seconden het aardoppervlak. Stel nou eens dat precies op de plek waar de appel neervalt een tunnel is gegraven dwars door de aarde heen. 

Schrijf een programma `Tunnel.py` die de beweging van de appel door de aarde heen beschrijft. Het deeltje beweegt langs de x-as met x=0 in het centrum van de aarde, start met snelheid 0 op hoogte 0 meter boven het aardoppervlak. Wat gebeurt er precies ?
 
![](EarthHole.png)

### Tips:
   - verwaarloos luchtweerstand in deze opgave
   - de effectieve massa van de aarde, de massa 'die aan je trekt' is
     wordt kleiner naarmate je dichter bij het centrum komt.
     Dus: als de aarde $$M_{\rm aarde}$$ weegt en je 50% van de afstand tot het
     centrum van de aarde hebt afgelegd 'weegt' de aarde in de formule van
     Newton nog maar $$\left(\frac{1}{2}\right)^3M_{\rm aarde}$$.
   - Neem aan dat de aarde een bol met constante dichtheid is.
   
### a) Maak een grafiek van de snelheid van de appel als functie van de tijd

### b) Maak een grafiek van de positie ( als functie van de tijd

### c) Wat is de maximale snelheid die de appel bereikt

### d) Hoe lang duurt het voor de appel weer terug is op de plek waar je hem losgelaten hebt ?



