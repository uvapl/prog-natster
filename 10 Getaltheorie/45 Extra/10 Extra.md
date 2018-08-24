# Co-primes

Implementeer een programma dat op verzoek het $$n$$-de priemgetal genereert.

	Naar welk priemgetal bent u op zoek? 1000
	7919

## Voorspelling vanuit de wiskunde

Er is een voorspelling vanuit de wiskunde. Riemann zeta.

## Stap 1: priem-check

Een belangrijk deel van de omschrijving hierboven is dat het om priemgetallen gaat. Wat is een priemgetal? Dat moeten we in Python zien uit te drukken.

Schrijf dus eerst een programma dat van een bepaald getal onderzoekt of het een priemgetal is of niet. Aan het eind van het programma moet duidelijk op het scherm geprint worden of het getal een priemgetal is of niet. Het begint met een variabele `number`, waarin we het getal zetten dat onderzocht moet worden:

    number = input("Voer een getal in: ")
    number = int(number)
    # TODO: hier komt jouw code

Als de gebruiker het getal 37 invult, moet aan het eind van het programma geprint worden:

    Het getal 37 is een priemgetal

Bij een niet-priemgetal, zoals 36, moet geprint worden:

	Het getal 36 is geen priemgetal

## Testen

Er is voor deze opdracht geen checkpy aanwezig. You're on your own.
