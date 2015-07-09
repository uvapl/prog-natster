> Het doel van deze oefening is om kennis te maken met de elementen om programma's mee te schrijven. Oefen met elk van de vijf elementen, zodat je in de volgende oefening een eerste programma kunt schrijven.

# Printen

Als je een programma hebt geschreven kun je het uitvoeren (*runnen*). De computer loopt dan stap voor stap door je programma en voert de instructies uit die op elke regel staan.

Maak tekstbestand **les1.py** en zet er de volgende regels in:

    print "Hallo, wereld!"
    print "Hee, hallo daar."
    print "Zo tikt het lekker door."
    print "Grappig"
    print 'Hee, print dit nog?'
    print "Ivo's computer doet het vandaag niet."
    print 'Hij zei: "Hallo."'

> Oefenen doe je in deze cursus door elk voorbeeld letterlijk over te tikken. Gebruik niet de *copy-paste* functie, want dan maak je geen fouten en dan leer je veel minder. Tik dus alle voorbeelden over en verbeter ze als je een fout krijgt!

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

Als je dit programma uitvoert, dan zie je dat precies waar `%d` stond, nu de uitkomst van de berekening is geplaatst.

> Prima. We kunnen nu allerlei dingen printen en uitrekenen. We kunnen ook de resultaten van een berekening op een nette manier printen, zodat de *gebruiker* van het programma begrijpt waar we mee bezig zijn.

