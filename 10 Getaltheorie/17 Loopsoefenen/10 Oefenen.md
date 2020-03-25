# Oefenen oefenen oefenen

Een belangrijk element in deze eerste module is het zoeken naar priemgetallen. We zullen dan voor elk getal moeten evalueren of het nou wel of niet deelbaar is door een van de getallen die kleiner zijn dan het getal zelf. Hoewel jullie in net wat gelezen hebben over algoritmen, voorwaardelijke instructies en loops is het goed om hier nog wat extra te oefenen voordat jullie in het diepe duiken. Vooral met het gebruik van loops. Het is belangrijk om die goed te begrijpen omdat die in de rest van deze cursus en in vrijwel elk Python programma een belangrijke rol spelen.  

We lopen een paar basis-voorbeelden langs en vragen jullie bij elke stap om ook zelf een programmaatje te schrijven. Dit is allemaal voorbereiding voor het zeken naar priegetallen. Het is ook handig om naar deze pagina terug te keren als je ergens in de cursus tegen een for-loop aanloopt die je niet goed begrijpt.

Maak een bestand loopsoefenen.py en implementeer daarin een paar van de onderstaannde voorbeelden.

### Loops - basis 

Maak een bestand `rekenwonder.py` en implementeer een programma dat de gebruiker vraagt om twee gehele getallen, waarna het product van de getallen met `print` op het scherm wordt getoond.

    for x in range(1, 11):
        print("x heeft nu de waarde ",x)
    
Dit programma heeft als output
        x heeft nu de waarde 1
        x heeft nu de waarde 2
        x heeft nu de waarde 3
        ...
        x heeft nu de waarde 10

Het programma verandert steeds de waarde in de variabele x. Hij begint door de waarde van x op 1 te zetten en gaat vervolgens *alle* instructies uitvoeren die in de loop staan. Daarna wordt aan x de waarde 2 toegekend en worden opnieuw alle instructies uitgevoerd. Op dit moment is er maar een enkele instructie, namelijk: print de waarde van het getal.

### Loops - basis,  meer instructies, variabelen manipuleren en het eind van de loop

Je kunt natuurlijk meer instructies laten uitvoeren. Naast het printen van het getal kunnen we het ook optellen bij een variabele 'som' die we helemaal aan het begin van het programma op nul hebben gezet. Zodra alle instructies zijn uitgevoerd voor de hoogste waarde die x kan aannemen gaat het programma gewoon verder. In dit geval met het printen van de laatste regel waarin we de som van de getallen 

    som = 0 
    for x in range(1, 11):
        print("x heeft nu de waarde ",x)
        som = som + x

    print("De som van de getallen van ", 1, " tot en met ", 10 = ", som)

**opdracht 1:** Op dit moment gaat het om de getallen van 1 tot en met 10. Probeer bovenstaand programma om te schrijven door op één plek bovenin het programma dit maximale getal te definiëren.

### Loops - basis, tellers en conditionals

Je kunt natuurlijk binnen loops ook gebruikmaken van conditionals. Als je bijvoorbeeld de loop wilt laten lopen van 1 tot en met 10 en alleen de getallen groter dan 15 en de getallen die deelbaar zijn door 3 wilt printen dan kan je dat als volgt doen?

    for x in range(1, 20):
        if x > 15:
		   print("Dit getal is groter dan 15, namelijk ", x)
        if x%3:
		   print("Dit getal is precies deelbaar door 3, -> ", x)

**opdracht 2:** Pas bovenstaand programma zo aan dat aan het eind van het programma op het scherm geprint wordt hoeveel getallen er precies deelbaar waren door 3. Je zult hiervoor een zogemaande 'teler' bij moeten houden. Een variabele die steeds met 1 opgehoogd qordt zodra je een 'goede' gevonden hebt. Doe de outpue netjes, dus laat je programma als output geven:

    Van de getallen 1 tot en met 20 zijn er precies xxx deelbaar door 3
	

### Loops - loops in loops

Het is ook mogelijk om loops in loops te maken. In het Engels worden dit 'nested loops' genoemd.

    for x in range(1, 6):
       for y in range(1, 3):
           print("x  = ", x, " en  y = ", y)
		   

Dit programma





## Probleemanalyse

Dit programma voldoet aan het cliché van een standaard computerprogramma: het heeft *invoer*, *berekeningen*, en *uitvoer*. Probeer die drie onderdelen ook terug te laten komen in je code!

## Hints

* Je kunt dit programma schrijven met alleen de Python-onderdelen die je tot nu toe hebt geleerd!

* Maak gebruik van de `input`-functie en gebruik `int()` om de invoer van de gebruiker om te zetten van een string naar een integer, zodat je de berekening kunt uitvoeren.

## Testen

Loop eerst je eigen programma na: werkt dit voor alle normale invoer? Start het programma door het volgende in te tikken in de terminal:

	python rekenwonder.py

Probeer dan de voorbeelden bovenaan de opgave uit. Lijkt alles te werken, dan is het tijd om `checkpy` erbij te pakken. Testen gaat net zo als bij `hello`, alleen roep je nu de test voor `rekenwonder` aan. Zo dus:

	checkpy rekenwonder

Zie je unhappy smileys, en kom je er niet uit wat er fout gaat? Vraag om hulp!
