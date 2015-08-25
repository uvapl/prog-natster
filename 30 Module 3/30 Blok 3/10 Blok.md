
# Simulaties

# Opgave 3: de ultieme free-fall

De appel in vraag 1 bereikt na iets meer dan 4 seconden het aardoppervlak. Stel nou 
eens dat precies op de plek waar de appel neervalt een tunnel is gegraven dwars door 
de aarde heen. 

Schrijf een programma `Tunnel.py` die de beweging van de appel door de aarde heen 
beschrijft. Het deeltje beweegt langs de x-as met x=0 in het centrum van de aarde, 
start met snelheid 0 op hoogte 0 meter boven het aardoppervlak. Wat gebeurt er 
precies ?
 
![](EarthHole.png)

### Tips:
   - verwaarloos luchtweerstand in deze opgave
   - de effectieve massa van de aarde, de massa 'die aan je trekt' is
     wordt kleiner naarmate je dichter bij het centrum komt.
     Dus: als de aarde $$M_{\rm aarde}$$ weegt en je 50% van de afstand tot het
     centrum van de aarde hebt afgelegd 'weegt' de aarde in de formule van
     Newton nog maar $$\left(\frac{1}{2}\right)^3M_{\rm aarde}$$.
   - Neem aan dat de aarde een bol met constante dichtheid is.
   
### a) Maak een grafiek van de snelheid van de appel als functie van de tijd

### b) Maak een grafiek van de positie als functie van de tijd

### c) Bereken de maximale snelheid die de appel bereikt

### d) Hoe lang duurt het voor de appel weer terug is op de plek waar je hem losgelaten hebt ?


## Natuurkunde inzicht achteraf

Hoewel dit een ingewikkeld probleem lijkt was het toch mogelijk geweest deze opgave op te lossen met pen en papier. De effectieve kracht die op een deeltje werkt groeit lineair als functie van de afstand tot het middelpunt van de aarde. Als een deeltje vanuit het centrum van de aarde (x=0) naar buiten beweegt (positie x=r) geldt immers:

  - de effectieve gravitatieconstante groeit als $$r^3$$ omdat de effectieve massa van de bol die aan het object trekt groeit met $$r^3$$. Er geldt dus: $$F\propto r^3$$.  

  - de kracht zelf neemt af met $$1/r^2$$ omdat de kracht nou eenmaal omgekeerd evenredig afneemt met het kwadraat van de afstand. Er geldt dus: $$F\propto r^{-2}$$
  
Uiteindelijk zal de kracht op een deeltje dat steeds verder uit het centrum beweegt lineair afnemen met de afstand. Dat is precies dezelfde situatie als een klassieke veer waarvoor de we bewegingsvergelijking wel kennen: de [wet van Hooke](https://nl.wikipedia.org/wiki/Wet_van_Hooke).

  
  
