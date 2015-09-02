# Het duizendste priemgetal

We gaan nu verder werken met de ideeën uit het vorige hoofdstuk en voorbeelden uit de getaltheorie bestuderen. Dit zijn problemen die handig met de computer uit te voeren zijn, omdat ze hele grote hoeveelheden klein rekenwerk vereisen. Aan ons de taak om op een efficiënte manier te noteren hoe de computer dit gaat aanpakken: programmeren dus!

> Twee dingen zijn belangrijk om te leren voor je met de opgave aan de slag gaat:
> 
> - Een computer is niet 'slim', maar voert droog commando's uit. Het is jouw taak als programmeur  om de computer alleen de hoogst noodzakelijke dingen te laten doen. 
> - Bepaal altijd met pen en papier je strategie en ga dus niet gelijk tikken. De 5-10 minuten die je hieraan besteedt verdien je dik terug tijdens de opdracht.
 
## Opgave

Schrijf een programma **primes1000.py** dat het duizendste priemgetal bepaalt en op het scherm print. Print ook de gehele lijst van duizend eerste priemgetallen.

Hoewel een computer je in staat stelt om snel te rekenen is het toch belangrijk om voor elk probleem de optimale strategie te bepalen. We geven een voorzetje:

- Verzin hoe je per kandidaat-priem bijhoudt of het inderdaad een priem is terwijl je over de mogelijke delers heenloopt.
- Bedenk van tevoren hoe je de lijst met (1000) gevonden priemgetallen gaat opslaan.
- Problemen? Print bij elke kandidaat-priem wat informatie, zodat je weet waar je bent in de berekening en je ziet of de computer ook echt jouw bedoelde strategie volgt.
- Begin klein. Zorg dat je programma eerst de priemetallen tot 10 kan vinden. Dat is klein genoeg om te zien of het programma precies doet wat de bedoeling is, en kun al snel ontdekken wat er mis gaat.

> Misschien is het raar of vervelend om een programma in te tikken, waarna je ontdekt dat het niet goed werkt. Dat is het lot van de programmeur: het is gewoon heel moeilijk om een precies algoritme te formuleren en dan helemaal correct om te zetten naar programmacode. Soms ben je een uitzondering vergeten, maar net zo goed heb je ergens een tikfout gemaakt. Onthou dat de beste programmeurs op deze manier werken!

     
### Wiskundetips

Hoewel het in deze opgave niet echt gaat om de snelheid van het programma is in deze specifieke opgave veel tijd te winnen door slim gebruik te maken van een aantal elementen uit de wiskunde. Maar let op! Doe dit pas als je zeker weet dat je programma hierboven correct is. Je kunt dan optimalisaties toepassen en snel vergelijken of je niet een *bug* in je code hebt geïntroduceerd. Dat zou jammer zijn voor een beetje tijdswinst!

- Behalve 2 zijn even getallen nooit een priemgetal

- Als je een deler vindt hoef je niet verder te zoeken

- Als je wilt bepalen of 37 een priemgetal welke kandidaat delers bekijk je dan voordat je zeker weet dat het een priemgetal is? Doe dit op pen en papier. Het zijn er maar 3 namelijk!

Als je wilt controleren of je programma goed werkt kun je je gevonden lijst priemgetallen hier controleren met een lijst bekende priemgetallen <http://primes.utm.edu/lists/small/1000.txt>


### Python tips

Soms is het handig om een loop eerder af te breken. Er zijn in Python verschillende mogelijkheden. De `while-loop` is 
de meest gebruikte, maar omdat dat aan het begin van jullie programmeer-carriere in dit korte introductievak tot 
verwarring kan leiden gaan we die niet introduceren. 

Hoewel het niet strikt noodzakelijk is voor de opgave van vandaag kan een stop misschien wel handig zijn. Naast de 
while-loop is er ook de `break` optie. Op het moment dat Python `break` ziet zal het de for-loop afbreken en verder 
gaan met de code. Hieronder een voorbeeld waarbij we de for-loop af willen breken zodra de som van de getallen tot 
dan toe groter is dan 50. Probeer onderstaande code te runnen zodat je ziet wat er precies gebeurt.

    som = 0
    for getal in range(1,100):
        som = som + getal
        print getal, " ", som
        if (som > 50): 
            break
            
    print "Ik stop omdat de som meer dan 50 is"  