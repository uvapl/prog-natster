# Variabelen

In je programma kun je grootheden (*waarden*) opslaan onder een zelfgekozen naam. Zo kun je bijvoorbeeld het resultaat van een berekening op de ene regel ook gebruiken op een andere regel later in het programma.

Als je een getal hebt, bijvoorbeeld het aantal studenten in je groep (20), en dat wilt onthouden, dan schrijf je dit:

	aantal = 20

We hebben gekozen voor `aantal`, maar we hadden net zo goed kunnen kiezen voor de naam `afstand` of `dx`, of iets anders. Zorg dat de naam van de variabele goed te begrijpen is, zodat je een week later weer makkelijk door kunt gaan met het uitbreiden van je programma.

Als je de *waarde* van de variabele op het scherm wil printen dan doe je dat als volgt:

	aantal = 20
	print aantal

Omdat de computer de regels in je programma van boven naar beneden uitvoert, kun je in regel 1 een waarde opslaan onder de naam `aantal` en op regel 2 deze naam gebruiken om te printen. De computer zoekt dan op wat de waarde is van deze variabele, en print deze waarde.

De variabele kun je ook tussentijds manipuleren. Als één van de je medestudenten besluit toch maar biologie te gaan studeren dan is er 1 student minder in de groep.

	aantal = 20
    print aantal
	aantal = aantal - 1
	print aantal

Op regel 3 krijgt `aantal` een nieuwe waarde (19). Deze wordt berekend uit de 'oude' waarde van `aantal` (20).
