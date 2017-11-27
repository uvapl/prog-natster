## Opdracht 3: Realisme toevoegen: twee spelers

In het echt wordt het spel Monopoly gespeeld door twee spelers. Doel van deze opdracht is om eerst te evalueren wat het voordeel is van de speler die begint met gooien en vervolgens te bestuderen hoe we in het spel dit nadeel voor speler 2 kunnen herstellen.
 
![](Balans.png){:.inline}{: style="width:35%"}
 
Let op: we gaan nu de code uit opdracht 1 en 2 aanpassen. Om te zorgen dat die werkende code bewaard blijft gaan we deze opdracht maken in een nieuw bestand. Maak een nieuw Python bestand aan, `Monopoly_realistisch.py`, kopieer de code die je tot nu toe hebt en ga verder in deze nieuwe file.

#### [deelopdracht 3a] voordeel van speler 1

Voeg eerst een tweede speler toe in je simulaties, laat beide spelers beginnen met 1500 euro startgeld en bepaal het verschil in aantal straten tussen speler 1 en speler 2 op het moment dat alle straten verkocht zijn. Dit verschil zal elk potje verschillen. Simuleer daarom 10000 potjes om een goede schatting te krijgen van het gemiddelde verschil. Je zal zien dat speler 1 inderdaad een klein voordeel heeft op speler 2.

Het doel is om dit verschil te achterhalen door een grot aantal potjes te simuleren:
{: .language-python}
	Monopoly simulator: twee spelers, 1500 euro startgeld, 10000 potjes
    Gemiddeld heeft speler 1 X.XX meer straten in bezit als alle straten verdeeld zijn


**Strategie:**

  - Aanpassing aan *input* functie `simuleer_potje_Monopoly()`
   
    De functie die een potje Monopoly simuleert heeft nu natuurlijk van beide spelers de hoeveelheid startgeld nodig. Geef beide als input variabalen mee aan de functie:
   `simuleer_potje_Monopoly(startgeld_speler_1,startgeld_speler_2)` 

 - Aanpassing aan *ouput* functie `simuleer_potje_Monopoly()`
   
   Tot nu toe hebben we de functie gevraagd het aantal worpen dat het potje geduurd heeft terug te geven als return waarde. Nu zijn we alleen geïnteresseerd in het verschil in aantal straten tussen speler 1 en speler 2: `delta = aantal_straten_speler_1 - aantal_straten_speler_2`. Dat is dat ook de variabele die we terug gaan geven als return waarden. **Let op:** deze waarde kan nu zowel positief als negatief zijn.

       delta = simuleer_potje_Monopoly(startgeld_speler_1,startgeld_speler_2)
       print 'Aan het eind van dit potje had speler 1 %d meer straten dan speler 2' % (delta)

 - Bijhouden hoeveelheid geld en posities van beide spelers:

   Hou voor beide spelers de hoeveelheid geld en positie bij. In het begin van het spel bijvoorbeeld geldt voor de posities van de spelers: `positie_1 = 0` en `positie_2 = 0`, maar de dapperen onder jullie kunnen de posities ook bijhouden in lijsten zoals `positie_lijst = [0,0]`. Dezelfde twee opties heeft u bij de hoeveelheid geld dat speler1 en speler 2 heeft tijdens het spel. Standaard is twee losse variabelen, maar je mag ook lijsten gebruiken.
   
Test de code altijd voor een enkel potje en bekijk goed of het doet wat je denk dat het zou moeten doen. Ga pas dan het aantal potjes vergroten. Gebruik daarvoor weer dezelfde opzet als je had in de functie `simuleer_groot_aantal_potjes_Monopoly()` en zorg ervoor dat je de vraag kunt beantwoorden. 

Print uiteindelijk het verschil naar het scherm:
{: .language-python}
	Monopoly simulator: twee spelers, 1500 euro startgeld, 10000 potjes
    Gemiddeld heeft speler 1 X.XX meer straten in bezit als alle straten verdeeld zijn

#### [deelopdracht 3b] nadeel van speler 2 repareren

De vraag is nu of en zo ja hoe we deze 'oneerlijke' situatie kunnen repareren. Een van de 'knoppen' waar je aan kan draaien in dit spel is de hoeveelheid startgeld die de spelers krijgen. Als speler 2 meer startgeld krijgt kan hij iets van zijn achterstand repareren. Bepaal de hoeveelheid extra startgeld die we aan speler 2 moeten geven aan het begin van het spel zodat hij gemiddeld net zoveel straten in zijn bezit heeft als speler 1 op het moment dat alle straten verdeeld zijn. Geef speler 2 steeds wat meer geld (kies een paar waardes van het startgeld en voer dat steeds handmatig in) en bereken steeds het verschil. Als je een paar simulaties hebt gedraaid heb je een kleine data-set waarmee je bovenstaande grafiek kan reproduceren en een goede schatting kan maken van de hoeveelheid extra geld dat we speler 2 moeten geven aan het begin van het spel om het evenwicht te herstellen. 

Reproduceer de grafiek en geef zowel in de grafiek als geprint naar het scherm aan hoeveel extra geld speler 2 moet krijgen om het evenwicht te herstellen. Het antwoord moet op 50 euro nauwkeurig zijn.

{: .language-python}
	Monopoly simulator: 2 spelers
    Als we speler 2 XXX euro meer startgeld meegeven hebben beide spelers gemiddeld evenveel straten in bezit


## Samenvatting

De simulatie die we hier gedaan hebben is een versimpelde versie van de vaak zeer complexe 
modellen waarmee grote financiele partijen risico's inschatten en strategieen bepalen. 
Tegelijkertijd worden deze simulaties ook gebruikt door politieke partijen om de effecten 
van hun keuzes door te rekenen in verschillende scenario's.




