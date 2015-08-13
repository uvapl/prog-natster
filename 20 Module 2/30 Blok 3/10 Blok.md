# Numeriek integreren [Monte Carlo methode]

Benader de integraal door gebruik te maken van random getallen. Gooi in een gebied (van bekende grootte) rond de integratie regio random punten en kijk welke fractie binnen het integratiegebied valt.

### a) Het probleem: 
Gegeven $$f(x)$$ op $$a \leq x \leq b$$, bereken $$\int_a^b f(x)~dx$$

### b) De oplossingsstrategie

Stap 1) Definieer een gebied (vaak een rechthoek) dat het de integraalregio omsluit: definieer $$x_{min}$$, $$x_{max}$$, $$y_{min}$$ en $$y_{max}$$ zodanig dat geldt dat $$x_{min} \leq a$$ en $$x_{max} \geq b$$ en dat:

$$
   \mbox{ voor } a \leq x \leq b \mbox{ : } y_{min} \leq f(x)  \leq y_{max}
$$

Note: in de meeste toepassingen wordt gekozen voor $$x_{min} = a$$ en $$x_{max} = b$$.

Stap 2) Gooi een groot aantal random punten $$(x_i, y_i)$$ in het rechthoek dat het integratiegebied om sluit en bekijk voor elk punt of het binnen het integratiegebied valt ('goed') of erbuiten ('fout'). Hou bij welke fratie van de punten in het integratiegebied vald: $$f_{goed}$$.

Stap 3) Bepaal de integraal

De integraal is de fractie punten die binnen de grafiek vallen keer de oppervlakte van de totale box. 
In ons geval (rechthoek als box) geldt dan:
$$
    \int_a^b f(x)~dx = f_{goed}~~ (x_{max}-x_{min})(y_{max}-y_{min})
$$

### Extra informatie:

In 'echte' toepassingen wordt voor effici$$\"{e}$$ntie maximalisatie de box zo gekozen dat hij de integraal zo nauw mogelijk omsluit: grootste fractie 'goede' worpen.



