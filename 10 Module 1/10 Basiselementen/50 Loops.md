# Loops

Soms is het handig om van een groot aantal getallen of lijsten van variabelen te bepalen of ze aan een bepaalde eis voldoen. Omdat dat nou precies is wat een computer zo goed kan is het een basiselement in bijna alle programmeertalen: `for loops`. Dit is een constructie waarbij een variabele een bepaalde beginwaarde toegewezen krijgt gevolgd door een set instructies. Zodra alle constructies uitgevoerd zijn wordt de variabele met 1 vergroot en worden weer alle constructies uitgevoerd. We zullen deze constructie veel tegenkomen in de cursus. Hier behandelen we de basis stap: de lijst met getallen.

Als we voor de getallen 1 tot 10 iets willen doen dan ziet de constructie er zo uit 

	for getal in range(1,10):
    	[doe hier alle handelingen]

We gebruiken hier het commando `range()` dat een begingetal en eindgetal. Let op, het is tot het eindgetal en niet tot en met. Aan het begin wordt de variabele `getal` op 1 gezet en worden de handelingen uitgevoerd die in het programma beschreven staan. Als alle handelingen uitgevoerd zijn gaat het programma terug naar de eerste regel en zet nu de variabelenaam `getal` op 2 en worden weer alle handelingen uitgevoerd. Etc etc.

Stel dat we bijvoorbeeld de getallen van 1 tot en met 10 op het scherm willen printen en vervolgens aan willen geven dat we klaar zijn dan werkt dat als volgt:

	for getal in range(1,11):
    	print getal
	print "Ik ben klaar" 
		
In plaats van op het scherm printen kan je nu ook met behulp van de conditionals samengestelde constructies maken.

Als je de som van alle getallen van 1 tot en met 20 wilt uitrekenen en vervolgens op het scherm wilt printen werkt dat als volgt:

    som = 0
	for getal in range(1,21):
    	som = som + getal
	print "de som van de getallen van 1 tot en met 20 is %d" % (som) 

Voordat je over de getallen 'loopt' zet je de variabele som op 0. Vervolgens tel je bij elke stap (elk getal) de waarde van het getal op bij de variabele som en verhoog je getal met 1. Nadat je alle getallen hebt doorlopen laat je de computer op het scherm printen wat de waarde van de variabele som is.

Je kan de getallen natuurlijk ook verschillend behandelen. Als we bijvoorbeeld de som van de even getallen tussen de 1 en de 20 willen printen kunnen we het `if` statement gebruiken

    som = 0
	for getal in range(1,21):
        if getal%2 == 0:
           som = som + getal
	print "de som van de even getallen van 1 tot en met 20 is %d" % (som)

In dit geval test je voor elk van de getallen eerst of het een even getal is (is de rest 0 als je door 2 deelt). Als dat zo is tel je het getal op bij de variabele som. Aan het eind van de loop print je de waarde weer op het scherm.

Je kan binnen een `if statement` ook verschillende dingen doen. Als je ook elk even getal op het scherm wilt zien dan kan je binnen het if statement ook verschillende handelingen uitvoeren. Hier is weer duidelijk dat indentatie in Python cruciaal is. Alles wat onder elkaar staat hoort bij elkaar.

    som = 0
	for getal in range(1,21):
        if getal%2 == 0:
           print "Yes!", getal, " is een even getal"
           som = som + getal
	print "de som van de even getallen van 1 tot en met 20 is %d" % (som)


Dit stukje code rekent heel specifiek de som van de even getallen van 1 tot en met 20 uit. Als je nu gevraagd wordt om de even getallen tussen 1 tot en met 88 bij elkaar op te tellen moet je op 2 plekken in de code een aanpassing maken (zie je welke ?). Bij een klein stukje code gaat dat nog wel, maar bij grotere problemen is dat al snel niet meer te overzien. 

Zorg daarom dat je, nadat je het specifieke probleem hebt opgelost, je code altijd zo 'universeel' mogelijk maakt. Het onderstaand stukje code rekent de som uit van de even getallen van 1 tot en met max_getal. Die variabele hoef je dus alleen in het begin van je code een waarde te geven (20, 138613 of in dit geval 88) en verder werkt je in je programma alleen met de naam van de variabele. Op elke plek in de code weet het programma namelijk wat de waarde van die variabele is.

    som = 0
    max_getal = 88
	for getal in range(1,max_getal+1):
        if getal%2 == 0:
           print "Yes!", getal, " is een even getal"
           som = som + getal
	print "de som van de even getallen van 1 tot en met %d is %d" % (max_getal, som)

Je kunt in `range` ook de stapgrootte opgeven. `for` telt dan van begin tot einde, rekening houdend met de stapgrootte. Dit ziet er zo uit:

    for getal in range(1,100,10):
       ...

Elke stap in de `for`-loop zal dan steeds 10 verder zijn dan de vorige. Denk even na welke stappen gemaakt zouden worden bij de loop hierboven!

## Oefening

Schrijf nu zelf een stukje code met `for`-loop die de som van de oneven getallen van 1 tot en met 20 uitrekent. Sla dit programmaatje apart op, in een bestand genaamd `oneven.py`. Gebruik de stapgrootte van `range`!
