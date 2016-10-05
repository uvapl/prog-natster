## Extra inzicht (niet voor inleveren)

Het fitten van een model aan metingen is een standaard procedure die je als onderzoeker vaak tegen zult komen. Hoewel we in deze cursus deze functionaliteit en alle bijbehorende details zullen gebruiken door gebrek aan tijd willen we hier toch een klein voorbeeld geven waarin je ziet hoe dat in de praktijk gaat. 

Hieronder dezelfde fit die jullie hierboven gedaan hebben, maar dan op de Python-manier.

    # import the module that contains the fit-tool
    from scipy.optimize import curve_fit

    # Define our model. In our case a constant function: f(x) = a 
    def MyFitFunction(x, a):
        return a

    # define data and errors
    L_data_x       = [1,2,3,4,5,6,7,8,9,10]
    L_data_y       = [55,50,39,58,54,57,78,66,62,82]
    L_data_y_error = [5,4,9,4,5,5,7,3,6,6]

    # do fit (using our own function f(x) = a)
    popt, pcov = curve_fit(MyFitFunction, L_data_x, L_data_y, None, L_data_y_error)
    print "Best value: f(x) = %5.2f" % popt[0]

De laatste regel blijft nu nog magie, maar *popt* is een lijst met de 'optimale' parameters van de functie die je aan de data hebt gefit. In ons geval is dat maar 1 parameter omdat we een constante functie aanhouden als model. Je kan zelf in de documentatie opzoeken hoe je zelf uit *pcov* de onzekerheid op de parameter kan bepalen. 

Als je nu in plaats van een constante functie een lineaire functie wilt fitten $$f(x) = ax+b$$ en je wilt de resultaten printen dan hoef je op 2 plekken een  verandering aan te brengen:

1. verander de functie die je aanhoudt als model

	    # Define our model. In our case a constant function: f(x) = a x + b 
	    def MyFitFunction(x, a, b):
	        return a * x + b

2. verander de regel waarin je het resultaat op het scherm print

	    print "Best value: f(x) = %5.2f * x + %5.2f" % (popt[0], popt[1])
