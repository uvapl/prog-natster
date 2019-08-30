# Klimaatdiscussie

![](KaartNederlandKlein.png){:.inline}

Laten we een steentje bijdragen aan de klimaatdiscussie en data analyseren die  door de ECA (European Climate Assessment) [beschikbaar](http://eca.knmi.nl/dailydata/predefinedseries.php) wordt gemaakt in grote  data files. We beperken ons tot data die de maximum- en minimumtemperatuur beschrijft voor elke dag in De Bilt sinds 1901. 

De bestanden die respectievelijk de hoogste en laagste temperatuur in De Bilt voor elke dag weergeven:


- <http://www.nikhef.nl/~ivov/Python/KlimaatData/DeBiltTempMaxSUMMER2019.txt>
- <http://www.nikhef.nl/~ivov/Python/KlimaatData/DeBiltTempMinSUMMER2019.txt>

Download de bestanden, open ze en lees bovenin hoe de data gecodeerd is. We zien dat de maximum(minimum)-temperatuur op 1 januari 1901 -3.1(-6.8) graden Celsius was.

> Let op! De datafiles bevatten ook allerlei uitleg. De bedoeling is dat je deze laat staan in het bestand. Je Python-programma moet zo geschreven zijn dat je deze regels netjes overslaat bij het verwerken!

Schrijf een programma **temperatuur.py** die de file regel voor regel inleest
en beantwoord de volgende vragen.

### Opdracht 1: extreme temperaturen

Schrijf een functie `ExtremeTemperatuur()` die de hoogste en laagste temperatuur vindt die in De Bilt is gemeten sinds het begin van de 20e eeuw. Zorg dat de functie de resultaten in een leesbaar formaat op het scherm print. Zeg dus niet: 

     Max 34.5 op 19670513

maar      

     De hoogste temperatuur ooit gemeten in de Bilt is 34.5 graden Celcius. Dat gebeurde op 13 mei 1967.

Let op: 

- maak een aparte functie `datum()` die een getal als `19670513` kan omzetten naar een goed leesbare beschrijving als `13 mei 1967`.

- geef de functie `ExtremeTemperatuur()` een inputparameter die de waarden -1 en +1 kan aannemen.   
  Zorg hierbij dat `ExtremeTemperatuur(1)` de hoogste temperatuur weergeeft op het scherm en `ExtremeTemperatuur(-1)` hetzelfde doet voor de laagste temperatuur.


### Opdracht 2: koud kouder koudst

Maak een functie `Nachtvorst()` die op zoek gaat naar de langste periode dat het aaneengesloten heeft gevroren (maximumtemperatuur onder 0◦C). Meer expliciet: hoe lang (dagen) duurde deze periode en op welke dag begon deze periode?  Zorg dat de output van je functie als volgt op het scherm wordt weergegeven:

`De langste periode dat het aaneengesloten heeft gevroren begon op <dag> <maand> <jaar> en duurde in totaal <aantal> dagen.`

Gebruik bij het weergeven van de datum ook leesbare tekst, net zoals bij opdracht 1.


### Opdracht 3: zomerse en tropische dagen

Deze We spreken van een zomerse dag als de maximumtemperatuur meer dan 25 graden Celcius was. Op een tropische dag is het in de Bilt zelfs 30 graden. Maak een grafiek waarin voor elk jaar zowel het aantal zomerse als het aantal tropische dagen weergegeven wordt.

### Opdracht 4: Eerste hittegolf

We spreken in Nederland van een hittegolf als de maximumtemperatuur ten minste vijf dagen achtereen minstens 25,0°C was (zomerse dagen) waarvan ten minste op drie dagen 30,0°C of meer (tropische dagen). Print het *eerste* jaartal uit de dataset waarin er sprake was van een hittegolf volgens deze regels.

### Nette code en nette uitvoer

Zorg dat de code van alle opdrachten in een functie of in functies staat. Gebruik geen globale variabelen (vraag indien nodig wat dit is)!

Je ziet hierboven dat je een aantal dingen moet uitprinten en één grafiek maken. Zorg dat de gevraagde informatie op losse regels wordt uitgeprint, in de juiste volgorde.
