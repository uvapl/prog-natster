# Kans dat twee willekeurige getallen relatief-priem zijn

Schrijf een programma `priemparen.py` dat de waarschijnlijkheid berekent dat twee willekeurig gekozen grote gehele getallen geen onderlinge deler hebben. Zo'n paar 
noemen we onderling-priem.

    #python priemparen.py
    De kans dat twee random grote getallen geen onderlinge deler hebben is:
        - voorspelling (wiskunde): x.xx %
	    - empirisch (Python): x.xx %

In deze opgave bedoelen we met 'groot' gehele getallen van 10.000 tot 100.000.

### Definitie van onderling-priem en de voorspelling vanuit de wiskunde
	    
Informatie over de definitie en wat eigenschappen van deze paren zijn hier te vinden:
[wikipedia co-primes](https://en.wikipedia.org/wiki/Coprime_integers).

Je kunt lezen dat de kans dat $$n$$ willekeurige getallen géén gemeenschappelijke deler hebben wordt gegeven door:

     $$\frac{1}{\zeta(n)}$$. 

, waarbij $$\zeta(s) $$de beroemde [Riemann zeta functie](https://en.wikipedia.org/wiki/Riemann_zeta_function) is.

**Let op:** in het geval van drie (of meer) of meer getallen betekent dit de kans is dat er geen getal is dat een deler is van alle drie (of meer) getallen *tegelijk*.

Voor twee getallen is die voorspelde kans dus $$1./\zeta(2) \approx 61\%$$ en de bedoeling van deze opgave is dat we zowel de voorspelling narekenen als ook empirisch gaan bekijken of dit inderdaad de juiste frequentie voorspelt.


### stap 1: lijst met priemfactoren

Elk getal is op een unieke manier te schrijven als het produkt van priemgetallen:

     34 = 2 x 17
     88 = 2 x 2 x 2 x 11
     79220  =  [2, 2, 5, 17, 233]

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
