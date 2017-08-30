# Opdracht: Sensordata verwerken  

![](StravaLogo.png){:.inline}{: style="width:8%"}

Een mobiele telefoon bevat enorm nauwkeurige sensoren om grootheden als positie, snelheid, versnelling etc vast te leggen. Naast navigatie wordt dit ook toegepast in allerlei apps die voor sporten worden gebruikt. In deze opgave gaan we aan de slag met de data die verzameld wordt in de app die door de meeste wielrenners gebruikt wordt: Strava. Na de rit kan je in de app allerlei gegevens over je rit terugkijken: de projectie van de route op een interactieve kaart, de gemiddelde snelheid, het hoogteprofiel, records op kleine stukken etc etc. We gaan in deze opgave een paar van deze dingen namaken en, niet verder vertellen, een deel van de data manipuleren: digitale doping.

Onze data-set is een fietsrit in de buurt van Leiden die een natuurkundige aan de universiteit van Amsterdam maakte samen met zijn buurman. De data-file zoals die door de app gebruikt wordt is te downloaden via de volgende link:

<http://www.nikhef.nl/~ivov/Python/SensorData/FietsRitData.gpx>

De eerste regels van de file bevatten wat tekst, maar daarna wordt het interessant. Er worden (ongeveer) elke seconde drie zaken vastgelegd: positie, hoogte (elevation) en de tijd. Dit is genoeg informatie om de rest te berekenen. In het plaatje hiernaast zie je een kleine preview van de eerste drie metingen die in de file te vinden zijn:


![](DataFilePreview.png){: style="width:40%"}


welke informatie elk veld bevat. Dit is typisch hoe je een databestand binnen krijgt: in een formaat dat snel automatisch te lezen is, maar soms ontbreken duidelijke omschrijvingen van wat het nu precies allemaal is. Toch moet je wel aardig kunnen afleiden wat je er mee kunt. (Probeer dus ook eerst zelf wijs te worden uit het bestand voordat je met anderen in discussie gaat hierover. Goede oefening!)





Schrijf een programma **fietsrit.py** dat de file doorloopt, de data verwerkt en beantwoord de volgende vragen.

## Afgelegde afstand

Maak een grafiek van de snelheid van de auto (in km/uur) als functie van de tijd en gebruik de data om een schatting te maken van de totaal afgelegde weg.

## De afgelegde route

Maak een grafiek van de positie van de auto en kleur de route groen (rood) op de stukken van de route waar de snelheid van de auto meer (minder) was dan 50 km/uur.
