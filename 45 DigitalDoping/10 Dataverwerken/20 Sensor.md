# Opdracht: Sensordata verwerken  

![](StravaLogo.png){:.inline}{: style="width:8%"}

Een mobiele telefoon bevat enorm nauwkeurige sensoren om grootheden als positie, snelheid, versnelling etc vast te leggen. Naast navigatie wordt dit ook toegepast in allerlei apps die voor sporten worden gebruikt. In deze opgave gaan we aan de slag met de data die verzameld wordt in de app die door de meeste wielrenners gebruikt wordt: Strava. Na de rit kan je in de app allerlei gegevens over je rit terugkijken: de projectie van de route op een interactieve kaart, de gemiddelde snelheid, het hoogteprofiel, records op kleine stukken etc etc. We gaan in deze opgave een paar van deze dingen namaken en, niet verder vertellen, een deel van de data manipuleren: digitale doping.

Onze data-set is een fietsrit in de buurt van Leiden die een natuurkundige aan de universiteit van Amsterdam maakte samen met zijn buurman. De data-file zoals die door de app gebruikt wordt is te downloaden via de volgende link:

<http://www.nikhef.nl/~ivov/Python/SensorData/FietsRitData.gpx>

De eerste regels van de file bevatten wat tekst, maar daarna wordt het interessant. Er worden (ongeveer) elke seconde drie zaken vastgelegd: positie, hoogte (elevation) en de tijd. Dit is genoeg informatie om de rest te berekenen. In het plaatje hiernaast zie je een kleine preview van de eerste drie metingen die in de file te vinden zijn:

![](DataFilePreview.png){: style="width:40%"}

Als je goed kikt zie je dat elk data-punt/meting bestaat in drie regels wordt weggeschreven:

	1) positie in lengte- en breedtegraad 
	2) de hoogte
	3) de datum en tijd

We gaan stap voor stap een programma **Strava.py** schrijven dat de volledige file doorloopt, de metingen uit de file decodeert en in afzonderlijke lijsten opslaat. We doen dat aan de hand van de volgende opdrachten:

## Afgelegde route op het scherm

Maak een functie **Fietsrit()** je Schrijf een programma **Strava.py** dat de volledige file doorloopt, de x-positie en y-positie van elke meting in twee afzonderlijke lijsten opslaat en er een grafiek van maakt op het scherm.

Tips:




Maak een grafiek van de positie van de auto en kleur de route groen (rood) op de stukken van de route waar de snelheid van de auto meer (minder) was dan 50 km/uur.


de data verwerkt en beantwoord de volgende vragen.




## Afgelegde afstand

Maak een grafiek van de snelheid van de auto (in km/uur) als functie van de tijd en gebruik de data om een schatting te maken van de totaal afgelegde weg.

## De afgelegde route

Maak een grafiek van de positie van de auto en kleur de route groen (rood) op de stukken van de route waar de snelheid van de auto meer (minder) was dan 50 km/uur.
