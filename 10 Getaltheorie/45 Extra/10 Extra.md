# Onderling priem

Schrijf een programma `priemparen.py` dat de waarschijnlijkheid berekent dat twee willekeurig gehele getallen geen gemeenschappelijke deler hebben. Zo'n paar wordt
'onderling-priem' genoemd. De Engelse term is 'coprime'.

    #python priemparen.py
    De kans dat twee random getallen geen onderlinge deler hebben is:
        - voorspelling (wiskunde): x.xx %
	    - empirisch (Python): x.xx %

Hoewel we in deze opdrachten jullie zoveel mogelijk vrij willen laten (er is ook geen `checkpy`) zullen we voor deze eerste extra opdracht nog een aantal tussenstappen aangeven. Volg deze stappen omdat we die nodig hebben bij het nakijken om te kijken hoe ver je bent gekomen.

### Definitie van onderling-priem en voorspelling vanuit getaltheorie
	    
In de informatie over de definitie van deze [wikipedia co-primes](https://en.wikipedia.org/wiki/Coprime_integers) lezen we ook terug wat de kans is dat *n* willekeurige getallen géén gemeenschappelijke deler hebben. Deze wordt gegeven door:

     $$\frac{1}{\zeta(n)}$$. 

, waarbij $$\zeta(s) $$de beroemde [Riemann zeta functie](https://en.wikipedia.org/wiki/Riemann_zeta_function) is.

**Let op:** in het geval van drie (of meer) of meer getallen betekent `gemeenschappelijke deler` dat er een getal is dat *tegelijkertijd* een deler is van *alle* drie (of meer) getallen.

*Twee getallen (n=2)*:
De kans dat twee willekeurige getallen gene gemeenschappelijke deler hebben is: 
$$1./\zeta(2) = \frac{6}{\pi^2} \approx 60,8\%$$.


In deze opdracht gaan we zelf van twee willekeurige getallen bekijken of ze een gemeenschappelijke deler hebben. Door dit een groot aantal keer doen kunnen we de kans bepalen dat twee van zulke getallen onderling-priem zullen zijn.

### stap 1: lijst met priemfactoren

Elk getal is op een unieke manier te schrijven als het product van priemgetallen:

        34 = 2 x 17
        88 = 2 x 2 x 2 x 11
     79220 = 2 x 2 x 5 x 17 x 233

Schrijf een functie `PriemFactoren(getal)` die voor een bepaald getal de lijst met priemfactoren vindt en op het scherm kan printen.

    python> Priemfactoren(79220) 
            Priemfactoren  79220  =  [2, 2, 5, 17, 233]

Zorg ook dat de functie de lijst met priemgetallen als output terugeeft aan de user (in return statement).
 
### stap 2: op zoek naar gemeenschappelijke delers

Schrijf een functie `AantalDelers(n1, n2)` die voor twee getallen aangeeft of er een gemeenschappelijke deler is of niet. Gebruik hierbij de functie `Priemfactoren()` om voor elk getal de priemfactor- lijst te vinden en ga op zoek naar getallen die in beide lijsten voorkomen.

Op dit moment is het niet van belang om het aantal delers te weten. We willen vooral weten als er *géén* gemeenschappelijke deler te vinden is. De functie moet dan als return argument 0 teruggeven.

### stap 3: frequentie testen



*Python tip:* om een willekeurig 



## Testen

Er is voor deze opdracht geen checkpy aanwezig. You're on your own.
