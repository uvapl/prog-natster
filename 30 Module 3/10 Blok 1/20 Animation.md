
# Animation

Hoewel een grafiek zeer inzichtelijk kan zijn om een proces te simuleren is niks 
inzichtelijker een animatie te maken. Python biedt je de mogelijkheid om een 
figuur steeds opnieuw te tekenen. Dat geeft je verschillende mogelijkheden om 
een beweging aan te geven. We bouwen hier een kort voorbeeld, waarin we een lijn 
(en punt) volgens $$f(x)=sin(x)$$ over het scherm laten bewegen. We bouwen de 
functie op in 3 stappen waarbij we telkens 1 element toevoegen. Met behulp van 
dezefunctionaliteit een groot scala aan animaties te maken.

## Voorbeeld (stap 1): bewegend punt
Als je een punt tekent (1 x-waarde en 1 y-waarde) waarvan je x en y steeds verandert 
dan lijkt het of het punt over het scherm beweegt. In de code hieronder nemen we 
steeds stapjes in x, rekenen y uit en tekenen het punt op het scherm. We kiezen de 
assen ook zodat het constant hetzelfde is. 

    import math
    import numpy as np
    import matplotlib.pyplot as plt
    
    #-- neem kleine stappen in x tussen 0 en 2pi
    for x in np.arange(0,2*math.pi,0.05):

        y = math.sin(x)

        #-- plot grafiek
        plt.plot(x, y, 'bo', markersize = 10)  #-- blauwe punt
        plt.xlim(0,2*math.pi)
        plt.ylim(-1,1)
        plt.draw()           #-- update grafiek
        plt.pause(0.001)
        plt.clf()            #-- clear grafiek

![](AnimationExampleSin1.gif)


## Voorbeeld (stap 2): bewegende lijn
Een grafiek tekenen we met behulp van lijsten: een lijst met x-waardes en een lijst 
met y-waardes. Als je die lijsten steeds uitbreidt dan krijg je het onderstaande 
effect: de functie $$f(x) = sin(x) $$ getekend met een rode lijn.

    import math
    import numpy as np
    import matplotlib.pyplot as plt
    
    L_x = []
    L_y = []

    #--/ take small steps in x
    for x in np.arange(0,2*math.pi,0.05):

        y = math.sin(x)

        L_x.append(x)
        L_y.append(y)

        #-- plot grafiek
        plt.plot(L_x, L_y, 'r-')            #-- rode lijn
        plt.xlim(0,2*math.pi)
        plt.ylim(-1,1)
        plt.draw()           #-- update grafiek
        plt.pause(0.001)
        plt.clf()            #-- clear grafiek


Zoals je ziet is de code maar op 3 regels anders dan in 
voorbeeld 1. Het resultaat ziet er als volgt uit:

![](AnimationExampleSin2.gif)

## Voorbeeld (stap 3): stip en lijn tegelijk en tekst op het scherm

Je kan de stip en de lijn ook tegelijk tekenen en op het scherm ook 
informatie weergeven over de (x,y) positie van het punt op het scherm.


    import math
    import numpy as np
    import matplotlib.pyplot as plt
    
    L_x = []
    L_y = []

    #--/ take small steps in x
    for x in np.arange(0,2*math.pi,0.05):

        y = math.sin(x)

        L_x.append(x)
        L_y.append(y)

        #-- plot grafiek
        plt.plot(L_x, L_y, 'r-',x, y, 'bo', markersize = 10)  #-- stip en lijn tegelijk
        plt.xlim(0,2*math.pi)
        plt.ylim(-1,1)

        #--/ text op scherm      
        plt.text( 0.25, -0.8, "(%.2f,%.2f)" % (x,y) )  

        plt.draw()           #-- update grafiek
        plt.pause(0.001)
        plt.clf()            #-- clear grafiek



![](AnimationExampleSin3.gif)

## Opgave 1: animatie van spiraliserende stip

Een balletje draait met een bepaalde hoeksnelheid rond en met elke stap in de tijd 
verandert niet alleen de hoek, maar wordt ook de straal steeds kleiner tot hij 
uiteindelijk precies in het midden stilstaat

![](AnimationInspiral.gif)

Op elk moment wordt een punt beschreven door 2 coordinaten (x,y), maar je kan ook 2 
andere variabelen gebruiken ($$\alpha$$,R), waarbij $$\alpha$$ de hoek is met de 
positieve x-as en R de afstand tot de oorsprong. De variabelen kunnen in elkaar omgeschreven 
worden zoals in de grafiek is aangegeven.

![](UitlegPolarCoordinates.png)

Details voor de animatie: 
   - $$\alpha$$ varieert van 0 tot 20 in stappen van 0.1
   - R hangt af van $$\alpha$$, nl: $$R=10-0.5\alpha$$ 


## Opgave 2: dronken studenten

Een dronken student (die natuurlijk geen natuurkunde studeert, want dan lag hij keurig 
vroeg in bed) neemt elke seconde een stap. De grootte van de stap is steeds hetzelfde 
(R = 1), maar de richting waarin hij die stap neemt is volledig random. Kies bij elke 
stap in de tijd een random hoek $$\alpha$$ en bepaald vervolgens de nieuwe x-positie en 
y-positie. Hieronder zie je de student als blauwe stip en het ook het pad dat hij gevolgd 
heeft. Dit staat bekend als een *random walk*.

![](AnimationRandomWalk.gif)

Als 2 studenten dronken zijn en ze elkaar uit het oog verliezen wordt het erg onwaarschijnlijk 
dat ze elkaar nog terugvinden. Probeer de volgende animatie na te maken waarin je de beide studenten 
ziet lopen. Laat op het scherm ook zien hoe lang de kijken nog moet wachten tot het programma 
afgelopen is.

![](AnimationRandomWalkDouble.gif)

Probeer ook eens of je (met en en papier) iets kan zeggen over de gemiddelde afstand die de 
studenten van elkaar verwijderd zijn als functie van het aantal stappen dat ze nemen.

Filmpje opslaan ? Probeer GifGrabber (app) te gebruiken om een animated gif te maken. Die kan je weer in een webbrowser bekijken.

