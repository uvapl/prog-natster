# Loops
Een belangrijk element in deze eerste module is een stukje code dat kan bepalen of een getal een priemgetal is of niet. Om dat te doen  zullen we voor elk getal moeten evalueren of het nou wel of niet deelbaar is door een getal dat kleiner is dan het getal zelf. Hoewel we net wat geleerd hebben over algoritmen, voorwaardelijke instructies is het belangrijk om nóg een concept te behandelen en daarmee te oefenen voor we in het diepe duiken en met de priemgetallen aan de slag gaan. 

Het is belangrijk om het concept van loops goed te begrijpen omdat die in de rest van deze cursus, en in vrijwel elk Python programma, een belangrijke rol spelen. We lopen hieronder een paar basis-constructies langs en zullen bij elke stap ook zelf kleine aanpassingen maken om te oefenen met de loops. Hoewel we hier vooral for-loops zullen bekijken is het ook belangrijk om met de while-loop aan de slag te gaan. Mede daarom ook een paar opdrachten om daarmee te oefenen. 

Maak een bestand loopsoefenen.py en implementeer daarin een paar van de onderstaande voorbeelden en de opdrachten.

## 1. Loops - de basis 

Het komt heel vaak voor dat je een set van instructies een groot aantal keer uit wilt voeren.

#### De basis - loops in Python

Een for-loop gebruik je als je een set instructies wilt herhalen voor een aantal verschillende waardes van een variabele. Als je bijvoorbeeld op het scherm de waardes van de getallen 1 tot en met 10 wilt printen kan je dat met tien afzonderlijke print statements doen, maar ook als volgt:

    for x in range(1, 11):
        print("x heeft nu de waarde ",x)
    
Dit programma heeft namelijk als output

    x heeft nu de waarde 1
    x heeft nu de waarde 2
    x heeft nu de waarde 3
    ...
    x heeft nu de waarde 10

Het programma verandert steeds de waarde die de variabele x heeft. Het loop begint door de waarde van x op 1 te zetten en gaat vervolgens *alle* instructies uitvoeren die in de loop staan. Daarna wordt aan x de waarde 2 toegekend en worden opnieuw alle instructies uitgevoerd. Op dit moment is er maar een enkele instructie, namelijk: print de waarde van het getal, maar dat kunnen we natuurlijk uitbreiden.


![](Loopsuitleg.png){: style="width:75%"}


Er zijn een paar dingen on te onthouden:

   - **Let op:** dat Python telt *tot* het eindgetal in de functie range(): range(1,11) loopt dus van 1 *tot en met* 10. Dit is een veelgemaakte fout als je begint te programmeren in Python. Het voelt onlogisch, maar that's just the way it is.
   - Je kunt met range ook de stapgrootte opgeven. Standaard neemt hij stapjes van 1, maar als je stapjes van 10 wilt nemen gebruik je de volgende syntax: for x in range (1,100, 10). Probeer dit zelf eens uit zodat je goed weet welke waarde x aanneemt.



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

**opdracht 3:** Maak een programma dat dezelfde werking heeft, maar gebruik nu de while-loop in plaats van de for-loop. 

**opdracht 4:** Gebruik een while-loop om te zorgen dat het programma getallen blijft printen (ook tot boven de 10) tot de som van de getallen groter is dan 123.


### Loops - basis, tellers en conditionals

Je kunt natuurlijk binnen loops ook gebruikmaken van conditionals. Als je bijvoorbeeld de loop wilt laten lopen van 1 tot en met 10 en alleen de getallen groter dan 15 en de getallen die deelbaar zijn door 3 wilt printen dan kan je dat als volgt doen?

    for x in range(1, 20):
        if x > 15:
		   print("Dit getal is groter dan 15, namelijk ", x)
        if x%3:
		   print("Dit getal is precies deelbaar door 3, -> ", x)

**opdracht 5:** Pas bovenstaand programma zo aan dat aan het eind van het programma op het scherm geprint wordt hoeveel getallen er precies deelbaar waren door 3. Je zult hiervoor een zogemaande 'teler' bij moeten houden. Een variabele die steeds met 1 opgehoogd wordt zodra je een 'goede' gevonden hebt. Doe de output netjes, dus laat je programma als printstatement weergeven:

    Van de getallen 1 tot en met 20 zijn er precies xxx deelbaar door 3.
	
	
	
#### Twee soorten loops: for-loops en while-loops

Er zijn in Python, net als in bijna elke programmeertaal, twee standaard constructies om te 'loopen': de **for-loop** en de **while-loop**. 

Een for-loop gebruik je als je precies weet hoe vaak je een instructie uit wilt/moet voeren. In gevallen waar je dat niet weet en steeds bij elke stapt wilt kunnen besluiten of je nog verder wilt tellen gebruik je een while-loop. In de uitleg hieronder wordt daar ook iets meer over gezegd.

In feite zijn `for` en `while` ook uitwisselbaar. Deze for-loop 

	    for i in range(100):
	        print("hi")

is gelijk aan de volgende `while`-loop:

	    i = 0
	    while i < 100:
	        print("hi")
	        i = i + 1

De `for`-loop is duidelijk wat compacter en zo sneller leesbaar. Dat is dus ook de loop die het meest gebruikt wordt. Maar toepassingen zoals gebruikersinvoer kun je eigenlijk alleen maar met een `while`-loop schrijven, dus deze heeft ook z'n nut.
	
	
#### Video van basiselementen in loops	

Een korte uitleg van een paar van de basis-elementen van loops kun je ook in de vier onderstaande filmpjes bekijken. 

![embed](https://vimeo.com/album/5380755/embed)
	
	
## 2. Loops in loops

In de bovenstaande voorbeelden verandert steeds de waarde van een enkele variabele, in dit geval x, en wordt er naast printen en dingen bewaren niet veel complex gedaan. Dat is niet altijd het geval. Loops worden vaak gebruik als onderdeel van ingewikkelder constructies. 

#### Loops in loops

Het is ook mogelijk om loops in loops te maken. In het Engels worden dit 'nested loops' genoemd. Als je voor elke waarde van x bijvoorbeeld een andere variabele wilt laten variëren van 1 tot en met 3 (denk hierbij bijvoorbeeld dat x het studentnummer is en y de cijfers voor drie verschillende opdrachten tijdens een tentamen), dan gebruiken we de volgende constructie. 

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


**opdracht 6:** Pas bovenstaand programma zo aan dat de printregel alleen geprint wordt als x+y groter is dan 6.

**opdracht 7:** Pas het bovenstaande programma zo aan dat vlak voor er een nieuwe waarde aan x wordt toegekend, dus net nadat de loop over y klaar is, op het scherm geprint wordt: 'x = <xxx> en we zijn net klaar met de loop over y'.  
	
**opdracht 8:** Pas bovenstaand programma zo aan dat y niet van 1 tot 4 loopt, maar van 1 tot en met de waarde van x. 

**opdracht 9:** Pas bovenstaand programma zo aan dat y niet van 1 tot 4 loopt, maar van 1 tot en met de waarde van x. Gebruik nu de while-constructie voor de waardes van y.


## Oefenen en debuggen

Omdat in vrijwel elk programma dat we zullen schrijven in deze cursus zullen loops voorkomen is het belangrijk dat je deze techniek goed onder de knie hebt. Deze pagina is ook handig om naar terug te keren als je ergens in de cursus een for-loop tegenkomt die je niet goed begrijpt. 

