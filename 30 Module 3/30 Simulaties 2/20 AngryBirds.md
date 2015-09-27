# Opgave 4: Angry Birds

We bekijken een situatie zoals in het plaatje hieronder getekend waarbij 
een object wordt weggeschoten vanaf de positie (x=0, y=20) met snelheid 
$v$ onder een hoek ($\alpha$). Net als in de vorige opgaves zal de kogel 
onder invloed van de zwaartekracht gaan bewegen.

![](AngryBirdOverview.png)

Als de bal de grond raakt zal hij terugstuiteren en weer omhoog bewegen. 
Naast de grond is er nog een object dat de beweging van de bak kan beinvloeden: 
een balk. De balk bevindt zich op een hoogte $$y_{balk}=20$$ en strekt zich 
uit van $$10 < x_{balk} < 20$$. En, let op, er zit een gat in de balk, 
namelijk: $$ 12 < x_{gat} < 14$$.

Schrijf een programma `AngryBirds.py` die bestudeert welke hoeken zorgen 
dat de weggeschoten kogel door het gat heen gaat als het met $v=16$ [m/s] 
wordt weggeschoten. Varieer hierbij de hoek $\alpha$ tussen -88 en +88 
graden in stapjes van 2 graden 
 
Probeer ook deze opdracht in kleine stapjes aan te pakken:

   - Maak eerst een functie dat de beweging van het kogeltje laat zien 
op het scherm met behulp van een animatie. Zorg dat deze functie als
input variabelen de snelheid en hoek mee kan krijgen. vergeet hierbij 
de balk.

   - vergeet de balk, maar kijk of je kan bepalen of de kogel door de lijn y=15
heengaat ergens tussen x=12 en x=14.

   - voeg de balk toe en zorg dat de functie een return-value geeft die laat 
zien of de kogel wel/niet door het gat is gegaan.

   - Zorg dat je bij aanroep van de functie kan kiezen of je wel/niet de animatie 
     op et scherm tekent. Dat tekene duurt erg lang en wil je niet altijd doen.
    
   - Varieer de hoeken en maak een grafiek waarbij duidelijk wordt welke 
     hoeken wel/niet zorgen dat de kogel door het gat gaat


## Extra (optioneel):

De standaard manier om de positie van de kogel te tekenen die we in deze cursus 
geleerd hebben is de volgende:

    plt.plot(x_kogel, y_kogel, 'bo')  

het is natuurlik veel leuker om in plaats van een stipje een plaatje van een 
vogel te laten rondvliegen. Je hebt daar de volgende constructie voor nodig. 
Het stuk `plt.imshow` tekent het plaatje op het scherm. Je moet hierbij duidelijk 
het gebied aangeven waar het plaatje afgebeeld wordt. Hier is gekozen als 
positie die van de kogel en een afmeting van 0.5 in x en 2.0 in y.

    import matplotlib.image as image

    im = image.imread('/Users/ivo/Desktop/AngryBirdsLogo.png')
    plt.imshow(im, aspect='auto', extent=(x_kogel, x_kogel+0.5, y_kogel, y_kogel+2), zorder=-1)

![](AngryBirdLogo.png)



