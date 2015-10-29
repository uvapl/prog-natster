# Lijsten

Naast getallen en strings zijn lijsten ook een basiselement van veel
programmeertalen. Lijsten is handig om data te groeperen en vervolgens als geheel te verwerken in bijvoorbeeld een berekening.

## Voorbeeld

Een lijstje met namen van docenten kun je zo bewaren:

	docenten = ["Martijn", "Ivo", "Rico", "Nick", "Rick", "Kelly"]

Elk element in deze lijst is een *string*, maar de lijst kan ook getallen of zelfs lijsten bevatten. Ook door elkaar heen. Je kunt elementen uit een lijst opvragen, ze veranderen of elementen toevoegen. Zo vraag je bijvoorbeeld een element op, om deze direct uit te printen:

    print docenten[2]

Probeer dit uit, want het antwoord is misschien niet precies wat je verwacht. Probeer daarom ook even het getal `2` te veranderen in andere getallen.

## Elementen toevoegen

Stel dat je een lijst met 5 temperatuurmetingen hebt (op het Science Park) en die wil je in een lijst opslaan en vervolgens wilt printen op het scherm dan gaat dat als volgt:

	metingen_science_park = [12.7, 18.8, 24.9, 14.5, 19.0]
    print metingen_science_park

Zoals je ziet kun je ook in één keer een hele lijst printen. Het hoeft niet per element.

Als je nu een zesde meting doet (20.5 graden) en die toe wilt voegen dan kan dat met behulp van het `append` commando:

    metingen_science_park.append(20.5)
    print metingen_science_park

In plaats van de lijst printen kunnen we ook de individuele elementen van de lijst printen of het aantal elementen in de lijst berekenen.

    print "Het eerste element van de lijst is %d" % metingen_science_park[0]
    print "Het aantal elementen in de lijst is %d" % len(metingen_science_park)

Nu kunnen we dus in ieder geval de hele lijst gebruiken, en invididuele elementen uitprinten.

## Loopen met een lijst

Je kunt ook elk element de lijst apart bekijken met behulp van een `for`-loop:

	metingen_science_park = [12.7, 18.8, 24.9, 14.5, 19.0]
    metingen_science_park.append(20.5)
    for meting in metingen_science_park:
	    print "de meting was %d graden" % meting

Zo zie je dat we direct over de elementen van een lijst kunnen loopen. We gebruiken dan niet meer het `range`-commando.

Zoals je ziet in bovenstaande voorbeeld zal het programma het gemiddelde
afronden. Het `%d` format zegt Python dat je een geheel getal op het scherm
wilt printen. Als je een reeel getal wilt printen zal je het `%f` commando
moeten gebruiken. We zullen dat later in de cursus in meer detail bekijken.

Nu is het in dit geval alleen wel informatief om mooi neer te zetten over *welke* meting het gaat. Dan moeten we zelf een tellertje bijhouden:

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

## Sanity check

Let op dat je alleen de volgende Python-onderdelen hebt gebruikt in je oplossingen:

- `print`
- `if`
- `else`
- `for` (en `in`)
- `range()`
- `len()`
- `.append()`
- en natuurlijk alle operators zoals `=`, `+`, `/`, `%`, `>`, `[]`
