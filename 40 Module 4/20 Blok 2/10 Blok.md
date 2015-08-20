
# Opgave 2: Klimaat in Nederland

![](KaartNederlandKlein.png)

Laten we een steentje bijdragen aan de klimaatdiscussie en data analyseren die 
door de ECA (European Climate Assessment) beschikbaar wordt gemaakt in grote 
ASCII files. Data sets zijn hier beschikbaar: ECA data-sets.

We hebben maar 1 dag de tijd dus we beperken ons tot de data die verzameld 
is in De Bilt.

Data Files: 

   - Maximum temperatuur: [DeBiltTempMax.txt](http://www.nikhef.nl/ ̃ivov/Python/KlimaatData/DeBiltTempMax.txt) 

   - Minimum temperatuur: [DeBiltTempMin.txt](http://www.nikhef.nl/ ̃ivov/Python/KlimaatData/DeBiltTempMin.txt) 

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

     De hoogste temperatuur die ooit werd gemeten was 34,5 graden Celcius op 13 mei 1967


### Vraag 2b) koud kouder koudst
Wat is de langste periode dat het aaneengesloten heeft gevroren (maximumtemperatuur 
onder 0 ◦C). Wat was de laatste dag van deze periode ?

### Vraag 2c) zomerse en tropische dagen
   
We spreken van een zomerse (tropische) dag als de maximumtemperatuur meer dan 25 
(30 graden Celcius was.

Maak een grafiek waarom (tegelijkertijd) het aantal zomerse en tropische dagen per 
jaar te zien is voor alle jaren waar we data van hebben.


### Vraag 2c) hittegolf in 2015

We spreken in Nederland van een hittegolf als:

     de maximumtemperatuur is ten minste vijf dagen achtereen minstens 25,0 °C 
     (zomerse dagen) waarvan ten minste op drie dagen 30,0 °C of meer (tropische dagen). 

Is er een hittegolf geweest in 2015 ?
   
