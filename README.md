# Python-Polar-Plot

#### Data
    minTrainCost = [0.0036 0.0173 0.0073 0.008  0.0081 0.004  0.0091]
    minTrainCostTime = [6.90675478 6.90675478 4.30406509 4.51085951 4.57471098 4.75359019
     4.90527478]

#### Plot
    N=7
    ind = np.arange(N)
    ## Train
    plt.figure(figsize=(5,5))
    ax = plt.axes([0,0,1,1],polar=True)
    ax.grid(alpha=0.5)  
    plt.setp(ax.yaxis.get_ticklabels(), visible=False) 
    N     = 7
    theta = np.arange(0, N)
    radii = np.array(minTrainCost)
    width = np.pi/20*np.array(minTrainCostTime)
    plt.bar(theta, radii,  width=width, color=['brown','red','green','blue','pink','yellow','purple'], edgecolor='black', linewidth=1.5, alpha=0.7)
    plt.xticks(ind, ('Constant', 'AdaGrad', 'AdaDelta', 'RMSprop', 'Adam','Cyclical','Energy'))
