# gebruik standaard modules



# plotjes maken


http://matplotlib.org/users/pyplot_tutorial.html


![](plotje1.png)

    import matplotlib.pyplot                   # importeer grafiekmaak module
	
    L_x = [0,1,2,3,4,5]                        # definieer lijst met x-waardes van de punten
    L_y = [0,1,4,9,16,25]                      # definieer lijst met y-waardes van de punten
	
    matplotlib.pyplot.plot(L_x, L_y,'go')      # plot punten (y tegen x) met groene rondjes	
	
    matplotlib.pyplot.show()                   # laat de grafiek op het scherm zien

Hierbij is ervoor gekozen om de 'marker' (figuur waarmee elk elk punt weergegeven wordt) weer te geven als een groen puntje. Vandaar het commando `'go'`. Als je een rode lijn had gewild die elk van de punten verbindt dat had je ook voor `'r-'` kunnen kiezen.

Om veel schrijven te voorkomen kan je een lange modulenaam ook intern in je code een kortere naam weergeven.

    import matplotlib.pyplot as plt
	
    L_x = [0,1,2,3,4,5]
    L_y = [0,1,4,9,16,25]
	
    plt.plot(L_x, L_y,'go')

    plt.show()

En natuurlijk behoren de assen labels te hebben, kan je 2 verschillende grafieken in 1 plot zetten en kan je zelf tekst weergeven. Om ook de grafiek x^3 in de grafiek te zetten (met rode lijnen) doe je het volgende:

    import matplotlib.pyplot as plt
	
    L_x  = [0,1,2,3,4,5]
    L_x2 = [0,1,4,9,16,25]
	L_x3 = [0,1,8,27,64,125]
	
	plt.plot(L_x, L_x2,'go', L_x, L_x3,'r-')                                  # plot 2 grafieken tegelijk
	
	plt.xlabel('de x-ax is klein')
	plt.ylabel('de y-as ix groot', fontsize = 25)
	plt.text(1.00,100., "mijn eerste plotje", color = 'blue', fontsize = 20)
	plt.text(4.00,100., "$x^3$", color = 'red', fontsize = 20)

	plt.show()

![](plotje2.png)

Hier hebben we een klein aantal punten gekozen waarbij je de waardes zelf in moet vullen. Je kan ook zelf x-waardes en y-waardes berekenen en in lijsten opslaan. Als we de functie sin(x) willen plotten in stapjes van 0.01 tussen 0 en 2*pi dan knopen we de verschillende dingen die we dit blok geleerd hebben aan elkaar en doen we het volgende:

	import numpy as np					# numpy mdule: nodig voor arange-functie
	import math							# math module: nodig voor sin()-functie
	import matplotlib.pyplot as plt		# pyplot module: nodig voor plotten

	L_x = []
	L_y = []

	for x in np.arange(0,2*math.pi, 0.01):   	# x loopt van 0 tot 2pi in stapjes van 0.01

		y = math.sin(x)    						# bereken de y-waarde: y = sin(x)

		L_x.append(x)							# sla x-waarde op in lijst
		L_y.append(y)							# sla y-waarde op in een lijst

	plt.plot(L_x, L_y,'b-')						# plot x tegen y

	plt.xlabel('x', fontsize = 20)
	plt.ylabel('sin(x)', fontsize = 20)
	plt.text(4.00,0.50, "f(x) = sin(x)", color = 'black', fontsize = 20)

	plt.show()


![](plotje3.png)


