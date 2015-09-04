
# Animation

Hoewel een grafiek zeer inzichtelijk kan zijn om een proces te simuleren is niks 
inzichtelijker een animatie te maken 


    fig, ax = plt.subplots()

    L_x  = []   # list of x-values
    y1   = 0    
    L_y2 = []   

    #--/ take small steps in x
    for x in np.arange(0,math.pi,0.02):

        y1 = math.sin(x)
        y2 = 0.5 * math.cos(5*x)
        L_x.append(x)
        L_y2.append(y2)

        #--/ plot graphs
        plt.plot(x, y1, 'bo', markersize = 10)            # sin(x), blauwe punt
        plt.plot(L_x, L_y2, 'r-', lw=2, markersize = 15)  #   f(x), rode lijn
        plt.plot(x, 0, 'go')                              #      0, groene punt

        plt.xlim(0,math.pi)
        plt.ylim(-1,1)
        plt.draw()      # Update graph
        plt.pause(0.001)
        plt.clf()       # Clear graph (important)


Hier het uiteindelijke resultaat:
![](AnimationExample.gif)