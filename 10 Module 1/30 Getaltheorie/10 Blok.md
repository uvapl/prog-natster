In dit blok gaan we de code die je aan het eind van in blok 2 ontwikkeld hebben iets uitbreiden en sneller maken door het iets slimmer aan te pakken. We gaan proberen het duizendste priemgetal te bepalen.

Twee dingen zijn belangrijk om te leren voor je met de opgave aan de slag gaat:

 - Een computer is niet 'slim'. Hij voert gewoon commando's uit. Als programmeur ben jij om de computer alleen de hoogst noodzakelijke dingen te laten doen. 
 - Bepaal altijd met pen en papier je strategie en ga dus niet gelijk tikken. De 5-10 minuten die je hieraan besteedt verdien je dik terug tijdens de opdracht.
 
# Opgave 1: het $$1000^{\rm ste}$$ priemgetal

schrijf een programma `Primes1000.py` dat het duizendste priemgetal bepaalt en op het scherm print. Print ook de lijst van alle 1000 priemgetallen.

Hoewel een computer je in staat stelt om snel te rekenen is het toch belangrijk om voor elk probleem de optimale strategie te bepalen. Het loont om voor je gaat programmeren eerst met pen en pepier je strategie uit te denken. In dit geval zijn er een aantal elementen van wiskunde kennis die je kan gebruiken om je programma een stuk sneller te maken:

- Behalve 2 zijn even getallen nooit een priemgetal
- Als je een deler vindt hoef je niet verder te zoeken
- Als je wilt bepalen of 37 een priemgetal welke kandidaat delers bekijk je dan voordat je zeker weet dat het een priemgetal is ? Doe dit op pen en papier. Het zijn er maar 3 nl.
- Verzin hoe je per priem-kandidaat bijhoudt of het wel/niet priem is als je over de mogelijke delers heenloopt. 
- Bedenk van tevoren hoe je de lijst met gevonden priemgetallen gaat opslaan.
- Problemen ? Print voor elke kandidaat informatie zodat je weet waar je bent in de berekening en je ziet of de computer ook echt jouw briljante strategie volgt
- Zorg dat het programma stopt bij het 1000ste priemgetal. Bedenk dat je programma waarschijnlijk niet het eerste priemgetal heeft gegenereerd (2)

Als je wilt controleren of je programma goed werkt kan je je gevonden lijst priemgetallen hier matchen met een lijst bekende priemgetallen <http://primes.utm.edu/lists/small/1000.txt>

*Hacker opgave (optioneel: snel sneller snelst*

Maak je priemgetallen-zoek-programma zo snel mogelijk en kijk wat het grootste priemgetal is dat jouw programma in 1 minuut uit kan rekenen. Maak bij het testen van een getal n nu bijvoorbeeld gebruik van de kennis over de priemgetallen onder de n.


# Opgave 2: werken met priemgetallen

Een van de deliverables van je vorige programma is een lijst van priemgetallen. We gaan in deze opgave proberen extra informatie uit die reeks priemgetallen te halen. Schrijf een programma `PrimesList.py` dat de langste aaneengesloten reeks niet-priemgetallen ? Start met de code uit de vorige opgave. Print naast de lengte van de reeks ook de 2 priemgetallen waartussen deze reeks ingeklemd zit.

Let op: in deze opgave gebruiken we niet de lijst met de eerste 1000 priemgetallen, maar alle priemgetallen onder het getal 10000. 




# Opgave 3: het vermoeden van Goldbach

Het vermoeden van Goldbach is een van de oudste onopgeloste problemen in de wiskunde. Goldbach postuleerde dat:

*Elk even getal groter dan 2 kan geschreven worden als de som van 2 priemgetallen*

Een priemgetal mag hierbij twee keer gebruikt worden. Hoewel dit inderdaad klopt voor alle getallen tot $4\cdot10^{18}$ is er nog geen bewijs. We gaan ons steentje bijdragen. 

Laat zien dat alle even getallen tot 1000 inderdaad te schrijven zijn als de som van 2 priemgetallen. Concreet: laat voor elk even getal ook expliciet zien dat het te schrijven is als de som van 2 priemgetallen:

   	16 = ...
	18 = 5 + 13 
    20 = 3 + 17 
    22 = 5 + 17
    24 = ...

Maar nog belangrijker is natuurlijk als je een getal vindt dat *niet* aan de Goldbach conjecture voldoet. Zorg dat jouw programma zo'n ontdekking duidelijk op het scherm aangeeft.

*Tip:* Je mag in deze opgave de onderstaande Python constructie gebruiken die kijkt of een element wel of niet in een in een lijst voorkomt. De volgend constructie zal op het scherm printen dat 7 inderdaad een priemgetal is.

    L_priem = [2,3,5,7,11]
    x = 7
	if x in L_priem:
	   print "Ja, het getal ", x, " komt voor in mijn priemlijst""

En als je voor elk van de getallen 1 tot en met 40 wilt bekijken of ze in de lijst staan gebruik je dus:

    L_priem = [2,3,5,7,11]
    for x in range(1,41):
	  if x in L_priem:
         print "Ja, het getal ", x, " komt voor in mijn priemlijst""
	  
# Opgave 4: bevriende getallen:

Twee getallen A en B zijn *bevriende* getallen als de som van de delers van A (niet A zelf, maar inclusief 1) precies B oplevert. Tegelijkertijd moet de som van de delers van B precies A opleveren. Het eerste paar bevriende getallen is al lang bekend (220,284). Er geldt immers:

	som delers 220 = 1 + 2 + 4 + 5 + 10 + 11 + 20 + 22 + 44 + 55 + 110 = 284
	som delers 284 = 1 + 2 + 4 + 71 + 142 = 220

Schrijf een programma dat het volgende paar bevriende getallen vindt en beschrijf je strategie.
 

