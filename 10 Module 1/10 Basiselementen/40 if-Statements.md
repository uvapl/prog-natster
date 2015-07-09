# if-Statements

Tot nu toe hebben we een lang tekstbestand gemaakt met drie soorten regels:

- instructies (die Python kent)
- commentaar (waar Python niets mee doet, maar die wij kunnen lezen)
- lege regels (waar Python niets mee doet, en die helpen onderscheid te maken tussen stukken code)

Nu gaan we een nieuwe Python-instructie (*statement*) gebruiken: `if`. Bij deze instructie combineer je een *voorwaarde* met een aantal regels die alleen uitgevoerd worden als de voorwaarde "waar" is.

Als je wilt kijken of een getal positief is bijvoorbeeld. Tik het maar over.
	
	x = 15
	if x > 0:
	    print "Het getal %d is positief." % x

Je ziet dat er een voorwaarde is: `x > 0`, ofwel `x` moet positief zijn. En er is een regel die alléén wordt uitgevoerd als `x > 0`. Probeer het maar uit.

Een belangrijk punt is dat de regel meteen na de `if` begint met vier spaties. Met deze spaties laat je zien dat dit de regels zijn die bij de `if` horen.

Om te printen of een getal een negatief is zou je een extra regel toe kunnen voegen, maar je kan de 'stroom' van het programma ook sturen als er juist niet aan de voorwaarde voldaan is. Als je bijvoorbeeld wilt testen of een getal positief of negatief is dan kan je naast de `'if` ook de `else` constructie gebruiken.

	x = 15
	if x > 0:
		print "het getal", x, " is positief"
	else
		print "het getal", x, " is negatief"

Je kan ook verschillende voorwaardes ook combineren. Als je wilt weten of een getal zich in een bepaalde range bevindt (bijvoorbeeld tussen de 3 en de 39) dan kan je met `and` verschillende condities (voorwaardes) combineren:

	x = 15
    x_min = 3
    x_max = 39	
	if x > x_min and x < x_max:
		print "het getal", x, " bevindt zich in de range"


De conditions die we hier gebruiken zijn:

- `>` 	groter dan
- `>=`	groter of gelijk aan
- `<` 	kleiner dan
- `<=`	kleiner dan of gelijk aan
- `==`	is gelijk aan
- `!=`	is niet gelijk aan


