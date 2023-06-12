# Project4
Project4- Jessica Tabak, Holly Martin, Caleb Thornsbury, Vanat Tham


##-Caleb##

My part of this project was to help us decide what models to use and then tune the parameters to create models with the best accuracy for this dataset. 


After looking at the original Random Forest Classifier that was brought up by Holly, I was tasked to try and see if we could tune the parameters to increase our accuracy. 
Doing a quick google search I was able to find that there are multiple ways to tune a model, which can help improve the accuracy. One of the simplest ways I found to tune the
parameters of a random forest classifier was by increasing the max features parameters. The one max feature parameter I decided to include in the revised version of the random 
forest classifier is called n_estimators. Now, with every change in parameters you make to a code some downsides follow, but with n_estimators the only downside was increased 
running time of the model. What this feature does is change the max number of trees created before taking the average, looking at the picture in the back you can see that by simply 
increasing the number of trees in a model that can improve the accuracy. We changed the numbers of trees to 500 which got our accuracy to go from the 71% that Holly observed to 85% 
from the improved model. 

My next part in the project was to create an auto-optimized Neural Network model, this was auto-optimized to find the best parameters that also gave the best accuracy for the model.
To do this I took what we learned in class for auto-optimization and then changed the units and activations for the layers to be more in tune with what we wanted from the model. I 
ended up deciding to have 2 hidden layers, one with units from 10 to 1000 and activation of ReLU. ReLU stands for Rectified Linear Unit(s) and its basic function is to introduce the 
property of non-linearity to a deep learning model. What that means is that any negative number put into the equations will result in 0 and every positive number gets returned as what
was entered. Looking at the fist picture in the top middle left you can see that the ReLU function is linear acting, which makes it the easiest type of function to optimize in neural 
networks. For the second hidden layer I had units from 10 to 100 with the activation of tanh. Looking into the tanh activation its short for Hyperbolic Tangent Function, the picture on 
the far right is a graph of the tang function, this function is important for Neural Networks because it helps with the backpropagation process. Backpropagation involves taking the error 
rate of a forward propagation and feeding this loss backward through the neural network layers to fine-tune the weights. This process happens in the changing of epochs during the running of  
Neural Network models to create better models vs the previous. It is also a good function to be used for multi-layer processes because it delivers better training performance. When creating 
the auto-optimization code we also coded to have the RMSE calculated. RMSE Is the Root Mean Standard Error, this calculation is important because it shows the accuracy between the trained d
ata and the test data entered into the model, a good RMSE score falls between .2 and .5.The model was also coded to run a total of 10 trials. Looking at the data from the 10 trials it can be 
seen that the best RMSE was found to be .394 which was trial 7/10. This trial also had 200 units, which is saying that the best Neural Network model for this dataset needs to include 200 units 
between the hidden layers.

The last model I worked on was the Decision Tree originally made by Holly. This time we had a model around the 69% accuracy mark and I was tasked with tuning the parameters to see if I 
could create a model with better accuracy. I again returned to google for help in this situation and found a lot of information about changing parameters for a Decision Tree Classifier. 
The first step I did was try default settings, with machine learning if you don't specify none or default settings it wont use them to help optimize. After doing this the accuracy still
only increased to around like 75%. So the next step I took was to look at the max features, like I did for the random forest classifier. This time i decided to look at the max depth of the
trees.The max depth was set to 2, which only allows for 2 branches to be made from each tree so I decided to also change that to default which is none, allowing for each tree to make as many
branches that it needed, this increased the accuracy to our final percentage of 83%. The picture in the back is the actual decision tree model that was created that has 83% accuracy, you can 
also see that the tuning to the model in the code block is all none/default, helping optimize the model.
