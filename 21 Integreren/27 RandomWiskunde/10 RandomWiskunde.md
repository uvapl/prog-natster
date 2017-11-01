# Interessant feitje over de som van random getallen 

Schrijf een functie die het gemiddeld aantal random getallen (uniform verdeeld tussen 0 en 1) dat je moet trekken om te zorgen dat de som van die random getallen groter is dan 1.00.

Gebruik de volgende strategie:

  - Genereer steeds random getallen, hou de som bij en stop zodra de som van de random getallen groter is dan 1.
  
  - Doe dit bovenstaande een groot aantal keer (N = 1 miljoen) 

  - Bepaal het gemiddeld aantal benodigde worpen en print dat naar het scherm
  
## Specificatie

- Maak een nieuw bestand genaamd `randomwiskunde.py`.

- Definieer in dit bestand een functie `randomwiskunde()` die geen parameters accepteert en die het gemiddeld aantal worpen bepaalt dat nodig is om random getallen te trekken waarvan de som groter is dan 1.000.

  De output op het scherm (op 4 decimalen nauwkeurig) is als volgt:

	Het gemidddeld aantal worpen (op basis van 1 miljoen trials) is: x.xxxx 
		

## Testen

	checkpy randomwiskunde.py