# Lijsten

Lijsten in Python zijn handig om data te groeperen en vervolgens als geheel te verwerken. Zo kun je berekeningen niet alleen maar op bijvoorbeeld losse getallen toepassen (is dit een priemgetal?) maar ook op hele verzamelingen.

## Lijsten maken

Een lijstje met namen van docenten kun je zo bewaren:

	docenten = ["Martijn", "Ivo", "David", "Florian", "Olmo", "Dominique", "Maarten"]

Elk element in deze lijst is een *string*, maar zo'n lijst kan ook getallen of zelfs andere lijsten bevatten. Ook door elkaar heen. Elk element heeft een *positie*; daarmee kun je een element uit een lijst opvragen:

    print docenten[2]

Probeer dit uit, want het antwoord is misschien niet precies wat je verwacht. Probeer daarom ook even het getal `2` te veranderen in andere getallen.

## Elementen toevoegen

Als je een lijst hebt met 5 temperatuurmetingen van het Science Park, dan kun je die als volgt definiëren en uitprinten:

	metingen_science_park = [12.7, 18.8, 24.9, 14.5, 19.0]
    print metingen_science_park

We printen hier de hele lijst in één keer uit, in plaats van een enkel element. Als je nu een zesde meting doet (20,5 graad) kun je die toevoegen met behulp van de `append`-instructie:

    metingen_science_park.append(20.5)
    print metingen_science_park

In plaats van de lijst printen kunnen we ook de individuele elementen van de lijst printen of het aantal elementen in de lijst berekenen.

    print "Het eerste element van de lijst is %d" % metingen_science_park[0]
    print "Het aantal elementen in de lijst is %d" % len(metingen_science_park)

Nu kunnen we dus in ieder geval de hele lijst gebruiken, en invididuele elementen uitprinten.

## Loopen met een lijst

Om nu de gegevens in een lijst te verwerken, moeten we vaak ieder element van de lijst individueel bekijken. Daarvoor kunnen we de `for`-loop gebruiken:

	metingen_science_park = [12.7, 18.8, 24.9, 14.5, 19.0]
    metingen_science_park.append(20.5)
    for meting in metingen_science_park:
	    print "de meting was %d graden" % meting

Probeer de code zeker even uit, zodat je goed ziet wat de uitvoer is. Let op dat de `for`-loop nu niet meer gebruik maakt van `range`.

> Zoals je ziet in bovenstaande voorbeeld zal het programma het gemiddelde afronden. `%d` zegt namelijk dat je een geheel getal op het scherm wilt printen. Als je een reëel getal wilt printen moet je `%f` gebruiken. Naar deze *formats* kijken we later in de cursus nog verder.

In dit geval is het wel informatief om neer te zetten over *welke* meting het gaat als we een waarde uitprinten. Om dat te doen, kunnen we zelf een teller bijhouden:

    teller = 0
    for meting in metingen_science_park:
        teller = teller + 1
        print "de %d e meting was %d graden" % (teller, meting)

Met behulp van al deze informatie kunnen we ook makkelijk het *gemiddelde* uitrekenen. Bedenk dan dat `teller` aan het einde van de loop precies de telling van het totaal aantal elementen van de lijst bevat!

    som = 0
    teller = 0
    for meting in metingen_science_park:
        teller = teller + 1
        som = som + meting
        print "De %d e meting was %d graden." % (teller, meting)
    gemiddelde_temp = som / teller
    print "De gemiddelde temperatuur was %d graden." % gemiddelde_temp

Of we kunnen met zo'n loopje bijhouden op hoeveel dagen de temperatuur boven de 20 graden uitkwam:

    hete_dagen = 0
    for meting in metingen_science_park:
        if meting > 20:
            hete_dagen = hete_dagen + 1
    print "Op %d dagen was de temperatuur boven de 20 graden" % hete_dagen

Van lijsten is het belangrijk dat je weet hoe je een lijst definiert, hoe je elementen toevoegt aan een lijst en hoe je de individuele elementen afzonderlijk lukt bekijken.

## Opdracht

Probeer nu eens een programma te schrijven dat een lijstje met temperaturen in graden Celcius omrekent naar een nieuw lijstje met overeenkomstige temperaturen in graden Fahrenheit. De formule zoek je natuurlijk even op in een zoekmachine. 

> Let op! Zorg dat de uitkomsten van je algoritme goed controleert met voorbeelden. Als je met breuken van natuurlijke getallen gaat werken (bijvoorbeeld `3/4`) dan zal Python de tussenresultaten afkappen. Zorg dus dat je een hint geeft dat je met reeële getallen wil werken: `3.0/4.0`.

Sla dit programma op in een bestand **temperaturen.py** en bewaar het voor het inleveren.
