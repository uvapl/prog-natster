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

## Oefening

Probeer nu eens een programma te schrijven dat een lijstje met temperaturen in graden Celcius omrekent naar een nieuw lijstje met overeenkomstige temperaturen in graden Fahrenheit. De formule zoek je natuurlijk even op in een zoekmachine. Sla dit programma op in een bestand `temperaturen.py` en bewaar het goed voor inleveren.
