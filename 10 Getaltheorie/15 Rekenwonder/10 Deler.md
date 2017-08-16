
# Rekenwonder: de mens

<div style="width: 40%; float:right; margin-left: 2em;">
![embed](https://www.youtube.com/embed/urFiv_PQ2FQ)
</div>

Voor het tijdperk van de computer werden lastige berekeningen gedaan door mensen. Bij het Europees laboratorium voor deeltjesfysica, CERN in Genève bijvoorbeeld werktes mensen als 'onze' Wim Klein, als 'menselijke supercomputers'. 

Het kan natuurlijk dat je een van die uitzonderlijke natuurtalenten bent, maar we gaan je voor de zekerheid toch maar leren hoe je met behulp van een computer nog veel een veel sneller kan rekenen. Eerst de basisstappen. 


# Rekenwonder: de computer laten rekenen

Implementeer een programma dat aan een gebruiker twee getallen vraagt en het product van de getallen uitrekent en op het scherm print.

	Wat is het eerste getal? 16
	Wat is het tweede getal? 4
	64

	Wat is het eerste getal? 27
	Wat is het tweede getal? 5
	135

## Specificatie

Schrijf in een nieuwe file genaamd `rekenwonder.py` een programma dat de gebruiker vraagt om twee gehele getallen, waarna het product van de getallen met `print` wordt doorgegeven aan de gebruiker.

## Hints

* Dit programma voldoet aan het cliché van een standaard computerprogramma: het heeft *invoer*, *berekeningen*, en *uitvoer*. Probeer die drie onderdelen ook terug te laten komen in je code!

* Maak gebruik van de `raw_input`-functie en gebruik `int()` om de invoer van de gebruiker om te zetten van een string naar een integer, zodat je de berekening kunt uitvoeren.

## Testen

Loop eerst je eigen programma na: werkt dit voor alle normale invoer? Start het programma door het volgende in te tikken in de terminal:

	python rekenwonder.py

Vul bijvoorbeeld eens het voorbeeld hier bovenaan in. Lijkt alles te werken, dan is het tijd om `checkpy` erbij te pakken. Testen gaat net zo als bij `hello`, alleen roep je nu de test voor `rekenwonder` aan. Zo dus:

	checkpy rekenwonder

Zie je unhappy smileys, en kom je er niet uit wat er fout gaat? Stuur een mail of kom langs!


