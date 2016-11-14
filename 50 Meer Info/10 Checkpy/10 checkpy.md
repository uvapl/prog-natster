# Testen van je opdrachten

We gebruiken een programma om te checken of je opdrachten op de juiste manier werken. We vragen je om heel precies te zijn in het geven van de juiste uitvoer!

Om zelf het check-programma te downloaden, moeten we een opdracht invoeren in de "Canopy Command Prompt" of "Canopy Terminal". Deze vind je in de Editor, in het menu genaamd "Tools". Je krijgt een apart scherm waar je commando's kunt intikken. Voer het volgende in:

	pip install checkpy

Je kunt nu de command prompt of terminal weer sluiten. Vervolgens ga je in de Canopy Editor naar de Python Pane, waar je Python-commando's in kunt voeren. Eerst `importen` we checkpy:

	import checkpy

En dan downloaden we éénmalig de checks:

	checkpy.download("https://github.com/Jelleas/progNS2016Tests")

Het checken zelf doe je dan als volgt, bijvoorbeeld om het programma `priem100.py` te controleren:

	checkpy.test("priem100")

Ben je klaar met je hele opdracht, check dan nog een keer de hele module:

	checkpy.testModule("module2")

Het check-programma is erg streng. Toch is het echt de bedoeling dat je zorgt dat je programma de check door komt. Mocht je niet begrijpen waarom je antwoord wordt afgekeurd, spreek dan meteen een docent aan tijdens het practicum. We kijken dan met je mee.
