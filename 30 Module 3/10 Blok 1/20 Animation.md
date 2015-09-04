
# Animation

Hoewel een grafiek zeer inzichtelijk kan zijn om een proces te simuleren is niks 
inzichtelijker een animatie te maken. Python biedt je de mogelijkheid om een 
figuur steeds opnieuw te tekenen. Dat geeft je verschillende mogelijkheden.

### Voorbeeld: bewegend punt (2x)
Als je een punt tekent (1 x-waarde en 1 y-waarde) waarvan je x en y steeds verandert 
dan lijkt het of het punt over het scherm beweegt. In de code hieronder nemen we 
steeds stapjes in x en laten we 2 punten over het scherm bewegen via de functies 
$$f_1(x) = sin(x)$$ (blauwe punt) en $$ f_3(x) = 0$$ (groene punt).

### Voorbeeld: bewegende lijn
Een grafiek tekenen we met behulp van lijsten: een lijst met x-waardes en een lijst 
met y-waardes. Als je die lijsten steeds uitbreidt dan krijg je het onderstaande 
effect: de functie $$f_2(x) = \frac{1}{2}cos(5x) $$ getekend met een rode lijn.

    fig, ax = plt.subplots()

    L_x  = []   # list of x-values
    L_y2 = []   # list of y-values for 1 of the functions

    #--/ kleine stapjes in x
    for x in np.arange(0,math.pi,0.02):

        y1 = math.sin(x)
        y2 = 0.5 * math.cos(5*x)
        y3 = 0
        
        L_x.append(x)
        L_y2.append(y2)

        #--/ plot graphs
        plt.plot(x, y1, 'bo', markersize = 10)            # sin(x), blauwe punt
        plt.plot(L_x, L_y2, 'r-', lw=2, markersize = 15)  #   f(x), rode lijn
        plt.plot(x, y3, 'go')                             #      0, groene punt

        plt.xlim(0,math.pi)
        plt.ylim(-1,1)
        plt.draw()      # Update graph
        plt.pause(0.001)
        plt.clf()       # Clear graph (important)


Hier het uiteindelijke resultaat:
![](AnimationExample.gif)

## Opgave 1: animatie van spiraliserende stip

Een balletje draait met een bepaalde hoeksnelheid rond en met elke stap in de tijd 
verandert niet alleen de hoek, maar wordt ook de straal steeds kleiner tot hij 
uiteindelijk precies in het midden stilstaat

![](AnimationInspiral.gif)


## Opgave 2: random walk

Een dronken student (die natuurlijk geen natuurkunde studeert, want dan lag hij keurig 
vroeg in bed) neemt elke seconde een stap. De grootte van de stap is steeds hetzelfde 
(R = 1), maar de richting waarin hij die stap neemt is volledig random. Kies bij elke 
stap in de tijd een random hoek $$\alpha$$ en bepaald vervolgens de nieuwe x-positie en 
y-positie. Teken niet alleen de student als blauwe stip, maar ook het pad dat hij gevolgd 
heeft.

![](AnimationRandomWalk.gif)

Probeer eens of je (met en en papier) iets kan zeggen over de gemiddelde afstand die de 
student van zijn startpunt verwijderd is na een bepaald aantal stappen.

Filmpje opslaan ? Probeer GifGrabber (app) te gebruiken om een animated gif te maken. Die kan je weer in een webbrowser bekijken.

