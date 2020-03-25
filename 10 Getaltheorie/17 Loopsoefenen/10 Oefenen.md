# Oefenen oefenen oefenen

Een belangrijk element in deze eerste module is het zoeken naar priemgetallen. We zullen dan voor elk getal moeten evalueren of het nou wel of niet deelbaar is door een van de getallen die kleiner zijn dan het getal zelf. Hoewel jullie in net wat gelezen hebben over algoritmen, voorwaardelijke instructies en loops is het goed om hier nog wat extra te oefenen voordat jullie in het diepe duiken. Vooral met het gebruik van loops. Het is belangrijk om die goed te begrijpen omdat die in de rest van deze cursus en in vrijwel elk Python programma een belangrijke rol spelen.  

We lopen een paar basis-voorbeelden langs en vragen jullie bij elke stap om ook zelf een programmaatje te schrijven. Dit is allemaal voorbereiding voor het zeken naar priegetallen. Het is ook handig om naar deze pagina terug te keren als je ergens in de cursus tegen een for-loop aanloopt die je niet goed begrijpt.

Maak een bestand loopsoefenen.py en implementeer daarin een paar van de onderstaande voorbeelden en de opdrachten.

## 1. Loops - de basis 

We gaan eerst aan de slag met een aantal basis-elementen. 

#### De basis 

Een loop gebruik je als je een set instructies wilt herhalen voor een aantal verschillende waardes van een variabele. Als je bijvoorbeeld op het scherm de waardes van de getallen 1 tot en met 10 wilt printen kan je dat met tien afzonderlijke print statements doen, maar ook als volgt:

    for x in range(1, 11):
        print("x heeft nu de waarde ",x)
    
Dit programma heeft namelijk als output

    x heeft nu de waarde 1
    x heeft nu de waarde 2
    x heeft nu de waarde 3
    ...
    x heeft nu de waarde 10

Het programma verandert steeds de waarde die de variabele x heeft. Het loop begint door de waarde van x op 1 te zetten en gaat vervolgens *alle* instructies uitvoeren die in de loop staan. Daarna wordt aan x de waarde 2 toegekend en worden opnieuw alle instructies uitgevoerd. Op dit moment is er maar een enkele instructie, namelijk: print de waarde van het getal, maar dat kunnen we natuurlijk uitbreiden.

#### Meer instructies, variabelen manipuleren en het eind van de loop

Je kunt meer instructies laten uitvoeren voor elke waarde die de variabele aanneemt. We kunnen het getal ook telkens optellen bij een variabele die we aan het begin van het programma op nul hebben gezet. Aan het eind van dat programma bevat die variabele dan de som van alle getallen van 1 tot en met 10.

Zodra alle instructies zijn uitgevoerd voor de hoogste waarde die x kan aannemen is de loop 'afgelopen' en gaat het programma gewoon verder. In dit geval laten we het programma de som van alle getallen printen op het scherm. Let ook goed op de indentatie van de laatste regel. 

    som = 0 
    for x in range(1, 11):
        print("x heeft nu de waarde ",x)
        som = som + x

    print("De som van de getallen van ", 1, " tot en met ", 10 = ", som)

**opdracht 1:** Pas bovenstaand programma eens aan door het paatste print-statement verder in te laten sprintenm tot het precies onder de regel 'som = som + x' staat. Run het programma en probeer te begrijpen wat er gebeurt. Dit is een veelgemaakte fout met loops dus belangrijk om dit goed te begrijpen.

**opdracht 2:** Op dit moment gaat het om de getallen van 1 tot en met 10. Probeer bovenstaand programma om te schrijven door op één plek bovenin het programma dit maximale getal te definiëren.

### Loops - basis, tellers en conditionals

Je kunt natuurlijk binnen loops ook gebruikmaken van conditionals. Als je bijvoorbeeld de loop wilt laten lopen van 1 tot en met 10 en alleen de getallen groter dan 15 en de getallen die deelbaar zijn door 3 wilt printen dan kan je dat als volgt doen?

    for x in range(1, 20):
        if x > 15:
		   print("Dit getal is groter dan 15, namelijk ", x)
        if x%3:
		   print("Dit getal is precies deelbaar door 3, -> ", x)

**opdracht 3:** Pas bovenstaand programma zo aan dat aan het eind van het programma op het scherm geprint wordt hoeveel getallen er precies deelbaar waren door 3. Je zult hiervoor een zogemaande 'teler' bij moeten houden. Een variabele die steeds met 1 opgehoogd wordt zodra je een 'goede' gevonden hebt. Doe de outpue netjes, dus laat je programma als output geven:

    Van de getallen 1 tot en met 20 zijn er precies xxx deelbaar door 3.
	
## 2. Loops in loops

Het is ook mogelijk om loops in loops te maken. In het Engels worden dit 'nested loops' genoemd.

    for x in range(1, 6):
       for y in range(1, 4):
           print("x  = ", x, " en  y = ", y)
		   
Dit programma heeft als output

    x = 1, y = 1 
    x = 1, y = 2 
    x = 1, y = 3 
    x = 2, y = 1 
    ...
    x = 6, y = 3 
    x = 6, y = 4 


**opdracht 4:** Pas bovenstaand programma zo aan dat de printregel alleen geprint wordt als x+y groter is dan 6.

**opdracht 5:** Pas bovenstaand programma zo aan dat y (automatisch) loopt van 1 tot en met de waarde van x.



## Probleemanalyse

Dit programma voldoet aan het cliché van een standaard computerprogramma: het heeft *invoer*, *berekeningen*, en *uitvoer*. Probeer die drie onderdelen ook terug te laten komen in je code!

