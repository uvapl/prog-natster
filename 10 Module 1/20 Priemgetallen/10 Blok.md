# code-bouwsteen: is een getal wel of niet een priemgetal 

Schrijf een stuk code (`blok2a.py`) dat van een bepaald getal onderzoekt of het een priemgetal is of niet. Aan het eind van het programma moet duidelijk op het scherm geprint worden of het getal een priemgetal is of niet.

  	x = 37
	[jouw code]
 
Het getal 37 mag de gebruiker van jouw code natuurlijk zelf veranderen en aan het eind van het programma moet in dit geval geprint worden:

  	Het getal 37 is een priemgetal 
	
###strategie:
In deze eerste opgave gaan we het probleem eerst brute-force('dom') aanpakken. Gebruik een `for loop` en de `%` operatie om te bepalen hoeveel van de gehele getallen (onder ons kandidaat-priemgetal x) te kijken of het een deler is van x. Houd bij hoeveel delers x heeft en bepaal aan de hand daarvan aan het eind van de loop of het getal x een priemgetal is of niet. Print je conclusie uiteindelijk op het scherm.

*Optioneel:* zorg dat je code bij het invoeren 1,0 of een negatief getal gelijk zegt dat het geen priemgetal is en print ook op het scherm de boodschap naar de gebruiker van je programma dat hij een geheel en positief getal in moet voeren dat groter of gelijk aan 2 is.


# code-bouwsteen: bepaal alle priemgetallen onder de 100

Het vorige stukje code bekeek alleen of een specfiek getal een priemgetal was of niet. We kunnen dit stukje code recyclen en voor elk getal onder de 100 bepalen of het een priemgetal is of niet. 

###strategie:
Maak een apart programma (`blok2b.py`) en gebruik de `for loop` om alle getallen onder de 100 te genereren en bepaal voor elk van deze getallen of het wel of niet een priemgetal is. Voor elk getal moet je dus weer het delers bepalen en je zal dus een tweede `for loop` moeten gebruiken binnen de loop die de 100 getallen maakt. Dit zijn zogenaamde nested-loops. 

Een extra opdracht hierbij is om, als je een getal identificeert als een priemgetal, het te bewaren in een lijst. Print aan het eind de volledige lijst priemgetallen.

	L_priem = []
    for getal in range(2,100):
       [jouw code]
    print L_priem
   
Geef na het printen van de lijst ook aan hoeveel priemgetallen je gevonden hebt en print ook dat op het scherm. Hoe weet je hoeveel priemgetallen er in de lijst staan ? Klopt je antwoord ? 
   



