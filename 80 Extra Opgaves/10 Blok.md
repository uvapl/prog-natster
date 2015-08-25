
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
    
    
# Opgave 1: klimaatdiscussie in het kikkerlandje    
    
    
![](KaartNederlandKlein.png)

Laten we een steentje bijdragen aan de klimaatdiscussie en data analyseren die door de ECA (European Climate Assessment) beschikbaar wordt gemaakt in grote ASCII files. Data sets zijn hier beschikbaar: 
http://eca.knmi.nl/dailydata/predefinedseries.php

We beginnen bescheiden: de temperatuur in De Bilt (station 162). Omdat
de data sets groot zijn hebben we die van De Bilt beschikbaar gemaakt op http://www.nikhef.nl/ ̃ivov/Python/KlimaatData/.

Download de files 

   - TX STAID000162.txt (maximum temperatuur per dag) 
   - TN STAID000162.txt (minimum temperatuur per dag)
   
Open ze en lees bovenin hoe de data gecodeerd is. Je kan dan bijvoorbeeld zien dat op 1 januari 1901 de max(min) temperatuur -3.1(-6.8) ◦C was. 


Schrijf een programma dat de file doorloopt en beantwoord de volgende vragen.
a) maximumtemperatuur
Wat waren de hoogste en laagste temperatuur die in De Bilt in de 20ste eeuw zijn gemeten ? Op welke dagen was dat ?
b) koud koud koud
Wat is de langste periode dat het aaneengesloten heeft gevroren (maximumtemper- atuur onder 0 ◦C). Wanneer eindigde deze periode ?