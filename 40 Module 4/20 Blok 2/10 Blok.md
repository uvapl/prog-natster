
# Opgave 2: Klimaat in Nederland

![](KaartNederlandKlein.png)

Laten we een steentje bijdragen aan de klimaatdiscussie en data analyseren die 
door de ECA (European Climate Assessment) beschikbaar wordt gemaakt in grote 
data files. Data sets zijn hier beschikbaar: [ECA data-sets](http://eca.knmi.nl/dailydata/predefinedseries.php)
We hebben maar 1 dag de tijd dus we beperken ons tot data die de maximum en minimum 
temperatuur beschrijft voor elke dag in De Bilt sinds 1901.

Data Files: 

   - Maximum temperatuur: [DeBiltTempMax.txt](http://www.nikhef.nl/~ivov/Python/KlimaatData/DeBiltTempMax.txt) 

   - Minimum temperatuur: [DeBiltTempMin.txt](http://www.nikhef.nl/~ivov/Python/KlimaatData/DeBiltTempMin.txt) 

Download de file, open ze en lees bovenin hoe de data gecodeerd is. We zien dat de 
maximum(minimum) temperatuur op 1 januari 1901 -3.1(-6.8) ◦C was.

Schrijf een programma `Temperatuur.py` die de file regel voor regel inleest en 
beantwoord de volgende vragen.

### Vraag 2a) extreme temperaturen
Wat waren de hoogste en laagste temperatuur die in De Bilt zijn gemeten sinds het begin 
van de 20ste eeuw ? Op welke dagen was dat ? Zorg dat je programma de datum netjes op 
het scherm print. Zeg dus niet: 

     Max 34,5 op 19670513

maar      

     De hoogste temperatuur was 34,5 graden Celcius werd gemeten op 13 mei 1967


### Vraag 2b) koud kouder koudst
Wat is de langste periode dat het aaneengesloten heeft gevroren (maximumtemperatuur 
onder 0 ◦C). Wat was de laatste dag van deze periode ?

### Vraag 2c) zomerse en tropische dagen
We spreken van een zomerse (tropische) dag als de maximumtemperatuur meer dan 25 
(30 graden Celcius was.

Maak een grafiek waarin voor elk jaar zowel het aantal zomerse als het aantal 
tropische dagen weergegeven wordt.

### Vraag 2d) hittegolf in 2015

We spreken in Nederland van een hittegolf als de maximumtemperatuur ten minste vijf 
dagen achtereen minstens 25,0 °C was (zomerse dagen) waarvan ten minste op drie 
dagen 30,0 °C of meer (tropische dagen). 

Bekijk of er een officiele hittegolf geweest in 2015 ?
   
