# Opdracht: Sensordata verwerken  

![](StravaLogo.png){:.inline}{: style="width:8%"}

Een mobiele telefoon bevat enorm nauwkeurige sensoren om grootheden als positie, snelheid, versnelling etc vast te leggen. Naast navigatie wordt dit ook toegepast in allerlei apps die voor sporten worden gebruikt. In deze opgave gaan we aan de slag met de data die verzameld wordt in de app die door de meeste wielrenners gebruikt wordt: Strava. Na de rit kan je in de app allerlei gegevens over je rit terugkijken: de projectie van de route op een interactieve kaart, de gemiddelde snelheid, het hoogteprofiel, records op kleine stukken etc etc. We gaan in deze opgave een paar van deze dingen namaken en, niet verder vertellen, een deel van de data manipuleren: digitale doping.

Onze data-set is een fietsrit in de buurt van Leiden die een natuurkundige aan de universiteit van Amsterdam maakte samen met zijn buurman. De data-file zoals die door de app gebruikt wordt is te downloaden via de volgende link:

<http://www.nikhef.nl/~ivov/Python/SensorData/FietsRitData.gpx>

De eerste regels van de file bevatten wat tekst, maar daarna wordt het interessant. Er worden (ongeveer) elke seconde drie zaken vastgelegd: positie, hoogte (elevation) en de tijd. Dit is genoeg informatie om de rest te berekenen. In het plaatje hiernaast zie je een kleine preview van de eerste drie metingen die in de file te vinden zijn:

![](DataFilePreview.png){: style="width:40%"}

Als je goed kijkt zie je dat elk data-punt/meting bestaat in drie regels wordt weggeschreven:

	1) positie in lengte- en breedtegraad 
	2) de hoogte
	3) de datum en tijd

We gaan stap voor stap een programma **Strava.py** schrijven dat de volledige file doorloopt, de metingen uit de file decodeert en in afzonderlijke lijsten opslaat. We doen dat aan de hand van de onderstaande opdrachten.

## Opdracht 1: de afgelegde route op het scherm

Maak een functie **Fietsrit()** die de file opent, alle metingen doorloopt en voor elk punt de positie bijhoudt in twee afzonderlijke lijsten: de latitude en de longitude. Maak aan het eind  een grafiek van de meetpunten. Orienteer het zo dat het op een kaart van Google maps geprojecteerd zou kunnen worden, dus het noorden netjes in het noorden etc.

Schrijf een programma **Strava.py** dat de volledige file doorloopt, de x-positie en y-positie van elke meting in twee afzonderlijke lijsten opslaat en er een grafiek van maakt op het scherm. Geef het beginpunt aan met een grote groene stip en het eindpunt met een kleine rode. 

Verderop in de opgave gaan we nog wat extra informatie toevoegen op het scherm. Hou dus iets ruimte over bij het tekenen van de grafiek.  Randen grafiek:
	 longitude tussen 4.325 en 4.675
	 latitude tussen 52.05 en 52.16

### Computing tips:

Tijdens het inlezen van elke regel kan je een test uitvoeren of er een bepaalde string in de regel voorkomt. Als je de file bekijkt zie je dat je de regel met de positie kan herkennen door de lettervolgorde *<trkpt*. Zodra je de regel 'herkend' hebt moet je natuurlijk zelf op de juiste manier de posities herkennen om de

       if "<trkpt" in line: 
           latitude = ....
           longitude = ....

*Let op:* zodra je het stukje regel hebt herkent waar de latitude is opgeslagen herkent de computer dit nog steeds al tekst en niet als getal. Gebruik de functie float() om dat stukje van de regel ook echt om te zetten in een getal voor je het opslaat in de lijst. Zo kan je er verderop in het programma ook mee rekenen.


## Opdracht 2: afgelegde afstand en de grafiek van de snelheid als functie van de tijd

Maak een grafiek van de snelheid als functie van de tijd, waarbij de tijd weergegeven is als aantal seconden na het begin van de rit. Geef ook in de grafiek duidelijk aan wat de maximale snelheid was: groene stip op het juiste tijdstip op de plek van de hoogste snelheid.

Print ook naar het scherm:


	- Rit: de totale duur van de rit was x uur, y minuten en z seconden
	- Rit: de totaal afgelegde weg was x.x km
	- Rit: de gemiddelde snelheid was xx.x km/uur
        
### Stappenplan:

	- stap 1: maak de lijst met meettijden (in seconden na het begin van de rit)


Als je de regel met de tijdstippen hebt gedecodeerd (uur, minuten en seconden) is het handig om die om te rekenen naar een aantal seconden sinds het begin van de dag. Dit maakt het daarna eenvoudig om het verschil tussen verschillende meetmomenten te berekenen. En om het helemaal makkelijk te maken kan je zodra je het eerste meetmoment hebt gevonden dat definieren als t=0. Elk meetpunt kan je daarna uitrekenen als verlopen tijd ten opzichte van dat tijdstip en dat zo in de lijst opslaan.

    - maak de lijst met snelheden 


Zodra je vanuit de datafile alle posities en tijden hebt ingelezen kan je de file sluiten. Je hebt dan alle informatie die je nodig hebt en kan de 'afgeleide' informatie zelf uitrekenen. Wij gaan bijvoorbeeld de totale afgelegde weg en de lijst met snelheden op elk tijdstip uitrekenen. Als we bij meetpunt *i* zijn aangekomen weten we zowel de afgelegde weg (verschil tussen de twee posities) als het tijdsverschil en kunnen zo de snelheid op dit kleine interval berekenen. Sla de snelheden op elk meetpunt op in een lijst.

*Let op:* we nemen aan dat de fietser stilstond op t=0, dus het eerste element in de lijst met snelheden is 0.

    - de lijst met totaal afgelegde afstand


Tijdens het (opnieuw) doorlopen van de lijsten om de snelheidslijst te vullen kan je nu ook de totale (tot nu toe) afgelegde weg bijhouden in een lijst. Ook deze list begint met 0 op t=0.

        


## Opdracht 3: afgelegde route op het scherm printen met extra informatie



## De afgelegde route

Maak een grafiek van de positie van de auto en kleur de route groen (rood) op de stukken van de route waar de snelheid van de auto meer (minder) was dan 50 km/uur.
