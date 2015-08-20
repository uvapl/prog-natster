
# Opzet en doel Module 4

Een veel voorkomende toepassing van computerprogramma’s is het inlezen en ver- werken van grote data bestanden. We zullen in Module 4 een korte toepassing bekijken hiervan.

a) lezen file:

	input_filehandle = open(’inputfile.txt’, ’r’)
	for line in input_filehandle:
        print line
	input_filehandle.close()

Toegang tot de verschillende parameters in de regel krijg je door de regel in stukken te ’knippen’, bijvoorbeeld met behulp van het `split` commando. Het commando elementen = `line.split()` produceert een lijst met elementen die de losse stukken bevatten. Hierop kan je afzonderlijke bewerkingen uitvoeren.


b) inlezen en uitschrijven file:

	input_filehandle = open(’inputfile.txt’, ’r’)
	output_filehandle = open(’outputfile.txt’, ’w’)
	for line in input_filehandle:
        newline = line + " XXXX"
        output_filehandle.write(newline)
    input_filehandle.close()
    output_filehandle.close()
    
    
# Opgave 1: Sensor Data 
    
Een iPhone bevat veel delicate sensoren die informatie verzamelen over de 
positie, snelheid, versnelling. We hebben gedurende een korte auto-rit de 
data opgeslagen en in een file weggeschreven met een frequentie van 1 [Hz]. 

![](KaartAmsterdam.png)


De sensor data is beschikbaar in de file `AutoRitData.csv` en is te downloaden 
via de volgende link:

Data-file: [AutoRitData.csv](http://www.nikhef.nl/~ivov/Python/SensorData/AutoRitData.csv)

Bovenin de file staat kort welke informatie elk veld bevat.

Het verzamelen van de data begon toen de auto zich bevond op de plek waar de 
snelweg A4 op de A10 aansluit. Het verzamelen van de data stopte toen de auto 
op het Nikhef was aangekomen. Schrijf een programma `Autorit.py` dat de file 
doorloopt, de data verwerkt en beantwoord de volgende vragen.

## vraag 1a) afgelegde afstand
Maak een grafiek van de snelheid van de auto (in km/uur) als functie van de 
tijd en gebruik de data om een schatting te maken van de totaal afgelegde weg.

## vraag 1b) teken de afgelegde route
Maak een grafiek van de positie van de auto en kleur de route groen(rood) 
op de stukken van de route waar de snelheid van de auto groter(kleiner) 
was dan 50 km/uur.


