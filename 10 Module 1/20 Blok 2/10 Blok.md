# Is een getal een priemgetal

Schrijf een stuk code (`blok2a.py`) dat van een bepaald getal onderzoekt of het een priemgetal is of niet. Aan het eind van het programma moet duidelijk op het scherm geprint worden of het getal een priemgetal is of niet.

  	x = 37
	[jouw code]
 
Het getal 37 mag de gebruiker van jouw code natuurlijk zelf veranderen en aan het eind van het programma moet in dit geval geprint worden:

  	Het getal 37 is geen priemgetal 
	
In deze eerste opgave gaan we eerst 'dom' kijken (later gaan we het slimmer aanpakken). Bekijk voor elk van de gehele getallen onder het te onderzoeken getal x of het een deler is van x. Bewaar het aantal delers voor x en bepaal aan de hand daarvan aan het eind van de loop of het getal een priemgetal is of niet. 

# Bepaal alle priemgetallen onder de 100

Het vorige stukje code bekeek alleen of een specfiek getal een priemgetal was of niet. We kunnen dit stukje code recyclen en voor elk getal onder de 100 bepalen of het een priemgetal is of niet. Maak een apart programma (`blok2b.py`) en gebruik de `for-loop` om alle getallen onder de 100 te genereren en te testen. Als je een getal identificeert als ene priemgetal bewaar het dan in een lijst. Print aan het eind de volledige lijst priemgetallen.

	L_priem = []
    for getal in range(2,100):
       [jouw code]
    print L_priem
   
Geef aan het eind van je programma ook aan hoeveel priemgetallen je gevonden hebt. Klopt je antwoord ?
   



