# Animaties

Hoewel een grafiek heel handig kan zijn om een simulatie te visualiseren is het soms inzichtelijker een animatie te maken. Python biedt je de mogelijkheid om een figuur snel opnieuw te tekenen. We bouwen hier een kort voorbeeld, waarin we een lijn (en een punt) volgens $$f(x)=sin(x)$$ over het scherm laten bewegen. Met behulp van deze functionaliteit kun je een groot scala aan animaties maken.

## Een bewegend punt

Als je een punt tekent waarvan je $$x$$ en $$y$$ steeds verandert dan lijkt het of het punt over het scherm beweegt. In de code hieronder nemen we steeds stapjes in $$x$$, rekenen $$y$$ uit en tekenen het punt op het scherm.

    import math
    import numpy as np
    import matplotlib.pyplot as plt
    
    # neem kleine stappen in x tussen 0 en 2pi
    for x in np.arange(0,2 * math.pi, 0.05):

        y = math.sin(x)

        # plot grafiek
        plt.plot(x, y, 'bo', markersize = 10)  # blauwe punt
        plt.xlim(0,2 * math.pi)
        plt.ylim(-1, 1)
		
		# update grafiek
        plt.draw()
        plt.pause(0.001)
		
		# clear grafiek
        plt.clf()

![](AnimationExampleSin1.gif)

Normaal kiest `pyplot` zelf een geschikt assenstelsel om alle punten in een grafiek weer te geven. Maar nu hebben we dus een punt dat steeds op een andere plek staat. Om te zorgen dat het beeld mooi statisch blijft, en de punt beweegt, kiezen we daarom met `xlim` en `ylim` welke $$x$$-waardes en $$y$$-waardes we willen zien.

Je ziet dat we in de code de functie `pause()` aanroepen. Dat doen we om `pyplot` de gelegenheid te geven de nieuwe figuur op het scherm te tekenen. Dit wordt alleen gedaan tijdens de pauzes die we geven.

## Een bewegende lijn

Een grafiek tekenen we met behulp van lijsten: een lijst met $$x$$-waardes en een lijst met $$y$$-waardes. Als je die lijsten per stap uitbreidt dan krijg je een mooi effect waarin de grafiek langzaam wordt opgebouwd.

    import math
    import numpy as np
    import matplotlib.pyplot as plt
    
    L_x = []
    L_y = []

    # neem kleine stappen in x tussen 0 en 2pi
    for x in np.arange(0,2 * math.pi, 0.05):

        y = math.sin(x)
        L_x.append(x)
        L_y.append(y)

		# rode lijn
        plt.plot(L_x, L_y, 'r-')
        plt.xlim(0,2 * math.pi)
        plt.ylim(-1, s1)
		
		# update grafiek
        plt.draw()
        plt.pause(0.001)
		
		# clear grafiek
        plt.clf()


Zoals je ziet is de code maar drie regels veranderd ten opzichte van voorbeeld
1. Het resultaat ziet er als volgt uit:

![](AnimationExampleSin2.gif)

## Een stip, een lijn en tekst op het scherm

Je kan de stip en de lijn ook tegelijk tekenen en op het scherm door de opdrachten te combineren. Bovendien voegen we hieronder informatie toe over de $$(x,y)$$ positie van het punt op het scherm.

    import math
    import numpy as np
    import matplotlib.pyplot as plt
    
    L_x = []
    L_y = []

    # neem kleine stappen in x tussen 0 en 2pi
    for x in np.arange(0,2*math.pi,0.05):

        y = math.sin(x)

        L_x.append(x)
        L_y.append(y)

		# rode lijn
        plt.plot(L_x, L_y, 'r-')

		# blauwe stip
        plt.plot(x, y, 'bo', markersize = 10)
        plt.xlim(0,2 * math.pi)
        plt.ylim(-1,1)

        # text op scherm      
        plt.text( 0.25, -0.8, "(%.2f,%.2f)" % (x,y) )

        plt.draw()
        plt.pause(0.001)
        plt.clf()

![](AnimationExampleSin3.gif)

