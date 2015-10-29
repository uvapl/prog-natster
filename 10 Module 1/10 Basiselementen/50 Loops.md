# Loops

Soms is het handig om van een groot aantal getallen of lijsten van variabelen te bepalen of ze aan een bepaalde eis voldoen. Omdat dat nou precies is wat een computer zo goed kan is het een basiselement in bijna alle programmeertalen: `for`-loops. Dit is een constructie waarbij een variabele een bepaalde beginwaarde toegewezen krijgt gevolgd door een set instructies. Zodra alle instructies uitgevoerd zijn, wordt de variabele met 1 vergroot en worden weer alle instructies uitgevoerd.

## De basis van loops

Als we voor de getallen 1 *tot* 10 iets willen doen dan ziet het er zo uit:

	for getal in range(1,10):
        actie1
        actie2
        actie3

Je ziet dat we net als bij `if` weer kunnen inspringen om duidelijk te maken welke volgende regels in de loop horen. Dat zijn dus de instructies die meerdere malen uitgevoerd gaan worden.

## De loop-variabele

Deze loop werkt met een *variabele* genaamd `getal` om voor elke iteratie (elke keer dat de loop uitgevoerd wordt) een andere waarde vast te houden. We gebruiken hier het commando `range()` met een begingetal en eindgetal om aan te geven hoe de variabele zal tellen. Daarbij telt Python van het begin *tot* het einde---dus niet *tot en met*!

In bovenstaand voorbeeld zal de variabele `getal` als eerste op 1 gezet worden en daarna worden de handelingen uitgevoerd die in het programma beschreven staan. Als alle handelingen uitgevoerd zijn gaat het programma terug naar de beginregel van de loop en zet nu de variabele `getal` op 2 en worden weer alle handelingen uitgevoerd. In de code binnen de loop kun je dus naar de variabele `getal` verwijzen om mee te rekenen of om iets uit te printen.

![embed](https://player.vimeo.com/video/137628513)

## Voorbeelden

Stel dat we bijvoorbeeld de getallen van 1 tot en met 10 op het scherm willen printen en dan aangeven dat we klaar zijn:

	for getal in range(1,11):
    	print getal
	print "Ik ben klaar" 
		
Als je de som van alle getallen van 1 tot en met 20 wil uitrekenen en vervolgens op het scherm wilt printen werkt dat als volgt:

    som = 0
	for getal in range(1,21):
    	som = som + getal
	print "de som van de getallen van 1 tot en met 20 is %d" % (som) 

Voordat je over de getallen 'loopt' zet je de variabele `som` op 0. Die gebruiken we om tijdens de loop het totaal bij te houden: we tellen bij elke stap (dus bij elk `getal`) de waarde van `getal` op bij de variabele `som`. Nadat we alle getallen hebben doorlopen laat de computer op het scherm zien wat de waarde van de variabele `som` is. Dat hebben we gedaan met de `print`-opdracht, die zoals je ziet niet in de loop staat.

## Een loop met een if

Je kunt tijdens de loop de getallen ook verschillend behandelen. Als we bijvoorbeeld de som van de even 
getallen tussen 1 en 20 willen printen kunnen we een `if`-statement gebruiken. 

We introduceren in het onderstaande stukje code ook 'ongemerkt' de `%` (modulo-operator) om te bepalen 
of een getal deelbaar een veelvoud is van 2. De modulo operator is werkt als volgt: `x%y` geeft je de 
rest van de deling als je het getal y door x hebt gedeeld. Het statement 7%2 geeft je dus 1, 35%8 = 3 
etc. Zo'n bouwsteen als de modulo operator kan je ook prima inzetten om te kijken of een getal een 
veelvoud is van een ander getal. Als 679875%37 nou precies gelijk is aan 0 betekent dat dat 679875 
een veelvoud is van 37 en in het onderstaande stukje code gebruiken we het om te kijken of een getal 
een veelvoud is van 2 en dus een even getal is.

Het printen van de som van de *even* getallen tussen 1 en 20 gaat dan ook als volgt:

    som = 0
	for getal in range(1,21):
        if getal % 2 == 0:
           som = som + getal
	print "De som van de even getallen van 1 tot en met 20 is %d" % (som)

In dit geval test je voor elk van de getallen eerst of het een even getal is (rest 0 
als je door 2 deelt). Als dat zo is tel je het getal op bij de variabele som. Aan het 
eind van de loop print je de waarde weer op het scherm. Alle oneven getallen worden 
helemaal genegeerd!

### Let op:

We gebruiken het `==` (dubbele =-teken) om te kijken of 2 getallen aan elkaar gelijk zijn. Het antwoord daarop 
is 'ja' of 'nee'. Een veelvoorkomende fout in programma's is dat hier een enkele `=` gebruikt wordt. 

Het volgende voorbeeld laat zien dat indentatie in Python cruciaal is. Alles wat recht 
onder elkaar staat hoort bij elkaar:

    som = 0
	for getal in range(1, 21):
        if getal % 2 == 0:
           print "Yes! %d is een even getal" % getal
           som = som + getal
	print "de som van de even getallen van 1 tot en met 20 is %d" % (som)

Dit stukje code rekent heel specifiek de som van de even getallen van 1 tot en met 20 uit. Als je nu gevraagd wordt om de even getallen tussen 1 tot en met 88 bij elkaar op te tellen moet je op 2 plekken in de code een aanpassing maken. Probeer dat maar. Bij een klein stukje code gaat dat nog wel, maar bij grotere problemen is dat al snel niet meer te overzien. 

## Een algemene oplossing maken

Zorg daarom dat je, nadat je het specifieke probleem hebt opgelost, je code altijd zo 'universeel' mogelijk maakt. Het onderstaand stukje code rekent de som uit van de even getallen van 1 tot en met `max_getal`. Die variabele hoef je dus alleen in het begin van je code een waarde te geven (20, 138613 of in dit geval 88) en verder werkt je in je programma alleen met de naam van de variabele. Op elke plek in de code weet het programma namelijk wat de waarde van die variabele is.

    som = 0
    max_getal = 88
	for getal in range(1,max_getal+1):
        if getal%2 == 0:
           print "Yes! %d is een even getal" % getal
           som = som + getal
	print "de som van de even getallen van 1 tot en met %d is %d" % (max_getal, som)

## Stapgrootte van een loop

Je kunt in `range` ook de stapgrootte opgeven. `for` telt dan van begin tot einde, rekening houdend met de stapgrootte. Dit ziet er zo uit:

    for getal in range(1,100,10):
       ...

Elke stap in de `for`-loop zal dan steeds 10 verder zijn dan de vorige. Denk even na welke stappen gemaakt zouden worden bij de loop hierboven!

## Opdracht

Schrijf nu zelf een stukje code met `for`-loop die de som van de oneven getallen van 1 tot en met 20 uitrekent. Sla dit programmaatje apart op, in een bestand genaamd **oneven.py**. Gebruik de stapgrootte van `range` om alleen de oneven getallen te genereren, zodat het programma efficiënt werkt. Vergeet niet om commentaar toe te voegen!
