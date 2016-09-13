# Opzet en doel van Module 2

In deze module zullen we een aantal nieuwe concepten behandelen en die gebruiken om een aantal problemen uit de wiskunde en natuurkunde aan te pakken.

  - Numeriek integreren:       
    Hoe berekent een computer een integraal die niet analytisch oplosbaar is ?	We zullen dit op 2 verschillende manieren doen: de Riemannsom (blok 3)en de Monte Carlo methode (blok 4).

Elk van deze onderwerpen is ondergebracht in een aparte module waarin we steeds in een stuk tekst en een korte film het concept uitleggen. Naast de nieuwe wiskunde/natuurkunde concepten zijn er ook twee nieuwe programmeer-functionaliteit die je moet leren gebruiken: 

   - gebruik van functies (Module 1)
   - het printen van reeele getallen
   - gebruik van de `arange()` functie uit de numpy bibliotheek
   - manipuleren en gebruik van *random getallen* (Module 2)
   - Het visualiseren van data met behulp van een frequentie distributie (histogram)

## Inleveren opgaves

Werk alles van vandaag uit in één Python-bestand genaamd **functies.py**.


## [1] Het printen van reele getallen

We hebben geleerd dat je een geheel getal als volgt print:

    x = 100
    print "x heeft de waarde %d" % (x)

Zodra de computer de string naar het scherm print zet hij op de plek waar `%d` staat de waarde die in de variabele *x* opgeslagen staat. In ons geval 100. De vorm `%d` geeft aan dat het een *geheel* getal is.

Vaak is een variabele die je gebruikt helemaal geen geheel getal.

    breuk = 3./17.
    print "breuk = %d" % (breuk)

Als je dit print zal je zien dat, hoewel de variabele `breuk` de waarde 0.176471 heeft, dit programma toch de waarde 0 op het scherm print. Dat komt omdat je met `%d` hebt aangegeven dat je een geheel getal wil afdrukken. In Python worden dan de cijfers achter de komma simpelweg afgekapt.

Als je wilt dat de computer een reeel getal, een `float` in computertaal, print op het scherm, dan geef je dat aan met het `%f` karakter.

    breuk = 3./17.
    print "breuk = %f" % (breuk)

Nu zal wel de volledige waarde geprint worden op het scherm. In veel toepassingen wil je vaak maar een beperkt aantal decimalen weergeven. Als je 2 getallen achter de komma wilt aangeven dan gebruik je de volgende syntax:

    breuk = 3./17.
    print "breuk = %.2f" % (breuk)

Probeer een aantal opties. Net als bij het printen kan het ook misgaan als reele getallen en gehele getallen gemixt worden in je programma zelf. Lees zeker het onderstaande stukje over een van de bekende valkuilen en de manier waarop je die kan omzeilen.

### Bekende valkuil: mix van gehele en reele getallen

Een veel voorkomende fout die gemaakt wordt in programma's is dat een computer denkt dat elke bewerking van gehele getallen zelf ook weer een geheel getal is. Het volgende programma zal aan de variabele z de waarde 1 toekennen, het eerste gehele getal onder de 1.3333. En dat is natuurlijk niet wat je bedoelde.

    x = 4
    y = 3
    z = x/y
    print z

Zodra een van de getallen in de wiskundige operatie een reeel getal is zal het resultaat ook een reeel getal zijn. De manier om de variabele z de waarde 1.3333 te geven is een van de variabelen (x of y of beide) een reeel getal te maken. De 2 meest gebruikte manieren om dat te doen:

Oplossing 1:

    x = 4.0
    y = 3
    z = x/y
    print z

Oplossing 2:

    x = float(4)
    y = 3
    z = x/y
    print z


## [2] Een rij reele getallen met behulp van numpy.arange()

In Module 1 hebben we de for-loop gebruikt om een variabele steeds met 1 op te hogen. In de for-loop constructie gebruikten we daarvoor de `range()` functie. De getallen 1 tot (en niet tot en met) 10, printen op het scherm, ze in een lijst stoppen en die printen aan het eind van het programma deden we als volgt.

    L_x = []
    for x in range(1,10):
	   print "x heeft nu de waarde %d" % (x)
	   L_x.append(x)
	print L_x


In Module 1 hebben we tijdens het tekenen van onze grafieken gezien hoe we punten (een lijst met x-waardes en een lijst met y-waardes) op het scherm kunnen tekenen. Om een functie te tekenen met een hoge precisie, in ons geval sin(x) leerden we dat we als we de functie wilde tekenen tussen 0 en 2pi we kleine stapjes, stel 0.01 moeten nemen. In Python is er een standaard functie die dat voor je kan doen, de `arange()` functie. Het is een functie die opgenomen is in de numpy bibliotheek.

    import numpy as np               # numpy mdule: nodig voor arange-functie
    import math                      # math module: nodig voor sin()-functie
    L_x = []
    L_y = []
    
    for x in np.arange(0,2*math.pi, 0.01):  # x loopt van 0 tot 2pi in stapjes van 0.01
        y = math.sin(x)
        L_x.append(x)
        L_y.append(y)		  

Als je bijvoorbeeld de getallen van 2 tot 3 op het scherm wilt printen in stapjes van 0.02 dan kan doe je dat als volgt:

    import numpy as np
	x_begin = 2
	x_eind = 3
    dx = 0.02
	for x in np.arange(x_begin, x_eind, dx):
	    print x
		  
### Bekende valkuil: subtiel verschil tussen 'tot' en 'tot en met'

In het laatste voorbeeld zal het getal 2.0 wel, maar het getal 3.0 niet op het scherm geprint worden. In een van de opgaves zal je wel degelijk het eindpunt moeten gebruiken. Let daarop. Probeer bovenstaande voorbeeld iets aan te passen zodat het eindpunt wel degelijk geprint wordt 		  
		 
# Functies

Bij het programmeren zal je vaak merken je een stuk code kan (of moet) hergebruiken. Zo'n stuk code kan je in een apart stuk van je programma onderbrengen als aparte entiteit (dat noemen we een *functie*). De 'echte' code wordt zo een stuk overzichtelijker en je kan dat aparte stukje functionaliteit ook gebruiken in andere programma's die je gaat schrijven. Een aantal functies die we al zijn tegengekomen zijn bijvoorbeeld de functie die de sinus van een getal berekent: de `sin()`-functie die in de wiskunde bibliotheek is ondergebracht: `math.sin()`. Zulke functies kan je zelf ook schrijven en zullen we in de opgaves vandaag gaan doen.

In je hoofdcode kun je een functie vervolgens vragen een opdracht uit te voeren. Een functie heeft altijd een input (de variabelen waar hij iets mee moet doen) en een output (het resultaat van het werk). De manier waarop je een functie definieert en input en output manipuleert worden duidelijk in onderstaande voorbeeld.

## [voorbeeld 1]: kwadraten berekenen

Als je van de getallen van 1 tot en met 20 de getallen zelf en hun kwadraten op het scherm wilt printen kan je gebruik maken van de standaard functie uit de wiskunde bibliotheek die kan machtsverheffen `pow()`:

    import math

    for x in range(1,21):
        x_kwadraat = math.pow(x,2) 
        print " %d in het kwadraat = %d" % (x, x_kwadraat) 

Je kan zo'n functie ook zelf schrijven natuurlijk. We zullen die `MijnKwadraatFunctie()` noemen. De functie heeft 1 input (het getal zelf) en 1 output (het getal in het kwadraat).   

    def MijnKwadraatFunctie(getal):
        antwoord = getal * getal
        return antwoord

    # hier begint het hoofdprogramma
    for x in range(1,21):
        x_kwadraat = MijnKwadraatFunctie(x) 
        print " %d in het kwadraat = %d" % (x, x_kwadraat) 

Eerst komt dus de definitie van de functie en zijn naam. Tussen de haakjes geef je aan welke variabelen er als input beschikbaar zijn. In dit geval de variabale `getal` waarna je het antwoord uitrekent. Dit antwoord, ook een getal, wordt vervolgens 'teruggegeven' aan de gebruiker die er vervolgens in de hoofdcode weer verder mee kan werken. In dit geval wordt het antwoord van de functie in de hoofdcode in een variabele (`x_kwadraat`) gestopt en vervolgens op het scherm geprint.

Belangrijk om hier op te merken is ook dat de naam van de variabelen in de functie zelf helemaal losstaat van de waarde en de naam van variabelen in de hoofdcode zelf. In de functie zelf weet het programma bijvoorbeeld niet wat `x` is. Het is een gesloten wereld en je kan in de functie alleen werken met de variabele `getal`. 

Bestudeer dit voorbeeld goed en probeer zelf de naam en functionaliteit te veranderen zodat het bijvoorbeeld de derdemacht van het getal uitrekent. In dit geval lijkt het een beetje overbodig om een aparte functie te maken voor een simpele opdracht, maar je zal al snel merken dat sommige stukken code die je in een functie onderbrengt al snel vrij groot kunnen worden.

## [voorbeeld  2]: meerder input variabelen

Je kan ook meerdere input-variabelen meegeven. Dit is bijvoorbeeld een functie die het grootste getal bepaald aan de hand van 2 getallen die meegegeven worden aan de functie. Dus 2 input variabelen en 1 output.

    def GrootsteGetal(a,b):
        grootste = 0
        if a > b:
           grootste = a
        else:
           grootste = b
        return grootste


    # hier begint het programma
    getal_1 = 126
    getal_2 = 14
    largest_number =  GrootsteGetal(getal_1, getal_2)
    print "het grootste getal = %d" % (largest_number)    


## [voorbeeld 3]: lijsten als input en output

Je kan meerdere variabelen meegeven als aparte waardes zoals hierboven, maar je kan ze ook in een lijst meegeven. Daarnaast is de uitkomst van een functie niet altijd 1 enkel getal, maar kan net zo goed een rij getallen zijn of een meer complex object.

In het onderstaande voorbeeld wordt in de hoofdcode een lijst met x-waardes geproduceerd waarna een functie gevraagd wordt alle bijbehorende y-waardes uit te rekenen (volgens de functie $$f(x)= 8x^2-5x+9$$) en in een lijst te stoppen zodat het op het scherm geplot kan worden.

    import matplotlib.pyplot as plt

    def MijnPolynoom(L_x):
        L_y = []
        for x in L_x:
            y = 8 * x * x - 5 * x + 9
            L_y.append(y)
        return L_y
 

    # hier begint het programma
    L_xwaardes = [1, 2, 3, 4, 5, 6]
    L_ywaardes = MijnPolynoom(L_xwaardes)

    plt.plot(L_xwaardes, L_ywaardes, 'g-')
    plt.show()
 

## Opgave: nulpunten vinden van een tweedegraads-polynoom en plotten

Schrijf een programma dat een functie van de vorm $$f(x)=ax^2+bx+c$$ op het scherm plot en ook de nulpunten vindt. Het vinden van de nulpunten  (de x-waardes waarvoor geldt $$f(x)=0$$) moet in een aparte functie `Nulpunten(a,b,c)` gebeuren die als input de parameters van de polynoom meekrijgt en de 2 nulpunten in een lijst teruggeeft. Bereken de nulpunten m.b.v. de abc-formule.

Roep de functie aan met de waarden $$a = 1$$, $$b = 2$$ en $$c = -10$$. Die polynoom heeft namelijk twee nulpunten.

Breid je functie nu uit zodat je functie ook raad weet met polynomen die helemaal geen nulpunten hebben. In dat geval moet je nog steeds de functie op het scherm printen, maar moet er op het scherm netjes verschijnen dat deze polynoom geen nulpunten heeft.

Extra: als je nog tijd over hebt kan je misschien de figuur 'mooi' te maken. Probeer bijvoorbeeld de polynoom zelf en de nulpunten duidelijk weer te geven op het scherm zoals in de figuur hieronder.


![](PolynoomAnalyse.png)


## Sanity check

Let op dat je alleen de volgende Python-onderdelen hebt gebruikt in je oplossingen:

- alle onderdelen van module 1
- `math.pow()`
- `def`
- `return`
- `elif` (find out what you can do with that!)

Let op! Andere functies van `math` en `numpy` mag je (nog) niet gebruiken!
