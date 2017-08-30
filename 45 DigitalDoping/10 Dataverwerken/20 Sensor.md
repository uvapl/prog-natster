# Opdracht: sensordata verwerken  

![](StravaLogo.png){:.inline}{: style="width:8%"}

Een mobiele telefoon bevat sensoren om grootheden als positie, snelheid, versnelling vast te 
leggen. Deze data wordt naast navigatie ook gebruikt in verschillende apps die voor sporten 
gebruikt worden. In deze opdracht gaan we aan de slag met de data die verzameld is in een 
app die door wielrenners gebruikt wordt: Strava. Na het sporten kan je in detail je rit 
terugkijken: de projectie van de route op een interactieve kaart, de gemiddelde snelheid, 
het hoogteprofiel, records op vooraf gedefiniëerde stukken weg en nog veel meer. We gaan 
in deze opgave zelf deze informatie uit de sensor-data halen en, niet verder vertellen, 
proberen de data in de file te manipuleren: digitale doping.

Onze data-file is een echte fietsrit die een natuurkundige aan de universiteit van Amsterdam 
maakte in de buurt van Leiden samen met zijn buurman. De data-file met de informatie zoals 
die door de app verzameld is is hier te downloaden: [FietsRitData.gpx](FietsRitData.gpx).

De eerste regels van de file bevatten wat algemene tekstuele informatie, maar daarna wordt 
het interessant. Elk meetpunt (ongeveer om de seconde) worden drie zaken vastgelegd: positie, 
hoogte en het tijdstip. Dit is voldoende informatie. In het plaatje hieronder zie je een 
kleine preview van de eerste drie meetpunten die in de file te vinden zijn:

![](DataFilePreview.png){: style="width:40%"}

Als je goed kijkt zie je dat de informatie van elke meting in drie regels wordt weggeschreven:

	1) positie in lengte- en breedtegraad 
	2) de hoogte
	3) de datum en tijd

We gaan in deze opgave stap voor stap een programma `Strava.py` schrijven dat de data inleest, 
decodeert, opslaat in afzonderlijke lijsten en vragen over de rit beantwoordt. We zullen dat 
doen dat aan de hand van de onderstaande opdrachten.

## Opdracht 1: teken de route op het scherm

Maak een functie `Fietsrit()` die de file opent, alle metingen doorloopt en voor elk meetpunt 
de locatie opslaat in twee afzonderlijke lijsten: de latitude en de longitude. Maak aan het 
eind een grafiek van de meetpunten. Oriënteer het zo dat het op een kaart van Google maps 
geprojecteerd zou kunnen worden, dus het noorden netjes in het noorden.

Een paar extra randvoorwaarden voor het tekenen van de grafiek:

	- Geef het beginpunt aan met een grote groene stip en het eindpunt met een kleine gele 
	- Verderop in de opgave gaan we nog wat extra informatie toevoegen op het scherm. Hou 
	  dus iets ruimte over bij het tekenen van de grafiek.  
	  Randen grafiek:
	     - longitude tussen 4.325 en 4.675
	     - latitude tussen 52.05 en 52.16

### Computing tip:

Tijdens het inlezen van elke regel kan je een test uitvoeren of er een bepaalde string in de 
regel voorkomt. Als je de string *<trkpt* tegenkomt weet je bijvoorbeeld dat je de regel met 
de positie aan het inlezen bent. Maar als je de regel 'herkend' hebt ben je er nog niet. Je 
moet daarna nog de latitude en longitude, die op vaste posities zitten, uit de string 'peuteren'. 

       if "<trkpt" in line: 
           latitude = ....
           longitude = ....

**Let op:** 
Zodra je het stukje regel hebt herkent waar de latitude is opgeslagen herkent de 
computer dit nog steeds al tekst en niet als getal. Gebruik de functie `float()` om dat 
stukje van de regel ook echt om te zetten in een getal voor je het opslaat in de lijst. Zo 
kan je er verderop in het programma ook mee rekenen.

## Opdracht 2: totaal afgelegde afstand en snelheidsgrafiek

Maak een grafiek van de snelheid als functie van de tijd, waarbij de tijd weergegeven is 
als het aantal seconden na het begin van de rit. 

Laat je programma ook deze grootheden printen in het volgende format:

	Rit: de totale duur van de rit was x uur, y minuten en z seconden
	Rit: de totaal afgelegde weg was x.x km
	Rit: de gemiddelde snelheid was xx.x km/uur
	Rit: de maximum snelheid was xx.x km/uur en werd gereden x seconden na de start van de rit
        
Volg de volgende stappen bij het beantwoorden van de opdracht.        
        
### Stappenplan:

	- stap 1: maak de lijst met meettijden (in seconden na het begin van de rit)

Als je de regel met de tijdstippen hebt gedecodeerd (uur, minuten en seconden) is het handig 
om die om te rekenen naar een aantal seconden sinds het begin van de dag. Dit maakt het daarna 
eenvoudig om het verschil tussen verschillende meetmomenten te berekenen. Het is handig om het 
eerste meetmoment te definiëren als t=0. Elk meetpunt kan je daarna uitrekenen als verlopen tijd 
ten opzichte van dat tijdstip en dat zo in de lijst opslaan.

    - stap 2: maak de lijst met snelheden 

Zodra je vanuit de datafile alle posities en tijden hebt ingelezen kan je de file sluiten. Je hebt dan alle informatie die je nodig hebt en kan de 'afgeleide' informatie zelf uitrekenen. Wij gaan bijvoorbeeld de totale afgelegde weg en de lijst met snelheden op elk tijdstip uitrekenen. Als we bij meetpunt *i* zijn aangekomen weten we zowel de afgelegde weg (verschil tussen de twee posities) als het tijdsverschil en kunnen zo de snelheid op dit kleine interval berekenen. Sla de snelheden op elk meetpunt op in een lijst.

*Let op:* we nemen aan dat de fietser stilstond op t=0, dus het eerste element in de lijst met snelheden is 0.

    - stap 3: de lijst met afgelegde afstanden


Tijdens het (opnieuw) doorlopen van de lijsten om de snelheidslijst te vullen kan je nu ook de totale (tot nu toe) afgelegde weg bijhouden in een lijst. Ook deze list begint met 0 op t=0.

Geef ook in de grafiek duidelijk aan wat de maximale snelheid was gedurende de rit. Geef 
de maximale snelheid met een groene stip aan in de grafiek en geef ook de numerieke waarde 
in de grafiek weer.



        
## Opdracht 3: afgelegde route met extra informatie

Teken opnieuw de grafiek van de afgelegde route (net als in opdracht 1), maar voeg nu wat extra elementen toe:


	- rit-karakteristieken (duur, afgelegde weg en gemiddelde snelheid) als tekst in de grafiek
	- groene stip waar de maximale snelheid werd behaald. Snelheid ook in groene tekst in buurt van de stip
	- rode bolletjes waar de snelheid lager was dan 20 km/uur


![](RitkaartWebsite.png){: style="width:80%"}


Laat je programma ook berekenen hoe lang er onder de 20 kilometer per uur gereden is. 

Print dus: 

	Er is gedurende x seconden langzamer gereden dan 20 km/uur
	


## Opdracht 4: Fake data: Nederlandse col van de buitencategorie

Oud wielrenner Thijs Zonneveld lanceerde een paar jaar geleden het idee om een berg in Nederland te plaatsen. Geen grap hè, kijk maar naar deze Youtube clip: [Die berg komt er!](https://www.youtube.com/embed/MVyWMS1Jj6M)

Om te kijken hoe dat er op een Strava profiel uit zou zien en om zijn buurman in een klap voorbij te gaan in het hoogtemeters-in-dit-kalenderjaar klassement besluit de natuurkundige de data van zijn rit zo te manipuleren dat het lijkt of hij al een berg zo hoog als de Matterhorn (4478 m) heeft geklommen tijdens dit zondagse ritje door het groene hart. Fake data!
 
### Opdracht 4a: teken het oorspronkelijke hoogteprofiel van de rit

Naast de locatie en de tijd is ook de hoogte opgeslagen op elk meetpunt. Sla ook die data op in een lijst en teken de grafiek van de hoogte als functie van de tijd (weer in seconden sinds het begin van de rit). 

![](Matterhorn.jpg){:.inline}{: style="width:40%"}

### Computing tip:
*Let op:* het kan erg verleidelijk zijn om op basis van de eerste paar regels in de data-file te concluderen dat de hoogte tijdens een rit is opgeslagen in een deel van de regel die maar 3 karakters breed is (X.Y) en dat dat correspondeert met X meter en Y decimeter boven zeeniveau. Nou klopt het dat je rond Leiden nooit boven tien meter boven of onder zeeniveau uitkomt, maar als je op elke andere plek inde wereld gaat fietsen zal de hoogte ook best tussen de -20 en +2500 kunnen liggen. Hoewel je niet van tevoren weet hoe hoog je zit weet je wel hoeveel karakters er *voor* de hoogte staan en ook hoeveel karakters er *achter* de hoogte staan. Je kan de hoogte dus zo wel uit de regel peuteren:

	dus niet:  hoogte = float( line[9:12] )
	maar:      hoogte = float( line[9:len(line)-7] )
	

### Opdracht 4b: creëer de fake data-set

Maak een nieuwe data-file `Matterhorn.gpx` die bijna identiek is aan de originale `FietsRitData.gpx` 
en die alleen verschilt in de regels die de hoogte aangeven. Pas de regels met de hoogte aan zodat 

	- eerste kwart: zeeniveau
	- tweede kwart: lineair omhoog tot we de hoogte van de Matterhorn bereiken halverwege de rit
	- derde kwart:  lineair omlaag tot weer op zeeniveau zitten
	- vierde kwart: zeeniveau
		
### Computing tip:

	- Volg het voorbeeld in het begin van de module om te hebben we gezien hoe je een file kan aanmaken en 
er een regel in weg kan schrijven.  
	- gebruik de code die je in opdracht 4a geschreven hebt om te verifiëren of het hoogteprofiel inderdaad
	  correct in de file is weggeschreven.


# Extra opdrachten (niet verplicht)

## Opdracht 5: snelste en langzaamste stukken van de rit

We kunnen de data in meer detail bekijken, Twee van de vele vragen die we kunnen stellen zijn 
die hieronder in vraag 5a en 5b zijn gesteld.

### Opdracht 5a: de langste en kortste afstand afgelegd *in een minuut*

Loop door de verzamelde data heen en zoek de minuut waarin de grootste en de langzaamste afstand is 
afgelegd. Hiermee weet je gedurende welke minuut er het respectievelijk het snelst en het langzaamst 
is gereden. Print deze data op het scherm:

	`Minuut: snelst  => afstand = x.xx m, gemiddelde snelheid = x.xx m/s`
	`Minuut: traagst => afstand = x.xx m, gemiddelde snelheid = x.xx m/s`

*Let op:*
Niet elke tijdstap tussen twee metingen is precies een seconde.


### Opdracht 5b: de langste en kortste afstand afgelegd *in een kilometer*

Loop door de verzamelde data heen en zoek de kilometer die in het kortste en het langste tijdsinterval is 
afgelegd. Hiermee weet je gedurende welke kilometer er het respectievelijk het snelst en het langzaamst 
is gereden. Print deze data op het scherm:

	`Kilometer: snelst  => tijdsduur = x s, gemiddelde snelheid = x.xx m/s`
	`Kilometer: traagst => tijdsduur = x s, gemiddelde snelheid = x.xx m/s`

*Let op:*
Niet elke tijdstap tussen twee metingen is precies een seconde.

## Opdracht 6: digital epo

Dit is niet een opdracht waarin je iets moet maken, maar waarin je na moet denken.

In opdracht 4 hebben we gezien hoe we de data kunnen manipuleren zodat het lijkt of we een enorme 
berg hebben bedwongen in een polderlandschap. Dat hebben we natuurlijk op een knullige manier 
gedaan, maar je kan je voorstellen dat je dat ook op een minder opzichtige manier doet.

Je zou bijvoorbeeld kunnen 

waarop je de data zo moet veranderen zodat het lijkt of je X% (zeg 5%) sneller hebt gereden dan in 
werkelijkheid. Beantwoord de volgende vragen:

	- Hoe moet je de file veranderen zodat het lijkt of je 5% sneller bent geweest?
	
Sommige mensen kunnen zich helaas niet inhouden: [digital epo](http://digitalepo.com/)

Nou zijn er verschillende manieren waarop je zou kunnen proberen te achterhalen waarop deze

	- Hoe zou je kunnen achterhalen of een file gemanipuleerd is?
	
Elk antwoord dat je hierboven opschrijft zou je natuurlijk ook kunnen gebruiken om de data op een 
gerafiniëerde manier te manipuleren zodat al deze tests negatief terugkomen. Het is het bekende kat- 
en muisspel in de sport, maar nu met digitale doping.




