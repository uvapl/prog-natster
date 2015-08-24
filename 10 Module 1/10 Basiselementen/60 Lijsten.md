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

    print "Het eerste element van de lijst is ", metingen_science_park[0]
    print "Het aantal elementen in de lijst is ", len(metingen_science_park)

Nu kunnen we dus in ieder geval de hele lijst gebruiken, en invididuele elementen uitprinten.

## Loopen met een lijst

Je kunt ook elk element de lijst apart bekijken met behulp van een `for`-loop:

	metingen_science_park = [12.7, 18.8, 24.9, 14.5, 19.0]
    metingen_science_park.append(20.5)
    for i in range(0,len(metingen_science_park)):
	    print "meting %d was %d graden" % (i, metingen_science_park[i])

Hierbij loopt het getal `i` (de *index*) van 0 tot het aantal elementen in de lijst en kan je de index gebruiken om het ie element in de lijst te printen. 

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

## Oefening

Probeer nu eens een programma te schrijven dat een lijstje met temperaturen in graden Celcius omrekent naar een nieuw lijstje met overeenkomstige temperaturen in graden Fahrenheit. De formule zoek je natuurlijk even op in een zoekmachine. Sla dit programma op in een bestand `temperaturen.py` en bewaar het goed voor inleveren.
