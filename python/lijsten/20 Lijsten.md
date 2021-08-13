# Lijsten

Lijsten in Python zijn handig om data te groeperen en vervolgens als geheel te verwerken. Zo kun je berekeningen niet alleen maar op bijvoorbeeld losse getallen toepassen (is dit specifieke getal een priemgetal?) maar ook op hele verzamelingen. In de video uitleg over simpele toepassingen.

![embed](https://api.eu.kaltura.com/p/120/sp/12000/embedIframeJs/uiconf_id/23449960/partner_id/120?iframeembed=true&playerId=kaltura_player&entry_id=0_62lftli0&flashvars[streamerType]=auto&amp;flashvars[localizationCode]=en_US&amp;flashvars[leadWithHTML5]=true&amp;flashvars[sideBarContainer.plugin]=true&amp;flashvars[sideBarContainer.position]=left&amp;flashvars[sideBarContainer.clickToClose]=true&amp;flashvars[chapters.plugin]=true&amp;flashvars[chapters.layout]=vertical&amp;flashvars[chapters.thumbnailRotator]=false&amp;flashvars[streamSelector.plugin]=true&amp;flashvars[EmbedPlayer.SpinnerTarget]=videoHolder&amp;flashvars[dualScreen.plugin]=true&amp;flashvars[hotspots.plugin]=1&amp;flashvars[Kaltura.addCrossoriginToIframe]=true&amp;&wid=0_1xzx48gp)

## Naslag

Het maken van een nieuwe lijst:

    docenten = ["Martijn", "Ivo", "Jelle", "Maarten", "Huub", "Marianne"]

Het opvragen van één element:

    docenten[2] # geeft "Jelle" en niet "Ivo"!

Het aanpassen van een element:

    docenten[3] = "Vera"

Een element toevoegen aan het einde van een lijst:

    docenten.append("Tom")

En loopen met een lijst:

    metingen_science_park = [12.7, 18.8, 24.9, 14.5, 19.0]
    metingen_science_park.append(20.5)
    for meting in metingen_science_park:
        print("de meting was", meting, "graden")
