# Random getallen en data visualisatie

In dit blok zullen we twee verschillende concepten behandelen:
    
 - [1] random getallen

 - [2] Het visualiseren van data met behulp van een frequentie distributie (histogram)


## [1] Gebruik van random getallen

Een zeer handige bouwsteen in computer is het random getal. In de bibliotheek `random` zit een functie `random() die een random getal produceert tussen 0 en 1 volgens. In Python gebruik je de functie als volgt:

    import random 
    x = random.random()
    print x

Elke keer dat je de functie aanroept zal het een nieuw getal opleveren. Tien random getallen achter elkaar doe je dus als volgt:

    import random 
    for i in range(1,11):
       x = random.random()
       print x

### bouwen met bouwstenen

Zodra je een bouwsteen hebt kan je met behulp van logica en wiskundige manipulaties hier zelf andere objecten van bouwen. Als de computer bijvoorbeeld een random getal tussen 0 en 1 kan produceren dan kunnen we die zo omschrijven dat het transformeert in een random getal tussen een getal a en b.

Voorbeeld: tien random getallen tussen 0 en 2

    import random 
    for i in range(1,11):
       x = random.random()
       y = 2*x
       print y

# Opgave 1: Een rij van 10 random getallen tussen a en b

Schrijf een programma dat 10 random getallen op het scherm print tussen *a* en *b* waarbij je de waardes van a en b zelf kan kiezen en een aparte functie de transformatie uitvoert.

    import random 

    #------------------------
    def MijnRandomGetal(a,b):
    #------------------------
    #--/ functie die een random getal produceert tussen a en b
         getal = <hier jouw code>           
         return getal
     
    #--/ main code
    a = 2
	b = 5 
    for i in range(1,11):
       x = MijnRandomGetal(a,b)
       print x

Bekijk goed het voorbeeld hierboven waarbij we een random getal tussen 0 en 2 maakten en probeer eerst uit te vinden hoe je een random getal tussen de -1 en +1 zou kunnen maken. Daarna kan je dat abstract programmeren naar een algemene *a* en *b* als begin en eindwaardes van het interval waarbinnen je random getallen wilt gebruiken.


#  Opgave 2: De gemiddelde afstand tussen 2 punten in een vierkant

Schrijf een functie `Vierkant()` die de gemiddelde afstand tussen 2 punten in een vierkant met afmeting 1 x 1 berekent. Gebruik de volgende strategie:

  - Genereer twee random punten: dus 2 keer een random x-waarde en 2x een random y-waarde en bereken de afstand tussen de punten

  - Doe dit bovenstaande een groot aantal (N) keer en bewaar de totale afstand (som afstanden)

  - Bereken de gemiddelde afstand door de totale afstand te delen door N.

![](vierkant.png)

Dit is een typisch voorbeeld van een duidelijk en simpel probleem dat analytisch nogal lastig op te lossen is. Probeer het maar eens. 


### Tip: bedenk van tevoren welk antwoord je verwacht
Net zoals je bij een gewone natuurkunde of wiskunde opgave is het belangrijk om vooraf een schattimng te maken van de uitkomst zodat je een duidelijk verkeerd antwoord gelijk herkent. Wat denk je dat het antwoord moet zijn ? Als je programma klaar is kan je ook heel makkelijk de gemiddelde afstand in een vierkant van 2x2 uitrekenen. Wat denk je ? Is dat 'gewoon' 2 keer zo groot als je antwoord bij het 1x1 vierkant .... of is het misschien $$x^2$$ keer zo groot ... of juist $$\sqrt{2}$$ ? 


# [2] Visualisatie van data: histogrammen

Een grafiek tekenen zoals in Module 1 is een van de manieren om data te visualiseren. Het is niet altijd de meest logische manier om data te representeren. Als de Volkskrant bijvoorbeeld een grafiek maakt van de lengte van iedereen in Nederland dan gebruiken ze een zogenaamd `histogram` (staafdiagram of frequentiedistributie) waarbij een deel van de data gegroepeerd wordt. Er wordt bijvoorbeeld bijgehouden hoeveel (procent van de) mensen een lengte hebben in een bepaald interval, bijvoorbeeld tussen 160 en 165 cm, maar ook in de gebieden 165-170, 170-175 etc etc. Die manier om de data te representeren geeft gelijk een goed beeld. 

In Python gebruik je daarvoor de optie `plt.hist` om de data te groeperen en laat het dan pas zien mbv `plt.show()`. je kunt bij het groeperen opgeven in hoeveel stukjes (bins) je de data op wilt delen. 


### voorbeeld: distributie van 10.000 random getallen

Het idee van een random getal is dat het uniform verdeeld is tussen 0 en 1. Om een indruk te kijken of de verdeling inderdaad 'vlak' is kunnen we van 10.000 random getallen kijken wat de frequentie is van de getallen die gegenereerd zijn. 

Hieronder een klein programma dat eerst 10.000 random getallen genereert en ze in een lijst stopt. Bij het commando `plt.hist()` wordt opgegeven dat we de frequentie willen bepalen van getallen in gebieden van 0.02 (immers 50 bins tussen de minimale en maximale waarde die we verwachten: 0.00 en 1.00).

    import matplotlib.pyplot as plt
    from pylab import plot,hist, show,ylim, xlim,ylabel,xlabel,text

    #--/ lijst waar je de random getallen in bewaart
    L_random_getallen = []
    
    #--/ genereer 10.000 random getallen
    n = 10000
    for i_getal in range(n):
        getal = random()          
        L_random_getallen.append(getal)
    
     #--/ plot de frequentie-distributie (50 bins)
     plt.xlim(-0.1,1.1)
     plt.hist(L_random_getallen,bins=50)
     plt.show()
       

![](HistogramExample.png)

Note: de extra optie `xlim` gebruiken we hier om te laten zien dat er geen getallen buiten het interval 0.00-1.00 zijn gegenereerd. Kijk in de documentatie op het web welke opties er allemaal zijn om het histogram de vorm te geven die jij wilt: relevant aantal bins, kleur, asbijschriften, legenda, tekst, etc etc.

# Opgave 3: distributie van de som van random getallen

Dat de random getallen zelf keurig uniform tussen 0 en 1 verdeeld zijn hebben we net gezien, maar hoe zit het eigenlijk met de verdeling van de som van 100 random getallen ? Als we een 'experiment' doen waarbij we 100 random getallen getallen genereren en bij elkaar optellen zal daar gemiddeld 50 uitkomen (omdat het gemiddelde getal 0.5 is), maar voor een individueel experiment is dat zelden precies 50 natuurlijk. De vraag is nou: hoe vaak vind je toevallig dat de som minder is dat 40 ? En komt dat evenveel voor als het aantal experimenten waarbij de som meer dan 60 is ? 

Schrijf een programma `SomRandomGetallen()` dat de distributie weergeeft van 10.000 experimenten. Teken de resultaten tussen x=30 en x = 70.

Genereer voor elk 'experiment' 100 random getallen en reken de som daarvan uit. Herhaal dit 10.000 keer en bewaar voor elk van de experimenten de som in een lijst. Maak uiteindelijk een frequentie-distributie (histogram) van de verdeling. Schrijf ook naar het scherm wat het percentage (in procent) van de  experimenten is waarbij de som respectievelijk minder dan 40 en meer dan 60 is.     



