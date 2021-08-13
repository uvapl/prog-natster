# Functies

Een *functie* is een stukje code waar je een naam aan geeft, zodat het hergebruikt kan worden. Een
functie die je eerder al gebruikt hebt is `len()`, om de lengte van een lijst op te vragen. En denk
aan de functies `arange()`, `plot()`, enzovoort.

Je kunt ook zelf functies definiëren. Als je bijvoorbeeld een stuk code hebt geschreven om data
mooi te plotten, wil je niet telkens opnieuw de hele code kopiëren als je nieuwe data hebt.

Functies zijn dus een belangrijk aspect van leren programmeren. Het begin van een functie wordt
aangegeven met `def`, daarna komt de functienaam (die je zelf mag kiezen), en vervolgens komen de
haakjes met daartussen mogelijke parameters:

    def print_groet():
        print("Hallo")

Dit is een functie die de string `Hallo` naar je terminal print. Als je bovenstaande *definitie* in
een Python-bestand zet weet de computer dat er nu een functie is met de naam `print_groet()`. Maar
de functie is nog niet *uitgevoerd*! Dit moet je zelf nog doen door de functie expliciet *aan te
roepen*. Dit doe je zo:

    print_groet()

## Functies met één parameter

![embed](https://api.eu.kaltura.com/p/120/sp/12000/embedIframeJs/uiconf_id/23449960/partner_id/120?iframeembed=true&playerId=kaltura_player&entry_id=0_hkab4t85&flashvars[streamerType]=auto&amp;flashvars[localizationCode]=en_US&amp;flashvars[leadWithHTML5]=true&amp;flashvars[sideBarContainer.plugin]=true&amp;flashvars[sideBarContainer.position]=left&amp;flashvars[sideBarContainer.clickToClose]=true&amp;flashvars[chapters.plugin]=true&amp;flashvars[chapters.layout]=vertical&amp;flashvars[chapters.thumbnailRotator]=false&amp;flashvars[streamSelector.plugin]=true&amp;flashvars[EmbedPlayer.SpinnerTarget]=videoHolder&amp;flashvars[dualScreen.plugin]=true&amp;flashvars[hotspots.plugin]=1&amp;flashvars[Kaltura.addCrossoriginToIframe]=true&amp;&wid=0_1czpky81)

## Functies met meer parameters

![embed](https://api.eu.kaltura.com/p/120/sp/12000/embedIframeJs/uiconf_id/23449960/partner_id/120?iframeembed=true&playerId=kaltura_player&entry_id=0_747kicts&flashvars[streamerType]=auto&amp;flashvars[localizationCode]=en_US&amp;flashvars[leadWithHTML5]=true&amp;flashvars[sideBarContainer.plugin]=true&amp;flashvars[sideBarContainer.position]=left&amp;flashvars[sideBarContainer.clickToClose]=true&amp;flashvars[chapters.plugin]=true&amp;flashvars[chapters.layout]=vertical&amp;flashvars[chapters.thumbnailRotator]=false&amp;flashvars[streamSelector.plugin]=true&amp;flashvars[EmbedPlayer.SpinnerTarget]=videoHolder&amp;flashvars[dualScreen.plugin]=true&amp;flashvars[hotspots.plugin]=1&amp;flashvars[Kaltura.addCrossoriginToIframe]=true&amp;&wid=0_s2jo0x4e)

## Functies met lijsten

![embed](https://api.eu.kaltura.com/p/120/sp/12000/embedIframeJs/uiconf_id/23449960/partner_id/120?iframeembed=true&playerId=kaltura_player&entry_id=0_0ip27jrj&flashvars[streamerType]=auto&amp;flashvars[localizationCode]=en_US&amp;flashvars[leadWithHTML5]=true&amp;flashvars[sideBarContainer.plugin]=true&amp;flashvars[sideBarContainer.position]=left&amp;flashvars[sideBarContainer.clickToClose]=true&amp;flashvars[chapters.plugin]=true&amp;flashvars[chapters.layout]=vertical&amp;flashvars[chapters.thumbnailRotator]=false&amp;flashvars[streamSelector.plugin]=true&amp;flashvars[EmbedPlayer.SpinnerTarget]=videoHolder&amp;flashvars[dualScreen.plugin]=true&amp;flashvars[hotspots.plugin]=1&amp;flashvars[Kaltura.addCrossoriginToIframe]=true&amp;&wid=0_t31b8uqq)

## Stijl en ontwerp

Het gebruik van functies bevordert de leesbaarheid van je code. Met goed gekozen namen voor deze
functies kun je snel een overzicht krijgen van wat het geheel doet. Je leest dan bijvoorbeeld eerst
alleen even snel de functienamen in een programma.

Functies kunnen ook een oplossing zijn als je vaak ongeveer het zelfde stukje code schrijft. Mocht
je nou jezelf betrappen op code kopiëren en plakken, probeer dan een manier te verzinnen hoe je de
code efficiënt kan hergebruiken! Gebruik dan een loop of een functie.
