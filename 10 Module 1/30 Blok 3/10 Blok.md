# Opgave 1: het 1000ste priemgetal

schrijf een programma `primes.py` dat het duizendste priemgetal berekent en po het scherm print. Print ook de lijst van alle 1000 priemgetallen.

Hoewel een computer je in staat stelt om snel te rekenen is het toch belangrijk om voor elk probleem de optimale strategie te bepalen. Het loont om voor je gaat programmeren eerst met pen en pepier je strategie uit te denken. In dit geval zijn er een aantal elementen van wiskunde kennis die je kan gebruiken om je programma een stuk sneller te maken:

- Behalve 2 zijn even getallen nooit een priemgetal
- Verzin hoe je per priem-kandidaat bijhoudt of het wel/niet priem is als je over de mogelijke delers heenloopt. Bedenk van tevoren hoe je de lijst met gevonden priemgetallen gaat opslaan.
- Wanneer kan je stoppen ? Als je wilt bepalen of 37 een priemgetal, welke kandidaat delers bekijk je voordat je zeker weet dat het een priemgetal is ? 
- Print voor elke kandidaat informatie zodat je weet waar je bent in de berekening en je ziet of de computer ook echt jouw strategie volgt
- Zorg dat het programma stopt bij het 1000ste priemgetal. Bedenk dat je programma waarschijnlijk niet het eerste priemgetal heeft gegenereerd (2)

Als je wilt controleren of je programma goed werkt kan je je gevonden lijst priemgetallen hier matchen met een lijst bekende priemgetallen <http://primes.utm.edu/lists/small/1000.txt>


# Opgave 2: werken met priemgetallen

Een van de deliverables van je vorige programma is een lijst van priemgetallen. We geen nu proberen extra informatie uit die reeks priemgetallen te halen. Let op: in deze opgave gebruiken we niet de lijst met de eerste 1000 priemgetallen, maar alle priemgetallen onder het getal 10000.

Welke getallen onder de 10000 vormen de langste reeks aaneengesloten niet-priemgetallen ? Start met de code uit de vorige opgave. Print naast de lengte van de reeks ook zowel het eerste als het laatste getal.


# Hacker opgave: snel sneller snelst

Maak je priemgetallen-zoek-programma zo snel mogelijk en kijk wat het grootste priemgetal is dat jouw programma in 1 minuut uit kan rekenen. Maak bij het testen van een getal n nu bijvoorbeeld gebruik van de kennis over de priemgetallen onder de n.


# Opgave 3: het vermoeden van Goldbach

Het vermoeden van Goldbach is een van de oudste onopgeloste problemen is in de wiskunde. Goldbach postuleerde dat:

*Elk even getal groter dan 2 kan geschreven worden als de som van 2 priemgetallen*

Een priemgetal mag hierbij twee keer gebruikt worden. Hoewel dit inderdaad klopt voor alle getallen tot $4\cdot10^{18}$ is er nog geen bewijs. We gaan ons steentje bijdragen. 

Laat zien dat alle even getallen tot 1000 inderdaad te schrijven zijn als de som van 2 priemgetallen

Je mag in deze opgave de directe Python constructie gebruiken die kijkt of een element wel of niet in een in een lijst voorkomt. De volgend constructie zal op het scherm printen dat 7 inderdaad een priemgetal is.

    L = [2,3,5,7,11]
    x = 7
	if x in L_mijnpriemgetallen:
	   print "Ja, het getal ", x, " komt voor in mijn priemlijst""

Laat voor elk getal dat je test expliciet zien dat het te schrijven is als de som van 2 priemgetallen:

   	16 = ...
	18 = 5 + 13 
    20 = 3 + 17 
    22 = 5 + 17
    24 = ...

Maar nog belangrijker is natuurlijk als je een getal vindt dat *niet* aan de Goldbach conjecture voldoet. Zorg dat jouw programma zo'n ontdekking duidelijk op het scherm aangeeft.
 
# Opgave 4: bevriende getallen:

Twee getallen A en B zijn *bevriende* getallen als de som van de delers van A (niet A zelf, maar inclusief 1) precies B oplevert. Tegelijkertijd moet de som van de delers van B precies A opleveren. Het eerste paar bevriende getallen is al lang bekend (220,284). Er geldt immers:

	som delers 220 = 1 + 2 + 4 + 5 + 10 + 11 + 20 + 22 + 44 + 55 + 110 = 284
	som delers 284 = 1 + 2 + 4 + 71 + 142 = 220

Schrijf een programma dat het volgende paar bevriende getallen vindt en beschrijf je strategie.
 

