
# Animation

#----------------------
def SimulatieExample():
#----------------------

  fig, ax = plt.subplots()

  L_x = []
  L_y = []

  for t in np.arange(0,2*math.pi,0.01):

      #--/ beginsituatie (startpunt 3 grafieken en afmating grafiek)
      if t == 0:
          points1, = ax.plot(0,0, marker='o', markersize = 10)  
          points2, = ax.plot(0,0, marker='o', markersize = 5)  
          points3, = ax.plot(0,0,lw=2)                        
          ax.set_xlim(0, 2*math.pi)
          ax.set_ylim(-1, 1.)

      #--/ bereken voor elk stapje  in tijd nieuwe x en y en teken ze op het scherm
      else:
          #--/ functie 1: punt met f(x) = sinus(x)
          x1 = t
          y1 = math.sin(t) 

          #--/ functie 2: punt met f(x) = 0
          x2 = t
          y2 = 0 

          #--/ functie 3: lijn met f(x) = 0.5*cos(5x)
          x3 = t
          y3 = 0.5*math.cos(5*t) 
          L_x.append(x3)
          L_y.append(y3)

          #--/ teken de 2 punten van functie 1 en 2 en hele lijst voor functie 3
          points1.set_data(x1,y1)
          points2.set_data(x2,y2)
          points3.set_data(L_x,L_y)
          
      #--/ pauzeer na elk stapje kort
      plt.pause(0.0001)



#=============
# MAIN PROGRAM
#=============

SimulatieExample()



![](collidingballs1.gif)