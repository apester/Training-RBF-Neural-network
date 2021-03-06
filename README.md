## Training-RBF-neural-network
using ES algorithm to train RBF network and implement regression and classification on dataset


in this project python DEAP library has been used in order to get access to Evolution Strategy algorithm
and the fitness of evolutionary algorithm has been calculated using the RBF network.

the activation function of the network(G), guessed output(guessedY), weights' matrix(W) and finally the loss which is
our fitness have been calculated and modified during the algorithm. ( relations available in the definition.pdf file )

the chromosomes(individuals) include gamma parameter (we know that the radial of the clusters is equal to 1/(gamma^1/2)) + cluster centers. each individual with the length of numOfClusters * (dimension+1) 

### for regression we have:
* X(our data) = n * d 
* Y = n * 1
* W = m * 1 (m = numOfClusters)
* G = n * m

#### the output of regdata2000 dataset:
iterations = 10

clusters = 10

* training mode:
error = 0.015
<img src = "images/reg.jpg" width = "550">

* testing mode:
error = 0.026
<img src = "images/regt.jpg" width = "550">

### for classification we have:
* X(data) = n * d
* Y = n * c
* W = m * c (m = numOfClusters)
* G = n * m

#### the output of 5clstest5000 dataset:
#### note that the wrong classified data is orange and the centers of clusters are green
iterations = 8

clusters = 10

* training mode:
accuracy = 96.5 %
<img src = "images/5clstest.jpg" width = "550">

* testing mode:
accuracy = 96.2 %
<img src = "images/5clstrain.jpg" width = "550">

