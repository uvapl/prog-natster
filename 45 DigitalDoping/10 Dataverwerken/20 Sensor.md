# Opdracht: Sensordata verwerken 
    
test

![](StravaLogo.png){:.inline}{: style="width:5%"}

Een mobiele telefoon bevat veel dlsensoren die informatie verzamelen over de positie, snelheid, versnelling. Een van de manieren waarop mensen die data gebruiken is met sporten. Er zijn veel apps die mensen gebruiken om hun hardloopprestaties bij te houden, maar in deze opgave gaan we specifiek aan de slag met de app die veel gebruikt wordt door mensen op de racefiets. Jullie kennen ze wel, de groep van (net even iets te dikke) mannen van in de veertig die zichzelf twee keer per week in een fietspak hijsen en zo, vaak tevergeefs, hun conditie op peil proberen te houden door met de racefiets eropuit te trekken. De meest populaire app om die ritten bij te houden is is Strava.

In deze opgave gaan we aan de slag met een data-set die verzameld is tijdens een fietsrit in het groene hart. De sensordata is beschikbaar in de file `FietsRitData.csv` en is te downloaden  via de volgende link:

<http://www.nikhef.nl/~ivov/Python/SensorData/FietsRitData.gpx>

Bovenin de file staat kort welke informatie elk veld bevat. Dit is typisch hoe je een databestand binnen krijgt: in een formaat dat snel automatisch te lezen is, maar soms ontbreken duidelijke omschrijvingen van wat het nu precies allemaal is. Toch moet je wel aardig kunnen afleiden wat je er mee kunt. (Probeer dus ook eerst zelf wijs te worden uit het bestand voordat je met anderen in discussie gaat hierover. Goede oefening!)

Schrijf een programma **fietsrit.py** dat de file doorloopt, de data verwerkt en beantwoord de volgende vragen.

## Afgelegde afstand

Maak een grafiek van de snelheid van de auto (in km/uur) als functie van de tijd en gebruik de data om een schatting te maken van de totaal afgelegde weg.

## De afgelegde route

Maak een grafiek van de positie van de auto en kleur de route groen (rood) op de stukken van de route waar de snelheid van de auto meer (minder) was dan 50 km/uur.
