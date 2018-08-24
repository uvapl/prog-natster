# Co-primes

Schrijf een programma `priemparen.py` dat de waarschijnlijkheid berekent dat twee willekeurig gekozen (grote) getallen geen onderlinge deler hebben. Zo'n paar getallen noemen we onderling priem.

    #python priemparen.py
    De kans dat twee random grote getallen geen onderlinge deler hebben is:
        - voorspelling (wiskunde): x.xx %
	    - empirisch (Python): x.xx %

## Definitie van onderling-priem en de voorspelling vanuit de wiskunde
	    
Op de wikipedia pagina van de zogenaamde [co-primes](https://en.wikipedia.org/wiki/Coprime_integers) vind je de definitie e en 

De kans dat $$n$$ getallen geen gemeenschappelijke deler hebben is gegeven door:

  - $$\frac{1}{\zeta(n)}$$. 

Waarbij $$\zeta(s) de beroemde [Riemann zeta functie]($$ https://en.wikipedia.org/wiki/Riemann_zeta_function) is.

*Let op:* in het geval van drie (of meer) of meer getallen betekent dit dat er geen getal is dat een deler is van alle drie (of meer) getallen **tegelijk**.

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
