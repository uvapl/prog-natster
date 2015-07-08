<style>
.dropcap
{
    display: block;
    float: left;
    font-size: 2em;
    line-height: 40px;
    padding: 4px 8px 0 0;
}
</style>

<span class="glyphicon glyphicon-pushpin dropcap"></span> Het doel van deze oefening is om kennis te maken met de elementen om programma's mee te schrijven. Oefen met elk van de vijf elementen, zodat je in de volgende oefening een eerste programma kunt schrijven.

<span class="glyphicon glyphicon-pushpin dropcap"></span> Oefenen doe je in deze cursus door elk voorbeeld letterlijk over te tikken. Gebruik niet de *copy-paste* functie, want dan maak je geen fouten en dan leer je veel minder. Tik dus alle voorbeelden over en verbeter ze als je een fout krijgt!

# Printen

Als je een programma hebt geschreven kun je het uitvoeren (*runnen*). De computer loopt dan stap voor stap door je programma en voert de instructies uit die op elke regel staan.

Maak tekstbestand **oef1.py** en zet er de volgende regels in:

    print "Hallo, wereld!"
    print "Hee, hallo daar."
    print "Zo tikt het lekker door."
    print "Grappig"
    print 'Hee, print dit nog?'
    print "Ivo's computer doet het vandaag niet."
    print 'Hij zei: "Hallo."'

Start nu het programma. Wat komt er uit? Voeg vervolgens ook nog de volgende regels toe:

    print 1
    print 1
    print 1 + 1
    print 1 + 1 + 1
    print 3 + 2
    print 8
    print 5 + 8 + 8 - 8
    print "5 + 8 + 8 - 8"

Je kunt dus ook rekenen. Het resultaat wordt eerst uitgerekend, en dan pas wordt er geprint. Behalve die laatste dan: daar staat de formule (*expressie*) tussen aanhalingstekens, en dan wordt het precies zo naar het scherm geprint. Net als hierboven bij de tekstjes.

Nu gaan we berekeningen en letterlijke tekstjes combineren:

    print "Het 1e getal van Fibonacci is %d" % 1
    print "Het 2e getal van Fibonacci is %d" % 1
    print "Het 3e getal van Fibonacci is %d" % (1 + 1)
    print "Het 4e getal van Fibonacci is %d" % (1 + 2)
    print "Het 5e getal van Fibonacci is %d" % (2 + 3)

<span class="glyphicon glyphicon-pushpin dropcap"></span> Prima. We kunnen nu allerlei dingen printen en uitrekenen. We kunnen ook de resultaten van een berekening op een nette manier printen, zodat de *gebruiker* van het programma begrijpt waar we mee bezig zijn.

# Commentaar

Als je in één bestand redelijk wat Python-code hebt geschreven, dan is het handig om duidelijk te maken *wat waar staat* (voor de lezer van de code zelf, niet voor de gebruiker!). Daarom kun je regels commentaar toevoegen in je programma. Die zien er zo uit:

    # Hier gaan we berekeningen en tekstjes combineren

Met zo'n hekje (`#`) laat je zien dat het geen *instructie* betreft, maar een stukje tekst waar de computer niets mee hoeft te doen.

Voeg nu commentaar toe aan je bestand **les1.py** om duidelijk te maken wat de verschillende onderdelen doen.

# Variabelen

In je programma kun je grootheden (*waarden*) opslaan onder een zelfgekozen naam. Zo kun je bijvoorbeeld het resultaat van een berekening op de ene regel ook gebruiken op een andere regel later in het programma.

Als je een getal hebt, bijvoorbeeld 20 (het aantal studenten in je groep), en dat wilt onthouden, dan schrijf je dit:

	aantal = 20

We hebben gekozen voor `aantal`, maar we hadden net zogoed kunnen kiezen voor de naam `afstand` of `dx`, of iets anders. Zorg altijd dat de naam van de variabele leesbaar is voor de gebruiker (en jezelf als je je eigen code een week later terugkijkt).

Als je de *waarde* van de variabele op het scherm wil printen dan doe je dat als volgt:

	aantal = 20
	print aantal

Omdat de computer de regels in je programma van boven naar beneden uitvoert, kun je in regel 1 een waarde opslaan onder de naam `aantal` en op regel 2 deze naam gebruiken om te printen. De computer zoekt dan op wat de waarde is van deze variabele, en print deze waarde.

De variabele kun je ook tussentijds manipuleren. Als één van de je medestudenten besluit toch maar biologie te gaan studeren dan is er 1 student minder in de groep.

	aantal = 20
    print aantal
	aantal = aantal - 1
	print aantal

Op regel 3 krijgt `aantal` een nieuwe waarde. Deze wordt berekend uit de 'oude' waarde van `aantal`.

# Conditionals

Je kan ok testen of een variabele aan een bepaalde set voorwaardes voldoet. Met behulp van het `if` statement kan je het programma iets laten doen uitsluitend in het geval er aan de voorwaardes is voldaan.

Als je wilt kijken of een getal positief is bijvoorbeeld.
	
	x = 15
	if x > 0:
		print "het getal", x, " is positief"

Om te printen of een getal een negatief is zou je een extra regel toe kunnen voegen, maar je kan de 'stroom' van het programma ook sturen als er juist niet aan de voorwaarde voldaan is. Als je bijvoorbeeld wilt testen of een getal positief of negatief is dan kan je naast de `'if` ook de `else` constructie gebruiken.

	x = 15
	if x > 0:
		print "het getal", x, " is positief"
	else
		print "het getal", x, " is negatief"

Je kan ook verschillende voorwaardes ook combineren. Als je wilt weten of een getal zich in een bepaalde range bevindt (bijvoorbeeld tussen de 3 en de 39) dan kan je met `and` verschillende condities (voorwaardes) combineren:

	x = 15
    x_min = 3
    x_max = 39	
	if x > x_min and x < x_max:
		print "het getal", x, " bevindt zich in de range"


De conditions die we hier gebruiken zijn:

- `>` 	groter dan

- `>=`	groter en gelijk aan

- `<` 	kleiner dan

- `<=`	kleiner en gelijk aan

- `==`	is precies gelijk aan

- `!=`	is niet gelijk aan


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
	print "de som van de getallen van 1 tot en met 20 is ", som 

Voordat je over de getallen 'loopt' zet je de variabele som op 0. Vervolgens tel je bij elke stap (elk getal) de waarde van het getal op bij de variabele som en verhoog je getal met 1. Nadat je alle getallen hebt doorlopen laat je de computer op het scherm printen wat de waarde van de variabele som is.

Je kan de getallen natuurlijk ook verschillend behandelen. Als we bijvoorbeeld de som van de even getallen tussen de 1 en de 20 willen printen kunnen we het `if` statement gebruiken

    som = 0
	for getal in range(1,21):
        if getal%2 == 0:
           som = som + getal
	print "de som van de even getallen van 1 tot en met 20 is ", som 

In dit geval test je voor elk van de getallen eerst of het een even getal is (is de rest 0 als je door 2 deelt). Als dat zo is tel je het getal op bij de variabele som. Aan het eind van de loop print je de waarde weer op het scherm.

Je kan binnen een `if statement` ook verschillende dingen doen. Als je ook elk even getal op het scherm wilt zien dan kan je binnen het if statement ook verschillende handelingen uitvoeren. Hier is weer duidelijk dat indentatie cruciaal is. Alles wat onder elkaar staat hoort bij elkaar.

    som = 0
	for getal in range(1,21):
        if getal%2 == 0:
           print "Yes!", getal, " is een even getal"
           som = som + getal
	print "de som van de even getallen van 1 tot en met 20 is ", som 



# Lijsten

Naast getallen en strings zijn lijsten ook een basiselementen bij veel programmeertalen.  Dit is handig om data te groeperen en als 1 object te behandelen.

Een lijstje met namen van docenten kan je bijvoorbeeld zo bewaren:
	L_docenten = ["Martijn", "Rico", "Nick", "Rick", "Kelly"]

Elk element in deze lijst is een string, maar de lijst kan zowel getallen, strings en zelf weer lijsten bevatten. Ook door elkaar heen. Je kan elementen uit een lijst opvragen, ze veranderen of elementen toevoegen. 

Tip:
   - elementen in een lijst beginnen bij 0
   - gebruik je keuze van je variabelenaam om aan te geven of iets een lijst is of gewoon een getal.
     ik heb hier L_ gebruikt zodat ik zelf weet dat het een lijst is. Kies wat je zelf handig vindt.
	 
Stel dat je een lijst met 5 temperatuurmetingen hebt (op het Science Park) en die wil je in een lijst opslaan en vervolgens wilt printen op het scherm dan gaat dat als volgt:

	L_temp = [12.7, 18.8, 24.9, 14.5, 19.0]
    print L_temp
	
Als je nu een zesde meting doet (20.5 graden) en die toe wilt voegen dan kan dat met behulp van het `append` commando

	L_temp = [12.7, 18.8, 24.9, 14.5, 19.0]
    L_temp.append(20.5)
    print L_temp

In plaats van de lijst zelf printen kunnen we ook de individuele elementen van de lijst printen of het aantal elementen in de lijst berekenen.

	L_temp = [12.7, 18.8, 24.9, 14.5, 19.0]
    L_temp.append(20.5)
    print "Het eerste element van de lijst = ", L_temp[0]
    print "Het aantal elementen in de lijst is ", len(L_temp)

Je kunnen we ook over een voor een de elementen in de lijst bekijken met behulp van de for loop:

	L_temp = [12.7, 18.8, 24.9, 14.5, 19.0]
    L_temp.append(20.5)
    for i in range(0,len(L_temp)):
	   print "meting ", i, " was ", L_temp[i], " graden" 

Hierbij loopt het getal (index) i van 0 tot het aantal elementen in de lijst en kan je de index gebruiken om het ie element in de lijst te printen. 

En daarmee kan je ook het gemiddelde bepalen:

	L_temp = [12.7, 18.8, 24.9, 14.5, 19.0]
    L_temp.append(20.5)
    som_temp = 0
    for i in range(0,len(L_temp)):
	   print "meting ", i, " was ", L_temp[i], " graden" 
       som_temp = som_temp + L_temp[i]
    gemiddelde_temp	= som_temp / len(L_temp)
	print "De gemiddelde temperatuur was ", gemiddelde_temp, " graden"

Of kijken op hoeveel dagen de temperatuur boven de 20 graden uitkwam

	L_temp = [12.7, 18.8, 24.9, 14.5, 19.0]
    L_temp.append(20.5)
    hete_dagen = 0
    for i in range(0,len(L_temp)):
       if L_temp[i] > 20 :
     	  hete_dagen = hete_dagen + 1
		  
    print "Op ", hete_dagen, " was de temperatuur boven de 20 graden"
		
Van lijsten is het belangrijk dat je weet hoe je een lijst definiert, hoe je elementen toevoegt aan een lijst en hoe je de individuele elementen afzonderlijk lukt bekijken.
